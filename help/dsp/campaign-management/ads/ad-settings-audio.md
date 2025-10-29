---
title: Ljudannonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för ljudannonser.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
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

**[!UICONTROL Select Rate]:** (Användare med endast behörighet) En förförhandlad ränta som faktureras via Adobe, eller en av de priser som du har förhandlat och som faktureras via leverantören. Om du vill lägga till en avgift kontaktar du ditt Adobe-kontoteam.

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
