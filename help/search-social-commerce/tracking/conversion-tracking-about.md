---
title: Alternativ för konverteringsspårning för Search, Social och Commerce
description: Läs mer om konverteringsspårningsalternativ för Sök, Social och Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Alternativ för konverteringsspårning för Search, Social och Commerce

I Sök, Sociala och Commerce kan du använda konverteringsdata som spåras på följande sätt:

* **Adobe Advertising-spårade konverteringar:** Annonsören infogar en Adobe Advertising-konverteringsspårningstagg på varje konverteringssida. Taggen skickar konverteringsdata till en spårningsserver. Du kan antingen använda den äldre pixeln från tredje part eller den nyare pixeln från första part. Se &quot;[Jämförelse av varje konverteringsspårningsmetod](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-konverteringar:** Annonsören använder Adobe Analytics tracking för alla konverteringar. Det här alternativet kräver integrering mellan Adobe Advertising och Adobe Analytics. Mer information finns i [Adobe Analytics-konverteringsspårning](conversion-tracking-analytics.md).

* **[!DNL Google Analytics]konverteringar:** Annonsören använder taggen [!DNL Google Analytics] för att spåra alla konverteringar. Mer information om konverteringar som synkroniseras automatiskt finns i [[!DNL Google Ads] konverteringsdata i Sök, Socialt och Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

* **Advertiser-spårade konverteringar:** (endast för Search-, Social- och Commerce-klienter) Annonsören tillhandahåller Search, Social och Commerce en feed-fil med valfri kombination av online- och offlinekonverteringsdata. Se &quot;[Konverteringsspårning med en EF ID-feed](feed-efid.md)&quot; och &quot;[Konverteringsspårning med en transaktions-ID-feed](feed-transaction-id.md).&quot;

## Jämförelse av varje konverteringsspårningsmetod {#conversion-tracking-comparison}

I takt med att webbläsar-cookie-reglerna blir allt strängare är det viktigt att du förstår vilka spårningsfunktioner du har och att du identifierar de bästa alternativen på längre sikt.

| Spårningsmetod | Beskrivning | Begränsningar | Fördelar | Rekommenderas? |
|----|----|----|----|----|
| Adobe Analytics | Annonsörer med [Adobe Analytics för Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=sv-SE) importerar automatiskt standardhändelser för [!DNL Analytics] och anpassade händelser till Adobe Advertising för rapportering och optimering. | <ul><li>[!DNL Safari] tillåter bara en sju dagars konverteringssökning, som återställs vid upprepande webbplatsbesök under uppslagsfönstret.</li><li> Förväntade liknande begränsningar i [!DNL Chrome] under 2024.</li></ul> | <ul><li>Smidig integrering med [!DNL Analytics]</li> <li>Visa betalda sökdata i [!DNL Analytics] Analysis Workspace</li><li>Fördelar utöver betald sökning</li></ul> | Ja |
| Äldre Adobe Advertising-pixel | Annonsörer lägger till äldre Adobe Advertising-bilder eller JavaScript-pixlar på konverteringssidorna. Pixeln utlöses när en användare som klickade på en annons når sidan. Den här metoden använder cookies från tredje part. | <ul><li>[!DNL Safari] blockerar all konverteringsspårning med den här metoden.</li><li>Förväntade liknande begränsningar i [!DNL Chrome] under 2024.</li></ul> | Pixeln är redan implementerad. Du måste dock fortfarande [implementera den extra ITP-mappningstaggen](itp-conversion-mapping-tag.md).<br><br>Rekommendation: Växla till pixeln från första part. | Nej |
| Adobe Advertising Pixel från första part | Annonsörer gör följande: <ul><li>Implementera JavaScript-biblioteket för tjänsten [Adobe Experience Cloud ID (ECID) ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=sv-SE) för hela webbplatsen.</li><li>Lägg till Adobe Advertising [JavaScript-taggar med ITP-mappning](itp-conversion-mapping-tag.md) på alla sidor som kan vara en landningssida från ett sökklick (helst på alla sidor, eftersom landningssidorna kan ändras över tid). Med taggen kan Adobe Advertising spåra en konverteringshändelse som inträffar på en sida som konverterar stora tal till en vetenskaplig notation på landningssidan.</li><li>Lägg till taggen [JavaScript för konverteringsspårning v3](format-conversion-tag-jsv3.md) i Adobe Advertising på konverteringssidorna.</li></ul> | <ul><li>[!DNL Safari] tillåter bara en sju dagars konverteringssökning, som återställs vid upprepande webbplatsbesök under uppslagsfönstret.</li><li>Förväntade liknande begränsningar i [!DNL Chrome] under 2022.</li></ul> | [!DNL Safari] spårar konverteringar under sju dagars uppslag. Eftersom uppslaget återställs vid upprepade webbplatsbesök under uppslagsfönstret påverkar begränsningen inte alla [!DNL Safari]-användare. | Nej |
| EFID-feed | Annonsörens sökkonton har konfigurerats för att generera mål-URL:er/slutliga URL:er med unika ID:n för Adobe Advertising (token). När en användare klickar på en annons skapar Adobe Advertising ett unikt ID (`EFID`) och visar det i slutet av den sista URL:en. Annonsörens klientsystem samlar in EFID:t som en unik identifierare för konverteringar som följer av klickningen och skickar det till Adobe Advertising i ett intäktsflöde som innehåller EFID, transaktionsdatum och konverteringsmått. Adobe Advertising använder sedan EFID för att matcha konverteringen till originalklickningen. | <ul><li>Annonsören måste ha ett sätt att hämta EFID och skicka automatiska flöden till Adobe Advertising varje dag.</li><li>Konverteringar kan spåras i upp till 180 dagar (per Adobe Advertising) eller i enlighet med annonsörens system.</li></ul> | <ul><li>Den här metoden använder konverteringsdata från första part, så den påverkas inte av cookie-begränsningar från tredje part.</li><li>Konverteringar online och offline kan skickas i en enda feed.</li><li>Inga kodändringar eller taggar krävs för platsen.</li></ul> | Ja |
| Kombinationsfeed för transaktions-ID [] | Annonsörer lägger till Adobe Advertising-pixlar som innehåller en parameter för ett unikt transaktions-ID (`ev_transid=&lt;transid&gt;`) på sina webbsidor, och Adobe Advertising hämtar det unika transaktions-ID som skapas när pixeln aktiveras. Annonsörens klientsystem hämtar också [!UICONTROL Transaction ID] och skickar en intäktsfeed till Adobe Advertising för offlinekonverteringar med matchande [!UICONTROL Transaction ID]-värden | <ul><li>Om annonsören använder den äldre pixeln, som [!DNL Safari] förhindrar att den aktiveras, hämtas inte ID:t för offlinedata.</li><li>Matningen är inte automatiserad.</li></ul> | <ul><li>Om du implementerar pixeln från första part hämtas [!UICONTROL Transaction ID] i [!DNL Safari].</li><li>Tillhandahåller spårning av konverteringshändelser offline/godkänt.</li></ul> | Nej |
| [!DNL Google] konverteringar | Konverteringar som spåras med [!DNL Google Analytics] taggar importeras automatiskt till Adobe Advertising via en API-anslutning. Varje konverteringsnamn har ett `&quot;GGL_&quot;`-prefix. | <ul><li>[!DNL Google] spårar vanligtvis inte offlinedata.</li><li>[!DNL Microsoft Advertising] konverteringar ingår inte.</li></ul> | [!DNL Google] använder maskininlärning för att extrapolera [modellerade konverteringar](https://support.google.com/google-ads/answer/10081327). | Nej |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Om Adobe Advertising-taggar för konvertering/spårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-konverteringsspårning](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konverteringsspårning med en EF ID-feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konverteringsspårning med en transaktions-ID-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
