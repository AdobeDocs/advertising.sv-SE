---
title: Vanliga frågor om anpassade rapporter
description: Lär dig svar på vanliga frågor om prestandarapporter, inklusive felsökning av dataproblem.
exl-id: 85707666-7c0f-4aa3-8c91-fb73ef6a5061
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '3919'
ht-degree: 0%

---

# Vanliga frågor om anpassade rapporter

## Allmänna frågor

+++Vad händer om datumintervallet för rapporten börjar innan rapportdata är tillgängliga?
Rapporten genereras, men innehåller bara data för de datum som det finns tillgängliga data för. Mer information om när data är tillgängliga för varje rapporttyp finns i &quot;[Data som används för rapporter](data-used-for-reports.md).&quot;
+++

+++Vad är skillnaden mellan datumbaserade rapporter och transaktionsrapporter?
När du rapporterar konverteringar efter transaktionsdatum inkluderar dessa data transaktioner vars transaktionsdatum inträffade under den angivna tidsperioden. Det här alternativet är standardinställningen i grundläggande rapporter och avancerade rapporter, och visar hur mycket intäkter som intjänats under den angivna tidsperioden.

När du rapporterar konverteringar med klickningsdatum innehåller data transaktioner som har skapats av ett klick som inträffade under den angivna tidsperioden. När en portfölj har betydande fördröjningar mellan klick och transaktioner visar den här typen av rapportering den historiska intäkten per klick för portföljen, vilket ger dig en uppfattning om vilka intäktsbeteenden du kan förvänta dig över tid.

![Rapportera per klickdatum och rapport per transaktionsdatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Rapportera per klickdatum och rapport per transaktionsdatum")
+++

+++Vad händer om jag ändrar fönstret för klicksökning eller fönstret för visningssökning?
(Annonsörer med enbart annonsering av pixelbaserad konverteringsspårning) Data för händelser som är ett resultat av den första klickningen samlas in under en längre eller kortare period.

En annonsörs [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j) bestämmer hur många dagar efter ett betalt klick eller ett visningsintryck (respektive) som händelsen kan tillskrivas en konvertering. Att ändra ett värde till en längre eller kortare period kan vara viktigt för annonsörer med särskilt korta eller långa klick-till-intäkt- eller visningsintryck-intäktsperioder.

**Bästa praxis:** Se till att lookback-fönstren är längre än klicka-till-intäkt och visar intryck-i-intäktstider för de flesta nyckelord eller annonser. När de är kortare är vissa konverteringar inte kopplade till den första klickningen eller det inledande intrycket.
+++

+++Hur vet jag vilka konverteringar som har gjorts av en [!DNL Google Ads] annonstillägg eller produktlista?
Du kan se vilka konverteringar som har gjorts genom att klicka på en [!DNL Google Ads] annonstillägg (i stället för själva annonsen) eller i en produktlista genom att generera en [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] kolumnvärdet visar typ och rubrik för en länk som du klickade på:

* Produktlistor listas som `pla:<product ID>`, till exempel `pla:8525822`.

* Webbplatslänkar listas som `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.

  Du kan även identifiera en platshållare om du har [!UICONTROL Tracking URL] i rapporten. The [!UICONTROL Tracking URL] för en sitelink innehåller attributet `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Konverteringar från [!DNL Google Ads] platser och telefontillägg inkluderas i data för de annonser som de medföljer. De rapporteras inte separat.

+++

+++The &quot;[!UICONTROL Keyword]&quot; i min rapport innehåller värdet &quot;(adgroup content) &lt;*annonsgruppsnamn*>.&quot;
När raden innehåller data för innehållsaktiverade sökkampanjer, webbkampanjer eller sociala kampanjer - som inte innehåller nyckelord - är [!UICONTROL Keyword] -kolumnen visar det tillämpliga annonsgruppsnamnet i stället.
+++

+++På grund av säsongsförändringar eller förändringar på marknaden visar mina rapporter atypiska data. Kommer detta att påverka buden när villkoren ändras?
Optimeringsfunktionen bygger sina intäktsmodeller för varje budenhet dagligen för att säkerställa att den identifierar och omedelbart reagerar på trender, och modellerna bygger på långsiktiga historiska data för att hjälpa till att förutsäga säsongsrelaterade resultat. Portföljens intäktsmodell, halveringstid<!-- add link to glossary? --> avgör också hur mycket de senaste intäktsuppgifterna viktas. Det bästa sättet är att minska halveringstiden under en period med atypiska resultat men öka den efter att intäktsmodellen har justerats. Om du har några frågor om huruvida det är nödvändigt att justera halveringstiden kontaktar du ditt Adobe-kontoteam.

Om du inte vill att data för perioden ska påverka framtida bud alls kan du välja att exkludera dessa datum från modellen. Kontakta kontoteamet på Adobe för att exkludera datum.
+++

+++Kan jag skapa en rapport om ett specifikt egenskapsmått, som [!UICONTROL Device] eller [!UICONTROL Objective Name]?
Kampanjentitetsrapporter ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report]och [!UICONTROL Product Group Report]) sammanställs mätdata dynamiskt av de egenskapskolumner som du inkluderar i rapporten. Du kan också ta bort rapportens nyckelkolumn och bara ta med de egenskapskolumner för vilka du vill samla in data.

