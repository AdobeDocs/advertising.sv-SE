---
title: Inställningar för [!DNL Microsoft Advertising]-kampanj
description: Referera inställningarna för [!DNL Microsoft Advertising] kampanjer.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '2075'
ht-degree: 0%

---

# Inställningar för [!DNL Microsoft Advertising]-kampanj

## \[Kampanjskapande skärm\]

**[!UICONTROL Campaign Type]:** (Endast tillgängligt när kampanjer skapas) Var annonser ska placeras och vilka annonstyper
kampanjen får innehålla

* *[!UICONTROL Search]:* Visar textannonser i söknätverket.

* *[!UICONTROL Shopping Network]:* Visar produktannonser - för dina produkter i din [!DNL Microsoft Merchant Center] produktkatalog - i shoppingnätverket.

* *[!UICONTROL Audience]:* Visar inbyggda/visade annonser på [!DNL Microsoft Audience Network]. Du kan antingen a) automatiskt generera feedbaserade annonser genom att länka kampanjen till en handlarcenterbutik i avsnittet [!UICONTROL Shopping Settings] eller b) skapa responsiva annonser med textresurser och överförda bilder. Båda alternativen kräver att ni skapar annonsgrupper med målgruppsanpassning.

* *[!UICONTROL Shopping Campaigns for Brands]:* Markerar dina produkter via länkade återförsäljare i söknings- och målgruppsnätverk. Du kan skapa underordnade annonsgrupper och produktgrupper (appar som ska marknadsföras) och valfria produktannonser för kampanjen. [!DNL Microsoft Advertising] skapar automatiskt annonser för produktgrupperna. Använd anbudsstrategin [!UICONTROL Manual CPC] för butikskampanjer för varumärken. Använd anbudsstrategin [!UICONTROL Cost per Sale] för butikskampanjer för varumärken.

* *[!UICONTROL Microsoft Store Ads Campaign]:* Markerar dina appar och spel som är tillgängliga i [!DNL Microsoft Store]. Du kan skapa underordnade annonsgrupper, produktgrupper och valfria produktannonser för kampanjen. [!DNL Microsoft Advertising] skapar automatiskt annonser för produktgrupperna.

* *[!UICONTROL Audience CTV Video]:* Visar videoannonser för uppkopplad TV (CTV) i målgruppsnätverket.

* *[!UICONTROL Audience Video]:* Visar standardvideoannonser i målgruppsnätverket.

* *[!UICONTROL Performance Max]:* Visar flera annonstyper i alla nätverk som använder [!DNL Microsoft Advertising] smart budgivning. Inom kampanjinställningarna måste du ange en eller flera resursgrupper, som omfattar bilder, logotyper, rubriker, beskrivningar, ett valfritt call to action och målgruppssignaler. Annonsnätverket kombinerar automatiskt resurserna för att leverera annonser baserat på kanalen.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ett kampanjnamn som är unikt i kontot. Maximala längden är 128 tecken.

**[!UICONTROL Status]:** Visningsstatusen för kampanjen: *Aktiv* eller *Pausad*. Standardvärdet för nya annonskampanjer är *Aktiv*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Gäller för kampanjer som riktar sig till målgrupper i EU) Om kampanjen innehåller politisk annonsering per krav för annonser som betjänas i EU enligt EU:s förordning 2024/90 eller inte: *[!UICONTROL Yes]* eller *[!UICONTROL No]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Anbudsstrategin för kampanjen:

