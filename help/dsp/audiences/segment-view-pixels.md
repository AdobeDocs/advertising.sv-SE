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

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** på huvudmenyn.

1. Håll markören över segmentraden och klicka på **[!UICONTROL Get Pixel]**.

   * Spårningstaggen för sidvyn, som spårar besökare på datorer och mobila enheter till en webbsida, har etiketten [!UICONTROL Desktop or mobile websites]. För segment som spårar [!DNL ID5] ID:n ersätter du `ID5_PARTNER_ID` i den kopierade taggen med det partner-ID som [!DNL ID5] tilldelades din organisation när den signerade ett avtal med [!DNL ID5]. Om du inte känner till ditt partner-ID kontaktar du ditt Adobe-kontoteam.

     Lägg till taggen på de sidor vars vyer du vill spåra.

   * (Endast anpassade segment) Taggen för visningsspårning, som spårar användare som exponeras för en annonsenhet på datorer, mobilenheter och CTV-enheter, har etiketten [!UICONTROL Desktop or mobile ads]. Lägg till taggen i de annonser vars vyer du vill spåra. Du kan också lägga till taggen på en plats för att som standard bifoga den till alla annonser som är kopplade till placeringen.

När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!MORELIKETHIS]
>
>* [Om målgruppshantering](audience-about.md)
>* [Skapa ett anpassat segment](custom-segment-create.md)
>* [Redigera segmentinformation](segment-edit.md)
>* [Ta bort ett segment](segment-delete.md)
>* [Dela eller sluta dela ett segment](segment-share.md)
