---
title: Implementera  [!DNL Google Ads] shoppingkampanjer
description: Läs mer om arbetsflödet för att konfigurera  [!DNL Google Ads] shoppingkampanjer.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementera [!DNL Google Ads] shoppingkampanjer

Annonser i shoppingkampanjer använder data om produkter i din befintliga [!DNL Google Merchant Center]-produktfeed, i stället för nyckelord, för att bestämma hur och var annonserna ska visas.

[!DNL Google Ads] kampanjer kan rikta in sig på [!DNL Google Shopping Network] med [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot;. Inställningarna för [!DNL Google Shopping] kampanjer innehåller en prioritet ([!UICONTROL High], [!UICONTROL Medium] eller [!UICONTROL Low]). Du kan även visa din lokala lagerinformation i dina shoppingannonser med hjälp av en inställning på kampanjnivå.

Du kan styra vilka produkter som visas med dina shoppingannonser genom att konfigurera *[produktgrupper på flera nivåer](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* på annonsgruppsnivå. Produktgrupper baseras på alla produktattribut (kategori, produkttyp, varumärke, villkor, produkt-ID och anpassade etiketter), och du kan skapa upp till sju nivåer av produktgrupper som ska inkluderas eller exkluderas från bud. Du kan ange offerter på den lägsta produktnivån med samma bud för alla matchande produkter. När samma produkt ingår i mer än en kampanj använder [!DNL Google Ads] kampanjnivåprioriteten först för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

## Steg för att konfigurera [!DNL Google Ads] shoppingkampanjer

Du kan ställa in shoppingkampanjer med hjälp av [lagerflödesmallar](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) för [!DNL Google Shopping], med [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) eller individuellt. Följande instruktioner innehåller länkar till hur du skapar enskilda enheter.

1. Konfigurera ditt [!DNL Google Merchant Center]-konto och fyll i det med produktdata.

1. [Tillåt att data hämtas från  [!DNL Google Merchant Center] kontot](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) via Search, Social och Commerce.

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) i shoppingnätverket.

1. [Skapa en annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) i kampanjen och ange standardbud för alla annonser.

   Du kan åsidosätta standardanbudet för enskilda produktgrupper.

1. Skapa produktgrupper för annonsgruppen:

   1. [Skapa produktgruppen&quot;Alla produkter&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Valfritt) [Skapa underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Ni behöver inte skapa shoppingannonser. Även om annonsgruppen inte innehåller annonsenheter visas fortfarande annonser för produkterna i [!DNL Google Ads].

1. (Valfritt) Om du vill spåra klick på annonsen [skapar du en spårnings-URL med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md) och lägger sedan till den i inställningarna för konto, kampanj eller produktgrupp.

1. Övervaka prestanda genom att [generera [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) och [&#x200B; [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Vid behov:

   1. [Redigera kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för att justera kampanjbudgeten.

      Om kampanjen är en del av en portfölj tillåter portföljinställningen [!UICONTROL Auto adjust campaign budget limits] Search, Social och Commerce att optimera budgeten för alla kampanjer i portföljen.

   1. [Justera det högsta anbudet för befintliga produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [ta bort produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) som du inte längre vill skapa annonser för, eller lägg till en [ny produktgrupp för alla produkter](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) eller [nya underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) om du vill skapa annonser för ytterligare produkter.

>[!NOTE]
>
>* Se de fält som krävs för att hantera [!DNL Google Shopping] kampanjer och produktgrupper med hjälp av [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) och [lagerfeed-mallar](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Mer information om [!DNL Google Shopping] kampanjer finns i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/2454022).
