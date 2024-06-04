---
title: Inställningar för målkälla
description: Läs mer om inställningarna för målgruppskällor.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Inställningar för målkälla

*Betafunktion*

**[!UICONTROL Data Visibility Level]:** Om segmenten är tillgängliga för en enskild annonsörer med tillgång till kontot (*[!UICONTROL Advertiser]*) eller till alla annonsörer med tillgång till kontot *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Endast annonsnivå) Annonsören som segmenten är tillgängliga för. Välj en i listan över annonsörer med åtkomst till kontot.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] endast källorna) Adobe Experience Cloud organisations-ID för [!DNL Adobe Experience Platform] konto.

**[!UICONTROL Convert PII to the following IDs]:** De ID-typer som du konverterar din personligt identifierbara information till (PII). Om du väljer flera typer fylls det genererade segmentet i med värden för varje vald ID-typ (till exempel en [!DNL RampID] och [!DNL Unified ID2.0] för varje e-postadress). Dataavgifter tillämpas på motsvarande sätt.

För [!DNL RampID] och [!DNL Unified ID2.0]söker leverantören upp varje e-postadress för att se om det redan finns ett ID och översätter adressen till ett matchande ID när den är tillgänglig. Om det inte finns något ID för adressen skapas ett nytt ID.

>[!NOTE]
>
>Du kan bara ange en typ av ID som mål på en enda placering. Om du vill testa prestanda efter ID-typ [skapa en separat placering](/help/dsp/campaign-management/placements/placement-create.md) för varje ID-typ i segmentet.

* *[!DNL RampID]:* Konvertera PII till [!DNL RampID]. Du kan använda [!DNL RampIDs] för återannonsering av inloggningsanvändare och för [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) mätning.

* *[!DNL Unified ID2.0](Beta):* Konvertera PII till [Enhetligt ID 2.0](https://unifiedid.com) ID för återmarknadsföring av inloggningsanvändare.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Villkor för serviceavtal för konvertering av PII till universella ID:n. Du eller en annan användare på DSP måste acceptera villkoren en gång innan du kan konvertera data till en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren å din organisations vägnar. Om du vill läsa villkoren klickar du **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Skrivskyddat, genererat automatiskt) Den källnyckel du kan använda för att skapa en målanslutning i kunddataplattformen för att dirigera målgrupper till DSP. Du kan kopiera värdet till Urklipp och klistra in det i inställningarna för målanslutningen eller i en fil.

>[!MORELIKETHIS]
>
>* [Skapa en målgruppskälla för att aktivera universella ID-målgrupper](source-create.md)
>* [Om källor för förstagångspubliker](source-about.md)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
