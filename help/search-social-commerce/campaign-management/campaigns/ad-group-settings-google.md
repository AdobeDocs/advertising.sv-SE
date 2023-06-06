---
title: "[!DNL Google Ads] annonsgruppsinställningar"
description: Referera inställningarna för [!DNL Google Ads] annonsgrupper.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] och gruppinställningar

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ett annonsgruppsnamn som är unikt i kampanjen. Maxlängden är 255 dubbelbyte-tecken.

**[!UICONTROL Status]:** Annonsgruppens visningsstatus: *Aktiv* eller *Pausad*. Standardinställningen för nya annonsgrupper är *Aktiv*.

**[!UICONTROL Ad Group Type]:** (Endast utökade dynamiska sökannonskampanjer) Annonsgrupp:

* *[!UICONTROL Search Standard]* (standard): För standardannonser.

* *[!UICONTROL Search Dynamic]:* För dynamiska sökannonser.

**[!UICONTROL Ad Rotation Mode]:** Hur ofta [!DNL Google Ads] levererar era aktiva annonser i relation till varandra inom annonsgruppen:

* *[!UICONTROL Optimize]:* Google Ads prioriterar annonser som förväntas prestera bättre än andra annonser i annonsgruppen. Dessa annonser kommer in på annonsauktionen oftare, och med tiden prioriteras en enskild annons. Detta kan vara inkonsekvent med era affärs- och optimeringsmål.

* *[!UICONTROL Rotate forever]:*   Var och en av era annonser går in i annonsauktionen ett jämnare antal gånger, vilket gör det möjligt för Search, Social och Commerce att göra annonser inte bara med klickfrekvens utan även med konverteringar.

* *[!UICONTROL Use campaign setting]*(standard för nya annonsgrupper): Använder den befintliga inställningen för kampanjnivå och rotation. **Obs!** Inställningen på kampanjnivå visas inte i Sök, Socialt och Handel.

Om kampanjen använder en strategi för smart budgivning (till exempel [!UICONTROL Target CPA], [!UICONTROL Target ROAS], eller [!UICONTROL Enhanced CPC]), sedan [!DNL Google Ads] anger automatiskt alternativet till[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Kampanjer som endast riktar sig till visningsnätverket) Så här lägger du ett bud: av *[!UICONTROL Ad Group]* (standard), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Intresse &amp; Remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (webbplats), *[!UICONTROL Unknown]*, eller *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* När du lägger ett bud med nyckelord skapar du spårningsmallar på nyckelordsnivå. På samma sätt kan du skapa spårningsmallar på placeringsnivå när du lägger ett bud per placering. För alla andra dimensioner skapar du spårningsmallar på annonsnivå.
>* När ni lägger bud per ålder, kön, ränta och lista eller vertikalt för kampanjer i portföljer optimerar inte optimeringsfunktionen budskapen för dimensionen. Dessutom tillämpas all attribuering på annonsgruppen.
>* I annonser i söknätverket används alltid nyckelordsbud.


## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Kampanjer med [!UICONTROL Target CPA] budgivning, (frivillig uppgift) Målkostnaden per förvärv (CPA) för annonsgruppen. Det här värdet åsidosätter kampanjnivåmålet.

**[!UICONTROL Target ROAS]:** (Kampanjer med [!UICONTROL Target ROAS] budgivning, (valfritt) Målavkastningen på annonskostnaderna (ROAS) för annonsgruppen, i procent. Det här värdet åsidosätter kampanjnivåmålet.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Kampanjer endast i söknätverket och befintliga, skrivskyddade [!DNL Gmail] kampanjer i visningsnätverket) Om du vill:

* *[!UICONTROL Target and Bid]:* Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:* Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

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

