---
title: Integrering av Adobe Advertising med Adobe Analytics
description: Lär dig mer om hur Adobe Advertising kan utbyta data med Adobe Analytics och hur du kan använda data i sökningar, sociala medier och handel.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integrering av Adobe Advertising med Adobe Analytics

Du kan integrera Adobe Advertising med Analytics på följande sätt.

## Utbyt data mellan [!DNL Analytics] och Adobe Advertising

### Dra [!DNL Analytics] Data till Adobe Advertising

Med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] och DSP in:

* **[!DNL Analytics]segment:**  Metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers segment som skapats i [!DNL Analytics] och publiceras i Experience Cloud.

* **[!DNL Analytics]mått för webbplatsengagemang**

* **[!DNL Analytics]standardvärden, anpassade värden och reserverade värden**

### Skicka Adobe Advertising-data till [!DNL Analytics]

* **Trafikstatistik från Adobe Advertising**

* **Dimensioner från Adobe Advertising**

>[!NOTE]
>
>För [!DNL Search, Social, & Commerce], stöds den här funktionen för de flesta annonsnätverk och kampanjtyper. Se&quot;Supported Inventory&quot; i [!DNL Search, Social, & Commerce] Guide för mer information.<!-- add link when that's published in ExL -->

### Använd [!DNL Analytics] Segment att skapa [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Search, Social, & Commerce] endast*

<!-- Verify all -->

Inom [!DNL Search, Social, & Commerce]kan du skapa [!DNL Google Ads] Google kund matchar målgrupper från användar-ID:n med era befintliga [!DNL Analytics] segment. Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud [!DNL Audience Library]. Mer information finns i &quot;[Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Kunden matchar målgrupper från användar-ID:n](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchning och taggbaserade målgrupper för webbplatser.

Om du vill skapa nödvändiga användar-ID:n måste du använda en JavaScript-tagg i Adobe Advertising <!-- with a user ID parameter -->på era webbplatser. Kontakta kontoteamet på Adobe för mer information.

![process för att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads] kampanjer som [mål eller undantag på kampanjnivå eller annonsnivå](#audience-manager-targets).

### Använd [!DNL Analytics] Segment att rikta eller exkludera annonser {#analytics-targets}

* (Valda annonsörer med [!DNL Search, Social, & Commerce]) Du kan använda valfritt [!DNL Google Ads] målgrupper som [skapad med [!DNL Analytics] segment](#audience-manager-google-audiences) som kampanjnivå eller annonsnivå som mål eller undantag i er [!DNL Google Ads] kampanjer.

* (Annonsörer med DSP) Du kan använda dina befintliga [!DNL Analytics] segment som mål för era annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Annonsörer med Advertising Creative) Du kan använda dina befintliga [!DNL Analytics] segment som mål för specifika kreatörer i era annonsupplevelser.
