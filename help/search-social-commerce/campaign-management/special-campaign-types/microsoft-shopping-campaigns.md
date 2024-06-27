---
title: Implementera [!DNL Microsoft Advertising] shoppingkampanjer
description: Läs mer om arbetsflödet för konfiguration [!DNL Microsoft Advertising] shoppingkampanjer.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementera [!DNL Microsoft Advertising] shoppingkampanjer

Annonser i shoppingkampanjer använder data om produkter i era befintliga [!DNL Microsoft Merchant Center] produktflöde, i stället för nyckelord, för att bestämma hur och var annonserna ska visas.

[!DNL Microsoft] målgruppsanpassa [!DNL Microsoft Advertising Shopping Network]. Inställningarna för shoppingkampanjer omfattar ett specifikt land där produkterna säljs och en prioritet ([!DNL High], [!DNL Medium], eller [!DNL Low]). Du kan även filtrera lagret så att du annonserar produkter med specifika attribut och ange eller exkludera specifika platser och enhetstyper.

Du kan styra vilka produkter som visas med dina shoppingannonser genom att konfigurera flera nivåer *[produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* på annonsgruppsnivå. Produktgrupper baseras på alla produktattribut (kategori, produkttyp, märke, villkor, produkt-ID och anpassade etiketter), och du kan skapa upp till sju nivåer av produktgrupper som ska inkluderas eller exkluderas från offert, exklusive &quot;[!DNL Add Products].&quot; Du kan ange offerter på den lägsta produktnivån med samma bud för alla matchande produkter. När samma produkt ingår i mer än en kampanj [!DNL Microsoft Advertising] använder prioriteten på kampanjnivå först för att avgöra vilken kampanj (och tillhörande bud) som är berättigad till annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

## Steg som ska konfigureras [!DNL Microsoft Advertising] shoppingkampanjer

Du kan skapa shoppingkampanjer med [mallar för lagerfeed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Microsoft Advertising], genom att använda [glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)eller individuellt. Följande instruktioner innehåller länkar till hur du skapar enskilda enheter.

1. Konfigurera [!DNL Microsoft Merchant Center] och fylla i produktdata.

1. [Tillåt att Search, Social och Commerce hämtar data från [!DNL Microsoft Merchant Center] konto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) i shoppingnätverket.

1. [Skapa en annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) inom kampanjen och ange standarderbjudandet för alla annonser.

   Du kan åsidosätta standardanbudet för enskilda produktgrupper.

1. Skapa produktgrupper för annonsgruppen:

   1. [Skapa en produktgrupp för Alla produkter](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Valfritt) [Skapa underordnade produktgrupper](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Skapa [produktannonser](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) med [kampanjrader som kan ingå i varje shoppingannons](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) inom annonsgruppen.

      Microsoft Advertising genererar dynamiskt annonskopian och landningssidans URL för varje annons.

      >[!NOTE]
      >
      >Även om annonsgruppen inte innehåller annonsenheter, [!DNL Microsoft Advertising] visar fortfarande annonser för produkterna.

1. (Valfritt) Om du vill spåra klickningar på annonsen [generera en spårnings-URL med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md). Det bästa sättet är att lägga till spårnings-URL:en i [!UICONTROL Tracking Template] i inställningarna för konto, kampanj eller produktgrupp. För enklare underhåll bör du lägga till det på högsta möjliga nivå.

   Du kan också lägga till spårnings-URL:en till produktdata i [!DNL Microsoft Merchant Center] konto. Om du vill göra det inkluderar du spårnings-URL:en, tillsammans med värdet i fältet &quot;link&quot; eller &quot;mobile_link&quot;, beroende på vad som är tillämpligt, i en anpassad kolumn &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; i produktflödet. Värdet i fältet &quot;bingads_redirect&quot; ersätter värdena i fälten &quot;link&quot; och &quot;mobile_link&quot;. URL-adresser som skapas med den här metoden innehåller inte spårningsparametrar som anges i inställningarna för kontot Sök, Socialt &amp; Commerce eller för kampanjen.

1. Övervaka prestanda med [genererar [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Vid behov:

   1. [Redigera kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för att justera kampanjbudgeten.

      Om kampanjen är en del av en portfölj är portföljinställningen[!UICONTROL Auto adjust campaign budget limits]&quot; gör det möjligt för Search, Social och Commerce att optimera budgeten för alla kampanjer i portföljen.

   1. Justera det maximala anbudet för befintliga produktgrupper, ta bort produktgrupper som du inte längre vill skapa annonser för, eller lägg till en ny produktgrupp för alla produkter eller nya underordnade produktgrupper för att skapa annonser för ytterligare produkter.

>[!NOTE]
>
>* Se obligatoriska fält för hantering [!DNL Microsoft Shopping] kampanjer och produktgrupper med [glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) och [mallar för lagerfeed](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Mer information om [!DNL Microsoft Shopping] kampanjer, se [[!DNL Microsoft Advertising] dokumentation](https://help.ads.microsoft.com/#apex/3/en/50903).
