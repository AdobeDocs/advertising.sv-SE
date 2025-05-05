---
title: Integrering med Adobe Experience Cloud lösningar och tjänster
description: Läs mer om lösningar och tjänster från Adobe Experience Cloud för sökmotoroptimering, sociala medier och Commerce.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Integrering med Adobe Experience Cloud lösningar och tjänster

Advertising Search, Social och Commerce är integrerade med följande [!DNL Adobe]-produkter.

* [Taggar från Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=sv-SE) - Du kan använda [Adobe Advertising Cloud-tillägget](https://exchange.adobe.com/apps/ec/100155) för Adobe Experience Platform för att skapa spårningstaggar för Adobe Advertising-konvertering samt spårningstaggar från tredje part för dina annonssidor. (Du kan också [skapa konverteringsspårningstaggar direkt i Sök, Socialt och Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Kontakta kontogruppen eller implementeringsteamet på Adobe för att få information om hur du tar med dina taggar.

* Adobe Analytics — (avanmälningsfunktion) Adobe Advertising och [!DNL Analytics] är integrerade på följande sätt:

   * Adobe Advertising och [!DNL Analytics] delar sömlöst data. [!DNL Analytics] kan dagligen skicka webbplatsengagemangs- och konverteringsdata till Search, Social och Commerce, där informationen är tillgänglig för annonsoptimering och rapportering. Dessutom kan Adobe Advertising dagligen skicka annonsdata - inklusive visningar, klickningar och kostnader - från dina annonsnätverk till [!DNL Analytics], där data finns tillgängliga i alla rapporteringsverktyg.

     Mer information om stöd för [!DNL Analytics] för varje annonsnätverk och annonstyp finns i [Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md). Se även [Översikt över [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=sv-SE){target="_blank"} för mer information om datautbytet.

     Både Adobe Advertising och [!DNL Analytics] måste vara konfigurerade för att kunna utbyta data. Kontakta kontoteamet på Adobe om du vill ha mer information om den första konfigurationen.

     >[!NOTE]
     >
     >Som standard visas inte måtten [!DNL Analytics] på skärmarna Sök, Socialt och Commerce. Du måste uttryckligen [göra mätvärdena tillgängliga i kampanjhanteringsvyer, portföljer och rapporter](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) när implementeringsteamet [!DNL Adobe] har konfigurerat valda standard- eller anpassade händelser som ska överföras till Adobe Advertising. Du kan ändra de måttnamn som visas (utan att ändra dem i [!DNL Analytics]). Du kan göra mätvärden synliga i gränssnittet och ändra namn på mätvärden från [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Annonsörer med [!DNL Analytics] men inte Audience Manager kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från [!DNL Analytics] segment som delas med Adobe Experience Cloud. För att vara berättigad måste en annonsörer implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=sv-SE) och distribuera en tagg på sina webbplatser. Du kan sedan använda målgrupperna i [!DNL Google Ads] kampanjer som [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) på kampanjnivå eller annonsgruppsnivå.

* Adobe Audience Manager-segment - (anmälningsfunktion) Du kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från Audience Manager-segment som har Sök, Socialt och Commerce som mål. Detta kan omfatta [!DNL Analytics] segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud Audience Library. Du kan sedan använda målgrupperna i [!DNL Google Ads] kampanjer som [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) på kampanjnivå eller annonsgruppsnivå.

  Mer information finns i [Integrering med Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=sv-SE).

* Adobe Target - Du kan implementera klickningsbaserad signaldelning mellan Search, Social och Commerce och [!DNL Target], konfigurera en A/B-testaktivitet i [!DNL Target] för dina annonser och sedan använda [!DNL Analytics] Analysis Workspace för att visa testdata.

* Adobe Campaign - Du kan [skapa och uppdatera en [!DNL Google Ads] kundmatchande målgrupp med hjälp av en e-postlista i [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-meddelanden - (När du är inloggad via Adobe Experience Cloud) Från meddelandelänken ([Varningsmeddelanden](/help/search-social-commerce/assets/notifications-panel.png "Varningsmeddelanden")) högst upp på varje sida kan du visa alla Adobe Experience Cloud-systemuppdateringar, inlägg, omnämnanden och delade resurser. Kontakta kontoteamet på Adobe för information om åtkomst till Adobe Experience Cloud.
