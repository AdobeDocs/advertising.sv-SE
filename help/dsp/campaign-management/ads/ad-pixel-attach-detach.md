---
title: Bifoga och ta bort pixlar från annonser
description: Lär dig hur du bifogar och tar bort pixlar för spårning från tredje part från annonser.
feature: DSP Ads
exl-id: 7b386a58-5300-49cf-9de8-4ce982a5181d
source-git-commit: 3538c1d881a3032863c5a6f8c7361ac1c0bc35f9
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Bifoga och ta bort pixlar från annonser

Du kan bifoga och frigöra pixlar från annonser från tredjepartsspårning.

## Öppna vyn [!UICONTROL Ad Tools] {#ad-tools-open}

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Öppna vyn [!UICONTROL Ad Tools] på något av följande sätt:

   * (I vyn [!UICONTROL Campaigns]) Klicka på **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]bredvid kampanjnamnet.**

   * (I vyn [!UICONTROL Packages], [!UICONTROL Placements] eller [!UICONTROL Ads]) Klicka **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]** i det övre högra hörnet.

## Koppla pixlar för spårning från tredje part till annonser på en plats {#attach-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools]-vyn](#ad-tools-open).

   Fliken **[!UICONTROL Attach Pixels]** öppnas.

1. I undervyn [!UICONTROL Edit]:

   1. (Valfritt) Hitta annonser och tredjepartspixlar på något av följande sätt:

      * Ovanför den vänstra tabellen klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrerar listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

      * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

   1. (Om det inte finns några pixlar för spårning från tredje part för kampanjen) Skapa en pixel:

      1. Klicka på **[!UICONTROL Create pixel]** i den högra tabellen.

      1. Ange inställningarna:

         **[!UICONTROL Integration Event]:** Händelsen som utlöser pixeln att utlösa, till exempel *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

         **[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

         **[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* eller *[!UICONTROL IAS]*.

      1. Klicka på **[!UICONTROL Save]**.

   1. I den vänstra tabellen markerar du kryssrutan bredvid varje annons för vilken du vill koppla pixlar för spårning från tredje part.

   1. I den högra tabellen markerar du kryssrutan bredvid varje spårningspixel från tredje part som du vill koppla till de valda annonserna.

      Endast pixlar som inte redan är kopplade till de markerade annonserna kan markeras.

   1. Klicka på **[!UICONTROL Attach]** längst ned till höger.

1. (Valfritt) Om du vill återgå till kampanjinformationsvyerna klickar du på ![Återgå till mappen](/help/dsp/assets/breadcrumb-return.png "Återgå till mappen") till vänster om [!UICONTROL Ad Tools] och väljer kampanjnamnet.

## Frigöra pixlar för spårning från tredje part från annonser i en placering {#detach-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools]-vyn](#ad-tools-open).

   Fliken **[!UICONTROL Attach Pixels]** öppnas.

1. I undervyn [!UICONTROL Edit]:

   1. (Valfritt) Hitta annonser och tredjepartspixlar på något av följande sätt:

      * Ovanför den vänstra tabellen klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrerar listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

      * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

   1. I den vänstra tabellen markerar du kryssrutan bredvid varje annons från vilken du vill koppla loss pixlar för spårning från tredje part.

   1. I den högra tabellen markerar du kryssrutan bredvid varje spårningspixel från tredje part som du vill koppla loss från de markerade annonserna.

      Endast pixlar som är kopplade till alla markerade annonser kan markeras.

   1. Klicka på **[!UICONTROL Detach]** längst ned till höger.

1. (Valfritt) Om du vill återgå till kampanjinformationsvyerna klickar du på ![Återgå till mappen](/help/dsp/assets/breadcrumb-return.png "Återgå till mappen") till vänster om [!UICONTROL Ad Tools] och väljer kampanjnamnet.

## Visa pixlar kopplade till annonser {#view-pixels-ads}

1. [Öppna [!UICONTROL Ad Tools]-vyn](#ad-tools-open).

   Fliken **[!UICONTROL Attach Pixels]** öppnas.

1. Växla till alternativet **[!UICONTROL View]** längst upp till höger.

1. (Valfritt) Hitta annonser och tredjepartspixlar efter behov:

   * Ovanför den vänstra tabellen klickar du på ![Filter](/help/dsp/assets/filter.png) och filtrerar listorna efter annonsstatus, annonstyp, pixelintegreringshändelse eller pixeltyp.

   * Ovanför den högra och vänstra tabellen söker du efter specifika textsträngar i annonsnamnen och pixelnamnen.

1. Klicka på en annonsrad i den vänstra tabellen för att visa de kopplade pixlarna i den högra tabellen.

1. (Valfritt) Om du vill bifoga fler pixlar till annonserna växlar du till vyn **[!UICONTROL Edit]** i det övre högra hörnet. Mer information finns i steg 3 i den föregående proceduren, [Koppla tredjepartsspårning av pixlar till annonser i en placering](#attach-pixels-ads).

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Bifoga annonser till placeringar](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Redigera en annons](ad-edit.md)
>* [Visa en lista över placeringar som är associerade med en annons](ad-list-placements.md)
>* [Redigera annonsplanerna för placeringar](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)
