---
title: "[!DNL Microsoft Advertising] kampanjinställningar"
description: Referera inställningarna för [!DNL Microsoft Advertising] kampanjer.
source-git-commit: 0706f4dbc5f2a27e7d0cf43a6865d242865f9d36
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] kampanjinställningar

## \[Kampanjskapande skärm\]

**[!UICONTROL Campaign Type]:** (Endast tillgängligt när kampanjer skapas) Var annonser ska placeras och vilka annonstyper kampanjen kan innehålla:

* *[!UICONTROL Search and Display Network]:* Visar endast textannonser i söknätverket.

* *[!UICONTROL Shopping Network]:* Visar produktannonser - för era produkter i [!DNL Microsoft Merchant Center] produktkatalog - i shoppingnätverket

* *[!UICONTROL Audience]:* Visar annonser på webben/i displayannonser på [!DNL Microsoft Audience Network]. Du kan antingen a) automatiskt generera feed-baserade annonser genom att länka kampanjen till en handlarcenterbutik i [!UICONTROL Shopping Settings] eller b) skapa responsiva annonser med textresurser och överförda bilder. Båda alternativen kräver att ni skapar annonsgrupper med målgruppsanpassning.

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

* *[!UICONTROL Enhanced CPC]:* (Kampanjer för målgrupp, söknätverk och shoppingnätverk) Använder annonsnätverkets förbättrade modell för kostnad per klick (eCPC), som gör att annonsnätverket automatiskt kan ändra priset per klick (CPC) för varje auktion i ett försök att maximera konverteringarna med hjälp av konverteringar som anges i annonsnätverket (inte i Sök, Socialt och Commerce), samtidigt som ni försöker hålla er genomsnittliga CPC under maximalt CPC.

När du lägger till en kampanj med eCPC i en optimerad portfölj för sökning, sociala medier och handel optimerar sökningen, sociala medier och handel basanbuden och - när &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; är aktiverat - kampanjbudgeten. Annonsnätverket optimerar alla offertjusteringar och kan ändra de söknings-, sociala- och handelsbudgivningar som genereras vid tidpunkten för användarfrågan baserat på egna data och insikter. **Varning:** Använd eCPC-kampanjer i portföljer endast när de totala konverteringarna i annonsnätverket är anpassade efter portföljmålet.

* *[!UICONTROL Manual CPC]* (standard): (Föråldrat av [!DNL Microsoft Advertising] 2021) Använder CPC-modellen (cost-per-click). Du kan också tillåta annonsnätverket att ändra anbud för kampanjen:

   * **[!UICONTROL Enable Enhanced CPC]** (inaktiverat som standard): Det är samma sak som att använda[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPM]* (Endast kampanjer i målgruppsnätverket) Använder modellen med kostnad per tusen visningar (CPM), där du anger vad du vill spendera per 1 000 visningar. Kampanjer med denna anbudsstrategi optimeras inte när de ingår i portföljer.

* *[!UICONTROL Maximize Clicks]:* (Sökning- och shoppingkampanjer) Annonsnätverket - inte Sök, Social och Commerce - optimerar offerterna för att maximera antalet klick. Om du vill kan du ange **[!UICONTROL Max CPC]** (kostnad per klick) för att säkerställa att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Varning:** När ni lägger till en kampanj med den här strategin i en portfölj styrs budgivningen av klickvikt, inte av portföljmålet.

* *[!UICONTROL Maximize Conversion Value]:* (Sökning- och shoppingnätverk/smarta shoppingnätverk) Annonsnätverket - inte Search, Social, &amp; Commerce - optimerar anbud för att maximera konverteringsvärdet. Du kan även ange en **[!UICONTROL Target Return on Ad Spend]** (ROAS) i procent. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Maximize Conversions]:* (Kampanjer i söknätverket) <!-- future: and audience network -->) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att maximera konverteringarna. Du kan även ange en **[!UICONTROL Target CPC]** (kostnad per klick)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior men inte i standardportfolior.

* *[!UICONTROL Target CPA]:* (Kampanjer i söknätverket) Annonsnätverket - inte Sök, Social och Commerce - optimerar anbud baserat på ett valfritt **[!UICONTROL Target CPA]** (kostnad per förvärv), vilket är det 30-dagars genomsnittliga belopp som du vill betala för ett förvärv (konvertering). **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target CPA].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

* *[!UICONTROL Target Impression Share]:* (Kampanjer i söknätverket) Annonsnätverket - inte Search, Social och Commerce - optimerar offerterna för att uppnå en målvisningsresurs och en annonsposition. Om du vill kan du ange **[!UICONTROL Target Impression Share]** som procent **[!UICONTROL Target Ad Position]** och en **[!UICONTROL Max CPC]** (kostnad per klick). **Obs!** Det här alternativet stöds inte i hybridportföljer.

* *[!UICONTROL Target Return on Ad Spend]:*  (Kampanjer i sök- och shoppingnätverken) Annonsnätverket - inte Sök, Social och Commerce - optimerar anbud baserat på er **[!UICONTROL Target ROAS]** (avkastning på annonsutgift), angett i procent. Om du vill kan du ange **[!UICONTROL Max CPC]** (kostnad per klick) för att säkerställa att annonsnätverket inte betalar mer än ett visst belopp för varje klick. **Obs!** Använd det här alternativet för kampanjer i hybridportfolior (men inte i standardportfolior) med alla utgiftsstrategier utom [!UICONTROL Weekly] eller [!UICONTROL Google Target ROAS].

  Genomsnittlig position och CPC-buddata är inte tillgängliga för kampanjer med den här anbudsstrategin.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Endast köpkampanjer. skrivskyddad för befintliga kampanjer) Det land där kampanjprodukterna säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Endast målgruppskampanjer; (valfritt) Länkar kampanjen till en specifik handlarcenterbutik för automatiska feedbaserade annonser i stället för responsiva annonser. När du väljer det här alternativet anger du [!UICONTROL Merchant ID] och [!UICONTROL Products]. Ni måste skapa annonsgrupper för kampanjen, men ni behöver inte skapa annonser.

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

**[!UICONTROL Negative Websites]:** (Endast kampanjer i displayen/det egna nätverket). (valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i Microsoft Advertising Help to &quot;[Förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

>[!MORELIKETHIS]
>
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
