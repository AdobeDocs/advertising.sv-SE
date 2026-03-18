---
title: Adobe Advertising-integreringar med Adobe Audience Manager
description: Läs om de olika sätten Adobe Advertising kan utbyta data med Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Adobe Advertising-integreringar med Adobe Audience Manager

Du kan integrera Adobe Advertising med Audience Manager på följande sätt.

## Synkronisera Audience Manager och andra [!DNL Adobe]-segment för annonsinriktning

[!DNL Search, Social, & Commerce] och DSP kan hämta in metadata, hierarkidata och unika målgruppsdata för alla en annonsörs eller agentes Audience Manager och andra [!DNL Adobe] målgrupper. Den här unika anslutningen är bara tillgänglig för marknadsförare som använder Adobe Advertising. Se &quot;[Importera Adobe Audience Manager-segment för annonsmål](/help/integrations/audience-manager/import-audiences.md).&quot;

### Använd Audience Manager och andra [!DNL Adobe]-segment för att skapa [!DNL Google Ads] målgrupper {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Search, Social, & Commerce] only*

Inom [!DNL Search, Social, & Commerce] kan du skapa [!DNL Google Ads] kundmatchande målgrupper från användar-ID:n med dina befintliga Audience Manager-segment som har [!UICONTROL Adobe Media Optimizer (HTTP)] och [!UICONTROL Adobe Media Optimizer Batch Destination] som mål. ([!DNL Media Optimizer] är ett tidigare namn för [!DNL Search, Social, & Commerce].) Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud [!DNL Audience Library]. Mer information finns i &quot;[Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Kunden matchar målgrupper från användar-ID](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII-ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchningar och webbplatstaggbaserade målgrupper.

Om du vill skapa nödvändiga användar-ID:n måste du använda en Adobe Advertising JavaScript-tagg <!-- with a user ID parameter --> på dina webbplatser. Kontakta Adobe Account Team för mer information.

![processen att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads]-kampanjer som [kampanjnivå eller annonsnivå som mål eller undantag](#audience-manager-targets).

### Använd Audience Manager och andra [!DNL Adobe]-segment för att rikta eller exkludera annonser {#audience-manager-targets}

* (Valda annonsörer med [!DNL Search, Social, & Commerce]) Du kan använda alla [!DNL Google Ads] målgrupper som har [skapats med  [!DNL Adobe] segment](#audience-manager-google-audiences) som mål eller undantag på kampanjnivå eller annonsgruppsnivå i dina [!DNL Google Ads]-kampanjer.

* (Annonsörer med DSP) Du kan använda dina befintliga [!DNL Adobe]-segment som mål för dina annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Annonsörer med Advertising Creative) Du kan använda dina befintliga [!DNL Adobe]-segment som mål för specifika kreatörer i dina annonsupplevelser.

>[!NOTE]
>
>Mer information om hur du skapar målgrupper i Audience Manager- och Experience Cloud [!DNL Audience Library]-gränssnitten och vanliga användningsområden för olika målgruppstyper finns i [Alternativ för att skapa målgrupper](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).

## Skicka exponeringsdata för DSP-medier till Audience Manager

*Annonsörer med endast DSP*

DSP-kunder med Adobe Audience Manager kan hämta in data från annonskampanjer med pixelanrop till Audience Manager. Sedan kan ni använda kampanjdata för att bygga regelbaserade egenskaper, som ni kan använda för att definiera nya segment för att möjliggöra olika DSP-användningsfall, som mer avancerad segmentering, frekvenshantering, marknadsföringsanalyser och rapportinsikter.

Mer information finns i [Översikt över hur du skickar exponeringsdata för DSP-medier till Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md).

## Få djupare insikter i webbplatsaktiviteten med Audience Analytics

Adobe Advertising-kunder med [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kan skicka både Adobe Advertising-spårade data och Audience Manager-segment till [!DNL Analytics] för bättre insikter om webbplatsaktiviteten.

Mer information finns i [[!DNL Adobe Audience Analytics] för Adobe Advertising-kunder](/help/integrations/audience-manager/audience-analytics.md).
