---
title: (Nytt användargränssnitt) Visa information om portföljprestanda
description: Lär dig hur du visar information om portföljens prestanda, inklusive faktiska och förväntade värden på portföljnivå och för varje tilldelad kampanj.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: e786ffc8c9e331fffcc8b0f7cce4cb082baea6ac
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# (Nytt användargränssnitt) Visa information om portföljprestanda

*Beta-funktion*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

Vyn Portföljinformation innehåller följande information om en portfölj:

* De faktiska och förväntade värdena för upp till tre prestandamått. Rapporterna innehåller de totala måttvärdena för portföljen och måttuppdelningen per datum.<!-- Not for active portfolios only?  -->

* Modellprecisionsdata för aktiva portföljer, som visar hur mycket modellerna avviker från prognoserna. Rapporten visar den totala dagliga eller rullande kostnadsnoggrannheten på sju dagar, klicknoggrannheten och det objektiva värdet är korrekt.

  Du kan visa data genom att klicka på datum (standard) eller efter transaktionsdatum.   Du kan även visa data som ett trenddiagram (standardvärdet) eller som en tabell.

* Målutgiften jämfört med de faktiska utgifterna för aktiva portföljer. Du kan också inkludera den totala kampanjbudgeten för portföljen.

* Exaktheten i kostnads-, klick- eller [objektiva värde](/help/search-social-commerce/glossary.md#o-p) -prognoser för aktiva portföljer per annonsnätverk.<!-- Verify -->

* Portföljinställningarna.

  Du kan även öppna portföljinställningarna för att redigera dem.

## Öppna prestandainformation för en portfölj

1. Klicka på **[!UICONTROL Manage]>[!UICONTROL Portfolios]** på huvudmenyn.

1. Klicka på portföljnamnet.

1. (Valfritt) Ändra datagranulariteten mellan **[!UICONTROL Granularity]**, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]eller* på menyn *[!UICONTROL Monthly].*

1. (Valfritt) Om du vill ändra datumintervallet för portföljinformationen klickar du på datumintervallet i det övre högra hörnet, anger datumintervallet och klickar sedan på **[!UICONTROL Apply]**.

## Anpassa fliken [!UICONTROL Portfolio Overview]

* (Valfritt) Gör något av följande om du vill anpassa [!UICONTROL Portfolio Performance]-rapporterna:

   * Om du vill ändra de prestandamått som används för både det totala måttet och de detaljerade måtten klickar du på **[!UICONTROL Metrics]** och väljer upp till tre mätvärden.

     Standardmåtten är *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* och *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Detaljerade mått:

      * Flytta växeln bredvid **[!UICONTROL Display predictions]** om du vill visa eller dölja de förväntade måttvärdena.

      * Växla mellan diagramvyn (![Diagramvy](/help/search-social-commerce/assets/chart-view.png "Diagramvy")) och tabellvyn (![Tabellvy](/help/search-social-commerce/assets/table-view.png "Tabellvy")).

      * (I diagramvyn) Om du vill visa data för en punkt i diagrammet håller du markören över punkten.

* (Valfritt) Gör något av följande om du vill anpassa [!UICONTROL Model accuracy]-trenddiagrammet:

   * Växla mellan diagramvyn (![Diagramvy](/help/search-social-commerce/assets/chart-view.png "Diagramvy")) och tabellvyn (![Tabellvy](/help/search-social-commerce/assets/table-view.png "Tabellvy")).

   * Växla mellan att visa data av *[!UICONTROL Click Date]* och *[!UICONTROL Transaction Date]*.

   * Växla mellan att visa data om *[!UICONTROL Daily Accuracy]* och *[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] är den genomsnittliga noggrannheten för prognosen för de senaste sju dagarna, uttryckt i procent. Värdet för den 8 maj 2025 är till exempel den genomsnittliga noggrannheten för perioden 1 maj-7 maj 2025.

   * (I diagramvyn) Om du vill visa data för en punkt i diagrammet håller du markören över punkten.

* (Valfritt) Gör något av följande om du vill anpassa [!UICONTROL Target vs actual spend]-trenddiagrammet:

   * Flytta växeln bredvid **[!UICONTROL Display budget]** om du vill visa eller dölja den totala kampanjbudgeten för varje datum.

   * Om du vill visa data för en punkt i diagrammet håller du markören över punkten.

* (Valfritt) Gör något av följande om du vill anpassa [!UICONTROL Network Accuracy]-trenddiagrammet:

   * Ändra det rapporterade måttet till *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* eller *[!UICONTROL Objective Value]*.

   * Om du vill visa data för en punkt i diagrammet håller du markören över punkten.

1. Klicka på **[!UICONTROL Download report]**.

## Visa kampanjerna i portföljen

* Klicka på fliken **[!UICONTROL Campaigns]**.

## Visa annonsgrupperna i portföljen

* Om du vill visa alla annonsgrupper i en kampanj i portföljen klickar du på fliken **[!UICONTROL Campaigns]** och sedan på kampanjnamnet.

## Visa nyckelorden i portföljen

* Om du vill visa alla nyckelord i portföljen klickar du på fliken **[!UICONTROL Keywords]**.

* Om du vill visa alla nyckelord i en annonsgrupp i portföljen klickar du på fliken **[!UICONTROL Ad Groups]** och sedan på annonsgruppens namn.

## Visa och redigera portföljinställningarna

* Klicka på **[!UICONTROL Portfolio Settings]** om du vill visa eller dölja portföljinställningarna.

   * Om du vill redigera synliga portföljinställningar klickar du på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") bredvid inställningsavsnittet och [redigerar portföljinställningarna](portfolio-edit.md).

Mer information om portföljinställningarna finns i Optimeringsguiden som du når via Sök, Socialt och Commerce.

## Ladda ned rapporter om portföljens prestanda och listor över portföljkomponenterna

* Så här hämtar du alla rapporter:

   1. Klicka på **[!UICONTROL Download report]** i verktygsfältet.

   1. Markera kryssrutan bredvid varje resultatrapport och portföljkomponenttyp som ska inkluderas.

      För vissa resultatrapporter kan du välja om du vill hämta data som ett diagram eller en tabell.

   1. Klicka på **[!UICONTROL Download report]**.

* Så här hämtar du en [!DNL model accuracy]-rapport med specifika datatyper:

   1. Klicka på **[!UICONTROL Download report]** i rapportens verktygsfält.

   1. Markera kryssrutan bredvid varje typ av data som ska inkluderas och hur data ska delas upp (per budenhet och/eller genom att klicka på volym).

   1. Klicka på **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(nytt användargränssnitt) Om portföljer &#x200B;](portfolio-about.md)
>* [(Nytt användargränssnitt) Redigera en portfölj &#x200B;](portfolio-edit.md)
>* [(Nytt användargränssnitt) Hämta data i [!UICONTROL Portfolios]-vyn &#x200B;](portfolio-view-report.md)
