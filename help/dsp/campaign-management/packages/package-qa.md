---
title: Granska och redigera paketinställningar med hjälp av flera kalkylblad
description: Lär dig hur du granskar och redigerar inställningar för nyckelpaket i grupp med kalkylblad.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Granska och redigera paketinställningar med hjälp av flera kalkylblad

Du kan hämta inställningarna för ett eller flera paket i XLSX-format ([!DNL Microsoft Excel] kalkylblad) för granskning. Filen *bulksheet* innehåller en separat flik med flyginformation.

Om du vill uppdatera flera inställningar samtidigt kan du göra något av följande:

* Gör ändringar i markerade fält, spara filen och överför den redigerade kalkylbladsfilen tillbaka till DSP.

* Om du vill ändra ytterligare paket, praktik eller annonser i kampanjen hämtar du ett kalkylblad för kampanjen. Ange eller klistra in uppdaterade inställningar i filen och överför sedan filen för att göra ändringarna. Instruktioner finns i &quot;[Granska och redigera inställningar för Campaign-komponenten med hjälp av gruppblad](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Redigerbara fält innehåller de flesta inställningar som normalt är redigerbara.

>[!TIP]
>
>Mer information om hur du snabbt redigerar fler fält för ett eller flera paket finns i [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md).

## Hämta inställningar för alla paket i en kampanj

När du hämtar inställningar för alla paket i en kampanj innehåller kalkylbladet separata flikar för paketinställningarna och för flyginformationen. Du kan även inkludera inställningar för de placeringar och annonser som är kopplade till paketen. Ytterligare flikar inkluderas för placerings- och annonsinställningar.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Gör något av följande:

   * Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** bredvid kampanjen.

   * Klicka på kampanjnamnet. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** i det övre högra hörnet.

1. Avmarkera de kampanjkomponenter vars inställningar du vill utesluta från den hämtade filen i dialogrutan [!UICONTROL Bulksheet Download] och klicka sedan på **[!UICONTROL Download]**.

Som standard väljs inställningar för alla placeringar och annonser som är kopplade till paketen.

Ett meddelande visas när filen är tillgänglig för hämtning.

1. Gör något av följande om du vill hämta filen:

   * Klicka på **[!UICONTROL Download]i meddelandet.**

   * Klicka på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden. Klicka på **[!UICONTROL Download]** bredvid jobbet.

     Filen sparas i webbläsarens hämtningsmapp.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Om du vill redigera någon av inställningarna redigerar du filen direkt och överför sedan ändringarna. Alla redigerbara kolumner markeras med blått.

## Hämta inställningar för specifika paket

När du hämtar inställningar för specifika paket innehåller kalkylbladsfilen separata flikar för paketinställningarna och för flyginformationen, och filen kan redigeras.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Packages]** på undermenyn.

1. Markera kryssrutorna för de paket vars inställningar du vill hämta.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** i verktygsfältet för gruppåtgärder.

   Ett meddelande visas när kalkylbladsfilen är tillgänglig för hämtning.

1. Gör något av följande om du vill hämta kalkylbladet:

   * Klicka på **[!UICONTROL Download]i meddelandet.**

   * Klicka på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden. Klicka på **[!UICONTROL Download]** bredvid jobbet.

     Filen sparas i mappen Downloads i webbläsaren. En lista över de inkluderade kolumnerna finns i [Placera kolumner i hämtade/överförda bulkblad](#qa-sheet-columns).

     Om du vill redigera någon av inställningarna redigerar du filen direkt och överför sedan ändringarna. Alla redigerbara kolumner markeras med blått. Om du vill använda rätt format för ett fält markerar och kopierar du värdet från den relevanta paketinställningen eller placeringsinställningen. För vissa målinställningar, t.ex. dagdelning, anpassade mål och konverteringsmått, finns det ett kopieringsalternativ i inställningen.

## Överför ett kalkylblad med paketinställningar {#upload-bulksheet-package}

Du kan överföra inställningar för dina paket, inklusive de placeringar och annonser som är kopplade till paketen, i en kalkylbladsfil.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Gör något av följande:

   * Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** bredvid den överordnade kampanjen.

   * Klicka på kampanjnamnet. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** i det övre högra hörnet.

     Det här alternativet är tillgängligt på fliken [!UICONTROL Packages], [!UICONTROL Placements] eller [!UICONTROL Ads].

   * Klicka på **[!UICONTROL Packages]** på undermenyn och markera kryssrutan för ett paket. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** i verktygsfältet för gruppåtgärder.

1. I dialogrutan [!UICONTROL Upload Bulksheet]:

   1. Dra och släpp en fil i rutan eller klicka i rutan för att välja en fil från enheten eller nätverket.

   1. Klicka på **[!UICONTROL Upload]**.

1. (Valfritt) Om du vill verifiera att uppdateringarna har bearbetats klickar du på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden.

När en inställningsuppdatering misslyckas kan du hämta en felfil för kalkylblad med färgkodning för att visa vilka inställningar (rader) som sparades och som misslyckades, med en orsak till varje fel. Du kan sedan åtgärda problemen i samma fil och överföra den igen för att bearbeta den korrigerade informationen.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Granska och redigera inställningar för Campaign-komponenten med hjälp av gruppblad](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
