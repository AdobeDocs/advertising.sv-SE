---
title: Hantera anpassade rapporter
description: Lär dig hur du genererar och hanterar korsgränssnittet [!UICONTROL Custom Creative Report].
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Du kan skapa, duplicera, redigera, köra, hämta och ta bort anpassade rapporter.

## Skapa en anpassad rapport {#report-create}

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create]** i det övre högra hörnet.

1. Ange [rapportinställningarna](#report-settings).

1. Klicka på **[!UICONTROL Create Custom Report]**.

## Duplicera en anpassad rapport

Duplicera en anpassad rapport om du vill skapa en ny rapport med liknande inställningar.

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka **[!UICONTROL ...]** > **[!UICONTROL Copy]** bredvid rapportnamnet.

1. (Valfritt) Redigera [rapportinställningarna](#report-settings.md) efter behov.

   Rapportnamnet är som standard &quot;\&lt;*befintligt rapportnamn*\> \#2&quot; (eller nästa nummer i sekvensen).

## Redigera en anpassad rapport {#report-edit}

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka **[!UICONTROL ...]** > **[!UICONTROL Edit]** bredvid rapportnamnet.

1. Redigera [rapportinställningarna](#report-settings.md).

1. Klicka på **[!UICONTROL Edit Custom Report]**.

## Köra en anpassad rapport &lbrace;report-run-now&rbrace;

Du kan köra alla rapporter som inte har gått ut och som inte körs just nu.

>[!NOTE]
>
>Du kan också köra en anpassad rapport när du [skapar](#report-create) eller [redigerar](#report-edit) den.

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka **[!UICONTROL ...]** > **[!UICONTROL Run Now]** bredvid rapportnamnet.

   När rapporten är klar skickas den till de mål som anges i rapportinställningarna.

## Hämta en anpassad rapport

Du kan hämta alla slutförda rapportinstanser från de senaste fyra månaderna, som har statusen [!UICONTROL Ready to Download] eller [!UICONTROL Completed].

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Gör följande i kolumnen [!UICONTROL Download Report] för rapportraden:

   * Klicka på **[!UICONTROL Download]** om du vill hämta den senaste instansen av rapporten.

   * (Rapporter med flera instanser) Klicka på ![nedpilen](/help/dsp/assets/chevron-down.png "nedpilen") intill [!UICONTROL Download] och klicka sedan på slutdatumet för rapporten som du vill hämta. Hämtningsbara rapportinstanser anges med en hämtningsikon (![hämtningsikon](/help/dsp/assets/indicator-downloadable.png "hämtningsikon")).

     När det finns många instanser klickar du **[!UICONTROL Load More]** längst ned i listan om det behövs.

     När en rapport körs flera gånger på samma dag visas rapportinstanserna för den dagen i kronologisk ordning med den senaste instansen överst.

     Misslyckade rapportjobb indikeras med en felikon (![felindikator](/help/dsp/assets/indicator-critical.png "felindikator")) och kan inte hämtas. Håll markören över felikonen om du vill se en beskrivning av felet.

## Ta bort en anpassad rapport

1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** på huvudmenyn.

1. Klicka **[!UICONTROL ...]** > **[!UICONTROL Delete]** bredvid rapportnamnet.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

## Rapportinställningar {#report-settings}

**[!UICONTROL Name]:** Rapportnamnet. Maximala längden är 180 tecken.

**[!UICONTROL Report Type]:** Typ av rapport.

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
  >Du kan också [köra en anpassad rapport när som helst](#report-run-now) från vyn [!UICONTROL Reports].

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

**[!UICONTROL Select To Add As Report Headers]:** Datakolumner, eller rubriker, som ska inkluderas i rapporten. Om du vill lägga till en kolumn expanderar du kategorin och markerar kryssrutan bredvid kolumnnamnet. De tillgängliga kolumnerna varierar beroende på rapport, och alla otillgängliga mått är inaktiverade.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Kolumnrubrikernas ordning. Du kan dra och släppa en kolumn för att anpassa ordningen.

**[!UICONTROL Format]:** Om en rapport ska genereras i formatet *[!UICONTROL CSV]* (kommaavgränsade värden) eller *[!UICONTROL Tab]* (tabbseparerade värden).

**[!UICONTROL Headers]:** Om *[!UICONTROL Include]* eller *[!UICONTROL Do Not Include]* kolumnrubriker ska användas.

### [!UICONTROL Multi-Touch Conversion Options] avsnitt

**[!UICONTROL Attribution Rule Settings]:** Inställningarna varierar beroende på rapporttyp:

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


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Prestandarapporter på erfarenhetsnivå](/help/creative/experiences/experience-performance-details.md)
>* [Om anpassade DSP-rapporter](/help/dsp/reports/report-about.md){target="_blank"}
>* [Om [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
