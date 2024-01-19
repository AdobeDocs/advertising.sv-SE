---
title: Arbetsflöde för att använda DSP integrering med [!DNL Adobe] [!DNL Real-time CDP]
description: Lär dig hur du aktiverar DSP att importera [!DNL Adobe] [!DNL Real-time CDP] förstahandssegment.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Arbetsflöde för att använda DSP integrering med [!DNL Adobe Real-Time CDP]

1. [Tillåt DSP att översätta kunddatasegment till [!DNL LiveRamp RampIDs]](source-universal-id.md) som är igenkännbara i en anbudsbar miljö.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Skapa en publikkälla](source-create.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto.

1. I Experience Platform konfigurerar du en DSP för annonsering med [!UICONTROL Source Key] som genererades i DSP källinställningar.

   Instruktioner om hur du aktiverar DSP målanslutning, markerar segment och får åtkomst till kontrollbehörigheter finns i &quot;[Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Kontakta ditt kontoteam på Adobe eller `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Aktivera autentiserade segment från universella ID-partners](source-universal-id.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målkälla](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Översikt över målkatalog](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Arbetsflöde för att använda DSP integrering med [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