* *[!UICONTROL Cost per Sale]:* (endast köpkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud baserat på [!UICONTROL Target CPS] (kostnad per försäljning). Du betalar bara när ett klick på produkten leder till en försäljning inom 24 timmar. **Obs!** Inkludera inte kampanjer med den här anbudsstrategin i portföljer. Optimering av sökmotorkampanjer, sociala kampanjer och Commerce är inte tillgängligt för kampanjer med den här anbudsstrategin.

  När ni väl har sparat en shoppingkampanj för varumärken med denna anbudsstrategi kan ni inte ändra anbudsstrategin. För andra typer av shoppingkampanjer är den här strategin bara tillgänglig för nya kampanjer.

* *[!UICONTROL CPV]* (Endast CTV-kampanjer för målgrupp) Använder modellen för kostnad per vy (CPV). Search, Social och Commerce erbjuder ingen optimering för kampanjer med denna anbudsstrategi som ingår i portföljer.

* *[!UICONTROL Enhanced CPC]:* (Kampanjer för målgrupp, söknätverk och shoppingnätverk) Använder annonsnätverkets förbättrade kostnadsmodell per klick (eCPC), som gör att annonsnätverket automatiskt kan ändra priset per klick (CPC) för varje auktion i ett försök att maximera konverteringar med hjälp av konverteringar som anges i annonsnätverket (inte i Search, Social och Commerce), samtidigt som det försöker att behålla din genomsnittliga CPC PC under din maximala CPC.

  När du lägger till en kampanj med eCPC i en optimerad Search-, Social- och Commerce-portfölj optimerar Search, Social och Commerce basanbuden och - när alternativet [!UICONTROL Auto adjust campaign budget limits] är aktiverat - kampanjbudgeten. Annonsnätverket optimerar alla offertjusteringar och kan ändra de söknings-, sociala och Commerce-genererade anbuden vid tidpunkten för användarfrågan baserat på egna data och insikter. **Varning!** Använd eCPC-kampanjer i portföljer endast när de totala konverteringarna som spåras i annonsnätverket är anpassade efter portföljmålet.

* *[!UICONTROL Manual CPC]*: (Köpkampanjer för varumärken, [!DNL Microsoft Store Ads] kampanjer, borttagna för andra kampanjtyper) Använder modellen för kostnad per klick (CPC). För vissa annonstyper kan ni välja att tillåta annonsnätverket att ändra anbud för kampanjen:

   * **[!UICONTROL Enable Enhanced CPC]** (inaktiverat som standard): Det här alternativet är detsamma som att använda alternativet [!UICONTROL Enhanced CPC].

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] kampanjer) Använder modellen för kostnad per förvärv (CPA).

* *[!UICONTROL Manual CPM]* (Endast målgruppskampanjer och målgruppsvideokampanjer) Använder CPM-modellen (kostnad per tusen visningar), där du anger vad du vill spendera per 1 000 visade visningar. Kampanjer med denna anbudsstrategi optimeras inte när de ingår i portföljer.

