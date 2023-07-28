---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Lär dig mer om rapporten om prognosnoggrannhet, inklusive datakolumner.
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# The [!UICONTROL Forecast Accuracy Report]

Rapporten visar hur korrekta kostnads- och intäktsmodellerna är per dag för angivna portföljer. Som standard inkluderar det dagliga förväntade och faktiska intäkter, kostnader och klickningar - samt precisionen i prognoserna - för varje portfölj. Det innehåller data från kampanjer som för närvarande är mappade till portföljerna.

Du kan visa data för de föregående 18 månaderna.

>[!NOTE]
>
>* Den här rapporten innehåller samma data som portföljnivån [!UICONTROL Model Accuracy Report] förutom att du kan köra det över flera portföljer och du kan ändra attribueringsregeln. Du kan också köra och schemalägga rapporten med anpassade parametrar, och du kan använda den för att skapa kalkylbladsflöden.
>
>* Det bästa sättet är att se [!UICONTROL Forecast Accuracy Report] under åtminstone de senaste sju dagarna eftersom de flesta portföljerna, oavsett portföljens utgiftsstrategi, ser en naturlig trend i veckan. Optimeringsfunktionen tar hänsyn till den här trenden och tilldelar därmed utgifter.
>
>* För kostnadsprognoser anses en avvikelse på 10 % under de senaste sju dagarna vara acceptabel, så de faktiska utgifterna som ligger mellan 90 % och 110 % av de prognostiserade utgifterna är utmärkta. För intäktsprognoser anses en 15-procentig avvikelse under de senaste sju dagarna godtagbar, så de faktiska intäkterna ligger mellan 85 % och 115 % av de prognostiserade utgifterna är bra. Prognoser med högre avvikelser bör undersökas.
>
>* När nyckelord i portföljen är kopplade till begränsningar för budskift, kommer portföljens över- eller underutgifter att motsvara det totala belopp som orsakas av budskiftet. Det innebär att de beräknade kostnadskolumnerna avviker från målutgifterna genom de ökade eller minskade utgifterna.

## Tillgängliga kolumner

Följande kolumner är tillgängliga för varje rapport. Standardkolumnerna inkluderas automatiskt som standard. Du kan lägga till tillgängliga anpassade kolumner från [!UICONTROL Columns] i rapportinställningarna.

| Kolumn | Standard? | Beskrivning |
|----|----|----|
| [!UICONTROL Portfolio] | Standard | Portföljen. |
| [!UICONTROL Day of Week] | Standard | Veckodagen som rapporterades: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, eller <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Standard | Första dagen som rapporterades. |
| [!UICONTROL End Date] | Standard | Den sista dagen som rapporterades. |
| [!UICONTROL Predicted Revenue] | Standard | Portföljens förväntade intäkter. |
| [!UICONTROL Revenue] | Standard | Portföljens faktiska intäkter. |
| [!UICONTROL Revenue Accuracy] | Standard | Exaktheten i intäktsprognosen, uttryckt i procent. |
| [!UICONTROL Predicted Cost] | Standard | Den förväntade kostnaden för portföljen. |
| [!UICONTROL Cost] | Standard | Den faktiska kostnaden för portföljen. |
| [!UICONTROL Cost Accuracy] | Standard | Kostnadsprognosens exakthet, uttryckt i procent. |
| [!UICONTROL Predicted Clicks] | Standard | Antal klick som förutsetts för portföljen. |
| [!UICONTROL Clicks] | Standard | Det faktiska antalet klick för portföljen. |
| [!UICONTROL Click Accuracy] | Standard | Exaktheten för klickprognosen, uttryckt i procent. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Det numeriska ID:t för den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio Group Name] | Standard | Namnet på den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio ID] | Standard | Numeriskt portfölj-ID. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Rapporter om modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Generera en modellnoggrannhetsrapport](model-accuracy-report-generate.md)
>* [Rapportinställningar för modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
