---
title: Bifoga annonser till placeringar
description: Lär dig hur du bifogar annonser till praktik.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Bifoga annonser till placeringar

Använd [!UICONTROL Ad Tools] för att bifoga annonser till praktik, bifoga pixlar för spårning från tredje part till annonserna och frigöra befintliga pixlar för spårning från tredje part från annonserna.

>[!NOTE]
>
>Universella videoannonser kan bara bifogas till universella videomaterial.

## Öppna [!UICONTROL Ad Tools] Visa {#ad-tools-open}

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Öppna [!UICONTROL Ad Tools] visa på något av följande sätt:

   * (Från [!UICONTROL Packages] , [!UICONTROL Placements], eller [!UICONTROL Ads] vy) Klicka på uppe till höger **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Från [!UICONTROL Placements] vy) Bredvid placeringsnamnet klickar du på **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Från [!UICONTROL Ads] vy) Bredvid annonsnamnet klickar du på  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   The [!UICONTROL Attach Ads] -fliken är markerad som standard.

## Bifoga annonser till placeringar {#attach-ads-campaign}

1. [Öppna [!UICONTROL Ad Tools] visa](#ad-tools-open).

1. I [!UICONTROL Edit] gör du följande för varje grupp med annonser som du vill bifoga till placeringar:

   1. (Valfritt) Hitta specifika placeringar och annonser på något av följande sätt:

      * Ovanför vänster tabell klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrera listorna efter paket, placeringstyp, placeringsstatus, annonstyp eller annonsstatus.

      * Sök efter specifika textsträngar i placerings- och annonsnamnen ovanför den högra och den vänstra tabellen.

   1. I den vänstra tabellen markerar du kryssrutan bredvid varje placering som annonserna ska kopplas till.

   1. I den högra tabellen markerar du kryssrutan bredvid varje annons som du vill bifoga till de markerade placeringarna.

      Endast annonser som gäller för placeringstypen och som inte redan är kopplade till de valda placeringarna kan markeras.

   1. Klicka längst ned till höger på **[!UICONTROL Attach]**.

1. (Valfritt) Om du vill återgå till kampanjdetaljvyerna klickar du på ![Återgå till mappen](/help/dsp/assets/breadcrumb-return.png "Återgå till mappen") till vänster om [!UICONTROL Ad Tools] och välj kampanjnamnet.

## Visa annonser som är kopplade till placeringar {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Öppna [!UICONTROL Ad Tools] visa](#ad-tools-open).

1. Växla till **[!UICONTROL View]** i det övre högra hörnet.

1. (Valfritt) Sök efter specifika placeringar och annonser efter behov:

   * Ovanför vänster tabell klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrera listorna efter paket, placeringstyp, placeringsstatus, annonstyp eller annonsstatus.

   * I den högra och vänstra tabellen söker du efter specifika textsträngar i placerings- eller annonsnamnet.

1. Klicka på en placeringsrad i den vänstra tabellen för att se de bifogade annonserna i den högra tabellen.

1. (Valfritt) Om du vill bifoga fler annonser till kampanjens praktik byter du till **[!UICONTROL Edit]** i det övre högra hörnet. Se steg 2 i föregående procedur, &quot;[Bifoga annonser till placeringar](#attach-ads-campaign),&quot; för instruktioner.

## Koppla tredjepartsspårning av pixlar till annonser i en placering {#attach-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools] visa](#ad-tools-open).

1. Klicka på **[!UICONTROL Attach Pixels]** -fliken.

1. I [!UICONTROL Edit] undervy:

   1. (Valfritt) Hitta annonser och tredjepartspixlar på något av följande sätt:

      * Ovanför vänster tabell klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrera listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

      * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

   1. (Om det inte finns några pixlar för spårning från tredje part för kampanjen) Skapa en pixel:

      1. Klicka på i den högra tabellen **[!UICONTROL Create pixel]**.

      1. Ange inställningarna:

         **[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses, till exempel *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

         **[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

         **[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, eller *[!UICONTROL IAS]*.

      1. Klicka på **[!UICONTROL Save]**.

   1. I den vänstra tabellen markerar du kryssrutan bredvid varje annons för vilken du vill koppla pixlar för spårning från tredje part.

   1. I den högra tabellen markerar du kryssrutan bredvid varje spårningspixel från tredje part som du vill koppla till de valda annonserna.

      Endast pixlar som inte redan är kopplade till de markerade annonserna kan markeras.

   1. Klicka längst ned till höger på **[!UICONTROL Attach]**.

1. (Valfritt) Om du vill återgå till kampanjdetaljvyerna klickar du på ![Återgå till mappen](/help/dsp/assets/breadcrumb-return.png "Återgå till mappen") till vänster om [!UICONTROL Ad Tools] och välj kampanjnamnet.

## Koppla loss pixlar från tredjepartsspårning från annonser i en placering {#detach-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools] visa](#ad-tools-open).

1. Klicka på **[!UICONTROL Attach Pixels]** -fliken.

1. I [!UICONTROL Edit] undervy:

   1. (Valfritt) Hitta annonser och tredjepartspixlar på något av följande sätt:

      * Ovanför vänster tabell klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrera listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

      * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

   1. I den vänstra tabellen markerar du kryssrutan bredvid varje annons från vilken du vill koppla loss pixlar för spårning från tredje part.

   1. I den högra tabellen markerar du kryssrutan bredvid varje spårningspixel från tredje part som du vill koppla loss från de markerade annonserna.

      Endast pixlar som är kopplade till alla markerade annonser kan markeras.

   1. Klicka längst ned till höger på **[!UICONTROL Detach]**.

1. (Valfritt) Om du vill återgå till kampanjdetaljvyerna klickar du på ![Återgå till mappen](/help/dsp/assets/breadcrumb-return.png "Återgå till mappen") till vänster om [!UICONTROL Ad Tools] och välj kampanjnamnet.

## Visa pixlar som är kopplade till annonser {#view-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools] visa](#ad-tools-open).

1. Klicka på **[!UICONTROL Attach Pixels]** -fliken.

1. Växla till **[!UICONTROL View]** i det övre högra hörnet.

1. (Valfritt) Hitta annonser och tredjepartspixlar efter behov:

   * Ovanför vänster tabell klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrera listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

   * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

1. Klicka på en annonsrad i den vänstra tabellen för att visa de kopplade pixlarna i den högra tabellen.

1. (Valfritt) Om du vill bifoga fler pixlar till annonserna växlar du till **[!UICONTROL Edit]** i det övre högra hörnet. Se steg 3 i föregående procedur, &quot;[Koppla tredjepartsspårning av pixlar till annonser i en placering](#attach-pixels-ads),&quot; för instruktioner.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Redigera en annons](ad-edit.md)
>* [Visa en lista över placeringar som är kopplade till en annons](ad-list-placements.md)
>* [Redigera annonsplanerna för praktik](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)
