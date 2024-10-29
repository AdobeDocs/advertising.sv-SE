---
title: Granska och redigera paketinställningar med hjälp av flera kalkylblad
description: Lär dig hur du granskar och redigerar inställningar för nyckelpaket i grupp med kalkylblad.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Granska och redigera paketinställningar med hjälp av flera kalkylblad

Du kan hämta inställningarna för ett eller flera paket i XLSX-format ([!DNL Microsoft Excel] kalkylblad) för granskning. Kalkylbladet innehåller en separat flik med flyginformation.

Om du vill uppdatera flera inställningar samtidigt kan du göra något av följande:

* Gör ändringar i markerade fält, spara filen och överför den redigerade kalkylbladsfilen tillbaka till DSP.

* Om du vill göra ändringar i ytterligare paket, och i inställningarna för en placering eller annons, hämtar du en tom mall som innehåller flikar för varje typ av kampanjkomponent, anger eller klistrar in nya eller uppdaterade inställningar i mallfilen och överför sedan filen för att göra ändringarna. Instruktioner finns i &quot;[Granska och redigera inställningar för Campaign-komponenten med hjälp av gruppblad](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Redigerbara fält innehåller de flesta inställningar som normalt är redigerbara.

>[!TIP]
>
>Mer information om hur du snabbt redigerar fler fält för ett eller flera paket finns i [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md).

## Hämta inställningar för alla paket i en kampanj

När du hämtar inställningar för alla paket i en kampanj innehåller kalkylbladet separata flikar för paketinställningarna och för flyginformationen. Du kan även inkludera inställningar för de placeringar och annonser som är kopplade till paketen. Ytterligare flikar inkluderas för placerings- och annonsinställningar.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]** i det övre högra hörnet.

1. Avmarkera de kampanjkomponenter vars inställningar du vill utesluta från den hämtade filen i dialogrutan [!UICONTROL QA Sheet Download] och klicka sedan på **[!UICONTROL Download]**.

Som standard väljs inställningar för alla placeringar och annonser som är kopplade till paketen.

Ett meddelande visas när filen är tillgänglig för hämtning.

