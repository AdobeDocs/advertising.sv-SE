---
title: Implementera  [!DNL Microsoft Advertising] shoppingkampanjer
description: Läs mer om arbetsflödet för att konfigurera  [!DNL Microsoft Advertising] shoppingkampanjer.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementera [!DNL Microsoft Advertising] shoppingkampanjer

Annonser i shoppingkampanjer använder data om produkter i din befintliga [!DNL Microsoft Merchant Center]-produktfeed, i stället för nyckelord, för att bestämma hur och var annonserna ska visas.

[!DNL Microsoft] shoppingkampanjer har [!DNL Microsoft Advertising Shopping Network] som mål. Inställningarna för shoppingkampanjer omfattar ett specificerat land där produkterna säljs och en prioritet ([!DNL High], [!DNL Medium] eller [!DNL Low]). Du kan även filtrera lagret så att du annonserar produkter med specifika attribut och ange eller exkludera specifika platser och enhetstyper.

Du kan styra vilka produkter som visas med dina shoppingannonser genom att konfigurera *[produktgrupper på flera nivåer](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* på annonsgruppsnivå. Produktgrupper baseras på alla produktattribut (kategori, produkttyp, varumärke, villkor, produkt-ID och anpassade etiketter), och du kan skapa upp till sju nivåer av produktgrupper som ska inkluderas eller exkluderas från bud, med undantag för [!DNL Add Products]. Du kan ange offerter på den lägsta produktnivån med samma bud för alla matchande produkter. När samma produkt ingår i mer än en kampanj använder [!DNL Microsoft Advertising] kampanjnivåprioriteten först för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

## Steg för att konfigurera [!DNL Microsoft Advertising] shoppingkampanjer

Du kan ställa in shoppingkampanjer med hjälp av [lagerflödesmallar](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) för [!DNL Microsoft Advertising], med [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) eller individuellt. Följande instruktioner innehåller länkar till hur du skapar enskilda enheter.

1. Konfigurera ditt [!DNL Microsoft Merchant Center]-konto och fyll i det med produktdata.

1. [Tillåt att data hämtas från  [!DNL Microsoft Merchant Center] kontot](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) via Search, Social och Commerce.

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) i shoppingnätverket.

1. [Skapa en annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) i kampanjen och ange standardbud för alla annonser.

   Du kan åsidosätta standardanbudet för enskilda produktgrupper.

1. Skapa produktgrupper för annonsgruppen:

   1. [Skapa produktgruppen&quot;Alla produkter&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Valfritt) [Skapa underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Skapa [produktannonser](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) med [kampanjrader som kan ingå i varje shoppingannons](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) i annonsgruppen.

      Microsoft Advertising genererar dynamiskt annonskopian och landningssidans URL för varje annons.

      >[!NOTE]
      >
      >Även om annonsgruppen inte innehåller annonsenheter visas fortfarande annonser för produkterna i [!DNL Microsoft Advertising].

1. (Valfritt) Om du vill spåra klick på annonsen [skapar du en spårnings-URL med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md). Det bästa sättet är att lägga till spårnings-URL:en i fältet [!UICONTROL Tracking Template] i inställningarna för konto, kampanj eller produktgrupp. För enklare underhåll bör du lägga till det på högsta möjliga nivå.

   Du kan också lägga till spårnings-URL:en till produktdata i [!DNL Microsoft Merchant Center]-kontot. Om du vill göra det inkluderar du spårnings-URL:en, tillsammans med värdet i fältet &quot;link&quot; eller &quot;mobile_link&quot;, beroende på vad som är tillämpligt, i den anpassade kolumnen &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; i produktflödet. Värdet i fältet &quot;bingads_redirect&quot; ersätter värdena i fälten &quot;link&quot; och &quot;mobile_link&quot;. URL-adresser som skapas med den här metoden innehåller inte spårningsparametrar som anges i inställningarna för kontot Sök, Socialt &amp; Commerce eller för kampanjen.

1. Övervaka prestanda genom att [generera [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Vid behov:

   1. [Redigera kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för att justera kampanjbudgeten.

      Om kampanjen är en del av en portfölj tillåter portföljinställningen [!UICONTROL Auto adjust campaign budget limits] Search, Social och Commerce att optimera budgeten för alla kampanjer i portföljen.

   1. Justera det maximala anbudet för befintliga produktgrupper, ta bort produktgrupper som du inte längre vill skapa annonser för, eller lägg till en ny produktgrupp för alla produkter eller nya underordnade produktgrupper för att skapa annonser för ytterligare produkter.

>[!NOTE]
>
>* Se de fält som krävs för att hantera [!DNL Microsoft Shopping] kampanjer och produktgrupper med hjälp av [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) och [lagerfeed-mallar](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Mer information om [!DNL Microsoft Shopping] kampanjer finns i [[!DNL Microsoft Advertising] dokumentationen](https://help.ads.microsoft.com/#apex/3/en/50903).
