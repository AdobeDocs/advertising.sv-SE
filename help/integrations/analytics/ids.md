---
title: Adobe Advertising ID som används av  [!DNL Analytics]
description: Adobe Advertising ID som används av  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 8128a29a044623d5161e4893fbc52cca626b8fe4
workflow-type: tm+mt
source-wordcount: '1731'
ht-degree: 0%

---

# Adobe Advertising ID som används av [!DNL Analytics]

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

*Gäller för Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising använder två ID:n för prestandaspårning på plats: *EF ID* och *AMO ID*.

När ett annonsintryck inträffar skapar Adobe Advertising värdena för AMO-ID och EF-ID och lagrar dem. När en besökare som har sett en annons komma in på webbplatsen utan att klicka på en annons, anropar [!DNL Analytics] dessa värden från Adobe Advertising via JavaScript-koden [!DNL Analytics for Advertising]. För genomsynstrafik genererar [!DNL Analytics] ett extra ID (`SDID`) som används för att sammanfoga EF-ID och AMO-ID till [!DNL Analytics]. För genomklickningstrafik inkluderas dessa ID:n i landningssidans URL med hjälp av frågesträngsparametrarna `ef_id` och `s_kwcid` (för AMO ID).

Adobe Advertising skiljer mellan klickbara eller genomskinliga poster på webbplatsen enligt följande kriterier:

