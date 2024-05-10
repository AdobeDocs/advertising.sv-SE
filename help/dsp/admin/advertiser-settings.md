---
title: Kontoinställningar för Advertiser
description: Se beskrivningar av tillgängliga inställningar för annonsörer.
role: User, Admin
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Kontoinställningar för Advertiser

*Inte tillgängligt för skrivskyddade användare*

## [!UICONTROL General] Inställningar

**[!UICONTROL Advertiser Name]:** Annonsörens namn.

**[!UICONTROL Category]:** Den kategori som annonsören bedriver verksamhet i. Kategorin meddelas utgivarna när ni lägger bud på lager. Se till att du väljer en kategori som passar dina annonser, eller så kan utgivare avvisa dina annonser.

>[!NOTE]
>
>Om du väljer *[!UICONTROL Other]*, kan annonsören inte komma åt DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Annonsörens hemsida eller webbplats-URL (börjar med `http://` eller `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Endast nya annonskonton) Gör alla privata utbytesflöden som har konfigurerats för organisationens DSP tillgängliga för annonsören.

### [!UICONTROL Adobe IMS IDs]

Annonsörer med andra Adobe Experience Cloud-produkter kan dela data mellan vissa produkter med hjälp av organisationens unika ID för Experience Cloud. Du kan konfigurera specifika produktintegreringar i [!UICONTROL Integrations] -avsnitt.

**[!UICONTROL Account IMS org and ID]:** (Annonsörer med ytterligare Experience Cloud-produkter som licensieras via ett Experience Cloud-konto hos flera annonsörer; valfritt) Annonsörens Experience Cloud-organisations-ID.

**[!UICONTROL Advertiser IMS org and ID]:** (Annonsörer med direktlicenser för ytterligare Experience Cloud-produkter; valfritt) Annonsörens organisation-ID för Experience Cloud.

### [!UICONTROL Integrations]

(Valfritt) Ytterligare Experience Cloud-produkter som är kopplade till DSP konto. Produkterna måste vara kopplade till samma Experience Cloud-organisations-ID som anges i [!UICONTROL Adobe IMS IDs] -avsnitt.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Annonsörer med [!DNL Advertising Search, Social, & Commerce] eller som använder konverteringspixlar för Adobe Advertising) A [!DNL Search, Social, & Commerce] vilket konto som DSP utbyter attribueringsdata med.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Annonsörer med Adobe Analytics; valfritt; endast tillgängligt för data som samlats in med hjälp av Adobe Advertising-konverteringstaggar som innehåller en [!DNL EF Redirect] och endast token) en eller flera [!DNL Analytics] rapportera programsviter till vilka DSP skickar in data från utgivare och leverantörer. Analytics skickar också de data som samlas in från kundens webbplats till DSP.

För att data ska visas i rapportsviterna bör [!DNL Search, Social, & Commerce] Inställningar på annonsörnivå måste aktiveras. Dessutom har annonsören [!DNL Analytics] kontot måste vara konfigurerat för att ta emot data från Adobe Advertising.

>[!WARNING]
>
>Om du tar bort en tidigare länkad rapportsvit utbyter DSP inte längre data med den sviten. Förvänta dig att se fluktuationer i data.

Mer information om integrationen med [!DNL Analytics], se &quot;[Översikt [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Advertisers with Adobe Audience Manager or Adobe Analytics; optional) An Audience Manager or [!DNL Analytics] vilket konto som DSP hämtar in segmentmetadata, hierarkidata och unika målgruppsdata för alla annonsörernas Adobe-målgrupper. Detta inkluderar data för:

* Audience Manager segment
* [!DNL Analytics] segment som publiceras till Adobe Experience Cloud
* Segment som har skapats med Adobe Experience Cloud [!DNL Audience Library]
* Segment som har skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager

Den första synkroniseringen tar ca 24 timmar. Efter det synkroniseras data i realtid med en fördröjning på en till två sekunder.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Inställningar

Du kan också konfigurera standardmål för annonserarens nya placeringar. Användarna kan åsidosätta standardmålen för alla nya placeringar.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Standardlandet för varje placering för geografisk inriktning. Användarna kan ändra land och konfigurera mer specifik geoanpassning för varje placering.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Alla målgrupper eller segment som ska undertryckas som standard. Användarna kan ändra undantagen för varje placering.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Typer av [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39] kontextuella filter som ska användas. Du kan åsidosätta inställningarna på annonsörsnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerkontext som ska blockeras som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Valfritt) En eller flera typer av lagerattribut att rikta som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerattribut att blockera som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Valfritt) Graden av vuxeninnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Alcohol Content]:** (Valfritt) Den alkoholhalt som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Typer av webbplatser som ska blockeras baserat på bedräglig trafik och misstänkta aktiviteter som mäts via [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39]. Du kan åsidosätta inställningarna på annonsörsnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Som standard blockeras all 100 % ogiltig trafik, inklusive trafik på kapade enheter, för nya placeringar. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Also block sites with]:** (Valfritt) Ytterligare en nivå av bedrägeri och ogiltig trafik som gör att DSP blockerar annonser som standard:  *[!UICONTROL None]* (standard, som inte blockerar ytterligare trafik), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, eller *[!UICONTROL >25% Average Fraud/IVT levels]*. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av bedrägeri som får DSP att blockera annonser som standard: *[!UICONTROL Fraud]* (som blockerar alla webbplatser med bedrägeri), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* och/eller *[!UICONTROL Fraud: Zero Ads]*. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Valfritt) En typ av misstänkt webbplats- eller appaktivitet som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar annonser som baseras på misstänkt aktivitet), *[!UICONTROL Suspicious Activity - High Risk]*, eller *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Ytterligare avgifter kan tillkomma.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Som standard är [[!DNL Ads.txt] filtrering före bud](https://iabtechlab.com/ads-txt-about/) att använda genom att utnyttja varje utgivares [!DNL Authorized Digital Sellers] lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: För att köpa lager från alla säljare.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Att prioritera inköp av lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare.

Du kan åsidosätta inställningen på annonsörnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Som standard aktiveras ett postbud-filter i realtid för att säkerställa att annonserna fungerar på de webbplatser som annonsören riktar sig mot. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] endast kunder (valfritt) Det varumärkessäkerhetssegment-ID som är kopplat till organisationens [!DNL DoubleVerify] konto.

**[!UICONTROL Enable Authentic Brand Safety]:** (Valfritt) Som standard aktiveras [!DNL DoubleVerify] Autentiell varumärkessäkerhet, som blockerar visningar efter bud med hjälp av anpassade varumärkessäkerhetsregler som konfigurerats för det angivna segment-ID:t. DSP fakturerar ditt konto för användning av segment-ID.

Du kan åsidosätta inställningen på annonsörnivå på placeringsnivån.

>[!MORELIKETHIS]
>
>* [Skapa ett Advertiser-konto](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
