---
title: Anpassade rapportinställningar
description: Se beskrivningar av anpassade rapportinställningar.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 65d554ef71e36b52a47fc24552d5db9b56072095
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 0%

---

# Anpassade rapportinställningar

**[!UICONTROL Name]:** Rapportnamnet. Maximala längden är 180 tecken.

**[!UICONTROL Report Type]:** Typ av rapport: *[!UICONTROL Custom]* (som innehåller de mest tillgängliga alternativen), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, **, *[!UICONTROL Path Length]* eller *[!UICONTROL Time to Conversion]*.

## [!UICONTROL Report Range] avsnitt

Det här avsnittet avgör vilka data som tas med i rapporten. Information om hur du ställer in datum för rapportschemat finns i avsnittet [!UICONTROL Report run schedule].

**[!UICONTROL Timezone]:** Tidszonen för rapportering.

**[!UICONTROL Observe Daylight Savings Time]:** anser att sommartid kan användas under de rapporterade tiderna.

**Intervall:** Datumintervallet som data ska genereras för. Antalet tillgängliga dagar varierar beroende på rapport och valda dimensioner. Välj ett alternativ:

* **[!UICONTROL Previous Calendar Week]:** Inkluderar data för föregående kalendervecka.

* **[!UICONTROL Previous Calendar Month]:** Inkluderar data för föregående kalendermånad.

* **[!UICONTROL Custom Range]:** Inkluderar data mellan specifika start- och slutdatum. Om du vill rapportera data genom föregående dag väljer du **[!UICONTROL Present]**.

## [!UICONTROL Report Run schedule] avsnitt

I det här avsnittet anges de datum då rapporten körs. Information om hur du ställer in datum för vilka rapportdata ska inkluderas finns i avsnittet [!UICONTROL Report range].

**\[Schema\]:** När rapporten ska genereras:

