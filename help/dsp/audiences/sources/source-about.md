---
title: Aktivera autentiserade segment från målgruppskällor
description: Lär dig mer om hur man hämtar in förstahandssegment från en kunddataplattform.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: e3e8753db31bc835c49eb2037fdcd7696a895a8c
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Aktivera autentiserade segment från målgruppskällor

DSP kan importera förstahandssegment som består av hash-kodade e-post-ID:n eller universella ID:n som skapats inom en kunddataplattform (CDP). Du kan använda de kapslade segmenten som mål för dina placeringar.

Följande CDP:er har upprättat anslutningar, men DSP kan även ansluta till valfri CDP med batchbaserad, direktuppspelad eller API-baserad datadelning. Om du vill integrera med en ny CDP kontaktar du kontoteamet på Adobe.

## [!DNL Adobe Real-Time Customer Data Platform]

DSP är integrerat med [den [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), som ingår i Adobe Experience Platform.

I [!DNL Real-Time CDP], *mål* är anslutningar till externa dataplattformar som möjliggör smidig dataaktivering. Du kan till exempel använda destinationer för att aktivera dina kända kundrelationer (till exempel hash-kodade e-postadresser) för riktad reklam i olika digitala format som stöds av DSP. Mer information om destinationer finns i Experience Platform [Destinationshandbok](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), inklusive en översikt över produkten, instruktioner för [skapa målarbetsytor](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) och [skapa målanslutningar](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)och [aktivera data till mål](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Se &quot;[Arbetsflöde för att använda DSP integrering med [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

## [!DNL ActionIQ]

Du kan dela organisationens egna data från [!DNL Action IQ] plattform för kunddata med DSP. Sedan kan du ange DSP för segmenten med [!DNL RampIDs] eller [!DNL Unified IDs 2.0].

Den här integreringen kräver anpassning. Kontakta kontoteamet på Adobe för mer information.

## [!DNL Tealium]

Du kan dela organisationens egna data från [!DNL Tealium] kunddataplattform som använder [!DNL Amazon Web Services]. Sedan kan du ange DSP för segmenten med [!DNL RampIDs]. Se &quot;[Arbetsflöde för att använda DSP integrering med [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Arbetsflöde för att använda DSP integrering med [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Arbetsflöde för att använda DSP integrering med [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målkälla](source-settings.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
