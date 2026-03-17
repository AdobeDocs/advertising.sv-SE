---
title: Om Adobe Advertising-taggar för konverteringsspårning
description: Läs om hur du använder Adobe Advertising-taggar för konverteringsspårning.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Om Adobe Advertising-taggar för konverteringsspårning

Adobe Advertising spårar konverteringar som följer av klickningar på annonser med hjälp av Adobe Advertising taggar för konverteringsspårning som infogas på de webbsidor som öppnas när en konverteringshändelse inträffar, till exempel en&quot;framgångssida&quot;. Taggarna innehåller inbäddad information för att skicka transaktionsdata, tillsammans med användarens Adobe Advertising-cookie, till en spårningsserver, varifrån transaktionen krediteras till rätt annons-klick eller -intryck (enligt annonsörens konverteringsattribueringsinställningar).

Du kan [generera konverteringsspårningstaggar](/help/search-social-commerce/tools/conversion-tag-generate.md) i Sök, Social och Commerce eller använda taggar i Adobe Experience Platform (tidigare Adobe Experience Platform Launch).

>[!NOTE]
>
>Om användaren inte har en giltig cookie rapporterar Adobe Advertising inte konverteringen.

För varje uppsättning konverteringsmått som du vill spåra måste du skapa och implementera en separat konverteringstagg. Du kan generera någon av följande typer av konverteringstaggar.

* (Rekommenderas) JavaScript-taggar (version 3 eller version 2) som inte visas på webbsidorna.

* HTML bildtaggar om du vill visa genomskinliga bilder (pixlar) med en pixel x en pixel, som är osynliga för slutanvändarna, på webbsidorna. Använd bara bildtaggar när företaget har en policy för att inte använda JavaScript-taggar.

Mer information om skillnaderna mellan taggtyperna finns i [Vanliga frågor om Advertising Cloud-konverteringstaggar](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

>[!NOTE]
>
>* Den här funktionen lägger inte till bildtaggar eller JavaScript-taggar på annonsörens webbsidor. Taggarna måste läggas till enligt annonsörens normala procedur för uppdatering av webbsidor.
>* Tänk på hur lång tid det tar att implementera taggarna. Beroende på företagets policy kan implementeringen ta veckor eller till och med månader.

## Funktioner för Adobe Advertising-taggar för konvertering

Med pixeln för konverteringsspårning kan Adobe Advertising göra följande:

* Spåra och rapportera konverteringsdata på nyckelordsnivå för sökkampanjer.

* Spåra och rapportera konverteringsdata på annonsnivå (kreativ) i alla marknadsföringskanaler (betalsökningar och displayannonser), vilket kan underlätta den kreativa testningen.

* Spåra och rapportera konverteringsdata på transaktionsnivå över alla era marknadsföringskanaler.

* Visa hur era konverteringar distribueras över olika marknadsföringskanaler så att ni kan se vilken som är mest effektiv.

* Rapportera och optimera på olika attribueringsnivåer (t.ex. genom att tilldela konverteringar till den senaste relaterade händelsen eller genom att väga alla händelser jämnt).

* Ge synlighet vid klickning (söknyckelord eller praktik som bidrog till en konvertering av funnel) och kanalassistenter (användarhändelser som bidrog till en konvertering av funnel, möjligen över flera marknadsföringskanaler).

* Ge synlighet åt den geografiska fördelningen och de hänvisande domänerna för er webbplatstrafik och konverteringar så att ni kan förfina er geografiska och webbplatsbaserade målinriktning.

* Analysera veckovisa eller intradagsvisa trender som kan användas för att förbättra konverteringsgraden.

>[!MORELIKETHIS]
>
>* [Alternativ för konverteringsspårning](conversion-tracking-about.md)
>* [Generera och implementera en konverteringstagg för Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format för JavaScript-konverteringstaggar, version 3](format-conversion-tag-jsv3.md)
>* [Format för JavaScript-konverteringstaggar, version 2](format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](format-conversion-tag-image.md)
>* [Frågor och svar om spårningstaggar för konvertering och sidvisning](faqs-conversion-page-view-tracking-tags.md)
>* [Konverteringsmappningstaggen för Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
