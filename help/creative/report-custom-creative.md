---
title: '[!UICONTROL Custom Creative Report]'
description: Lär dig hur du genererar korsgränssnittet [!UICONTROL Custom Creative Report].
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: 3033f26bba5a9e7622d0de51b36035be1005c60f
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*Stängd beta*

Med [!UICONTROL Custom Creative Report] kan du anpassa innehållet och leveransen av rapportdata för alla era annonsupplevelser.

Du kan generera rapporter en gång, eller schemalägga dem dagligen, veckovis eller månadsvis kl. 03:00 i den angivna tidszonen enligt angivna villkor (t.ex. var 15:e dag eller den 1:e varje månad). När en rapport har skapats kan du hämta den från [!UICONTROL Reports] > [!UICONTROL Custom Reports] eller från länkade [rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md) av följande typer:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

## Skapa en [!UICONTROL Custom Creative Report]

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create]** i det övre högra hörnet.

1. Ange [rapportinställningarna](#report-settings).

1. Klicka på **[!UICONTROL Create Custom Report]**.

## Rapportinställningar {#report-settings}

**[!UICONTROL Name]:** Rapportnamnet. Maximala längden är 180 tecken.

**[!UICONTROL Report Type]:** Typ av rapport: *[!UICONTROL Custom Creative Beta]*.

### [!UICONTROL Report Range] avsnitt

Det här avsnittet avgör vilka data som tas med i rapporten. Information om hur du ställer in datum för rapportschemat finns i avsnittet [!UICONTROL Report run schedule].

**[!UICONTROL Timezone]:** Tidszonen för rapportering.

**[!UICONTROL Observe Daylight Savings Time]:** anser att sommartid kan användas under de rapporterade tiderna.

**Intervall:** Datumintervallet som data ska genereras för. Antalet tillgängliga dagar varierar beroende på rapport och valda dimensioner. Välj ett alternativ:

* **[!UICONTROL Previous Calendar Week]:** Inkluderar data för föregående kalendervecka.

* **[!UICONTROL Previous Calendar Month]:** Inkluderar data för föregående kalendermånad.

* **[!UICONTROL Custom Range]:** Inkluderar data mellan specifika start- och slutdatum. Om du vill rapportera data genom föregående dag väljer du **[!UICONTROL Present]**.

### [!UICONTROL Report Run schedule] avsnitt

I det här avsnittet anges de datum då rapporten körs. Information om hur du ställer in datum för vilka rapportdata ska inkluderas finns i avsnittet [!UICONTROL Report range].

**\[Schema\]:** När rapporten ska genereras:

* *[!UICONTROL Immediately]*: Lägger omedelbart till rapporten i rapportkön.

  >[!NOTE]
  >
  >Du kan också [köra en anpassad rapport när som helst](/help/dsp/reports/report-run-now.md) från vyn [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Kör rapporten på ett angivet datum för slutförande senast 09:00 i kontots tidszon.

* *[!UICONTROL Recurring]:* Kör rapporten enligt ett schema under en angiven tidsperiod.

   * **\[Schedule\]:** Hur ofta rapporten ska köras:

      * *Dagligen* om du vill köra rapporten var N:e dag. Om du till exempel vill köra rapporten varannan vecka (14 dagar) markerar du det här alternativet och anger **14**.

      * *Veckovis* om du vill köra rapporten på angivna veckodagar. Om du till exempel vill köra rapporten varje måndag och fredag markerar du det här alternativet och markerar kryssrutorna intill **måndag** och **fredag**.

      * *Månadsvis* om du vill köra rapporten på en viss numerisk dag i månaden, från 1 till 30. Kör till exempel rapporten den första dagen i varje månad, markera det här alternativet och ange **1**.

   * **Från**: Det första datum då rapporten kan köras. Beroende på angivet schema kan den första rapportinstansen inträffa efter detta datum.

   * **Till**: Rapportens förfallodatum, som kan vara upp till fyra kalendermånader bort. Innan en rapport förfaller får alla angivna e-postmål en e-postavisering sju dagar och en dag före förfallodatumet. Ändra det här datumet om du vill behålla rapporten längre.

### [!UICONTROL Apply Filters] avsnitt

**[!UICONTROL Filter by]:** (Valfritt) Ytterligare dimensioner som data kan filtreras med, oavsett om dimensionerna inkluderas som kolumner i rapporten eller inte. De tillgängliga filtren varierar beroende på rapporttyp och kan omfatta: *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* och *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Så här använder du ett eller flera filter:

* Välj en dimension, markera operatorn (*är lika med* eller *är inte lika med*) och välj sedan önskat värde. Om du till exempel vill returnera data för enbart förhandsannonser anger du [!UICONTROL Ad Type equals Preroll].
* (Valfritt) Lägg till ytterligare villkor till filtret.
* (Valfritt) Lägg till ytterligare filter, där vart och ett har ett eller flera villkor.

### [!UICONTROL Build Your Report] avsnitt

**[!UICONTROL Select To Add As Report Headers]:** Datakolumner, eller rubriker, som ska inkluderas i rapporten. Om du vill lägga till en kolumn expanderar du kategorin och markerar kryssrutan bredvid kolumnnamnet. De tillgängliga kolumnerna varierar beroende på rapport, och alla otillgängliga värden är inaktiverade. Se [Tillgängliga rapportkolumner](#report-custom-creative-columns) för beskrivningar av alla alternativ.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Kolumnrubrikernas ordning. Du kan dra och släppa en kolumn för att anpassa ordningen.

**[!UICONTROL Format]:** Om en rapport ska genereras i formatet *[!UICONTROL CSV]* (kommaavgränsade värden) eller *[!UICONTROL Tab]* (tabbseparerade värden).

**[!UICONTROL Headers]:** Om *[!UICONTROL Include]* eller *[!UICONTROL Do Not Include]* kolumnrubriker ska användas.

### [!UICONTROL Multi-Touch Conversion Options] avsnitt

**[!UICONTROL Attribution Rule Settings]:** Inställningarna varierar beroende på rapporttyp:

* **\[Attributtyp\]:** (Endast annonsörer med Adobe Advertising-konverteringsspårning) I rapporten, hur du attributerar konverteringsdata i en serie händelser som leder till en konvertering:

   * *[!UICONTROL Unique]:* (Standard) Räknar antalet gånger som ett dimensionsvärde (till exempel en enhet eller placering) fanns på sökvägen till konverteringen.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribuerar krediten för varje konvertering baserat på frekvensen för förekomsten av dimensionsvärdet (till exempel en enhet eller placering) på sökvägen till konverteringen. Om det till exempel fanns totalt 10 visningar före konverteringen, med 8 på CTV och 2 på Mobile, ges 80 % av krediten (0,8) till CTV-skärmar och 0,2 till Mobile.

* **\[Regeltyp\]:** (Endast annonsörer med Adobe Advertising-konverteringsspårning) I rapporten, hur du attributerar konverteringsdata i en serie händelser som leder till en konvertering. Du kan välja mer än en regel om du vill jämföra skillnader mellan reglerna.

  >[!NOTE]
  >
  >Konverteringssökvägar innehåller alla visningar och klickningar i annonsörens intryck eller klickningsfönster som har konfigurerats i [!DNL Advertising Search, Social, & Commerce]. Klick ges företräde framför visningar under konverteringsattribuering. Alla klick i en konverteringsväg får full kredit baserat på attribueringsregeln. Impressions får bara kredit när inga klick spåras i konverteringssökvägen.

   * *[!UICONTROL Last Event]:* Attribut konverteras till det sista klicket eller det sista intrycket i konverteringssökvägen.

   * *[!UICONTROL Weight Last More]:* Attribut konverteras till alla händelser i konverteringssökvägen, men ger den största vikten till den senaste händelsen och har en successivt mindre vikt än föregående händelser.

   * *[!UICONTROL Even Distribution]:* Attribut konverteras lika till alla händelser i konverteringssökvägen.

   * *[!UICONTROL Weight First More]:* Attribut konverteras till alla händelser i konverteringssökvägen, men ger störst vikt till den första händelsen och har en successivt mindre vikt till följande händelser.

   * *[!UICONTROL First Event]:* Attribut konverteras till det första klicket eller intrycket i konverteringssökvägen.

   * *[!UICONTROL U-shaped]:* Attributerar konverteringen till alla händelser i konverteringssökvägen men ger den största vikten till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringssökvägen.

   * *[!UICONTROL Display Only]:* Attribut konverteras till den sista klickningen eller det sista intrycket i konverteringssökvägen i DSP. Detta inkluderar videoklipp och anslutna TV-annonser och utesluter klick på [!DNL Advertising Search, Social, & Commerce] annonser.

   * *[!UICONTROL Social Only]:* Föråldrad

Se även [Hur attribueringsregler beräknas för Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md).

**[!UICONTROL Paths as Columns]:** Vilka typer av konverteringar som ska rapporteras när tidigare händelser inträffar på samma enhet. Du kan inkludera upp till tre typer. För varje vald typ inkluderas en separat kolumn för varje konverteringsmått och den läggs till med det angivna suffixet ([!UICONTROL (tl)], [!UICONTROL (ct)] eller [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inkluderar konverteringar som tilldelats klickningar (CT för klickning) och till visningar (VT för genomgång). Konverteringar som kan härledas till visningar multipliceras med den angivna genomsiktsvikten. Standardbredden är 100 %, vilket innebär att konverteringar som kan tillskrivas visningar räknas som 100 % av värdet på konverteringar som kan tillskrivas klickningar.

* *[!UICONTROL With Clicks (CT)]:* Inkluderar endast konverteringar som har tilldelats klickningar.

* *[!UICONTROL Impressions Only (VT)]:* Inkluderar endast konverteringar som har tilldelats avbildningar eftersom inga klick har spårats i konverteringssökvägen.

### [!UICONTROL Add Report Destinations] avsnitt

**[!UICONTROL Destination Type]:** Var de slutförda rapporterna och felmeddelandena ska levereras. Du kan inte ändra måltypen när du har sparat rapporten.

>[!NOTE]
>
>Du kan alltid hämta slutförda rapporter från vyn [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Att inte leverera några rapporter eller meddelanden.

* *[!UICONTROL S3]:* Om du vill skicka den slutförda rapporten till en eller flera [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) platser, som du måste välja i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Om du vill skicka den slutförda rapporten till en eller flera SFTP-platser, som du måste markera i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Om du vill skicka den slutförda rapporten till en eller flera FTP-platser, som du måste markera i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL] (för närvarande i Beta):* Om du vill skicka den slutförda rapporten till en eller flera FTP SSL-platser, som du måste välja i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Om du vill ange e-postadresser som slutförda rapporter eller meddelanden ska skickas till, om rapporten avbryts på grund av fel.

**[!UICONTROL Email]:** (Endast måltyp för e-post) Ange adressen för varje adress och klicka på **+**.

**[!UICONTROL Destination Name]:** (endast måltyperna S3, FTP, sFTP och FTP SSL) Namnen på de [rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} som den anpassade rapporten skickas till.

* Om du vill ange ett befintligt mål väljer du ett målnamn i listan. Du kan markera flera målnamn separat.

* Så här skapar du ett nytt mål:

   1. Klicka på **Lägg till nytt mål**.

   1. Ange [rapportens målinställningar](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} och klicka på **Spara**.

   1. Klicka på **Uppdatera målnamn.** i rapportinställningarna.

      Det nya målet är nu tillgängligt i listan över befintliga mål och du kan lägga till det i rapporten om du vill.

## Tillgängliga rapportkolumner {#report-custom-creative-columns}

<!-- Need to finish these definitions -->

| Mätningstyp | Undertyp | Kolumnnamn | Beskrivning |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | Den publicerade annonsens dimensioner. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Om den serverade annonsen var en standardbild för upplevelsen. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Anger om annonserna har roterats enligt relativa vikter (*Viktad*) eller algoritmiskt (*Algoritmisk*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | Det ID som [!UICONTROL Creative] tilldelade den kreativa. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | Den kreativa personens namn. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | Typen av kreativ (till exempel [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | Det ID som [!UICONTROL Creative] tilldelade den överordnade kreativiteten. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | Namnet på den överordnade kreativiteten. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | Typen av överordnad kreativ (till exempel [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | . |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | Klickningstypen. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | Webbläsaren som annonsen visades i (till exempel [!UICONTROL Chrome] eller [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | Det operativsystem som annonsen visades på (till exempel [!UICONTROL Windows]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | Den typ av enhet som annonsen visades på (till exempel [!UICONTROL Desktop]). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Ad ID] | Annonsens ID. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Buy ID] | Köp-ID för annonsplaceringen. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Creative ID] | Den kreativa personens ID. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP ID] | ID:t för den DSP som annonserna kördes på. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | Namnet på den DSP som annonserna kördes på. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | ID för den placering som annonserna kördes för. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | Namnet på den placering som annonserna kördes för. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | ID:t för den webbplats där annonserna kördes. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | Namnet på den webbplats där annonserna kördes. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | Det ID som [!UICONTROL Creative] tilldelade annonsupplevelsetaggen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | Annonsörens namn. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | Datum och tid för händelsen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | Det ID som [!UICONTROL Creative] tilldelade upplevelsen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | Namnet på upplevelsen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | Målet. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | Den stad som de rapporterade uppgifterna härrör från. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | Landskoden för det land som de rapporterade uppgifterna härrör från. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | Det utsedda marknadsområde (DMA) som de rapporterade uppgifterna tillskrivs. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | Statuskoden för det tillstånd som de rapporterade uppgifterna tilldelas. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | Postnumret som de rapporterade uppgifterna ska tilldelas till. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Dynamiska annonser) Målproduktkategori-ID. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Dynamiska annonser) Namnet på målproduktkategorin. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Dynamiska annonser) Det första kreativa attributet. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Dynamiska annonser) Det andra kreativa attributet. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Dynamiska annonser) Det tredje kreativa attributet. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Dynamiska annonser) Det fjärde kreativa attributet. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Dynamiska annonser) Det femte kreativa attributet. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Dynamiska annonser) Målprodukt-ID. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Dynamiska annonser) Målproduktens namn. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | ID:t för det målgruppssegment som de rapporterade uppgifterna ska tilldelas till. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | Segmentets-ID för ett målgruppssegment som de rapporterade uppgifterna tilldelas till. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | Namnet på ett målgruppssegment som de rapporterade uppgifterna är kopplade till. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Attributen för ett målgruppssegment som de rapporterade uppgifterna tilldelas till. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | Summan av alla klick på en annons. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | Klickfrekvensen, som är procentandelen klickningar dividerat med annonsvisningar. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | Den procentandel av visningar som resulterade i användarengagemang. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Antalet interaktioner för en serverad annons. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Totalt antal annonsvisningar. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | Summan av alla klick på annonser för en produkt. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | Summan av alla konverteringar på annonser för en produkt. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | Procentandel annonser för en produkt som resulterade i konverteringar. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | Klickfrekvensen för annonser för en produkt, vilket är procentandelen klickningar dividerat med annonsvisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | Det totala antalet visningar för en produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | Den totala intäkten för serverade annonser för en produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | De totala intäkterna för serverade annonser. |
| [!UICONTROL Conversion Metrics] | [Grupperad av annonsören i rapportinställningarna] | [Annonsspecifik konvertering] | Summan för en angiven annonsörspecifik konverteringsmetod eller Adobe Analytics-händelse. |
| [!UICONTROL Custom Goals] | [Grupperad av annonsören i rapportinställningarna] | [Advertiser-specifikt anpassat mål] | (Annonsörer med Advertising DSP) Den viktade summan av alla konverteringar som ingår i det angivna [anpassade Advertising DSP-målet](/help/dsp/optimization/custom-goal.md). |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Prestandarapporter på erfarenhetsnivå](/help/creative/experiences/experience-performance-details.md)
>* [Om anpassade DSP-rapporter](/help/dsp/reports/report-about.md){target="_blank"}
>* [Om [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
