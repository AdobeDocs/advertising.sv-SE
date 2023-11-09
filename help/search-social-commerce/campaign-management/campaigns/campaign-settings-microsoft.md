---
title: '''[!DNL Microsoft® Advertising] kampanjinställningar'
description: Referera inställningarna för [!DNL Microsoft® Advertising] kampanjer.
exl-id: c6d86fb8-48b0-40fd-bcfc-c4afdccd5283
feature: Search Campaign Management
source-git-commit: 236224a1d8e38862f70db63b3762b763f5703623
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] kampanjinställningar

## \[Kampanjskapande skärm\]

**[!UICONTROL Campaign Type]:** (Endast tillgängligt när kampanjer skapas) Var annonser ska placeras och vilka annonstyper kampanjen kan innehålla:

* *[!UICONTROL Search]:* Visar textannonser i söknätverket.

* *[!UICONTROL Shopping Network]:* Visar produktannonser - för era produkter i [!DNL Microsoft® Merchant Center] produktkatalog - i shoppingnätverket.

* *[!UICONTROL Audience]:* Visar annonser på webben/skärmen på [!DNL Microsoft® Audience Network]. Du kan antingen a) automatiskt generera feed-baserade annonser genom att länka kampanjen till en handlarcenterbutik i [!UICONTROL Shopping Settings] eller b) skapa responsiva annonser med textresurser och överförda bilder. Båda alternativen kräver att ni skapar annonsgrupper med målgruppsanpassning.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Betafunktion) Marknadsför dina produkter via länkade återförsäljare i söknings- och målgruppsnätverk. Du kan skapa underordnade annonsgrupper och produktgrupper (appar som ska marknadsföras) för kampanjen, och [!DNL Microsoft® Advertising] skapar automatiskt annonser för produktgrupperna.

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Betafunktion) Markerar dina appar och spel som är tillgängliga i [!DNL Microsoft® Store]. Du kan skapa underordnade annonsgrupper och produktgrupper för kampanjen, och [!DNL Microsoft® Advertising] skapar automatiskt annonser för produktgrupperna.

* *[!UICONTROL Audience Video]:* (Betafunktion) Visar videoannonser i målgruppsnätverket.

* *[!UICONTROL Audience Video]:* (Betafunktion) Visar videoannonser på uppkopplade TV-apparater (CTV) i målgruppsnätverket.

* *[!UICONTROL Performance Max]:* Visar flera annonstyper i alla nätverk.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ett kampanjnamn som är unikt inom kontot. Maximala längden är 128 tecken.

**[!UICONTROL Status]:** Visningsstatus för kampanjen: *Aktiv* eller *Pausad*. Standardinställningen för nya annonskampanjer är *Aktiv*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Anbudsstrategin för kampanjen:

* *[!UICONTROL CPV]* (Endast CTV-kampanjer för målgrupp) Använder modellen för kostnad per vy (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Kampanjer för målgrupp, söknätverk och shoppingnätverk) Använder annonsnätverkets förbättrade modell för kostnad per klickning (eCPC), som gör att annonsnätverket automatiskt kan ändra priset per klick (CPC) för varje auktion i ett försök att maximera konverteringarna med hjälp av konverteringar som anges i annonsnätverket (inte i Sök, Social och Commerce), samtidigt som man försöker hålla den genomsnittliga CPC:n under den maximala antalet. .

  När du lägger till en kampanj med eCPC i en optimerad portfölj för sökning, sociala medier och handel optimerar sökningen, sociala medier och handel basanbuden och - när &quot;[!UICONTROL Auto adjust campaign budget limits]Alternativet &quot; är aktiverat - kampanjbudgeten. Annonsnätverket optimerar alla offertjusteringar och kan ändra de söknings-, sociala- och handelsbudgivningar som genereras vid tidpunkten för användarfrågan baserat på egna data och insikter. **Varning:** Använd eCPC-kampanjer i portföljer endast när de totala konverteringarna i annonsnätverket är anpassade efter portföljmålet.

* *[!UICONTROL Manual CPC]*: (Köpkampanjer för varumärken; [!DNL Microsoft Store Ads] kampanjer, borttagna av [!DNL Microsoft® Advertising] 2021 för andra kampanjtyper) Använder CPC-modellen (cost-per-click). För vissa annonstyper kan ni välja att tillåta annonsnätverket att ändra anbud för kampanjen:

   * **[!UICONTROL Enable Enhanced CPC]** (inaktiverat som standard): Detta är samma sak som att använda &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] kampanjer) Använder modellen för kostnad per förvärv (CPA).

* *[!UICONTROL Manual CPM]* (Endast målgruppskampanjer och målgruppsvideokampanjer) Använder modellen med CPM (cost-per-tusen-imponsions), där du anger vad du vill spendera per 1 000 visningar. Kampanjer med denna anbudsstrategi optimeras inte när de ingår i portföljer.

* *[!UICONTROL Maximize Clicks]:* (Sökning- och shoppingkampanjer) Annonsnätverket - inte Sök, Social och Commerce - optimerar offerterna för att maximera antalet klick. Du kan även ange **[!UICONTROL Max CPC]** (kostnad per klick) för att säkerställa att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Varning:** När ni lägger till en kampanj med den här strategin i en portfölj styrs budgivningen av klickvikt, inte av portföljmålet.

* *[!UICONTROL Maximize Conversion Value]:* (Sökning och shopping/smarta shoppingnätverk, maximala resultatkampanjer) Annonsnätverket - inte Search, Social, &amp; Commerce - optimerar anbud för att maximera konverteringsvärdet. Du kan även ange **[!UICONTROL Target Return on Ad Spend]** (ROAS) i procent. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Maximize Conversions]:* (Kampanjer i söknätverket) <!-- future: and audience network -->, max-kampanjer) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera konverteringarna. Du kan även ange **[!UICONTROL Target CPC]** (kostnad per klick)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Target CPA]:* (Kampanjer i söknätverket) Annonsnätverket - inte Sök, Social och Commerce - optimerar anbud baserat på ett valfritt **[!UICONTROL Target CPA]** (kostnad per förvärv), vilket är det 30-dagars genomsnittliga belopp som du vill betala för ett förvärv (konvertering). **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target CPA].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

* *[!UICONTROL Target Impression Share]:* (Kampanjer i söknätverket) Annonsnätverket - inte Search, Social och Commerce - optimerar anbud för att uppnå en målvisningsresurs och en annonsposition. Du kan även ange **[!UICONTROL Target Impression Share]** som procent **[!UICONTROL Target Ad Position]** och en **[!UICONTROL Max CPC]** (kostnad per klick). **Obs!** Det här alternativet stöds inte i hybridportföljer.

* *[!UICONTROL Target Return on Ad Spend]:*  (Kampanjer i sök- och shoppingnätverken) Annonsnätverket - inte Sök, Social och Commerce - optimerar anbud baserat på er **[!UICONTROL Target ROAS]** (avkastning på annonsutgift), angett i procent. Du kan även ange **[!UICONTROL Max CPC]** (kostnad per klick) för att säkerställa att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target ROAS].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Endast köpkampanjer; skrivskyddat för befintliga kampanjer) Det land där kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Endast målgruppskampanjer, valfritt) Länkar kampanjen till en viss handlarcenterbutik för automatiska flödesbaserade annonser i stället för responsiva annonser. När du väljer det här alternativet anger du [!UICONTROL Merchant ID] och [!UICONTROL Products]. Ni måste skapa annonsgrupper för kampanjen, men ni behöver inte skapa annonser.

När du har länkat kampanjen till en butik och sparat inställningarna kan du inte ändra det här alternativet.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Målgruppskampanjer som endast är kopplade till en återförsäljarcenterbutik) De produkter som ska annonseras. Som standard *[!UICONTROL All products]* är markerat. Om du bara vill annonsera produkter med specifika attribut väljer du *[!UICONTROL Filter products]* och ange upp till sju produktdimensions- och attributkombinationer där du kan filtrera produkterna. Alla angivna värden måste gälla för att annonser ska visas för produkten. Om du till exempel vill visa annonser för Acme-djurförråd kan du skapa filtren `Custom Label 1=animals`, `Category=pet supplies`och `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

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

**[!UICONTROL Negative Websites]:** (Kampanjer endast på displayen/det ursprungliga nätverket, valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i Microsoft® Advertising help to &quot;[Förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Om *[!UICONTROL Use account conversion goals for this campaign]* (standard) eller *[!UICONTROL Use campaign specific conversion goals]*. Om du väljer att ange konverteringsmål för kampanjen väljer du målen i listan med alla tillgängliga mål. **Obs!** Mål synkroniseras dagligen, så mål som skapats under de senaste 24 timmarna kanske inte visas. Om du vill uppdatera listan [manuellt synkronisera annonsens nätverksdata](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Om kampanjen ingår i en portfölj ska du använda samma konverteringsmål som portföljens mål. Olika konverteringsmål kan påverka portföljens prestanda.

>[!MORELIKETHIS]
>
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
