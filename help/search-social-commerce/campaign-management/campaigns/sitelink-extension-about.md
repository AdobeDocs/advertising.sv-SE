---
title: Om tillägg för sitelink
description: Lär dig mer om tillägg för sitelink.
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Om tillägg för sitelink

*[!DNL Google Ads]och [!DNL Microsoft Advertising] only*

En sitelink är en extra textlänk i en textannonslista. Använd sitelinks för att dirigera användare direkt till specifika sidor på webbplatsen. Annonsnätverket avgör vilka sitelinks som ska visas med en annons, baserat på hur relevant sitelink är för annonsen. Du kan också inkludera beskrivande text för varje sitelink, som kan inkluderas i annonsen. Annonsnätverket kan automatiskt visa och kopiera från befintliga annonser på kontot med sitelink när annonskopian är mycket relevant för sitelänken. [!DNL Google Ads] kan visa 2-6 sitelinks i en skrivbordsannons och upp till fyra sitelinks i en mobilannons. [!DNL Microsoft Advertising] kan visa två, fyra eller sex sitelinks med beskrivningar eller 4-6 sitelinks utan beskrivningar.

Du skapar text och inställningar för delad sitelink, inklusive datum då sitelinks kan visas med annonser, på kontonivån.

## [!UICONTROL Sitelinks]- och [!UICONTROL Associations]-vyerna

I biblioteket [!UICONTROL Extensions] > [!UICONTROL Sitelinks] i [!UICONTROL Campaigns] > [!UICONTROL Campaigns] visas alla dina sitelinks på kontonivå, och du kan skapa och hantera dina delade sitelinks där. I annonsnätverkshjälpen finns det maximala antalet annonseringstillägg per [[!DNL Google Ads] konto](https://support.google.com/google-ads/answer/6372658) och per [[!DNL Microsoft Advertising] konto](https://help.ads.microsoft.com/#apex/3/en/52001). Webbplatslänkar i ditt bibliotek används inte med dina annonser förrän du tilldelar dem till kontoenheter.

Från vyn [!UICONTROL Extensions] > [!UICONTROL Associations] kan du tilldela alla dina sitelinks som möjliga tillägg till alla annonser på kontonivå ([!DNL Google Ads] enbart), kampanjnivå eller annonsgruppsnivå ([!DNL Google Ads] enbart).

## Prestandadata för sitelinks

Search, Social, &amp; Commerce mappar klickningarna på ett tillägg och den resulterande konverteringen till nyckelordet som är associerat med den annons som tillägget ingår i. Det finns inga kostnadsdata eller klickdata på tilläggsnivån i Search, Social och Commerce. I [&#x200B; [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) kan du dock se om en transaktion har skapats från en sitelink (i stället för från själva annonsen) när värdet i kolumnen Länktyp anges som `sl:<Sitelink text>`, till exempel sl:See Current Offers.

I [!DNL Google Ads] och [!DNL Microsoft Advertising] kan du se kostnad och klicka på data på fliken [!DNL Ad Extensions].

>[!MORELIKETHIS]
>
>* [Hantera delade tillägg för sitelink](sitelink-extension-manage.md)
>* [Associera delade tillägg för sitelink med kampanjer eller annonsgrupper](sitelink-extension-associate.md)
