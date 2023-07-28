---
title: Format för spårningstaggar för JavaScript-konvertering, version 3
description: Referera formatet för spårningstaggar för JavaScript-konvertering version 3.
exl-id: 1e177c52-f93c-4800-afb5-28f2336117b9
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Format för spårningstaggar för JavaScript-konvertering, version 3

Följande format gäller för webbplatser som använder HTTPS. För webbplatser som använder HTTP bör URL:erna börja med &quot;http&quot;.

>[!NOTE]
>
>Information om när version 2 och version 3 ska användas finns i [Vanliga frågor om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

där:

* `<ef-userid>` är ett unikt, numeriskt användar-ID som tilldelas annonsören av Search, Social och Commerce.

* `<propertyname>` är konverteringen som spåras. Om du till exempel spårar en konvertering som kallas &quot;registrering&quot;, kommer taggen att innehålla parametern `ev_registration=<registration>`och du måste överföra de faktiska intäkterna för varje transaktion (till exempel `ev_registration=1`). När flera egenskaper spåras sammanfogas de av ett et-tecken (`&`), till exempel `ev_registration=<registration>&ev_sale=<sale>` (till exempel `ev_registration=1&ev_sale=12.99`). **Obs!**  Egenskapsnamnet får inte innehålla specialtecken.

* `<transid>` är ett unikt transaktions-ID (t.ex. ett faktiskt order-ID) som annonsören genererar och skickar för att identifiera en transaktion. Den inkluderas endast när[!UICONTROL Include unique transaction IDs]&quot; är valt.

  I Sök, Socialt och Commerce används transaktions-ID:t för att ta bort dubbletter av transaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t ingår i [!UICONTROL Transaction Report], som du kan använda för att validera data i Adobe Advertising med annonsörens data. **Obs!** Om annonsörens data inte innehåller ett unikt ID per transaktion genereras ändå ett baserat på transaktionstid av Search, Social och Commerce.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Om taggar för Adobe Advertising-konverteringsspårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generera en konverteringstagg för Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för spårningstaggar för JavaScript-konvertering version 2](format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)
