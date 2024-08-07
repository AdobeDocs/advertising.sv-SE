---
title: Ljudannonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för ljudannonser.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Ljudannonsinställningar

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]**: VAST-taggens URL.

**[!UICONTROL Title]**: Ett namn för filen, som används i vyn och rapporterna för [!UICONTROL Ads].

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära överkanten.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till. Standardvärdet är *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i [!UICONTROL Ads]-vyn och i rapporter. Beskriv t.ex. enhetstypen och vissa nyckelattribut (t.ex. heldagsproduktförhandsvisning: 30sek-ljud&quot;).

**[!UICONTROL Ad Duration]:** Längden på ljudfilen. Den anges automatiskt som antingen [!UICONTROL 15] eller [!UICONTROL 30], beroende på den valda annonsenheten.

Det här fältet kanske visas eller inte, beroende på kontobehörigheterna.

**[!UICONTROL VAST Tag]:** (Lägger till med endast VAST-taggar) En URL för en annonskälla från tredje part. Kontrollera att VAST-taggen bara innehåller ljudmediefiler.

**[!UICONTROL Final VAST Tag]:** (Lägger till med endast VAST-taggar) URL:en för tredjeparts annonskälla med nödvändiga [Advertising DSP-spårningsmakron](/help/dsp/campaign-management/macros.md) infogade, om tillämpligt.

**[!UICONTROL Select Rate]:** (Användare med endast behörighet) En förförhandlad ränta som faktureras via Adobe, eller en av de priser som du har förhandlat och som faktureras via leverantören. Om du vill lägga till en avgift kontaktar du kontoteamet på Adobe.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen. **Tips!** Om du vill redigera tredjepartspixlar för spårning av annonser för flera annonser på en plats samtidigt i vyn [!UICONTROL Ad Tools] ska du läsa &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Händelsen som utlöser pixeln att utlösa. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* eller *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är associerade med en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP makron](/help/dsp/campaign-management/macros.md)
