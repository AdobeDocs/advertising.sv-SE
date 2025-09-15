---
title: Nyheter
description: Läs om uppdateringar av integreringar mellan Adobe Advertising och andra produkter och tjänster i Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: 5025b135385c2e1fc7a026aa4cb6489765f0d34c
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Nyheter

Följande funktioner är nya eller nyligen ändrade.

| Datum | Funktion | Beskrivning | Mer information |
| ---- | ------- | ----------- | -------------------- |
| 8 september 2025 | Integrering med Customer Journey Analytics | (Beta-funktion) Annonsörer med Customer Journey Analytics, men inte [!DNL Analytics for Advertising], kan nu utbyta data mellan Adobe Advertising och Customer Journey Analytics med [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=sv-SE). | Se &quot;[Översikt över integrationen mellan Adobe Advertising och Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).&quot; |
| 26 mars 2025 | [!DNL Adobe Analytics for Advertising] | (Annonsörer med Search, Social, &amp; Commerce, [!DNL Microsoft Advertising]-konton och [!DNL Adobe Analytics for Advertising]) För konton med spårningsalternativet [!UICONTROL Auto Upload] uppdaterades formatet för AMO ID-parametern i landningssidans suffix för alla kampanjtyper till det senaste formatet. Tidigare migrerades maximala prestandakampanjer för de flesta konton till det nya formatet.<br><br>För konton utan spårningsalternativet [!UICONTROL Auto Upload] som inte redan har migrerats till det nya formatet måste du uppdatera varje landningssidessuffix manuellt så att det nya AMO-ID-formatet inkluderas.<br><br>Aktuellt format: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Se &quot;[Översikt över [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot; och [AMO ID-format](/help/integrations/analytics/ids.md#amo-id-formats).&quot; |
| 13 november 2024 | [!DNL Analytics for Advertising] | (Annonsörer med [!DNL Analytics for Advertising] och Adobe Customer Journey Analytics) Om du använder reserverade variabler för att hämta AMO-ID:n och EF-ID:n kan du förbereda dig för en framtida integrering mellan Adobe Advertising och Adobe Customer Journey Analytics genom att kopiera dina reserverade variabler för AMO-ID:t och EF-ID:t till standard [!DNL eVars] så snart som möjligt. Detta gör det möjligt att samla in historiska data för AMO-ID:n och EF-ID:n så snart du har slutfört uppgiften, och historiska data blir tillgängliga för framtida bruk. Kontoteamet på Adobe meddelar dig om du använder reserverade variabler och behöver slutföra den här uppgiften. | Se &quot;[Samla in historiska data för AMO-ID:n och EF-ID:n för användning i Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).&quot; |
| Utgiven 29 oktober 2024 | [!DNL Adobe Analytics for Advertising] | (Annonsörer med [!DNL Adobe Analytics for Advertising] och [!DNL Microsoft Advertising] maximala prestandakampanjer) Data på resursgruppsnivå för era maximala prestandakampanjer är nu tillgängliga i Adobe Analytics när du implementerar en ny AMO ID-parameter ([!DNL s_kwcid]) i spårnings-URL:erna för era maximala prestandakampanjer, som inte innehåller annonser och nyckelord. Spårning för de flesta konton med maximala prestandakampanjer har redan migrerats till det nya formatet. För konton med maximala prestandakampanjer utan alternativet [!UICONTROL Auto Upload] för spårning som inte redan har migrerats till det nya formatet måste du uppdatera varje landningssidessuffix manuellt så att det nya AMO-ID-formatet inkluderas.<br><br>Adobe Analytics-data för maximala prestandakampanjer finns även i Search, Social och Commerce. | Se det nya [AMO ID-formatet](/help/integrations/analytics/ids.md#amo-id-formats) och [när och hur du lägger till parametern i spårnings-URL:erna](/help/integrations/analytics/ids.md#amo-id-implement). |
| 16 december 2023 | Hjälp | I ett nytt dokument förklaras hur du konfigurerar A/B-tester i [!DNL Target] för klickbar trafik från annonser i Sök, Social och Commerce, samt tips om hur du mäter och visualiserar dina tester i [!DNL Analytics]. | Se &quot;[Konfigurera A/B-tester i Adobe Target för sök-, sociala och Commerce-annonser](/help/integrations/target/ab-tests-search.md).&quot; |
| 8 augusti 2023 | [!DNL Analytics for Advertising] | Vissa [!DNL Analytics] framgångsmått, inklusive standardvärden, anpassade värden och reserverade konverteringsvärden och trafikvärden, är automatiskt tillgängliga i DSP och i Search, Social och Commerce. Nu kan du även konfigurera egna framgångsmått baserat på dina befintliga [!DNL Analytics] [!DNL eVars] och [!DNL props] genom att samla data på [!DNL eVar] - och [!DNL prop]-nivå i en anpassad success-händelse. | Se [Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md). |
| 13 juli 2023 | Rapportering | (DSP-användare med [!DNL Analytics for Advertising]) Vykonverteringar för anslutna TV-apparater (CTV) ingår nu i konverteringsdata som är tillgängliga i Adobe Analytics. | Se avsnittet &quot;Exempel på hur du använder integreringen&quot; i &quot;[Översikt över [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| 1 november 2022 | Hjälp | I ett nytt dokument beskrivs hur du implementerar klicknings- och genomskinlighetssignaldelning mellan Advertising DSP och Adobe Target, konfigurerar en A/B-testaktivitet i [!DNL Target] för dina DSP-annonser och hur du konfigurerar Adobe Analytics Analysis Workspace för att visa testdata. | Se &quot;[Konfigurera A/B-tester i Adobe Target för Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md).&quot; |
| 17 augusti 2022 | Hjälp | I ett nytt kapitel förklaras alla sätt som Adobe Advertising är integrerat med Adobe Audience Manager på. | Se kapitlet om&quot;Integrering med Adobe Audience Manager&quot;, inklusive en översikt över &quot;[Adobe Advertising Integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| 27 april 2021 | [!DNL Analytics for Advertising] | Lär dig varför och hur du lägger till [!DNL Analytics for Advertising]-makron i dina [!DNL Google Campaign Manager 360] -annonstaggar för att skicka klickdata till Adobe Analytics. | Se &quot;[Lägg till [!DNL Analytics for Advertising] makron i [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;. |
| 19 april 2021 | [!DNL Analytics for Advertising] | Lär dig varför och hur du lägger till makron i dina [!DNL Flashtalking]-annonstaggar för att skicka klickdata till Adobe Analytics. | Se &quot;[Lägg till [!DNL Analytics for Advertising] makron i [!DNL Flashtalking] Lägg till taggar](/help/integrations/analytics/macros-flashtalking.md)&quot;. |
| 27 oktober 2021 | [!DNL Analytics for Advertising] | Om din organisation vill växla från att använda det gamla Adobe Analytics `visitorAPI.js`-biblioteket till [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=sv-SE)-biblioteket (`alloy.js`) för datainsamling, måste du göra några ändringar för att aktivera ID-sammanfogning. | Se [Använda  [!DNL Last Event Service] JavaScript-biblioteket med Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md). |
| 26 maj 2021 | Hjälp | Kapitlet [!DNL Analytics for Advertising] innehåller nu ett underkapitel om Arbeta i [!DNL Analytics Marketing Channels]. | Se: &quot;[Grundläggande om marknadsföringskanaler](/help/integrations/analytics/marketing-channels/mc-overview.md)&quot; [Använda Adobe Advertising-id:n för att skapa [!DNL Analytics Marketing Channels] bearbetningsregler](/help/integrations/analytics/marketing-channels/mc-ids.md)&quot;, &quot;[Använda [!DNL Analytics Marketing Channels] med Adobe Advertising-data](/help/integrations/analytics/marketing-channels/mc-ac-data.md)&quot; och &quot;[Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md).&quot; |
| 26 maj 2021 | Hjälp | En länk till alla videokurser om [!DNL Analytics for Advertising] har lagts till. | Se: &quot;[Videosjälvstudiekurser om Adobe Advertising-integreringar](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=sv-SE).&quot; |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
