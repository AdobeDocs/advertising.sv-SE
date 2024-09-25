---
title: Kampanjinställningar
description: Se beskrivningar av tillgängliga kampanjinställningar.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Kampanjinställningar

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Kampanjnamnet.

**[!UICONTROL Advertiser]:** (Skrivskyddad för befintliga kampanjer) Den tillämpliga annonseraren (varumärke). Välj en befintlig annonsör eller skapa en ny.

**[!UICONTROL Advertiser URL]:** Annonsörens officiella sida. Det här fältet snabbar upp er process för godkännande av annonser med lagerpartners.

**[!UICONTROL Timezone]:** (Skrivskyddad för befintliga kampanjer) Tidszonen för rapportering och budgivning.

**[!UICONTROL Customer PO]:** (Valfritt) En kundinköpsorder för insättningsordern/inköpsordern.

**[Kampanjdatum]:** Kampanjens start- och slutdatum.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Om marginaler ska hanteras för kampanjen: *[!UICONTROL Yes]* eller *[!UICONTROL No]* (standardvärdet).

När du väljer *[!UICONTROL Yes]anger* marginaltyp och belopp:

* **[!UICONTROL Margin Type]:** Marginaltypen. Du kan inte ändra marginaltypen när du har aktiverat marginalhantering och sparat kampanjen.

   * *[!UICONTROL Fixed]:* (standardvärdet) Tillåter DSP att beräkna automatiskt och sätta ändar baserat på en fast marginalprocent för [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Gör att du kan hantera marginaler ned till placeringsnivån genom att ange separata [!UICONTROL Budget Reserve %] och [!UICONTROL Gross Budget] för varje paket och placering i kampanjen. DSP optimerar utifrån varje placerings ekonomiska effektivitet, utan att garantera en viss marginal. Använd detta för infogningsorder som består av flera radobjekt för vilka du har godkänt att leverera ett fast antal enheter eller enhetstyper till en fast ränta.

* **[!UICONTROL Fixed Margin %]:** (Endast kampanjer med fasta marginaler) Standardkoden för varje infogningsordning <!-- impression? -->, i procent. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

* **[!UICONTROL Budget Reserve %]:** (Endast kampanjer med fasta marginaler, valfritt) Reserverar en angiven procentandel av [!UICONTROL Gross Budget] som en säkerhetslösning. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

**[!UICONTROL Gross Budget]:** (Endast kampanjer med marginalhantering) Bruttokampanjbudgeten, innan de angivna marginaljusteringarna tillämpas.

Du kan lägga till ytterligare en daglig, vecko- eller månadsbudget (brutto):

1. Klicka på **[!UICONTROL Add an additional Gross Budget]**.

1. Ange **[!UICONTROL Gross Budget]** och välj budgetintervallet: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* eller *[!UICONTROL Monthly]*.

Den totala nettobudgeten, som är utgiftstaket för kampanjen, beräknas automatiskt baserat på marginalinställningarna och anges under det här värdet.

**[!UICONTROL Budget]:** (kampanjer utan marginallösning) Den övergripande kampanjbudgeten.

**[!UICONTROL Estimated Tax Withholding]:** Innehåller en procentandel av de totala utgifterna över annonsavgifter, och servar avgifter och/eller datarån på kontonivån för nationella eller lokala skatter. Kurser är uppskattningar av budgeterings- och kostnadsredovisningsändamål, så de fakturerade skattesatserna kan variera.

Så här beräknar du källskatt:

1. Klicka på **[!UICONTROL Update rates here]**.

1. Ange **[!UICONTROL Estimated tax rate]** som en procentandel.

1. Markera kryssrutan bredvid varje avgiftstyp för vilken du vill hålla inne skatt. Avgiftstyperna är:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gäller alla utgifter för Advertising DSP-media, inklusive skatter på kampanjhanteringsavgifter.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gäller för alla utgifter på Advertising DSP utom för media och data. exklusive moms för kampanjhanteringsavgifter

   * *[!UICONTROL Include estimated tax - data fee]:* Gäller alla datatillgångar på Advertising DSP.

1. Klicka på **[!UICONTROL Submit]**.

>[!NOTE]
>
>* I USA kan olika länder ta med skatteavgifter i annonser, annonsservrar och data. För organisationer i andra länder ska alla tre kategorier av avgifter tas med i beräkningen av momsen.
>
>* Du kan också konfigurera dessa värden i kontots avgiftsinställningar.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Skrivskyddat för befintliga kampanjer som skapats sedan den 22 juni 2020, inte tillgängligt för kampanjer som skapats före den 22 juni 2020) Den nivå på vilken DSP annonserar och tillämpar frekvensomfång: *Samma enhet* för att rikta in en enhet eller *Personer* för att rikta en person över alla kända enheter. **Obs!** Stöd för flera enheter är inte tillgängligt för platser som har universella ID som mål.

