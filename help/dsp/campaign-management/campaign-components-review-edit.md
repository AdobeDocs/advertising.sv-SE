---
title: Granska och redigera inställningar för Campaign-komponenten med hjälp av flera kalkylblad
description: Lär dig hur du granskar och redigerar viktiga paket-, placerings- och annonsinställningar i grupp med kalkylblad.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Granska och redigera inställningar för Campaign-komponenten med hjälp av flera kalkylblad

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

Du kan hämta inställningarna för paket, placeringar och annonser i en enda kampanj i XLSX-format ([!DNL Microsoft Excel] kalkylblad) för granskning. Som standard innehåller den hämtade filen separata flikar för paketinställningar, paketflyginformation, placeringsinställningar och monteringsscheman. Du kan också exkludera inställningarna för vissa kampanjkomponenttyper.

Om du vill uppdatera flera inställningar samtidigt överför du en giltig kalkylbladsfil med ändringarna. Om du vill skapa kalkylbladet kan du hämta en tom mall med flikar för varje typ av kampanjkomponent, ange eller klistra in nya eller uppdaterade inställningar i mallfilen och sedan spara filen för att överföra den. Redigerbara fält innehåller de flesta inställningar som normalt är redigerbara.

>[!NOTE]
>
>Du kan även hämta och redigera inställningarna för enbart specifika paket och specifika placeringar. Se &quot;[Granska och redigera paketinställningar med hjälp av bulkblad](/help/dsp/campaign-management/packages/package-qa.md)&quot; och &quot;[Granska och redigera placeringsinställningar med hjälp av bulkblad](/help/dsp/campaign-management/placements/placement-qa.md).&quot;

## Hämta inställningar för paket, placeringar och annonser i en kampanj

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]** i det övre högra hörnet.

1. Avmarkera de kampanjkomponenter vars inställningar du vill utesluta från den hämtade filen i dialogrutan [!UICONTROL QA Sheet Download] och klicka sedan på **[!UICONTROL Download]**.

Som standard väljs inställningar för alla kampanjkomponenter.

Ett meddelande visas när filen är tillgänglig för hämtning.