Om du till exempel skapar en [!UICONTROL Keyword Report] som innehåller [!UICONTROL Ad Group] och  Enhetskolumner sammanställer sedan rapporten som standard mätvärden för varje nyckelord per annonsgrupp och enhetstyp. Om du däremot tar bort [!UICONTROL Keyword] innan du genererar rapporten, genererar rapporten dynamiskt mått för de angivna annonsgrupperna efter enhetstyp.

>[!NOTE]
>
>Du kan inte använda den här funktionen för att samla in data efter etikettklassificeringar. Alla etikettklassificeringskolumner i rapporten utelämnas. Använd i stället [Klassificeringsrapport för etikett](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Allmänna dataproblem

+++Rapporter som genereras med olika attribueringsregler visar olika summor.
Om du genererar en rapport flera gånger med samma rapportparametrar men med olika attribueringsregler, kan data skilja sig på grund av någon av följande orsaker:

* Datumbaserade klickdata kan ligga utanför det angivna datumintervallet.

  Om du använder rapportparametern[!UICONTROL Conversions based on click date]&quot; gäller det angivna datumintervallet för klickdatumet i stället för datumet för transaktionen. Om attribueringsregeln &quot;First Event&quot; eller &quot;Last Event&quot; också används i rapporten kan den första eller sista händelsen som ledde till konverteringen ligga utanför det angivna datumintervallet. Anta till exempel att en användare klickade på Nyckelord_1 den 30 april, klickade på Nyckelord_2 den 20 maj och konverterades den 21 maj. Om rapporten använder &quot;[!UICONTROL First Event]&quot; och datumintervallet 1-21 maj, inkluderas inte den första händelsen (ett klick på Keyword_1 den 30 april) i rapporten. Om du kör rapporten med samma datumintervall men använder kommandot[!UICONTROL Last Event]&quot;attribueringsregel, så inkluderas konverteringen i rapporten eftersom den senaste klickningen inträffade inom det angivna datumintervallet.

* Portföljfiltervalet utesluter vissa händelser som leder till konverteringen.

  Om du rapporterar om en delmängd av portföljer kanske du inte inkluderar kampanjer som innehöll händelsen som konverteringen tilldelades enligt någon av attribueringsreglerna. Anta att en användare klickar på Nyckelord_1 från Portfolio_1, klickar på Nyckelord_2 från Portfolio_2 och sedan konverterar. Om rapporten använder &quot;[!UICONTROL First Event]&quot; attribueringsregel, så måste Portfolio_1 inkluderas för att konverteringen ska tas med i rapporten. Om attribueringsregeln &quot;Last Event&quot; används i rapporten måste Portfolio_2 inkluderas.

>[!TIP]
>
>Om du vill jämföra konverteringssummor enligt olika attribueringsregler kör du rapporter med rapportparametern &quot;[!UICONTROL Conversions based on transaction date]&quot; och välj alla annonsnätverk eller alla portföljer. Om du inte anger några andra filter bör konverteringssummorna stämma överens.

+++

+++Enskilda datafält är felaktiga, men summorna är korrekta.
Detta kan inträffa när heltal används i mätformaten:

* Om du skapar [anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) med formatet *Antal decimalpunkter utan decimaltecken* (som visar data som heltal) och inkludera dem i en vy eller en rapport som använder en viktad konverteringsattribueringsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], eller [!UICONTROL Even Distribution]) visas utdata i heltal, inte i decimaler. I det här fallet kan enskilda datafält vara felaktiga, även om summorna är korrekta. Om en ordning till exempel fördelas jämnt mellan tre händelser, fördelas en ordning (i stället för 0,33) på var och en av de tre händelserna. För att lösa problemet [ändra måttformatet](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) till *Antal till 2 decimalpunkter*.

