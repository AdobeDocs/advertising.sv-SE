---
title: Hantera era kampanjdatavyer
description: Lär dig hur du kan anpassa datavyer för kampanjer, paket, ersättningar och annonser.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 40cfd72c0f295ab1b6b7743828dded4032d435d4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Hantera era kampanjdatavyer

Du kan anpassa de data som visas i kampanjhanteringsvyer ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads]).

## Hantera datavisualiseringar {#data-visualizations-manage}

Ni kan ändra mätvärden och diagram för alla datavisualiseringar över kampanjer eller för en enda kampanj. Ändringar i en enskild kampanj tillämpas för alla datavisualiseringar för kampanjen, inklusive de i vyerna [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads].

### Ändra mått för datavisualisering

1. Klicka på ![Inställningar](/help/dsp/assets/settings-chart.png) i det övre högra hörnet av datavisualiseringen.

1. Välj mätvärden.

   Du kan inte markera samma mätvärde två gånger.

1. Klicka på **[!UICONTROL Apply]**.

### Ändra visningsläge för datavisualisering

* Klicka på [!UICONTROL Overlay]-växeln (![Övertäckningsväxel](/help/dsp/assets/overlay.png)) i det övre högra hörnet av datavisualiseringen om du vill växla mellan övertäckningsläge (alla diagram överlappar varandra) och trellis-diagramläge (tre separata diagram).

## Hantera datatabeller {#data-tables-manage}

I alla kampanjhanteringsvyer ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads]) kan du anpassa de data som visas i datatabellen.

### Hantera kolumnvyer {#column-views-manage}

Varje kampanjhanteringsnivå ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads]) innehåller inbyggda [!UICONTROL Pacing]- och [!UICONTROL Performance]-vyer som innehåller relevanta mått för den entiteten. Som standard visas vyn [!UICONTROL Pacing] så att du kan identifiera underpresterande kampanjer och kampanjkomponenter i en översikt. Du kan också skapa och redigera anpassade kolumnuppsättningar.

![kolumnvyväljare](/help/dsp/assets/column-view-selector.png)

DSP sparar den senaste vyn som standardvy så att du alltid ser de mätvärden som är relevanta för dig varje gång du återgår till sidan.

#### Ändra kolumnvyn {#column-view-change}

* Klicka på ![nedpilen](/help/dsp/assets/chevron-down.png) i visningsväljaren och klicka sedan på namnet på den önskade kolumnvyn.

#### Skapa en anpassad kolumnvy {#column-view-create}

1. Klicka på ![nedpilen](/help/dsp/assets/chevron-down.png) i visningsväljaren och klicka sedan på **[!UICONTROL Create View]**.

1. Ange de mått som ska inkluderas i vyn:

   1. I listan med tillgängliga mätvärden markerar du kryssrutan bredvid varje mätvärde som ska inkluderas.

      Alla mätvärden är alfabetiska efter kategori: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (standardmått som spåras i DSP), [!UICONTROL Viewability] och [!UICONTROL Conversions]. Mätvärden som har lagts till med &quot;([!UICONTROL Lifetime])&quot; returnerar värden från kampanjens början, oavsett vilket datumintervall som har valts på sidan.

   1. Redigera kolumnordningen efter behov genom att klicka på kolumnnamnen på den högra panelen och dra dem till önskade positioner.

   Vissa kolumner har fasta positioner och kan inte flyttas eller tas bort.

1. Använd eller spara inställningarna:

   * Om du vill använda inställningarna tillfälligt utan att spara dem i vyn klickar du på **[!UICONTROL Apply].**

   * Om du vill spara inställningarna i en ny anpassad kolumnvy klickar du på **[!UICONTROL Save As]**. I fönstret [!UICONTROL Save View] anger du namnet på den nya vyn och klickar sedan på **[!UICONTROL Save]**.

#### Redigera en kolumnvy {#column-view-edit}

>[!NOTE]
>
>Du kan inte spara ändringar i en standardkolumnvy (fördefinierad), men du kan tillämpa ändringarna tillfälligt eller spara dem i en ny anpassad vy.

1. Klicka på ![nedpilen](/help/dsp/assets/chevron-down.png) i visningsväljaren och klicka sedan på det befintliga kolumnvisningsnamnet.

1. Klicka på ![nedpilen](/help/dsp/assets/chevron-down.png) i visningsväljaren och klicka sedan på **[!UICONTROL Edit View]**.

