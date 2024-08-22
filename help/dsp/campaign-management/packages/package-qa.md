---
title: Granska och redigera paketinställningar med kalkylblad
description: Lär dig hur du granskar och redigerar inställningar för nyckelpaket med hjälp av kalkylblad.
feature: DSP Packages
source-git-commit: ad00092c4ef5d44c364ab0593826220054f715c3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Granska och redigera paketinställningar med kalkylblad

Du kan hämta inställningarna för ett eller flera paket i XLSX-format ([!DNL Microsoft Excel] kalkylblad) för granskning. Kalkylbladet innehåller en separat flik med flyginformation. Du kan sedan ändra fälten på båda flikarna och överföra data till DSP alla samtidigt. Redigerbara fält innehåller de flesta inställningar som normalt är redigerbara.

>[!TIP]
>
>Mer information om hur du redigerar fler fält för ett eller flera paket finns i [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md).

## Hämta inställningar för ett eller flera paket

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Packages]** på undermenyn.

1. Markera kryssrutan bredvid varje paket vars inställningar du vill hämta.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]** i verktygsfältet för gruppåtgärder.

Filen sparas automatiskt i webbläsarens hämtningsmapp. En lista över de kolumner som ingår finns i [Paketera kolumner i hämtade/överförda kalkylblad](#qa-sheet-columns-packages).

## Överför inställningar för ett eller flera paket

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Packages]** på undermenyn.

1. Markera kryssrutan bredvid varje paket vars inställningar du vill överföra.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]** i verktygsfältet för gruppåtgärder.

1. I dialogrutan [!UICONTROL Edit in Excel]:

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

### Fliken [!UICONTROL Package_Flights]

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
>* [Redigera paket](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
