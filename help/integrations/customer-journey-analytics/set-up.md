---
title: Ställa in datainsamling, dataöverföring och rapportering
description: Lär dig hur du ställer in datainsamling, dataöverföring och rapportering.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 0b6a939a706d0e9155f9cc6335a947cc31192ac7
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# Ställa in datainsamling, dataöverföring och rapportering

*Beta-funktion*

Följande åtgärder krävs för att visa Advertising Cloud-data i Customer Journey Analytics.

1. (Organisationens webbanalytiker; valfritt) [Samla in historiska data för AMO-ID:n och EF-ID:n](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Det här steget gäller endast för annonsörer med [!DNL Analytics for Advertising].

1. (Organisationens webbplatsadministratör för Adobe Experience Platform) [Konfigurera datainsamling i Experience Platform och implementera taggar för konverteringsspårning](#data-collection).

1. (Organisationens webbplatsadministratör för Customer Journey Analytics) [Skapa en anslutning till dina Experience Platform-datauppsättningar i Customer Journey Analytics](#dataset-connection).

1. (Organisationens webbanalytiker) [Konfigurera datavyer i Customer Journey Analytics](#cja-data-views).

1. (Organisationens webbanalytiker) [Konfigurera rapporter och visualiseringar i Customer Journey Analytics Workspace](#cja-reports).

I följande avsnitt finns detaljerade procedurer, som innehåller de uppgifter och inställningar som krävs för integreringen, men som inte förklarar alla funktioner som är tillgängliga i arbetsflödena. Mer information finns i de länkade resurserna.

## Konfigurera datainsamling i Adobe Experience Platform och på din webbplats {#data-collection}

Följande uppgifter krävs för att ställa in datainsamling i Experience Platform och implementera taggar för konverteringsspårning. Organisationens webbplatsadministratör för Experience Platform kan utföra dessa uppgifter, men IT-avdelningen i din organisation kan behöva hjälpa till med att distribuera spårningstaggar.

### Samla in och skicka data från Adobe Advertising till Experience Platform Edge Network som en datauppsättning

1. I Experience Platform [definierar du ett manuellt schema](https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/ui/resources/schemas) för de data som du vill samla in med hjälp av Experience Data Model (XDM).

   * I [!UICONTROL Schema Details] väljer du **[!UICONTROL Experience Event]** som basklass för schemat för att hämta webbplatshändelser. Namnge ditt schema och klicka på **[!UICONTROL Finish]**.

   * Lägg till fältgruppen `Adobe Advertising Cloud ExperienceEvent Full Extension` i den vänstra panelen för att lägga till fält som är specifika för Adobe Advertising.<!-- Add link once published --> Inkludera åtminstone objektet conversionDetails med egenskaperna `trackingCode` och `trackingIdentities` som innehåller [AMO ID och EF ID](ids.md). De andra fälten är valfria.

   * (Valfritt) Lägg till ytterligare fältgrupper efter behov för att ansluta ytterligare datafält till Adobe Advertising-data.

   **Obs!** Du kan skapa flera scheman, men du kan bara använda ett schema per datauppsättning och per datastream, som du skapar i följande steg.

1. [Skapa en datauppsättning](https://experienceleague.adobe.com/sv/docs/experience-platform/catalog/datasets/create) baserat på schemat för att lagra och hantera samlingen med händelsedata.

   * Välj alternativet **[!UICONTROL Create dataset from schema]** och välj ditt schema.

     Adobe Advertising skapar ytterligare datauppsättningar för relaterade sammanfattningsmätdata (till exempel konverteringsvärden) och sökdata (dimensioner/klassificeringsmetadata, till exempel Adobe Advertising kampanjnamn) baserat på din händelsedatamängd. Data för datauppsättningarna fylls i dagligen i Experience Platform.

1. [Skapa en datastream](https://experienceleague.adobe.com/sv/docs/experience-platform/datastreams/configure) för schemat.

   * Välj ditt schema för inställningen [!UICONTROL Mapping schema].

   * Lägg till och aktivera tjänsterna `Adobe Advertising` och `Adobe Experience Platform` i datastream.

     Med dessa tjänster kan Edge Network lagra datauppsättningen och dirigera den till Adobe Advertising.

   * Välj din datauppsättning för inställningen [!UICONTROL Event dataset].

     Varje datastream kan bara infoga data i en datauppsättning.

### Skicka webbplatsdata till Experience Platform datastream

1. Använd Experience Platform [tags](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/home) (tidigare [!DNL Launch]) för att generera en JavaScript-tagg och skicka webbplatsdata till dataströmmen.

   * Skapa en taggegenskap, som är behållaren för taggkonfigurationen.

   * [Installera tillägget Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) från tilläggskatalogen för din egenskap.

     Det här tillägget skickar data från dina webbegenskaper till Experience Cloud via Experience Platform Edge Network.

     Använd inte Adobe Advertising-tillägget.

   * Skapa en anpassad Web SDK-version:

      * Aktivera komponenten [!UICONTROL Custom build components]Advertising **i avsnittet**.

        Den här komponenten innehåller all JavaScript-kod som behövs för Adobe Advertising i taggen. Den lägger också till en&quot;Advertising&quot;-inställning i taggregler (som är valfria) för att definiera hur annonsdata ska användas för attribueringsmätning.

        Du kan även aktivera ytterligare komponenter efter behov.

      * I avsnittet [!UICONTROL SDK Instances]:

         * I inställningarna för [!UICONTROL Datastreams] väljer du datastream som ska användas för alla dina webbmiljöer (produktion, mellanlagring, utveckling).

         * (Endast för organisationer med Adobe Advertising DSP) I inställningarna för [!UICONTROL Adobe Advertising]:

            * Aktivera inställningen **[!UICONTROL Adobe Advertising DSP]** om du vill aktivera genomsiktsspårning.

            * Ange för vilka annonsörer du vill aktivera vystyrningsspårning.

            * (Valfritt) Ange din organisations ID5-partner-ID för att samla in ID:n.

            * (Valfritt) Ange sökvägen till din organisations [!DNL LiveRamp RampID] JavaScript-kod (ats.js) för att samla in ID:n.

         * Spara bygget.

   * (Valfritt) [Skapa regler](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/ui/rules) efter behov för att avgöra när Web SDK ska skicka data till Edge Network.

      * Ange hur annonsdata ska användas för attribueringsmätning för inställningen [!UICONTROL Advertising]. Den här inställningen är användbar när regeln innehåller en sekvens med flera åtgärder och endast är tillgänglig när du har valt komponenten [!UICONTROL Advertising] för den anpassade byggkomponenten. Alternativen är:

        *Automatiskt:* Tillåter att annonsdata kan användas för att mäta annonsattribuering i den aktuella `sendEvent` -åtgärden baserat på data i cachen. I det här fallet utlöses annonsexponeringshändelsen när den får en chans, och den kanske inte är tillgänglig för den aktuella händelsen. Om du till exempel utlöser en utcheckningshändelse för inköp och inga annonsexponeringsdata är tillgängliga i cachen, kommer utcheckningshändelsen inte att tillskrivas annonsexponeringen.

        *Vänta:* Fördröjer utförandet av anropet tills annonseringsdata har hämtats från servern och lösts, vilket garanterar korrekt attribueringsmätning. Du kan till exempel vänta på att händelsen annonsexponering ska lösas innan du utlöser en utcheckningshändelse för inköp. **Obs!** Det kan ta några sekunder att matcha ID:n beroende på webbläsare och ID-typ. Använd det här alternativet om den aktuella `sendEvent`-åtgärden kan hantera några sekunder av fördröjning.

        *Inaktiverad:* (Standard) Utesluter annonsdata från den begäran som du utlöser, vilket gör den otillgänglig för attribuering eller relaterad spårning.

        *Ange ett dataelement:* Använd ett dataelement för att inkludera eller exkludera annonsdata under sidinläsning. Lösta värden för dataelementet kan innehålla `automatic`, `wait` och `disabled`. Se nästa steg.

     Om du inte använder en regel för att konfigurera en `sendEvent`-åtgärd skickas annonsdata som en separat Advertisement enrichment-händelse.

   * Skapa [dataelement](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/ui/data-elements) efter behov för att mappa variabler på webbplatsen till strukturen i XDM-schemat som du skapade tidigare.

1. [Publicera taggen ](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/publish/publishing-flow) i en testmiljö där du kan upprepa utvecklingen av taggar.

1. Validera leveransen av datauppsättningarna och [publicera sedan taggen i din produktionsmiljö](https://experienceleague.adobe.com/sv/docs/experience-platform/tags/publish/publishing-flow).

   Din organisations IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

## Skapa en anslutning till dina Experience Platform-datauppsättningar i Customer Journey Analytics {#dataset-connection}

Följ de här stegen för att hämta Adobe Advertising-data från dina Experience Platform-datauppsättningar till Customer Journey Analytics. Organisationens webbplatsadministratör för Customer Journey Analytics kan utföra dessa åtgärder.

1. I Customer Journey Analytics [skapar du en anslutning](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-connections/create-connection) som innehåller Experience Platform datamängder och schema.

   **Obs!** För närvarande måste du skicka data för alla DSP- och Search-, Social- och Commerce-konton till en enda Experience Platform-instans och sandlåda.

   * Lägg till din datamängd för Experience Platform-händelser (mätvärden), sammanfattningsdatamängd och dimensioner (klassificeringar/metadata).

     Teamet skapade händelsedatamängden och Adobe Advertising skapade sammanfattnings- och dimensionsuppsättningarna baserat på din händelsetabell.

     Du kan även inkludera ytterligare datauppsättningar efter behov.

   * Mappa dimensionsdatauppsättningen till händelsedatauppsättningen:

      1. Öppna inställningarna för dimensionsuppsättningen.

         Rubriken på inställningssidan är [!UICONTROL Lookup Dataset], vilket anger att du kan koppla din dimensionsuppsättning till en av dina måttspecifika datamängder.

      1. Mappa dimensionsdatauppsättningen till händelsedatamängden i avsnittet [!UICONTROL Adobe Advertising Dimensions]:

         1. För fältet [!UICONTROL Key] väljer du det fält som ska användas som nyckel för dimensionsuppsättningen: `Adobe Advertising ID` (vilket är samma som fältet `trackingCode` i schemat).

         1. För fältet [!UICONTROL Matching key] väljer du det fält som ska användas som matchningsnyckel för händelsedatamängden. De tillgängliga fältnamnen innehåller datauppsättningsnamnet inom parentes. Om du till exempel mappar din dimensionsdatauppsättning till din händelsedatauppsättning väljer du `Tracking Code (Event datasets)`.

         Senare mappar du även händelsedatauppsättningen till sammanfattningsdatauppsättningen när du konfigurerar datavyn (#cja-data-views).

1. Efter ett par timmar kontrollerar du att informationen är tillgänglig i Customer Journey Analytics.

   1. I Customer Journey Analytics går du till **[!UICONTROL Connections]** och väljer din anslutning.

   1. Kontrollera att [!UICONTROL Number of Records]-rapporten visar att data har lagts till i listan över datauppsättningar som visas.

## Ställa in datavyer i Customer Journey Analytics {#cja-data-views}

Skapa en eller flera datavyer i Customer Journey Analytics för att definiera mätvärden och dimensioner för rapportering. En webbanalytiker kan utföra dessa uppgifter.

1. I Customer Journey Analytics [skapar du en datavy](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Konfigurera vyn så att den innehåller följande information.

   * Om du har ett Adobe Analytics-konto använder du [!UICONTROL Time Zone] för ditt [!DNL Analytics]-konto i avsnittet [!UICONTROL Calendar] på fliken [!UICONTROL Configure].

   * På fliken [!UICONTROL Components]:

      * Lägg till dimensioner, händelser och sammanfattningsdata.

      * Välj mätvärden från datauppsättningen för händelser (mätvärden) och din dimensionsuppsättning (klassificeringar/metadata) som ska inkluderas i datavyn.

        Du har redan anslutit dessa två datauppsättningar i anslutningen som du skapade i den [senaste proceduren](#dataset-connection).

      * Koppla händelsedatauppsättningen till sammanfattningsdatauppsättningen, som ännu inte är kopplad till något:

         * [Skapa ett härlett fält](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-dataviews/derived-fields) för varje dimension med sammanfattningsdata som du vill ska vara tillgängliga i Customer Journey Analytics.

           Om du till exempel vill visa sammanfattningsdata för kampanjer skapar du ett härlett fält för dimensionen `Adobe Advertising Campaign`.

           Du länkar de två datauppsättningarna med matchande nyckel `trackingCode` (som är schemafältet för Adobe Advertising-ID).

            * I avsnittet [!UICONTROL Lookup] i det härledda regelbyggaren:

               * För fältet **[!UICONTROL Value]** väljer du [!UICONTROL Tracking Code] i datamängden för sammanfattningsstatistik.

               * För fältet **[!UICONTROL Lookup dataset]** väljer du dimensionsuppsättningen (till exempel&quot;Adobe Advertising-klassificering&quot;).

               * För fältet **[!UICONTROL Matching Key]** väljer du [!UICONTROL Tracking Code] från klassificeringsdatamängden.

               * För fältet **[!UICONTROL Values to return]** väljer du dimensionen (till exempel [!UICONTROL Adobe Advertising Campaign]) från klassificeringsdatamängden.

           Det härledda fältnamnet har lagts till med&quot;(DF)&quot;, till exempel `Adobe Advertising Campaign(DF)`.

         * För varje härlett fält:

            * Lägg till det härledda fältet i avsnittet [!UICONTROL Included components].

              Två namn visas nu för samma dimension (till exempel&quot;Adobe Advertising Campaign(DF)&quot; (det härledda fältet) och&quot;Adobe Advertising Campaign&quot; (fältet i sammanfattningsdatauppsättningen)).

            * Markera dimensionen i sammanfattningsdatauppsättningen (till exempel&quot;Adobe Advertising Campaign&quot;) och redigera inställningarna för datauppsättningen.

              Inställningarna öppnas till höger.

               * Välj alternativet **[!UICONTROL Create grouping]** i avsnittet Sammanfattningsdatagrupp.

               * För fältet **[!UICONTROL Dimension]** väljer du det härledda fältet (som bifogas med&quot;(DF)&quot;, t.ex. &quot;Adobe Advertising Campaign(DF)&quot;).

               * Välj alternativet **[!UICONTROL Hide in reporting]** som döljer det härledda fältnamnet i Workspace.

## Ställ in rapporter och visualiseringar i Customer Journey Analytics Workspace {#cja-reports}

Följ de här stegen i Customer Journey Analytics Workspace för att konfigurera rapporter och visualiseringar. En webbanalytiker kan utföra dessa uppgifter.

1. [Skapa ett projekt](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) i Workspace för att skapa rapporter och visualiseringar baserat på de dimensioner och mått som har konfigurerats i datavyn.

1. (Om du har data från [!DNL Google Ads] eller [!DNL Microsoft Advertising]) Skapa en rapport med utgivarspårade konverteringar med hjälp av fält för nätverksspecifika mått, som grupperas som `googleConversions` och `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Översikt](overview.md)
>* [Förutsättningar](prerequisites.md)
>* [Adobe Advertising ID:n som används av [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising-mått och mått i Customer Journey Analytics](advertising-data-in-cja.md)
>* [Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Customer Journey Analytics Guide](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Användarhandbok för Adobe Analytics-användare](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
