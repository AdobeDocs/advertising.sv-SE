---
title: Typer av prestandarapporter i Campaign Management-vyer
description: Läs mer om rapportdata som ingår i kampanjhanteringsvyer.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Typer av prestandarapporter i Campaign Management-vyer

Vyerna för kampanjhantering omfattar omfattande rapportdata. De tillgängliga rapporterna hjälper dig att identifiera de paket och placeringar som fungerar bra och de som behöver din uppmärksamhet. Snabba åtgärdsknappar gör dig också mer produktiv.

## Vyn Alla kampanjer

The [!UICONTROL Campaigns] -vyn öppnas med en uppsättning resultatdata och en lista över alla kampanjer på ditt konto.

### Diagramvy {#chart-view}

Du kan [anpassa trenddiagram för tidsserier](campaign-data-views-manage.md#data-visualizations-manage) för alla kampanjer med hjälp av tre mätvärden. Som standard används data för [!UICONTROL Net Spend], [!UICONTROL Impressions]och [!UICONTROL Net CPM] ingår i separata diagram (trellis charts). Du kan ändra måtten om du vill. Om du vill aktivera timdata i trenddiagram för tidsserier ändrar du datumvalet till en enda dag ([!UICONTROL Today], [!UICONTROL Yesterday], eller en viss dag).

![separata trenddiagram för tre mätvärden](/help/dsp/assets/trend-chart-separate.png)

Du kan också täcka över de tre mätvärdena för att enkelt upptäcka avvikelser och områden där du kan förbättra skalan eller prestandan.

![trenddiagram med övertäckning](/help/dsp/assets/trend-chart.png)

### Tabellvy

![Kampanjlista](/help/dsp/assets/campaigns-list.png)

Som standard innehåller varje kampanjrad pacing- och leveransstatistik. Mellanrumsmått innehåller [!UICONTROL Gross Spend (Lifetime)], som inkluderar en mätare av de faktiska utgifterna på målet jämfört med de förväntade utgifterna på målsidan för alla paket i kampanjen, så att ni kan identifiera underpresterande kampanjer i en enda gång. Du kan välja att [ändra kolumnvyn](campaign-data-views-manage.md#column-view-change) eller jämn [skapa en anpassad kolumnvy](campaign-data-views-manage.md#column-view-create).

Du kan fortsätta [anpassa datatabellerna](campaign-data-views-manage.md#data-tables-manage) på ytterligare sätt och [filtrera synliga data](campaign-data-views-manage.md#filter-data-tables).

<!--
An "Alerts" column indicates when a campaign (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

Klicka på kampanjnamnet om du vill visa en mer detaljerad kampanj.

## Single Campaign Reporting {#single-campaign-reporting}

Inom en kampanj kan ni filtrera data baserat på kampanjentiteten: [!UICONTROL Packages], [!UICONTROL Placements]och [!UICONTROL Ads]. Du kan fortsätta [filtrera synliga data](campaign-data-views-manage.md#filter-data-tables) om du bara vill inkludera de paket, placeringar eller annonser som du vill se.

![Kampanjentitetsflikar](/help/dsp/assets/campaign-subtabs.png)

### Diagramvy

För varje kampanj kan ni [anpassa trenddiagram för tidsserier](campaign-data-views-manage.md#data-visualizations-manage) med tre mätvärden som är tillgängliga i varje enhetsvy. Samma mätvärden används för alla trenddiagram för kampanjen.

Se [Diagramvy om kampanjstatistik](#chart-view) för mer information.

### Tabellvy

På varje enhetsflik innehåller varje rad som standard värden för avstånd och leverans, men du kan [ändra kolumnvyn](campaign-data-views-manage.md#column-view-change) eller jämn [skapa en anpassad kolumnvy](campaign-data-views-manage.md#column-view-create) som ska gälla alla underflikar för kampanjen. Du kan fortsätta [anpassa datatabellerna](campaign-data-views-manage.md#data-tables-manage) på ytterligare sätt. Varje datatabell innehåller en [!UICONTROL Subtotals] rad, som visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

<!--
An "Alerts" column indicates when a package, placement, or ad &mdash; or any child entity under a package or placement &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

### Andra typer av kampanjnivårapportering

Om du vill se andra databrytningar [rapportsidor på kampanjnivå](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]och [!UICONTROL Audience Performance] data.

### Andra typer av rapportering på placeringsnivå

Om du vill se andra databrytningar [rapportsidor på placeringsnivå](/help/dsp/campaign-management/placements/placement-view-report.md). Rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications]och [!UICONTROL Ads] data.

Dessutom kan du visa följande data i placeringsinställningarna:

* [A (detaljvy) [!UICONTROL Inspector])](placement-details-view.md), som visar alla riktade webbplatser, annonser, frekvensdata och erbjudanden för en placering.

* A [placeringsprognosrapport](/help/dsp/campaign-management/reports/placement-forecast.md)

* [Diagnostikrapporter för placering](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Andra typer av rapportering på annonsnivå

Om du vill se andra databrytningar [rapportsidor på annonsnivå](/help/dsp/campaign-management/ads/ad-view-report.md). Rapporten innehåller [!UICONTROL Overview], [!UICONTROL Geography]och [!UICONTROL Viewability] data.

>[!MORELIKETHIS]
>
>* [Visa Sites, Ads och Frequency Details för en placering](placement-details-view.md)
>* [Hantera era kampanjdatavyer](campaign-data-views-manage.md)
>* [Exportera data från en Campaign Management-vy](campaign-export-data.md)
>* [Visa en detaljerad rapport för en kampanj](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
