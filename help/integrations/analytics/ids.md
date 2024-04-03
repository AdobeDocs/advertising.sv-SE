---
title: Adobe Advertising-ID som används av [!DNL Analytics]
description: Adobe Advertising-ID som används av [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 9374f5ef6aaff1f638022bc878c7af190e31888f
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# Adobe Advertising-ID som används av [!DNL Analytics]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*Gäller DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising använder två ID:n för prestandaspårning på plats: *EF ID* och *AMO-ID*.

När ett annonsintryck inträffar skapar Adobe Advertising värdena för AMO ID och EF ID och lagrar dem. När en besökare som har sett en annons komma in på webbplatsen utan att klicka på en annons, [!DNL Analytics] anropar dessa värden från Adobe Advertising via [!DNL Analytics for Advertising] JavaScript-kod. För genomskinlig trafik [!DNL Analytics] genererar ett extra ID (`SDID`), som används för att sammanfoga EES ID och AMO ID till [!DNL Analytics]. För genomklickningstrafik inkluderas dessa ID:n i landningssidans URL med hjälp av `ef_id` och `s_kwcid` (för AMO ID) frågesträngsparametrar.

Adobe Advertising skiljer mellan klicknings- och vyposter på webbplatsen enligt följande kriterier:

* En genomsiktspost hämtas när en användare besöker webbplatsen efter att ha visat en annons, men inte klickat på den. [!DNL Analytics] spelar in en genomskinlig vy om två villkor uppfylls:

   * Besökaren har ingen klickfrekvens för en [!DNL DSP] eller [!DNL Search, Social, & Commerce] under [klicka på uppslagsfönstret](#lookback-a4adc).

   * Besökaren har sett minst en [!DNL DSP] under [visningsfönster](#lookback-a4adc). Det sista intrycket skickas som en genomgång.

* En klickbar post hämtas när en besökare klickar på en annons innan han/hon kommer in på webbplatsen. [!DNL Analytics] hämtar en klickning genom när något av följande inträffar:

   * URL:en innehåller ett EF-ID och AMO-ID som Adobe Advertising har lagt till i landningssidans URL.

   * URL:en innehåller inga spårningskoder, men JavaScript-koden i Adobe Advertising identifierar ett klick inom de senaste två minuterna.

![Adobe Advertising vybaserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Bild 1: Visningsbaserad i Adobe Advertising [!DNL Analytics] integration*

![Adobe Advertising-klicka på URL-baserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Bild 2: Adobe Advertising-klicka på URL-baserad [!DNL Analytics] integration*

## ADOBE ADVERTISING EF ID

EF ID är en unik variabel som Adobe Advertising använder för att koppla aktiviteter till en onlineklickning eller annonsexponering. EF-ID:t lagras i [en [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller [!DNL rVar] (reserverad [!DNL eVar]) dimension (Adobe Advertising EF ID) och spårar varje annons som klickas eller exponeras på den enskilda webbläsarens eller enhetens nivå. EF ID fungerar i första hand som nycklar för att skicka [!DNL Analytics] data till Adobe Advertising för rapportering och budoptimering inom Adobe Advertising.

### EF ID-format

>[!NOTE]
>
>EF ID:n är skiftlägeskänsliga. Om en [!DNL Analytics] implementeringen tvingar URL-spårning till gemener, så kommer Adobe Advertising inte att känna igen EF-ID:t. Detta påverkar Adobe Advertising budgivning och rapportering men påverkar inte Adobe Advertising rapportering inom [!DNL Analytics].

#### [!DNL Google Ads] sökannonser

```
{gclid}:G:s
```

där:

* `gclid` är [!DNL Google Click ID] (GCLID).
* `s` är nätverkstypen (&quot;s&quot; för sökning).

#### [!DNL Microsoft Advertising] sökannonser

```
{msclkid}:G:s
```

där:

* `msclkid` är [!DNL Microsoft Click ID] (MSCLKID).
* `s` är nätverkstypen (&quot;s&quot; för sökning).

#### Visa annonser och sökannonser i andra sökmotorer

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

där:

* &lt;*Adobe Advertising besökar-ID*> är ett unikt ID per besökare (till exempel EKVaAABCkJ0mDt). Kallas även *surfer-ID*.

* &lt;*tidsstämpel*> är tiden i formatet YYYMMDDHMMSS (t.ex. 20190821192533 för år 2019, månad 08, dag 21, tid 19):25:3).

* &lt;*kanaltyp*> är den kanaltyp som ansvarar för klickningen eller exponeringen:

   * `d` för ett klick på en DSP annons (visa klickfrekvens)
   * `i` för ett intryck av en DSP displayannons (visningsvy)
   * `s` för att klicka på en sökannons (sök-klickning).

Exempel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### EF ID-Dimensionen i [!DNL Analytics]

I [!DNL Analytics] rapporter kan du hitta data för EF ID genom att söka efter [!UICONTROL EF ID] -dimensionen och använda [!UICONTROL EF ID Instance] mätvärden.

EF ID:n omfattas av den unika identifierargränsen på 500 kB i Analysis Workspace. När 500 kB-värdet har uppnåtts rapporteras alla nya spårningskoder under rubriken&quot; på en rad[!UICONTROL Low Traffic].&quot; På grund av risken för att rapporteringsnoggrannheten saknas klassificeras inte dessa EF-ID:n, och du bör inte använda dem för segment eller rapportering i [!DNL Analytics].

## Adobe Advertising AMO-ID {#amo-id}

AMO ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för [!DNL Analytics] dataklassificering och konsumtion av annonsstatistik (t.ex. visningar, klickningar och kostnader) från Adobe Advertising. AMO-ID:t lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller rVar dimension (AMO ID) och används exklusivt för rapportering i [!DNL Analytics].

AMO-ID:t kallas även `s_kwcid`, som ibland uttalas som[!DNL the squid].&quot;

### Sätt att implementera AMO-ID {#amo-id-implement}

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) När infogningsfunktionen på serversidan implementeras.

   * DSP: Pixelservern lägger automatiskt till parametern s_kwcid i landningssidans suffix när en användare tittar på en displayannons med pixeln Adobe Advertising.

   * Kunder inom sökning, sociala medier och handel:

      * För [!DNL Google Ads] och [!DNL Microsoft® Advertising] konton med [!UICONTROL Auto Upload] om inställningen är aktiverad för kontot eller kampanjen lägger pixelservern automatiskt till parametern s_kwcid i landningssidans suffix när en slutanvändare klickar på en annons med Adobe Advertising.

      * för andra annonsnätverk, eller [!DNL Google Ads] och [!DNL Microsoft® Advertising] konton med [!UICONTROL Auto Upload] inställning inaktiverad, lägg till parametern manuellt i [tilläggsparametrar på kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den till dina bas-URL:er.

* När infogningsfunktionen på serversidan inte är implementerad:

   * DSP: [JavaScript-kod](javascript.md) registrerar automatiskt klickningar och genomgångar. När en webbläsare inte stöder cookies från tredje part kan du fortfarande spåra klickbaserade konverteringar för följande annonstyper:

      * För [!DNL Flashtalking] annonstaggar, infoga ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * För [!DNL Google Campaign Manager 360] annonstaggar, infoga ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Kunder inom sökning, sociala medier och handel:

      * För ([!DNL Google Ads] och [!DNL Microsoft® Advertising]), lägger du till AMO ID-parametern manuellt i landningssidans suffix, helst på sidan [kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} såvida inte olika spårning för enskilda kontokomponenter krävs.

      * För annonser i alla andra annonsnätverk lägger du manuellt till parametern AMO ID i [tilläggsparametrar på kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den till dina bas-URL:er.

Om du vill implementera infogningsfunktionen på serversidan eller fastställa det bästa alternativet för din verksamhet kan du tala med ditt Adobe-kontoteam.

### AMO ID-format {#amo-id-formats}

#### AMO ID-format för [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

där:

* `AC` anger visningskanalen.

* `{TM_AD_ID}` är den Adobe Advertising-genererade alfanumeriska annonstangenten. Den används som en unik identifierare för en annons och fungerar som en nyckel för att omvandla metadata för Adobe Advertising-entitet till läsbara [!DNL Analytics] dimensioner.

* `{TM_PLACEMENT_ID}` är den Adobe Advertising-genererade alfanumeriska placeringsnyckeln. Den används som en unik identifierare för en placering och fungerar som en nyckel för att omvandla metadata för Adobe Advertising-entitet till läsbara [!DNL Analytics] dimensioner.

Exempel på AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID-format för sök-, sociala och kommersiella annonser {#amo-id-format-search}

Parametrarna varierar beroende på annonsnätverk, men följande parametrar är gemensamma för alla:

* `AL` anger sökkanalen. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` är ett unikt användar-ID som tilldelats annonsören.

* `{sid}` ersätts med det numeriska ID:t för annonsören och annonsnätverkskontot: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (borttagen), eller *106* for [!DNL Pinterest] (föråldrat).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{placement}` är den webbplats där annonsen klickades.
* `{keywordid}` är annonsnätverkets unika numeriska ID för det nyckelord som utlöste annonsen.

##### [!DNL Google Ads]

Detta inkluderar shoppingkampanjer som använder [!DNL Google Merchant Center].

* Konton som använder det senaste AMO ID-formatet, som har stöd för kampanjrapportering och rapportering på annonsnivå för maximala prestandakampanjer samt utkast och experimentkampanjer:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alla andra konton:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

där:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` är [!DNL Google Ads] unikt numeriskt ID för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `e` för exakta, `p` för fras, eller `b` för breda.
* `{placement}` är domännamnet för den webbplats där annonsen klickades. Det finns ett värde för annonser i riktade kampanjer och för annonser i kampanjer riktade mot nyckelord som visas på innehållswebbplatser.
* `{network}` anger nätverket som klickningen inträffade från: `g` for [!DNL Google] sökning (endast för annonser riktade mot nyckelord), `s` för en sökpartner (endast för annonser riktade till nyckelord), eller `d` för visningsnätverket (för antingen nyckelordsriktade eller placeringsriktade annonser).
* `{product_partition_id}` är annonsnätverkets unika numeriska ID för produktgruppen som används med produktannonser.
* `{keyword}` är antingen det specifika nyckelord som utlöste din annons (på sökwebbplatser) eller det bästa matchande nyckelordet (på innehållswebbplatser).
* `{campaignid}` är annonsnätverkets unika numeriska ID för kampanjen.
* `{adgroupid}` är annonsnätverkets unika numeriska ID för annonsgruppen.

>[!NOTE]
>
>* För dynamiska sökannonser {keyword} fylls i med det automatiska målet.
>* När du genererar spårning för [!DNL Google] shoppingannonser, en produkt-ID-parameter, `{adwords_producttargetid}`infogas före nyckelordsparametern. Produkt-ID-parametern visas inte i [!DNL Google Ads] spårningsparametrar på kontonivå och kampanjnivå.
>* Information om hur du använder den senaste spårningskoden för AMO-ID finns i &quot;[Uppdatera spårningskoden för AMO ID för en [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Sökkampanjer:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Shoppingkampanjer (med [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Målgruppskampanjer:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

där:

* `{AdId}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{OrderItemId}` är annonsnätverkets numeriska ID för nyckelordet.
* `{CriterionId}` är annonsnätverkets numeriska ID för produktgruppen som används med produktannonser.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `be` för exakta, `bp` för fras, eller `bb` för breda.
* `{network}` anger nätverket som klickningen inträffade från: `n` för inbyggt eller `s` för sökning.
* `{keyword}` är nyckelordet som utlöste din annons.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

där:

* `{ad_id}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{source_type}` är den typ av webbplats där annonsen har visats: *b* för sökning, *c* för kontext (innehåll), eller *ct* för kategori.
* `{phrase_id}` är annonsnätverkets numeriska ID för nyckelordet.

### AMO ID-Dimension i [!DNL Analytics]

I analysrapporter kan du söka efter AMO ID-data genom att söka efter [!UICONTROL AMO ID] -dimensionen och använda [!UICONTROL AMO ID Instances] mätvärden. The [!UICONTROL AMO ID] dimensioner innehåller alla värden för AMO ID, medan [!UICONTROL AMO ID Instances] anger hur ofta ett AMO ID-värde hämtades av platsen. Om användaren till exempel klickade fyra gånger på samma sökannons men Analytics spårade sju webbplatsposter, kommer [!UICONTROL AMO ID Instances] skulle vara sju (7) och [!UICONTROL Clicks] skulle vara fyra (4).

För rapportering och revision inom [!DNL Analytics]är det bästa sättet att använda AMO-ID tillsammans med motsvarande instans. Mer information finns i &quot;[Klicka igenom dataverifiering för [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; i &quot;Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising.&quot;

## Om analysklassificeringar

I [!DNL Analytics], a [klassificering](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) är en del metadata för en viss spårningskod, till exempel Konto, Kampanj eller Annons. Adobe Advertising kategoriserar rådata i Adobe Advertising med hjälp av klassificeringar så att du kan visa data på olika sätt (t.ex. efter annonstyp eller Campaign) när du genererar rapporter. Klassificeringar utgör grunden för Adobe Advertising rapportering i [!DNL Analytics] och kan användas med AMO-värden, som [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions]och [!UICONTROL AMO Clicks], liksom med anpassade och standardiserade händelser på plats som [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]och [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
