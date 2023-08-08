---
title: Adobe Advertising-ID som används av [!DNL Analytics]
description: Adobe Advertising-ID som används av [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Adobe Advertising-ID som används av [!DNL Analytics]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*Gäller DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising använder två ID:n för prestandaspårning på plats: *EF ID* och *AMO-ID*.

När ett annonsintryck inträffar skapar Adobe Advertising värdena för AMO ID och EF ID och lagrar dem. När en besökare som har sett en annons komma in på webbplatsen utan att klicka på en annons, [!DNL Analytics] anropar dessa värden från Adobe Advertising via [!DNL Analytics for Advertising] JavaScript-kod. För genomskinlig trafik [!DNL Analytics] genererar ett extra ID (`SDID`), som används för att sammanfoga EES ID och AMO ID till [!DNL Analytics]. För genomklickningstrafik inkluderas dessa ID:n i landningssidans URL med hjälp av `s_kwcid` och `ef_id` frågesträngparametrar.

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

#### Microsoft Advertising search ads

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

## Adobe Advertising AMO-ID

AMO ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för [!DNL Analytics] dataklassificering och konsumtion av annonsstatistik (t.ex. visningar, klickningar och kostnader) från Adobe Advertising. AMO-ID:t lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller rVar dimension (AMO ID) och används exklusivt för rapportering i [!DNL Analytics].

AMO-ID:t kallas även `s_kwcid`, som ibland uttalas som[!DNL the squid].&quot;

### AMO ID-format för [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

där:

* &lt;*Kanal-ID*> kan vara:

   * `AC` = DSP
   * `AL` for [!DNL Advertising Search, Social, & Commerce]

* &lt;*Annons-ID*> används en Adobe Advertising-genererad unik identifierare för en annons. Det fungerar som en nyckel för översättning av Adobe Advertising-entitetsmetadata till läsbara [!DNL Analytics] dimensioner.

* &lt;*Placement-ID*> är en Adobe Advertising-genererad unik identifierare för en placering. Det fungerar som en nyckel för översättning av Adobe Advertising-entitetsmetadata till läsbara [!DNL Analytics] dimensioner.

Exempel på AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO ID-format för [!DNL Search, Social, & Commerce]

AMO-ID:n för [!DNL Search, Social, & Commerce] följer ett distinkt format för varje sökmotor. Formatet för alla sökmotorer börjar med följande:

```
AL!{userid}!{sid}
```

där:

* `AL` är kanal-ID:t för annonsnätverket.
* `{userid}` är det unika numeriska användar-ID som Adobe Advertising tilldelar annonsören.
* `{sid}` är det numeriska ID som Adobe Advertising använder för det angivna annonsnätverket, till exempel `3` for [!DNL Google Ads] eller `10` for [!DNL Microsoft Advertising].

Nedan följer de fullständiga AMO ID-formaten för ett par annonsnätverk. Om du vill ha AMO ID-format för andra annonsnätverk kontaktar du kontoteamet på Adobe.

AMO ID-format för [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

där:

* `{creative}` är [!DNL Google Ads] unikt numeriskt ID för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `e` för exakta, `p` för fras, eller `b` för breda.
* `{placement}` är domännamnet för den webbplats där annonsen klickades. Det finns ett värde för annonser i riktade kampanjer och för annonser i kampanjer riktade mot nyckelord som visas på innehållswebbplatser.
* `{network}` anger nätverket som klickningen inträffade från:  `g` for [!DNL Google] sökning (endast för annonser riktade mot nyckelord), `s` för en sökpartner (endast för annonser riktade till nyckelord), eller `d` för Display Network (för antingen nyckelordsriktade eller placeringsriktade annonser).
* `{keyword}` är antingen det specifika nyckelord som utlöste din annons (på sökwebbplatser) eller det bästa matchande nyckelordet (på innehållswebbplatser).

AMO ID-format för [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

där:

* `{AdId}` är [!DNL Microsoft Advertising] unikt numeriskt ID för den kreativa.
* `{OrderItemId}` är [!DNL Microsoft Advertising] numeriskt ID för nyckelordet.

### AMO ID-Dimension i [!DNL Analytics]

I analysrapporter kan du söka efter AMO ID-data genom att söka efter [!UICONTROL AMO ID] -dimensionen och använda [!UICONTROL AMO ID Instance] mätvärden. The [!UICONTROL AMO ID] dimensioner innehåller alla värden för AMO ID, medan [!UICONTROL AMO ID Instance] anger hur ofta ett AMO ID-värde hämtades av platsen. Om användaren till exempel klickade fyra gånger på samma sökannons men Analytics spårade sju webbplatsposter, kommer [!UICONTROL AMO ID Instance] skulle vara sju (7) och [!UICONTROL Clicks] skulle vara fyra (4).

För rapportering och revision inom [!DNL Analytics]är det bästa sättet att använda AMO-ID tillsammans med motsvarande instans. Mer information finns i &quot;[Dataverifiering för [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; i &quot;Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising.&quot;

## Om analysklassificeringar

I [!DNL Analytics], a [klassificering](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) är en del metadata för en viss spårningskod, till exempel Konto, Kampanj eller Annons. Adobe Advertising kategoriserar rådata i Adobe Advertising med hjälp av klassificeringar så att du kan visa data på olika sätt (t.ex. efter annonstyp eller Campaign) när du genererar rapporter. Klassificeringar utgör grunden för Adobe Advertising rapportering i [!DNL Analytics] och kan användas med AMO-värden, som [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]och [!UICONTROL AMO Clicks], liksom med anpassade och standardiserade händelser på plats som [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]och [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
