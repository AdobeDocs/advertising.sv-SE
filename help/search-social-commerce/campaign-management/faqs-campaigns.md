---
title: Frågor och svar om kampanjer
description: Se svar på frågor om kampanjhantering och kampanjdatavyer.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Frågor och svar om kampanjhantering

## Allmän information

+++Kan jag flytta kampanjer och komponenter från ett konto till ett annat?

Flytta eller kopiera inte en kampanj- eller kampanjkomponent, som har ett unikt ID, till ett konto med ett annat konto-ID. Om du gör det uppstår datafel.
+++

+++När uppdateras klickdata från annonsnätverken?

Processen med att hämta föregående dags klickdata från sökmotorerna börjar klockan 06:00 i annonsörens tidszon.

Dessutom hämtas [!DNL Google Ads] resultatmått på kampanjnivå i söknätverket för den aktuella dagen kl. 08:00 och 16:00 i annonsörens tidszon.
+++

+++Vilka åtgärder gör att nyckelord och annonser förlorar sin historik?

>[!NOTE]
>
>(Annonsörer med portföljer) Förvänta dig att prestanda för kombinationer av nya nyckelord och matchningstyper ska bli instabila när Search, Social och Commerce samlar in data för att skapa modeller för dem.

**Åtgärder i vyerna [!UICONTROL Search] > [!UICONTROL Campaigns], i publiceringsprocessen för kalkylbladet och i annonsnätverkets egen redigerare:**

Det befintliga nyckelordet eller annonsen tas bort och ett annat skapas när:

* ([!DNL Baidu], [!DNL Google Ads] och [!DNL Yandex]) Du redigerar ett nyckelordsnamn.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yandex]) Du ändrar matchningstypen för ett nyckelord.

* Du flyttar ett nyckelord mellan annonsgrupper.

* ([!DNL Google Ads] dynamiska sökannonser, [!DNL Microsoft Advertising] expanderade textannonser och alla annonstyper i andra annonsnätverk som stöds) Du redigerar och kopierar (rubrik/titel eller beskrivning) eller en annonsbild.

* Du flyttar en annons mellan annonsgrupper.

**Händelser i produktionsflödets bokföringsprocess:**

En befintlig annons eller ett nyckelord tas bort och ett annat skapas när:

* En feed-fil innehåller ett nytt värde för en kolumn som används i en annonsvariant.

* Mallinställningarna för en annons har ändrats sedan den senaste spridningen.

* En ny feed-fil innehåller en rad för en annons eller ett nyckelord som a) fanns i en tidigare fil men b) har utelämnats sedan dess och pausats eller tagits bort enligt feed-datainställningarna.

Beroende på [feed-datainställningarna](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) kan en befintlig annons eller ett nyckelord tas bort när:

* En ny feed-fil innehåller inte en rad för en befintlig annons eller ett befintligt nyckelord.

* Det schemalagda slutdatumet för komponenterna i en bokförd feed-fil inträffar.

* Lagernivån för ett objekt sjunker under ett minimum som anges i inställningarna för feed-data.
+++

+++([!DNL Google Ads] kampanjer) Ändringarna av visningsnamnen för mina [!DNL Google]-spårade konverteringar har återförts.

Om du ändrar visningsnamnen för konverteringsmåtten i Sök, Socialt och Commerce skrivs ändringarna över med de namn som konfigurerats i [!DNL Google Ads]. Gör eventuella namnändringar i [!DNL Google Ads].
+++

+++ (Google Ads-kampanjer) Kan jag använda en delad budget för kampanjer i portfolior?

För bästa resultat ska du inte lägga till [!DNL Google Ads] kampanjer i en [!DNL Google Ads] delad budget om de finns i optimerade portföljer som är konfigurerade till [!UICONTROL Auto adjust campaign budget limits]. Om du gör det åsidosätter [!DNL Google Ads] budgeten för sök-, sociala och Commerce-optimerade kampanjer, vilket kan leda till ineffektivitet i budgivning.
+++

+++([!DNL Google Ads] kampanjer) Kan jag skicka mobilanvändare och icke-mobilanvändare till olika landningssidor?

Du kan använda [!DNL Google Ads] [!DNL ValueTrack] parametrarna `{ifmobile}` och `{ifnotmobile}` för att fastställa domännamnet för landningssidan på ett av två sätt, beroende på vad som gäller för dina platser:

