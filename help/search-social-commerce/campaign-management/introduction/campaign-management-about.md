---
title: Om kampanjhantering i Search, Social och Commerce
description: Läs om kampanjhanteringsfunktionerna i Search, Social och Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Om kampanjhantering i Search, Social och Commerce

Med Search, Social och Commerce kan ni spåra och/eller hantera era söknings-, display-/innehållsbaserade, sociala, shoppingbaserade, målgrupps- och prestandamängdskampanjer på ett och samma ställe. Beroende på annonsnätverk och kampanjtyp kan de tillgängliga funktionerna omfatta synkronisering med annonsnätverk, skapa och redigera funktioner, spårning och konverteringsattribuering, rapportering samt optimering av bud och budget. Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).

När du lägger till och redigerar kampanjdata i [!UICONTROL Campaigns]-vyerna skickas dataändringarna direkt till annonsnätverket via Search, Social och Commerce. Search, Social, &amp; Commerce hämtar också kampanjstrukturdata och klickar på data från synkroniserade annonsnätverkskonton en gång om dagen (eller oftare när nya kampanjer identifieras) och on demand.

## Konfigurera åtkomst till dina annonsnätverkskonton

För att spåra annonsernas prestanda i annonsnätverkskontot (och för att eventuellt lägga bud för annonserna) skapar kontogruppen [en motsvarande kontopost](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) i Search, Social och Commerce på Adobe. Kontoposten innehåller spårningsalternativ.

För konton som synkroniseras via annonsnätverkets API innehåller kontoposten även inloggningsuppgifter för kontoåtkomst. När kontot är aktiverat hämtas kontodata från annonsnätverket. Du kan sedan visa befintliga kontodata samt skapa och redigera kampanjstruktur och annonsdata.

## Klicka på spärra/knip för att knyta klickningar till konverteringar

Om du använder tjänsten för spårning av konvertering av Adobe Advertising måste du inkludera kod för klickspårning i sökningen, sociala medier och Commerce i landningssidans suffix, spårningsmallar och URL:er för slutprodukt/mål för annonser, nyckelord och placeringar, sitelinks och produktlistor. För [annonsnätverk och kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md) vars kampanjinställningar innefattar [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] lägger Search, Social och Commerce automatiskt till en egen omdirigerings- och spårningskod när du sparar posten, så du behöver inte lägga till den manuellt. Annars måste du lägga till koden manuellt i spårningsmallarna eller de slutliga URL:erna.

Mer information om spårning finns i kapitlet om spårning.

## Automatisera budgivning och budgethantering

För [annonsnätverk som stöds och kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md) kan du gruppera dina kampanjer i portföljer, där vart och ett har ett specifikt affärsmål och ett specifikt budget- eller prestationsmål. I standardportfolior optimerar Search, Social och Commerce nyckelordserbjudanden och kampanjbudgetar för CPC. Hybridportföljer kombinerar optimeringstekniker från Search, Social och Commerce samt dina annonsnätverk.

Mer information om tillgängliga portföljalternativ och hur du konfigurerar portföljer finns i kapitlet om optimeringsguiden för Portfolio, som är tillgänglig i Sök, Socialt och Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Vyer för kampanjhantering

I kampanjhanteringsvyerna kan du övervaka och hantera dina sökkonton. Följande vyer är tillgängliga:

* **[!UICONTROL Campaigns]** - [!UICONTROL Campaigns]-vyerna visar data från varje anslutet annonsnätverkskonto. Du kan visa kostnads-, klick-, intrycks- och intäktsdata för alla annonsnätverkskonton och för enskilda konton, kampanjer, annonsgrupper, annonser, kundproduktgrupper, praktik, automatiska mål (dynamiska sökmål), målgrupper och annonstilläggsbibliotek samt tillhörande kontoenheter. För [kampanjtyper som stöds i annonsnätverk som stöds](/help/search-social-commerce/introduction/supported-inventory.md) kan du skapa och redigera data för enskilda kampanjer och kampanjkomponenter direkt i gränssnittet. Du kan också exportera data i de flesta undervyer till en kalkylbladsfil.

  >[!NOTE]
  >
  >Data på annonsnivå är inte tillgängliga för [!DNL Google Ads] dynamisk sökannons (DSA), prestandamängd, smart shopping och [!DNL YouTube] kampanjer.

* **[!UICONTROL Products]** - [!UICONTROL Products]-vyerna visar data för varje [[!DNL Google] - eller [!DNL Microsoft] handelscenterkonto som synkroniseras](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Standardundervyn [!UICONTROL Accounts] visar alla synkroniserade konton. Vissa användartyper kan lägga till nya konton från den här vyn. I [!UICONTROL Products]-undervyn visas alla produkter i kontot.

* **[!UICONTROL Advanced (ACM)]** - Från vyn [!DNL Advanced] ([!DNL AMC] för avancerad Campaign Management) kan du skapa automatiska processer för att skapa [dynamiska annonser och nyckelord för varje objekt i ditt lager](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) enligt en annonsspecifik annonsmall som du skapar och innehållet i [!DNL Google Merchant Center]-konton eller lagerdatafiler som du överför till en FTP-plats. Delvisningar visar information om varje flödesmall för annonsören och varje kampanj, annonsgrupp, nyckelord och annons som ingår i en feed som har spridits via en flödesmall men inte publicerats i annonsnätverket.

* **[!UICONTROL Bulksheets]** - Använd [!UICONTROL Bulksheets]-vyn för att skapa [kalkylbladsfiler](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) som innehåller så mycket data som du vill ha för ett konto i ett [annonsnätverk som stöds](/help/search-social-commerce/introduction/supported-inventory.md) och publicera dem sedan i annonsnätverket.

* **[!UICONTROL Audiences]** - [I [!UICONTROL Audiences]-vyerna](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) visas alla dina [!DNL Google Ads]- och [!DNL Microsoft Advertising]-målgrupper som genererats från olika typer av användarlistor. Du kan skapa [!DNL Google Ads] målgrupper från dina befintliga Adobe Experience Cloud-målgrupper och dina e-postlistor för kunder. Du kan också visa och hantera målgruppsmål och undantag för dina [!DNL Google Ads]- och [!DNL Microsoft Advertising]-annonser.

* **[!UICONTROL Label Classifications]** - Använd den här vyn för att skapa och ta bort [etikettklassificeringar](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), vilket kan hjälpa dig att gruppera dina etiketter i meningsfulla uppsättningar.

>[!MORELIKETHIS]
>
>* [Översikt över implementering av annonsnätverkskonton och kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera prestandan för annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Google Ads-konverteringsdata i Search, Social och Commerce](google-conversion-data.md)
