---
title: Format för JavaScript-konverteringstaggar, version 3
description: Referera formatet för JavaScript-konverteringstaggar, version 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: 8bed8f22c112abcff67727456ef4aad3b38d0ca6
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Format för JavaScript-konverteringstaggar, version 3

Följande format gäller för webbplatser som använder HTTPS. För webbplatser som använder HTTP bör URL:erna börja med &quot;http&quot;.

>[!NOTE]
>
>Mer information om när version 2 och version 3 ska användas finns i [Vanliga frågor och svar om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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
        window.id5PartnerId=<Your_ID5_PartnerID>
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

* `<Your_ID5_PartnerID>` är organisationens ID5-partner-ID, som organisationen får efter att ha signerat ett avtal med [!DNL ID5]. Inkludera endast den här variabeln när organisationen använder DSP och har [anpassade segment som spårar användare som är kopplade till universella ID:n för ID5](/help/dsp/audiences/universal-ids.md).

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
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)
