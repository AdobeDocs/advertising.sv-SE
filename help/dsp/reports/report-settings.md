---
title: Anpassade rapportinställningar
description: Se beskrivningar av anpassade rapportinställningar.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 54e60a47c54eaac687fd0b385a94b25818b66b71
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Anpassade rapportinställningar

**[!UICONTROL Name]** Rapportnamnet. Maximala längden är 180 tecken.

**[!UICONTROL Report Type]** Typ av rapport: *[!UICONTROL Custom]* (som innehåller de mest tillgängliga alternativen), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, eller *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] Avsnitt

**[!UICONTROL Timezone]:** Tidszonen för rapportering.

**[!UICONTROL Observe Daylight Savings Time]:** Beaktar sommartid i de rapporterade tiderna.

**\[Datumintervall\]:** Datumintervallet som data ska genereras för. Antalet tillgängliga dagar varierar beroende på rapport och valda dimensioner. Välj ett alternativ:

* **[!UICONTROL Previous N days]:** Inkluderar data för ett visst antal dagar före idag.

* **[!UICONTROL Custom]:** Inkluderar data mellan specifika start- och slutdatum. Om du vill rapportera data till föregående dag väljer du **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Inkluderar data för föregående kalendermånad.

**[!UICONTROL Add Filters]:** (Valfritt) Ytterligare dimensioner som data kan filtreras med, oavsett om dimensionerna inkluderas som kolumner i rapporten eller inte. De tillgängliga filtren varierar beroende på rapporttyp och kan omfatta: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* och *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* är bara tillgängligt för följande rapporttyper när din organisation har konfigurerats för [kontorapportering](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]och [!UICONTROL Conversion]. Kontakta kontoteamet på Adobe för mer information om kontorapportering.

Så här använder du ett eller flera filter:

* Välj en dimension, välj operatorn (*är lika med* eller *inte lika med*) och sedan välja önskat värde. Om du till exempel vill returnera data för enbart inledningsannonser anger du &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Valfritt) Lägg till ytterligare villkor till filtret.
* (Valfritt) Lägg till ytterligare filter, där vart och ett har ett eller flera villkor.

## [!UICONTROL Build Your Report] Avsnitt

**[!UICONTROL Select To Add As Report Headers]:**  De datakolumner, eller rubriker, som ska inkluderas i rapporten. Om du vill lägga till en kolumn expanderar du kategorin och markerar kryssrutan bredvid kolumnnamnet. De tillgängliga kolumnerna varierar beroende på rapport, och alla otillgängliga värden är inaktiverade. De tillgängliga datakategorierna är:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > The [!UICONTROL Household Reach & Frequency] -rapporten kan bara innehålla en dimension.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >The [!UICONTROL Household Reach & Frequency] kan innehålla antingen överlappningsvärden eller icke-överlappande värden, men inte båda.

* [!UICONTROL Conversion Metrics] (sorterat efter annonsörer)

* [!UICONTROL Custom Goals] (sorterat efter annonsörer)

Se &quot;[Tillgängliga rapportkolumner](report-columns.md)&quot; för beskrivningar av alla alternativ.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordningen på kolumnrubrikerna. Du kan dra och släppa en kolumn för att anpassa ordningen.

**[!UICONTROL Format]:** Om en rapport ska genereras i *[!UICONTROL CSV]* (kommaavgränsade värden) eller *[!UICONTROL Tab]* (tabbseparerade värden).

**[!UICONTROL Headers]:** Om *[!UICONTROL Include]* eller *[!UICONTROL Do Not Include]* kolumnrubriker.

## [!UICONTROL Multi-Touch Conversion Options] Avsnitt

**[!UICONTROL Attribution Rule Settings]:** Inställningarna varierar beroende på rapporttyp:

* **\[Attribution Type\]:** ([!UICONTROL Household Conversion] rapporter med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner, annonsörer med endast spårning av konvertering i Adobe Advertising) I rapporten, hur man attribuerar konverteringsdata i en serie händelser som leder till en konvertering:

   * *[!UICONTROL Unique]:* (Standard) Räknar det antal gånger som ett dimensionsvärde (till exempel en enhet eller placering) befann sig på sökvägen till konverteringen.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  Fördelar krediten för varje konvertering baserat på frekvensen för förekomsten av dimensionsvärdet (till exempel en enhet eller placering) på sökvägen till konverteringen. Om det till exempel fanns totalt 10 visningar före konverteringen, med 8 på CTV och 2 på Mobile, ges 80 % av krediten (0,8) till CTV-skärmar och 0,2 till Mobile.

