---
title: Om anpassade rapporter
description: Lär dig mer om alternativ för att skapa anpassade rapporter manuellt eller med förkonfigurerade rapportmallar.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Om anpassade rapporter

Med anpassade rapporter kan ni anpassa innehållet i och leveransen av rapportdata med kampanjdimensionerna (som annonsören, placeringen, webbplatser eller geos) och de mätvärden som är viktiga för er. Du kan antingen:

* Konfigurera kampanjresultatrapporter helt och hållet på detaljnivå.

* Välj bland förkonfigurerade rapportmallar och anpassa dem ytterligare.

Du kan generera rapporter en gång eller schemalägga att de ska genereras varje dag, vecka eller månad klockan 03:00 i den angivna tidszonen enligt angivna villkor (t.ex. var 15:e dag eller den 1:e varje månad). När en rapport har skapats kan du hämta den från [!UICONTROL Reports] > [!UICONTROL Custom Reports] eller från länkade [rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md) av följande typer:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Du kan även visa on demand-data på alla nivåer i en kampanj (kampanj, paket, placering eller annons) [i den relevanta kampanjhanteringsvyn](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tillgängliga rapporttyper

* **[!UICONTROL Custom]:** Den här rapporten är en tom mall som du kan använda för att skapa en egen anpassad rapport med de flesta mått och mått. [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]- och [!UICONTROL Site]-rapporter är varianter av den här mallen med förvalda kolumner och dimensioner för respektive användningsfall.

* Förkonfigurerade rapportmallar

   * **[!UICONTROL Billing]:** Använd den här rapporten för att förstå viktiga faktureringsmått, som utgiftsmått för mediefakturering per kampanj. Data är inte tillgängliga för placeringar som har universella ID som mål.

     >[!NOTE]
     >
     >Den här rapporten innehåller data om faktureringssegmentet. Om en användare eller enhet får ett intryck som tillhör flera segment, krediteras endast ett fakturerbart segment med intrycket.

   * **[!UICONTROL Conversion]:** Använd den här rapporten för att förstå hur era kampanjer fungerar baserat på konverteringsstatistik som hämtats med Adobe Advertising-konverteringsspårning. Den här rapporten innehåller multitouch-attribuering.

   * **[!UICONTROL Device]:** Använd den här förifyllda mallen för att visa nyckelmått efter enhetsrelaterade dimensioner.

   * **[!UICONTROL Frequency (by Impression)]:** Använd den här rapporten för att förstå hur visningar som visas för unika tittare är fördelade (till exempel hur många unika tittare som såg ett intryck, två visningar, tre visningar och så vidare). Data är tillgängliga via placering eller kampanj.

     >[!NOTE]
     >
     >* Data är tillgängliga efter den 1 mars 2019.
     >* Frekvensen beräknas utifrån ett urval data.
     >* För en del lager skickas ingen enhets-ID, vilket förhindrar frekvensspårning. Den här rapporten innehåller bara avtryck som det fanns en enhetsidentifierare för.

   * **[!UICONTROL Frequency (by App/Site)]:** Använd den här rapporten för att förstå hur många unika användare som har nåtts per app eller per webbplats. Du kan också se hur många unika användare som har nåtts via en viss app eller webbplats (&quot;distinkta unika användare&quot;).

     >[!NOTE]
     >
     >* Data är tillgängliga efter 15 november 2018.
     >* För vissa privata lager skickas ingen enhets-ID, vilket förhindrar frekvensspårning.

   * **[!UICONTROL Geo]**: Använd den här förifyllda mallen för att se nyckelvärden efter geografiska dimensioner.

   * **[!UICONTROL Margin]:** Använd den här rapporten om du vill se nyckeltal som marginal, vinst och andra utgiftsmått per kampanj eller placering. Data är inte tillgängliga för placeringar som har universella ID som mål.

   * **[!UICONTROL Segment]:** Använd den här förifyllda mallen för att visa nyckeltal efter segment.

     >[!NOTE]
     >
     >* Den här rapporten ska visa hur olika målsegment fungerar. Den använder data om segmentmedlemskap. När ett intryck skickas till en person eller enhet som tillhör två eller flera målsegment innehåller rapporten en rad för varje segment. Av den anledningen kanske inte summorna i den här rapporten matchar den faktiska leveransen.
     >* Konverteringsstatistik och anpassade måldata för segment är tillgängliga efter 2 augusti 2019. Alla andra data för segment är tillgängliga från och med den 1 juni 2018.

   * **[!UICONTROL Site]:** Inkluderar som standard standardvärden, totala medienettoutgifter och totala fakturerbara nettoutgifter per webbplats.

   * **[!UICONTROL Household Reach & Frequency]:** Använd den här rapporten om du vill visa visningar, räckvidd och frekvens för en enda dimension i alla annonsformat på en hushållsnivå baserat på IP-adress, i stället för på enhets-/cookienivå. Använd insikterna för att optimera din mediemix, förbättra prestanda och identifiera möjligheter för ökad räckvidd. Mer information finns i [Vanliga frågor om hushållsrapporter](/help/dsp/reports/faq-household-report.md). Data är inte tillgängliga för placeringar som har universella ID som mål.

   * **[!UICONTROL Household Conversions]:** Använd den här rapporten om du vill visa genomsiktskonverteringar på hushållsnivå baserat på IP-adress, i stället för på enhets-/cookienivå. Använd insikterna för att mäta och optimera kampanjresultatet. Mer information finns i [Vanliga frågor om hushållsrapporter](/help/dsp/reports/faq-household-report.md). Data är inte tillgängliga för placeringar som har universella ID som mål.

## Kontorapportering {#cross-account-reporting}

Alla organisationer som har flera DSP-konton kan välja att aktivera kontoöverskridande data i anpassade rapporter, beroende på organisationens behov. Du kan till exempel ge konto A åtkomst till data för konto B och ge konto B åtkomst till data för konto C (men inte konto A). Kontakta ditt Adobe-kontoteam om du vill aktivera och konfigurera den här funktionen.

När funktionen har aktiverats för din organisation kan du [filtrera](report-settings.md) någon av följande rapporttyper efter konto: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] och [!UICONTROL Conversion].