* Om du har ett intäktsmått som skickas som heltal händer samma sak. (Intäktsformatet styrs av konverteringstaggen som skickar data.) För att lösa problemet [skapa ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) som endast består av intäktsmåtten och med formatet *Antal till 2 decimalpunkter*och inkludera det i vyer och rapporter i stället för i det ursprungliga måttet.
+++

+++Hur förhindrar jag att klicknings- eller intäktsdata påverkar framtida anbud?
Klickdatafel uppstår när sökning, sociala medier och handel inte är synkroniserat med annonsnätverket. Kontakta kontoteamet på Adobe om du vill synkronisera kontot manuellt. Om klickdata saknas för en hel dag ber du ditt Adobe-kontoteam att exkludera den dagen från kostnadsmodellerna.

Intäktsdataproblem kan uppstå på grund av ett problem med spårning eller feed-fil. Kontakta kontoteamet på Adobe för att undersöka problemet. Om intäktsdata saknas för en hel dag ber du ditt Adobe-kontoteam att exkludera den dagen från intäktsmodellerna.
+++

+++monetära data visas i fel format.
Som standard visas alla monetära data i rapporter i formatet för USD (till exempel 1 000,00). Om du vill visa värdet i rätt valutaformat (men utan valutasymboler i CSV- och TSV-format) lägger du till &quot;[!UICONTROL Currency]till rapporten. Om rapporten innehåller data för konton med olika valutor, kan alla &quot;[!UICONTROL Total]&quot;monetära värden är helt enkelt summan av alla tal i kolumnen, oavsett valuta.
+++

+++Varför ser jag decimalvärden för en transaktionsegenskap som ska vara ett naturligt tal (1, 2 och så vidare)?
Du kan se decimalvärden i följande fall:

* Om du körde rapporten med någon annan parameter för konverteringsattribueringsregel än [!UICONTROL Last Event] eller [!UICONTROL First Event]kan intäkterna delas upp mellan flera händelser i konverteringsvägen.

