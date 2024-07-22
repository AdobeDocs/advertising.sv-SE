---
title: Vanliga frågor om anpassade rapporter
description: Lär dig svar på vanliga frågor om prestandarapporter, inklusive felsökning av dataproblem.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Vanliga frågor om anpassade rapporter

## Allmänna frågor

+++Vad händer om datumintervallet för rapporten börjar innan rapportdata är tillgängliga?
Rapporten genereras, men innehåller bara data för de datum som det finns tillgängliga data för. Mer information om när data är tillgängliga för varje rapporttyp finns i [Data som används för rapporter](data-used-for-reports.md).
+++

+++Vad är skillnaden mellan datumbaserade rapporter och transaktionsrapporter?
När du rapporterar konverteringar efter transaktionsdatum inkluderar dessa data transaktioner vars transaktionsdatum inträffade under den angivna tidsperioden. Det här alternativet är standardinställningen i grundläggande rapporter och avancerade rapporter, och visar hur mycket intäkter som intjänats under den angivna tidsperioden.

När du rapporterar konverteringar med klickningsdatum innehåller data transaktioner som har skapats av ett klick som inträffade under den angivna tidsperioden. När en portfölj har betydande fördröjningar mellan klick och transaktioner visar den här typen av rapportering den historiska intäkten per klick för portföljen, vilket ger dig en uppfattning om vilka intäktsbeteenden du kan förvänta dig över tid.

![Rapportera per klickdatum kontra rapport per transaktionsdatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Rapportera per klickningsdatum kontra rapport per transaktionsdatum")
+++

+++Vad händer om jag ändrar fönstret för klicksökning eller fönstret för visningssökning?
(Annonsörer med Advertising pixelbaserad konverteringsspårningstjänst) Data för händelser som är ett resultat av den första klickningen samlas in under en längre eller kortare period.

En annonsörs [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j) avgör hur många dagar efter ett betalt klick eller ett visningsintryck (respektive) som händelsen kan tilldelas till en konvertering. Att ändra ett värde till en längre eller kortare period kan vara viktigt för annonsörer med särskilt korta eller långa klick-till-intäkt- eller visningsintryck-intäktsperioder.

**Bästa tillvägagångssätt:** Kontrollera att uppslagsfönstren är längre än&quot;click-to-revenue&quot; och att de visar intäktstider för de flesta av dina nyckelord eller annonser. När de är kortare är vissa konverteringar inte kopplade till den första klickningen eller det inledande intrycket.
+++

+++Hur vet jag vilka konverteringar som är resultatet av ett [!DNL Google Ads]-annonstillägg eller en produktlista?
Du kan se vilka konverteringar som är resultatet av ett klick på ett [!DNL Google Ads]-annonstillägg (i stället för på själva annonsen) eller på en produktlista genom att generera ett [!UICONTROL Transaction Report]. Kolumnvärdet [!UICONTROL Link Type] visar typ och rubrik för en länk som du klickade på:

* Produktlistor listas som `pla:<product ID>`, till exempel `pla:8525822`.

* Webbplatslänkar listas som `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.

  Du kan också identifiera en sitellänk om du tar med kolumnen [!UICONTROL Tracking URL] i rapporten. [!UICONTROL Tracking URL] för en sitelink innehåller attributet `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Konverteringar från [!DNL Google Ads] platser och telefontillägg inkluderas i data för de annonser som de följer. De rapporteras inte separat.

+++

+++Kolumnen [!UICONTROL Keyword] i min rapport innehåller värdet &quot;(adgroup content) &lt;*ad group name*>.&quot;
När raden innehåller data för innehållsaktiverade sökkampanjer, webbannonskampanjer eller sociala kampanjer - som inte innehåller nyckelord - visas i kolumnen [!UICONTROL Keyword] det tillämpliga annonsgruppsnamnet i stället.
+++

+++På grund av säsongsförändringar eller förändringar på marknaden visar mina rapporter atypiska data. Påverkar detta anbud när villkoren ändras?
Optimeringsfunktionen bygger sina intäktsmodeller för varje budenhet dagligen för att säkerställa att den identifierar och omedelbart reagerar på trender, och modellerna bygger på långsiktiga historiska data för att hjälpa till att förutsäga säsongsrelaterade resultat. Portföljens halveringstid för intäktsmodellen <!-- add link to glossary? --> avgör också hur kraftigt senaste intäktsdata viktas. Det bästa sättet är att minska halveringstiden under en period med atypiska resultat men öka den efter att intäktsmodellen har justerats. Om du har några frågor om huruvida det är nödvändigt att justera halveringstiden kontaktar du ditt Adobe-kontoteam.

Om du inte vill att data för perioden ska påverka framtida bud alls kan du välja att exkludera dessa datum från modellen. Kontakta kontoteamet på Adobe för att exkludera datum.
+++

+++Kan jag skapa en rapport för ett specifikt kontoegenskapsmått, till exempel [!UICONTROL Device] eller [!UICONTROL Objective Name]?
För kampanjentitetsrapporter ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] och [!UICONTROL Product Group Report]) aggregeras mätdata dynamiskt av egenskapskolumnerna som du inkluderar i rapporten. Du kan också ta bort rapportens nyckelkolumn och bara ta med de egenskapskolumner för vilka du vill samla in data.

