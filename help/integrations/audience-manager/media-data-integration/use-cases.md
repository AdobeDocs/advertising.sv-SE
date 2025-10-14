---
title: Användningsfall
description: Läs om användningsfall för att dela dina DSP-mediedata om reklam med Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Använd exempel för att hämta medieexponeringsdata i Adobe Audience Manager

*Annonsörer med endast Advertising DSP*

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Audience Manager*

Här följer några exempel på hur du kan dra nytta av att hämta dina Advertising DSP-medieexponeringsdata <!-- ad impression data? --> i Audience Manager.

## Hantering av senaste och frekvenser

Genom att samla in visningsdata i Audience Manager kan ni förbättra frekvenshanteringen genom att skapa segment med användare som har exponerats för en viss annons eller kampanj. Du kan använda de här segmenten för annonsanpassning om du vill öka frekvensen eller för annonshämning om du vill begränsa frekvensen.

Med Audience Manager [!DNL Segment Builder] kan du dessutom använda [- och frekvenskontroller &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html?lang=sv-SE) på alla [regelbaserade traits](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=sv-SE) som innehåller åtgärdbara signaler. På så sätt kan du till exempel begränsa hur många gånger en användare visas som en viss kreativ del i en mediekampanj. Läs [Undertryckande av direktenheter](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html?lang=sv-SE) om du vill veta mer om detta.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sekventiellt meddelande

Genom att samla in visningsdata kan du skapa ett segment med användare som har exponerats för en kampanj eller annons och använda det här segmentet för sekventiella meddelanden eller undertryckande. Du kan till exempel återannonsera användare som såg `123` men som inte klickade eller konverterade genom att visa dem som `456`.

Om du vill köra det här exemplet i Audience Manager följer du de här stegen:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Skapa ett drag för att fånga användare som såg det kreativa.

   Om du till exempel vill namnge egenskapen `Creative Trait 123` använder du följande egenskapsregel:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Skapa ett drag för att fånga in användare som klickar på eller konverterar.

   Om du till exempel vill namnge egenskapen `Click and Converter` använder du följande egenskapsregel:

   ```
   d_event == click OR d_event=conv
   ```

1. Skapa ett segment med namnet `Retarget Users` för att fylla användare som såg den kreativa `123` men inte klickade eller konverterade. Använd följande egenskapsregel:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mappa segmentet `Retarget Users` till ett mål och ange användare i målet med kreativa `456`.

## [!DNL Adobe Audience Analytics] och kampanjexponeringsdata

När kampanjintrycket och klickdata är tillgängliga i Audience Manager kan du skapa drag och segment av användare som exponerades för eller interagerade med en viss kampanj eller taktik. Med en [[!DNL Audience Analytics] integrering](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=sv-SE) kan dina Audience Manager-segment synkroniseras med [!DNL Analytics] för ytterligare analys. Potentiella användningsfall inkluderar följande:

* **Interaktionsanalys mellan DSP och [!DNL Advertising Search, Social, & Commerce] annonser:** Standardintegreringen [[!DNL Analytics for Advertising] 4&rbrace; ger inte insikter i interaktionen mellan DSP och [!DNL Search, Social, & Commerce] eftersom båda kanalerna använder AMO ID som följer AMO ID-attributregler, för vilka ett sökklick åsidosätter en visningsvy. &#x200B;](/help/integrations/analytics/overview.md) Genom att skapa ett DSP exponeringssegment i Audience Manager kan du använda [!DNL Audience Analytics] för att analysera interaktionen mellan DSP och [!DNL Search, Social, & Commerce] annonser i [!DNL Analytics].

* **Frekvensanalys:** Du kan skapa segment i Audience Manager baserat på hur många gånger en användare exponerades för en viss annons eller kampanj. Sedan kan du analysera de olika exponeringssegmenten i Analytics för att se hur användarbeteendet ändras beroende på antalet DSP exponeringar.

## [!DNL Audience Optimization Reports]

Du kan utnyttja [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=sv-SE) för att identifiera potentiella prestandamöjligheter för segment i alla era kampanjer. Dessa rapporter kombinerar kampanjexponering, klickfrekvens och konverteringsdata med segmentstatistik för att skapa segmentbaserade optimeringar och en effektiv kanalmix.

### Typer av relevanta Audience Optimization-rapporter

| Rapport | Beskrivning |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=sv-SE) | Jämför mappade och omappade segment med visningar och konverteringsgrader. |
| [[!UICONTROL Trend Analysis and Volume Analysis] rapporter]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Returnera data om visningar, klickfrekvens och konverteringar för ett stort antal olika annonsdimensioner. |
| [[!UICONTROL Optimal Frequency] rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=sv-SE) | Hjälper dig att hitta den optimala balansen mellan antalet visningar och konverteringar. Det gör att du kan justera antalet visningar som ska visas innan du börjar se minskande avkastning. |
| [[!UICONTROL Unique User Reach] rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=sv-SE) | Ett bubbeldiagram, i vilket varje bubbla visas i direkt proportion till antalet unika användare för den valda dimensionen. |

### Överväganden

* Om [!DNL Audience Optimization Reports]-användare har rollbaserade åtkomstkontroller (RBAC) måste [!DNL Adobe Customer Care] konfigurera en mappning mellan annonserings-ID:t och organisationens integrationskod för datakällan Audience Manager. Administratörsanvändare kan sedan tillhandahålla RBAC-rättigheter till olika användare.

* Konverteringsrapportering i [!DNL Audience Optimization Reports] kräver att slutanvändaren har konfigurerat något. Användarna måste fylla i metadatafiler.

* [!DNL Audience Optimization Reports] stöder inte ändringar i kampanjmetadata (till exempel kampanjnamn eller placeringsnamn).

* Klickningar på sökannonser inkluderas endast i [!DNL Audience Optimization Reports] när de är korrelerade med visningar. Med andra ord behandlas klickningar som konverteringar efter visningar. Därför kanske inte många sökklick tas med i [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Översikt över att skicka DSP Media-exponeringsdata till Adobe Audience Manager](overview.md)
>* [Samla in klicknings- och imponeringsdata från Advertising DSP Campaigns](collect.md)
