---
title: Användningsexempel
description: Läs om användningsexempel för delning av Advertising DSP-mediedata med Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Användningsexempel för att hämta medieexponeringsdata i Adobe Audience Manager

*Annonsörer med endast Advertising DSP*

*Annonsörer med endast Adobe Advertising-Adobe Audience Manager-integrering*

Här följer några exempel på hur du kan dra nytta av att hämta dina Advertising DSP-medieexponeringsdata <!-- ad impression data? --> i Audience Manager.

## Hantering av senaste och frekvenser

Genom att samla in visningsdata i Audience Manager kan ni förbättra frekvenshanteringen genom att skapa segment med användare som har exponerats för en viss annons eller kampanj. Du kan använda de här segmenten för annonsinriktning om du vill öka frekvensen eller för annonsundertryckning om du vill begränsa frekvensen.

Med Audience Manager [!DNL Segment Builder] kan du dessutom använda [- och frekvenskontroller ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) på alla [regelbaserade traits](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) som innehåller åtgärdbara signaler. På så sätt kan du till exempel begränsa hur många gånger en användare visas som en viss kreativ del i en mediekampanj. Läs [Undertryckande av direktenheter](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html) om du vill veta mer om detta.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sekventiellt meddelande

Genom att samla in visningsdata kan du skapa ett segment med användare som har exponerats för en kampanj eller annons och använda det här segmentet för sekventiella meddelanden eller undertryckande. Du kan till exempel återannonsera användare som såg `123` men som inte klickade eller konverterade genom att visa dem som `456`.

Så här kör du det här exemplet i Audience Manager:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Skapa ett varumärke för att fånga användare som såg den kreativa sidan.

   Använd följande trait-regel om du till exempel vill namnge trait `Creative Trait 123`:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Skapa en egenskap för att fånga in användare som klickar eller konverterar.

   Om du till exempel vill namnge den här egenskapen `Click and Converter` använder du följande trait-regel:

   ```
   d_event == click OR d_event=conv
   ```

1. Skapa ett segment med namnet `Retarget Users` för att fylla i med användare som såg det kreativa `123` men som inte klickade eller konverterade. Använd följande trait-regel:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mappa segmentet `Retarget Users` till ett mål och ange målanvändare i målet med det kreativa `456`.

## [!DNL Adobe Audience Analytics] och kampanjexponeringsdata

När kampanjens intryck och klickdata är tillgängliga i Audience Manager kan ni skapa egenskaper och segment för användare som exponerats för, eller interagerats med, en viss kampanj eller taktik. Med en [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kan dina Audience Manager-segment synkroniseras med [!DNL Analytics] för ytterligare analys. Exempel på användningsområden är följande:

* **Interaktionsanalys mellan DSP och [!DNL Advertising Search, Social, & Commerce] annonser:** Standardintegreringen [[!DNL Analytics for Advertising]  ](/help/integrations/analytics/overview.md) ger inga insikter i interaktionen mellan DSP och [!DNL Search, Social, & Commerce] eftersom båda kanalerna använder AMO-ID:n som följer AMO ID-attribueringsregler, där ett sökklick åsidosätter en visningsvy. Genom att skapa ett DSP-exponeringssegment i Audience Manager kan du använda [!DNL Audience Analytics] för att analysera interaktionen mellan DSP och [!DNL Search, Social, & Commerce] annonser i [!DNL Analytics].

* **Frekvensanalys:** Du kan skapa segment i Audience Manager baserat på hur många gånger en användare exponerades för en viss annons eller kampanj. Du kan sedan analysera de olika exponeringssegmenten i Analytics för att se hur användarbeteendet ändras beroende på antalet exponeringar i DSP.

## [!DNL Audience Optimization Reports]

Du kan utnyttja [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) för att identifiera potentiella prestandamöjligheter för segment i era kampanjer. Dessa rapporter kombinerar kampanjexponering, klickfrekvens och konverteringsdata med segmentstatistik för att skapa segmentbaserade optimeringar och en effektiv kanalmix.

### Typer av relevanta Audience Optimization-rapporter

| Rapport | Beskrivning |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Jämför mappade och omappade segment med visningar och konverteringsgrader. |
| [[!UICONTROL Trend Analysis and Volume Analysis] rapporter]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Returnera data om visningar, klickfrekvens och konverteringar för ett stort antal olika annonsdimensioner. |
| [[!UICONTROL Optimal Frequency] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Hjälper er att hitta den optimala balansen mellan antalet betjänade visningar och konverteringar. Det gör att du kan justera antalet visningar som ska visas innan du börjar se minskande avkastning. |
| [[!UICONTROL Unique User Reach] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Ett bubbeldiagram där varje bubbla storleksanpassas i direkt proportion till antalet unika användare för den valda dimensionen. |

### Överväganden

* Om [!DNL Audience Optimization Reports] användare har rollbaserade åtkomstkontroller (RBAC) måste [!DNL Adobe Customer Care] konfigurera en mappning mellan Advertiser-ID:t och organisationens integreringskod för Audience Manager-datakällan. Administratörsanvändare kan sedan tillhandahålla RBAC-rättigheter till olika användare.

* Konverteringsrapportering i [!DNL Audience Optimization Reports] kräver att slutanvändaren har konfigurerat något. Användarna måste fylla i metadatafiler.

* [!DNL Audience Optimization Reports] stöder inte ändringar i kampanjmetadata (till exempel kampanjnamn eller placeringsnamn).

* Klickningar på sökannonser inkluderas endast i [!DNL Audience Optimization Reports] när de är korrelerade med visningar. Med andra ord behandlas klickningar som konverteringar efter visningar. Därför kanske inte många sökklick tas med i [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Översikt över att skicka exponeringsdata för DSP-medier till Adobe Audience Manager](overview.md)
>* [Samla in klicknings- och visningsdata från Advertising DSP-kampanjer](collect.md)
