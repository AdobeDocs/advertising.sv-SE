---
title: Kampanjinställningar
description: Se beskrivningar av tillgängliga kampanjinställningar.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Kampanjinställningar

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Kampanjnamnet.

**[!UICONTROL Advertiser]:** (Skrivskyddat för befintliga kampanjer) Den tillämpliga annonseraren (varumärke). Välj en befintlig annonsör eller skapa en ny.

**[!UICONTROL Advertiser URL]:** Annonsörens officiella sida. Det här fältet snabbar upp er process för godkännande av annonser med lagerpartners.

**[!UICONTROL Timezone]:** (Skrivskyddat för befintliga kampanjer) Tidszonen för rapportering och budgivning.

**[!UICONTROL Customer PO]:** (Valfritt) En kundinköpsorder för infogningsordern/inköpsordern.

**[Kampanjdatum]:** Start- och slutdatum för kampanjen.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Om marginaler ska hanteras för kampanjen: *[!UICONTROL Yes]* eller *[!UICONTROL No]* (standard).

När du väljer *[!UICONTROL Yes],* ange marginaltyp och marginalbelopp:

* **[!UICONTROL Margin Type]:** Marginaltypen. Du kan inte ändra marginaltypen när du har aktiverat marginalhantering och sparat kampanjen.

   * *[!UICONTROL Fixed]:* (standard) Tillåter DSP att beräkna automatiskt och använda tak baserat på en fast marginalprocent av [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Gör att du kan hantera marginaler ned till placeringsnivån genom att ange en separat [!UICONTROL Budget Reserve %] och [!UICONTROL Gross Budget] för varje paket och placering i kampanjen. DSP optimerar utifrån varje placerings ekonomiska effektivitet, utan att garantera en viss marginal. Använd detta för infogningsorder som består av flera radobjekt för vilka du har godkänt att leverera ett fast antal enheter eller enhetstyper till en fast ränta.

* **[!UICONTROL Fixed Margin %]:** (Endast kampanjer med fasta marginaler) Standardkoden för varje infogningsorder <!-- impression? -->, som ett procenttal. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

* **[!UICONTROL Budget Reserve %]:** (Endast kampanjer med fasta marginaler, valfritt) Reserverar en angiven procentandel av [!UICONTROL Gross Budget] som skydd. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

**[!UICONTROL Gross Budget]:** (Endast kampanjer med marginalledning) Bruttokampanjbudgeten, innan de angivna marginaljusteringarna tillämpas.

Du kan lägga till ytterligare en daglig, vecko- eller månadsbudget (brutto):

1. Klicka på **[!UICONTROL Add an additional Gross Budget]**.

1. Ange **[!UICONTROL Gross Budget]** och välj budgetintervall: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* eller *[!UICONTROL Monthly]*.

Den totala nettobudgeten, som är utgiftstaket för kampanjen, beräknas automatiskt baserat på marginalinställningarna och anges under det här värdet.

**[!UICONTROL Budget]:** (Kampanjer utan marginalhantering) Den övergripande kampanjbudgeten.

**[!UICONTROL Estimated Tax Withholding]:** Innehåller en procentandel av de totala utgifterna över annonsavgifter, annonsavgifter och/eller dataavgifter på kontonivån för nationella eller lokala skatter. Kurser är uppskattningar av budgeterings- och kostnadsredovisningsändamål, så de fakturerade skattesatserna kan variera.

Så här beräknar du källskatt:

1. Klicka på **[!UICONTROL Update rates here]**.

1. Ange **[!UICONTROL Estimated tax rate]**, som ett procenttal.

1. Markera kryssrutan bredvid varje avgiftstyp för vilken du vill hålla inne skatt. Avgiftstyperna är:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gäller alla utgifter för annonsering DSP media, inklusive skatter på kampanjhanteringsavgifter.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gäller för alla utgifter för DSP med annonsering utom för media och data. exklusive moms för kampanjhanteringsavgifter

   * *[!UICONTROL Include estimated tax - data fee]:* Gäller för alla datatillgångar för DSP.

1. Klicka på **[!UICONTROL Submit]**.

>[!NOTE]
>
>* I USA kan olika länder ta med skatteavgifter i annonser, annonsservrar och data. För organisationer i andra länder ska alla tre kategorier av avgifter tas med i beräkningen av momsen.
>
>* Du kan också konfigurera dessa värden i kontots avgiftsinställningar.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Skrivskyddat för befintliga kampanjer som skapats sedan den 22 juni 2020, inte tillgängligt för kampanjer som skapats före den 22 juni 2020) Den nivå på vilken DSP avser annonser och tillämpar frekvensgränser: *Samma enhet* för en enhet eller *Folk* för att rikta sig till en person på alla deras kända enheter. **Obs!** Stöd för flera enheter är inte tillgängligt för placeringar som har universella ID som mål.

**[!UICONTROL Device Graph]:** (Skrivskyddat för befintliga kampanjer; kampanjer med personbaserad målinriktning över flera enheter) Det enhetsdiagram som ska användas för målinriktning mellan olika enheter och frekvenshantering:

