---
title: Visa annonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för displayannonser.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '444'
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

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen. **Tips!** Om du vill redigera tredjepartspixlar för spårning av annonser för flera annonser på en plats samtidigt i vyn [!UICONTROL Ad Tools] ska du läsa &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Händelsen som utlöser pixeln att utlösa. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för angiven [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* eller *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP makron](/help/dsp/campaign-management/macros.md)
