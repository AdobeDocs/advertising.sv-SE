---
title: Kontoinställningar för Advertiser
description: Se beskrivningar av tillgängliga inställningar för annonsörer.
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Kontoinställningar för Advertiser

*Inte tillgängligt för skrivskyddade användare*

<!-- Not published -->

## Inställningar för [!UICONTROL General]

**[!UICONTROL Advertiser Name]:** Annonsörens namn.

**[!UICONTROL Category]:** Kategorin som annonsören arbetar i. Kategorin meddelas utgivarna när ni lägger bud på lager. Se till att du väljer en kategori som passar dina annonser, eller så kan utgivare avvisa dina annonser.

>[!NOTE]
>
>Om du väljer *[!UICONTROL Other]* kan annonsören inte komma åt DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Annonsörens hemsida eller webbplats-URL (med början `http://` eller `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Endast nya annonskonton) Gör alla privata utbytesfeeds som konfigurerats för organisationens DSP-konto tillgängliga för annonseraren.

### [!UICONTROL Adobe IMS IDs]

Annonsörer med andra Adobe Experience Cloud-produkter kan dela data mellan vissa produkter med hjälp av organisationens unika ID för Experience Cloud. Du kan konfigurera specifika produktintegreringar i avsnittet [!UICONTROL Integrations].

**[!UICONTROL Account IMS org and ID]:** (Advertisers with additional Experience Cloud products that are licensed through through an Experience Cloud account with multiple publishers; optional) The publish&#39;s Experience Cloud Organization ID.

**[!UICONTROL Advertiser IMS org and ID]:** (Annonsörer med direktlicenser för ytterligare Experience Cloud-produkter; valfritt) Annonsörens Experience Cloud organisations-ID.

### [!UICONTROL Integrations]

(Valfritt) Ytterligare Experience Cloud-produkter som är kopplade till DSP-kontot. Produkterna måste vara associerade med samma Experience Cloud-organisations-ID som anges i avsnittet [!UICONTROL Adobe IMS IDs].

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (annonsörer med [!DNL Advertising Search, Social, & Commerce] eller som använder Adobe Advertising-konverteringspixlar) Ett [!DNL Search, Social, & Commerce]-konto som DSP använder för att utbyta attributdata.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Advertisers with Adobe Analytics; optional; applicable only to data collect using using Adobe Advertising conversion tracking tags that include an [!DNL EF Redirect] and token only) One or more [!DNL Analytics] report suites to which DSP send data it collection from publishers and delivery-side partners. Analytics skickar också de data som samlas in från kundens webbplats till DSP.

För att data ska kunna visas i rapportsviterna måste rätt inställning på [!DNL Search, Social, & Commerce] annonsnivå aktiveras. Dessutom måste annonserarens [!DNL Analytics]-konto vara konfigurerat för att ta emot data från Adobe Advertising.

>[!WARNING]
>
>Om du tar bort en tidigare länkad rapportsvit utbyter DSP inte längre data med den sviten. Förvänta dig att se fluktuationer i data.

Mer information om integrationen med [!DNL Analytics] finns i [Översikt över  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (annonsörer med Adobe Audience Manager eller Adobe Analytics; valfritt) Ett Audience Manager- eller [!DNL Analytics]-konto som DSP hämtar in segmentmetadata, hierarkidata och unika målgruppsdata från för alla annonsörernas Adobe-målgrupper. Detta inkluderar data för:

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

## Inställningar för [!UICONTROL Targeting]

Du kan också konfigurera standardmål för annonserarens nya placeringar. Användarna kan åsidosätta standardmålen för alla nya placeringar.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Standardlandet för varje placerings geo-targeting. Användarna kan ändra land och konfigurera mer specifik geoanpassning för varje placering.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Alla målgrupper eller segment som ska undertryckas som standard. Användarna kan ändra undantagen för varje placering.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Typer av [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39] kontextfilter som ska användas. Du kan åsidosätta inställningarna på annonsörnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerkontext som ska blockeras som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Valfritt) En eller flera typer av lagerattribut att rikta som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerattribut att blockera som standard. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Valfritt) Graden av vuxeninnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]* eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Alcohol Content]:** (Valfritt) Den grad av alkoholinnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]* eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Typer av webbplatser som ska blockeras baserat på bedräglig trafik och misstänkta aktiviteter som mäts via [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39]. Du kan åsidosätta inställningarna på annonsörnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Som standard blockerar all 100 % ogiltig trafik, inklusive trafik på kapade enheter, för nya platser. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Also block sites with]:** (Valfritt) En extra nivå av bedrägeri och ogiltig trafik som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar ytterligare trafik), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* eller *[!UICONTROL >25% Average Fraud/IVT levels]*. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av bedrägeri som gör att DSP blockerar annonser som standard: *[!UICONTROL Fraud]* (som blockerar alla webbplatser med bedrägeri), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* och/eller *[!UICONTROL Fraud: Zero Ads]*. Ytterligare avgifter kan tillkomma.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Valfritt) En typ av misstänkt webbplats- eller appaktivitet som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar annonser baserat på misstänkt aktivitet), *[!UICONTROL Suspicious Activity - High Risk]* eller *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Ytterligare avgifter kan tillkomma.

#### [!UICONTROL Pre-Bid Viewability]

Valfria visningsfilter före bud av [!DNL DoubleVerify] och [!DNL Integral Ad Science] som ska användas på placeringar. Standardvärdena på annonsörnivå väljs för nya placeringar. Du kan åsidosätta inställningarna på annonsörnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**. Välj villkor med det här alternativet.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Välj villkor med det här alternativet.

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average player size composition is]**. Välj villkor med det här alternativet.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Visa

**&#x200B; **&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Välj villkor med det här alternativet.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Välj villkor med det här alternativet.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Ett valfritt **[!UICONTROL Video Viewability Targets]**-filter och ett valfritt **[!UICONTROL Display Viewability Targets]**-filter. Ytterligare avgifter kan tillkomma.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Som standard, vilken nivå av [[!DNL Ads.txt] föranbudsfiltrering](https://iabtechlab.com/ads-txt-about/) som ska användas genom att utnyttja varje utgivares [!DNL Authorized Digital Sellers]-lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: Om du vill köpa lager från alla säljare.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: För att prioritera inköp av lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Om du bara vill köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Om du bara vill köpa lager från en domäns auktoriserade direktförsäljare.

Du kan åsidosätta inställningen på annonsörnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Som standard aktiverar ett postbud-filter i realtid för att säkerställa att annonserna fungerar på de webbplatser som annonsören har som mål. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] enbart kunder; valfritt) Ett [!DNL DoubleVerify Authentic Brand Safety] segment-ID som är associerat med organisationens [!DNL DoubleVerify]-konto som ska användas som standard för alla ersättningar. Om du anger ett ID-block hämtas efter bud med hjälp av anpassade varumärkessäkerhetsregler som konfigurerats för det angivna segment-ID:t. DSP debiterar ditt konto för användning av segment-ID.

ID:t måste börja med &quot;51&quot; och bestå av åtta siffror. Du kan ändra eller ta bort annonsörnivå-ID på placeringsnivå.

>[!MORELIKETHIS]
>
>* [Skapa ett Advertiser-konto](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
