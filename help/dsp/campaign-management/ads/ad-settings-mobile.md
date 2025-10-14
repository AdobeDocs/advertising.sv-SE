---
title: Inställningar för mobilannonsering
description: Se beskrivningar av tillgängliga annonsinställningar för mobilannonser.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Inställningar för mobilannonsering

## [!UICONTROL Insert Ad Tag]

*Nya videoannonseringsformat för mobiler endast*

**[!UICONTROL URL]** eller **[!UICONTROL Ad Tag]**: En VAST-annonstagg eller annonstagg från tredje part som innehåller kreativa resurser och spårar pixlar

**[!UICONTROL Ad Title]** eller **[!UICONTROL Title]**: Ett namn på annonsen som används i vyn och rapporterna för [!UICONTROL Ads].

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära överkanten.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Mobilvisningsannonser

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Holiday Product Preview: 300x250 Gamer&quot;).

**\[Lägg till Source\]**: (skrivskyddat) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** Webbadressen till den kreativa resursen från tredje part. Alla parametrar för [tidsstämpel] och [[tidsstämpel]] ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** URL:en för den kreativa resursen från tredje part, där nödvändiga [Advertising DSP spårningsmakron &#x200B;](/help/dsp/campaign-management/macros.md) infogas, om tillämpligt.

### [!UICONTROL Basic]: Videobandspelare

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. heldagsproduktsförhandsvisning: 30sek telefoninledning&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** Annonsenhetens X-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Annonsenhetens Y-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Var ska videokontroller för annonsen inkluderas? *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* eller *[!UICONTROL None]* (standardvärdet).

**[!UICONTROL Preserve Aspect Ratio]:** Om bredd- och höjdproportionerna för videon ska behållas (*[!UICONTROL Yes]*) eller om videon ska sträckas ut för att fylla det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Vissa annonstyper) Antal sekunder som stängningsknappens utseende ska fördröjas.

**[!UICONTROL VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som kreativ resurs.

**[!UICONTROL Final VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som den kreativa resursen med nödvändiga [Advertising DSP-spårningsmakron](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Wmode]:** (Vissa annonstyper) Fönsterläget: *[!UICONTROL window]*, *[!UICONTROL transparent]* eller *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen. **Tips!** Om du vill redigera tredjepartspixlar för spårning av annonser för flera annonser på en plats samtidigt i vyn [!UICONTROL Ad Tools] ska du läsa &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)&quot;.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Händelsen som utlöser pixeln att utlösa. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för angiven [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* eller *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Föråldrat

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP-makron](/help/dsp/campaign-management/macros.md)
