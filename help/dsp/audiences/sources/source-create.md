---
title: Skapa en målgruppskälla för att aktivera förstahandspubliker
description: Lär dig hur du skapar en källa för att importera målgrupper till ditt konto eller till ett annonserarkonto.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 9ca42d078c0d0b6a08d521c8465eca69c2affce5
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Skapa en målgruppskälla för att aktivera förstahandspubliker

*Betafunktion*

<!-- Will this remain for admin users/Adobe account teams only? -->

Skapa en källa för att importera målgrupper till ditt DSP eller ett annonserarkonto. För närvarande kan du importera målgrupper från [den [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>När du har skapat en källa för [!DNL Real-Time CDP]måste du aktivera [!DNL Real-Time CDP] målgrupper genom Adobe Advertising DSP destination inom [!DNL Real-Time CDP] för att börja importera dem. Se [stegen i aktiveringsarbetsflödet](source-about.md#workflow-sources).

1. På huvudmenyn klickar du på **[!UICONTROL Audiences]** > **[!UICONTROL Sources (BETA)].

1. Klicka på [!UICONTROL Add Source].

1. I [!UICONTROL Select a Type] väljer du källtyp.

   *[!UICONTROL RT-CDP]*: Den här källtypen för [den [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), är det enda alternativet.

1. Ange [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* eller *[!UICONTROL Account]*.

1. Ange återstående [källinställningar](source-settings.md).

   Behåll en kopia av [!UICONTROL Source Key] som genereras. Du behöver värdet senare.

1. Klicka på **[!UICONTROL Save]**.

1. I Experience Platform skapar du en DSP målanslutning med [!UICONTROL Source Key] som genererades i DSP källinställningar.

   Instruktioner om hur du aktiverar DSP målanslutning, markerar segment och får åtkomst till kontrollbehörigheter finns i &quot;[Adobe Advertising Cloud DSP-anslutning](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Inställningar för målgruppskälla](source-settings.md)
>* [Om aktivering av autentiserade segment från målgruppskällor](source-about.md)
>* [Aktivera autentiserade segment från varaktiga ID-partners](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP-anslutning](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)

