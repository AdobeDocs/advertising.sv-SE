---
title: Visa annonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för displayannonser.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Visa annonsinställningar

Följande inställningar gäller för vanliga displayannonser.

## [!UICONTROL Ad Options]

### Grundläggande

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till. Standardvärdet är *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i [!UICONTROL Ads]-vyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Holiday Product Preview: 300x250 Gamer&quot;).

**\[Lägg till Source\]**: (skrivskyddat) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Endast annonser från tredje part) Anger att annonsen är en utbyggbar banners. De relaterade expansionsinställningarna avgör vilket lager som ska köpas, så se till att de återspeglar annonsbeteendet.

**[!UICONTROL Expansion Method]:** (Endast utbyggbara banners från tredje part) Om bannern utökas *[!UICONTROL Click]* eller *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Endast expanderbara banners från tredje part) Riktningen som annonsen utökas i: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* eller *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Endast utbyggbara banners från tredje part) Den certifierade leverantör som annonsen är tillgänglig för: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* eller *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part. Alla parametrar för [tidsstämpel] och [[tidsstämpel]] ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part, med nödvändiga [Advertising DSP-spårningsmakron](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Ad Size]:** Annonsens bredd och höjd. Det måste vara en [standardstorlek för visning och visning](ad-specs.md) som stöds. Du kan ange annonsstorleken manuellt innan du överför annonsen eller ange en [!UICONTROL Display Code]. Om du inte anger annonsstorleken anges dimensionerna för den överförda annonstaggen eller annonstaggen automatiskt som skrivskyddade.

>[!IMPORTANT]
>
> Annonsstorleken som deklareras i fälten för bredd och höjd matchas med inkommande anbudsförfrågningar. Leveransproblem kan uppstå om annonsens dimensioner inte matchar den deklarerade annonsstorleken.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP-makron](/help/dsp/campaign-management/macros.md)