* *[!UICONTROL Maximize Clicks]:* (sök- och shoppingkampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera antalet klick. Du kan också ange en **[!UICONTROL Max CPC]** (kostnad per klick) för att se till att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Varning!** När du lägger till en kampanj med den här strategin i en portfölj genererar klickvikten (inte portföljmålet) anbud.

* *[!UICONTROL Maximize Conversion Value]:* (Söknings- och shoppingnätverk/smarta shoppingnätverk, maximala prestandakampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud för att maximera konverteringsvärdet. Du kan också ange en **[!UICONTROL Target Return on Ad Spend]** (ROAS) i procent. **Obs!** Använd det här alternativet för kampanjer i hybridportföljer men inte standardportföljer. I hybridportföljer optimerar Search, Social och Commerce Target ROAS.

* *[!UICONTROL Maximize Conversions]:* (Prestanda för max antal kampanjer och kampanjer i söknätverket eller målgruppsnätverket (men inte i målgruppsvideor eller ansluten TV)) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera konverteringarna. Du kan också ange **[!UICONTROL Target CPC]** (kostnad per klick). För målgruppskampanjer kan du även ange en valfri **[!UICONTROL Target CPA]** (kostnad per förvärv). **Obs!** Använd det här alternativet för kampanjer i hybridportföljer men inte standardportföljer. I hybridportföljer optimerar Search, Social och Commerce Target CPA.

* *[!UICONTROL Target CPA]:* (Kampanjer i söknätverket) Annonsnätverket - inte Search, Social, &amp; Commerce - optimerar anbud baserat på ett valfritt **[!UICONTROL Target CPA]** (kostnad per förvärv), som är det 30-dagars genomsnittsbelopp som du vill betala för ett förvärv (konvertering). **Obs!** Använd det här alternativet för kampanjer i hybridportföljer (men inte standardportföljer) med någon utgiftsstrategi förutom [!UICONTROL Weekly] eller [!UICONTROL Google Target CPA]. I hybridportföljer optimerar Search, Social och Commerce Target CPA.

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

* *[!UICONTROL Target Impression Share]:* (Kampanjer i söknätverket) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att uppnå en målvisningsresurs och en annonsposition. Du kan också ange **[!UICONTROL Target Impression Share]** som ett procentvärde, **[!UICONTROL Target Ad Position]** och **[!UICONTROL Max CPC]** (kostnad per klick). **Obs!** Det här alternativet stöds inte i hybridportföljer.

* *[!UICONTROL Target Return on Ad Spend]:* (Kampanjer i sök- och köpnätverk) Annonsnätverket - inte Search, Social, &amp; Commerce - optimerar anbud baserat på din **[!UICONTROL Target ROAS]** (avkastning på annonsutgift), angett i procent. Du kan också ange en **[!UICONTROL Max CPC]** (kostnad per klick) för att se till att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Obs!** Använd det här alternativet för kampanjer i hybridportföljer (men inte standardportföljer) med någon utgiftsstrategi förutom [!UICONTROL Weekly] eller [!UICONTROL Google Target ROAS]. I hybridportföljer optimerar Search, Social och Commerce Target ROAS.

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (endast köpkampanjer, skrivskyddad för befintliga kampanjer) Det land där
kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Endast målgruppskampanjer, valfritt) Länkar kampanjen till en specifik butiksförsäljning för automatiserade feedbaserade annonser i stället för responsiva annonser. När du väljer det här alternativet anger du [!UICONTROL Merchant ID] och [!UICONTROL Products]. Ni måste skapa annonsgrupper för kampanjen, men ni behöver inte skapa annonser.

När du har länkat kampanjen till en butik och sparat inställningarna kan du inte ändra det här alternativet.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Målgruppskampanjer som endast är länkade till en handlarcenterbutik) Produkterna som ska annonseras. Som standard är *[!UICONTROL All products]* markerat. Om du bara vill annonsera produkter med specifika attribut väljer du *[!UICONTROL Filter products]* och anger upp till sju produktdimension- och attributkombinationer som du vill filtrera produkterna på. Alla angivna värden måste gälla för att annonser ska visas för produkten. Om du till exempel vill visa annonser för Acme-djurleveranser kan du skapa filtren `Custom Label 1=animals`, `Category=pet supplies` och `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Endast maximala prestandakampanjer) Språket för annonsen, som ska matcha språket för de webbplatser där annonsen kan visas. [!DNL Microsoft Advertising] avgör användarens språk utifrån olika signaler, inklusive användarens fråga, utgivarens land och användarens språkinställning.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

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

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Endast kampanjer på skärmen/i det ursprungliga nätverket; valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i hjälpen för Microsoft Advertising om att [förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).

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

**[!UICONTROL Asset Group Name]:** Namnet på resursmappen (resursgrupp).

**[!UICONTROL Asset Group Status]:** Resursgruppens status: *[!UICONTROL Active]* eller *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Den sista URL:en för alla annonser som har skapats från resursgruppen.

**[!UICONTROL Images]:** Upp till 20 bilder för annonsen, inklusive minst en fyrkantig bild och en liggande bild. Se [[!DNL Microsoft Advertising] bildriktlinjerna](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Du kan antingen överföra bilder eller välja dem från [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. Klicka på [!UICONTROL Upload from Device] på fliken **[!UICONTROL +]** och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du har angett klart bilder klickar du på **[!UICONTROL Upload]**.

* Om du vill välja bilder från din [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer bilderna.

**[!UICONTROL Logos]:** Minst en logotyp. Du kan inkludera upp till fem. Se [[!DNL Microsoft Advertising] riktlinjerna för mediefiler](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Du kan antingen överföra bilder eller välja dem från [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här överför du bilder:

   1. Klicka på [!UICONTROL Upload from Device] på fliken **[!UICONTROL +]** och välj bilder från enheten eller nätverket.

   1. För varje bild:

      1. Välj proportioner.

      1. Dra och placera beskärningsrutan efter behov för att markera den del av bilden som kan visas och ändra storleken på den del av bilden som kan visas när det är möjligt.

      1. (Valfritt) Välj ytterligare bildproportioner och ändra eventuellt bildens placering och storlek efter behov för varje vald bildproportion.

         En resurs skapas för varje vald proportion.

      1. Klicka på **[!UICONTROL Proceed]**.

   1. När du har angett klart bilder klickar du på **[!UICONTROL Upload]**.

* Om du vill välja bilder från din [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer bilderna.

**[!UICONTROL Headlines]:** Minst tre och upp till 15 korta rubriker med högst 30 tecken vardera. Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Long Headlines]:** Minst en och upp till fem långa rubriker med högst 90 tecken vardera. Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Descriptions]:** Minst två och upp till fem beskrivningar med högst 90 tecken vardera. Du kan antingen ange text eller välja resurser från din [!UICONTROL Asset Library] - men inte båda i samma åtgärd.

* Så här skriver du text:

   1. Ange texten på fliken [!UICONTROL Enter Text].

   1. (Valfritt) Om du vill lägga till ytterligare en textsträng klickar du på **[!UICONTROL + Add]** och anger strängen.

* Om du vill välja resurser från [!UICONTROL Asset Library] klickar du på **[!UICONTROL Asset Library]** och väljer resurserna.

**[!UICONTROL Call to Action]:** Den call to action som ska inkluderas i annonsen. Som standard är *[!UICONTROL Act Now]* markerat.

**[!UICONTROL Business Name]:** Företagsnamnet, med högst 25 tecken. Det får inte innehålla skript, HTML eller något annat kodspråk.

**[!UICONTROL Audience Signal]:** (Valfritt) [!DNL Microsoft Advertising] målgrupper som ska användas som målgruppssignaler för kampanjen. [!DNL Microsoft Advertising] maskininlärningsmodeller använder målgrupperna för att hitta liknande webbsurfningar att rikta sig till och kan även visa annonser till målgrupper som inte har angetts som signaler som hjälper dig att uppnå dina prestationsmål. Välj de målgrupper som mest sannolikt konverterar.

>[!NOTE]
>Målgruppssignaler skiljer sig från [annonsmålgruppsmål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Gör att du kan ange en annan resursgrupp.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Om *[!UICONTROL Use account conversion goals for this campaign]* (standard) eller *[!UICONTROL Use campaign specific conversion goals]* ska användas. Om du väljer att ange konverteringsmål för kampanjen väljer du målen i listan med alla tillgängliga mål. **Obs!** Mål synkroniseras dagligen, så mål som skapats under de senaste 24 timmarna kanske inte visas. [synkronisera annonsens nätverksdata manuellt](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) om du vill uppdatera listan.

>[!TIP]
>
>Om kampanjen ingår i en blandad portfölj är det bästa sättet att använda kampanjnivåmål som matchar konverteringsmålen i portföljens mål. Om ytterligare konverteringsmål inkluderas kan portföljens resultat påverkas.
>
> För kampanjer i hybridportfolior för vilka du [överför mål till annonsnätverket](/help/search-social-commerce/tools/objective-upload-to-networks.md) gör du följande i annonsnätverkets redigerare i stället för här: a) lägg till det överförda söknings-, sociala och Commerce-portföljsmålet (som börjar med&quot;O_ACS_OBJ&quot;) som ett konverteringsmål för kampanjen, och b) lägg till alla kampanjmål som omfattar konverteringar som spåras av den universella eventspårningen [!DNL Microsoft Advertising] (spårning) UET)-tagg eftersom annonsnätverkets spårade mätvärden inte överförs till annonsnätverket med målet.

>[!MORELIKETHIS]
>
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
