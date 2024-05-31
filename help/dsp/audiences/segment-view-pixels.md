---
title: Visa spårningspixlar för ett segment
description: Lär dig hur du visar spårningspixlar för ett anpassat eller CCPA-avanmäl dig från ett försäljningssegment.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
source-git-commit: 8e3afe50db8f3d0795838c071a01f3c5688f701f
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Visa spårningspixlar för ett segment

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Håll markören över segmentraden och klicka **[!UICONTROL Get Pixel]**.

   * Taggen för spårning av sidvy, som spårar besökare på datorer och mobila enheter till en webbsida, heter &quot;[!UICONTROL Desktop or mobile websites].&quot; För segment som spåras [!DNL ID5] ID, ersätt `ID5_PARTNER_ID` i den kopierade taggen med partner-ID som [!DNL ID5] som tilldelats din organisation när den har signerat ett avtal med [!DNL ID5]. Om du inte känner till ditt partner-ID kontaktar du ditt Adobe-kontoteam.

     Lägg till taggen på de sidor vars vyer du vill spåra.

   * (Endast anpassade segment) Taggen för visningsspårning, som spårar användare som exponeras för en annonsenhet på datorer, mobiler eller CTV-enheter, har etiketten &quot;[!UICONTROL Desktop or mobile ads].&quot; Lägg till taggen i de annonser vars vyer du vill spåra. Du kan också lägga till taggen på en plats för att som standard bifoga den till alla annonser som är kopplade till placeringen.

När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Skapa ett anpassat segment](custom-segment-create.md)
>* [Redigera segmentinformation](segment-edit.md)
>* [Ta bort ett segment](segment-delete.md)
>* [Dela eller Sluta dela ett segment](segment-share.md)
