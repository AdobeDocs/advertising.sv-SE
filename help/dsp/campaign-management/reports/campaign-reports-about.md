---
title: Typer av prestandarapporter i Campaign Management-vyer
description: Läs mer om rapportdata som ingår i kampanjhanteringsvyer.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 4e82caa995286635b4a181f186d6a1fabb09847d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Typer av prestandarapporter i Campaign Management-vyer

Vyerna för kampanjhantering omfattar omfattande rapportdata. De tillgängliga rapporterna hjälper dig att identifiera de paket och placeringar som fungerar bra och de som behöver din uppmärksamhet. Snabba åtgärdsknappar gör dig också mer produktiv.

## Vyn Alla kampanjer

Vyn [!UICONTROL Campaigns] öppnas med en uppsättning prestandadata och en lista över alla kampanjer i ditt konto.

### Diagramvy {#chart-view}

Du kan [anpassa trenddiagram för tidsserier](campaign-data-views-manage.md#data-visualizations-manage) för alla kampanjer med hjälp av tre mätvärden. Som standard ingår data för [!UICONTROL Net Spend], [!UICONTROL Impressions] och [!UICONTROL Net CPM] i separata diagram (trellis-diagram). Du kan ändra måtten om du vill. Om du vill aktivera timdata i trenddiagram för tidsserier ändrar du datumvalet till en enda dag ([!UICONTROL Today], [!UICONTROL Yesterday] eller en viss dag).

![separata trenddiagram för tre mätvärden](/help/dsp/assets/trend-chart-separate.png)

Du kan också täcka över de tre mätvärdena för att enkelt upptäcka avvikelser och områden där du kan förbättra skalan eller prestandan.

![trenddiagram med övertäckning](/help/dsp/assets/trend-chart.png)

### Tabellvy

![Kampanjlista](/help/dsp/assets/campaigns-list.png)

Som standard innehåller varje kampanjrad pacing- och leveransstatistik. Mellanrumsmåtten inkluderar [!UICONTROL Gross Spend (Lifetime)], som innehåller en mätare för den faktiska utgiften på målet jämfört med den förväntade utgiften på målet för alla paket i kampanjen, så att ni snabbt kan identifiera underpresterande kampanjer. Du kan [ändra kolumnvyn](campaign-data-views-manage.md#column-view-change) eller till och med [skapa en anpassad kolumnvy](campaign-data-views-manage.md#column-view-create).

Du kan [anpassa datatabellerna](campaign-data-views-manage.md#data-tables-manage) ytterligare och [filtrera synliga data](campaign-data-views-manage.md#filter-data-tables).

Klicka på kampanjnamnet om du vill visa en mer detaljerad kampanj.

#### Varningsindikatorer

*Beta-funktion*

En [!UICONTROL Alerts]-kolumn anger när en kampanj, eller någon underordnad entitet under den, har ett problem. En [!UICONTROL Pulse Panel]-ikon till höger om verktygsfältet anger också om det finns några varningar tillgängliga för de enheter som visas. Mer information finns i [Visa aviseringar](campaign-alerts.md).

## Single Campaign Reporting {#single-campaign-reporting}

Inom en kampanj kan du filtrera data baserat på kampanjentiteten: [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads]. Du kan [filtrera synliga data](campaign-data-views-manage.md#filter-data-tables) ytterligare så att endast de paket, placeringar eller annonser som du vill se inkluderas.

![Flikar för kampanjentitet](/help/dsp/assets/campaign-subtabs.png)

### Diagramvy

För varje kampanj kan du [anpassa trenddiagram för tidsserier](campaign-data-views-manage.md#data-visualizations-manage) med tre mätvärden, som är tillgängliga i varje entitetsvy. Samma mätvärden används för alla trenddiagram för kampanjen.

Mer information finns i avsnittet [&quot;Diagramvy&quot; om mått för olika kampanjer ](#chart-view).

### Tabellvy

På varje enhetsflik innehåller varje rad som standard plats- och leveransmått, men du kan [ändra kolumnvyn](campaign-data-views-manage.md#column-view-change) eller till och med [skapa en anpassad kolumnvy](campaign-data-views-manage.md#column-view-create) som ska användas på alla underflikar för kampanjen. Du kan ytterligare [anpassa datatabellerna](campaign-data-views-manage.md#data-tables-manage) på andra sätt. Varje datatabell innehåller en [!UICONTROL Subtotals]-rad, som visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

#### Varningsindikatorer

*Beta-funktion*

En [!UICONTROL Alerts]-kolumn anger när ett paket, en placering eller en annons - eller någon underordnad enhet under ett paket eller en placering - har problem. En [!UICONTROL Alerts]-kolumn anger när en kampanj, eller någon underordnad entitet under den, har ett problem. En [!UICONTROL Pulse Panel]-ikon till höger om verktygsfältet anger också om det finns några varningar tillgängliga för de enheter som visas. Mer information finns i [Visa aviseringar](campaign-alerts.md).

### Andra typer av kampanjnivårapportering

Visa [rapportsidorna på kampanjnivå](/help/dsp/campaign-management/campaigns/campaign-view-report.md) om du vill se andra databrytningar. Rapporten innehåller avsnitt om [!UICONTROL Geography]-, [!UICONTROL Device]-, [!UICONTROL Viewability]- och [!UICONTROL Audience Performance]-data.

### Andra typer av rapportering på placeringsnivå

Visa [rapportsidorna på placeringsnivå](/help/dsp/campaign-management/placements/placement-view-report.md) om du vill se andra databrytningar. Rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] och [!UICONTROL Ads] data.

Dessutom kan du visa följande data i placeringsinställningarna:

* [A (detaljvy [!UICONTROL Inspector])](placement-details-view.md), som visar alla målwebbplatser, annonser, frekvensdata och erbjudanden för en placering.

* En [placeringsprognosrapport](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Placeringsdiagnostikrapporter](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Andra typer av rapportering på annonsnivå

Visa [rapportsidorna på annonsnivå](/help/dsp/campaign-management/ads/ad-view-report.md) om du vill se andra databrytningar. Rapporten innehåller [!UICONTROL Overview], [!UICONTROL Geography] och [!UICONTROL Viewability] data.

>[!MORELIKETHIS]
>
>* [Visa platser, annonser och frekvensinformation för en placering](placement-details-view.md)
>* [Hantera dina kampanjdatavyer](campaign-data-views-manage.md)
>* [Exportera data från en Campaign Management-vy](campaign-export-data.md)
>* [Visa en detaljerad rapport för en kampanj](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Visa aviseringar](campaign-alerts.md)