* *[!UICONTROL LiveRamp - U.S. only]:* Tillgängligt för alla annonsörer för målinriktning mellan olika enheter på 0,35 CPM för visningar som levereras med [!DNL LiveRamp] enhetsdiagram (d.v.s. för enheter som inte hittas inom målgruppssegmenten). Ni kan ange målinriktning mellan olika enheter på placeringsnivå.

  Det här alternativet är även tillgängligt för alla annonsörer, utan avgifter, för frekvenshantering och attribueringsmätning.

  Stöd för flera enheter gäller endast för placeringar som har äldre ID:n som mål, men inte för placeringar som har universella ID:n som mål (inklusive [!DNL LiveRamps]). Målinriktning, frekvenshantering och attribuering för universella ID:n används endast på ID-nivå.

**[!UICONTROL Frequency Cap]:** (Valfritt) Antalet gånger som en unik enhet, ett universellt ID eller person (beroende på den angivna [!UICONTROL Cross Device Level] och placeringen [!UICONTROL Targeting] -inställning) kan användas för annonser från kampanjen. Alternativen inkluderar *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Packages]:** The [paket](/help/dsp/campaign-management/packages/package-about.md) som ska ingå i kampanjen. Välj befintliga paket och/eller skapa paket som ska inkluderas. Om du skapar paket läser du beskrivningar om [paketinställningar](/help/dsp/campaign-management/packages/package-settings.md) för mer information.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Följande inställningar aktiverar endast mät- och rapporteringsfunktioner. Prestandaoptimering utförs endast på paket- och placeringsnivå.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Valfritt) Aktiverar [!DNL IAS] mätning och rapportering av synlighet, bedrägeri, varumärkessäkerhet och målgruppsverifiering med angivna inställningar. Ytterligare avgifter tillkommer.

* **[!UICONTROL Measure On]:** Det lager som ska mätas: *[!UICONTROL Display and VPAID video inventory]* (standard) eller *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >Videosynlighet kan endast mätas i VPAID-lager.

* **[!UICONTROL IAS Account ID (AnID)]:** (Advertisers with their own [!DNL IAS] konton; valfritt) Organisationens [!DNL IAS] konto-ID, som [!DNL IAS] fakturerar direkt för användning.

* **[!UICONTROL IAS Team ID]:** (Advertisers with their own [!DNL IAS] (valfritt) ID för team för organisationens [!DNL IAS] konto, som [!DNL IAS] fakturerar direkt för användning. <!-- verify -->

**[!UICONTROL MOAT]:** (Valfritt) Aktiverar [!DNL MOAT] mätning och rapportering av synlighet, bedrägeri, varumärkessäkerhet och målgruppsverifiering. Ytterligare avgifter tillkommer.

#### Målgruppsverifiering

**[!UICONTROL comScore Campaign Ratings]:** (Valfritt) Aktiverar [!DNL Comscore] validerad [!DNL Campaign Ratings] mätning och rapportering av målgruppsverifiering, med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Target Gender]:** Det kön som målet ska vara: *[!UICONTROL Both]* (standard), *[!UICONTROL Male]*, eller *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Det åldersintervall som ska anges som mål. Använd vänster och höger skjutreglage för att minska intervallet efter behov.

* **[!UICONTROL Target Country]:** (Valfritt) Ett land att rikta sig till. [!DNL Comscore] endast i de länder som stöds.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Aktiverar spårning för placeringsnivån [!UICONTROL Attention Score] mått (det vägda genomsnittliga antalet [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; över intryck). Mätvärden är tillgängliga för alla placeringstyper förutom för [!DNL Roku] ansluten TV, endast VPAID-pre-roll och ljud som inte är en poddsändning. DSP kopplar automatiskt en JavaScript-tagg till alla associerade kreatörer, och [!DNL Adelaide] spårar exponeringsdata och skickar dem till DSP dagligen. Du kan använda datumet för att manuellt optimera dina utgifter mot placeringsstrategier med bättre resultat.

The [!UICONTROL Attention Score] fältet är tillgängligt i [!UICONTROL Metrics] rapportavsnitt, inom [!UICONTROL Campaigns], [!UICONTROL Packages]och [!UICONTROL Placements] åsikter, och på [!UICONTROL Sites], [!UICONTROL Ads]och [!UICONTROL Inventory] -flikar i [vyn med placeringsinformation](/help/dsp/campaign-management/reports/placement-details-view.md).

Använda [!DNL Adelaide] segment för mätning medför en CPM-avgift för varje intryck som skickas från annonser med [!DNL Adelaide] måttetiketter. Avgiften är skild från avgifterna för [målinriktning på placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Aktiverar förstahandsmätning och rapportering av visningsbarhet med [!DNL IAB Open Video Viewability (OpenVV)] teknik som bygger på den angivna känslighetsnivån:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Om Campaign Management](campaign-about.md)
>* [Skapa en kampanj](campaign-create.md)
>* [Redigera en kampanj](campaign-edit.md)
>* [Visa ändringsloggen för en kampanj](campaign-change-log.md)