* *[!UICONTROL Immediately]*: Lägger omedelbart till rapporten i rapportkön.

  >[!NOTE]
  >
  >Du kan också [köra en anpassad rapport när som helst](report-run-now.md) från vyn [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Kör rapporten på ett angivet datum för slutförande senast 09:00 i kontots tidszon.

* *[!UICONTROL Recurring]:* Kör rapporten enligt ett schema under en angiven tidsperiod.

   * **\[Schedule\]:** Hur ofta rapporten ska köras:

      * *Dagligen* om du vill köra rapporten var N:e dag. Om du till exempel vill köra rapporten varannan vecka (14 dagar) markerar du det här alternativet och anger **14**.

      * *Veckovis* om du vill köra rapporten på angivna veckodagar. Om du till exempel vill köra rapporten varje måndag och fredag markerar du det här alternativet och markerar kryssrutorna intill **måndag** och **fredag**.

      * *Månadsvis* om du vill köra rapporten på en viss numerisk dag i månaden, från 1 till 30. Kör till exempel rapporten den första dagen i varje månad, markera det här alternativet och ange **1**.

   * **Från**: Det första datum då rapporten kan köras. Beroende på angivet schema kan den första rapportinstansen inträffa efter detta datum.

   * **Till**: Rapportens förfallodatum, som kan vara upp till fyra kalendermånader bort. Innan en rapport förfaller får alla angivna e-postmål en e-postavisering sju dagar och en dag före förfallodatumet. Ändra det här datumet om du vill behålla rapporten längre.

## [!UICONTROL Apply Filters] avsnitt

**[!UICONTROL Filter by]:** (Valfritt) Ytterligare dimensioner som data kan filtreras med, oavsett om dimensionerna inkluderas som kolumner i rapporten eller inte. De tillgängliga filtren varierar beroende på rapporttyp och kan omfatta: *[!UICONTROL Account]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, *[!UICONTROL Deal]*, *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* och *[!UICONTROL Video Duration]*.

<!-- Add when available:
*[!UICONTROL Deal ID]*, *[!UICONTROL Deal List]*, 
-->

Så här använder du ett eller flera filter:

* Välj en dimension, markera operatorn (*är lika med* eller *är inte lika med*) och välj sedan önskat värde. Om du till exempel vill returnera data för enbart förhandsannonser anger du [!UICONTROL Ad Type equals Preroll].
* (Valfritt) Lägg till ytterligare villkor till filtret.
* (Valfritt) Lägg till ytterligare filter, där vart och ett har ett eller flera villkor.

\* *[!UICONTROL Account]* är bara tillgängligt för följande rapporttyper när din organisation har konfigurerats för [korskontorapportering](report-about.md#cross-account-reporting): [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] och [!UICONTROL Conversion]. Kontakta Adobe Account Team om du vill ha mer information om kontorapportering.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (Endast rapporter om sökväg till konvertering, sökvägslängd och tid till konvertering) Inkluderar data för klickningar på sökannonser från angivna Advertising Search-, Social- och Commerce-kampanjer. När du väljer det här alternativet:

1. Välj kontot Sök, Socialt och Commerce med hjälp av filtret **Filtrera efter[!UICONTROL SSC Account]**.

1. Välj kampanjer med filtret **Filtrera efter[!UICONTROL SSC Campaign]**.

   Om du vill välja flera kampanjer klickar du på **[!UICONTROL Add Criteria]** för den andra och efterföljande kampanjer.

## [!UICONTROL Build Your Report] avsnitt

**[!UICONTROL Select To Add As Report Headers]:** Datakolumner, eller rubriker, som ska inkluderas i rapporten. Om du vill lägga till en kolumn expanderar du kategorin och markerar kryssrutan bredvid kolumnnamnet. De tillgängliga kolumnerna varierar beroende på rapport, och alla otillgängliga värden är inaktiverade. De tillgängliga datakategorierna kan omfatta:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Rapporterna [!UICONTROL Household Reach & Frequency] och [!UICONTROL Path to Conversion] kan bara innehålla en dimension.
  > Rapporterna [!UICONTROL Path Length] och [!UICONTROL Time to Conversion] innehåller inga dimensioner.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Rapporten [!UICONTROL Household Reach & Frequency] kan innehålla antingen överlappningsmått eller icke-överlappande mått, men inte båda.

* [!UICONTROL Conversion Metrics] (sorterad av annonsören)

* [!UICONTROL Custom Goals] (sorterad av annonsören)

Se [Tillgängliga rapportkolumner](report-columns.md) för beskrivningar av alla alternativ.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Kolumnrubrikernas ordning. Du kan dra och släppa en kolumn för att anpassa ordningen.

**[!UICONTROL Format]:** Om en rapport ska genereras i formatet *[!UICONTROL CSV]* (kommaavgränsade värden) eller *[!UICONTROL Tab]* (tabbseparerade värden).

**[!UICONTROL Headers]:** Om *[!UICONTROL Include]* eller *[!UICONTROL Do Not Include]* kolumnrubriker ska användas.

## [!UICONTROL Multi-Touch Conversion Options] avsnitt

**[!UICONTROL Attribution Rule Settings]:** Inställningarna varierar beroende på rapporttyp:

* **\[Attributtyp\]:** ([!UICONTROL Household Conversion] rapporter med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner) I rapporten, hur du attributerar konverteringsdata i en serie händelser som leder till en konvertering:

   * *[!UICONTROL Unique]:* (Standard) Räknar antalet gånger som ett dimensionsvärde (till exempel en enhet eller placering) fanns på sökvägen till konverteringen.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribuerar krediten för varje konvertering baserat på frekvensen för förekomsten av dimensionsvärdet (till exempel en enhet eller placering) på sökvägen till konverteringen. Om det till exempel fanns totalt 10 visningar före konverteringen, med 8 på CTV och 2 på Mobile, ges 80 % av krediten (0,8) till CTV-skärmar och 0,2 till Mobile.

* **\[Regeltyp\]:** (Alla [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] och [!UICONTROL Site] rapporterar med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner; annonsörer med endast Adobe Advertising-konverteringsspårning) I rapporten, hur du attributerar konverteringsdata i en serie händelser som leder till en konvertering. Du kan välja mer än en regel om du vill jämföra skillnader mellan reglerna.

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

* **Uppslag:** ([!UICONTROL Household Conversion] rapporterar med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner och [!UICONTROL Path to Conversion], [!UICONTROL Path Length] eller [!UICONTROL Time to Conversion] enbart med [!UICONTROL Conversion Metrics] kolumner; endast annonsörer med Adobe Advertising-konverteringsspårning) I rapporten är det högsta antalet dagar efter en intryckshändelse eller en klickhändelse (för [!UICONTROL Path to Conversion], [!UICONTROL Path Length] eller [!UICONTROL Time to Conversion] rapporter) i vilket en konverteringshändelse kan tilldelas den. Standardvärdet är *[!UICONTROL 30 days]* och det högsta antalet är 92 dagar.

  >[!TIP]
  >
  >Om du använder [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) ska du använda samma uppslagsfönster som du använder i [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (Alla [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] och [!UICONTROL Site] rapporterar med [!UICONTROL Conversion Metrics]- eller [!UICONTROL Custom Goals]-kolumner) Vilka typer av konverteringar som ska rapporteras när tidigare händelser inträffar på samma enhet. Du kan inkludera upp till tre typer. För varje vald typ inkluderas en separat kolumn för varje konverteringsmått och den läggs till med det angivna suffixet ([!UICONTROL (tl)], [!UICONTROL (ct)] eller [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inkluderar konverteringar som tilldelats klickningar (CT för klickning) och till visningar (VT för genomgång). Konverteringar som kan härledas till visningar multipliceras med den angivna genomsiktsvikten. Standardbredden är 100 %, vilket innebär att konverteringar som kan tillskrivas visningar räknas som 100 % av värdet på konverteringar som kan tillskrivas klickningar.

* *[!UICONTROL With Clicks (CT)]:* Inkluderar endast konverteringar som har tilldelats klickningar.

* *[!UICONTROL Impressions Only (VT)]:* Inkluderar endast konverteringar som har tilldelats avbildningar eftersom inga klick har spårats i konverteringssökvägen.

**[!UICONTROL Conversion Reporting Based On]:** Så här rapporterar du konverteringsdata:

* *[!UICONTROL Conversion Timestamp]:* (Standard) Konverteringar är associerade med konverteringsdatumet.

* *[!UICONTROL Event Timestamp]:* Konverteringar rapporteras baserat på datumet för det intryck eller klick som orsakade konverteringen, enligt angivet [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] avsnitt

**[!UICONTROL Destination Type]:** Var de slutförda rapporterna och felmeddelandena ska levereras. Du kan inte ändra måltypen när du har sparat rapporten.

>[!NOTE]
>
>Du kan alltid hämta slutförda rapporter från vyn [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Att inte leverera några rapporter eller meddelanden.

* *[!UICONTROL S3]:* Om du vill skicka den slutförda rapporten till en eller flera [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) platser, som du måste välja i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Om du vill skicka den slutförda rapporten till en eller flera SFTP-platser, som du måste markera i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Om du vill skicka den slutförda rapporten till en eller flera FTP-platser, som du måste markera i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL](för närvarande i Beta):* Om du vill skicka den slutförda rapporten till en eller flera FTP SSL-platser, som du måste välja i fältet **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Om du vill ange e-postadresser som slutförda rapporter eller meddelanden ska skickas till, om rapporten avbryts på grund av fel.

**[!UICONTROL Email]:** (Endast måltyp för e-post) Ange adressen för varje adress och klicka på **+**.

**[!UICONTROL Destination Name]:** (endast måltyperna S3, FTP, sFTP och FTP SSL) Namnen på rapportdestinationerna som den anpassade rapporten skickas till.

* Om du vill ange ett befintligt mål väljer du ett målnamn i listan. Du kan markera flera målnamn separat.

* Så här skapar du ett nytt mål:

   1. Klicka på **Lägg till nytt mål**.

   1. Ange [rapportens målinställningar](/help/dsp/reports/report-destinations/report-destination-settings.md) och klicka på **Spara**.

   1. Klicka på **Uppdatera målnamn.** i rapportinställningarna.

      Det nya målet är nu tillgängligt i listan över befintliga mål och du kan lägga till det i rapporten om du vill.

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Duplicera en anpassad rapport](/help/dsp/reports/report-copy.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Hämta en anpassad rapport](/help/dsp/reports/report-download.md)
>* [Kör en anpassad rapport](/help/dsp/reports/report-run-now.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Om rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
