---
title: Implementera [!DNL Google Ads] shoppingkampanjer
description: Läs mer om arbetsflödet för konfiguration [!DNL Google Ads] shoppingkampanjer.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 3c702a01df1186e74c4f329a08199ce829be0827
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementera [!DNL Google Ads] shoppingkampanjer

Annonser i shoppingkampanjer använder data om produkter i era befintliga [!DNL Google Merchant Center] produktflöde, i stället för nyckelord, för att bestämma hur och var annonserna ska visas.

[!DNL Google Ads] kampanjer kan rikta sig till [!DNL Google Shopping Network] med [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; Inställningar för [!DNL Google Shopping] kampanjer innehåller en prioritet ([!UICONTROL High], [!UICONTROL Medium], eller [!UICONTROL Low]). Du kan även visa din lokala lagerinformation i dina shoppingannonser med hjälp av en inställning på kampanjnivå.

Du kan styra vilka produkter som visas med dina shoppingannonser genom att konfigurera flera nivåer *[produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* på annonsgruppsnivå. Produktgrupper baseras på alla produktattribut (kategori, produkttyp, varumärke, villkor, produkt-ID och anpassade etiketter), och du kan skapa upp till sju nivåer av produktgrupper som ska inkluderas eller exkluderas från bud. Du kan ange offerter på den lägsta produktnivån med samma bud för alla matchande produkter. När samma produkt ingår i mer än en kampanj [!DNL Google Ads] använder prioriteten på kampanjnivå först för att avgöra vilken kampanj (och tillhörande bud) som är berättigad till annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

## Steg som ska konfigureras [!DNL Google Ads] shoppingkampanjer

Du kan skapa shoppingkampanjer med [mallar för lagerfeed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Google Shopping], genom att använda [glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)eller individuellt. Följande instruktioner innehåller länkar till hur du skapar enskilda enheter.

1. Konfigurera [!DNL Google Merchant Center] och fylla i produktdata.

1. [Tillåt att Search, Social och Commerce hämtar data från [!DNL Google Merchant Center] konto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) i shoppingnätverket.

1. [Skapa en annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) inom kampanjen och ange standarderbjudandet för alla annonser.

   Du kan åsidosätta standardanbudet för enskilda produktgrupper.

1. Skapa produktgrupper för annonsgruppen:

   1. [Skapa en produktgrupp för Alla produkter](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Valfritt) [Skapa underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Ni behöver inte skapa shoppingannonser. Även om annonsgruppen inte innehåller annonsenheter, [!DNL Google Ads] visar fortfarande annonser för produkterna.

1. (Valfritt) Om du vill spåra klickningar på annonsen [generera en spårnings-URL med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md)och lägg sedan till den i inställningarna för konto, kampanj eller produktgrupp.

1. Övervaka prestanda med [genererar [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) och [den [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Vid behov:

   1. [Redigera kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för att justera kampanjbudgeten.

      Om kampanjen är en del av en portfölj är portföljinställningen[!UICONTROL Auto adjust campaign budget limits]&quot; gör det möjligt för Search, Social och Commerce att optimera budgeten för alla kampanjer i portföljen.

   1. [Justera det högsta anbudet för befintliga produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [ta bort produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) som du inte längre vill skapa annonser för, eller lägga till en [ny produktgrupp&quot;alla produkter&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) eller [nya underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) för att skapa annonser för ytterligare produkter.

>[!NOTE]
>
>* Se obligatoriska fält för hantering [!DNL Google Shopping] kampanjer och produktgrupper med [glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) och [mallar för lagerfeed](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Mer information om [!DNL Google Shopping] kampanjer, se [[!DNL Google Ads] dokumentation](https://support.google.com/google-ads/answer/2454022).