Om du till exempel skapar en [!UICONTROL Keyword Report] som innehåller kolumnerna [!UICONTROL Ad Group] och  Device, aggregerar rapporten som standard mått för varje nyckelord per annonsgrupp och enhetstyp. Om du däremot tar bort kolumnen [!UICONTROL Keyword] innan du genererar rapporten, genererar rapporten dynamiskt mått för de angivna annonsgrupperna efter enhetstyp.

>[!NOTE]
>
>Du kan inte använda den här funktionen för att samla in data efter etikettklassificeringar. Alla etikettklassificeringskolumner i rapporten utelämnas. Använd i stället [Etikettklassificeringsrapporten](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Allmänna dataproblem

+++Rapporter som genereras med olika attribueringsregler visar olika summor.
Om du genererar en rapport flera gånger med samma rapportparametrar men med olika attribueringsregler, kan data skilja sig på grund av någon av följande orsaker:

* Datumbaserade klickdata kan ligga utanför det angivna datumintervallet.

  Om du använder rapportparametern [!UICONTROL Conversions based on click date] gäller det angivna datumintervallet för klickdatumet i stället för datumet för transaktionen. Om attribueringsregeln &quot;First Event&quot; eller &quot;Last Event&quot; också används i rapporten kan den första eller sista händelsen som ledde till konverteringen ligga utanför det angivna datumintervallet. Anta till exempel att en användare klickade på Nyckelord_1 den 30 april, klickade på Nyckelord_2 den 20 maj och konverterades den 21 maj. Om rapporten använder attribueringsregeln [!UICONTROL First Event] och datumintervallet 1-21 maj inkluderas inte den första händelsen (ett klick på Nyckelord_1 den 30 april) i rapporten. Om du kör rapporten med samma datumintervall men använder attribueringsregeln [!UICONTROL Last Event], inkluderas konverteringen i rapporten eftersom den senaste klickningen inträffade inom det angivna datumintervallet.

* Portföljfiltervalet utesluter vissa händelser som leder till konverteringen.

  Om du rapporterar om en delmängd av portföljer kanske du inte inkluderar kampanjer som innehöll händelsen som konverteringen tilldelades enligt någon av attribueringsreglerna. Anta att en användare klickar på Nyckelord_1 från Portfolio_1, klickar på Nyckelord_2 från Portfolio_2 och sedan konverterar. Om attribueringsregeln [!UICONTROL First Event] används i rapporten måste Portfolio_1 inkluderas för att konverteringen ska inkluderas i rapporten. Om attribueringsregeln &quot;Last Event&quot; används i rapporten måste Portfolio_2 inkluderas.

>[!TIP]
>
>Om du vill jämföra konverteringssummor enligt olika attribueringsregler kör du rapporter med rapportparametern [!UICONTROL Conversions based on transaction date] och väljer alla annonsnätverk eller alla portföljer. Om du inte anger några andra filter bör konverteringssummorna stämma överens.

+++

+++Enskilda datafält är felaktiga, men summorna är korrekta.
Detta kan inträffa när heltal används i mätformaten:

* Om du skapar ett [anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) med formatet *Number w/out Decimal Points* (som visar data som heltal) och inkluderar det i en vy eller i en rapport som använder en viktad konverteringsattribueringsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] eller [!UICONTROL Even Distribution]) visas utdata i heltal, inte i decimaler. I det här fallet kan enskilda datafält vara felaktiga, även om summorna är korrekta. Om en ordning till exempel fördelas jämnt mellan tre händelser, fördelas en ordning (i stället för 0,33) på var och en av de tre händelserna. Du löser problemet genom att [ändra måttformatet ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) till *Nummer till 2 decimalpunkter*.