Kontoinställningarna på [!UICONTROL Settings] > [!UICONTROL Account] anger a) de andra konton vars data är tillgängliga för ditt konto och b) de andra konton som kan komma åt dina kontodata.

## Vyn [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] visar dina befintliga rapporter, inklusive rapporter som har genererats, rapporter som är schemalagda för framtida generering och rapporter som har misslyckats. Kolumnen [!UICONTROL Report Run] visar datum då rapporten startades med början den 22 augusti 2024. Som standard visas alla oarkiverade rapporter som skapas av användaren, med den senaste överst. Du kan filtrera listan ytterligare efter status, oavsett om rapporten är återkommande eller en gång, rapporttyp, måltyp och rapportskapare.

Du kan skapa nya anpassade rapporter, redigera befintliga rapporter eller duplicera dem för att skapa nya rapporter, köra rapporter direkt, ladda ned alla rapportinstanser från de senaste fyra månaderna och ta bort rapporter.

## Rapportstatus {#custom-report-status}

* **[!UICONTROL Yet to start]:** Rapporten har aldrig körts.

* **[!UICONTROL Report generating]:** Rapporten skapas.

* **[!UICONTROL Ready to download]:** (Endast återkommande rapporter) En eller flera instanser av rapporten är tillgängliga för hämtning och fler rapportinstanser är schemalagda.

* **[!UICONTROL Failed]:** Rapportjobbet misslyckades. Om du vill se varför enskilda rapportinstanser misslyckades för en rapportruta klickar du på ![nedpilen](/help/dsp/assets/chevron-down.png "nedpilen") bredvid [!UICONTROL Download]. Misslyckade rapportjobb anges med en felikon (![felindikator](/help/dsp/assets/indicator-critical.png "felindikator")). Håll markören över felikonen om du vill se en beskrivning av felet.

* **[!UICONTROL Completed]:** Rapporten har slutförts för icke-återkommande rapporter. För återkommande rapporter slutförs alla rapportinstanser. Du kan hämta alla rapporter som har slutförts de senaste fyra månaderna.

* **[!UICONTROL Archived]:** Rapporten är arkiverad och kan inte köras. Den här statusen anges när rapportgenereringen misslyckas flera gånger för en rapport. För närvarande kan du inte ange den här statusen från användargränssnittet.

>[!MORELIKETHIS]
>
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Hämta en anpassad rapport](/help/dsp/reports/report-download.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Frågor och svar om hushållsrapporter](/help/dsp/reports/faq-household-report.md)
>* [Typer av prestandarapporter i Campaign Management-vyer](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
>* [Om [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