1. Gör något av följande om du vill hämta filen:

   * Klicka på **[!UICONTROL Download]i meddelandet.**

   * Klicka på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden. Klicka på **[!UICONTROL Download]** bredvid jobbet.

     Filen sparas i mappen Downloads i webbläsaren. En lista över de kolumner som ingår finns i [Placera kolumner i hämtade/överförda kalkylblad](#qa-sheet-columns).

>[!NOTE]
>
>Du kan inte redigera och överföra QA-filer på kampanjnivå igen. Om du vill ändra inställningarna för kampanjkomponenten i de här filerna [hämtar du en separat inställningsmallfil (konfigurationsfil)](#download-template), anger eller klistrar in rader från QA-filen i mallen och sparar filen. Sedan [överför du den ifyllda mallfilen](#upload-bulksheet-campaign-components).

## Ladda ned en gruppmallsmall för en kampanj {#download-template}

Hämta en tom mall med flikar för varje typ av kampanjkomponent. Du kan lägga till rader senare på valfri flik i mallen och [överföra den redigerade filen](##upload-bulksheet-campaign-components) för att göra ändringar i kampanjkomponenterna.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** i det övre högra hörnet.

1. Klicka på **[!UICONTROL Bulksheet Template]i dialogrutan [!UICONTROL Upload Bulksheet].**

   Filen sparas i mappen Downloads i webbläsaren. En lista över de kolumner som ingår finns i [Placera kolumner i hämtade/överförda kalkylblad](#qa-sheet-columns).

## Ladda upp ett bulkblad med paket, placering och annonsinställningar för en kampanj{#upload-bulksheet-campaign-components}

Överför inställningar för paket, praktik och annonser i en enda kampanj i ett ifyllt kalkylblad.

1. [Hämta en kalkylbladsmall](#download-template) om det behövs, ange eller klistra in paket, placering och/eller annonsinställningar på de relevanta flikarna i en kalkylbladsmall och spara sedan filen på enheten eller i nätverket.

   Se de tillgängliga inställningarna nedan.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** i det övre högra hörnet.

1. I dialogrutan [!UICONTROL Upload Bulksheet]:

   1. Dra och släpp en fil i rutan eller klicka i rutan för att välja en fil från enheten eller nätverket.

   1. Klicka på **[!UICONTROL Upload]**.

1. (Valfritt) Om du vill verifiera att uppdateringarna har bearbetats klickar du på ![Jobb](/help/dsp/assets/downloads.png) till höger om den övre menyraden.

## Placera kolumner i hämtade/överförda kalkylblad{#qa-sheet-columns}

>[!TIP]
>
> I ett nedladdat kalkylblad markeras alla redigerbara kolumner med blått.

### Kampanjnivåkalkylblad

| Avsnitt | Kolumn | Beskrivning | Redigerbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Placeringens numeriska ID. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Placeringens namn. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Etiketter som används för rapportering. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | En länk för att öppna placeringen i redigeringsläget. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Placeringsstatus: *[!UICONTROL active]* eller *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Placeringstypen. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Namnet på det överordnade paketet, om tillämpligt. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Placeringens startdatum. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Placeringens slutdatum. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Anger om dagen är *[!UICONTROL ON]* eller *[!UICONTROL OFF]*.<br><b>Obs!</b> Om du vill kontrollera det faktiska sommarschemat öppnar du placeringsinställningarna i DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Placeringsbudgeten, om det finns en sådan. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Budgetintervallet: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* eller *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Paketets syfte. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Målvärdet för målet. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Anger om placeringen är i linje med *[!UICONTROL Budget]* eller *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Det högsta anbudet för placeringen. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Flightpaketeringsstrategin för placeringen: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* eller *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Intraday-paketeringsstrategi för placeringen: *[!UICONTROL Even]* eller *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Eventuella filtervillkor före bud som ska tillämpas. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Om budgivningsreglerna (inaktuella) är *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Det primära frekvensskyddet för placeringen under den angivna [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervallet för den primära frekvensbegränsningen: *[!UICONTROL Day]*, *[!UICONTROL Week]* eller *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Det sekundära frekvensskyddet för placeringen under angiven [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Intervalltypen för den sekundära frekvensbegränsningen: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* eller *[!UICONTROL Minute]*. Det tillämpliga antalet veckor, dagar, timmar eller minuter anges av [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Antalet veckor, dagar, timmar eller minuter som [!UICONTROL Secondary Frequency Cap] gäller. Om det sekundära gränsvärdet till exempel är tre avtryck per sex timmar blir värdet här `6`. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Antalet riktade geografiska platser, *[!UICONTROL All]* eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | De angivna geografiska platserna, avgränsade med semikolon eller *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Antalet uteslutna geografiska platser eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Undantagna geografiska platser, avgränsade med semikolon eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Antalet riktade offentliga inventeringserbjudanden, om sådana har angetts, *[!UICONTROL All]* eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Antalet uteslutna offentliga lagererbjudanden, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Antalet riktade privata lagererbjudanden, om sådana har angetts, *[!UICONTROL All]* eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Antalet uteslutna privata lagererbjudanden, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Antalet riktade [!UICONTROL On-Demand Inventory] erbjudanden, om sådana har angetts, *[!UICONTROL All]* eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Antalet uteslöta behovsbaserade inventeringsavtal, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Måltypen för trafik: *[!UICONTROL Website]* och/eller *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Anger om alternativet Inventory Targeting för att exkludera trafik utanför strömmen är &lt;i[!UICONTROL >ON]* eller *[!UICONTROL OFF]*.<br>Outstream-annonser visas vanligtvis över innehållet som ett popup-fönster eller instoppat i innehåll (i den ursprungliga upplevelsen), i stället för som vanliga videoannonser i en videospelare. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Kvaliteten på de webbplatser som ska målas: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* eller *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Antalet målwebbplatskategorier, om sådana har angetts, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Antalet uteslutna webbplatskategorier, om sådana har angetts, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Undantagna webbplatser, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Målwebbplatsspråken. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Endast standardvisningsplaceringar) Om annonsleverans ska tillåtas på webbplatser som inte är granskade: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. När placeringen avser privat lager kan det här alternativet leverera annonser på blockerade webbplatser. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Antalet målwebbplatser, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Målgrupperna, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | De uteslutna målgrupperna, om det finns några, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Anger om [!DNL Comscore] demografiska segment är aktiverade för placeringen (och andra placeringar i kampanjen): *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. Den här funktionen kan bara aktiveras för kampanjer för vilka funktionen [!DNL Audience Verification] är aktiverad för [!DNL Nielsen] och/eller [!DNL Comscore].  Det medför ytterligare avgifter. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Anger om annonsen ska utökas för olika enheter: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. Målinriktning på flera enheter utökar er målinriktning på alla en persons kända enheter, enligt det enhetsdiagram som anges i kampanjinställningarna. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Inkluderat # | Antalet målämneskoder, om sådana finns, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Antalet undantagna ämneskoder, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Antalet målenhetsmål, om några, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Antalet uteslutna enhetsmål, om några, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Antalet riktade ISP-providers, om sådana finns, eller *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Antalet utelämnade ISP-providers, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Antalet säkerhetsfilter för varumärke som används, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Antalet filter för spärrning av bedrägeri före bud har tillämpats, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Antalet visningsfilter före bud som används, om sådana har angetts, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Om Site Safety Block är aktiverat eller inte: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Antalet pixlar för händelsespårning från tredje part som är kopplade till placeringen, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Antalet pixlar för konverteringsspårning som är kopplade till placeringen, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per 1000 visningar, om tillämpligt. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Antalet annonser som är kopplade till placeringen, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Namnen på alla annonser som är kopplade till placeringen, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Unika DSP-genererade ID:n för annonser som är kopplade till placeringen, avgränsade med semikolon. Om du vill hämta en lista med annonsnamn och associerade ID:n från vyn [!UICONTROL Ads] skapar du en anpassad vy som innehåller måttet [!UICONTROL Ad ID] och [exporterar sedan data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Ja |

>[!MORELIKETHIS]
>
>* [Granska och redigera paketinställningar med hjälp av flera blad](/help/dsp/campaign-management/packages/package-qa.md)
>* [Granska och redigera placeringsinställningar med hjälp av kalkylblad](/help/dsp/campaign-management/placements/placement-qa.md)
