---
title: Vanliga frågor om taggar för annonskonvertering och spårning av sidvy i Adobe
description: Se en jämförelse av spårningstaggar för annonskonvertering i Adobe och sidvy.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Vanliga frågor om taggar för annonskonvertering och spårning av sidvy i Adobe

Följande gäller taggar för konverteringsspårning och spårning av sidvy i Adobe.

|  | JS-taggar med ECID | JS version 3-taggar | JS version 2-taggar | Bildtaggar |
| ---- | ---- | ---- | ---- | ---- |
| Kan användas på samma webbsida som en annan JS-version | — | — | — | n/a |
| Tillåter användning av flera taggar med samma annonsörs-ID på samma webbsida | Ja | Ja | Ja | — |
| Tillåter användning av flera taggar med olika användar-ID för annonsörer på samma webbsida | Ja | Ja | Nej | Nej |
| Används av Adobe Advertising-tillägget för Adobe Experience Platform och är kompatibelt med andra taggar som genererats med Experience Platform | Ja | Ja | — | — |
| Tillåter alla konverteringar som kommer från [!DNL Apple Safari] och [!DNL Mozilla Firefox] som ska spåras när den används med konverteringstaggen för JavaScript-konvertering i Adobe | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alla nya implementeringar använder JavaScript version 3.
>* JavaScript-taggen med ECID använder [Tjänsten Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) samt den gamla ef_id och gsurferid som mäter konverteringar. Den senaste taggen skapar [cookies från första part i Experience Cloud s_ecid](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) och ger bättre integrering med andra Experience Cloud-produkter.
>* Använd JavaScript version 2-taggar endast när de redan är implementerade taggar på annonsörens webbsidor.
>* Det bästa sättet är att använda JavaScript-taggar i stället för bildtaggar, såvida inte webbplatsen har en policy som förhindrar att de används.
>* JavaScript-taggar krävs för annonsörer som vill rikta sig till målgrupper som skapats i Adobe Experience Cloud, skapats i Adobe Audience Manager eller publicerats i Adobe Experience Cloud från Audience Manager eller Adobe Analytics.


>[!MORELIKETHIS]
>
>* [Om konverteringsspårningstaggar för Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](/help/search-social-commerce/tracking/format-conversion-tag-image.md)


<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
