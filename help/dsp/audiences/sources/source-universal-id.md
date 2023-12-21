---
title: Aktivera autentiserade segment från universella ID-partners
description: Lär dig hur du aktiverar autentiserade målgrupper med en universell ID-lösning.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: e9ff454428d0256402a2ef2fa74f8bd45bd7592f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Aktivera autentiserade segment från universella ID-partners

För att aktivera autentiserade målgrupper via en universell ID-lösning i DSP måste era segment översättas till [!DNL RampIDs], som kan kännas igen i en anbudsbar miljö. Du kan uppnå detta genom att antingen:

* Utnyttja DSP integrering med [!DNL Adobe Real-Time Customer Data Platform (CDP)] och [!DNL Adobe-LiveRamp Retrieval API].

* Skicka autentiserade segment manuellt till DSP från [!DNL LiveRamp] [!DNL Connect] kontrollpanel.

## Uppgifter

1. För båda alternativen kontaktar du `adcloud-support@adobe.com` för att aktivera följande inställningar i DSP, vilket gör att ni kan inrikta er på autentiserade segment i DSP kampanjer en gång [alla steg i aktiveringsarbetsflödet är slutförda](source-adobe-rtcdp.md):

   1. [!DNL LiveRamp] [!DNL RampID] kampanjkonfiguration före segmentdelning från [!DNL Real-Time CDP].

   1. Kontonivån &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Användare delar autentiserade segment manuellt från [!DNL LiveRamp]) Utför följande steg i [!DNL LiveRamp] [!DNL Connect] kontrollpanel:

   1. Aktivera målplattan **[!DNL AAC API 1P Onboarding]**.

   1. Ange [!DNL Identifier Settings] till **[!DNL Ramp ID]** endast.

      ![Identifieringsinställningar](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Valfritt) Om du fortfarande vill få cookie-baserade identifierare skapar du en andra [!DNL AAC API 1P Onboarding] målplatta med &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; och &quot;[!DNL AAID]&quot; har valts.

## Bästa metoder för testning och dataverifiering

* **Mål [!DNL RampID]-baserade segment och cookie-baserade segment i separata kampanjer.**

   * I kampanjinställningarna kan bara en identifierare prioriteras.

   * För närvarande [!DNL RampIDs] går inte att hämta under webbplatshändelser. Det innebär att vissa anpassade mål, som lägsta CPA och ROAS, inte är tillgängliga med autentiserade segment. Använd bara cookie-baserade segment om du har en begränsande KPI för prestanda.

* **Skapa en placering i båda [!DNL RampID] och kakbaserade kampanjer.**

   * Ange segment som delas från [!DNL LiveRamp] med standardprocessen för aktivering av segment.

   * Samarbeta med Adobe Advertising supportteam för att validera datadistributionen.

Läs mer om DSP integration med [!DNL LiveRamp], kontakt `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Aktivera autentiserade segment från målgruppskällor](source-about.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målkälla](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
