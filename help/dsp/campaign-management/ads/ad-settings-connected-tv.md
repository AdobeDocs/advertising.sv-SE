---
title: Inställningar för ansluten TV-annons
description: Se beskrivningar av tillgängliga annonsinställningar för anslutna TV-annonser.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Inställningar för ansluten TV-annons

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]**: VAST-taggens URL.

**[!UICONTROL Title]**: Ett namn på filen som ska användas i annonsvyn och -rapporter.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]** -tangenten. Om märkordet är giltigt visas en XML-fil som innehåller `<VAST>` nära toppen.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering i [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. heldagsproduktsförhandsvisning: 30sek CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height | Ad Unit Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** X-koordinaten för annonsenheten. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Y-koordinaten för annonsenheten. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma sak som **[!UICONTROL Width]** fält.

**[!UICONTROL Player Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma sak som **[!UICONTROL Height]** fält.

**[!UICONTROL Show Controls]:** Var videokontroller för annonsen ska inkluderas: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, eller *[!UICONTROL None]* (standard).

**[!UICONTROL Preserve Aspect Ratio]:** Om videons bredd- och höjdproportioner ska behållas (*[!UICONTROL Yes]*) eller för att sträcka ut videon så att den fyller ut det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Lägger till annonser med enbart VAST-taggar; skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla.

**[!UICONTROL Final VAST Tag]:** (Annonserar endast med VAST-taggar; skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla med nödvändiga [Annonsera DSP spårningsmakron](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Clock Number]**: (Används endast i Storbritannien; endast för användare med tillstånd) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen. **Tips:** Redigera pixlar för spårning från tredje part för flera annonser på en plats samtidigt med hjälp av [!UICONTROL Ad Tools] visa, se &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. För den här annonstypen använder du pixlar som aktiveras på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, eller *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP makron](/help/dsp/campaign-management/macros.md)
