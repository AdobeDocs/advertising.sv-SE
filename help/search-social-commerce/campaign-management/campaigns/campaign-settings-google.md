---
title: Inställningar för [!DNL Google Ads]-kampanj
description: Referera inställningarna för [!DNL Google Ads] kampanjer.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: cbe18b75d49ca53460883931ecea21aa6c2d8326
workflow-type: tm+mt
source-wordcount: '2472'
ht-degree: 0%

---

# Inställningar för [!DNL Google Ads]-kampanj

## \[Kampanjskapande skärm\]

**[!UICONTROL Campaign Type]:** (Endast tillgängligt när kampanjer skapas) Var annonser ska placeras och vilka annonstyper kampanjen kan innehålla:

* *[!UICONTROL Search Network Only]:* Visar annonser i söknätverket, som innehåller [!DNL Google] sökresultat och, om så önskas, sökpartnerwebbplatser. Du måste ange nyckelord för varje annonsgrupp.

* *[!UICONTROL Search with Display Select]:* Visar annonser i söknätverket (vilket inkluderar [!DNL Google] sökresultat och, eventuellt, sökpartnerwebbplatser) och kan visa annonser på visningsnätverksplatser. I visningsnätverket visar [!DNL Google Ads] dina annonser selektivt med automatiserad budgivning, oavsett kampanjens anbudsstrategi. För sökannonser anger du nyckelord för varje annonsgrupp. För visningsannonser anger du placeringar och kan även ange nyckelord för varje annonsgrupp.

* *[!UICONTROL Shopping Network]:* Visar produktannonser, som [!DNL Google] genererar automatiskt baserat på dina produkter i [!DNL Google Merchant Center] den [!DNL Google Shopping] , området bredvid [!DNL Google] sökresultat (separat från textannonser) och (valfritt) sökpartnerwebbplatser. För varje annonsgrupp i kampanjen kan du ange vilka produktgrupper som ska annonseras.

* *[!UICONTROL Display Network Only]:* Visar annonser i visningsnätverket. För varje annonsgrupp måste du ange placeringar och om du vill kan du ange nyckelord.

* *[!UICONTROL Performance Max]:* Visar och optimerar konverteringar för annonser i alla kanaler med hjälp av [!DNL Google Ads] smart budgivning. Inom kampanjinställningarna måste du ange en eller flera resursgrupper, som omfattar bilder, logotyper, rubriker, beskrivningar, valfria videor och målgruppssignaler. [!DNL Google Ads] kombinerar automatiskt resurserna för att hantera annonser baserat på kanalen (till exempel [!DNL YouTube], [!DNL Gmail] eller [!DNL Search]).

  **Anteckningar:**

   * Endast nödvändiga inställningar är tillgängliga. Logga in på [!DNL Google Ads]-redigeraren om du vill ha valfria inställningar.

   * Länkar till [!DNL Google Merchant Center] produktfeeds stöds inte.

   * Stöd för listgrupper är inte tillgängligt. Om du vill hantera och visa data för listgrupper loggar du in på [!DNL Google Ads]-redigeraren.

   * Hybridoptimering stöds. Anbudsstrategiska mål och kampanjbudgetar fastställs på kampanjnivå.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ett kampanjnamn som är unikt i kontot.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Befintliga, skrivskyddade Gmail-kampanjer endast) Anger om:

* *[!UICONTROL Target and Bid]* Om du bara vill visa annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:* Så här visar du annonser även för personer som inte är associerade med målgrupper så länge de uppfyller andra annonsgruppsmål. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

**[!UICONTROL Status]:** Visningsstatusen för kampanjen: *Aktiv* eller *Pausad*. Standardvärdet för nya annonskampanjer är *Aktiv*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Kampanjer som endast riktar sig till söknätverket, inklusive shoppingkampanjer) Visar
era annonser i annonsnätverkets nätverk av sökpartners. Som standard är det här alternativet *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Anbudsstrategin för kampanjen:

