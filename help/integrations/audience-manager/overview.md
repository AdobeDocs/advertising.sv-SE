---
title: Integrering av Adobe Advertising med Adobe Audience Manager
description: Läs om de olika sätten som Adobe Advertising kan använda för att utbyta data med Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Integrering av Adobe Advertising med Adobe Audience Manager

Du kan integrera Adobe Advertising med Audience Manager på följande sätt.

## Synkronisera Audience Manager och andra [!DNL Adobe]-segment för annonsinriktning

[!DNL Search, Social, & Commerce] och DSP kan hämta in metadata, hierarkidata och unika målgruppsdata för alla Audience Manager och andra [!DNL Adobe]-målgrupper hos en annonsörer eller byrå. Den här unika anslutningen är bara tillgänglig för marknadsförare som använder Adobe Advertising. Se &quot;[Importera Adobe Audience Manager-segment för annonsinriktning](/help/integrations/audience-manager/import-audiences.md).&quot;

### Skapa [!DNL Google Ads Audiences] med Audience Manager och andra [!DNL Adobe]-segment {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Search, Social, & Commerce] only*

Inom [!DNL Search, Social, & Commerce] kan du skapa [!DNL Google Ads] kundmatchande målgrupper från användar-ID:n med dina befintliga Audience Manager-segment som har [!UICONTROL Adobe Media Optimizer (HTTP)] och [!UICONTROL Adobe Media Optimizer Batch Destination] som mål. ([!DNL Media Optimizer] är ett tidigare namn för [!DNL Search, Social, & Commerce].) Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud [!DNL Audience Library]. Mer information finns i &quot;[Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Kunden matchar målgrupper från användar-ID](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII-ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchningar och webbplatstaggbaserade målgrupper.

Om du vill skapa nödvändiga användar-ID:n måste du använda en Adobe Advertising JavaScript-tagg <!-- with a user ID parameter --> på dina webbplatser. Kontakta kontoteamet på Adobe för mer information.

![processen att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads]-kampanjer som [kampanjnivå eller annonsnivå som mål eller undantag](#audience-manager-targets).

### Använd Audience Manager och andra [!DNL Adobe]-segment för att rikta eller exkludera annonser {#audience-manager-targets}

* (Valda annonsörer med [!DNL Search, Social, & Commerce]) Du kan använda alla [!DNL Google Ads] målgrupper som har [skapats med  [!DNL Adobe] segment](#audience-manager-google-audiences) som mål eller undantag på kampanjnivå eller annonsgruppsnivå i dina [!DNL Google Ads]-kampanjer.

* (Annonsörer med DSP) Du kan använda dina befintliga [!DNL Adobe]-segment som mål för dina annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Annonsörer med Advertising Creative) Du kan använda dina befintliga [!DNL Adobe]-segment som mål för specifika kreatörer i dina annonsupplevelser.

>[!NOTE]
>
>Mer information om hur du skapar målgrupper i Audience Manager och Experience Cloud [!DNL Audience Library]-gränssnitten och vanliga användningsområden för olika målgruppstyper finns i [Alternativ för att skapa målgrupper](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).

## Skicka DSP data för medieexponering till Audience Manager

*Annonsörer med endast DSP*

DSP kunder med Adobe Audience Manager kan hämta in data från annonskampanjer med pixelanrop till Audience Manager. Sedan kan ni använda kampanjdata för att bygga regelbaserade egenskaper, som ni kan använda för att definiera nya segment för att möjliggöra olika DSP, som mer avancerad segmentering, frekvenshantering, marknadsföringsanalyser och rapportinsikter.

Mer information finns i [Översikt över att skicka DSP medieexponeringsdata till Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md).

## Få djupare insikter om webbplatsaktivitet med Audience Analytics

Adobe Advertising-kunder med [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kan skicka både data som spårats i Adobe Advertising och segment i Audience Manager till [!DNL Analytics] för att få bättre insikter om webbplatsaktiviteten.

Mer information finns i &quot;[[!DNL Adobe Audience Analytics] for Adobe Advertising Customers](/help/integrations/audience-manager/audience-analytics.md)&quot;.