* Inkludera mobilbeteckningen som värdserver med `{ifmobile:m}{ifnotmobile:www}`.

  Till exempel tar `http://{ifmobile:m}{ifnotmobile:www}.example.com` mobilanvändare till m.example.com och icke-mobilanvändare till www.example.com.

* Inkludera mobilbeteckningen som toppnivådomän med `{ifmobile:mobi}{ifnotmobile:com}`.

  Till exempel tar `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` mobilanvändare till www.example.mobi och icke-mobilanvändare till www.example.com.

I båda fallen inkluderar bas-URL:erna med sök-, sociala och Commerce-spårning de okodade `{}`-taggarna och eventuella ytterligare parametrar som lagts till i bas-URL:en.

>[!NOTE]
>
>Använd inte en fullständig URL som värde för parametrar för ifnotmobile och ifmobile. Använd bara den variabla delen av URL:en (till exempel&quot;m&quot; jämfört med&quot;www&quot; eller&quot;mobi&quot; jämfört med&quot;com&quot;).

+++

+++([!DNL Google Ads] kampanjer i söknätverket) Vilka data visas för i dag?

[!DNL Google Ads] resultatmått på kampanjnivå i söknätverket för den aktuella dagen hämtas kl. 08.00 och kl. 16.00 i annonsörens tidszon.

På fliken [!UICONTROL Campaigns] i både vyn [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] och vyn [!UICONTROL Optimization] > [!UICONTROL Portfolios], inkluderar data de senast synkroniserade data när du rapporterar [!UICONTROL Today] eller ett anpassat datumintervall som inkluderar den aktuella dagen.

>[!NOTE]
>
>Data för klickningar, visningar och konverteringar fördröjs med tre timmar och är inte fullständiga förrän nästa data hämtas.

+++

+++Vad är skillnaden mellan en spårningsmall och ett landningssidessuffix?

Använd bara ett landningssidessuffix för annonsnätverk som stöder parallell spårning. I Sök, Socialt och Commerce ska både spårningsmallar och landningssidans suffix innehålla en klickidentifierare från annonsnätverket, men spårningsmallarna innehåller ytterligare spårningsparametrar.

