---
title: Hantera kampanjdatavyer
description: Lär dig hur du kan anpassa datavyer för kampanjer, paket, ersättningar och annonser.
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Hantera kampanjdatavyer

## Hantera datavisualiseringar

Ni kan ändra mätvärden och diagram för alla datavisualiseringar över kampanjer eller för en enda kampanj. Ändringar i en enskild kampanj tillämpas för alla datavisualiseringar för kampanjen, inklusive [!UICONTROL Packages], [!UICONTROL Placements]och [!UICONTROL Ads] -tabbar.

### Ändra mått för datavisualisering

1. Klicka på uppe till höger i datavisualiseringen ![Inställningar](/help/dsp/assets/settings-chart.png).
1. Välj mätvärden.
Du kan inte markera samma mätvärde två gånger.
1. Klicka på **[!UICONTROL Apply]**.

### Ändra visningsläge för datavisualisering

* Klicka på knappen [!UICONTROL Overlay] switch (![Övertäckningsväxling](/help/dsp/assets/overlay.png)) om du vill växla mellan övertäckningsläge (alla diagram överlappar varandra) och trellis-diagramläge (tre separata diagram).

## Hantera datatabeller

I alla vyer för kampanjhantering ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]och [!UICONTROL Ads]) kan du anpassa de data som visas i datatabellen.

### Ändra kolumnvyn

* Klicka på i vyväljaren ![nedpil](/help/dsp/assets/chevron-down.png)och klicka sedan på namnet på den kolumnvy du vill använda.

### Skapa en anpassad kolumnvy

1. Klicka på i vyväljaren ![nedpil](/help/dsp/assets/chevron-down.png)och klicka sedan på **[!UICONTROL Create View]**.

1. Ange de mått som ska inkluderas i vyn:

   1. I listan med tillgängliga mätvärden markerar du kryssrutan bredvid varje mätvärde som ska inkluderas.

   1. Redigera kolumnordningen efter behov genom att klicka på kolumnnamnen på den högra panelen och dra dem till önskade positioner.

   Vissa kolumner har fasta positioner och kan inte flyttas eller tas bort.

1. Använd eller spara inställningarna:

   * Om du vill använda inställningarna tillfälligt utan att spara dem i vyn klickar du på **[!UICONTROL Apply].**

   * Om du vill spara inställningarna i en ny anpassad kolumnvy klickar du på **[!UICONTROL Save As]**. I [!UICONTROL Save View] anger du namnet på den nya vyn och klickar sedan på **[!UICONTROL Save]**.

### Redigera en anpassad kolumnvy

>[!NOTE]
>
>Du kan inte redigera en standardkolumnvy (fördefinierad).

1. Klicka på i vyväljaren ![nedpil](/help/dsp/assets/chevron-down.png)och klicka sedan på det befintliga kolumnvynamnet.

1. Klicka på i vyväljaren ![nedpil](/help/dsp/assets/chevron-down.png)och klicka sedan på **[!UICONTROL Edit View]**.

1. Redigera mätvärdena som ska inkluderas i vyn:

   1. I listan med tillgängliga mått markerar du kryssrutan intill varje mätvärde som ska inkluderas och avmarkerar kryssrutan intill varje mätvärde som ska uteslutas.

   1. Redigera kolumnordningen efter behov genom att klicka på kolumnnamnen på den högra panelen och dra dem till önskade positioner.

   Vissa kolumner har fasta positioner och kan inte flyttas eller tas bort.

1. Använd eller spara inställningarna:

   * Om du vill använda inställningarna tillfälligt utan att spara dem i vyn klickar du på **[!UICONTROL Apply].**

   * Om du vill spara inställningarna i en ny anpassad kolumnvy klickar du på **[!UICONTROL Save As]**. I [!UICONTROL Save View] anger du namnet på den nya vyn och klickar sedan på **[!UICONTROL Save]**.

### Filtrera kampanjdata

1. Klicka på i huvudverktygsfältet ![Filterknapp](/help/dsp/assets/filter.png).
1. För varje filter som du vill använda klickar du på filternamnet i den vänstra kolumnen och anger sedan filtervärdena.
1. Klicka på **[!UICONTROL Apply]**.

#### Tillgängliga filter

Följande filter är tillgängliga för [!UICONTROL Campaigns], [!UICONTROL Packages]och [!UICONTROL Placements] vyer:

* [!UICONTROL Campaigns] visningsfilter:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] visningsfilter:
   * [!UICONTROL Custom flights] (oavsett om de finns eller inte)
   * [!UICONTROL Custom goal] (om tillämpligt)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] visningsfilter:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (om tillämpligt)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], eller [!UICONTROL equal to] ett angivet värde)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] eller [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] visningsfilter:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Sortera en datakolumn

Du kan sortera valfri datakolumn i stigande ordning (A till Z eller 1 till 10) eller i fallande ordning (Ö till A eller 10 till 1).

* Klicka på kolumnrubriken om du vill växla mellan stigande och fallande ordning.

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [Om rapporter på plattformen](campaign-reports-about.md)
>* [Hantera datavisualiseringar](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Ändra kolumnvyn](column-view-change.md)
>* [Skapa en anpassad kolumnvy](column-view-create.md)
>* [Redigera en anpassad kolumnvy](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filtrera kampanjdata](campaign-data-filter.md)
>* [Sortera en datakolumn](campaign-data-sort.md)
>* [Visa Sites, Ads och Frequency Details för en placering](placement-details-view.md)
>* [Visa prognosrapport för placering](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Visa diagnostikrapporter för placering](placement-diagnostics.md)
>* [Exportera data från en Campaign Management-vy](campaign-export-data.md)
>* [Video: DSP och användargränssnitt](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
