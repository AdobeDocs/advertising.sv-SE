---
title: Annonsinställningar för inbyggd bildskärm
description: Se beskrivningar av tillgängliga annonsinställningar för inbyggda displayannonser.
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Annonsinställningar för inbyggd bildskärm

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Annonstypen används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i [!UICONTROL Ads]-vyn och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. Heldagsproduktförhandsvisning: 15sec Native&quot;).

**[!UICONTROL Native Creative]:** En bild på 1 200 x 627 som maximerar leveransen på mobilt lager. Klicka på **[!UICONTROL Browse]**, leta upp filen på enheten eller i nätverket och klicka sedan på **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** En iögonfallande titel för att engagera tittarna.

**[!UICONTROL Description]:** Annonsens brödtext. Maximala längden är 100 tecken.

**[!UICONTROL Landing Page]:** Den URL som visningsprogrammet hamnar på när de klickar på annonsen.

**[!UICONTROL Final Landing Page]:** URL:en [!UICONTROL Landing Page] med nödvändiga [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Sponsored By (Advertiser Name)]:** Annonsens annonsörer.

**[!UICONTROL Call to Action]:** (Valfritt) Det steg som du vill att tittarna ska ta när annonsen har visats.

**[!UICONTROL Advertiser Logo]:** (Valfritt) En 1:1-logotyp som ska inkluderas med annonsen för mer varumärkesigenkänning. Klicka på **[!UICONTROL Browse]**, leta upp filen på enheten eller i nätverket och klicka sedan på **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen. **Tips!** Om du vill redigera tredjepartspixlar för spårning av annonser för flera annonser på en plats samtidigt i vyn [!UICONTROL Ad Tools] ska du läsa &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Händelsen som utlöser pixeln att utlösa. Det enda alternativet för den här annonstypen är *[!UICONTROL Impression]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för angiven [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* eller *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP makron](/help/dsp/campaign-management/macros.md)
