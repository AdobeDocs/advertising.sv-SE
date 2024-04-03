---
title: Alternativ för konverteringsspårning för sökning, sociala medier och handel
description: Läs mer om konverteringsspårningsalternativ för sökning, sociala medier och handel.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: c23028701ff0064bae04135d9e7a70da4c85e937
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Alternativ för konverteringsspårning för sökning, sociala medier och handel

I Sök, Socialt och Commerce kan du använda konverteringsdata som spåras på följande sätt:

* **Konverteringar som spåras i Adobe Advertising:** Annonsören infogar en Adobe Advertising-tagg för konvertering på varje konverteringssida. Taggen skickar konverteringsdata till en spårningsserver. Du kan antingen använda den äldre pixeln från tredje part eller den nyare pixeln från första part. Se &quot;[Jämförelse av varje konverteringsspårningsmetod](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-konverteringar:** Annonsören använder Adobe Analytics tracking för alla konverteringar. Det här alternativet kräver integrering mellan Adobe Advertising och Adobe Analytics. Se &quot;[Konverteringsspårning för Adobe Analytics](conversion-tracking-analytics.md)&quot; för mer information.

* **[!DNL Google Analytics]konverteringar:** Annonsören använder [!DNL Google Analytics] för att spåra alla konverteringar. Se &quot;[[!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; om du vill ha mer information om de konverteringar som synkroniseras automatiskt.

* **Konverteringar som spåras i annonser:** (Endast klient för sökning, sociala medier och handel) Annonsören tillhandahåller en flödefil med valfri kombination av konverteringsdata online och offline för sökning, sociala medier och handel. Se &quot;[Konverteringsspårning med en EF ID-feed](feed-efid.md)och &quot;[Konverteringsspårning med en transaktions-ID-feed](feed-transaction-id.md).&quot;

## Jämförelse av varje konverteringsspårningsmetod {#conversion-tracking-comparison}

I takt med att webbläsar-cookie-reglerna blir allt strängare är det viktigt att du förstår vilka spårningsfunktioner du har och att du identifierar de bästa alternativen på längre sikt.

| Spårningsmetod | Beskrivning | Begränsningar | Fördelar | Rekommenderas? |
|----|----|----|----|----|
| Adobe Analytics | Annonsörer med [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) automatiskt importera [!DNL Analytics] standardhändelser och anpassade händelser till Adobe Advertising för rapportering och optimering. | <ul><li>[!DNL Safari] tillåter endast sju dagars konverteringssökning, som återställs vid återkommande webbplatsbesök under uppslagsfönstret.</li><li> Förvänta dig liknande begränsningar i [!DNL Chrome] 2024.</li></ul> | <ul><li>Smidig integrering med [!DNL Analytics]</li> <li>Se betalda sökdata i [!DNL Analytics] Analysis Workspace</li><li>Fördelar utöver betald sökning</li></ul> | Ja |
| Äldre Adobe Advertising-pixel | Annonsörer lägger till äldre Adobe Advertising-bilder eller JavaScript-pixlar på sina konverteringssidor. Pixeln utlöses när en användare som klickade på en annons når sidan. Den här metoden använder cookies från tredje part. | <ul><li>[!DNL Safari] blockerar all konverteringsspårning med den här metoden.</li><li>Förvänta dig liknande begränsningar i [!DNL Chrome] 2024.</li></ul> | Pixeln är redan implementerad. Du måste dock fortfarande [implementera ytterligare ITP-mappningstagg](itp-conversion-mapping-tag.md).<br><br>Rekommendation: Växla till pixeln från första part. | Nej |
| Adobe Advertising Pixel från första part | Annonsörer gör följande: <ul><li>Implementera JavaScript-biblioteket för [Tjänsten Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) på hela webbplatsen.</li><li>Lägg till Adobe Advertising [JavaScript-taggar med ITP-mappning](itp-conversion-mapping-tag.md) till en sida som kan vara en landningssida från ett sökklick (helst på alla sidor, eftersom landningssidorna kan ändras över tid). Med taggen kan Adobe Advertising spåra en konverteringshändelse som inträffar på en sida som konverterar stora tal till en vetenskaplig notation på landningssidan.</li><li>Lägg till Adobe Advertising [JavaScript-konverteringsspårningstagg v3](format-conversion-tag-jsv3.md) till konverteringssidor.</li></ul> | <ul><li>[!DNL Safari] tillåter endast sju dagars konverteringssökning, som återställs vid återkommande webbplatsbesök under uppslagsfönstret.</li><li>Förvänta dig liknande begränsningar i [!DNL Chrome] 2022.</li></ul> | [!DNL Safari] spårar konverteringar under sjudagars uppslag. Eftersom uppslaget återställs vid återkommande webbplatsbesök under uppslagsfönstret, påverkar inte begränsningen alla [!DNL Safari] -användare. | Nej |
| EFID-feed | Annonsörens sökkonton har konfigurerats för att generera mål-URL:er/slutliga URL:er med unika ID:n för Adobe Advertising (token). När en användare klickar på en annons skapar Adobe Advertising ett unikt ID (`EFID`) och visar den i slutet av den slutliga URL:en. Annonsörens klientsystem samlar in EFID:t som en unik identifierare för konverteringar som följer av klickningen och skickar det till Adobe Advertising i ett intäktsflöde som innehåller EFID, transaktionsdatum och konverteringsmått. Adobe Advertising använder sedan EFID för att matcha konverteringen till originalklickningen. | <ul><li>Annonsören måste ha ett sätt att hämta EFID och skicka automatiska flöden till Adobe Advertising varje dag.</li><li>Konverteringar kan spåras i upp till 180 dagar (per Adobe Advertising) eller i enlighet med annonsörens system.</li></ul> | <ul><li>Den här metoden använder konverteringsdata från första part, så den påverkas inte av cookie-begränsningar från tredje part.</li><li>Konverteringar online och offline kan skickas i en enda feed.</li><li>Inga kodändringar eller taggar krävs för platsen.</li></ul> | Ja |
| Transaktions-ID-feed [kombinationsfeed] | Annonsörer lägger till Adobe Advertising-pixlar som innehåller en parameter för ett unikt transaktions-ID (`ev_transid=&lt;transid&gt;`) till sina webbsidor och Adobe Advertising hämtar det unika transaktions-ID som skapas när pixeln aktiveras. Annonsörens klientsystem fångar även [!UICONTROL Transaction ID] och skickar Adobe Advertising en intäktsfeed för offlinekonverteringar med matchning [!UICONTROL Transaction ID] values | <ul><li>Om annonsören använder den äldre pixeln, som [!DNL Safari] blockerar från att brännas, så registreras inte ID:t för att användas för offlinedata.</li><li>Matningen är inte automatiserad.</li></ul> | <ul><li>Om du implementerar pixeln från första part ska du [!UICONTROL Transaction ID] hämtas in [!DNL Safari].</li><li>Tillhandahåller spårning av konverteringshändelser offline/godkänt.</li></ul> | Nej |
| [!DNL Google] Konverteringar | Konverteringar spårade med [!DNL Google Analytics] -taggar importeras automatiskt till Adobe Advertising via en API-anslutning. Varje konverteringsnamn har en `&quot;GGL_&quot;` prefix. | <ul><li>[!DNL Google] spårar vanligtvis inte offlinedata.</li><li>[!DNL Microsoft® Advertising] konverteringar tas inte med.</li></ul> | [!DNL Google] använder maskininlärning för att extrapolera &quot;[modellerade konverteringar](https://support.google.com/google-ads/answer/10081327).&quot; | Nej |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Om taggar för Adobe Advertising-konverteringsspårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Konverteringsspårning för Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konverteringsspårning med en EF ID-feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konverteringsspårning med en transaktions-ID-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
