---
title: HTML5 - kreativ specifikation
description: Se den kreativa specifikationen för HTML5 för Advertising Creative.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# HTML5 creative specification for Advertising Creative

Det här dokumentet innehåller en översikt över kraven och API-stödet för HTML5-användare inom [!DNL Creative]. API:t gör det möjligt att utveckla HTML5-kreatörer vars attribut kan konfigureras när de distribueras.

## Omfång

[!DNL Creative] har stöd för HTML5-banners med mediekreatörer som inte har så mycket innehåll och som visas inom angivna gränser på en sida. Du kan använda följande typer av HTML5-kreatörer:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** Stöder upp till 5 URL:er för landningssidor som kan konfigureras när du skapar eller arbetar med innehåll.

* **Flexibel HTML5:** Har stöd för upp till 5 URL:er för landningssidor som kan konfigureras när du skapar eller arbetar med innehåll, och tillåter även att kreativa attribut ändras när du skapar eller arbetar med innehåll.

## Krav

### Krav på mapp och komprimering

* Den kreativa delen måste paketeras i en ZIP-fil (.ZIP-format). Kapslade ZIP-filer stöds inte, så ta inte med en komprimerad mapp i den yttre komprimerade mappen.

* ZIP-filen måste innehålla minst en HTML-fil - huvudvisningsfilen för HTML - som innehåller en referens till JavaScript-biblioteket [!DNL Creative]. Huvudfilen för HTML kan finnas antingen i rotmappen eller i en undermapp.

* Huvudfilen för HTML kan heta vad som helst, förutsatt att den inte innehåller specialtecken, även om `index.html` rekommenderas.

* Alla resurser som stöds och som behövs för att återge den slutliga kreativa delen måste antingen finnas i samma mapp som visningsfilen för HTML eller i undermappar i huvudmappen.

* Ta inte med filer i den kreativa delen som inte refereras till den kreativa delen.

### Inkludering av Advertising Creative JavaScript-filen

Huvudfilen HTML - och inga andra filer - måste innehålla en referens till JavaScript-filen `AMOLibrary.js`. Anropa filen på den första raden i avsnittet `<head>` med följande adress:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Den här filen innehåller funktioner som säkerställer att lokal testning av avslutshändelser utförs utan problem.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5 - kreativa krav

#### Stöd för klickbara URL:er i statiska HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registrerar klicknings-URL:er och den associerade parametern som används för att referera till varje URL (kallas `clickTag`). Detta informerar annonsservern [!DNL Creative] om var klickspårning ska läggas till. Du kan använda det här API:t för att registrera upp till fem klickvariabler, var och en med en motsvarande landningssidas URL.

>[!NOTE]
>
>De statiska URL:er som du inkluderar i HTML5-projekt används endast i lokala testningssyften och skrivs över. När du överför en HTML5-creative definierar du standardlandningssidan för varje `clickTag`-variabel. När du tilldelar en uppladdad HTML5-creative till en annonsupplevelse kan du eventuellt åsidosätta standardlandningssidan för varje `clickTag`-variabel och [!DNL Creative] lägger till klickspårning i URL:erna när du sparar upplevelsen.

###### Parametrar

* `clkVar` - Namnet på klickvariabeln (vanligtvis &quot;clickTag&quot;), omsluten med dubbla citattecken.

* `clkUrl` - Landningssidans URL för den här klickvariabeln, omsluten av dubbla citattecken.

###### Användning

Anropa `amo.registerClick()` i avsnittet `<head>` i HTML-huvudfilen.

###### Exempel

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Startar exit-händelsen, som dirigerar om användaren till startsidan som konfigurerats för `clickTag`. Vid lokal testning varnar den här funktionen utvecklarna om URL:en som skickas till funktionen har registrerats.

###### Parametrar

* `clkTag` - Namnet på klickvariabeln som du använder för att tilldela landningssidans URL med funktionen `amo.registerClick()`, omsluten med enkla citattecken.

* `event` — (Valfritt) Händelseobjektet JavaScript &quot;click&quot;. Detta registrerar koordinaterna för klickningarna, som kan användas för att analysera den kreativa prestandan.

###### Användning

Anropa `amo.onAdClick()` i avsnittet `<body>` i HTML-huvudfilen.

###### Exempel

`amo.onAdClick('clickTag')` ELLER `amo.onAdClick('clickTag',clickEvt)`

### Flexibla kreativa krav för HTML5