* I [!UICONTROL Transaction Report], om flera [mängdenheter](/help/search-social-commerce/glossary.md#a-b) om olika matchningstyper har samma transaktions-ID delas intäkten för spårnings-ID upp enligt antalet klick på det angivna klickdatumet.
+++

## Standardprestanda, mått

+++Klicka-data saknas i rapporter.
Nedan följer några vanliga orsaker till att klickdata saknas.

| Orsak | Upptäckt/analys | Upplösning |
|---|---|---|
| Processen som hämtar klickdata från annonskontot misslyckades. | Det finns inget systematiskt sätt att upptäcka detta problem, men ni kanske märker att en kampanj inte visar någon kostnads- eller klickinformation trots att annonskontot spenderade pengar. | Kontakta kundsupport på &lt;*ditt användarkonto för sökning, sociala medier och handel*>@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>Om data saknas i mer än 24 timmar ska dessa datum uteslutas från kostnadsprognoserna tills data har hämtats. Kontoteamet på Adobe kan exkludera datum. |
| Ett faktureringsproblem mellan annonsören och annonsnätverket förhindrar annonskontot från att spendera pengar. | Det finns inget systematiskt sätt att upptäcka detta problem, men du kanske märker att en kampanj inte visar någon kostnads- eller klickinformation. | Om du vet att ett annonskonto inte kunde användas på grund av ett faktureringsproblem, ska du undanta dessa datum från kostnadsprognoserna. Kontoteamet på Adobe kan exkludera datum. |
+++

+++Prestandadata skiljer sig från data i annonsnätverkets redigerare.
När annonsnätverket skickar uppdateringar till tidigare data (ofta för att de har tilldelat klickbedrägeri) uppdateras inte data i Sök, Socialt och Commerce, såvida det inte finns mer än 5 % diskrepans och Adobe Account Team skickar en begäran.

När du jämför visningsdelningsdata som aggregerats över ett datumintervall kan de data som rapporteras i rapporten Sök, Socialt och Commerce skilja sig från de data som annonsnätverket rapporterar. Den här skillnaden beror på hur data rapporteras av annonsnätverkets API, som används för att hämta in data i Search, Social och Commerce. Till exempel [!DNL Google Ads] data:

* För de flesta intrycket används samma mätvärden [!DNL Google Ads] Ändrar antingen den nedre eller övre delen av de värden som rapporteras för värden som är antingen mindre än 10 % eller större än 90 %. Data rapporteras som 0,0999 för &lt;10% och 0,9001 för >90%

* När det finns en blandning av begränsade och obegränsade data inom datumintervallet delar Search, Social och Commerce in visningsdata med hjälp av de värden som skickas i API:t i befintligt skick. 0,0999 används för rader med &lt;10% och 0,9001 för rader med >90 %. Den här aggregeringen kan resultera i en avvikelse från [!DNL Google Ads] föraggregerade data eftersom [!DNL Google Ads] kan använda faktiska procentvärden, som 7 % eller 97 %.
+++

+++Prestandadata i rapporter skiljer sig från data i [!DNL Google Analytics].
De två systemen mäter olika data, så du bör förvänta dig att se olika data. Exempel:

* Sök, social, &amp; Commerce (och Google Ads) spårar klick, medan [!DNL Google Analytics] spårar besök per 30-minuters webbläsarsession. Om en användare till exempel klickar på din annons en gång, klickar på knappen Bakåt och sedan klickar på annonsen igen, registrerar sökning, sociala medier och handel två klick, men [!DNL Google Analytics] registrerar ett besök.

* [!DNL Google Analytics] visar alla trafikdata, medan Sök, Social och Commerce (och [!DNL Google Ads]) filtrerar ogiltiga klick (t.ex. överdrivet, upprepade klick).

* [!DNL Google Analytics] innehåller klicknings- och intäktsdata för alla klickningar. Det går inte att spåra klick- och intäktsdata för annonser och nyckelord med felaktiga eller saknade spårnings-URL:er i sökningen, sociala medier och e-handel.
+++

## Konverteringsmått

+++Min rapport visar inga konverteringsdata.
Rapporten får inte innehålla konverteringsvärden för vilka konverteringar har gjorts.
+++

+++Intäkter saknas i rapporter.

**Annonsörer som använder konverteringstaggar i Adobe Advertising**

*Möjliga orsaker:*

* Nyckelord eller annonser lades till utan att prefixet Sök, Socialt och Commerce för klickspårning lades till i spårningsmallarna eller mål-URL:erna, eller så är spårningsprefixet felaktigt.

* Taggen för konverteringsspårning implementeras inte korrekt på alla tillämpliga webbsidor eller redigerades.

* Transaktionsegenskaperna som spåras av Search, Social och Commerce är exkluderade från rapporter och visas därför inte.

* Inkomstparsern för klienten implementerades inte.

*Möjlig lösning eller tillfällig lösning:*

1. Kontrollera att rätt kolumner inkluderas i rapporter eller datavyer. Om rätt kolumner inte är tillgängliga att lägga till måste du eller ditt Adobe-kontoteam [göra transaktionsegenskaperna tillgängliga för rapporter](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Kontrollera att rätt konverteringsspårningstaggar implementeras på alla tillämpliga webbsidor. Om det behövs kan du be ditt kontoteam på Adobe att skapa en testtransaktion för varje tillämplig spårningstagg för konvertering och att registrera information om transaktionen, till exempel `transactionid` och detaljer från cookien (t.ex. `trackingid`, `clickid`och så vidare).

1. Om [!UICONTROL Auto Upload] är inaktiverat för kampanjen och du har lagt till nyckelord eller annonser. Kontrollera sedan att du har skapat en spårningsmall eller en mål-URL som innehåller sök-, sociala och handelsklickningsspårning för varje. Kontoteamet på Adobe kan köra en intern rapport för att se om det finns klickspårnings-URL:er (spårningsmallar eller mål-URL:er) som saknas eller är felaktiga.

   Generera vid behov spårning genom att skapa en kalkylbladsfil med rätt URL:er och posta filen till rätt konto med hjälp av **Generera spårnings-URL:er** alternativ.

   Mål-URL:en ska börja med&quot;http://pixel.everesttech.net&quot; eller&quot;https://pixel.everesttech.net&quot;.

1. Om inget av dessa steg löser problemet kan du [kontakta Kundtjänst](/help/search-social-commerce/get-help.md).

   Om klienten inte har startats eller om den har startats nyligen verifierar kundtjänst om en intäktsparser har ställts in. Om parsern är konfigurerad kontrollerar de om Search, Social, &amp; Commerce tar emot pixelkonverteringar och felsöker problemet.

**Annonsörer som skickar konverteringsdataflöden**

*Möjliga orsaker:*

* Feed-filen levererades inte, den parsades inte helt eller så innehöll feeden överblivna transaktioner.

* De relevanta transaktionsegenskaperna utelämnas från rapporter och syns därför inte.

>[!NOTE]
>
>Data visas vanligtvis inte i användargränssnittet förrän 2-4 timmar efter att feeden har tagits emot.

*Möjlig lösning eller tillfällig lösning:*

1. Kontrollera att rätt kolumner inkluderas i rapporter eller datavyer. Om rätt kolumner inte är tillgängliga att lägga till måste du eller ditt Adobe-kontoteam [göra transaktionsegenskaperna tillgängliga för rapporter](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Kör [!UICONTROL Portfolio Report]. Om den är tom kör du [!UICONTROL Campaign Report] och [!UICONTROL Search Engine Report] för att se om intäkterna visas i dessa rapporter. Om den gör det kanske kampanjerna inte tilldelas rätt portfölj.

1. Kontrollera att filen skickades till intäktsservern och att filen följde samma format och filnamnsregler som tidigare filer.

   Om formatet eller namnkonventionen ändras korrigerar du filen och skickar den igen.

1. Om filen skickades [kontakta Kundtjänst](/help/search-social-commerce/get-help.md).

   Kundtjänst kontrollerar om filen har tagits emot och tolkats. Om filen bearbetades utan fel söker de efter överblivna transaktioner.
+++

+++Vissa avancerade rapporter innehåller inte konverteringsdata från en annonsörmatning.
The [!UICONTROL Geo Distribution Report] och [!UICONTROL Domain Referral Report] använda data som samlats in via tjänsten för spårning av konvertering till Adobe Advertising och kan genereras endast för annonsörer med tjänsten. Rapporterna innehåller inte konverteringsdata som spåras utanför Adobe Advertising-konverteringsspårningssystemet.
+++

+++Intäktsdata skiljer sig från annonsörens egna intäktsdata.

**Annonsörer som använder konverteringstaggar i Adobe Advertising**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien har gått ut eller tagits bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* Taggen för konverteringsspårning implementeras inte korrekt på alla tillämpliga webbsidor eller redigerades.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce tog emot med annonsörens data.

1. Om vissa transaktioner är felaktiga eller saknas kontrollerar du att den relevanta spårningstaggen för konvertering har implementerats på alla tillämpliga webbsidor och inte har redigerats om inte kontoteamet på Adobe har sagt att du ska göra det. En tagg kan saknas eller ändras om webbplatsen nyligen uppdaterades.

   För sökning, sociala medier och handel förväntas välformade URL:er (med parametrar i namnvärdespar) i `ef_transaction_properties` variabeln och inom `src` -elementet i `img` -tagg.

1. Om du inte kan fastställa och lösa problemet kan du [kontakta Kundtjänst](/help/search-social-commerce/get-help.md).

   Kundtjänst kommer att försöka identifiera de saknade transaktionerna och sedan söka efter enstaka transaktioner och transaktioner som inte kommer från en annons (&quot;okorrelerade konverteringar&quot;).

**Annonsörer med konverteringsdataflöden som använder `ef_id` values**

Se möjliga orsaker och lösningar för pixelimplementeringar ovan.

**Annonsörer med konverteringsdataflöden med transaktions-ID:n**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien förfaller eller tas bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* En offlinekonvertering rapporterades innan en onlinetransaktion med samma transaktions-ID inträffade. Onlinetransaktionen måste ske först.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce tog emot med annonsörens flödesuppgifter.

1. Om en transaktion i feed-filen saknas i rapporten kontrollerar du om en onlinetransaktion med samma transaktions-ID (spårad via pixeln) inträffade före offlinekonverteringen.

1. Om du inte kan fastställa och lösa problemet kan du [kontakta Kundtjänst](/help/search-social-commerce/get-help.md).

   Kundtjänst kommer att söka efter fel vid dataanalys och [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

**Annonsörer med andra typer av konverteringsdataflöden**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien har gått ut eller tagits bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* Det finns [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p)så Search, Social, &amp; Commerce räknar inte alla intäkter som det ska ha.

* Annonsören validerade en rapport för sökning, sociala medier och handel mot en annan uppsättning data än de skickade i flödet.

* Transaktions-ID:n (`ev_transid` värden) skickades inte, är inte unika eller är felaktiga.

* Feed-filen innehåller ID:n för dubblettspårning.

* Fel uppstod när filen parsades.

* Annonsörens dedupliceringslogik skiljer sig från logiken Sök, Social och Commerce.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce tog emot med annonsörens data.

1. Om vissa transaktioner är felaktiga eller saknas kontrollerar du att a) matningsfilen innehåller alla nödvändiga transaktions-ID:n och att inga dubbletter av spårnings-ID:n och b) transaktions-ID:n är unika och korrekta.

1. Om du inte kan fastställa och lösa problemet kan du [kontakta Kundtjänst](/help/search-social-commerce/get-help.md).

   Kundtjänst kommer att söka efter dataparsningsfel och överblivna transaktioner.
+++

+++Intäktsdata skiljer sig från data i Adobe Analytics Se [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Särskilda rapporter

+++Ska [!UICONTROL Portfolio Report] visa samma siffror som [!UICONTROL Portfolios] visa?
The [!UICONTROL Portfolio Report] och [!UICONTROL Portfolios] visar samma data när alla filter för vyn, rapportparametrarna och datakolumnerna för vyn och rapporten är desamma. Om [!UICONTROL Portfolios] visa portföljer som är[!UICONTROL All but inactive]&quot; för datumintervallet &quot;[!UICONTROL Last 7 days]&quot; och bara med de standarddatakolumner som visas, [!UICONTROL Portfolio Report] med standardparametrarna visas identiska data. Om du ändrar någon av rapportparametrarna eller använder andra filter i [!UICONTROL Portfolios] kan datavärdena vara olika.
+++

+++Data i [!UICONTROL Portfolio Report] matchar inte data i [!UICONTROL Search Engine Report] eller [!UICONTROL Search Engine Account Report].
The [!UICONTROL Portfolio Report] visar endast data för de kampanjer som har tilldelats de angivna portföljerna, men [!UICONTROL Search Engine Report] och [!UICONTROL Search Engine Account Report] kan även innehålla data för kampanjer som inte är tilldelade till en portfölj.
+++

+++Hur är [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] som skiljer sig från portföljnivån [!UICONTROL Model Accuracy Report]?
(Endast kontohanterare, kontohanterare på Adobe och administratörsanvändare) [!UICONTROL Forecast Accuracy Report] tillgänglig från [!UICONTROL Reports] > [!UICONTROL Model Accuracy] ger samma data som portföljnivån [!UICONTROL Model Accuracy Report] förutom att du kan köra det över flera portföljer och du kan ändra attribueringsregeln. Du kan också köra och schemalägga rapporten med anpassade parametrar, och du kan använda den för att skapa kalkylbladsflöden. Dessutom är [!UICONTROL Forecast Accuracy Report] är exaktare än den äldre portföljnivårapporten eftersom den utvärderar intäktsnoggrannheten med hjälp av portföljens historiska mål snarare än det nuvarande målet, och den ger mer korrekta uppgifter för den tillämpliga tidszonen.
+++

+++Data på annandenivå är inte tillgängliga för [!DNL Google Ads] dynamisk sökannons (DSA), prestanda max, smart shopping och [!DNL YouTube] kampanjer.
Annonsnätverken tillhandahåller inte den identifierare som krävs för att tilldela intäkter till en enskild annons för dessa kampanjer. Följaktligen är inte annonsnivådata tillgängliga för de kampanjtyperna i [!UICONTROL Ads] eller i [!UICONTROL Ad Variation Report]. Förvänta diskrepanser mellan den totala annonsnivån för en kampanj och kampanjens totala data.
+++

+++ I [!UICONTROL Transaction Report]Hur vet jag vilken transaktionsegenskap som kommer från en datafeed eller som spåras av Adobe Advertising-spårningspixeln?
I en transaktionsrapport kan du se om en inkluderad transaktionsegenskap spårades av spårningspixeln för Adobe Advertising om du inkluderar den anpassade kolumnen &quot;[!UICONTROL Tracking URL].&quot; Spåra URL:er med spårningspixeln Adobe Advertising börjar med`http://pixel.everesttech.net`.&quot;
+++

+++Data i [!UICONTROL Transaction Report] matchar inte data i [!UICONTROL Keyword Report].
När du genererar båda rapporterna per portfölj blir data annorlunda om du genererar [!UICONTROL Keyword Report] använda historiska data (d.v.s. baserat på portföljkonfigurationen under de angivna datumen) i stället för att använda data för aktuella kampanjer. När du genererar [!UICONTROL Transaction Report] per portfölj innehåller data för de aktuella kampanjerna i portföljen.
+++

## Kalkylbladsflöden

+++Rapport innehåller en blandning av datumintervall.
Du kan se olika datumintervall om feed aggregerar data med någon annan datagenereringsnivå än &quot;[!UICONTROL Daily].&quot;

Du löser problemet genom att uppdatera kalkylbladsflödet så att data samlas in dagligen. Den här uppgiften innefattar att uppdatera rapportmallen, generera en rapport med hjälp av mallen, skapa en anpassad [!DNL Microsoft® Excel] -mallen som använder rapporten och sedan uppdaterar feed-inställningarna så att de inkluderar den nya Excel-mallen. Mer information finns i &quot;[Redigera inställningar för matning av kalkylbladsrapporter](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Ett kalkylbladsflöde resulterar i ett internt fel.
Det här felet kan inträffa om du ändrar kolumnerna i rapportmallen men inte uppdaterar [!DNL Microsoft® Excel] i enlighet med detta.

Du löser problemet genom att uppdatera kalkylbladsflödet så att de nya kolumnerna inkluderas. Den här uppgiften innefattar att uppdatera rapportmallen, generera en rapport med hjälp av mallen, skapa en anpassad [!DNL Excel] -mallen som använder rapporten och sedan uppdaterar feed-inställningarna så att de inkluderar den nya Excel-mallen. Mer information finns i &quot;[Redigera inställningar för matning av kalkylbladsrapporter](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++När jag försöker öppna ett kalkylbladsflöde i [!DNL Excel], [!DNL Excel] rapporterar ett fel om oläsbart innehåll och data tas bort från det återskapade innehållet.
När [!DNL Microsoft® Excel] data sorteras inte efter startdatum i stigande ordning, kalkylbladsflödet kan innehålla tomma rader. Särskilt gäller följande: [!DNL Excel] rapporterar felet &quot;Excel hittade oläsligt innehåll i &#39;&lt;*rapportnamn*>.xlsx.&#39; Vill du återställa innehållet i arbetsboken? Om du litar på källan till arbetsboken klickar du på Ja.&quot; Om du klickar på Ja visas följande meddelande: &quot;Borttagna poster: Cellinformation från /xl/worksheets/sheet1.xml&quot; och kalkylbladsflödet innehåller tomma rader.

Du löser problemet genom att redigera [!DNL Excel] mall som är associerad med feeden för att sortera data efter [!DNL Start date in Ascending (Oldest to Newest) order]och överför sedan den uppdaterade mallen via inställningarna för kalkylbladsflöde. Mer information finns i &quot;[Redigera rapportflöden för kalkylblad](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
