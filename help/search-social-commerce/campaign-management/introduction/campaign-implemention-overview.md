---
title: Översikt över att implementera annonsnätverkskonton och -kampanjer
description: Lär dig mer om de uppgifter som krävs för att konfigurera, synkronisera och hantera era annonsnätverkskonton.
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Översikt över att implementera annonsnätverkskonton och -kampanjer

Adobe samarbetar med varje annonsör för att upprätta sina annonsnätverkskonton och -kampanjer. Detta innefattar att konfigurera sökmarknadsföring, sociala medier och handel för att ansluta till och synkronisera med annonsörens konton, skapa nya kampanjer och kampanjkomponenter efter behov, konfigurera spårning för komponentannonser, alternativt lägga till kampanjer i portfolior för att göra det möjligt för Search, Social och Commerce att optimera offerterna och validera initiala kostnader, klick och intäktsdata.

När en kampanj har aktiverats och lagts till i en portfölj måste kontohanteringsgruppen, reklamteamet eller annonsören (beroende på villkoren i servicenivåavtalet) övervaka varje kampanj och ändra de relevanta komponenterna och inställningarna efter behov för att uppfylla annonsörens mål.

Den här sidan innehåller information om alla kontotyper, inklusive hur du ställer in kampanjstrukturen för synkroniserade konton. Mer information om hur du konfigurerar konton för enbart spårning finns i [!DNL Naver], se &quot;[Implementera [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Inledande inställningsuppgifter för konton och kampanjer

[!DNL Adobe] och/eller kommer att arbeta tillsammans med er och göra följande:

1. (Nya annonserkonton) Konfigurera administratörskonton:

   1. Ställ in annonsörens konto.

   1. (Om det behövs) Skapa användarkonton för annonsören för att visa och hantera kampanjdata och för att generera rapporter.

1. (Vissa annonsnätverk) Få behörighet för sökning, sociala medier och handel att komma åt varje konto via annonsnätverkets API och användargränssnittet för sökning, sociala medier och handel.

1. För varje annonsnätverkskonto:

   1. (Om det behövs) Konfigurera kontot i annonsnätverket.

   1. Integrera med kontot via [skapa en motsvarande kontopost](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) i Sök, Socialt, &amp; Commerce som innehåller kontoinloggningsuppgifter och spårningsalternativ, och ange kontostatus till aktiverad.

      Search, Social, &amp; Commerce synkroniseras sedan med annonsnätverket. Om kontot redan innehåller kampanjdata är informationen tillgänglig på cirka 24 timmar.

   1. ([Annonstyper som du kan skapa/redigera](/help/search-social-commerce/introduction/supported-inventory.md) i Sök, Socialt, &amp; Commerce) Om kontot inte redan innehåller kampanjdata skapar du kampanjstruktur och kampanjkomponenter i Sök, Socialt och Commerce med någon av följande metoder som är tillgängliga för annonstypen:

      * (Google Ads, Microsoft Advertising, Yahoo! Ads, and Yandex accounts only) Set up an [automatiserad process för att skapa dynamiska annonser och nyckelord för varje objekt i ert lager](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) enligt en annonsspecifik annonsmall som du skapar och innehållet i lagerdatafiler som du överför till en FTP-plats.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, and Yandex accounts only) Upload [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) som innehåller så mycket data som du vill ha för ett konto och sedan bokför dem i annonsnätverken.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads och Yandex (endast konton) Ange data för enskilda komponenter direkt i gränssnittet. För de flesta kampanj- och annonstyper kan ni skapa data på kampanjnivå, annonsgruppnivå och individuella nyckelord, placeringar och annonsnivåer.

      Vissa kampanjer och annonstyper kräver dock unika arbetsflöden. Se instruktionerna för konfiguration [[!DNL Microsoft Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamiska sökannonser](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] max-kampanjer för prestanda](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md)och [[!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] endast konton för spårning) Överför [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) med data för att replikera befintliga kampanjer, annonsgrupper och nyckelord i Sök, Social och Commerce utan att publicera dem på [!DNL Naver].

1. Ställ in spårning för alla annonser som Adobe Advertising ska spåra konverteringar för:

   1. (Annonsörer med Adobe Advertising-tjänst för spårning av konvertering) Vid behov [konfigurera klickspårning](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) för annonser och om du vill kan du söka efter nyckelord, placeringar och annonser genom att generera och överföra klicknings-URL:er för sökning, sociala medier och handel.

      För [!DNL Google Ads] maximala prestandakampanjer, konfigurera all spårning i [kampanjens spårningsinställningar](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. För kampanjer som bara kan spåras måste du i stället generera mål-URL:er med hjälp av kalkylblad och sedan lägga till de genererade mål-URL:erna till de relevanta entiteterna med annonsnätverkets interna redigerare.

   1. Ställ in konverteringsspårning. Beroende på implementeringen kan detta innebära att konverteringsspårningstaggar läggs till på annonsörens webbsidor och/eller att en daglig feed-släppning ställs in för konverteringsdata som annonsören har samlat in separat.

      Om du använder tjänsten för spårning av konvertering i Adobe Advertising kan du generera spårningstaggar för konvertering [inom sökning, sociala medier och handel](/help/search-social-commerce/tools/conversion-tag-generate.md) eller [använda Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Validera de data som spåras.

   Mer information om hur du ställer in spårning finns i kapitlet om spårning.

1. (Annonsörer med Adobe Analytics) [Integrera Adobe Advertising och analyser](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) så att de kan utbyta data.

1. (Att göra det möjligt för Search, Social och Commerce att optimera anbud och/eller kampanjbudgetar. [kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md) endast) [Tilldela kampanjen till en portfölj](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Om portföljen inte redan har startats (optimera anbud och/eller budgetar) kan optimeringsfunktionen samla in tillräckligt med data för att kunna skapa kostnads- och intäktsmodeller så att du kan fastställa portföljens baslinjeprestanda innan du startar den.

   Aktivera inlärning för portföljen om portföljen redan har startats. Mer information finns i&quot;Justera portföljstrategier&quot;. Ni bör förvänta er att portföljen blir rörlig när ni lägger till nya kampanjer, medan optimeringsfunktionen samlar in data om kampanjens budenheter. Bindningen justeras automatiskt inom en till tre veckor.

   Mer information om portföljer finns i Optimeringshandboken, som finns i Sök, Socialt och Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Om nya konverteringar spåras för annonsören) [Göra konverteringarna tillgängliga](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) för rapporter, kampanjhanteringsvyer och portföljmål.

1. Verifiera för varje kampanj att Search, Social och Commerce tar emot klick- och kostnadsdata från annonsnätverket och validera de intäktsdata som visas i Search, Social och Commerce med annonsörens egna intäktsdata.

1. (Valfritt) Automatisera rapporteringen genom att skapa rapportmallar, kalkylbladsflöden och FTP-leverans av schemalagda rapporter.

   Instruktioner finns i kapitlet&quot;Rapporter&quot;.

>[!MORELIKETHIS]
>
>* [Om kampanjhantering i Sök, Social och Commerce](campaign-management-about.md)
>* [Övervaka och hantera resultatet för era annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Google Ads-konverteringsdata i Search, Social och Commerce](google-conversion-data.md)
>* [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md)
