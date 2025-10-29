---
title: Inställningar för ansluten TV-annons
description: Se beskrivningar av tillgängliga annonsinställningar för anslutna TV-annonser.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Inställningar för ansluten TV-annons

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]**: VAST-taggens URL.

**[!UICONTROL Title]**: Ett namn för filen, som används i annonsvyn och rapporter.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära överkanten.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i [!UICONTROL Ads]-vyn och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. heldagsproduktsförhandsvisning: 30sek CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height | Ad Unit Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** Annonsenhetens X-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Annonsenhetens Y-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Var ska videokontroller för annonsen inkluderas? *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* eller *[!UICONTROL None]* (standardvärdet).

**[!UICONTROL Preserve Aspect Ratio]:** Om bredd- och höjdproportionerna för videon ska behållas (*[!UICONTROL Yes]*) eller om videon ska sträckas ut för att fylla det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla.

**[!UICONTROL Final VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla med nödvändiga [Advertising DSP-spårningsmakron](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Clock Number]**: (Används endast i Storbritannien, endast för användare med behörighet) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP-makron](/help/dsp/campaign-management/macros.md)
