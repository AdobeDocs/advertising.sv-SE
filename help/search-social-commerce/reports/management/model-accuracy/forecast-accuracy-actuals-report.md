---
title: "[!UICONTROL Forecast Accuracy (Actuals) Report]"
description: Läs mer om [!UICONTROL Forecast Accuracy (Actuals) Report], inklusive datakolumnerna.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# The [!UICONTROL Forecast Accuracy (Actuals) Report]

Den här rapporten visar faktiskt intryck, klickningar, kostnader och intäkter från annonsnätverket per dag för varje portfölj.

## Tillgängliga kolumner

Följande kolumner inkluderas automatiskt i varje rapport. Du kan inte lägga till fler kolumner.

| Kolumn | Standard? | Beskrivning |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Standard | Namnet på den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio ID] | Standard | Det numeriska portfölj-ID:t. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Det numeriska ID:t för portföljgruppen som portföljen tillhör. |
| [!UICONTROL Portfolio] | Standard | Portföljen. |
| [!UICONTROL Portfolio Status] | Standard | Portföljstatus:<ul><li><i>[!UICONTROL Optimize]:</i> Optimeringsfunktionen är att samla in klickdata och intäktsdata för relevanta kampanjer, modellera data för att optimera anbud och optimera bud och/eller kampanjbudgetar (beroende på optimeringstyp och kampanjstrategier).</li><li><i>[!UICONTROL Active]:</i> Optimeringsfunktionen samlar in klicknings- och intäktsdata för relevanta kampanjer och modellerar data, men optimerar inte offerter eller kampanjbudgetar.</li><li><i>[!UICONTROL Inactive]:</i> Optimeringsfunktionen samlar in klickdata för relevanta kampanjer i rapporteringssyfte, men den modellerar inte data och optimerar inte offerter eller kampanjbudgetar. |
| [!UICONTROL Day of Week] | Standard | Veckodagen som rapporterades: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, eller <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Standard | Det datum som rapporteras. |
| [!UICONTROL Device] | Standard | (Google Ads, Microsoft® Advertising, Yahoo! Display Network, Yahoo! Japan Ads och Yahoo Native-kampanjer) Enhetstypen som annonserna visades på: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, eller <i>[!UICONTROL N/A]</i> (inget värde). Rader för andra annonsnätverk har värden för <i>[!UICONTROL N/A]</i>.<br><br>Om spårningsmallarna eller mål-URL:erna för nyckelorden, annonserna och/eller tilläggen i sökkampanjer innehöll parametrar för att spåra data per enhet (&amp;ev_dvc={device}&amp;ev_dvm={devicemodel})</code>) när man klickade på annonsen inkluderas även konverteringsdata på raden för varje enhetstyp. Om konverteringsdata inte kan tilldelas en enhetstyp, sammanställs de i en separat rad med ett &quot;[!UICONTROL Device]&quot; värde för <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Standard | De totala intäkterna. |
| [!UICONTROL Impressions] | Standard | Det totala intrycket. |
| [!UICONTROL Clicks] | Standard | De totala klickningarna. |
| [!UICONTROL Cost] | Standard | Den totala kostnaden. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Rapporter om modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Generera en modellnoggrannhetsrapport](model-accuracy-report-generate.md)
>* [Rapportinställningar för modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
