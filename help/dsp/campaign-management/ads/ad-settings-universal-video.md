---
title: Universella inställningar för videoreklam
description: Se beskrivningar av tillgängliga annonsinställningar för universella videoannonser.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Universella inställningar för videoreklam

>[!NOTE]
>
>Universella videoannonser kan bara bifogas till universella videomaterial.

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]:** VAST-taggens URL.

**[!UICONTROL Title]:** En rubrik för filen, som finns i vyn [!UICONTROL Ads] och rapporter.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` i närheten av den övre delen.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i [!UICONTROL Ads]-vyn och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. Holiday Product Preview: 30sec Universal Video&quot;).

**[!UICONTROL Show Controls]:** Var ska videokontroller för annonsen inkluderas? *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* eller *[!UICONTROL None]* (standardvärdet).

**[!UICONTROL Preserve Aspect Ratio]:** Om bredd- och höjdproportionerna för videon ska behållas (*[!UICONTROL Yes]*) eller om videon ska sträckas ut för att fylla det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla.

**[!UICONTROL Final VAST Tag]:** (Lägger till med endast VAST-taggar, skrivskyddat) Den VAST-tagg från tredje part som du angav som annonskälla med nödvändiga [Advertising DSP-spårningsmakron](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Wmode]:** Fönsterläget: *[!UICONTROL window]*, *[!UICONTROL transparent]* eller *[!UICONTROL opaque]*. Om den här inställningen inte är tillämplig lämnar du den tom.

**[!UICONTROL Video Format]:** Annonsspelarens format för potentiell inventering: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* eller *[!UICONTROL VAST]*. Visningsbarheten mäts alltid för [!UICONTROL VPAID], men [!UICONTROL VPAID & VAST] innehåller lager som inte tillåter visning. Tänk på den här skillnaden om mätvärden för visningsbarhet är viktiga för er kampanj.

Använd [!UICONTROL VAST], som inte tillåter visningsmätning, när du har en ansluten TV eller ett lager som endast kräver VAST-format (vanligtvis från leverantörer som Google Ad Manager, Appnexus, SpotX och Freewheel) som mål. Använd även det här alternativet för lager som tidigare var kompatibla med förrullningar/annonser av standardtyp (VAST) eller telefon + surfplatta av standardtyp (VAST).

**[!UICONTROL Clock Number]**: (Används endast i Storbritannien, endast för användare med behörighet) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP-makron](/help/dsp/campaign-management/macros.md)