1. Redigera mätvärdena som ska inkluderas i vyn:

   1. I listan med tillgängliga mått markerar du kryssrutan intill varje mätvärde som ska inkluderas och avmarkerar kryssrutan intill varje mätvärde som ska uteslutas.

      Alla mätvärden är alfabetiska efter kategori: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (standardmått som spåras i DSP), [!UICONTROL Viewability] och [!UICONTROL Conversions]. Mätvärden som har lagts till med &quot;([!UICONTROL Lifetime])&quot; returnerar värden från kampanjens början, oavsett vilket datumintervall som har valts på sidan.

   1. Redigera kolumnordningen efter behov genom att klicka på kolumnnamnen på den högra panelen och dra dem till önskade positioner.

   Vissa kolumner har fasta positioner och kan inte flyttas eller tas bort.

1. Använd eller spara inställningarna:

   * (Endast anpassade vyer) Klicka på **[!UICONTROL Save]** om du vill spara inställningarna.

   * Om du vill använda inställningarna tillfälligt utan att spara dem i vyn klickar du på **[!UICONTROL Apply].**

   * Om du vill spara inställningarna i en ny anpassad kolumnvy klickar du på **[!UICONTROL Save As]**. I fönstret [!UICONTROL Save View] anger du namnet på den nya vyn och klickar sedan på **[!UICONTROL Save]**.

### Filtrera kampanjdata {#filter-data-tables}

Filter ändrar de data som visas på den aktuella fliken. Vilka filter som är tillgängliga varierar beroende på enhetstyp, men kan innehålla kolumnerna enhetsnamn, status och ytterligare egenskaper.

1. Klicka på knappen ![Filter](/help/dsp/assets/filter.png) i huvudverktygsfältet.
1. För varje filter som du vill använda klickar du på filternamnet i den vänstra kolumnen och anger sedan filtervärdena.
1. Klicka på **[!UICONTROL Apply]**.

#### Tillgängliga filter

Följande filter är tillgängliga för vyerna [!UICONTROL Campaigns], [!UICONTROL Packages] och [!UICONTROL Placements]:

* Visningsfilter för [!UICONTROL Campaigns]:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* Visningsfilter för [!UICONTROL Packages]:
   * [!UICONTROL Custom flights] (vare sig de finns eller inte)
   * [!UICONTROL Custom goal] (om tillämpligt)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* Visningsfilter för [!UICONTROL Placements]:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (om tillämpligt)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] eller [!UICONTROL equal to] ett angivet värde)
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
* Visningsfilter för [!UICONTROL Ads]:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Ändra datumintervall

Ändra datumintervallet som används i alla standardvyer och anpassade vyer med datumintervallväljaren ovanför en datatabell.

![Datumintervallväljare](/help/dsp/assets/date-range-selector.png "Datumintervallväljare")

* För ett förinställt intervall: Välj i listan över vanliga tidssteg. Standardvärdet är [!UICONTROL Last 30 days]*.

* Gör något av följande för ett visst intervall:

   * Klicka på ![Kalender](/help/dsp/assets/calendar.png "Kalender") och klicka sedan på startdatumet och slutdatumet i kalendern.

   * Klicka i datumintervallet och ange sedan ett start- och slutdatum eller markera dem i kalendern.

     Du kan ange numeriska värden (från M-D-YY till MM-DD-YYY) och/eller namn på månader eller förkortningar (till exempel Jan eller Januari).

### Sortera en datakolumn

Du kan sortera valfri datakolumn i stigande ordning (A till Z eller 1 till 10) eller i fallande ordning (Ö till A eller 10 till 1).

* Klicka på kolumnrubriken om du vill växla mellan stigande och fallande ordning.


### Ange antalet datarader

Välj *[!UICONTROL 25]*, *[!UICONTROL 50]* eller *[!UICONTROL 100]* längst ned till höger på en sida, intill **[!UICONTROL Items per page]**.

>[!MORELIKETHIS]
>
>* [Typer av prestandarapporter i kampanjhanteringsvyer](campaign-reports-about.md)
>* [Visa platser, annonser och frekvensinformation för en placering](placement-details-view.md)
>* [Visa prognosrapport för placering](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Visa diagnostikrapporter för placering](placement-diagnostics.md)
>* [Exportera data från en kampanjhanteringsvy](campaign-export-data.md)
>* [Video: DSP kontostruktur och användargränssnitt](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=sv-SE)
