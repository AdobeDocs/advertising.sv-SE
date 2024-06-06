---
title: Importera autentiserade segment manuellt från [!DNL LiveRamp]
description: Läs om hur du aktiverar autentiserade målgrupper via [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Importera autentiserade segment manuellt från [!DNL LiveRamp]

*Betafunktion*

Du kan skicka autentiserade manuellt [!DNL LiveRamp] segment att DSP med [!DNL LiveRamp] [!DNL Connect] kontrollpanel. Du kan använda importerade segment för placering. För förstapartssegment kostar det 0,15 USD per skärmannons som skickas och 0,25 USD per videoreklam som visas.

Segmentmappningen och överföringen för varje importjobb kan ta upp till sju dagar.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Utför följande steg i [!DNL Connect] kontrollpanel:

   1. Aktivera målplattan **[!DNL AAC API 1P Onboarding]**.

   1. Ange [!DNL Identifier Settings] till **[!DNL Ramp ID]** endast.

      ![Identifieringsinställningar](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Valfritt) Om du fortfarande vill få cookie-baserade identifierare skapar du en andra [!DNL AAC API 1P Onboarding] målplatta med &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; och &quot;[!DNL AAID]&quot; har valts.

   1. Verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att hela segmentantalet importerades.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Inställningar för målkälla](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
