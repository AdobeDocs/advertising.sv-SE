---
title: Adobe Advertising-integreringar med Adobe Analytics
description: Läs om hur Adobe Advertising kan utbyta data med Adobe Analytics och hur du kan använda data i Search, Social och Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe Advertising-integreringar med Adobe Analytics

Du kan integrera Adobe Advertising med Analytics på följande sätt.

## Utbyt data mellan [!DNL Analytics] och Adobe Advertising

### Hämta [!DNL Analytics]-data till Adobe Advertising

Med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] och DSP in:

* **[!DNL Analytics]segment:** Metadata, hierarkidata och unika målgruppsdata för alla en annonsörs- eller agentsegment som skapats i [!DNL Analytics] och publicerats till Experience Cloud.

* **[!DNL Analytics]mått för webbplatsengagemang**

* **[!DNL Analytics]standardvärden, anpassade värden och reserverade värden**

### Skicka Adobe Advertising-data till [!DNL Analytics]

* **Trafikstatistik från Adobe Advertising**

* **Dimensioner från Adobe Advertising**

>[!NOTE]
>
>För [!DNL Search, Social, & Commerce] stöds den här funktionen för de flesta annonsnätverk och kampanjtyper. Mer information finns i &quot;Supported Inventory&quot; i [!DNL Search, Social, & Commerce]-handboken.<!-- add link when that's published in ExL -->

### Använd [!DNL Analytics] segment för att skapa [!DNL Google Ads] målgrupper {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Inom [!DNL Search, Social, & Commerce] kan du skapa [!DNL Google Ads] Google kundmatchningar från användar-ID:n med dina befintliga [!DNL Analytics]-segment. Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud [!DNL Audience Library]. Mer information finns i &quot;[Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Kunden matchar målgrupper från användar-ID](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII-ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchningar och webbplatstaggbaserade målgrupper.

Om du vill skapa nödvändiga användar-ID:n måste du använda en Adobe Advertising JavaScript-tagg <!-- with a user ID parameter --> på dina webbplatser. Kontakta Adobe Account Team för mer information.

![processen att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads]-kampanjer som [kampanjnivå eller annonsnivå som mål eller undantag](#audience-manager-targets).

### Använd [!DNL Analytics] segment för att rikta eller exkludera annonser {#analytics-targets}

* (Valda annonsörer med [!DNL Search, Social, & Commerce]) Du kan använda alla [!DNL Google Ads] målgrupper som har [skapats med  [!DNL Analytics] segment](#audience-manager-google-audiences) som mål eller undantag på kampanjnivå eller annonsgruppsnivå i dina [!DNL Google Ads]-kampanjer.

* (Annonsörer med DSP) Du kan använda dina befintliga [!DNL Analytics]-segment som mål för dina annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Annonsörer med Advertising Creative) Du kan använda dina befintliga [!DNL Analytics]-segment som mål för specifika kreatörer i dina annonsupplevelser.
