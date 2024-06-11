---
title: Hantera målgruppskällor för att aktivera universella ID-målgrupper
description: Lär dig hur du skapar och hanterar en källa för att importera målgrupper från din kunddataplattform och konvertera dem till segment som innehåller universella ID:n.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 78b1a8a8e0567afb0c172c7bef1a639ab5b47bab
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Hantera målgruppskällor för att aktivera universella ID-målgrupper

*Betafunktion*

Skapa en källa i DSP för varje enskild målgrupp på kunddataplattformen som du vill konvertera till segment som innehåller angivna universella ID-typer. Du kan importera segmenten till din organisations DSP eller till ett annonsörskonto. Dataavgifter tillämpas baserat på de valda universella ID-typerna. När du har skapat en källa krävs ytterligare steg för att importera målgrupperna från varje kunddataplattform. Se kommentaren i slutet av proceduren för att skapa en källa.

Du kan senare ändra de universella ID-typer som källmålgruppen översätts till och visa en logg över ändringarna.

Du kan också ta bort en källa.

## Skapa en publikkälla

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicka på **[!UICONTROL Add Source]**.

1. I [!UICONTROL Select a Type] väljer du [plattform för kunddata](source-about.md):

   * *[!UICONTROL RT-CDP]*: [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*: [!DNL ActionIQ] plattform för kunddata.

   * *[!UICONTROL Amperity]*: [!DNL Amperity] plattform för kunddata.

   * *[!UICONTROL Optimizely]*: [!DNL Optimizely]: [!DNL Amperity] plattform för kunddata.

   * *[!UICONTROL Tealium CDP]*: (Endast konfigurerade användare) [!DNL Tealium] plattform för kunddata.

1. Ange [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* eller *[!UICONTROL Account]*.

1. Ange återstående [källinställningar](#source-settings).

   Behåll en kopia av [!UICONTROL Source Key] som genereras. Du behöver värdet senare.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>När ni har skapat en källa för er kunddataplattform måste ni slutföra ytterligare steg för att importera er målgrupp. Se [arbetsflöde [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> den [arbetsflöde [!DNL Amperity]](source-amperity.md), [arbetsflöde [!DNL Optimizely]](source-optimizely.md)och [arbetsflöde [!DNL Tealium]](source-tealium.md).

## Ändra ID-typer för en målkälla

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Edit]**.

1. Ändra [ID som valts för källan](#source-settings).

1. Klicka på **[!UICONTROL Save]**.

## Ta bort en publikkälla

När du tar bort en källa tas de segment som översatts genom källan bort.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]**.

## Visa ändringsloggen för en publikkälla

Du kan visa information om ändringar i en målgruppskällpost och eventuellt bifoga anteckningar till loggen.

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Change log]**.

1. (Valfritt) Så här bifogar du en anteckning till ändringsloggen:

   1. Håll markören över källraden och klicka **[!UICONTROL Add Notes]**.

   1. Skriv anteckningen och klicka sedan på **[!UICONTROL Save]**.

      Maximala längden är 256 tecken.

1. (Valfritt) Om du vill öppna loggen på en större detaljskärm håller du markören över källraden och klickar på **[!UICONTROL View Details]**.

## Inställningar för målkälla {#source-settings}

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
>* [Om källor för förstagångspubliker](source-about.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Amperity] till universella ID](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertera användar-ID:n från [!DNL Optimizely] till universella ID](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID](/help/dsp/audiences/sources/source-tealium.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
