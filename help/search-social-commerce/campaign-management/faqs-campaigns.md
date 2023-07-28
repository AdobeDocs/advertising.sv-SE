---
title: Frågor och svar om kampanjer
description: Se svar på frågor om kampanjhantering och kampanjdatavyer.
exl-id: b5975869-4bc3-461d-8cb7-eeefab157137
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Frågor och svar om kampanjhantering

## Allmän information

+++Kan jag flytta kampanjer och komponenter från ett konto till ett annat?

Flytta eller kopiera inte en kampanj- eller kampanjkomponent, som har ett unikt ID, till ett konto med ett annat konto-ID. Om du gör det kommer datafel att uppstå.
+++

+++När uppdateras klickdata från annonsnätverken?

Processen med att hämta föregående dags klickdata från sökmotorerna börjar klockan 06:00 i annonsörens tidszon.

Dessutom [!DNL Google Ads] Resultatstatistik på kampanjnivå i söknätverket för den aktuella dagen hämtas kl. 08.00 och kl. 16.00 i annonsörens tidszon.
+++

+++Vilka åtgärder gör att nyckelord och annonser förlorar sin historik?

>[!NOTE]
>
>(Annonsörer med portföljer) Förvänta dig att prestanda för kombinationer av nya nyckelord och matchningstyper blir instabila medan Sök, Socialt och Commerce samlar in data för att skapa nya modeller.

**Åtgärder i [!UICONTROL Search] > [!UICONTROL Campaigns] vyer, i utskicksprocessen för kalkylblad och i annonsnätverkets egen redigerare:**

Det befintliga nyckelordet eller annonsen tas bort och ett annat skapas när:

* ([!DNL Baidu], [!DNL Google Ads]och [!DNL Yandex]) Du redigerar ett nyckelordsnamn.

* ([!DNL Google Ads], [!DNL Microsoft Advertising]och [!DNL Yandex]) Du ändrar nyckelordets matchningstyp.

* Du flyttar ett nyckelord mellan annonsgrupper.

* ([!DNL Google Ads] dynamiska sökannonser, [!DNL Microsoft Advertising] expanderade textannonser och alla annonstyper i andra annonsnätverk som stöds) Du kan redigera och kopiera (rubrik/rubrik eller beskrivning) eller en annonsbild.

* Du flyttar en annons mellan annonsgrupper.

**Händelser i produktlagrets feedbokföringsprocess:**

En befintlig annons eller ett nyckelord tas bort och ett annat skapas när:

* En feed-fil innehåller ett nytt värde för en kolumn som används i en annonsvariant.

* Mallinställningarna för en annons har ändrats sedan den senaste spridningen.

* En ny feed-fil innehåller en rad för en annons eller ett nyckelord som a) fanns i en tidigare fil men b) har utelämnats sedan dess och pausats eller tagits bort enligt feed-datainställningarna.

Beroende på [inställningar för feed-data](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)kan en befintlig annons eller ett befintligt nyckelord tas bort när:

* En ny feed-fil innehåller inte en rad för en befintlig annons eller ett befintligt nyckelord.

* Det schemalagda slutdatumet för komponenterna i en bokförd feed-fil inträffar.

* Lagernivån för ett objekt sjunker under ett minimum som anges i inställningarna för feed-data.
+++

++([!DNL Google Ads] kampanjer) Ändringar av visningsnamnen för [!DNL Google]-spårade konverteringar har återförts.

Om du ändrar visningsnamnen för transaktionsegenskaperna i Sök, Socialt och Commerce skrivs ändringarna över med de namn som konfigurerats i [!DNL Google Ads]. Gör alla namnändringar i [!DNL Google Ads].
+++

+++ (Google Ads-kampanjer) Kan jag använda en delad budget för kampanjer i portfolior?

Bäst resultat får du om du inte lägger till [!DNL Google Ads] kampanjer till [!DNL Google Ads] delad budget om de finns i optimerade portföljer som är konfigurerade för[!UICONTROL Auto adjust campaign budget limits].&quot; Om du gör det, [!DNL Google Ads] åsidosätter budgeten för sök-, sociala och handels-optimerade kampanjer, vilket kan leda till ineffektiva anbud.
+++

