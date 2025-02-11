---
title: Resultatrapporter på erfarenhetsnivå
description: Lär dig hur du visar resultatrapporter på erfarenhetsnivå.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: c5ce127f9a9573962939539c6c449b83715d2e4c
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 0%

---

# Resultatrapporter på erfarenhetsnivå

*Stängd beta*

Du kan visa detaljerade prestandadata för alla upplevelser.

## Data i resultatrapporter på erfarenhetsnivå

I rapportvyn finns följande data:

* Fliken **Översikt**: En prestandaöversikt för hela upplevelsen, inklusive:

   * Avsnittet **Övergripande prestanda**:

   * **Övergripande prestanda**: Det totala antalet visningar, klick, klickfrekvens (CTR) samt genomskinlighetskonverteringar och klickkonverteringar för ett enda konverteringsmått. <!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **Standardfrekvens**: (Erfarenheter med endast mål för beslutsträd) Antalet visningar från målgruppsanpassade kreatörer, generiska kreatörer utan mål eller som är riktade till &quot;Alla andra&quot; och det kreativa standardvärdet för upplevelsen.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **Avsnittet** för prestandafördelning:

      * **Regional Performance:*: Individuella mätvärden per geografisk plats.

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Enhetsprestanda:** Individuella mått per enhetstyp, operativsystem och webbläsare. Du kan också klicka på värdet för en enhetskategori för att visa en lista över de <!-- NN --> främsta kreatörerna som uppfyller det villkoret.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Fliken Creative Performance***: En prestandaöversikt av creative och bundle- eller ad-tagg, inklusive:

   * **Creative** subtab: The total number of imponsions, clicks, and CTR for each creative in the experience.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * Underfliken **Paket/taggar**: Det totala antalet visningar, klickningar och CTR för enskilda paket (upplevelser med mål för beslutsträd) eller annonstaggar (upplevelser utan mål för beslutsträd) i upplevelsen.

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## Visa resultatrapporter för en upplevelse

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika upplevelser.

1. Välj upplevelse:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Reports]**.

   * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Reports]**.

   Fliken [!UICONTROL Overview] öppnas.

1. (Valfritt) I det övre högra verktygsfältet anger du datumintervall, konverteringsattribueringsregel och konverteringar som rapporterats i alla resultatrapporter:

   * (Valfritt) Om du vill ändra datumintervallet för prestandadata väljer du ett alternativ på datummenyn:

      * Om du vill ange en förinställd period väljer du rapporten: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* eller *[!UICONTROL Yesterday]*.

      * Om du vill ange ett anpassat datumintervall anger du startdatum och slutdatum <!-- in the format MM/DD/YYYY or M/D/YYYY,--> eller klickar på ![kalenderikon](/help/search-social-commerce/assets/calendar.png) bredvid ett fält och väljer ett datum.

   * (Valfritt) Om du vill ändra regeln som används för att attributera konverteringsdata i en serie händelser som leder till en konvertering klickar du på ![Inställningar](/help/creative/assets/settings.png) och ändrar **[!UICONTROL Attribution Rule]**.

   * (Valfritt) Om du vill ändra de konverteringar som rapporteras klickar du på ![Inställningar](/help/creative/assets/settings.png) och väljer konverteringsnamnen på **[!UICONTROL Conversions]** -menyn.&lt;!— Bara en eller flera? Kontrollera hur de visas - jag behöver en annonsör med flera konverteringar redan installerade —>

     De tillgängliga konverteringskolumnerna innehåller konverteringar som är tillgängliga i Advertising Search, Social och Commerce, oavsett om du är kund hos Search, Social eller Commerce eller inte. Detta kan inkludera konverterings- och webbplatsengagemangsmått som synkroniseras från Adobe Analytics. <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> Mer information om hur du inkluderar insamlade konverteringar i rapporter finns i avsnittet om sök-, sociala och Commerce-handboken [Om att hantera en annonsörs konverteringsmått](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md).

1. (På fliken [!UICONTROL Overview]):

   * (Valfritt) I avsnittet [!UICONTROL Overall Regional Performance] håller du markören över en punkt i diagrammet för att se data för den punkten.

   * (Valfritt) Gör något av följande i avsnittet [!UICONTROL Regional Performance]:

      * Klicka på ett måttnamn (till exempel [!UICONTROL Impressions]) för att visa måttet.

      * Markera området på menyn [!UICONTROL Region].

      * Håll markören över ett land eller en delstat för att se data för den regionen.

   * (Valfritt) Gör något av följande i avsnittet [!UICONTROL Device Performance]:

      * Håll markören över värdet för en enhetskategori för att se data för det villkoret.

      * Klicka på värdet för en enhetskategori för att visa en lista över de <!-- NN--> främsta kreatörerna som uppfyller det villkoret.

1. (Valfritt) Klicka på fliken **[!UICONTROL Creative Performance]** om du vill visa data efter kreativt innehåll och per paket- eller annonstagg.

   * På underfliken [!UICONTROL Creatives] kan du göra något av följande:

      * (Valfritt) Om du vill växla mellan diagramvyn och stödrastervyn klickar du på ![Diagram](/help/creative/assets/chart-view-button.png "Diagram") respektive ![Stödraster](/help/creative/assets/table-view-button.png "Stödraster").

      * (Valfritt) Håll markören över en punkt i diagrammet i diagramvyn om du vill visa data för den punkten.

      * (Erfarenheter med enbart mål för beslutsträd; valfritt) Aktivera **[!UICONTROL Split targeting]** om du vill dela upp resultatet för varje tillämpat annonseringsmål.

1. Klicka på underfliken **[!UICONTROL Bundles]** om du vill visa data per paket (upplevelser med målgruppsanpassning för beslutsträd) eller annonstagg (upplevelser utan målgruppsanpassning för beslutsträd). Du kan göra något av följande:

   * (Valfritt) Om du vill växla mellan diagramvyn och stödrastervyn klickar du på ![Diagram](/help/creative/assets/chart-view-button.png "Diagram") respektive ![Stödraster](/help/creative/assets/table-view-button.png "Stödraster").

   * (Valfritt) Håll markören över en punkt i diagrammet i diagramvyn om du vill visa data för den punkten.

   * (Erfarenheter med enbart mål för beslutsträd; valfritt) Aktivera **[!UICONTROL Split targeting]** om du vill dela upp resultatet för varje tillämpat annonseringsmål.

1. (Valfritt) Om du vill hämta data i en [!DNL Microsoft Excel]-fil i kalkylbladsformat (XLSX) klickar du på ![Hämta](/help/creative/assets/download.png "Hämta") i verktygsfältet.

   Filen laddas ned enligt webbläsarens normala procedur.

>[!MORELIKETHIS]
>
>* [Anpassad kreativ rapport](/help/creative/report-custom-creative.md)
