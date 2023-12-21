---
title: Skapa en målgruppskälla för att aktivera förstahandspubliker
description: Lär dig hur du skapar en källa för att importera målgrupper till ditt konto eller till ett annonserarkonto.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# Skapa en målgruppskälla för att aktivera förstahandspubliker

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Skapa en källa i DSP för att importera förstahandsmålgrupper till ditt DSP eller ett annonserarkonto.

Ytterligare steg som krävs för att importera segment från specifika kunddataplattformar finns i [målgruppsspecifika arbetsflöden för aktivering](source-about.md)

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicka på **[!UICONTROL Add Source]**.

1. I [!UICONTROL Select a Type] väljer du källtyp.

   * *[!UICONTROL RT-CDP]*: [The [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: [[!DNL Tealium] plattform för kunddata](source-about.md).

1. Ange [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* eller *[!UICONTROL Account]*.

1. Ange återstående [källinställningar](source-settings.md).

   Behåll en kopia av [!UICONTROL Source Key] som genereras. Du behöver värdet senare.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>När du har skapat en källa för din kunddataplattform måste du slutföra ytterligare steg. Se [aktiveringsarbetsflöde för [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> och [aktiveringsarbetsflöde för [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Inställningar för målkälla](source-settings.md)
>* [Aktivera autentiserade segment från målgruppskällor](source-about.md)
>* [Aktivera autentiserade segment från universella ID-partners](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