* **\[Regeltyp\]:** (Alla [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]och [!UICONTROL Site] rapporter med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner, annonsörer med enbart konverteringsspårning för Adobe Advertising) I rapporten, hur du attributerar konverteringsdata i en serie händelser som leder till en konvertering. Du kan välja mer än en regel om du vill jämföra skillnader mellan reglerna.

  >[!NOTE]
  >
  >Konverteringssökvägarna innehåller alla visningar och klickningar i annonsörens intryckt eller klickbara fönster som är konfigurerade i [!DNL Advertising Search, Social, & Commerce]. Klick ges företräde framför visningar under konverteringsattribuering. Alla klick i en konverteringsväg får full kredit baserat på attribueringsregeln. Impressions får bara kredit när inga klick spåras i konverteringssökvägen.

   * *[!UICONTROL Last Event]:* Attribut konverteras till det sista klicket eller det sista intrycket i konverteringssökvägen.

   * *[!UICONTROL Weight Last More]:* Attribut konverteras till alla händelser i konverteringsbanan, men ger störst vikt till den senaste händelsen och har en successivt mindre vikt än föregående händelser.

   * *[!UICONTROL Even Distribution]:* Attribut konverteras lika till varje händelse i konverteringssökvägen.

   * *[!UICONTROL Weight First More]:* Attribut konverteras till alla händelser i konverteringsbanan, men ger den största vikten till den första händelsen och minskar successivt till följande händelser.

   * *[!UICONTROL First Event]:* Attribut konverteras till det första klicket eller intrycket i konverteringssökvägen.

   * *[!UICONTROL U-shaped]:* Attributerar konverteringen till alla händelser i konverteringsbanan, men ger störst vikt till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringsbanan.

   * *[!UICONTROL Display Only]:*  Attribut konverteras till den sista DSP klickningen eller intrycket i konverteringssökvägen. Detta inkluderar videoklipp och anslutna TV-annonser och utesluter klickningar på [!DNL Advertising Search, Social, & Commerce] annonser.

   * *[!UICONTROL Social Only]:* Föråldrad

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Lookback:** ([!UICONTROL Household Conversion] rapporter med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner, annonsörer med endast spårning av konvertering mellan Adobe Advertising) I rapporten, det maximala antal dagar efter en intryckshändelse som en konverteringshändelse kan tilldelas till den. Standardvärdet är *[!UICONTROL 30 days]*, och det högsta antalet är 92 dagar.

**[!UICONTROL Paths as Columns]:**  (Alla [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]och [!UICONTROL Site] rapporter med [!UICONTROL Conversion Metrics] eller [!UICONTROL Custom Goals] kolumner) Vilka typer av konverteringar som ska rapporteras när tidigare händelser inträffar på samma enhet. Du kan inkludera upp till tre typer. För varje vald typ inkluderas en separat kolumn för varje konverteringsmått och den läggs till med det angivna suffixet ([!UICONTROL (tl)], [!UICONTROL (ct)], eller [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inkluderar konverteringar som härrör från klick (CT för klickning) och tryck (VT för genomskinlighet). Konverteringar som kan härledas till visningar multipliceras med den angivna genomsiktsvikten. Standardbredden är 100 %, vilket innebär att konverteringar som kan tillskrivas visningar räknas som 100 % av värdet på konverteringar som kan tillskrivas klickningar.

* *[!UICONTROL With Clicks (CT)]:* Inkluderar endast konverteringar som kan härledas till klickningar.

* *[!UICONTROL Impressions Only (VT)]:* Inkluderar endast konverteringar som tillskrivits exponeringar eftersom inga klick spårades i konverteringsbanan.

**[!UICONTROL Conversion Reporting Based On]:**  Rapportera konverteringsdata:

* *[!UICONTROL Conversion Timestamp]:* (Standardvärdet) Konverteringar associeras med konverteringsdatumet.

* *[!UICONTROL Event Timestamp]:* Konverteringar rapporteras baserat på datumet för det intryck eller klick som orsakade konverteringen, enligt det angivna [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Avsnitt

**[!UICONTROL Destination Type]:** Välj någon av följande måltyper:

* *[!UICONTROL S3]:* Skicka den färdiga rapporten till en eller flera [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) -platser, som du anger i **[!UICONTROL Destination Name]** fält.
* *[!UICONTROL sFTP]:* Skicka den färdiga rapporten till en eller flera SFTP-platser, som du anger i dialogrutan **[!UICONTROL Destination Name]** fält.
* *[!UICONTROL FTP]:* Skicka den färdiga rapporten till en eller flera FTP-platser, som du anger i dialogrutan **[!UICONTROL Destination Name]** fält.
* *[!UICONTROL FTP SSL](För närvarande i betaversion):* Skicka den färdiga rapporten till en eller flera FTP SSL-platser, som du anger i dialogrutan **[!UICONTROL Destination Name]** fält.
* *[!UICONTROL Email]:* Ange e-postadresser dit slutförda rapporter eller meddelanden ska skickas om rapporten avbryts på grund av fel. Om du vill ange flera adresser avgränsar du dem med kommatecken eller mellanslag.

>[!NOTE]
>
> Du kan inte ändra måltypen när du har sparat rapporten.

**[!UICONTROL Destination Name]:** (Endast måltyperna S3, FTP, sFTP och FTP SSL) Namnen på rapportdestinationerna som den anpassade rapporten ska skickas till.

* Om du vill ange ett befintligt mål väljer du ett målnamn i listan. Du kan markera flera målnamn separat.

* Så här skapar du ett nytt mål:

   1. Klicka **Lägg till nytt mål**.

   1. Ange [inställningar för rapportmål](/help/dsp/reports/report-destinations/report-destination-settings.md)och klicka **Spara**.

   1. Tillbaka i rapportinställningarna, klicka på **Uppdatera målnamn.**

      Det nya målet är nu tillgängligt i listan över befintliga mål och du kan lägga till det i rapporten om du vill.

**[!UICONTROL Frequency]:** (För varje [!UICONTROL Destination Name] Hur ofta rapporten ska skickas till målet: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, eller *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Avsnitt

**[!UICONTROL Send & Save]:** När rapporten ska skickas: *[!UICONTROL On Schedule]* eller *[!UICONTROL Run Now]*. Schemalagda rapporter levereras senast 09:00 i kontots tidszon.

>[!NOTE]
>
>Du kan [köra en anpassad rapport när som helst](report-run-now.md) från [!UICONTROL Reports] vy.

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Duplicera en anpassad rapport](/help/dsp/reports/report-copy.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Kör en anpassad rapport](/help/dsp/reports/report-run-now.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Om rapportdestinationer](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
