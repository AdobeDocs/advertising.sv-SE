---
title: Importera autentiserade segment manuellt från  [!DNL LiveRamp]
description: Läs om hur du aktiverar autentiserade målgrupper via  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Importera autentiserade segment manuellt från [!DNL LiveRamp]

*Beta-funktion*

Du kan skicka autentiserade [!DNL LiveRamp] segment manuellt till DSP med kontrollpanelen [!DNL LiveRamp] [!DNL Connect]. Du kan använda importerade segment för placering. För förstapartssegment kostar det 0,15 USD per skärmannons som skickas och 0,25 USD per videoreklam som visas.

Segmentmappningen och överföringen för varje importjobb kan ta upp till sju dagar.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Utför följande steg på kontrollpanelen [!DNL Connect]:

   1. Aktivera målplattan **[!DNL AAC API 1P Onboarding]**.

   1. Ange bara [!DNL Identifier Settings] till **[!DNL Ramp ID]**.

      ![Identifieringsinställningar](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Valfritt) Om du fortfarande vill ta emot cookie-baserade identifierare skapar du en andra [!DNL AAC API 1P Onboarding]-målplatta där [!DNL Cookies], [!DNL IDFA] och [!DNL AAID] är markerade.

   1. Kontrollera i målgruppsbiblioteket (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller i placeringsinställningarna) att hela segmentantalet har importerats.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Anslutning till Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=sv-SE)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
