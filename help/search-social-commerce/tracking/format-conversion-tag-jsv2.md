---
title: Format för spårningstaggar för JavaScript-konvertering, version 2
description: Referera formatet för spårningstaggar för JavaScript-konvertering version 2.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Format för spårningstaggar för JavaScript-konvertering, version 2

Följande format gäller för webbplatser som använder HTTPS. För webbplatser som använder HTTP bör URL:erna börja med &quot;http&quot;.

>[!NOTE]
>
>Information om när version 2 och version 3 ska användas finns i [Vanliga frågor om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

där:

* `<ef-userid>` är ett unikt, numeriskt användar-ID som tilldelas annonsören av Search, Social och Commerce.

* `<propertyname>` är konverteringen som spåras. Om du till exempel spårar en konvertering som kallas &quot;registrering&quot;, kommer taggen att innehålla parametern `ev_registration=<registration>`och du måste överföra de faktiska intäkterna för varje transaktion (till exempel `ev_registration=1`). När flera egenskaper spåras sammanfogas de av ett et-tecken (`&`), till exempel `ev_registration=<registration>&ev_sale=<sale>` (t.ex. `ev_registration=1&ev_sale=12.99`). **Obs!**  Egenskapsnamnet får inte innehålla specialtecken.

* `<transid>` är ett unikt transaktions-ID (t.ex. ett faktiskt order-ID) som annonsören genererar och skickar för att identifiera en transaktion. Den inkluderas endast när[!UICONTROL Include unique transaction IDs]&quot; är valt.

   I Sök, Socialt och Commerce används transaktions-ID:t för att ta bort dubbletter av transaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t ingår i [!UICONTROL Transaction Report], som ni kan använda för att validera data i Adobe Advertising med annonsörens data. **Obs!** Om annonsörens data inte innehåller ett unikt ID per transaktion genereras ändå ett baserat på transaktionstid av Search, Social och Commerce.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Om konverteringsspårningstaggar för Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 2](format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)

