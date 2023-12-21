---
title: Inställningar för målkälla
description: Läs mer om inställningarna för målgruppskällor.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Inställningar för målkälla

**[!UICONTROL Data Visibility Level]:** Om segmenten är tillgängliga för en enskild annonsörer med tillgång till kontot (*[!UICONTROL Advertiser]*) eller till alla annonsörer med tillgång till kontot *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Endast annonsnivå) Annonsören som segmenten är tillgängliga för. Välj en i listan över annonsörer med åtkomst till kontot.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] endast källorna) Adobe Experience Cloud organisations-ID för [!DNL Adobe Experience Platform] konto.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] och [!DNL Tealium] Endast källor) Den ID-typ som du vill konvertera din personligt identifierbara information till (PII). Dataavgifter tillämpas på motsvarande sätt.

* *[!DNL RampID]:* Konvertera PII till ett rampID. Om du väljer *[!DNL RampID]*&#x200B;översätts era segment till [!DNL RampIDs] automatiskt.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] endast källor) Konvertera PII till [Enhetligt ID 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Skrivskyddat, genererat automatiskt) Den källnyckel du kan använda för att skapa en målanslutning i kunddataplattformen för att dirigera målgrupper till DSP. Du kan kopiera värdet till Urklipp och klistra in det i inställningarna för målanslutningen eller i en fil.

>[!MORELIKETHIS]
>
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Aktivera autentiserade segment från målgruppskällor](source-about.md)
>* [Aktivera autentiserade segment från universella ID-partners](source-universal-id.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