* Om du har ett intäktsmått som skickas som heltal händer samma sak. (Intäktsformatet styrs av konverteringstaggen som skickar data.) Du löser problemet genom att [skapa ett anpassat mått ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) som består enbart av intäktsmåttet och med formatet *Nummer till 2 decimalpunkter*, och ta med det i vyer och rapporter i stället för i det ursprungliga måttet.
+++

+++Hur förhindrar jag att klicknings- eller intäktsdata påverkar framtida anbud?
Klicka på dataproblem när sökningen, sociala medier och Commerce inte är synkroniserade med annonsnätverket. Kontakta kontoteamet på Adobe om du vill synkronisera kontot manuellt. Om klickdata saknas för en hel dag ber du ditt Adobe-kontoteam att exkludera den dagen från kostnadsmodellerna.

Intäktsdataproblem kan uppstå på grund av ett problem med spårning eller feed-fil. Kontakta kontoteamet på Adobe för att undersöka problemet. Om intäktsdata saknas för en hel dag ber du ditt Adobe-kontoteam att exkludera den dagen från intäktsmodellerna.
+++

+++monetära data visas i fel format.
Som standard visas alla monetära data i rapporter i formatet för USD (till exempel 1 000,00). Om du vill visa värdet i rätt valutaformat (men utan valutasymboler i CSV- och TSV-format) lägger du till kolumnen [!UICONTROL Currency] i rapporten. Om rapporten innehåller data för konton med olika valutor är alla [!UICONTROL Total]-monetära värden bara summan av alla tal i kolumnen, oavsett valuta.
+++

+++Varför ser jag decimalvärden för ett konverteringsmått som ska vara ett naturligt tal (1, 2 och så vidare)?
Du kan se decimalvärden i följande fall:

* Om du har kört rapporten med någon annan parameter för konverteringsattribueringsregel än [!UICONTROL Last Event] eller [!UICONTROL First Event] kan intäkterna delas mellan flera händelser i konverteringssökvägen.