Mer information om hur spårningsmallar och suffix för landningssidor läses in när en användare klickar på en annons finns i nästa vanliga frågor om [stöd för parallell spårning](#parallel-tracking).

+++

+++([!DNL Google Ads] och [!DNL Microsoft Advertising]) Har Search, Social och Commerce stöd för parallell spårning av annonser i [!DNL Google Ads] eller [!DNL Microsoft Advertising]? {#parallel-tracking}

Parallell spårning skickar kunder direkt från annonsen till den slutliga URL:en, som kan innehålla tillagda parametrar från ett slutligt URL-suffix, eller&quot;landningssidessuffix&quot;. URL:en till spårningsmallen (med ytterligare parametrar för klickmätning) läses in separat i bakgrunden. Detta innebär att landningssidan läses in snabbare.

Search, Social och Commerce har stöd för parallell spårning för sök- och shoppingkampanjer med annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]; `gclid` för [!DNL Google Ads]). Använd en [kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) eller [kampanjnivå](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (kallas [!DNL final URL suffix] i annonsnätverken), som läggs till i URL:er för landningssidor för att spåra klick på underordnade annonser från webbläsare som stöder parallell spårning. Se de [suffixformat som krävs för  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

När en användare tittar på din annons i en webbläsare som inte stöder parallell spårning, använder annonsnätverket sekventiell spårning i stället: kunderna skickas först till din spårningsmalls-URL, som kan dirigera om kunder till mellanliggande spårningsservrar innan de dirigeras om till den slutliga URL:en (som kan innehålla ytterligare parametrar i ett landningssidessuffix). Alla spårningsmallar för ett annonsnätverkskonto ska innehålla samma klickidentifierarparameter som du använder i [!UICONTROL Landing Page Suffix]. Se mallformaten [för spårning för  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och mallformaten [spårning för  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Varför inkluderar spårnings-URL:er för mina annonser `&EV_HASH={<hash>}`?

När du överför annonser med hjälp av en [produktinventeringsfeed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) för ett konto med omdirigeringen av pixlar i Search, Social och Commerce och med nyckelords- och kreativ spårning, lägger Search, Social och Commerce till hash-parametern och värdet i annonsens spårningsmall eller mål-URL för att identifiera att den har skapats med funktionen för lagerfeed.
+++

## Lagerfeeds

+++(Produktinventeringsflöden) Ska jag pausa eller ta bort annonser som är föråldrade eller för en produkt vars lagernivå ligger under ett visst minimivärde?

Det beror på annonsörens verksamhetskrav.

När du pausar annonser återaktiveras de om du skickar in samma annons igen eller om lagernivån överstiger minimivärdet. På så sätt kan ni behålla annonsens historik.

När du tar bort annonser och skickar in dem igen skapas nya annonser och historiska data måste samlas in för de nya annonserna. Om du inte förväntar dig att skicka in raderade annonser igen är det dock inte viktigt att ha historiska data.
+++

+++(Produktinventeringsflöden) Om jag tar bort en annonsmall och sedan skapar en ny, identisk, saknas objekt i nästa feed-fil som pausats (när inställningarna för feed-filen har konfigurerats för detta)?

Om nästa feed-fil saknar radobjekt och du inte tidigare har bokfört radobjekten från den nya mallen via en tidigare feed-fil, tolkas inte de saknade radobjekten som&quot;saknade&quot;, så de skapas inte. Du undviker detta genom att sprida den tidigare feeden genom den nya mallen och publicera data innan du sprider och publicerar data från en ny fil.
+++

+++ (produktinventeringsflöden) Kan jag uppdatera priserna för mina produkter utan att påverka en annons kvalitetspoäng?

För [!DNL Google Ads]-kampanjer, ja: Med variablerna [!DNL Google Ads] `{Param 1}` och `{Param 2}` kan du infoga numeriska värden dynamiskt i en annonsvariation utan att ta bort och återskapa annonsen, och därför utan att påverka kvalitetspoängen.

Om du vill använda en `{Param 1}`- eller `{Param 2}`-variabel för dina prisdata mappar du priskolumnen i din datafil till den variabeln i rätt feedmallar och tar sedan med variabeln i dina annonsvariantmallar.

Om kolumnen till exempel heter&quot;Pris&quot;, öppnar du den feed-mall som skapar annonserna, klickar i indatafältet bredvid **[!UICONTROL Param 1]** och sedan på kolumnen **[!UICONTROL Price]** i listan [!UICONTROL Feeds/Available Columns] som infogar `[Price]` som värde för [!UICONTROL Param 1]. I annonsvariationsmallen längst ned i feed-mallen infogar du sedan `{param1:default text}`, där&quot;standardtext&quot; är text som ska användas om parameterkolumnen i feed-filen är tom för en annonsrad.

När du skickar data kan datafälten för kolumnerna [!UICONTROL Param1] och [!UICONTROL Param2] innehålla upp till 25 tecken, inklusive numeriska data, valutasymboler och valutakoder samt följande icke-numeriska tecken: `, . % + - /`
+++

+++Mina kampanjer som genereras från lagerfeeds har många överblivna transaktioner.

Om [feed-datainställningarna](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) är konfigurerade att ta bort annonser i olika situationer kan fördröjda konverteringar som inträffar efter klickningar på annonsen orsaka [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p). Det bästa sättet är att pausa annonser i stället för att ta bort dem. Om en annons fortfarande inte har fått några intäkter på lång tid kan du ta bort den via ett kalkylblad eller annonshanteringsvyn.
+++

## Konto- och kampanjrelaterade prestandaproblem

+++Vissa av mina kampanjer spenderar mer eller mindre än kampanjbudgeten.

* Detta är normalt i en optimerad portfölj som har konfigurerats med alternativet [!UICONTROL Auto-adjust campaign budget limits]. När det här alternativet är aktiverat kan du spendera upp till *N* gånger varje kampanjs budget, där *N* är värdet för inställningen [!UICONTROL Multiple]. Med det här alternativet kan optimeringsmöjligheterna justera utgifterna för enskilda kampanjer efter behov, samtidigt som hela portföljen styrs för att uppnå sitt mål.
* Om [!DNL Google Ads] kampanjer använder en delad budget justerar [!DNL Google Ads] utgifterna för enskilda kampanjer efter behov för att spendera hela den delade budgeten.
+++
