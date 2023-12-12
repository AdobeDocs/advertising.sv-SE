---
title: Skapa och implementera ett anpassat segment
description: Lär dig hur du skapar och implementerar ett anpassat segment för att spåra användare som exponeras för annonser eller användare som besöker dina webbsidor.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Skapa och implementera ett anpassat segment

Ni kan samla in era egna data från förstapartsmålgrupper genom att skapa och implementera ett anpassat DSP. Du kan använda segmentet för att spåra a) användare som exponeras för annonser från datorer och mobila enheter och b) användare som besöker specifika webbsidor. Du kan senare rikta om användare i segmentet med ytterligare annonser eller hindra användare i segmentet från att få ytterligare annonser.

>[!NOTE]
>
>Om du vill spåra användar-ID:n från förfrågningar om avanmälan till försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA), skapar du en [CCPA Avanmäl segmentet](ccpa-opt-out-segment-create.md).

1. Skapa segmentet:

   1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Ovanför datatabellen klickar du **[!UICONTROL Create]**.

   1. Ange ett unikt **[!UICONTROL Segment Name]**.

   1. För **[!UICONTROL Segment Type]**, markera *[!UICONTROL Custom]*.

   1. Ange **[!UICONTROL Segment Window]**, vilket är antalet dagar som en användares cookie stannar kvar i segmentet.

      Standardfönstret är 45 dagar. Ange ett värde mellan 1 och 365.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera taggar för att spåra segmentet efter behov:

   1. Återgå till **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Håll markören över segmentraden och klicka **[!UICONTROL Get Pixel]**.

      * Så här spårar du besökare på en webbsida:

         1. Kopiera spårningstaggen för sidvyn, som har etiketten[!UICONTROL Desktop or mobile websites].&quot;

         1. Ange taggen till annonsören eller webbplatskontakten för distribution.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      * Så här spårar du användare som exponeras för en annonsenhet på datorer eller mobila enheter:

         1. Kopiera taggen för visningsspårning, som har etiketten &quot;[!UICONTROL Desktop or mobile ads].&quot;

1. Lägg till taggen i antingen [!UICONTROL Pixel] för varje relevant annons eller för [!UICONTROL Event Pixels] i [[!UICONTROL Tracking] inställningar för varje relevant placering](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!TIP]
>
>Håll reda på segmentstorleken när användarna spåras.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Redigera segmentinformation](segment-edit.md)
>* [Ta bort ett segment](segment-delete.md)
>* [Visa spårningspixlar för ett segment](segment-view-pixels.md)
>* [Dela eller Sluta dela ett segment](segment-share.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
