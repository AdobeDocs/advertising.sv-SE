---
title: Integrering med Adobe Experience Cloud lösningar och tjänster
description: Läs mer om integrering av sökning, sociala medier och handel med Adobe Experience Cloud lösningar och tjänster.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integrering med Adobe Experience Cloud lösningar och tjänster

Reklamsökning, sociala medier och handel är integrerade med följande [!DNL Adobe] produkter.

* [Taggar från Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Du kan använda [Adobe Advertising Cloud Extension](https://exchange.adobe.com/apps/ec/100155) för att Adobe Experience Platform ska kunna skapa spårningstaggar för Adobe Advertising, liksom spårningstaggar från tredje part, för era annonssidor. (Du kan också [skapa spårningstaggar för konvertering direkt i Sök, Social och Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Kontakta kontogruppen eller implementeringsteamet på Adobe för att få information om hur du tar med dina taggar.

* Adobe Analytics - (anmälningsfunktion) Adobe Advertising och [!DNL Analytics] är integrerade på följande sätt:

   * Adobe Advertising och [!DNL Analytics] dela data smidigt. [!DNL Analytics] kan skicka data om webbplatsengagemang och konvertering dagligen till sökningar, sociala medier och handel, där data är tillgängliga för annonsoptimering och rapportering. Dessutom kan Adobe Advertising skicka annonsdata - inklusive visningar, klickningar och kostnader - från ert annonsnätverk dagligen till [!DNL Analytics], där data är tillgängliga i alla rapporteringsverktyg.

     Se &quot;[Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md)&quot; för mer information om [!DNL Analytics] stöd för varje annonsnätverk och annonstyp. Se även &quot;[Översikt [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; för mer information om datautbytet.

     Att utbyta data, både Adobe Advertising och [!DNL Analytics] måste initialt konfigureras. Kontakta kontoteamet på Adobe om du vill ha mer information om den första konfigurationen.

     >[!NOTE]
     >
     >Som standard är [!DNL Analytics] mätvärden visas inte på skärmar för sökning, sociala medier och handel. Du måste uttryckligen [göra mätvärdena tillgängliga i kampanjhanteringsvyer, portfolior och rapporter](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) efter [!DNL Adobe] implementeringsteamet har konfigurerat utvalda standard- eller anpassade händelser som ska skickas till Adobe Advertising. Du kan ändra de måttnamn som visas (utan att ändra dem i [!DNL Analytics]). Du kan göra mätvärden synliga i användargränssnittet och ändra namn på mätvärden från [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * Annonsörer med [!DNL Analytics] men inte Audience Manager kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från [!DNL Analytics] segment som delas med Adobe Experience Cloud. För att vara berättigad måste annonsören implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) och distribuera en tagg på sina webbplatser. Sedan kan du använda målgrupperna i [!DNL Google Ads] kampanjer på kampanjnivå eller annonsgruppnivå [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager segment - (anmäl dig) Du kan [skapa [!DNL Google Ads] kundmatchande målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) från Audience Manager-segment som har Sök, Social och Commerce som mål. Detta kan omfatta [!DNL Analytics] segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud Audience Library. Sedan kan du använda målgrupperna i [!DNL Google Ads] kampanjer på kampanjnivå eller annonsgruppnivå [mål](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) eller [undantag](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Se &quot;[Integrering av Adobe Advertising med Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; för mer information.

* Adobe Target - Du kan implementera klickbar signaldelning mellan Search, Social och Commerce och [!DNL Target], konfigurera en A/B-testaktivitet i [!DNL Target] för era annonser och sedan använda [!DNL Analytics] Analysis Workspace för att visa testdata.

* Adobe Campaign - du kan [skapa och uppdatera en [!DNL Google Ads] kundmatchande målgrupp med hjälp av en e-postlista i [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud Notifications - (When you are logged in through Adobe Experience Cloud) From the notifications link ([Varningsmeddelanden](/help/search-social-commerce/assets/notifications-panel.png "Varningsmeddelanden")) högst upp på varje sida kan du visa alla systemuppdateringar, meddelanden, omnämnanden och delade resurser för Adobe Experience Cloud. Kontakta kontoteamet på Adobe för information om åtkomst till Adobe Experience Cloud.
