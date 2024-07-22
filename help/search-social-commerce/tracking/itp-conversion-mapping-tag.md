---
title: Adobe Advertising-konverteringstaggen
description: Lär dig mer om den JavaScript-baserade konverteringstaggen för ITP 2.2, som gör att Adobe Advertising kan spåra en konverteringshändelse som inträffar på en sida som inte är landningssidan.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Konverteringstaggen Adobe Advertising JavaScript

*Annonsörer med endast Adobe Advertising-konverteringsspårning*

Med den Adobe Advertising JavaScript-baserade konverteringsmappningstaggen kan Adobe Advertising spåra konverteringshändelser som inträffar på en sida som inte är landningssidan, utöver taggen Adobe Advertising JavaScript v2 eller v3 för konverteringsspårning. ITP 2.2-lösningen lagrar en användares cookie i lokal lagring i en annonsörägd iFrame. Lokal lagring kan sedan behålla cookie-värdet från klickningen nedåt till konverteringssidan.

Använd taggen för konverteringsmappning för att se till att Adobe Advertising kan spåra alla konverteringar som sker i webbläsarna Apple Safari och Mozilla Firefox, vilket begränsar beständigheten hos cookies från första part. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

Så här använder du konverteringsmappningstaggen:

1. [Distribuera konverteringsmappningstaggen](#deploy-conversion-mapping-tag).

1. Om din organisation använder flera Adobe Experience Cloud Identity Service-organisations-ID:n (kallades tidigare IMS-organisations-ID:n) [uppdaterar du dina konverteringstaggar](#update-conversion-tags) så att de innehåller organisations-ID:t.

1. [Verifiera taggdistributionen](#validate-conversion-mapping).

## Distribuera JavaScript konverteringstagg för ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Om du använder konverteringstaggen för JavaScript för ITP 2.0 ska du ersätta den befintliga taggen på alla konverteringssidor med någon av följande taggar.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Om din organisation använder ett enda organisations-ID, som används för ditt Search-, Social- och Commerce-konto, använder du följande tagg:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  där du ersätter `{AMO User ID}` med det unika användar-ID:t för ditt Search-, Social- och Commerce-konto.

* Om din organisation använder flera organisations-ID:n använder du följande tagg:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  där:

   * du ersätter värdet `{xxxxxx@AdobeOrg}` med organisations-ID:t som sidans konverteringar spåras för. Använd samma organisations-ID för alla konverteringssidor.

   * du ersätter `{AMO User ID}` med det unika användar-ID:t för ditt Search-, Social- och Commerce-konto.

* Om du använder ett tagghanteringssystem som inte har stöd för att lägga till variabeln `imsorgid` i skripttaggen ska du använda följande kod i stället:

  *Om din organisation använder ett enda organisations-ID:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  där du ersätter `{AMO User ID}` med det unika användar-ID:t för ditt Search-, Social- och Commerce-konto.

   * Om din organisation använder flera organisations-ID:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     där:

      * du ersätter värdet `{xxxxxx@AdobeOrg}` med organisations-ID:t som sidans konverteringar spåras för. Använd samma organisations-ID för alla konverteringssidor.

      * du ersätter `{AMO User ID}` med det unika användar-ID:t för ditt Search-, Social- och Commerce-konto.

Om du inte känner till värdet på ditt företags-ID eller ditt användar-ID för sökningar, sociala medier och Commerce frågar du din kontoansvarige på Adobe.

### Exempel

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Var ska taggen läggas till?

Lägg till taggen på en sida som kan vara en landningssida från ett sökklick (helst på alla sidor, eftersom landningssidorna kan ändras över tid). Den måste läsas in före konverteringstaggen för JavaScript v3 i Adobe Advertising.

Om den är placerad i en iframe- eller container-tagg:

* iframe-domänen bör ligga på samma nivå som domänen på den översta nivån.

* Konverteringsmappningstaggen får bara vara en (1) nivå under domänen på den översta nivån.

## Uppdatera dina JavaScript-konverteringstaggar {#update-conversion-tags}

Om din organisation använder flera organisations-ID:n lägger du till det organisations-ID för vilket en sidas konverteringar spåras till dina befintliga JavaScript-konverteringstaggar.

Om din organisation använder ett organisations-ID är det här steget inte nödvändigt.

### JavaScript V2-taggar

Lägg till följande sträng i början av konverteringsskripttaggen:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

där du ersätter värdet `{xxxxxx@AdobeOrg}` med organisations-ID:t som sidans konverteringar spåras för.

Exempel:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### JavaScript V3-taggar

När `window.EF` har definierats lägger du till följande sträng:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

där du ersätter värdet `{xxxxxx@AdobeOrg}` med organisations-ID:t som sidans konverteringar spåras för.

Exempel:

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
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## Validera taggdistributionen {#validate-conversion-mapping}

Be ditt kontoteam på Adobe om hjälp med att validera konverteringstaggen och den vanliga konverteringstaggen (om du har uppdaterat den).