#### Stöd för klickbara URL:er i flexibel HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registrerar klicknings-URL:er och den associerade parametern som används för att referera till varje URL (kallas `clickTag`). Detta informerar annonsservern [!DNL Creative] om var klickspårning ska läggas till. Du kan använda det här API:t för att registrera upp till fem klickvariabler, var och en med en motsvarande landningssidas URL.

>[!NOTE]
>
>De statiska URL:er som du inkluderar i HTML5-projekt används endast i lokala testningssyften och skrivs över. När du överför en HTML5-creative definierar du standardlandningssidan för varje `clickTag`-variabel. När du tilldelar en uppladdad HTML5-creative till en annonsupplevelse kan du eventuellt åsidosätta standardlandningssidan för varje `clickTag`-variabel och [!DNL Creative] lägger till klickspårning i URL:erna när du sparar upplevelsen.

###### Parametrar

* `clkVar` - Namnet på klickvariabeln (vanligtvis &quot;clickTag&quot;), omsluten med dubbla citattecken.

* `clkUrl` - Landningssidans URL för den här klickvariabeln, omsluten av dubbla citattecken.

###### Användning

Anropa `amo.registerClick()` i avsnittet `<head>` i HTML-huvudfilen.

###### Exempel

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Startar exit-händelsen, som dirigerar om användaren till startsidan som konfigurerats för `clickTag`. Vid lokal testning varnar den här funktionen utvecklarna om URL:en som skickas till funktionen har registrerats.

###### Parametrar

* `clkTag` - Namnet på klickvariabeln som du använder för att tilldela landningssidans URL med funktionen `amo.registerClick()`, omsluten med enkla citattecken.

* `event` — (Valfritt) Händelseobjektet JavaScript &quot;click&quot;. Detta registrerar koordinaterna för klickningarna, som kan användas för att analysera den kreativa prestandan.

###### Användning

Anropa `amo.onAdClick()` i avsnittet `<body>` i HTML-huvudfilen.

###### Exempel

`amo.onAdClick('clickTag')` ELLER `amo.onAdClick('clickTag',clickEvt)`

#### Stöd för kreativa attribut i flexibla HTML5

##### `amo.registerAttribute(key, type, value)`

Definierar attribut för de kreatörer som kan ändras när de skapar material eller upplevelser. Du kan definiera upp till 20 kreativa attribut som kan konfigureras när du skapar kreativa eller upplevelser.

>[!NOTE]
>
>De värden som definieras i den här metoden används endast för lokal utveckling och används inte för att serva annonser live.

###### Parametrar

* `key` - Attributets alfanumeriska namn. Det måste börja med ett alfabetiskt tecken.

* `type` - Attributtypen (`TEXT` eller `IMAGE`).

* `value` - Värdet på attributet för testning. För attribut av typen `IMAGE` måste värdet vara den relativa sökvägen till bildfilen.

###### Användning

Anropa `amo.registerAttribute()` för att registrera ett kreativt attribut, typ och värde under testning i lokalt läge. Alla bildfiler som används som exempelvärden ska paketeras i ZIP-filen tillsammans med det överförda paketet.

##### `amo.attributes`

Ett JSON-objekt som frågar efter variabelnamnen och värdena för det kreativa attributet. Objektnycklarna blir attributnamnen och värdena blir värdena för dessa attribut.

I det lokala testläget är nyckelvärdepar de par som registrerats av API:t `amo.registerAttribute`. För produktion måste variabelnamnen och värdena för det kreativa attributet konfigureras samtidigt som kreativa projekt skapas och säljs.

### Krav på kreativt innehåll

De flesta bildskärmsutbyten som är tillgängliga i Advertising DSP har följande kreativa krav:

* En heldragen kant måste omge alla annonsbilder.

* Det är inte tillåtet att utöka annonser.

* Landningssidan måste öppnas i ett nytt fönster.

* Domänen för landningssidan och dess underdomäner får inte vara längre än 35 tecken. **Obs!** De slutliga URL-adresserna för landningssidan definieras i DSP och inte i själva HTML5-resurserna.

* Alla friskrivningar till ett annonserbjudande måste ingå i själva annonsen och inte bara på landningssidan.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Exempelinnehåll som ett JSON-objekt och en array

### Exempelinnehåll som ett JSON-objekt

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Exempelinnehåll som en JSON-array

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Exempel på HTML5 creative

### Exempel på mappstruktur (efter dekomprimering)

* index.html

* /assets (mapp)

   * bg.jpg (JPG, PNG, SVG eller GIF)

### Exempel på HTML-fil (index.html) för enkla HTML 5-kreatörer

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Exempel på HTML-fil (index.html) för HTML 5-kreatörer

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Lägg till standardkreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-standard.md)