1. Gör något av följande om du vill hämta filen:

   * Klicka på **[!UICONTROL Download]i meddelandet.**

   * Klicka på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden. Klicka på **[!UICONTROL Download]** bredvid jobbet.

     Filen sparas i mappen Downloads i webbläsaren. En lista över de kolumner som ingår finns i [Placera kolumner i hämtade/överförda kalkylblad](#qa-sheet-columns).

>[!NOTE]
>
>Du kan inte redigera och överföra QA-blad på kampanjnivå igen. Om du vill ändra inställningarna för kampanjkomponenten i de här filerna hämtar du en separat mall för kalkylblad, anger eller klistrar in rader från QA-bladet i mallen för kalkylblad, sparar filen och överför sedan det ifyllda kalkylbladet. Instruktioner finns i &quot;[Granska och redigera inställningar för Campaign-komponenten med hjälp av gruppblad](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

## Hämta inställningar för ett eller flera paket

När du hämtar inställningar för specifika paket innehåller kalkylbladsfilen separata flikar för paketinställningarna och för flyginformationen, och filen kan redigeras.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Packages]** på undermenyn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** i verktygsfältet för gruppåtgärder.

   Ett meddelande visas när kalkylbladsfilen är tillgänglig för hämtning.

1. Gör något av följande om du vill hämta kalkylbladet:

   * Klicka på **[!UICONTROL Download]i meddelandet.**

   * Klicka på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden. Klicka på **[!UICONTROL Download]** bredvid jobbet.

     Filen sparas i mappen Downloads i webbläsaren. En lista över de kolumner som ingår finns i [Placera kolumner i hämtade/överförda kalkylblad](#qa-sheet-columns).

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Överför ett kalkylblad med paketinställningar {#upload-bulksheet-package}

Du kan överföra inställningar för dina paket, inklusive de placeringar och annonser som är kopplade till paketen, i en kalkylbladsfil.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** i det övre högra hörnet.

1. I dialogrutan [!UICONTROL Upload Bulksheet]:

   1. Dra och släpp en fil i rutan eller klicka i rutan för att välja en fil från enheten eller nätverket.

   1. Klicka på **[!UICONTROL Upload]**.

1. (Valfritt) Om du vill verifiera att uppdateringarna har bearbetats klickar du på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden.

## Paketera kolumner i hämtade/överförda kalkylblad{#qa-sheet-columns-packages}

>[!TIP]
>
> I ett nedladdat kalkylblad markeras alla redigerbara kolumner med blått.

### Fliken [!UICONTROL Package]

| Avsnitt | Kolumn | Beskrivning | Redigerbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | Paketets numeriska ID. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | Paketets namn. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Status] | Paketstatus: *[!UICONTROL active]* eller *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Description] | En valfri beskrivning av paketet. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per 1000 visningar, om tillämpligt. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | En valfri beskrivning av tredjepartsavgiften, om tillämpligt. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | Paketets startdatum. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | Paketets slutdatum. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | På vilken nivå placeras plats och ändpunkter i paketet: *[!UICONTROL Package]* eller *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Paketbudgeten. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Budgetintervallet: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* eller *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | En valfri övre gräns för budgetintervall. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Intervallet för det valfria budgetintervallets tak: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* eller *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | Paketets syfte. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | Målvärdet för målet. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Endast paket med optimeringsmålen [!UICONTROL Highest Return on Ad Spend] och [!UICONTROL Lowest Cost per Acquisition]) Ett [anpassat mål](/help/dsp/optimization/custom-goal.md) som innehåller de intäkt- eller konverteringshändelser som används för att beräkna CPA- eller ROAS-måttet. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Valfritt; paket med optimeringsmålen [!UICONTROL Highest Return on Ad Spend] och [!UICONTROL Lowest Cost per Acquisition]) Den slutliga konverteringshändelsen eller intäktshändelsen/försäljningsbeloppet som ska användas för att beräkna avkastningen på annonskostnaderna eller kostnaden per förvärv. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Paket med enbart anpassade optimeringsmål) Paketets syfte, som hjälper till att avgöra hur paketet ska optimeras: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* eller *[!UICONTROL Other]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Endast paket med anpassade optimeringsmål) Paket-ID:t för ett annat paket vars tidigare data används som indata för optimering av paketet. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Endast paket med anpassade optimeringsmål) Ett annat paket vars tidigare data används som indata för optimering av paketet. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Anger om paketet ska paketeras mot *[!UICONTROL budget]* eller *[!UICONTROL primary_goal]* (för visningar). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (När du placerar paketet på visningar) Målantalet visningar under det angivna tidsintervallet. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (När du placerar paketet på visningar) Tidsintervallet för målantalet visningar. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | Flygpaketeringsstrategin för paketet: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* eller *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | Intraday-paketeringsstrategi för paketet: *[!UICONTROL Even]* eller *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Den primära frekvensen för paketet under angiven [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Intervallet för den primära frekvensbegränsningen: *[!UICONTROL Day]*, *[!UICONTROL Week]* eller *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Antalet veckor, dagar, timmar eller minuter som primär [!UICONTROL Frequency Cap] gäller för. Om det primära gränsvärdet till exempel är 12 visningar per månad blir värdet här `12`. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Den sekundära frekvensen för paketet under den angivna [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Intervalltypen för den sekundära frekvensbegränsningen: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* eller *[!UICONTROL Minute]*. Det tillämpliga antalet veckor, dagar, timmar eller minuter anges av [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Antalet veckor, dagar, timmar eller minuter som [!UICONTROL Secondary Frequency Cap] gäller. Om det sekundära gränsvärdet till exempel är tre avtryck per sex timmar blir värdet här `6`. | Ja |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Om icke-jämna mellanrum ska skapas för paketet *T* (true) eller *F* (false). När du har aktiverat anpassad felsökning och sparat paketet kan du inte inaktivera anpassad felsökning eller redigera paketets startdatum. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Endast tillgängligt när alternativet [!UICONTROL Activate Custom Flighting] är aktiverat) Om du vill lägga till återstående budget automatiskt från föregående flygning till den befintliga budgeten för nästa flygning eller inte: *T* (true) eller *F* (false). | Ja |
| [!UICONTROL Error] | [!UICONTROL Error] | Alla relevanta fel. | — |

### Fliken [!UICONTROL Package_Flights] {#qa-sheet-columns-package-flights}

| Avsnitt | Kolumn | Beskrivning | Redigerbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Paketets numeriska ID. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Det numeriska ID:t för flygningen. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | Flygningens första datum. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | Slutdatum för flygningen. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | Målet för flygresan. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Befintliga paket utan alternativet [!UICONTROL Automatically rollover remaining flight budget to next flight] aktiverat) Ett belopp med eventuellt oanvänd budget att lägga till i nästa flight. | Ja |

>[!MORELIKETHIS]
>
>* [Granska och redigera inställningar för Campaign-komponenten med hjälp av gruppblad](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
