---
title: '''[!DNL Google Ads] kampanjinställningar'
description: Referera inställningarna för [!DNL Google Ads] kampanjer.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '2430'
ht-degree: 0%

---

# [!DNL Google Ads] kampanjinställningar

## \[Kampanjskapande skärm\]

**[!UICONTROL Campaign Type]:** (Endast tillgängligt när kampanjer skapas) Var annonser ska placeras och vilka annonstyper kampanjen kan innehålla:

* *[!UICONTROL Search Network Only]:* Visar annonser i söknätverket, som innehåller [!DNL Google] sökresultat och, om så önskas, sökpartnerwebbplatser. Du måste ange nyckelord för varje annonsgrupp.

* *[!UICONTROL Search with Display Select]:* Visar annonser i söknätverket (som inkluderar [!DNL Google] sökresultat och, om så önskas, sökpartnerwebbplatser) och eventuellt annonser på webbplatser i visningsnätverk. På visningsnätverket [!DNL Google Ads] visar era annonser selektivt med hjälp av automatiserade budgivning, oavsett kampanjens anbudsstrategi. För sökannonser anger du nyckelord för varje annonsgrupp. För visningsannonser anger du placeringar och kan även ange nyckelord för varje annonsgrupp.

* *[!UICONTROL Shopping Network]:* Visar produktannonser, som [!DNL Google] genererar automatiskt baserat på dina produkter i [!DNL Google Merchant Center] på [!DNL Google Shopping], området intill [!DNL Google] sökresultat (separerade från textannonser) och (valfritt) sökpartnerwebbplatser. För varje annonsgrupp i kampanjen kan du ange vilka produktgrupper som ska annonseras.

* *[!UICONTROL Display Network Only]:* Visar annonser i visningsnätverket. För varje annonsgrupp måste du ange placeringar och om du vill kan du ange nyckelord.

* *[!UICONTROL Performance Max]:* (Betafunktion) Visar och optimerar konverteringar för era annonser i alla kanaler med [!DNL Google Ads] smart budgivning. Inom kampanjinställningarna måste du ange en eller flera resursgrupper, som omfattar bilder, logotyper, rubriker, beskrivningar, valfria videor och målgruppssignaler. [!DNL Google Ads] kombinerar automatiskt resurserna för att leverera annonser baserat på kanalen (som [!DNL YouTube], [!DNL Gmail], eller [!DNL Search]).

  **Anteckningar:**

   * Endast nödvändiga inställningar är tillgängliga. Logga in på [!DNL Google Ads] redigerare.

   * Länkar till [!DNL Google Merchant Center] produktflöden stöds inte.

   * Stöd för listgrupper är inte tillgängligt. Om du vill hantera och visa data för listgrupper loggar du in på [!DNL Google Ads] redigerare.

   * Hybridoptimering stöds. Anbudsstrategiska mål och kampanjbudgetar fastställs på kampanjnivå.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ett kampanjnamn som är unikt inom kontot.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Endast befintliga, skrivskyddade Gmail-kampanjer) Om du vill:

* *[!UICONTROL Target and Bid]* Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:*  Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

**[!UICONTROL Status]:** Visningsstatus för kampanjen: *Aktiv* eller *Pausad*. Standardinställningen för nya annonskampanjer är *Aktiv*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Kampanjer som endast riktar sig till söknätverket, inklusive shoppingkampanjer) Visar annonserna i annonsnätverkets nätverk av sökpartner. Som standard är det här alternativet *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Anbudsstrategin för kampanjen:

* *[!UICONTROL Enhanced CPC]:* (Inte tillgängligt för högsta prestanda eller befintlig, skrivskyddad [!DNL Gmail] kampanjer) Använder annonsnätverkets utökade modell för kostnad per klick (eCPC), som gör att annonsnätverket automatiskt kan ändra priset per klick (CPC) för varje auktion i ett försök att maximera konverteringar, med hjälp av konverteringar som anges i annonsnätverket (inte i Search, Social, &amp; Commerce), samtidigt som ni försöker hålla den genomsnittliga CPC:n under den maximala CPC:n.

När ni lägger till en kampanj med eCPC i en optimerad Search-, Social- och Commerce-portfolio optimerar Search, Social och Commerce basanbuden och - när &quot;[!UICONTROL Auto adjust campaign budget limits]Alternativet &quot; är aktiverat - kampanjbudgeten. Annonsnätverket optimerar alla offertjusteringar och kan ändra de söknings-, sociala och Commerce-genererade anbuden vid tidpunkten för användarfrågan baserat på egna data och insikter. **Varning:** Använd eCPC-kampanjer i portföljer endast när de totala konverteringarna i annonsnätverket är anpassade efter portföljmålet. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (standard): (Inte tillgängligt för maximala prestandakampanjer) Använder CPC-modellen (cost-per-click). Du kan också tillåta annonsnätverket att ändra anbud för kampanjen:

   * **[!UICONTROL Enable Enhanced CPC]** (inaktiverat som standard): Detta är samma sak som att använda &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Sök-, displays- och shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera antalet klick. Du kan även ange **[!UICONTROL Max CPC]** (kostnad per klick) för att säkerställa att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Varning:** När ni lägger till en kampanj med den här strategin i en portfölj styrs budgivningen av klickvikt, inte av portföljmålet.

* *[!UICONTROL Maximize Conversion Value]:* (Sökning, maximalt resultat och smarta shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud för att maximera konverteringsvärdet. Du kan även ange **[!UICONTROL Target Return on Ad Spend]** (ROAS) i procent. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Maximize Conversions]:* (max antal sök-, display- och prestandakampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för maximal konvertering. Du kan även ange **[!UICONTROL Target CPA]** (kostnad per förvärv). **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Target CPA]:* (Visningskampanjer, befintliga sökkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud baserat på ett valfritt **[!UICONTROL Target CPA]** (kostnad per förvärv), vilket är det 30-dagars genomsnittliga belopp som du vill betala för ett förvärv (konvertering). **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target CPA].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

  För nya sökkampanjer [!DNL Google Ads] har ersatt denna anbudsstrategi med [!UICONTROL Maximize Conversions] strategi med [!UICONTROL Target CPA] värde. För befintliga sökkampanjer med den här strategin kan du bara redigera målvärdet, och om du gör det ändras strategin till [!UICONTROL Maximize Conversions] strategi som använder den angivna [!UICONTROL Target CPA] värde.

* *[!UICONTROL Target Impression Share]:* (Sökkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att uppnå en målvisningsresurs och en annonsposition. Du kan även ange **[!UICONTROL Target Impression Share]** som en procentandel, **[!UICONTROL Target Ad Position]** och en **[!UICONTROL Max CPC]** (kostnad per klick). **Obs!** Det här alternativet stöds inte i portföljer.

* *[!UICONTROL Target Return on Ad Spend]:*  (Visnings- och shoppingkampanjer, befintliga sökkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud baserat på en viss angiven **[!UICONTROL Target ROAS]** (avkastning på annonsutgift), angett i procent. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target ROAS].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

  För nya sökkampanjer [!DNL Google Ads] har ersatt denna anbudsstrategi med [!UICONTROL Maximize Conversion Value] strategi med [!UICONTROL Target Return on Ad Spend value]. För befintliga sökkampanjer med den här strategin kan du bara redigera målvärdet, och om du gör det ändras strategin till [!UICONTROL Maximize Conversion Value] strategi som använder den angivna [!UICONTROL Target Return on Ad Spend] värde.

* *[!UICONTROL Viewable CPM]:* (Befintlig, skrivskyddad) [!DNL Gmail] endast kampanjer) Annonsnätverket - inte Search, Social och Commerce - erbjuder endast annonser som kan visas. **Obs!** Optimering för den här strategin stöds inte i någon typ av portfölj.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Endast köpkampanjer; skrivskyddat för befintliga kampanjer) Det land där kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Endast köpkampanjer; annonsörer som redan deltar i det lokala shoppingprogrammet med [!DNL Google Merchant Center] butiker i USA, Storbritannien, DE, FR, JP och AU (valfritt) Tillåter [!DNL Google Ads] för att automatiskt lägga till din lokala lagerinformation i dina shoppingannonser på Google.com.

**Tips:** Om du använder den här inställningen ska du inte utesluta lokala annonser i [!UICONTROL Inventory Filter] inställning.

**Obs!** Annonser om lokala lager kräver ytterligare två feeds för [!DNL Google Merchant Center] - en med era lokala produktdata och en annan med ert lokala produktlager. Se [!DNL Google Ads] dokumentation om mer information om [lokala shoppingannonser](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Endast sök- och visningsnätverk) Ett eller flera målspråk för annonser i kampanjen.

[!DNL Google Ads] bestämmer användarens språk från användarens [!DNL Google] språkinställning för sökfrågans språk, den aktuella sidan eller nyligen visade sidor på sidan [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Specifika användargeografiska platser att inkludera eller exkludera som mål. Som standard anges alla platser som mål. Du kan inkludera och exkludera användare i valfri kombination av platser. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla platser som mål väljer du inga platser.

* Så här anger du specifika platser som mål eller exkluderar:

   * (Länder, delstater, storstadsområden eller städer) Klicka **[!UICONTROL Location Target]** (![Platsmål](/help/search-social-commerce/assets/location-target.png "Platsmål")) och hitta de platser som ska inkluderas och exkluderas:

      * Om du vill ta med en plats och dess underordnade platser klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas.

      * Om du vill utesluta en plats klickar du två gånger på cirkeln bredvid den så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

      * Klicka på platsnamnet om du vill expandera en plats till dess underkomponenter (t.ex. delstater, storstadsområden eller städer i USA).

      * Om du vill söka efter en plats anger eller klistrar du in minst de tre första tecknen på platsen i indatafältet. Klicka på **[!UICONTROL Include]** bredvid en plats att ta med eller **[!UICONTROL Exclude]** bredvid en plats som ska uteslutas.

   * (Platser nära en adress; endast inkluderade mål) Klicka **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) och sedan klicka på **[!UICONTROL Address]**. Ange adressen och radien i engelska mil eller kilometer runt den adress du vill ange som mål och klicka sedan på **[!UICONTROL Add]**.

   * (Platser nära geografiska koordinater; endast inkluderade mål) Klicka **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) och sedan klicka på **[!UICONTROL Coordinate]**. Ange latitud och longitud samt radien i engelska mil eller kilometer runt den plats du vill rikta, och klicka sedan på **[!UICONTROL Add]**.

* (Så här lägger du till en anbudsjustering för en inkluderad målplats) Ange ett värde för anbudsjustering:

* 0 %: Om du inte vill justera anbuden för annonser på den här platsen.

* \[Övriga värden från -90 % till 300 %\]: Om du vill öka eller minska antalet annonser på den här platsen.

**Obs!**

* Sökning, Socialt och Commerce erbjuder inte automatiska justeringar av anbudsjusteringar för följande platsmål på grund av begränsningar i de data som [!DNL Google Ads] innehåller funktioner för mappning av surfer-platser till platsmål:

   * Radie-mål.

   * Vissa platser nedanför delstat/provins/region/län/prefektur för vilka [!DNL Google Ads] skickar inte någon överordnad plats på surfarens URL, inklusive flygplatser och kongressdistrikt i USA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Endast displaynätverk) Specifika mobiloperatörer att rikta sig till. Transportörerna sorteras efter land. Om du inte markerar något, anges alla som mål.

**[!UICONTROL Mobile Carriers]:** (Endast bildskärmsnätverk) Specifika operativsystem att rikta sig till. Om du inte markerar något, anges alla som mål.

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

**[!UICONTROL Track Product Group]:** (för [!UICONTROL EF Redirect] endast) Ej implementerat

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per tillgångsgrupp)

**[!UICONTROL Asset Group Name]:** Namnet på tillgångsgruppen. Länkar till [!DNL Google Merchant Center] produktflöden stöds inte.

**[!UICONTROL Asset Group Status]:** Tillgångsgruppens status: *[!UICONTROL Active]* eller *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Den slutliga URL:en för alla annonser som skapats från resursgruppen. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Upp till 15 bilder för annonsen, inklusive följande storlekar: 1) minst tre fyrkantiga bilder, 2) minst tre liggande bilder och 3) minst en stående bild. Se [[!DNL Google Ads] bildspecifikationer](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Du kan överföra bilder eller välja dem från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. På [!UICONTROL Upload from Device] flik, klicka **[!UICONTROL +]** och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du är klar med att ange bilder klickar du på **[!UICONTROL Upload]**.

* Välj bilder från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och markera bilderna.

**[!UICONTROL Logos]:** Minst en logotyp med fyrkantig (1:1) och en liggande (4:1) logotyp. Du kan inkludera upp till fem av varje storlek. Se [[!DNL Google Ads] logotypspecifikationer](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Du kan överföra bilder eller välja dem från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. På [!UICONTROL Upload from Device] flik, klicka **[!UICONTROL +]** och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du är klar med att ange bilder klickar du på **[!UICONTROL Upload]**.

* Välj bilder från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och markera bilderna.

**[!UICONTROL Videos]:** (Valfritt) Minst en och upp till fem, [!DNL YouTube] videor som är minst 10 sekunder långa. Du kan antingen ange URL:er eller välja dem från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här anger du URL:er:

   1. På [!UICONTROL Enter Video Url] anger du en URL-adress.

   1. (Valfritt) Om du vill lägga till en annan URL klickar du på **[!UICONTROL + Add]** och ange webbadressen.

* Så här väljer du videofilmer från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och välj videoklipp.

**[!UICONTROL Headlines]:** Minst tre och upp till fem korta rubriker med högst 30 tecken vardera. Minst en rubrik får innehålla högst 15 tecken. Om alternativet på kampanjnivå för att aktivera slutlig URL-utökning har angetts i [!DNL Google Ads]sedan [!DNL Google Ads] ersätter det här värdet med en anpassad rubrik baserad på landningssidans innehåll.

Du kan antingen ange text eller välja resurser från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här skriver du text:

   1. På [!UICONTROL Enter Text] anger du texten.

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och ange strängen.

* Välj resurser från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och välj resurser.

**[!UICONTROL Long Headlines]:** Minst en och upp till fem långa rubriker med högst 90 tecken vardera. Du kan antingen ange text eller välja resurser från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här skriver du text:

   1. På [!UICONTROL Enter Text] anger du texten.

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och ange strängen.

* Välj resurser från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och välj resurser.

**[!UICONTROL Descriptions]:** Minst två och upp till fyra beskrivningar med högst 90 tecken vardera. Minst en beskrivning måste innehålla minst 30 tecken. Du kan antingen ange text eller välja resurser från [!UICONTROL Asset Library] — men inte båda i samma åtgärd.

* Så här skriver du text:

   1. På [!UICONTROL Enter Text] anger du texten.

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och ange strängen.

* Välj resurser från [!UICONTROL Asset Library], klicka **[!UICONTROL Asset Library]** och välj resurser.

**[!UICONTROL Call to Action]:** Uppmaningen att ta med i annonsen. Som standard *[!UICONTROL Automated]* är markerat och [!DNL Google Ads] väljer anropet till åtgärd. Du kan välja en annan åtgärd.

**[!UICONTROL Business Name]:** Affärsnamnet med högst 25 tecken.

**[!UICONTROL Audience Signal]:** (Valfritt) [!DNL Google Ads] målgrupper som ska användas som målgruppssignaler för kampanjen. [!DNL Google Ads] maskininlärningsmodeller använder målgrupperna för att hitta liknande webbsurfarenheter att rikta in sig på och kan även visa annonser för målgrupper som inte är angivna som signaler som hjälper er att uppnå era prestationsmål. Välj de målgrupper som mest sannolikt konverterar.

>[!NOTE]
>Målgruppssignaler skiljer sig från [målgrupper på kampanjnivå och annonsnivå](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Gör att du kan ange en annan resursgrupp.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Om *[!UICONTROL Use account conversion goals for this campaign]* (standard) eller *[!UICONTROL Use campaign specific conversion goals]*. Om du väljer att ange konverteringsmål för kampanjen väljer du standardmål och/eller skapar ett anpassat mål för kampanjen.

Mål synkroniseras dagligen, så befintliga mål som skapats under de senaste 24 timmarna kanske inte visas. Om du vill uppdatera listan [manuellt synkronisera annonsens nätverksdata](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Om du vill skapa ett anpassat konverteringsmål klickar du **[!UICONTROL + Add custom goal]**, ange det anpassade målnamnet och välj [konverteringsåtgärder](https://support.google.com/google-ads/answer/6032150) som ska ingå i det anpassade målet och sedan klicka **[!UICONTROL Save]**. **Obs!** Varje kampanj kan bara ha ett anpassat mål.

>[!TIP]
>
>För kampanjer i hybridportfolior för vilka ni överför mål till annonsnätverket är det bästa sättet att använda kampanjnivåmål som matchar konverteringsmålen i portföljens mål. Men om kampanjmålen omfattar [!DNL Google]-spårade konverteringar och lägg sedan till dem i [!DNL Google Ads] redigerare eftersom de inte överförs till annonsnätverket igen med målet. I [!DNL Google Ads] kan du ta bort kampanjens konverteringsåtgärder som standardmål genom att markera dem som sekundära (inte primära) mål.

<!-- Check on this:
>If the campaign is part of a hybrid portfolio, then use only conversion goals that are included in the portfolio's objective for the campaign. Including additional conversion goals may impact portfolio performance.
>
>The objective may include conversion goals or other conversions that aren't included for the campaign, but the campaign can't include conversion goals that aren't included in the objective.
-->

>[!MORELIKETHIS]
>
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