* *[!UICONTROL Enhanced CPC]:* har tagits bort. [!DNL Google Ads] började automatiskt ändra befintliga [utökade CPC-anbudsstrategier](https://support.google.com/google-ads/answer/2464964) till manuell CPC den 15 mars 2025.

* *[!UICONTROL Manual CPC]* (standard): (Inte tillgängligt för maximala prestandakampanjer) Använder CPC-modellen (cost-per-click). Du kan också tillåta annonsnätverket att ändra anbud för kampanjen:

   * **[!UICONTROL Enable Enhanced CPC]** (inaktiverat som standard): Detta är samma sak som att använda alternativet [!UICONTROL Enhanced CPC], som är inaktuellt. [!DNL Google Ads] började automatiskt ändra befintliga [utökade CPC-anbudsstrategier](https://support.google.com/google-ads/answer/2464964) till manuell CPC den 15 mars 2025.

* *[!UICONTROL Maximize Clicks]:* (sök-, display- och shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera antalet klick. Du kan också ange en **[!UICONTROL Max CPC]** (kostnad per klick) för att se till att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Varning!** När du lägger till en kampanj med den här strategin i en portfölj styrs budgivningen av klickvikt, inte av portföljmålet.

* *[!UICONTROL Maximize Conversion Value]:* (Sök, prestanda max och smarta shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera konverteringsvärdet. Du kan också ange **[!UICONTROL Target Return on Ad Spend]** (ROAS) som en procentandel. **Obs!** Använd det här alternativet för kampanjer i hybridportföljer men inte standardportföljer. I hybridportföljer optimerar Search, Social och Commerce kampanjnivån eller målavkastningen på gruppnivå (om tillgängligt).

* *[!UICONTROL Maximize Conversions]:* (max antal sök-, display- och prestandakampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera konverteringarna. Du kan också ange **[!UICONTROL Target CPA]** (kostnad per förvärv). **Obs!** Använd det här alternativet för kampanjer i hybridportföljer men inte standardportföljer. I hybridportföljer optimerar Search, Social och Commerce kampanjnivån eller (om tillgängligt) målgruppsmålgruppsmålgruppsanpassningen.

* *[!UICONTROL Target CPA]:* (Visningskampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud baserat på ett valfritt **[!UICONTROL Target CPA]** (kostnad per förvärv), som är det 30-dagars genomsnittsbelopp som du vill betala för ett förvärv (konvertering). **Obs!** Använd det här alternativet för kampanjer i hybridportföljer (men inte standardportföljer) med någon utgiftsstrategi förutom [!UICONTROL Weekly] eller [!UICONTROL Google Target CPA]. I hybridportföljer optimerar Search, Social och Commerce kampanjnivån eller (om tillgängligt) målgruppsmålgruppsmålgruppsanpassningen.

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

* *[!UICONTROL Target Impression Share]:* (sökkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud för att uppnå en målvisningsresurs och en annonsposition. Du kan också ange **[!UICONTROL Target Impression Share]** som en procentandel, **[!UICONTROL Target Ad Position]** och **[!UICONTROL Max CPC]** (kostnad per klick). **Obs!** Det här alternativet stöds inte i portföljer.

* *[!UICONTROL Target Return on Ad Spend]:* (Visnings- och shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud baserat på en angiven **[!UICONTROL Target ROAS]** (avkastning på annonskostnader), angiven som en procentandel. **Obs!** Använd det här alternativet för kampanjer i hybridportföljer (men inte standardportföljer) med någon utgiftsstrategi förutom [!UICONTROL Weekly] eller [!UICONTROL Google Target ROAS]. I hybridportföljer optimerar Search, Social och Commerce kampanjnivån eller målavkastningen på gruppnivå (om tillgängligt).

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

* *[!UICONTROL Viewable CPM]:* (Endast befintliga, skrivskyddade [!DNL Gmail] kampanjer) Annonsnätverket - inte Search, Social och Commerce - erbjuder endast annonser som kan visas. **Obs!** Optimering för den här strategin stöds inte i någon typ av portfölj.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (endast köpkampanjer, skrivskyddad för befintliga kampanjer) Det land där
kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Endast köpkampanjer; annonsörer som redan deltar i det lokala shoppingprogrammet med [!DNL Google Merchant Center] butiker i USA, Storbritannien, DE, FR, JP och AU; valfritt) Tillåter [!DNL Google Ads] att automatiskt lägga till din lokala lagerinformation i dina shoppingannonser på Google.com.

**Tips!** Om du använder den här inställningen ska du inte utesluta lokala annonser i inställningen [!UICONTROL Inventory Filter].

**Obs!** Lokala lagerannonser kräver ytterligare två flöden till [!DNL Google Merchant Center] - en med dina lokala produktdata och en annan med din lokala produktinventering. Mer information om [lokala kundannonser](https://www.google.com/retail/local-inventory-ads/) finns i dokumentationen för [!DNL Google Ads].

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Endast sök- och visningsnätverk) Ett eller flera målspråk för annonser i kampanjen.

[!DNL Google Ads] bestämmer en användares språk utifrån användarens [!DNL Google]-språkinställning eller språket för sökfrågan, den aktuella sidan eller nyligen visade sidor på [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Specifika geografiska platser för användare som ska inkluderas eller exkluderas som mål. Som standard anges alla platser som mål. Du kan inkludera och exkludera användare i valfri kombination av platser. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla platser som mål väljer du inga platser.

* Så här anger du specifika platser som mål eller exkluderar:

   * (Länder, lägen, storstadsområden eller städer) Klicka på **[!UICONTROL Location Target]** (![Sökvägsmål](/help/search-social-commerce/assets/location-target.png "Sökvägsmål")) och leta reda på de platser som ska inkluderas och exkluderas:

      * Om du vill inkludera en plats och dess underordnade platser klickar du en gång på den intilliggande cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas.

      * Om du vill utesluta en plats klickar du två gånger på den intilliggande cirkeln så att en röd bock (![Uteslut](/help/search-social-commerce/assets/exclude.png "Uteslut")) visas.

      * Klicka på platsnamnet om du vill expandera en plats till dess underkomponenter (t.ex. delstater, storstadsområden eller städer i USA).

      * Om du vill söka efter en plats anger eller klistrar du in minst de tre första tecknen på platsen i indatafältet. I sökresultaten klickar du på **[!UICONTROL Include]** bredvid en plats som ska inkluderas eller **[!UICONTROL Exclude]** bredvid en plats som ska uteslutas.

   * (Platser nära en adress, endast inkluderade mål) Klicka på **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) och klicka sedan på **[!UICONTROL Address]**. Ange adressen och radien i engelska mil eller kilometer runt den adress du vill rikta och klicka sedan på **[!UICONTROL Add]**.

   * (Platser nära geografiska koordinater, endast inkluderade mål) Klicka på **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) och klicka sedan på **[!UICONTROL Coordinate]**. Ange latitud och longitud samt radien i engelska mil eller kilometer runt den plats som du vill ha som mål och klicka sedan på **[!UICONTROL Add]**.

* (Så här lägger du till en anbudsjustering för en inkluderad målplats) Ange ett värde för anbudsjustering:

* 0 %: Om du inte vill justera anbuden för annonser på den här platsen.

* \[Övriga värden från -90 % till 300 %\]: Om du vill öka eller minska antalet annonser på den här platsen.

**Obs!**

* I Sök, Socialt och Commerce finns inga automatiskt justerade budjusteringar för följande platsmål på grund av begränsningar i data som [!DNL Google Ads] tillhandahåller för mappning av surfer-platser till platsmål:

   * Radie-mål.

   * Vissa platser nedanför den delstat/provins/region/region/prefecture-nivå för vilken [!DNL Google Ads] inte skickar någon överordnad plats på surfarens URL, inklusive flygplatser och kongressdistrikt i USA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Endast visningsnätverk) Specifika mobiloperatörer att rikta sig till; bärarna sorteras
efter land. Om du inte markerar något, anges alla som mål.

**[!UICONTROL Mobile Carriers]:** (Endast visningsnätverk) Specifika operativsystem att rikta sig till. Om du inte markerar något, anges alla som mål.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** (Max. prestanda och endast sökkampanjer) Så här tilldelar du anbud till nya kunder och befintliga kunder:

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **Obs!** Om du vill använda den här inställningen måste du först aktivera det nya kundvärvningsmålet för [!DNL Google Ads]-kontot eller, om tillämpligt, för chefskontot. Målet definierar de giltiga befintliga kundlistorna och det extra konverteringsvärdet för nya kunder i konverteringsinställningarna. Se steg 1-2 i [!DNL Google Ads]-hjälpen [Aktivera det nya kundförvärvsmålet](https://support.google.com/google-ads/answer/14007601).

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (endast för [!UICONTROL EF Redirect]) har inte implementerats

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per tillgångsgrupp)

**[!UICONTROL Asset Group Name]:** Namnet på resursgruppen. Länkar till [!DNL Google Merchant Center] produktfeeds stöds inte.

**[!UICONTROL Asset Group Status]:** Resursgruppens status: *[!UICONTROL Active]* eller *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Den sista URL:en för alla annonser som har skapats från resursgruppen. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Upp till 15 bilder för annonsen, inklusive följande storlekar: 1) minst tre kvadratiska bilder, 2) minst tre liggande bilder och 3) minst en stående bild. Se [[!DNL Google Ads] bildspecifikationerna](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Du kan antingen överföra bilder eller välja dem från [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. Klicka på **[!UICONTROL +]** på fliken [!UICONTROL Upload from Device] och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du har angett klart bilder klickar du på **[!UICONTROL Upload]**.

* Om du vill välja bilder från din [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer bilderna.

**[!UICONTROL Logos]:** Minst en logotyp med fyrkantig (1:1) och en logotyp med liggande (4:1). Du kan inkludera upp till fem av varje storlek. Se [[!DNL Google Ads] logotypspecifikationerna](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Du kan antingen överföra bilder eller välja dem från [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. Klicka på **[!UICONTROL +]** på fliken [!UICONTROL Upload from Device] och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du har angett klart bilder klickar du på **[!UICONTROL Upload]**.

* Om du vill välja bilder från din [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer bilderna.

**[!UICONTROL Videos]:** (Valfritt) Minst en och upp till fem, [!DNL YouTube] videor som är minst 10 sekunder långa. Du kan antingen ange URL:er eller välja dem från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här anger du URL:er:

   1. Ange en URL på fliken [!UICONTROL Enter Video Url].

   1. (Valfritt) Om du vill lägga till en annan URL-adress klickar du på **[!UICONTROL + Add]** och anger URL-adressen.

* Om du vill välja videofilmer från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer videofilmerna.

**[!UICONTROL Headlines]:** Minst tre och upp till fem korta rubriker med högst 30 tecken vardera. Minst en rubrik får innehålla högst 15 tecken. Om alternativet på kampanjnivå för att aktivera slutlig URL-utökning är inställt inom [!DNL Google Ads], ersätter [!DNL Google Ads] det här värdet med en anpassad rubrik baserad på innehållet på landningssidan.

Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Long Headlines]:** Minst en och upp till fem långa rubriker med högst 90 tecken vardera. Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Descriptions]:** Minst två och upp till fyra beskrivningar med högst 90 tecken vardera. Minst en beskrivning måste innehålla minst 30 tecken. Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Call to Action]:** Den call to action som ska inkluderas i annonsen. Som standard är *[!UICONTROL Automated]* markerat och [!DNL Google Ads] väljer call to action. Du kan välja en annan åtgärd.

**[!UICONTROL Business Name]:** Företagsnamnet, med högst 25 tecken.

**[!UICONTROL Audience Signal]:** (Valfritt) [!DNL Google Ads] målgrupper som ska användas som målgruppssignaler för kampanjen. [!DNL Google Ads] maskininlärningsmodeller använder målgrupperna för att hitta liknande webbsurfningar att rikta sig till och kan även visa annonser till målgrupper som inte har angetts som signaler som hjälper dig att uppnå dina prestationsmål. Välj de målgrupper som mest sannolikt konverterar.

>[!NOTE]
>Målgruppssignaler skiljer sig från [målgruppsmål på kampanjnivå och annonsnivå](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (skrivskyddat fält för befintliga resursgrupper i maximala prestandakampanjer) Varför resursgruppen har eller inte har full kapacitet. Den tar hänsyn till tillgångsgruppens status samt andra signaler, såsom policy- och kvalitetsgodkännanden. Värdena kan vara *ELIGIBLE,* *LIMITED,* *NOT_ELIGIBLE,* *PAUSED,* *PENDING,* *REMOVED,* *UNKNOWN,* eller *UNSPECIFICED.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (skrivskyddat fält för befintliga resursgrupper i maximala prestandakampanjer) Ytterligare information om resursgruppens primära status. Värdena kan vara *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_Under_REVIEW,* *ASSET CAMPAIGN_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *OKÄND,* ELLER *OSPECIFICERAD.*

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Om *[!UICONTROL Use account conversion goals for this campaign]* (standard) eller *[!UICONTROL Use campaign specific conversion goals]* ska användas. Om du väljer att ange konverteringsmål för kampanjen väljer du standardmål och/eller skapar ett anpassat mål för kampanjen.

Mål synkroniseras dagligen, så befintliga mål som skapats under de senaste 24 timmarna kanske inte visas. [synkronisera annonsens nätverksdata manuellt](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) om du vill uppdatera listan.

Om du vill skapa ett anpassat konverteringsmål klickar du på **[!UICONTROL + Add custom goal]**, anger det anpassade målnamnet, väljer de [konverteringsåtgärder](https://support.google.com/google-ads/answer/6032150) som ska inkluderas i det anpassade målet och klickar sedan på **[!UICONTROL Save]**. **Obs!** Varje kampanj kan bara ha ett anpassat mål.

>[!TIP]
>
>Om kampanjen ingår i en blandad portfölj är det bästa sättet att använda kampanjnivåmål som matchar konverteringsmålen i portföljens mål. Om ytterligare konverteringsmål inkluderas kan portföljens resultat påverkas.
>
>För kampanjer i hybridportfolior för vilka du [överför mål till annonsnätverket](/help/search-social-commerce/tools/objective-upload-to-networks.md) gör du följande i annonsnätverkets redigerare i stället för här: a) lägg till det överförda söknings-, sociala och Commerce-portföljsmålet (som börjar med&quot;O_ACS_OBJ&quot;) som en konverteringsåtgärd för kampanjen, och b) lägg till kampanjmål som omfattar [!DNL Google] spårade konverteringar på grund av annonsnätverksportföljen spårade mätvärden överförs inte till annonsnätverket med målet.

>[!MORELIKETHIS]
>
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
