---
title: Hantera budmultiplikationer för praktik
description: Lär dig xxx
feature: DSP Placements
source-git-commit: c0dd18a3ce8759214813b7303c590a28febf1b37
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# XXX

## Hantera budmultiplikatorer för en enda placering

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Justera budmultiplikaterna för giltiga mål:

   * Om du vill justera budmultiplikatorvärdena manuellt går du till varje [målspecifik flik](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]och [!UICONTROL Brand Safety]) och redigera de befintliga värdena för placeringsmålen.

     De flesta målkategorierna listar underkategorier till vänster. Klicka på en underkategori för att hantera budmultiplikatorer för den underkategorin, beroende på vad som är tillämpligt.

   * Så här överför du en CSV-fil med budmultiplikatorvärden för att skriva över alla befintliga värden:

      1. Klicka **[!UICONTROL CSV File Edit]** i det övre högra hörnet.

      1. Antingen a) klickar du **[!UICONTROL Download Template]** och redigera filen eller b) redigera en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

         Nedladdade kalkylblad innehåller ett ark för varje måltyp (t.ex. Land, Källor och Platskategori). Endast befintliga budmultiplikatorer med värden &lt; 1.0 eller > 1.0 inkluderas.

         * Om du vill lägga till en budmultiplikator för ett befintligt mål anger du målet med samma syntax som visas i användargränssnittet och motsvarande budmultiplikatorvärde.

         * Om du vill ta bort en budmodifierare anger du multiplikatorvärdet 1.0 eller tar bort all information för raden.

         ![Exempelrad i en anbudsmultiplikator-kalkylbladsfil](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exempelrad i en anbudsmultiplikator-kalkylbladsfil")

      1. Klicka **[!UICONTROL Next]** för att gå till [!UICONTROL Upload File] och antingen a) dra och släpp den redigerade filen i rutan eller b) klicka inuti rutan för att välja filen från enheten eller nätverket.

      1. Verifiera överförda data i [!UICONTROL Review & Submit] och klicka sedan på **[!UICONTROL Save]**.

## Hantera budmultiplikatorer för en eller flera placeringar

<!-- verify all and edit accordingly -->

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Markera kryssrutan bredvid varje placering vars budmultiplikatorer du vill hantera.

1. Klicka på i verktygsfältet för gruppåtgärder **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. Justera budmultiplikaterna för giltiga mål:

   * Flytta till varje målspecifik flik ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]och[!UICONTROL Brand Safety]) och redigera de befintliga värdena för placeringsmålen.

   Samma ändringar gäller för alla markerade placeringar.

* Så här överför du en CSV-fil med budmultiplikatorvärden för att skriva över alla befintliga värden:

   1. Klicka **[!UICONTROL CSV File Edit]** i det övre högra hörnet.

   1. Antingen a) klickar du **[!UICONTROL Download Template]** och redigera filen eller b) redigera en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

      Nedladdade kalkylblad innehåller ett ark för varje måltyp (t.ex. Land, Källor och Platskategori). Endast befintliga budmultiplikatorer med värden &lt; 1.0 eller > 1.0 inkluderas.

      * Om du vill lägga till en budmultiplikator för ett befintligt mål anger du målet med samma syntax som visas i användargränssnittet och motsvarande budmultiplikatorvärde.

      * Om du vill ta bort en budmodifierare anger du multiplikatorvärdet 1.0 eller tar bort all information för raden.

      ![Exempelrad i en anbudsmultiplikator-kalkylbladsfil](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exempelrad i en anbudsmultiplikator-kalkylbladsfil")

   1. Klicka **[!UICONTROL CSV Edit]** i det övre högra hörnet.

   1. Antingen a) klickar du **[!UICONTROL Download Template]** och redigera värdena för budmultiplikatorn eller b) redigera en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

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
