---
title: Alternativ för konverteringsspårning för sökning, sociala medier och handel
description: Läs mer om konverteringsspårningsalternativ för sökning, sociala medier och handel.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Alternativ för konverteringsspårning för sökning, sociala medier och handel

Adobe Advertising kan använda konverteringsdata som spåras på följande sätt:

* **Adobe Advertising-tracking convertions:** Annonsören infogar en Adobe-tagg för konvertering på varje konverteringssida. Taggen skickar konverteringsdata till en spårningsserver. Du kan antingen använda den äldre pixeln från tredje part eller den nyare pixeln från första part. Se &quot;[Jämförelse av varje konverteringsspårningsmetod](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-konverteringar:** Annonsören använder Adobe Analytics tracking för alla konverteringar. Det här alternativet kräver integrering mellan Adobe Advertising och Adobe Analytics. Se &quot;[Konverteringsspårning för Adobe Analytics](conversion-tracking-analytics.md)&quot; för mer information.

* **[!DNL Google Analytics]konverteringar:** Annonsören använder [!DNL Google Analytics] för att spåra alla konverteringar. Se &quot;[[!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; om du vill ha mer information om de konverteringar som synkroniseras automatiskt.

* **Konverteringar som spåras i annonser:** (Endast klient för sökning, sociala medier och handel) Annonsören tillhandahåller en flödefil med valfri kombination av konverteringsdata online och offline för sökning, sociala medier och handel. Se &quot;[Konverteringsspårning med en EF ID-feed](feed-efid.md)&quot; och &quot;[Konverteringsspårning med en transaktions-ID-feed](feed-transaction-id.md).&quot;

## Jämförelse av varje konverteringsspårningsmetod {#conversion-tracking-comparison}

I takt med att webbläsar-cookie-reglerna blir allt strängare är det viktigt att du förstår vilka spårningsfunktioner du har och att du identifierar de bästa alternativen på längre sikt.

| Spårningsmetod | Beskrivning | Begränsningar | Fördelar | Rekommenderas? |
|----|----|----|----|----|
| Adobe Analytics | Annonsörer med [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) automatiskt importera [!DNL Analytics] standardhändelser och anpassade händelser till Adobe Advertising för rapportering och optimering. | <ul><li>[!DNL Safari] tillåter endast sju dagars konverteringssökning, som återställs vid återkommande webbplatsbesök under uppslagsfönstret.</li><li> Förvänta dig liknande begränsningar i [!DNL Chrome] 2024.</li></ul> | <ul><li>Smidig integrering med [!DNL Analytics]</li> <li>Se betalda sökdata i [!DNL Analytics] Analysis Workspace</li><li>Fördelar utöver betald sökning</li></ul> | Ja |
| Adobe-reklampixel - äldre | Annonsörer lägger till äldre Adobe-reklambilder eller JavaScript-pixlar på sina konverteringssidor. Pixeln utlöses när en användare som klickade på en annons når sidan. Den här metoden använder cookies från tredje part. | <ul><li>[!DNL Safari] blockerar all konverteringsspårning med den här metoden.</li><li>Förvänta dig liknande begränsningar i [!DNL Chrome] 2024.</li></ul> | Pixeln är redan implementerad. Du måste dock fortfarande [implementera ytterligare ITP-mappningstagg](itp-conversion-mapping-tag.md).<br><br>Rekommendation: Växla till pixeln från första part. | Nej |
| Adobe Advertising First-party Pixel | Annonsörer gör följande: <ul><li>Implementera JavaScript-biblioteket för [Tjänsten Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) på hela webbplatsen.</li><li>Lägg till Adobe-annonsering [JavaScript-taggar med ITP-mappning](itp-conversion-mapping-tag.md) till en sida som kan vara en landningssida från ett sökklick (helst på alla sidor, eftersom landningssidorna kan ändras över tid). Med taggen kan Adobe Advertising spåra en konverteringshändelse som inträffar på en sida som konverterar stora tal till en vetenskaplig notation på landningssidan.</li><li>Lägg till Adobe-annonsering [JavaScript-konverteringsspårningstagg v3](format-conversion-tag-jsv3.md) till konverteringssidor.</li></ul> | <ul><li>[!DNL Safari] tillåter endast sju dagars konverteringssökning, som återställs vid återkommande webbplatsbesök under uppslagsfönstret.</li><li>Förvänta dig liknande begränsningar i [!DNL Chrome] 2022.</li></ul> | [!DNL Safari] spårar konverteringar under sjudagars uppslag. Eftersom uppslaget återställs vid återkommande webbplatsbesök under uppslagsfönstret, påverkar inte begränsningen alla [!DNL Safari] -användare. | Nej |
| EFID-feed | Annonsörens sökkonton är konfigurerade för att generera mål-URL:er/slutliga URL:er med Adobe Advertising unique IDs (tokens). När en användare klickar på en annons skapar Adobe Advertising ett unikt ID (`EFID`) och visar den i slutet av den slutliga URL:en. Annonsörens klientsystem samlar in EFID:t som en unik identifierare för konverteringar som följer av klickningen och skickar det till Adobe Advertising i ett intäktsflöde som innehåller EFID, transaktionsdatum och konverteringsegenskap. Adobe Advertising använder sedan EFID för att matcha konverteringen till originalklickningen. | <ul><li>Annonsören måste ha ett sätt att hämta EFID och skicka automatiska flöden till Adobe Advertising dagligen.</li><li>Konverteringar kan spåras i upp till 180 dagar (per Adobe Advertising) eller i enlighet med annonsörens system.</li></ul> | <ul><li>Den här metoden använder konverteringsdata från första part, så den påverkas inte av cookie-begränsningar från tredje part.</li><li>Konverteringar online och offline kan skickas i en enda feed.</li><li>Inga kodändringar eller taggar krävs för platsen.</li></ul> | Ja |
| Transaktions-ID-feed [kombinationsfeed] | Annonsörer lägger till Adobe-reklampixlar som innehåller en parameter för ett unikt transaktions-ID (`ev_transid=&lt;transid&gt;`) på sina webbsidor och Adobe Advertising fångar upp det unika transaktions-ID som skapas när pixeln utlöses. Annonsörens klientsystem fångar även [!UICONTROL Transaction ID] och skickar Adobe Advertising a intäktsfeed för offlinekonverteringar med matchning [!UICONTROL Transaction ID] values | <ul><li>Om annonsören använder den äldre pixeln, som [!DNL Safari] blockerar från att brännas, så registreras inte ID:t för att användas för offlinedata.</li><li>Matningen är inte automatiserad.</li></ul> | <ul><li>Om du implementerar pixeln från första part ska [!UICONTROL Transaction ID] hämtas in [!DNL Safari].</li><li>Tillhandahåller spårning av konverteringshändelser offline/godkänt.</li></ul> | Nej |
| Google Conversion | Konverteringar spårade med [!DNL Google Analytics] -taggar importeras automatiskt till Adobe Advertising via en API-anslutning. Varje konverteringsnamn har en `&quot;GGL_&quot;` prefix. | <ul><li>Google spårar vanligtvis inte offlinedata.</li><li>Konverteringar med Microsoft® Advertising ingår inte.</li></ul> | Google använder maskininlärning för att extrapolera &quot;[modellerade konverteringar](https://support.google.com/google-ads/answer/10081327).&quot; | Nej |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Om konverteringsspårningstaggar för Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Konverteringsspårning för Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konverteringsspårning med en EF ID-feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konverteringsspårning med en transaktions-ID-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)

