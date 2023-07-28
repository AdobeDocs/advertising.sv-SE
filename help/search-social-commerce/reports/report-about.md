---
title: Rapporter
description: Lär dig mer om resultatrapporter, inklusive de olika rapporttyper som finns tillgängliga och hur du automatiserar rapporter.
exl-id: a945b255-a9b0-42f4-85ea-44416c837fc0
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Rapporter

Med resultatrapporter kan ni spåra och hantera resultatet för era portföljer, annonsnätverk och annonsnätverkskontoenheter på så detaljerad nivå som ni vill. De flesta rapporter ger fullständig insyn i hur annonserna i varje marknadsföringskanal bidrar till den totala konverteringsgraden.

Data för en rapport kompileras dynamiskt varje gång du kör rapporten. Du kan också generera en ny rapport från en befintlig rapport. Vilka rapportparametrar som är tillgängliga varierar beroende på rapporttyp. För de flesta rapporter kan du förhandsgranska de första 50 raderna i stället för att generera hela rapporten. När du genererar en rapport kan du skicka ett meddelande med nedladdningslänkar till en eller flera e-postadresser när rapporten är klar, och mottagarna kan [hantera meddelanden i [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Alla slutförda rapporter finns i [!UICONTROL Latest Reports] i [!UICONTROL Reports] och du kan antingen visa dem i tabellformat i webbläsarfönstret eller öppna eller ladda ned dem som filer.

## Tillgängliga rapportkategorier

Följande rapportkategorier är tillgängliga från [!UICONTROL Reports] vy. Du kanske inte har tillgång till alla, tillgängliga rapporter och data som de genererar avgörs av din roll och hur ditt kundkonto är konfigurerat.

| Rapportkategori | Beskrivning |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Grundläggande rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), som är tillgängliga för alla användare, visa den faktiska kostnaden och klicka på data för portföljer, annonsnätverkskonton, specifika annonsnätverkskonton, kampanjer, annonsgrupper, annonser, nyckelord, produktgrupper, etikettklassificeringar och etikettvärden, begränsningar för budenheter och nätverksbegränsningar. De baseras på klick som faktureras av tillämpliga annonsnätverk och de kan även innehålla konverteringsdata eller andra mätvärden som du skapar. |
| [!UICONTROL Advanced Reports] | [Avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) ge ytterligare insikter i er annonskonfiguration, så att ni kan identifiera var ni kan dra nytta av detta genom att ändra er geografiska målinriktning eller nätverksinställningar. De kan också hjälpa er att validera konverteringsdata i kampanjer, portföljhanteringsvyer och rapporter mot annonsörens interna konverteringsspårningsdata. |
| [!UICONTROL Assist Reports] | [Assistentrapporter](/help/search-social-commerce/reports/management/assist/assist-report-about.md) ge insikter om konverteringsmöjligheterna för alla annonsörers nyckelord och annonser. De använder data som samlats in via tjänsten för spårning av konvertering till Adobe Advertising och kan bara genereras för annonsörer som har tjänsten. |
| [!UICONTROL Specialty Reports] | [Specialrapporter](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) De består av uppgifter som samlats in av annonsnätverken (i stället för av spårning av Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Rapporter om modellprecision](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) ange riktigheten i de kostnads- och intäktsmodeller som används för att optimera anbud. |

## Automatisering av rapporter

Schemalägg anpassade rapporter som ska genereras automatiskt på något eller båda av följande sätt:

* Generera rapporter automatiskt varje dag, eller en viss dag i veckan eller månaden, med [rapportmallar](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Du kan välja att konfigurera [FTP-leverans av grundläggande och avancerade rapporter](/help/search-social-commerce/reports/automation/ftp-reports.md) som använder en mall.

* Uppdatera kalkylbladsmallar med dagliga prestandadata med [kalkylarksflöden](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Vyerna Rapporter

The [!UICONTROL Reports] vyer på [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] I kan du skapa och hantera rapporter, mallar och kalkylbladsflöden. Vyn innehåller två flikar:

* The **[!UICONTROL Latest Reports]** På -fliken visas alla rapporter som är tillgängliga för dig och som har begärts under de senaste sju dagarna, förutom de som har tagits bort manuellt, med den senaste rapporten överst som standard. Den information som visas för varje rapport omfattar schemat för körning (i tillämpliga fall), start- och slutdatum för vilka data genererades eller kommer att genereras samt rapportens status (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]*, eller *[!UICONTROL Error]*).

  Med hjälp av länkar bredvid varje rapport kan du visa rapporten i webbläsaren eller öppna eller spara den som en [!DNL Microsoft Excel] arbetsbok (XLS) eller tabbseparerad värdefil (TSV); vissa rapporttyper kan också sparas som [!UICONTROL Excel] arbetsböcker med ett separat kalkylblad för varje tillämplig kampanj.

  På den här fliken kan du även skapa en ny rapport (som kan användas som mall), skapa en ny rapport baserat på inställningarna för en befintlig rapport, avbryta pågående rapporter som är tillgängliga för dig genom att ta bort dem och ta bort alla slutförda rapporter som är tillgängliga för dig. Rapporter som är äldre än sju dagar tas automatiskt bort.

* The **[!UICONTROL Templates]** På -fliken visas alla sparade grundläggande och avancerade rapportmallar som du har tillgång till, inklusive information om scheman som är kopplade till dem. Den senaste mallen visas överst som standard.

  På den här fliken skapar du en ny mall, redigerar en mall som du har skapat (t.ex. lägger till, ändrar eller tar bort schemat), skapar en rapport från en mall och tar bort alla mallar som är tillgängliga för dig.

## Så här använder du rapporter

| Syfte | Rapport |
| ---- | ---- |
| Prestandaövervakning | <ul><li>[The [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[The [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[The [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[The [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[The [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[The [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Prestandafelsökning och trendanalys | <ul><li>[The [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[The [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[The [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[The [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[The [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) och [The [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Alla grundläggande rapporter som jämför två tidsfönster med[!UICONTROL Compare with]&quot;-funktion</li></ul> |
| Identifiera affärstillväxtmöjligheter | <ul><li>(Annonsörer med endast spårning av konvertering till Adobe Advertising) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Annonsörer med endast spårning av konvertering till Adobe Advertising) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Annonsörer med [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Anpassade rapporter i Adobe Analytics Analysis Workspace</li></ul> |
| Analyser | <ul><li>(Annonsörer med endast spårning av konvertering till Adobe Advertising) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Annonsörer med [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Anpassade rapporter i Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Data som används för rapporter](data-used-for-reports.md)
>* [Inledande inställningsuppgifter för rapporter](initial-setup.md)
>* [Generera en grundläggande eller avancerad rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Generera en modellnoggrannhetsrapport](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Generera en specialrapport](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Generera en assistentrapport](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
