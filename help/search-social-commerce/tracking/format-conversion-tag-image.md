---
title: Format för spårningstaggar för bildkonvertering
description: Referera formatet för spårningstaggar för bildkonvertering.
source-git-commit: b230c593d93dfa868b8f075939fc9940ea74fa13
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format för spårningstaggar för bildkonvertering

>[!NOTE]
>
>Mer information om när du ska använda bildtaggar jämfört med JavaScript-taggar finns i [Vanliga frågor om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Osäkra taggar för webbplatser med HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Säkra taggar för webbplatser med HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

där:

* `<ef-userid>` är ett unikt, numeriskt användar-ID som tilldelas annonsören av Search, Social och Commerce.

* `<propertyname>` är konverteringen som spåras. Om du till exempel spårar en konvertering som kallas &quot;registrering&quot;, kommer taggen att innehålla parametern `ev_registration=<registration>`och du måste överföra de faktiska intäkterna för varje transaktion (till exempel `ev_registration=1`). När flera egenskaper spåras sammanfogas de av ett et-tecken (`&`), till exempel `ev_registration=<registration>&ev_sale=<sale>` (t.ex. `ev_registration=1&ev_sale=12.99`). **Obs!**  Egenskapsnamnet får inte innehålla specialtecken.

* `<transid>` är ett unikt transaktions-ID (t.ex. ett faktiskt order-ID) som annonsören genererar och skickar för att identifiera en transaktion. Den inkluderas endast när[!UICONTROL Include unique transaction IDs]&quot; är valt.

  I Sök, Socialt och Commerce används transaktions-ID:t för att ta bort dubbletter av transaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t ingår i [!UICONTROL Transaction Report], som du kan använda för att validera data i Adobe Advertising med annonsörens data. **Obs!** Om annonsörens data inte innehåller ett unikt ID per transaktion genereras ändå ett baserat på transaktionstid av Search, Social och Commerce.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Om konverteringsspårningstaggar för Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 2](format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](format-conversion-tag-jsv3.md)
