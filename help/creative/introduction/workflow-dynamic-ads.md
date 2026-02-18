---
title: Arbetsflöden för dynamiska annonser
description: Läs mer om arbetsflödena för hantering av dynamiska annonser.
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Arbetsflöden för dynamiska annonser

*Användare med behörighet att skapa dynamiska annonser*

Du kan konfigurera dynamiska annonser på två sätt:

* Arbetsflöde 1: Ladda upp en annonsmall och en annonsvariationskatalog direkt i de dynamiska annonsinställningarna när du lägger till dynamiska annonser i ett kreativt bibliotek. Du kan hämta en befintlig feed-mall för att skapa katalogen.

  Använd det här arbetsflödet när samma person kan tillhandahålla all information (med undantag för flödesmallen) för att skapa annonserna. De överförda filerna är fortfarande tillgängliga för framtida bruk.

* Arbetsflöde 2: Skapa en annonsmall och annonsvariationskataloger i separata vyer och lägg sedan in dynamiska annonser separat i en kreatör med hjälp av de redan tillgängliga annonsmallarna och katalogerna.

  Använd det här arbetsflödet när olika personer utför olika uppgifter eller när du bara vill slutföra en uppgift åt gången.

## Arbetsflöde 1

>[!PREREQUISITES]
>
>* Annonsmallar: En mall för visningsannonser (en ZIP-fil med HTML5-filer) eller en videoannonsmall (en ZIP-fil med en .scene-fil)
>* Produktkataloger i CSV-, TSV- eller Microsoft Excel-format (XLSX)

1. [Skapa dynamiska kreatörer](/help/creative/creative-libraries/creative-add-dynamic.md) för ett kreativt bibliotek. Om du vill ha dynamiska annonser för HTML5 och video överför eller väljer du en befintlig annonsmall och katalog.

1. Använd de dynamiska kreatörerna för annonsupplevelser:

   1. [Skapa dynamiska annonspaket](/help/creative/creative-libraries/bundle-manage.md) som du kan koppla alla samtidigt till en annonsupplevelse.

   1. Skapa dynamiska annonsupplevelser [med målinriktning](/help/creative/experiences/experience-create-targeting.md) eller [utan målinriktning](/help/creative/experiences/experience-create-no-targeting.md) och [tilldela de kreativa paketen till upplevelserna](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Generera och implementera taggar för annonsupplevelser](/help/creative/experiences/experience-tag-export.md) för att köra dem som annonser i din DSP.

      Om du vill använda en annonsupplevelse som en annons i Adobe Advertising DSP överför du annonsupplevelsetaggen till en Advertising DSP-kampanj. Om du vill använda en annonsupplevelse som en annons i en annan DSP implementerar du taggen för annonsupplevelsen i den DSP-versionen.

## Arbetsflöde 2

1. [Skapa en annonsmall](/help/creative/ad-templates/ad-template-manage.md) för dina dynamiska annonser baserat på tillgängliga resurser. Annonsmallen måste vara i ZIP-format och innehålla:<!-- Need to add more specs for templates -->

* Visningsalternativ: HTML5-filer med önskat annonsformat och (endast dynamiska HTML5-annonser) en fil med annonsattributen (.tdf)

* Videoredigerare: En .scene-fil med önskat annonsformat och en fil med annonsattributen (.tdf)

1. Konfigurera era annonselement:

   * (För enstaka statiska HTML5-annonser) Samla in och [ladda upp bildresurserna](/help/creative/feeds/asset-manage.md) för dina annonser.

   * (För dynamiska HTML5- och videoannonser) Skapa kataloger med dina annonselement:

      1. Skapa en feed-fil i Microsoft Excel-kalkylbladsformat (XLSX), med en rad för varje annonsvariant. Inkludera ett bild- eller videonamn i varje rad. Samla in tillhörande bild- och videomaterial separat.

      1. [Överför feedsfilen och resurserna](/help/creative/feeds/asset-manage.md).

      1. [Skapa en feed-mall](/help/creative/feeds/feed-template-manage.md) för att mappa fälten i din feed-fil (kalkylblad) till fält i Advertising Creative serverdel. Du kan även hämta och fylla i mallflödesmallar med fält som är relevanta för butik<!-- and what is the creative template?-->.

      1. [Skapa en katalog](/help/creative/feeds/catalog-manage.md#feed-catalog-create) från en angiven feed-fil och en angiven feed-mall och [bearbeta sedan katalogen](/help/creative/feeds/catalog-manage.md#feed-catalog-process) för att se vilka annonsvariationer som kan skapas från den.

         Du kan bara använda varje feed-fil för en katalog.

         Du kan [spåra statusen för katalogbearbetningsjobb](/help/creative/feeds/job-status-track.md) på fliken [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Skapa dynamiska kreatörer](/help/creative/creative-libraries/creative-add-dynamic.md) för ett kreativt bibliotek. Använd en angiven annonsmall och angivna kataloger för dynamiska HTML5-annonser.

1. Använd de dynamiska kreatörerna för annonsupplevelser:

   1. [Skapa dynamiska annonspaket](/help/creative/creative-libraries/bundle-manage.md) som du kan koppla alla samtidigt till en annonsupplevelse.

   1. Skapa dynamiska annonsupplevelser [med målinriktning](/help/creative/experiences/experience-create-targeting.md) eller [utan målinriktning](/help/creative/experiences/experience-create-no-targeting.md) och [tilldela de kreativa paketen till upplevelserna](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Generera och implementera taggar för annonsupplevelser](/help/creative/experiences/experience-tag-export.md) för att köra dem som annonser i din DSP.

      Om du vill använda en annonsupplevelse som en annons i Adobe Advertising DSP överför du annonsupplevelsetaggen till en Advertising DSP-kampanj. Om du vill använda en annonsupplevelse som en annons i en annan DSP implementerar du taggen för annonsupplevelsen i den DSP-versionen.
