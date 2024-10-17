---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Lär dig mer om [!UICONTROL Forecast Accuracy (Actuals) Report], inklusive datakolumner.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy (Actuals) Report]

Den här rapporten visar faktiskt intryck, klickningar, kostnader och intäkter från annonsnätverket per dag för varje portfölj.

## Tillgängliga kolumner

Följande kolumner inkluderas automatiskt i varje rapport. Du kan inte lägga till fler kolumner.

| Kolumn | Standard? | Beskrivning |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Standard | Namnet på den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio ID] | Standard | Numeriskt portfölj-ID. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Det numeriska ID:t för den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio] | Standard | Portföljen. |
| [!UICONTROL Portfolio Status] | Standard | Portföljens status:<ul><li><i>[!UICONTROL Optimize]:</i> Optimeringsfunktionen samlar in klicknings- och intäktsdata för relevanta kampanjer, modellerar data som används för optimering och optimerar bud, kampanjbudgetar och strategiska mål för kampanjbud (beroende på optimeringstyp och anbudsstrategier).</li><li><i>[!UICONTROL Active]:</i> Optimeringsfunktionen samlar in klicknings- och intäktsdata för relevanta kampanjer och modellerar data, men optimerar inte offerter eller kampanjbudgetar.</li><li><i>[!UICONTROL Inactive]:</i> Optimeringsfunktionen samlar in klickdata för relevanta kampanjer i rapporteringssyfte, men den modellerar inte data och optimerar inte offerter eller kampanjbudgetar. |
| [!UICONTROL Day of Week] | Standard | Veckodagen som rapporterades: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> eller <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Standard | Det datum som rapporteras. |
| [!UICONTROL Device] | Standard | (Google Ads, Microsoft Advertising, Yahoo! Display Network, Yahoo! Japan Ads och Yahoo Native-kampanjer) Enhetstypen som annonserna visades på: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> eller <i>[!UICONTROL N/A]</i> (inget värde). Rader för andra annonsnätverk har värdena <i>[!UICONTROL N/A]</i>.<br><br>I sökkampanjer, om spårningsmallarna eller mål-URL:erna för nyckelorden, annonserna och/eller tilläggen innehåller parametrar för att spåra data per enhet (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel})</code>) när man klickade på annonsen inkluderas även konverteringsdata på raden för varje enhetstyp. Annars, om konverteringsdata inte kan tilldelas en enhetstyp, aggregeras de i en separat rad med värdet [!UICONTROL Device] för <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Standard | De totala intäkterna. |
| [!UICONTROL Impressions] | Standard | Det totala intrycket. |
| [!UICONTROL Clicks] | Standard | De totala klickningarna. |
| [!UICONTROL Cost] | Standard | Den totala kostnaden. |

>[!MORELIKETHIS]
>
>* [Rapporter om modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Generera en modellnoggrannhetsrapport](model-accuracy-report-generate.md)
>* [Rapportinställningar för modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
