---
title: '[!DNL Google Ads] och gruppinställningar'
description: Referera inställningarna för  [!DNL Google Ads] annonsgrupper.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: 345c2af5363ca10412f3809700e281af5b06897f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!DNL Google Ads] och gruppinställningar

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ett annonsgruppsnamn som är unikt i kampanjen. Maxlängden är 255 dubbelbyte-tecken.

**[!UICONTROL Status]:** Annonsgruppens visningsstatus: *Aktiv* eller *Pausad*. Standardvärdet för nya annonsgrupper är *Aktiv*.

**[!UICONTROL Ad Group Type]:** (Endast expanderade dynamiska sökannonskampanjer) Typ av annonsgrupp:

* *[!UICONTROL Search Standard]* (standard): För standardannonser.

* *[!UICONTROL Search Dynamic]:* För dynamiska sökannonser.

**[!UICONTROL Ad Rotation Mode]:** Hur ofta [!DNL Google Ads] skickar dina aktiva annonser i relation till varandra inom annonsgruppen:

* *[!UICONTROL Optimize]:* Google Ads prioriterar annonser som förväntas utföras bättre än andra annonser i annonsgruppen. Dessa annonser kommer in på annonsauktionen oftare, och med tiden prioriteras en enskild annons. Detta kan vara inkonsekvent med era affärs- och optimeringsmål.

* *[!UICONTROL Rotate forever]:*   Var och en av era annonser går in i annonsauktionen ett jämnare antal gånger, vilket gör att Search, Social och Commerce kan få sina annonser inte bara i klickfrekvens utan även i konverteringar.

* *[!UICONTROL Use campaign setting]*(standard för nya annonsgrupper): Använder den befintliga inställningen för kampanjnivå och rotation. **Obs!** Inställningen på kampanjnivå visas inte i Sök, Socialt och Commerce.

Om kampanjen använder en strategi för Smart Bidding-bud (till exempel [!UICONTROL Target CPA], [!UICONTROL Target ROAS]) anger [!DNL Google Ads] automatiskt alternativet till [!UICONTROL Optimize].

**[!UICONTROL Custom Bid Level]:** (Kampanjer som endast riktar sig till visningsnätverket) Så här lägger du till: av *[!UICONTROL Ad Group]* (standard), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Intresse &amp; Remarketing i Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (webbplats), *[!UICONTROL Unknown]* eller *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* När du lägger ett bud med nyckelord skapar du spårningsmallar på nyckelordsnivå. På samma sätt kan du skapa spårningsmallar på placeringsnivå när du lägger ett bud per placering. För alla andra dimensioner skapar du spårningsmallar på annonsnivå.
>* När ni lägger bud per ålder, kön, ränta och lista eller vertikalt för kampanjer i portföljer optimerar inte optimeringsfunktionen budskapen för dimensionen. Dessutom tillämpas all attribuering på annonsgruppen.
>* I annonser i söknätverket används alltid nyckelordsbud.

**[!UICONTROL AI Max Search Term Matching]:** (Kampanjer som riktar sig till söknätverket och för vilka funktionen [AI Max &#x200B;](https://support.google.com/google-ads/answer/15910366) och söktermmatchningen på kampanjnivå är aktiverad; skrivskyddad) Anger om söktermmatchning på ad gruppnivå är aktiverad: *[!UICONTROL Disabled]* eller *[!UICONTROL Enabled]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Kampanjer med [!UICONTROL Target CPA] budgivning; valfritt) Målkostnaden per förvärv (CPA) för annonsgruppen. Det här värdet åsidosätter kampanjnivåmålet.

**[!UICONTROL Target ROAS]:** (Kampanjer med [!UICONTROL Target ROAS] budgivning; valfritt) Målavkastningen på annonskostnaderna (ROAS) för annonsgruppen, som en procentandel. Det här värdet åsidosätter kampanjnivåmålet.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (kampanjer endast i söknätverket och befintliga, skrivskyddade [!DNL Gmail]-kampanjer i visningsnätverket) Om du vill:

* *[!UICONTROL Target and Bid]:* Om du bara vill visa annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:* Så här visar du annonser även för personer som inte är associerade med målgrupper så länge de uppfyller andra annonsgruppsmål. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Hantera annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
