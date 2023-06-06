---
title: Om konverteringsspårningstaggar för Adobe
description: Lär dig mer om att använda Adobe Advertising conversion-tracking-taggar.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Om konverteringsspårningstaggar för Adobe

Adobe Advertising spårar konverteringar som är ett resultat av klickningar på annonser med hjälp av Adobe Advertising conversion tracking-taggar som infogas på de webbsidor som öppnas när en konverteringshändelse inträffar, till exempel en&quot;success&quot;-sida. Taggarna innehåller inbäddad information för att skicka transaktionsdata, tillsammans med användarens Adobe Advertising-cookie, till en spårningsserver, varifrån transaktionen krediteras till rätt annons-klick eller -intryck (enligt annonsörens konverteringsattribueringsinställningar).

>[!NOTE]
>
>Om användaren inte har en giltig cookie rapporterar inte Adobe Advertising konverteringen.

För varje uppsättning konverteringsmått som du vill spåra måste du skapa en separat konverteringstagg. Ge annonsören eller reklambyrån taggarna med en lista över webbsidor där varje sida ska infogas. Du kan generera någon av följande typer av konverteringstaggar. Se &quot;[Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; för instruktioner.

* (Rekommenderas) JavaScript-taggar (version 3 eller version 2) som inte visas på webbsidorna.

* HTML-bildtaggar om du vill visa genomskinliga bilder (pixlar) på 1 pixel x 1 pixel, som är osynliga för slutanvändarna, på webbsidorna. Använd bara bildtaggar när företaget har en policy för att använda JavaScript-taggar.

Mer information om skillnaderna mellan taggtyperna finns i &quot;[Frågor och svar om Advertising Cloud taggar för konverteringsspårning](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Den här funktionen lägger inte till bildtaggar eller JavaScript-taggar på annonsörens webbsidor. Taggarna måste läggas till enligt annonsörens normala procedur för uppdatering av webbsidor.
>* Tänk på hur lång tid det tar att implementera taggarna. Beroende på företagets policy kan implementeringen ta veckor eller till och med månader.


## Funktioner för Adobe Advertising conversion-tracking-taggar

Med pixeln för konverteringsspårning kan Adobe Advertising göra följande:

* Spåra och rapportera konverteringsdata på nyckelordsnivå för sökkampanjer.

* Spåra och rapportera konverteringsdata på annonsnivå (kreativ) i alla marknadsföringskanaler (betalsökningar och displayannonser), vilket kan underlätta den kreativa testningen.

* Spåra och rapportera konverteringsdata på transaktionsnivå över alla era marknadsföringskanaler.

* Visa hur era konverteringar distribueras över olika marknadsföringskanaler så att ni kan se vilken som är mest effektiv.

* Rapportera och optimera på olika attribueringsnivåer (t.ex. genom att tilldela konverteringar till den senaste relaterade händelsen eller genom att väga alla händelser jämnt).

* Ge synlighet vid klickassistenter (söknyckelord eller placeringar som har bidragit till en konverteringstratt) och kanalassistenter (användarhändelser som har bidragit till en konverteringstratt, möjligen över flera marknadsföringskanaler).

* Ge synlighet åt den geografiska fördelningen och de hänvisande domänerna för er webbplatstrafik och konverteringar så att ni kan förfina er geografiska och webbplatsbaserade målinriktning.

* Analysera veckovisa eller intradagsvisa trender som kan användas för att förbättra konverteringsgraden.

>[!MORELIKETHIS]
>
>* [Alternativ för konverteringsspårning](conversion-tracking-about.md)
>* [Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 2](format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript-konverteringskoden Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

