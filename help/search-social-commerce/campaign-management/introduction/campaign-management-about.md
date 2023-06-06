---
title: Om kampanjhantering i Sök, Social och Commerce
description: Läs om kampanjhanteringsfunktioner i Sök, Socialt och Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Om kampanjhantering i Sök, Social och Commerce

Med hjälp av sökningar, sociala medier och handel kan ni spåra och/eller hantera era sök-, display-/innehållsbaserade, sociala, shoppingrelaterade, målgrupps- och prestandamängdskampanjer på ett och samma ställe. Beroende på annonsnätverk och kampanjtyp kan de tillgängliga funktionerna omfatta synkronisering med annonsnätverk, skapa och redigera funktioner, spårning och konverteringsattribuering, rapportering samt optimering av bud och budget. Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i &quot;[Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

När du lägger till och redigerar kampanjdata i [!UICONTROL Campaigns] vyer, sökningar, sociala medier och handel överför omedelbart dataändringarna till annonsnätverket. Search, Social, &amp; Commerce hämtar också kampanjstrukturdata och klickar på data från synkroniserade annonsnätverkskonton en gång om dagen (eller oftare när nya kampanjer identifieras) och on demand.

## Konfigurera åtkomst till dina annonsnätverkskonton

För att spåra hur annonser fungerar i annonsörer i annonsnätverkskonton (och för att eventuellt lägga bud för annonserna) kan Adobe Account Team [skapar en motsvarande kontopost](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) i sökmotorkampanjer, sociala medier och handel. Kontoposten innehåller spårningsalternativ.

För konton som synkroniseras via annonsnätverkets API innehåller kontoposten även inloggningsuppgifter för kontoåtkomst. När kontot är aktiverat hämtas kontodata från annonsnätverket. Du kan sedan visa befintliga kontodata samt skapa och redigera kampanjstruktur och annonsdata.

## Klicka på spärra/knip för att knyta klickningar till konverteringar

Om du använder tjänsten för konvertering av annonsering i Adobe måste du inkludera klickspårningskod för sökning, sociala medier och handel i landningssidans suffix, spårningsmallar och URL:er för slutmål/mål för annonser, nyckelord och placeringar, sitelinks och produktlistor. För [annonsnätverk som stöds och kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md) vars kampanjinställningar innehåller &quot;[!UICONTROL EF Redirect]&quot; och &quot;[!UICONTROL Auto Upload],&quot; Search, Social, &amp; Commerce lägger automatiskt till sin egen omdirigerings- och spårningskod när du sparar posten, så du behöver inte lägga till den manuellt. Annars måste du lägga till koden manuellt i spårningsmallarna eller de slutliga URL:erna.

Mer information om spårning finns i kapitlet om spårning.

## Automatisera budgivning och budgethantering

För [annonsnätverk som stöds och kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md)kan ni gruppera era kampanjer i portföljer, där vart och ett har ett specifikt affärsmål och ett specifikt budget- eller prestationsmål. I standardportföljer optimerar Search, Social och Commerce CPC-nyckelordsbud och kampanjbudgetar. Hybridportföljer kombinerar optimeringstekniker från Search, Social, &amp; Commerce och era annonsnätverk.

Mer information om tillgängliga portföljalternativ och hur du ställer in portföljer finns i kapitlet om optimeringsguiden för hantering av Portfolio, som du når från Search, Social och Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Vyer för kampanjhantering

I kampanjhanteringsvyerna kan du övervaka och hantera dina sökkonton. Följande vyer är tillgängliga:

* **[!UICONTROL Campaigns]** — [!UICONTROL Campaigns] vyer visar data från varje anslutet annonsnätverkskonto. Du kan visa kostnads-, klick-, intrycks- och intäktsdata för alla annonsnätverkskonton och för enskilda konton, kampanjer, annonsgrupper, annonser, kundproduktgrupper, praktik, automatiska mål (dynamiska sökmål), målgrupper och annonstilläggsbibliotek samt tillhörande kontoenheter. För [kampanjtyper som stöds i annonsnätverk som stöds](/help/search-social-commerce/introduction/supported-inventory.md)kan ni skapa och redigera data för enskilda kampanjer och kampanjkomponenter direkt i gränssnittet. Du kan också exportera data i de flesta undervyer till en kalkylbladsfil.

   >[!NOTE]
   >
   >Data på annonsnivå är inte tillgängliga för [!DNL Google Ads] dynamisk sökannons (DSA), prestanda max, smart shopping och [!DNL YouTube] kampanjer.

* **[!UICONTROL Products]** — [!UICONTROL Products] vyer visar data för varje [[!DNL Google] or [!DNL Microsoft] handelscentkonto som synkroniseras](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Standardvärdet [!UICONTROL Accounts] I undervyn visas alla synkroniserade konton. vissa användartyper kan lägga till nya konton från den här vyn. The [!UICONTROL Products] i en undervy visas varje produkt i kontot.

* **[!UICONTROL Advanced (ACM)]** — Från [!DNL Advanced] ([!DNL AMC], för vyn Avancerade Campaign Management) kan du skapa automatiserade processer för att [dynamiska annonser och nyckelord som är riktade till varje objekt i ert lager](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) enligt en annonsspecifik annonsmall som du skapar och innehållet i [!DNL Google Merchant Center] konton eller inventeringsdatafiler som du överför till en FTP-plats. Delvisningar visar information om varje flödesmall för annonsören och varje kampanj, annonsgrupp, nyckelord och annons som ingår i en feed som har spridits via en flödesmall men inte publicerats i annonsnätverket.

* **[!UICONTROL Bulksheets]** — Använd [!UICONTROL Bulksheets] vy att skapa [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) som innehåller så mycket data som du vill ha för ett konto på en [stöds i annonsnätverk](/help/search-social-commerce/introduction/supported-inventory.md)och publicera dem sedan i annonsnätverket.

* **[!UICONTROL Audiences]** — [The [!UICONTROL Audiences] vyer](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) visar alla [!DNL Google Ads] och [!DNL Microsoft Advertising] målgrupper som genereras från olika typer av användarlistor. Du kan skapa [!DNL Google Ads] målgrupper från era befintliga Adobe Experience Cloud-målgrupper och era e-postlistor till kunder. Ni kan också visa och hantera målgruppsmål och undantag för era [!DNL Google Ads] och [!DNL Microsoft Advertising] annonser.

* **[!UICONTROL Label Classifications]** — Använd den här vyn för att skapa och ta bort [etikettklassificeringar](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)som kan hjälpa dig att gruppera etiketter i meningsfulla uppsättningar.

>[!MORELIKETHIS]
>
>* [Översikt över att implementera annonsnätverkskonton och -kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera resultatet för era annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Google Ads-konverteringsdata i Search, Social och Commerce](google-conversion-data.md)