**[!UICONTROL Device Graph]:** (Skrivskyddat för befintliga kampanjer, kampanjer med personbaserad målinriktning endast över enheter) Enhetsgrafen som ska användas för målinriktning mellan enheter och frekvenshantering:

* *[!UICONTROL LiveRamp - U.S. only]:* Tillgängligt för alla annonsörer för målinriktning mellan olika enheter på 0,35 CPM för visningar som levereras med hjälp av enhetsdiagrammet [!DNL LiveRamp] (det vill säga för enheter som inte hittas i målgruppssegmenten). Ni kan ange målinriktning mellan olika enheter på placeringsnivå.

  Det här alternativet är även tillgängligt för alla annonsörer, utan avgifter, för frekvenshantering och attribueringsmätning.

  Stöd för flera enheter gäller endast för placeringar som har äldre ID:n som mål, men inte för placeringar som har universella ID:n som mål (inklusive [!DNL LiveRamps]). Målinriktning, frekvenshantering och attribuering för universella ID:n används endast på ID-nivå.

**[!UICONTROL Frequency Cap]:** (Valfritt) Det antal gånger som en unik enhet, ett universellt ID eller en person (beroende på angiven [!UICONTROL Cross Device Level] och placeringens [!UICONTROL Targeting]-inställning) kan få annonser från kampanjen. Alternativen är *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Packages]:** De [paket](/help/dsp/campaign-management/packages/package-about.md) som ska inkluderas i kampanjen. Välj befintliga paket och/eller skapa paket som ska inkluderas. Om du skapar paket kan du läsa beskrivningar om [paketinställningarna](/help/dsp/campaign-management/packages/package-settings.md) för mer information.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Följande inställningar aktiverar endast mät- och rapporteringsfunktioner. Prestandaoptimering utförs endast på paket- och placeringsnivå.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Valfritt) Aktiverar [!DNL IAS] mätning och rapportering av visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Measure On]:** Det lager som ska mätas: *[!UICONTROL Display and VPAID video inventory]* (standard) eller *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >Videosynlighet kan endast mätas i VPAID-lager.

* **[!UICONTROL IAS Account ID (AnID)]:** (Annonsörer med egna [!DNL IAS]-konton; valfritt) Organisationens [!DNL IAS] konto-ID, som [!DNL IAS] debiterar direkt för användning.

* **[!UICONTROL IAS Team ID]:** (Advertisers with their own [!DNL IAS] accounts; optional) The team ID for the organization&#39;s [!DNL IAS] account, which [!DNL IAS] will Bill directly for usage. <!-- verify -->

#### Målgruppsverifiering

**[!UICONTROL Comscore Campaign Ratings]:** (Valfritt) Aktiverar [!DNL Comscore] verifierad [!DNL Campaign Ratings] mätning och rapportering av målgruppsverifiering med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Target Gender]:** Genus att ange som mål: *[!UICONTROL Both]* (standard), *[!UICONTROL Male]* eller *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Det åldersintervall som ska anges som mål. Använd vänster och höger skjutreglage för att minska intervallet efter behov.

* **[!UICONTROL Target Country]:** (valfritt) Ett land att rikta sig till. [!DNL Comscore] mäter endast exponeringar i länder som stöds.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Aktiverar spårning för mätvärdet för placeringsnivå [!UICONTROL Attention Score] (det viktade genomsnittliga antalet [!DNL Adelaide] [!DNL Attention Units] för alla visningar). Mätvärden är tillgängliga för alla placeringstyper förutom för [!DNL Roku] ansluten TV, förrullning endast för VPAID och ljud som inte är en poddsändning. DSP kopplar automatiskt en JavaScript-tagg till alla associerade kreatörer och [!DNL Adelaide] spårar exponeringsdata och skickar dem till DSP dagligen. Du kan använda datumet för att manuellt optimera dina utgifter mot placeringsstrategier med bättre resultat.

Fältet [!UICONTROL Attention Score] är tillgängligt i avsnittet [!UICONTROL Metrics] i rapporter, i vyerna [!UICONTROL Campaigns], [!UICONTROL Packages] och [!UICONTROL Placements] samt på flikarna [!UICONTROL Sites], [!UICONTROL Ads] och [!UICONTROL Inventory] i vyn [placeringsinformation](/help/dsp/campaign-management/reports/placement-details-view.md).

Om [!DNL Adelaide] segment används för mätning medför det en CPM-avgift för varje intryck som skickas från annonser med [!DNL Adelaide]-mätningstaggar. Avgiften är skild från avgifter för [målinriktning på placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Aktiverar förstahandsmätning och rapportering av visningsbarhet med hjälp av [!DNL IAB Open Video Viewability (OpenVV)] -tekniken, baserat på den angivna känslighetsnivån:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Om Campaign Management](campaign-about.md)
>* [Skapa en kampanj](campaign-create.md)
>* [Redigera en kampanj](campaign-edit.md)
>* [Visa ändringsloggen för en kampanj](campaign-change-log.md)
