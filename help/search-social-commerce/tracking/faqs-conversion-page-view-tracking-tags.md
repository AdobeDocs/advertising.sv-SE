---
title: Frågor och svar om spårningstaggar för Adobe Advertising och sidvisning
description: Se en jämförelse av spårningstaggar för sidkonvertering och sidvisning i Adobe Advertising.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Frågor och svar om spårningstaggar för Adobe Advertising och sidvisning

Följande gäller spårningstaggar för konvertering av Adobe Advertising och spårningstaggar för sidvisning.

| | JS-taggar med ECID | JS version 3-taggar | JS version 2-taggar | Bildtaggar |
| ---- | ---- | ---- | ---- | ---- |
| Kan användas på samma webbsida som en annan JS-version | — | — | — | n/a |
| Tillåter användning av flera taggar med samma annonsörs-ID på samma webbsida | Ja | Ja | Ja | — |
| Tillåter användning av flera taggar med olika användar-ID för annonsörer på samma webbsida | Ja | Ja | — | — |
| Används av tillägget Adobe Advertising för Adobe Experience Platform och är kompatibelt med andra taggar som genererats med Experience Platform | Ja | Ja | — | — |
| Tillåter att alla konverteringar som kommer från [!DNL Apple Safari] och [!DNL Mozilla Firefox] spåras när de används med konverteringstaggen för Adobe Advertising JavaScript | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alla nya implementeringar använder JavaScript version 3.
>* JavaScript-taggen med ECID använder [Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) samt den äldre ef_id och gsurferid för att mäta konverteringar. Den senaste taggen skapar [cookies från första part från Experience Cloud s_ecid](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) och ger bättre integrering med andra Experience Cloud-produkter.
>* Använd JavaScript version 2-taggar endast när de redan är implementerade taggar på annonsörens webbsidor.
>* Det bästa sättet är att använda JavaScript-taggar i stället för bildtaggar, såvida inte webbplatsen har en policy som förhindrar att de används.
>* JavaScript-taggar krävs för annonsörer som vill rikta sig till målgrupper som skapats i Adobe Experience Cloud, skapats i Adobe Audience Manager eller publicerats i Adobe Experience Cloud från Audience Manager eller Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Om Adobe Advertising-taggar för konvertering/spårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format för JavaScript-konverteringstaggar, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format för JavaScript-konverteringstaggar, version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
