---
title: Integrering med Adobe Experience Cloud lösningar och tjänster
description: Läs mer om lösningar och tjänster från Adobe Experience Cloud för sökmotoroptimering, sociala medier och Commerce.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Integrering med Adobe Experience Cloud lösningar och tjänster

Advertising Search, Social och Commerce är integrerade med följande [!DNL Adobe]-produkter.

* [Taggar från Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=sv-SE) - Du kan använda [Adobe Advertising Cloud Extension](https://experienceleague.adobe.com/sv/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) för Adobe Experience Platform för att [skapa Adobe Advertising-taggar för konverteringsspårning](/help/search-social-commerce/tools/conversion-tag-generate.md), samt spårningstaggar från tredje part, för dina annonssidor. Om din organisation inte har något Experience Platform-konto kan du fortfarande installera tillägget direkt i [användargränssnittet för Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection/), som är kostnadsfritt för Adobe Experience Cloud-kunder.

  Om du vill installera det nödvändiga tillägget kontaktar du din organisations administratör för att få åtkomst till datainsamlingsfunktioner i användargränssnittet och ber dem att ge dig behörighet för `manage_properties`.

  **Obs!** Du kan också [skapa konverteringsspårningstaggar direkt i Sök, Socialt och Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (anmälningsfunktion) Adobe Advertising och [!DNL Analytics] är integrerade på följande sätt:

   * Adobe Advertising och [!DNL Analytics] delar sömlöst data. [!DNL Analytics] kan dagligen skicka webbplatsengagemangs- och konverteringsdata till Search, Social och Commerce, där informationen är tillgänglig för annonsoptimering och rapportering. Dessutom kan Adobe Advertising dagligen skicka annonsdata - inklusive visningar, klickningar och kostnader - från dina annonsnätverk till [!DNL Analytics], där informationen finns tillgänglig i alla rapportverktyg.

     Mer information om stöd för [&#x200B; för varje annonsnätverk och annonstyp finns i &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)Supported Inventory[!DNL Analytics]. Mer information om datautbytet finns även i [Översikt över [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=sv-SE){target="_blank"}.

     För att kunna utbyta data måste både Adobe Advertising och [!DNL Analytics] vara konfigurerade från början. Kontakta ditt Adobe-kontoteam om du vill ha mer information om den första konfigurationen.

     >[!NOTE]
     >
     >Som standard visas inte måtten [!DNL Analytics] på skärmarna Sök, Socialt och Commerce. Du måste uttryckligen [göra mätvärdena tillgängliga i kampanjhanteringsvyer, portföljer och rapporter](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) när implementeringsteamet [!DNL Adobe] har konfigurerat valda standard- eller anpassade händelser som ska överföras till Adobe Advertising. Du kan ändra de måttnamn som visas (utan att ändra dem i [!DNL Analytics]). Du kan göra mätvärden synliga i gränssnittet och ändra namn på mätvärden från [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Annonsörer med [!DNL Analytics] men inte Audience Manager kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från [!DNL Analytics] segment som delas med Adobe Experience Cloud. För att vara berättigad måste en annonsörer implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=sv-SE) och distribuera en tagg på sina webbplatser. Du kan sedan använda målgrupperna i [!DNL Google Ads] kampanjer som [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) på kampanjnivå eller annonsgruppsnivå.

* Adobe Audience Manager-segment - (anmälningsfunktion) Du kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från Audience Manager-segment som har Sök, Socialt och Commerce som mål. Detta kan omfatta [!DNL Analytics] segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud Audience Library. Du kan sedan använda målgrupperna i [!DNL Google Ads] kampanjer som [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) på kampanjnivå eller annonsgruppsnivå.

  Mer information finns i [Adobe Advertising-integreringar med Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=sv-SE).

* Adobe Target - Du kan implementera klickningsbaserad signaldelning mellan Search, Social och Commerce och [!DNL Target], konfigurera en A/B-testaktivitet i [!DNL Target] för dina annonser och sedan använda [!DNL Analytics] Analysis Workspace för att visa testdata.

* Adobe Campaign - Du kan [skapa och uppdatera en [!DNL Google Ads] kundmatchande målgrupp med hjälp av en e-postlista i [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-meddelanden - (När du är inloggad via Adobe Experience Cloud) Från meddelandelänken ([Varningsmeddelanden](/help/search-social-commerce/assets/notifications-panel.png "Varningsmeddelanden")) högst upp på varje sida kan du visa alla Adobe Experience Cloud-systemuppdateringar, inlägg, omnämnanden och delade resurser. Kontakta Adobe Account Team för att få information om Adobe Experience Cloud.