++([!DNL Google Ads] kampanjer) Kan jag skicka mobilanvändare och icke-mobilanvändare till olika landningssidor?

Du kan använda [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` och `{ifnotmobile}` för att fastställa landningssidans domännamn på ett av två sätt, beroende på vad som gäller för dina platser:

* Inkludera mobilbeteckningen som värdserver med `{ifmobile:m}{ifnotmobile:www}`.

  Till exempel: `http://{ifmobile:m}{ifnotmobile:www}.example.com` tar mobilanvändare till m.example.com och icke-mobilanvändare till www.example.com.

* Inkludera mobilbeteckningen som toppnivådomän med `{ifmobile:mobi}{ifnotmobile:com}`.

  Till exempel: `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` tar mobilanvändare till www.example.mobi och icke-mobilanvändare till www.example.com.

I båda fallen inkluderar bas-URL:erna med sök-, sociala och handelsuppföljning den okodade `{}` -taggar och eventuella ytterligare parametrar som har lagts till i bas-URL:en.

>[!NOTE]
>
>Använd inte en fullständig URL som värde för parametrar för ifnotmobile och ifmobile. Använd bara den variabla delen av URL:en (till exempel&quot;m&quot; jämfört med&quot;www&quot; eller&quot;mobi&quot; jämfört med&quot;com&quot;).

+++

++([!DNL Google Ads] kampanjer i söknätverket) Vilka data visas idag?

[!DNL Google Ads] Resultatstatistik på kampanjnivå i söknätverket för den aktuella dagen hämtas kl. 08.00 och kl. 16.00 i annonsörens tidszon.

I [!UICONTROL Campaigns] i båda [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] visa och [!UICONTROL Optimization] > [!UICONTROL Portfolios] visa, när du rapporterar [!UICONTROL Today] eller ett anpassat datumintervall som inkluderar den aktuella dagen, kommer data att innehålla de data som har hämtats senast.

>[!NOTE]
>
>Data för klickningar, visningar och konverteringar fördröjs med tre timmar och är inte fullständiga förrän nästa data hämtas.

+++

++([!DNL Google Ads] och [!DNL Microsoft Advertising]) Stöder sökning, sociala medier och handel parallell spårning för annonser i [!DNL Google Ads] eller [!DNL Microsoft Advertising]?

Parallell spårning skickar kunder direkt från annonsen till den slutliga URL:en och URL:en för spårningsmallen (med klickmätning) läses in i bakgrunden, vilket innebär att landningssidan läses in snabbare.

Sökning, sociala medier och handel stöder parallell spårning för sök- och shoppingkampanjer med annonsnätets klickidentifierare (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]). Använd en [kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) eller [kampanjnivå](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (anropades &quot;[!DNL final URL suffix]&quot; i annonsnätverket), som bifogas till landningssidans URL:er för att spåra klick på underordnade annonser från webbläsare som stöder parallell spårning. Se [obligatoriska suffixformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

När en användare tittar på din annons i en webbläsare som inte stöder parallell spårning, använder annonsnätverket sekventiell spårning i stället: kunderna skickas först till din URL-adress för spårningsmall, som kan dirigera om kunder till mellanliggande spårningsservrar innan de dirigeras om till den slutliga URL-adressen. Alla spårningsmallar för ett annonsnätverkskonto ska innehålla samma klickidentifierarparameter som du använder i [!UICONTROL Landing Page Suffix]. Se [spåra mallformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [spåra mallformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Varför ska jag spåra URL:er för mina annonser med &quot;`&EV_HASH={<hash>}`?&quot;

När du överför annonser med en [produktinventeringsfeed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) för ett konto med omdirigering av pixlar för sökning, sociala medier och handel och med nyckelord- och kreativ spårning, lägger sedan sökningen, sociala medier och handel till hash-parametern och värdet i annonsens spårningsmall eller mål-URL för att identifiera att den har skapats med funktionen för lagerfeed.
+++

## Lagerfeeds

+++(Produktinventeringsflöden) Ska jag pausa eller ta bort annonser som är föråldrade eller för en produkt vars lagernivå ligger under ett visst minimivärde?

Det beror på annonsörens verksamhetskrav.

När du pausar annonser återaktiveras de om du skickar in samma annons igen eller om lagernivån överstiger minimivärdet. På så sätt kan ni behålla annonsens historik.

När ni tar bort annonser och skickar in dem igen skapas nya annonser och historiska data måste samlas in. Om du inte förväntar dig att skicka in raderade annonser igen är det dock inte viktigt att ha historiska data.
+++

+++(Produktinventeringsflöden) Om jag tar bort en annonsmall och sedan skapar en ny, identisk, saknas objekt i nästa feed-fil som pausats (när inställningarna för feed-filen har konfigurerats för detta)?

Om nästa feed-fil saknar radobjekt och du inte tidigare har bokfört radobjekten från den nya mallen via en tidigare feed-fil, tolkas inte de saknade radobjekten som&quot;saknade&quot;, så de skapas inte. Du undviker detta genom att sprida den tidigare feeden genom den nya mallen och publicera data innan du sprider och publicerar data från en ny fil.
+++

+++ (produktinventeringsflöden) Kan jag uppdatera priserna för mina produkter utan att påverka en annons kvalitetspoäng?

För [!DNL Google Ads] kampanjer, ja: [!DNL Google Ads] `{Param 1}` och `{Param 2}` Med variabler kan du dynamiskt infoga numeriska värden i en annonsvariation utan att ta bort och återskapa annonsen, och därför utan att påverka kvalitetspoängen.

Använda en `{Param 1}` eller `{Param 2}` -variabel för dina prisdata, mappa priskolumnen i datafilen till den variabeln i rätt feed-mallar och ta sedan med variabeln i dina annonsvariantmallar.

Om kolumnen till exempel heter&quot;Pris&quot;, öppnar du den feed-mall som skapar annonserna genom att klicka i inmatningsfältet bredvid **[!UICONTROL Param 1]** och klickar sedan på **[!UICONTROL Price]** kolumn i [!UICONTROL Feeds/Available Columns] lista, som infogar `[Price]` som värdet för [!UICONTROL Param 1]. Infoga sedan i annonsvariantmallen längst ned i feed-mallen `{param1:default text}`, där&quot;standardtext&quot; är text som ska användas om parameterkolumnen i matningsfilen är tom för en annonsrad.

När du skickar data, datafälten för [!UICONTROL Param1] och [!UICONTROL Param2] kolumner kan innehålla upp till 25 tecken, inklusive numeriska data, valutasymboler och valutakoder samt följande icke-numeriska tecken: `, . % + - /`
+++

+++Mina kampanjer som genereras från lagerfeeds har många överblivna transaktioner.

Om [inställningar för feed-data](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) har konfigurerats för att ta bort annonser i olika situationer, och eventuella fördröjda konverteringar som inträffar efter klickningar på annonsen kan orsaka [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p). Det bästa sättet är att pausa annonser i stället för att ta bort dem. Om en annons fortfarande inte har fått några intäkter efter en längre tid kan du ta bort den via ett kalkylblad eller annonshanteringsvyn.
+++

## Konto- och kampanjrelaterade prestandaproblem

+++Vissa av mina kampanjer spenderar mer eller mindre än kampanjbudgeten.

* Detta är normalt i en optimerad portfölj som har konfigurerats med[!UICONTROL Auto-adjust campaign budget limits]&quot;. När det här alternativet är aktiverat kan du spendera upp till *N* gånger varje kampanjs budget, där *N* är värdet på[!UICONTROL Multiple]&quot;. Med det här alternativet kan optimeringsmöjligheterna justera utgifterna för enskilda kampanjer efter behov, samtidigt som hela portföljen styrs för att uppnå sitt mål.
* If [!DNL Google Ads] kampanjerna använder en delad budget, och sedan [!DNL Google Ads] justerar utgifter för enskilda kampanjer efter behov för att spendera hela den delade budgeten.
+++
