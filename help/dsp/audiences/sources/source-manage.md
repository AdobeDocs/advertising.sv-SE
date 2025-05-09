---
title: Hantera målgruppskällor för att aktivera universella ID-målgrupper
description: Lär dig hur du skapar och hanterar en källa för att importera målgrupper från din kunddataplattform och konvertera dem till segment som innehåller universella ID:n.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Hantera målgruppskällor för att aktivera universella ID-målgrupper

*Beta-funktion*

Skapa en källa i DSP för varje enskild målgrupp på kunddataplattformen som du vill konvertera till segment som innehåller angivna universella ID-typer. Du kan importera segmenten till din organisations DSP eller till ett annonsörskonto. Dataavgifter tillämpas baserat på de valda universella ID-typerna. När du har skapat en källa krävs ytterligare steg för att importera målgrupperna från varje kunddataplattform. Se kommentaren i slutet av proceduren för att skapa en källa.

Du kan senare ändra de universella ID-typer som källmålgruppen översätts till och visa en logg över ändringarna.

Du kan också ta bort en källa.

## Skapa en målgrupps-Source

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** på huvudmenyn.

1. Klicka på **[!UICONTROL Add Source]**.

1. Välj din [kunddataplattform](source-about.md) på menyn [!UICONTROL Select a Type]:

   * *[!UICONTROL RT-CDP]*: [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]*: [!DNL ActionIQ]-kunddataplattformen.

   * *[!UICONTROL Amperity]*: [!DNL Amperity]-kunddataplattformen.

   * *[!UICONTROL Optimizely]*: [!DNL Optimizely]-kunddataplattformen.

   * *[!UICONTROL Tealium CDP]*: (Endast konfigurerade användare) Kunddataplattformen [!DNL Tealium].

1. Ange [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* eller *[!UICONTROL Account]*.

1. Ange de återstående [källinställningarna](#source-settings).

   Behåll en kopia av [!UICONTROL Source Key] som genereras. Du behöver värdet senare.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>När ni har skapat en källa för er kunddataplattform måste ni slutföra ytterligare steg för att importera målgruppen. Se [arbetsflödet för [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> [arbetsflödet för [!DNL Amperity]](source-amperity.md), [arbetsflödet för [!DNL Optimizely]](source-optimizely.md) och [arbetsflödet för [!DNL Tealium]](source-tealium.md).

## Ändra ID-typer för en Audience Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** på huvudmenyn.

1. Håll markören över källraden och klicka på **[!UICONTROL Edit]**.

1. Ändra de [ID:n som har valts för källan ](#source-settings).

1. Klicka på **[!UICONTROL Save]**.

## Ta bort en målgrupp-Source

Om du tar bort en källa tas segmenten som översatts via källan bort.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** på huvudmenyn.

1. Håll markören över källraden och klicka på **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

## Visa ändringsloggen för en målgrupp-Source

Du kan visa information om ändringar i en målgruppskällpost och eventuellt bifoga anteckningar till loggen.

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** på huvudmenyn.

1. Håll markören över källraden och klicka på **[!UICONTROL Change log]**.

1. (Valfritt) Så här bifogar du en anteckning till ändringsloggen:

   1. Håll markören över källraden och klicka på **[!UICONTROL Add Notes]**.

   1. Skriv anteckningen och klicka sedan på **[!UICONTROL Save]**.

      Maximala längden är 256 tecken.

1. (Valfritt) Om du vill öppna loggen på en större detaljskärm håller du markören över källraden och klickar på **[!UICONTROL View Details]**.

## Inställningar för målgrupp i Source {#source-settings}

**[!UICONTROL Data Visibility Level]:** Om segmenten är tillgängliga för en enskild annonsörer med åtkomst till kontot (*[!UICONTROL Advertiser]*) eller för alla annonsörer med åtkomst till kontot *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (endast synlighet på annonsnivå) Annonsören som segmenten är tillgängliga för. Välj en i listan över annonsörer med åtkomst till kontot.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] endast källor) Adobe Experience Cloud organisations-ID för [!DNL Adobe Experience Platform]-kontot.

**[!UICONTROL Convert PII to the following IDs]:** De ID-typer som du konverterar din personligt identifierbara information till (PII). Om du väljer flera typer fylls det genererade segmentet i med värden för varje vald ID-typ (till exempel [!DNL RampID] och [!DNL Unified ID2.0] för varje e-postadress). Dataavgifter tillämpas på motsvarande sätt.

För [!DNL RampID] och [!DNL Unified ID2.0] söker leverantören upp varje e-postadress för att se om det redan finns ett ID och översätter adressen till ett matchande ID när den är tillgänglig. Om det inte finns något ID för adressen skapas ett nytt ID.

>[!NOTE]
>
>Du kan bara ange en typ av ID som mål på en enda placering. Om du vill testa prestanda efter ID-typ [skapar du en separat placering](/help/dsp/campaign-management/placements/placement-create.md) för varje ID-typ i segmentet.

* *[!DNL RampID]:* Att konvertera PII till en [!DNL RampID]. Du kan använda [!DNL RampIDs] för återmarknadsföring av inloggningsanvändare och för [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)-mätning.

* *[!DNL Unified ID2.0] (Beta):* Så här konverterar du PII till ett [Unified ID 2.0](https://unifiedid.com)-ID för återmarknadsföring av inloggningsanvändare.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Villkoren i serviceavtalet för konvertering av PII till universella ID:n. Du eller en annan användare på DSP måste acceptera villkoren en gång innan du kan konvertera data till en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren å din organisations vägnar. Om du vill läsa villkoren klickar du på **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (skrivskyddad, genererad automatiskt) Den källnyckel du kan använda för att skapa en målanslutning i kunddataplattformen för att skicka målgrupper till Advertising DSP. Du kan kopiera värdet till Urklipp och klistra in det i inställningarna för målanslutningen eller i en fil.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](source-about.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID:n](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Amperity] till universella ID:n](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID:n](/help/dsp/audiences/sources/source-tealium.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
