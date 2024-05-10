---
title: Hantera budmultiplikationer för praktik
description: Lär dig hur du skapar och redigerar budmultiplikatorer för angivna placeringsmål.
feature: DSP Placements
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Hantera budmultiplikationer för praktik


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Du kan ändra budmultiplikaterna för dina befintliga placeringsmål med den här funktionen.

Information om hur du ändrar de valda målen för dina placeringar finns i &quot;[Redigera placeringar](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Hantera budmultiplikatorer för en eller flera placeringar

För alla markerade placeringar kan du antingen redigera värden manuellt eller överföra ett kalkylblad med värden.

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Markera kryssrutan bredvid varje placering vars budmultiplikatorer du vill hantera.

1. Klicka på i verktygsfältet för gruppåtgärder **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Justera budmultiplikatorerna för det berättigade målet manuellt eller genom att överföra en CSV-fil med målvärden:

   * Flytta till varje målspecifik flik ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]och[!UICONTROL Brand Safety]) och redigera de befintliga värdena för placeringsmålen.

   Samma ändringar gäller för alla markerade placeringar.

   * Så här överför du en CSV-fil med budmultiplikatorvärden som skriver över befintliga värden:

     >[!NOTE]
     >
     >Om du lämnar ett fält tomt tas alla värden för den måltypen bort.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there only one data row is applicable for all. -->

      1. Klicka **[!UICONTROL CSV Edit]** i det övre högra hörnet.

      1. Antingen a) klickar du **[!UICONTROL Download Template]** och redigera värdena för budmultiplikatorn eller b) redigera en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

      1. antingen a) dra och släpp den redigerade filen i rutan eller b) klicka inuti rutan för att välja filen från enheten eller nätverket.

   1. Klicka på **[!UICONTROL Upload]**.

   Som standard är budmultiplikatorn för ett mål 1,00, vilket innebär att anbudet inte justeras för det målet. Värdena kan ligga mellan 0,10 och 10,00. En budmodifierare på 0,5 minskar till exempel ett USD 6-bud till USD 3 (0,5 x 6). Du kan ange budmultiplikatorer (med andra värden än 1,00) för en [begränsat antal mål](#bid-multiplier-limits-by-target).

   När en auktion kvalificerar sig för flera budmodifierare multipliceras alla tillämpliga budmodifierare.

   Anbudsmodifierare ökar aldrig anbudet till mer än det högsta anbudet.

1. Klicka på **[!UICONTROL Save]**.

—>

## Ladda upp ett kalkylblad för att hantera budmultiplikatorer för en enstaka placering<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Ändringar i den överförda filen skriver över de befintliga budmultiplikatorvärdena.<!-- what if you delete a row? -->

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. Antingen a) klickar du **[!UICONTROL Download Template]** och redigera värdena för budmultiplikatorn eller b) redigera en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

   Som standard är budmultiplikatorn för ett mål 1,00, vilket innebär att anbudet inte justeras för det målet. Värdena kan ligga mellan 0,10 och 10,00. En budmodifierare på 0,5 minskar till exempel ett USD 6-bud till USD 3 (0,5 x 6). Du kan ange budmultiplikatorer (med andra värden än 1,00) för en [begränsat antal mål](#bid-multiplier-limits-by-target).

   När en auktion kvalificerar sig för flera budmodifierare multipliceras alla tillämpliga budmodifierare.

   Anbudsmodifierare ökar aldrig anbudet till mer än det högsta anbudet.

1. antingen a) dra och släpp den redigerade filen i rutan eller b) klicka inuti rutan för att välja filen från enheten eller nätverket.

1. Klicka på **[!UICONTROL Upload]**.

1. Klicka på **[!UICONTROL Save]**.

## Måltyper som är berättigade för budmultiplikatorer {#bid-multiplier-by-target}

inte dubbad här

## Maximalt antal buddelsemultiplikatorer per måltyp {#bid-multiplier-limits-by-target}

inte dubbad här

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
