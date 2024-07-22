---
title: Format för spårningstaggar för bildkonvertering
description: Referera formatet för spårningstaggar för bildkonvertering.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format för spårningstaggar för bildkonvertering

>[!NOTE]
>
>Mer information om när du ska använda bildtaggar jämfört med JavaScript-taggar finns i [Vanliga frågor och svar om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Osäkra taggar för webbplatser med HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Säkra taggar för webbplatser med HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

där:

* `<ef-userid>` är ett unikt, numeriskt användar-ID som tilldelas annonsören av Search, Social och Commerce.

* `<propertyname>` är konverteringen som ska spåras. Om du till exempel spårar en konvertering som kallas registrering, kommer taggen att innehålla parametern `ev_registration=<registration>` och du måste skicka den faktiska intäkten för varje transaktion (till exempel `ev_registration=1`). När flera egenskaper spåras förenas de med ett et-tecken (`&`), till exempel `ev_registration=<registration>&ev_sale=<sale>` (till exempel `ev_registration=1&ev_sale=12.99`). **Obs!** Egenskapsnamnet får inte innehålla specialtecken.

* `<transid>` är ett unikt transaktions-ID (till exempel ett faktiskt order-ID) som annonsören genererar och skickar för att identifiera en transaktion. Det inkluderas bara när alternativet [!UICONTROL Include unique transaction IDs] har valts.

  För Search, Social och Commerce används transaktions-ID:t för att eliminera dubbletttransaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t ingår i [!UICONTROL Transaction Report], som du kan använda för att validera data i Adobe Advertising med annonsörens data. **Obs!** Om annonsörens data inte innehåller ett unikt ID per transaktion genererar Search, Social och Commerce fortfarande ett baserat på transaktionstid.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Om Adobe Advertising-taggar för konvertering/spårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Frågor och svar om spårningstaggar för konvertering och sidvisning](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för JavaScript-konverteringstaggar, version 2](format-conversion-tag-jsv2.md)
>* [Format för JavaScript-konverteringstaggar, version 3](format-conversion-tag-jsv3.md)
