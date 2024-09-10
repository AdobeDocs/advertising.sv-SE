---
title: Format för JavaScript konverteringsspårningstaggar, version 2
description: Referera formatet för JavaScript-konverteringstaggar, version 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: f73e91c54fb58cbd165ddf4ca652033435fbbede
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Format för JavaScript konverteringsspårningstaggar, version 2

Följande format gäller för webbplatser som använder HTTPS. För webbplatser som använder HTTP bör URL:erna börja med &quot;http&quot;.

>[!NOTE]
>
>Mer information om när version 2 och version 3 ska användas finns i [Vanliga frågor och svar om spårningstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<Your_ID5_PartnerID>
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
>* [Format för JavaScript-konverteringstaggar, version 3](format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)
