---
title: Översikt över att implementera annonsnätverkskonton och -kampanjer
description: Lär dig mer om de uppgifter som krävs för att konfigurera, synkronisera och hantera era annonsnätverkskonton.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Översikt över att implementera annonsnätverkskonton och -kampanjer

Adobe samarbetar med varje annonsör för att upprätta sina annonsnätverkskonton och -kampanjer. Detta innefattar att konfigurera Search, Social och Commerce för att ansluta och synkronisera med annonsörens konton, skapa nya kampanjer och kampanjkomponenter efter behov, konfigurera spårning för komponentannonser, alternativt lägga till kampanjer i portfolior för att göra det möjligt för Search, Social och Commerce att optimera anbuden på annonserna samt validera initiala kostnader, klick- och intäktsdata.

När en kampanj har aktiverats och lagts till i en portfölj måste kontohanteringsgruppen, reklamteamet eller annonsören (beroende på villkoren i servicenivåavtalet) övervaka varje kampanj och ändra de relevanta komponenterna och inställningarna efter behov för att uppfylla annonsörens mål.

Den här sidan innehåller information om alla kontotyper, inklusive hur du ställer in kampanjstrukturen för synkroniserade konton. Mer information om hur du konfigurerar konton med enbart spårning för [!DNL Naver] finns i [Implementera [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Inledande inställningsuppgifter för konton och kampanjer

[!DNL Adobe] och/eller din byrå kommer att arbeta med dig för att göra följande:

1. (Nya annonserkonton) Konfigurera administratörskonton:

   1. Ställ in annonsörens konto.

   1. (Om det behövs) Skapa användarkonton för annonsören för att visa och hantera kampanjdata och för att generera rapporter.

1. (Vissa annonsnätverk) Få behörighet för Search, Social och Commerce att komma åt varje konto via annonsnätverkets API och användargränssnittet i Search, Social och Commerce.

1. För varje annonsnätverkskonto:

   1. (Om det behövs) Konfigurera kontot i annonsnätverket.

   1. Integrera med kontot genom att [skapa en motsvarande kontopost](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) i Sök, Socialt och Commerce som innehåller autentiseringsuppgifter för kontoåtkomst och spårningsalternativ, och ange kontostatusen till aktiverad.

      Search, Social och Commerce synkroniserar sedan med annonsnätverket. Om kontot redan innehåller kampanjdata är informationen tillgänglig på cirka 24 timmar.

   1. ([Annonstyper som du kan skapa/redigera](/help/search-social-commerce/introduction/supported-inventory.md) i Sök, Socialt och Commerce) Om kontot inte redan innehåller kampanjdata skapar du kampanjstruktur och kampanjkomponenter i Search, Social och Commerce på något av följande sätt som är tillgängliga för annonstypen:

      * (Google Ads, Microsoft Advertising, Yahoo! Endast annonser och Yandex-konton) Konfigurera en [automatiserad process för att skapa dynamiska annonser och nyckelord för varje objekt i ditt lager](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) enligt en annonsspecifik annonsmall som du skapar och innehållet i lagerdatafiler som du överför till en FTP-plats.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, and Yandex accounts only) Överför [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) som innehåller så mycket data som du vill ha för ett konto och bokför dem sedan i annonsnätverken.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads och Yandex (endast konton) Ange data för enskilda komponenter direkt i gränssnittet. För de flesta kampanj- och annonstyper kan ni skapa data på kampanjnivå, annonsgruppnivå och individuella nyckelord, placeringar och annonsnivåer.

      Vissa kampanjer och annonstyper kräver dock unika arbetsflöden. Se instruktionerna för att konfigurera [[!DNL Microsoft Advertising] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamiska sökannonser](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads] maximala prestandakampanjer](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) och [[!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. ([!DNL Naver] endast för spårning av konton) Överför [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) med data för att replikera befintliga kampanjer, annonsgrupper och nyckelord i Sök, Social och Commerce utan att publicera dem på [!DNL Naver].

1. Ställ in spårning för alla annonser som Adobe Advertising ska spåra konverteringar för:

   1. (Annonsörer med konverteringstjänsten Adobe Advertising) Om det behövs kan [konfigurera klickspårning](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) för annonser och eventuellt för nyckelord, placeringar och annonser genom att generera och överföra klickspårnings-URL:er för Search, Social och Commerce.

      Ställ in all spårning i [kampanjens spårningsinställningar](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) för [!DNL Google Ads] maximala prestandakampanjer.

1. För kampanjer som bara kan spåras måste du i stället generera mål-URL:er med hjälp av kalkylblad och sedan lägga till de genererade mål-URL:erna till de relevanta entiteterna med annonsnätverkets interna redigerare.

   1. Ställ in konverteringsspårning. Beroende på implementeringen kan detta innebära att konverteringsspårningstaggar läggs till på annonsörens webbsidor och/eller att en daglig feed-släppning ställs in för konverteringsdata som annonsören har samlat in separat.

      Om du använder tjänsten för spårning av konvertering i Adobe Advertising kan du generera konverteringsspårningstaggar [i Search, Social och Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) eller [med Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Validera de data som spåras.

   Mer information om hur du ställer in spårning finns i kapitlet om spårning.

1. (Annonsörer med Adobe Analytics) [Integrera Adobe Advertising och analys](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) så att de kan utbyta data.

1. (Om du vill att Search, Social och Commerce ska kunna optimera anbud, kampanjbudgetar och/eller strategiska mål för kampanjanbudsstrategier, endast [kampanjtyper som stöds](/help/search-social-commerce/introduction/supported-inventory.md)) [Tilldela kampanjen till en portfölj](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Om portföljen inte redan har startats (optimera anbud och/eller budgetar) kan optimeringsfunktionen samla in tillräckligt med data för att kunna skapa kostnads- och intäktsmodeller så att du kan fastställa portföljens baslinjeprestanda innan du startar den.

   Aktivera inlärning för portföljen om portföljen redan har startats. Mer information finns i&quot;Justera portföljstrategier&quot;. Ni bör förvänta er att portföljen blir rörlig när ni lägger till nya kampanjer, medan optimeringsfunktionen samlar in data om kampanjens budenheter. Bindningen justeras automatiskt inom en till tre veckor.

   Mer information om portföljer finns i Optimeringsguiden som är tillgänglig via Sök, Socialt och Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Om nya konverteringar spåras för annonsören) [Gör konverteringarna tillgängliga](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) för rapporter, kampanjhanteringsvyer och portföljmål.

1. Verifiera för varje kampanj att Search, Social och Commerce tar emot klickdata och kostnadsdata från annonsnätverket och validera de intäktsdata som visas i Search, Social och Commerce med annonsörens egna intäktsdata.

1. (Valfritt) Automatisera rapporteringen genom att skapa rapportmallar, kalkylbladsflöden och FTP-leverans av schemalagda rapporter.

   Instruktioner finns i kapitlet&quot;Rapporter&quot;.

>[!MORELIKETHIS]
>
>* [Om kampanjhantering i Sök, Socialt och Commerce](campaign-management-about.md)
>* [Övervaka och hantera prestandan för annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Google Ads-konverteringsdata i Search, Social och Commerce](google-conversion-data.md)
>* [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md)