* En genomsiktspost hämtas när en användare besöker webbplatsen efter att ha visat en annons, men inte klickat på den. [!DNL Analytics] spelar in en genomgång om två villkor uppfylls:

   * Besökaren har inga klickningar för en [!DNL DSP] eller [!DNL Search, Social, & Commerce] annons under [klickningsfönstret](#lookback-a4adc).

   * Besökaren har sett minst en [!DNL DSP] annons under [visningsfönstret](#lookback-a4adc). Det sista intrycket skickas som en genomgång.

* En klickbar post hämtas när en besökare klickar på en annons innan han/hon kommer in på webbplatsen. [!DNL Analytics] hämtar en klickfrekvens när något av följande inträffar:

   * URL:en innehåller ett EF-ID och AMO-ID som har lagts till i Adobe Advertising-URL:en för landningssidan.

   * URL:en innehåller inga spårningskoder, men Adobe Advertising JavaScript-koden hittar ett klick under de senaste två minuterna.

![Adobe Advertising vybaserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figur 1: Adobe Advertising vybaserad [!DNL Analytics] integrering*

![Adobe Advertising klickar på URL-baserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figur 2: Adobe Advertising klickar på URL-baserad [!DNL Analytics] integrering*

## Adobe Advertising EF ID:n

EF ID är en unik variabel som Adobe Advertising använder för att koppla aktiviteter till en onlineklickning eller annonsexponering. EF-id:t lagras i dimensionen [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller [!DNL rVar] (reserverad [!DNL eVar]) (Adobe Advertising EF-id) och spårar varje annons som klickas eller exponeras på den enskilda webbläsaren eller enheten. EF ID:n fungerar främst som nycklar för att skicka [!DNL Analytics]-data till Adobe Advertising för rapportering och budoptimering inom Adobe Advertising.

### EF ID-format

>[!NOTE]
>
>EF ID:n är skiftlägeskänsliga. Om en [!DNL Analytics]-implementering tvingar URL-spårning till gemener, känner Adobe Advertising inte igen EF-ID:t. Detta påverkar Adobe Advertising budgivning och rapportering men påverkar inte Adobe Advertising-rapportering inom [!DNL Analytics].

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

* &lt;*Adobe Advertising besökar-ID*> är ett unikt ID per besökare (till exempel EhKVaAABCkJ0mDt). Kallas även *surfer-ID*.

* &lt;*timestamp*> är tiden i formatet YYYYMMDDHMMSS (till exempel 20190821192533 för År 2019, Month 08, Day 21, Time 19:25:33).

* &lt;*kanaltyp*> är den kanaltyp som ansvarar för klickningen eller exponeringen:

   * `d` för en klickning på en DSP-displayannons (visa klickfrekvens)
   * `i` om du vill se en visningsannons från DSP (visa-genomgång)
   * `s` om du vill ha en klickning på en sökannons (sökklickning).

Exempel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### EF ID Dimension i [!DNL Analytics]

I [!DNL Analytics]-rapporter kan du hitta EF ID-data genom att söka efter dimensionen [!UICONTROL EF ID] och använda måttet [!UICONTROL EF ID Instance].

EF ID:n omfattas av den unika identifierargränsen på 500 kB i Analysis Workspace. När 500 kB-värdet har nåtts rapporteras alla nya spårningskoder under rubriken [!UICONTROL Low Traffic] för radartikel. Eftersom det är möjligt att rapportens följsamhet saknas klassificeras inte dessa ID:n, och du bör inte använda dem för segment eller rapportering i [!DNL Analytics].

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO-ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för [!DNL Analytics]-dataklassificering och förtäring av reklamstatistik (t.ex. visningar, klick och kostnader) från Adobe Advertising. AMO-ID:t lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) - eller rVar-dimension (AMO-ID) och används exklusivt för rapportering i [!DNL Analytics].

AMO-ID:t kallas även `s_kwcid`, som ibland uttalas som [!DNL squid].

### Sätt att implementera AMO-ID {#amo-id-implement}

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) När infogningsfunktionen på serversidan implementeras.

   * DSP-kunder: Pixelservern lägger automatiskt till parametern s_kwcid i landningssidans suffix när en användare tittar på en displayannons med Adobe Advertising pixel.

   * Sök-, sociala och Commerce-kunder:

      * För [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton med inställningen [!UICONTROL Auto Upload] aktiverad för kontot eller kampanjen, lägger pixelservern automatiskt till parametern s_kwcid i landningssidans suffix när en slutanvändare klickar på en annons med Adobe Advertising pixel.

      * För andra annonsnätverk, eller för [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton med inställningen [!UICONTROL Auto Upload] inaktiverad, lägger du manuellt till parametern i [på kontonivå-tilläggsparametrarna](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den till dina bas-URL:er.

* När infogningsfunktionen på serversidan inte är implementerad:

   * DSP-kunder: I [JavaScript-koden](javascript.md) registreras klickningar och genomgångar automatiskt. När en webbläsare inte stöder cookies från tredje part kan du fortfarande spåra klickbaserade konverteringar för följande annonstyper:

      * För [!DNL Flashtalking]-annonstaggar infogar du ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] makron till [!DNL Flashtalking] Lägg till taggar](/help/integrations/analytics/macros-flashtalking.md)&quot;.

      * För [!DNL Google Campaign Manager 360]-annonstaggar infogar du ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] makron till [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;.

   * Sök-, sociala och Commerce-kunder:

      * För annonser ([!DNL Google Ads] och [!DNL Microsoft Advertising]) lägger du manuellt till parametern AMO ID i landningssidans suffix, helst på [kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, såvida inte olika spårning för enskilda kontokomponenter krävs.

      * För annonser i alla andra annonsnätverk lägger du till AMO ID-parametern manuellt i [tilläggsparametrarna på kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den i dina bas-URL:er.

Om du vill implementera infogningsfunktionen på serversidan, eller fastställa det bästa alternativet för ditt företag, pratar du med ditt Adobe-kontoteam.

### AMO ID-format {#amo-id-formats}

#### AMO ID-format för [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

där:

* `AC` anger visningskanalen.

* `{TM_AD_ID}` är den Adobe Advertising-genererade alfanumeriska annonstangenten. Den används som en unik identifierare för en annons och fungerar som en nyckel för översättning av Adobe Advertising-entitetsmetadata till läsbara [!DNL Analytics]-dimensioner.

* `{TM_PLACEMENT_ID}` är den Adobe Advertising-genererade alfanumeriska placeringsnyckeln. Den används som en unik identifierare för en placering och fungerar som en nyckel för översättning av Adobe Advertising-entitetsmetadata till läsbara [!DNL Analytics]-dimensioner.

Exempel på AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID-format för sök-, sociala och Commerce-annonser {#amo-id-format-search}

Parametrarna varierar beroende på annonsnätverk, men följande parametrar är gemensamma för alla:

* `AL` anger sökkanalen. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` är ett unikt användar-ID som tilldelats annonsören.

* `{sid}` ersätts med det numeriska ID:t för annonserarens annonsnätverkskonto: ** för [!DNL Google Ads], ***för [!DNL Microsoft Advertising],* 45 *för [!DNL Meta], 86* för [!DNL Yahoo! Display Network], *87* för [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (utgått) eller *106*  för [!DNL Pinterest] (borttagen).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{placement}` är den webbplats där annonsen klickades.
* `{keywordid}` är annonsnätverkets unika numeriska ID för nyckelordet som utlöste annonsen.

##### [!DNL Google Ads]

Detta inkluderar shoppingkampanjer som använder [!DNL Google Merchant Center].

* Konton som använder det senaste AMO ID-formatet, som har stöd för kampanjrapportering och rapportering på annonsnivå för maximala prestandakampanjer samt utkast och experimentkampanjer:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alla andra konton:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

där:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` är det [!DNL Google Ads] unika numeriska ID:t för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `e` för exakt, `p` för fras eller `b` för bred.
* `{placement}` är domännamnet för den webbplats där annonsen klickades. Det finns ett värde för annonser i riktade kampanjer och för annonser i kampanjer riktade mot nyckelord som visas på innehållswebbplatser.
* `{network}` anger nätverket som klickningen inträffade från: `g` för [!DNL Google]-sökning (endast för nyckelordsriktade annonser), `s` för en sökpartner (endast för nyckelordsriktade annonser) eller `d` för visningsnätverket (antingen för nyckelordsriktade eller placeringsriktade annonser).
* `{product_partition_id}` är annonsnätverkets unika numeriska ID för produktgruppen som används med produktannonser.
* `{keyword}` är antingen det specifika nyckelord som utlöste din annons (på sökwebbplatser) eller det bästa matchande nyckelordet (på innehållswebbplatser).
* `{campaignid}` är annonsnätverkets unika numeriska ID för kampanjen.
* `{adgroupid}` är annonsnätverkets unika numeriska ID för annonsgruppen.

>[!NOTE]
>
>* För dynamiska sökannonser har {keyword} fyllts i med det automatiska målet.
>* När du genererar spårning för [!DNL Google] shoppingannonser infogas en produkt-ID-parameter, `{adwords_producttargetid}`, före nyckelordsparametern. Produkt-ID-parametern visas inte i parametrarna [!DNL Google Ads] på kontonivå och kampanjnivå.
>* Information om hur du använder den senaste spårningskoden för AMO-ID finns i [Uppdatera spårningskoden för AMO-ID för ett [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md). <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Alla kampanjtyper:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

där:

* `{AdId}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{OrderItemId}` är annonsnätverkets numeriska ID för nyckelordet.
* `{CampaignId}` är annonsnätverkets unika numeriska ID för kampanjen.
* `{AdGroupId}` är annonsnätverkets unika numeriska ID för annonsgruppen.

>[!NOTE]
>
> För konton med kampanjer utan alternativet [!UICONTROL Auto Upload] för spårning som inte redan har migrerats till det nya formatet måste du manuellt uppdatera varje landningssidesuffix så att det innehåller ovanstående format.
>Under tiden fungerar de äldre formaten enligt följande:
>* Sökkampanjer:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shoppingkampanjer (med [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Målgruppskampanjer:
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `be` för exakt, `bp` för fras eller `bb` för bred.
* `{network}` anger nätverket som klickningen inträffade från: `n` för internt eller `s` för sökning.
* `{keyword}` är nyckelordet som utlöste din annons.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

där:

* `{ad_id}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{source_type}` är den typ av webbplats där annonsen har visats: *b* för sökning, *c* för kontext (innehåll) eller *ct* för kategori.
* `{phrase_id}` är annonsnätverkets numeriska ID för nyckelordet.

### AMO ID Dimension i [!DNL Analytics]

I analysrapporter kan du hitta AMO ID-data genom att söka efter dimensionen [!UICONTROL AMO ID] och använda måttet [!UICONTROL AMO ID Instances]. Dimensionen [!UICONTROL AMO ID] lagrar alla infångade AMO ID-värden, medan måttet [!UICONTROL AMO ID Instances] anger hur ofta ett AMO ID-värde hämtades av webbplatsen. Om till exempel samma sökannons klickades fyra gånger men Analytics spårade sju webbplatsposter, skulle [!UICONTROL AMO ID Instances] vara sju (7) och [!UICONTROL Clicks] skulle vara fyra (4).

För alla rapporter och granskningar inom [!DNL Analytics] är det bästa sättet att använda AMO-ID tillsammans med motsvarande instans. Mer information finns i &quot;[Genomklickningsdataverifiering för [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; i &quot;Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising&quot;.

## Om analysklassificeringar

I [!DNL Analytics] är en [klassificering](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) en del metadata för en viss spårningskod, till exempel Konto, Kampanj eller Annons. Adobe Advertising kategoriserar Adobe Advertising-rådata med hjälp av klassificeringar så att du kan visa data på olika sätt (t.ex. efter annonstyp eller Campaign) när du genererar rapporter. Klassificeringar utgör grunden för Adobe Advertising-rapportering i [!DNL Analytics] och kan användas med AMO-mått, som [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] och [!UICONTROL AMO Clicks], samt med anpassade och standardbaserade händelser på plats som [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] och [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