* Om flera [budenheter](/help/search-social-commerce/glossary.md#a-b) med olika matchningstyper i [!UICONTROL Transaction Report] har samma transaktions-ID delas intäkten för spårnings-ID upp enligt antalet klick på det angivna klickdatumet.
+++

## Standardprestanda, mått

+++Klicka-data saknas i rapporter.
Nedan följer några vanliga orsaker till att klickdata saknas.

| Orsak | Upptäckt/analys | Upplösning |
|---|---|---|
| Processen som hämtar klickdata från annonskontot misslyckades. | Det finns inget systematiskt sätt att upptäcka detta problem, men ni kanske märker att en kampanj inte visar någon kostnads- eller klickinformation trots att annonskontot spenderade pengar. | Kontakta kontoteamet på Adobe.<br><br>Om data saknas i mer än 24 timmar ska du utelämna dessa datum från kostnadsprognoserna tills data har hämtats. Kontoteamet på Adobe kan exkludera datum. |
| Ett faktureringsproblem mellan annonsören och annonsnätverket förhindrar annonskontot från att spendera pengar. | Det finns inget systematiskt sätt att upptäcka detta problem, men du kanske märker att en kampanj inte visar någon kostnads- eller klickinformation. | Om du vet att ett annonskonto inte kunde användas på grund av ett faktureringsproblem, ska du undanta dessa datum från kostnadsprognoserna. Kontoteamet på Adobe kan exkludera datum. |
+++

+++Prestandadata skiljer sig från data i annonsnätverkets redigerare.
När annonsnätverket skickar uppdateringar till tidigare data (ofta för att de har tilldelat klickbedrägeri) uppdaterar inte Search, Social och Commerce data om det inte finns mer än 5 % diskrepans och Adobe Account Team skickar en begäran.

När du jämför visningsdelningsdata som aggregerats över ett datumintervall kan de data som rapporteras i Search, Social och Commerce skilja sig från de data som annonsnätverket rapporterar. Skillnaden beror på hur data rapporteras av annonsnätverkets API, som används av Search, Social och Commerce för att hämta in data. För [!DNL Google Ads]-data:

* För de flesta visningsvärden delar [!DNL Google Ads] antingen den nedre eller övre delen av de värden som rapporteras för värden som är mindre än 10 % eller större än 90 %. Data rapporteras som 0,0999 för &lt;10% och 0,9001 för >90%

* När det finns en blandning av begränsade och obegränsade data inom datumintervallet delar Sökning, Sociala och Commerce-aggregerade visningsdata med hjälp av de värden som skickas i API:t i befintligt skick. 0,0999 används för rader med &lt;10% och 0,9001 för rader med >90 %. Den här aggregeringen kan resultera i en avvikelse från de [!DNL Google Ads] föraggregerade data eftersom [!DNL Google Ads] kan använda faktiska procentvärden, som 7 % eller 97 %.
+++

+++Prestandadata i rapporter skiljer sig från data i [!DNL Google Analytics].
De två systemen mäter olika data, så du bör förvänta dig att se olika data. Exempel:

* Sök, socialt och Commerce (och Google Ads) spårar klickningar, medan [!DNL Google Analytics] spårar besök per 30-minuters webbläsarsession. Om en användare till exempel klickar på din annons en gång, klickar på knappen Bakåt och sedan klickar på annonsen igen, registrerar Search, Social och Commerce två klick, men [!DNL Google Analytics] registrerar ett besök.

* [!DNL Google Analytics] visar alla trafikdata, medan Sök, Social och Commerce (och [!DNL Google Ads]) filtrerar ogiltiga klick (till exempel överflödiga, upprepade klick).

* [!DNL Google Analytics] innehåller klicknings- och intäktsdata för alla klick. Search, Social och Commerce kan inte spåra klicknings- och intäktsdata för annonser och nyckelord med felaktiga eller saknade spårnings-URL:er.
+++

## Konverteringsmått

+++Min rapport visar inga konverteringsdata.
Rapporten får inte innehålla konverteringsvärden för vilka konverteringar har gjorts.
+++

+++Intäkter saknas i rapporter.

**Annonsörer som använder konverteringstaggar för Adobe Advertising**

*Möjliga orsaker:*

* Nyckelord eller annonser lades till utan att prefixet Sök, Socialt och Commerce klickspårning lades till i spårningsmallarna eller mål-URL:erna, eller så är spårningsprefixet felaktigt.

* Taggen för konverteringsspårning implementeras inte korrekt på alla tillämpliga webbsidor eller redigerades.

* Konverteringsmåtten som Search, Social och Commerce spårar är exkluderade från rapporter och syns därför inte.

* Inkomstparsern för klienten implementerades inte.

*Möjlig lösning eller tillfällig lösning:*

1. Kontrollera att rätt kolumner inkluderas i rapporter eller datavyer. Om rätt kolumner inte är tillgängliga att lägga till måste du eller ditt Adobe-kontoteam [göra konverteringsmåtten tillgängliga för rapporter](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Kontrollera att rätt konverteringsspårningstaggar implementeras på alla tillämpliga webbsidor. Om det behövs kan du be ditt Adobe-kontoteam att skapa en testtransaktion för varje tillämplig konverteringsspårningstagg och att hämta information om transaktionen, som `transactionid` och information från cookien (som `trackingid`, `clickid` och så vidare).

1. Om alternativet [!UICONTROL Auto Upload] är inaktiverat för kampanjen och du har lagt till nyckelord eller annonser, kontrollerar du att du har genererat en spårningsmall eller mål-URL som innehåller sök-, sociala och Commerce-klickspårning för varje. Kontoteamet på Adobe kan köra en intern rapport för att se om det finns klickspårnings-URL:er (spårningsmallar eller mål-URL:er) som saknas eller är felaktiga.

   Generera vid behov spårning genom att skapa en kalkylbladsfil med rätt URL:er och posta filen till rätt konto med alternativet **Skapa spårnings-URL:er** .

   Mål-URL:en ska börja med&quot;http://pixel.everesttech.net&quot; eller&quot;https://pixel.everesttech.net&quot;.

1. Om inget av dessa steg löser problemet kontaktar [kundtjänst](/help/search-social-commerce/get-help.md).

   Om klienten inte har startats eller om den har startats nyligen verifierar kundtjänst om en intäktsparser har ställts in. Om parsern är konfigurerad kontrollerar de om Search, Social och Commerce tar emot pixelkonverteringar och felsöker problemet.

**Annonsörer som skickar konverteringsdataflöden**

*Möjliga orsaker:*

* Feed-filen levererades inte, den parsades inte helt eller så innehöll feeden överblivna transaktioner.

* De relevanta konverteringsvärdena ingår inte i rapporterna och syns därför inte.

>[!NOTE]
>
>Data visas vanligtvis inte i användargränssnittet förrän 2-4 timmar efter att feeden har tagits emot.

*Möjlig lösning eller tillfällig lösning:*

1. Kontrollera att rätt kolumner inkluderas i rapporter eller datavyer. Om rätt kolumner inte är tillgängliga att lägga till måste du eller ditt Adobe-kontoteam [göra konverteringsmåtten tillgängliga för rapporter](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Kör [!UICONTROL Portfolio Report]. Om den är tom kör du [!UICONTROL Campaign Report] och [!UICONTROL Search Engine Report] för att se om intäkten visas i rapporterna. Om den gör det kanske kampanjerna inte tilldelas rätt portfölj.

1. Kontrollera att filen skickades till intäktsservern och att filen följde samma format och filnamnsregler som tidigare filer.

   Om formatet eller namnkonventionen ändras korrigerar du filen och skickar den igen.

1. Om filen skickades [kontaktar du kundtjänst](/help/search-social-commerce/get-help.md).

   Kundtjänst kontrollerar om filen har tagits emot och tolkats. Om filen bearbetades utan fel söker de efter överblivna transaktioner.
+++

+++Vissa avancerade rapporter innehåller inte konverteringsdata från en annonsörmatning.
[!UICONTROL Geo Distribution Report] och [!UICONTROL Domain Referral Report] använder data som hämtats via tjänsten för spårning av konvertering till Adobe Advertising och kan bara genereras för annonsörer som har tjänsten. Rapporterna innehåller inte konverteringsdata som spåras utanför Adobe Advertising-konverteringsspårningssystemet.
+++

+++Intäktsdata skiljer sig från annonsörens egna intäktsdata.

**Annonsörer som använder konverteringstaggar för Adobe Advertising**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien har gått ut eller tagits bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* Taggen för konverteringsspårning implementeras inte korrekt på alla tillämpliga webbsidor eller redigerades.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce har tagit emot med annonsörens data.

1. Om vissa transaktioner är felaktiga eller saknas kontrollerar du att den relevanta spårningstaggen för konvertering har implementerats på alla tillämpliga webbsidor och inte har redigerats om inte kontoteamet på Adobe har sagt att du ska göra det. En tagg kan saknas eller ändras om webbplatsen nyligen uppdaterades.

   För Sök, Socialt och Commerce förväntas URL:er med rätt format (med parametrar i namnvärdespar) i variabeln `ef_transaction_properties` och i elementet `src` i taggen `img`.

1. [Kontakta kundtjänst](/help/search-social-commerce/get-help.md) om du inte kan fastställa och lösa problemet.

   Kundtjänst kommer att försöka identifiera de saknade transaktionerna och sedan söka efter enstaka transaktioner och transaktioner som inte kommer från en annons (&quot;okorrelerade konverteringar&quot;).

**Annonsörer med konverteringsdataflöden som använder `ef_id` values**

Se möjliga orsaker och lösningar för pixelimplementeringar ovan.

**Annonsörer med konverteringsdataflöden med transaktions-ID:n**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien förfaller eller tas bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* En offlinekonvertering rapporterades innan en onlinetransaktion med samma transaktions-ID inträffade. Onlinetransaktionen måste ske först.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce har tagit emot med annonsörens flödesuppgifter.

1. Om en transaktion i feed-filen saknas i rapporten kontrollerar du om en onlinetransaktion med samma transaktions-ID (spårad via pixeln) inträffade före offlinekonverteringen.

1. [Kontakta kundtjänst](/help/search-social-commerce/get-help.md) om du inte kan fastställa och lösa problemet.

   Kundtjänst kommer att söka efter dataparsningsfel och [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

**Annonsörer med andra typer av konverteringsdataflöden**

*Möjliga orsaker:*

* Search, Social och Commerce ignorerar intäkter när cookien har gått ut eller tagits bort, men annonsören kan anse att den är giltig.

* Trafiken till annonsörens sida kom från ett bokmärke eller en organisk sökning istället för från en annons.

* Det finns [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p), så Search, Social och Commerce räknar inte alla intäkter som de ska ha.

* Annonsören validerade en Search-, Social- och Commerce-rapport mot en annan uppsättning data än de skickade i feeden.

* Transaktions-ID:n (`ev_transid` värden) skickades inte, är inte unika eller är felaktiga.

* Feed-filen innehåller ID:n för dubblettspårning.

* Fel uppstod när filen parsades.

* Annonsörens dedupliceringslogik skiljer sig från logiken i Search, Social och Commerce.

*Möjlig lösning eller tillfällig lösning:*

1. Gå till **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** och generera en [!UICONTROL Transaction Report]. Jämför de transaktioner som Search, Social och Commerce har tagit emot med annonsörens data.

1. Om vissa transaktioner är felaktiga eller saknas kontrollerar du att a) matningsfilen innehåller alla nödvändiga transaktions-ID:n och att inga dubbletter av spårnings-ID:n och b) transaktions-ID:n är unika och korrekta.

1. [Kontakta kundtjänst](/help/search-social-commerce/get-help.md) om du inte kan fastställa och lösa problemet.

   Kundtjänst kommer att söka efter dataparsningsfel och överblivna transaktioner.
+++

+++Intäktsdata skiljer sig från data i Adobe Analytics
Se [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Särskilda rapporter

+++Ska [!UICONTROL Portfolio Report] visa samma siffror som vyn [!UICONTROL Portfolios]?
[!UICONTROL Portfolio Report]- och [!UICONTROL Portfolios]-vyn visar samma data när alla filter för vyn, rapportparametrarna och datakolumnerna för vyn och rapporten är desamma. Om [!UICONTROL Portfolios]-vyn till exempel visar portföljer som är [!UICONTROL All but inactive] för datumintervallet [!UICONTROL Last 7 days] och endast innehåller standarddatakolumner, visar en [!UICONTROL Portfolio Report] som använder standardparametrarna identiska data. Om du ändrar någon av rapportparametrarna eller använder andra filter i vyn [!UICONTROL Portfolios] kan datavärdena vara olika.
+++

+++Data i min [!UICONTROL Portfolio Report] matchar inte data i min [!UICONTROL Search Engine Report] eller [!UICONTROL Search Engine Account Report].
[!UICONTROL Portfolio Report] visar endast data för de kampanjer som har tilldelats de angivna portföljerna, men [!UICONTROL Search Engine Report] och [!UICONTROL Search Engine Account Report] kan även innehålla data för kampanjer som inte har tilldelats en portfölj.
+++

+++Hur skiljer sig [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] från portföljnivån [!UICONTROL Model Accuracy Report]?
(Endast för kontohanterare, kontohanterare för Adobe och administratörsanvändare) [!UICONTROL Forecast Accuracy Report] som är tillgänglig från [!UICONTROL Reports] > [!UICONTROL Model Accuracy] tillhandahåller samma data som portföljnivån [!UICONTROL Model Accuracy Report] förutom att du kan köra den över flera portföljer och du kan ändra attribueringsregeln. Du kan också köra och schemalägga rapporten med anpassade parametrar, och du kan använda den för att skapa kalkylbladsflöden. Dessutom är [!UICONTROL Forecast Accuracy Report] mer exakt än den äldre portföljnivårapporten eftersom den utvärderar intäktsnoggrannheten med hjälp av portföljens historiska mål i stället för det aktuella målet, och ger en mer korrekt bild av data för den aktuella tidszonen.
+++

+++Ad-nivå-data är inte tillgängliga för [!DNL Google Ads] dynamisk sökannons (DSA), prestandamängd, smart shopping och [!DNL YouTube] kampanjer.
Annonsnätverken tillhandahåller inte den identifierare som krävs för att tilldela intäkter till en enskild annons för dessa kampanjer. Följaktligen är annonsnivådata inte tillgängliga för de kampanjtyperna i vyn [!UICONTROL Ads] eller i vyn [!UICONTROL Ad Variation Report]. Förvänta diskrepanser mellan den totala annonsnivån för en kampanj och kampanjens totala data.
+++

+++I [!UICONTROL Transaction Report], hur vet jag vilken konverteringsmetod som kommer från en datafeed eller som spåras av Adobe Advertising-spårningspixeln?
I en transaktionsrapport kan du se om ett inkluderat konverteringsmått spårades av spårningspixeln för Adobe Advertising om du inkluderar den anpassade kolumnen [!UICONTROL Tracking URL]. Spårnings-URL:er med spårningspixeln för Adobe Advertising börjar med `http://pixel.everesttech.net`.
+++

+++Data i min [!UICONTROL Transaction Report] matchar inte data i min [!UICONTROL Keyword Report].
När du genererar båda rapporterna per portfölj, skiljer sig data åt om du genererar [!UICONTROL Keyword Report] med historiska data (d.v.s. baserat på portföljkonfigurationen under de angivna datumen) i stället för att använda data för de aktuella kampanjerna. När du genererar [!UICONTROL Transaction Report] efter portfölj inkluderas data för de aktuella kampanjerna i portföljen.
+++

## Kalkylbladsflöden

+++Rapport innehåller en blandning av datumintervall.
Du kan se olika datumintervall om feeden aggregerar data med någon annan datamängdsnivå än [!UICONTROL Daily].

Du löser problemet genom att uppdatera kalkylbladsflödet så att data samlas in dagligen. Den här aktiviteten omfattar uppdatering av rapportmallen, generering av en rapport med hjälp av mallen, skapande av en anpassad [!DNL Microsoft Excel]-mall med hjälp av rapporten och uppdatering av feed-inställningarna så att de inkluderar den nya Excel-mallen. Mer information finns i &quot;[Redigera inställningar för kalkylbladsrapportfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

+++Ett kalkylbladsflöde resulterar i ett internt fel.
Det här felet kan inträffa om du ändrar kolumnerna i rapportmallen men inte uppdaterar [!DNL Microsoft Excel]-mallen därefter.

Du löser problemet genom att uppdatera kalkylbladsflödet så att de nya kolumnerna inkluderas. Den här aktiviteten omfattar uppdatering av rapportmallen, generering av en rapport med hjälp av mallen, skapande av en anpassad [!DNL Excel]-mall med hjälp av rapporten och uppdatering av feed-inställningarna så att de inkluderar den nya Excel-mallen. Mer information finns i &quot;[Redigera inställningar för kalkylbladsrapportfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

+++När jag försöker öppna en kalkylbladsfeed i [!DNL Excel] rapporterar [!DNL Excel] ett fel om oläsbart innehåll och data tas bort från det återskapade innehållet.
När mallen [!DNL Microsoft Excel] inte sorterar data efter startdatum i stigande ordning kan kalkylbladsflödet innehålla tomma rader. I synnerhet rapporterar [!DNL Excel] felet &quot;Excel hittade oläsligt innehåll i &quot;&lt;*rapportnamn*>.xlsx&quot;. Vill du återställa innehållet i arbetsboken? Om du litar på källan till arbetsboken klickar du på Ja.&quot; Om du klickar på Ja visas följande meddelande: &quot;Borttagna poster: Cellinformation från /xl/worksheets/sheet1.xml&quot; och kalkylbladsflödet innehåller tomma rader.

Lös problemet genom att redigera mallen [!DNL Excel] som är associerad med feeden för att sortera data efter [!DNL Start date in Ascending (Oldest to Newest) order] och sedan överföra den uppdaterade mallen via inställningarna för kalkylbladsfeeden. Mer information finns i &quot;[Redigera rapportflöden för kalkylblad](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++
