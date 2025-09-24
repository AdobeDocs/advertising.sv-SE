---
title: Arbetsflöde för dynamiska annonser
description: Läs mer om arbetsflödet för hantering av dynamiska annonser.
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Arbetsflöde för dynamiska annonser

1. [Skapa en annonsmall](/help/creative/ad-templates/ad-template-manage.md) för dina dynamiska annonser baserat på tillgängliga resurser

1. Konfigurera era annonselement:

   * (För enstaka statiska HTML5-annonser) Samla in och [ladda upp bildresurserna](/help/creative/feeds/asset-manage.md) för dina annonser.

   * (För dynamiska HTML5-annonser) Skapa kataloger av dina annonselement:

      1. Skapa en feed-fil i Microsoft Excel-kalkylbladsformat (XLSX), med en rad för varje annonsvariant. Inkludera ett bildnamn eller en referens till en Adobe Experience Manager på varje rad. Samla in associerade bildresurser separat.

      1. [Överför feeden och bildresurserna](/help/creative/feeds/asset-manage.md).

      1. [Skapa en feed-mall](/help/creative/feeds/feed-template-manage.md) för att mappa fälten i din feed-fil (kalkylblad) till fält i Advertising Creative serverdel.

      1. [Skapa en katalog](/help/creative/feeds/catalog-manage.md#feed-catalog-create) från en angiven feed-fil och en angiven feed-mall och [bearbeta sedan katalogen](/help/creative/feeds/catalog-manage.md#feed-catalog-process) för att se vilka annonsvariationer som kan skapas från den.

         Du kan bara använda varje feed-fil för en katalog.

         Du kan [spåra statusen för katalogbearbetningsjobb](/help/creative/feeds/job-status-track.md) på fliken [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Skapa dynamiska kreatörer](/help/creative/creative-libraries/creative-add-dynamic.md) för ett kreativt bibliotek. Använd en angiven annonsmall och angivna kataloger för dynamiska HTML5-annonser.

1. [Skapa dynamiska annonspaket](/help/creative/creative-libraries/bundle-manage.md) som du kan koppla alla samtidigt till en annonsupplevelse.

1. Skapa dynamiska annonsupplevelser [med målinriktning](/help/creative/experiences/experience-create-targeting.md) eller [utan målinriktning](/help/creative/experiences/experience-create-no-targeting.md) och [tilldela de kreativa paketen till upplevelserna](/help/creative/experiences/experience-assign-creative-bundles.md).

1. [Generera och implementera taggar för annonsupplevelser](/help/creative/experiences/experience-tag-export.md) för att köra dem som annonser i din DSP.

   Om du vill använda en annonsupplevelse som en annons i Adobe Advertising DSP överför du annonsupplevelsetaggen till en Advertising DSP-kampanj. Om du vill använda en annonsupplevelse som en annons i en annan DSP implementerar du taggen för annonsupplevelsen i den DSP-versionen.
