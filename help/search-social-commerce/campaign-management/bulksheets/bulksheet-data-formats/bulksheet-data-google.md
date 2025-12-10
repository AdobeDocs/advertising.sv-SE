---
title: Obligatoriska kalkylbladsdata för  [!DNL Google Ads] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för  [!DNL Google Ads] konton.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '7898'
ht-degree: 0%

---

# Bilaga - Obligatoriska balansräkningsdata för [!DNL Google Ads]-konton

Om du vill skapa och uppdatera [!DNL Google Ads]-kampanjdata i grupp kan du använda skalkylbladsfiler för sökning, sociala medier och Commerce som är särskilt formaterade för [!DNL Google Ads]-konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det filformat som krävs eller b) skapa dem manuellt (mer information om vilka filformat som stöds finns i [Filformat som stöds i bulkblad](bulksheet-file-formats.md)).

Varje kalkylblad måste innehålla rubrikfält och motsvarande datafält som krävs för de [specifika åtgärder som du vill utföra](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (till exempel skapa en annons). När ett fält inte är obligatoriskt kan du utesluta det från rubriken och dataraderna. Alla anpassade kolumner tas bort när du överför bulkbladsfilen.

Nedan följer en tabell över alla tillgängliga datafält och ytterligare tabeller som anger vilka fält som krävs för att lägga till, redigera eller ta bort data för enskilda enheter (till exempel kampanjer och nyckelord).

## Alla tillgängliga datafält {#bulksheet-fields-all-google}

I följande tabell beskrivs alla tillgängliga datafält.

Information om de datafält som är relevanta för kontoentiteter finns i [Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent](#bulksheet-fields-per-component-google).

>[!NOTE]
>
>* Värdena i alla textkolumner är skiftlägeskänsliga.
>* När du skapar en ny post och inte inkluderar värden för alla obligatoriska datafält, tilldelas vissa av dessa fält de angivna standardvärdena.
>* För fält som inte anges nedan används standardvärdet för annonsnätverket.
>* En lista över tillgängliga kalkylbladsrader i dialogrutan [!UICONTROL Download Bulksheet] finns i &quot;[Bulkbladsrader per annonsnätverk](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)&quot;.

| Fält | Beskrivning |
| ---- | ---- |
| [!UICONTROL Platform] | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Acct Name] | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Campaign Budget] | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| [!UICONTROL Delivery Method] | <p>Så här visar du annonser för kampanjen varje dag:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (standard för nya kampanjer): För att sprida annonsintrycken över dagen.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (borttagen i oktober 2019) Om du vill visa dina annonser så ofta som möjligt tills din budget är nådd. Därför kanske era annonser inte visas senare under dagen.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>De kanaler där annonser ska placeras. Ange ett eller flera alternativ:</p><ul><li><p><i>[!UICONTROL Search]</i> (standard för nya kampanjer): Om du vill placera annonser i söknätverket [!DNL Google Ads] (inklusive [!DNL Google Ads] partnerwebbplatser för sökning och sökning) och eventuellt även i visningsnätverket [!DNL Google Ads]. <b>Obs!</b> Kampanjer som riktar sig till både söknätverket och visningsnätverket kan inte läggas till i en portfölj för anbudsoptimering.</p></li><li><p><i>[!UICONTROL Display]</i>: Om du bara vill placera annonser i visningsnätverket [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i>: Om du vill placera shoppingannonser i [!DNL Google Ads] shoppingnätverket (i vissa länder) och i söknätverket [!DNL Google Ads] (inklusive [!DNL Google Ads] partnerwebbplatser för sökning och sökning). Om du vill skapa shoppingannonser måste du ha produkter på ett [!DNL Google Merchant Center]-konto och [tillåta att data hämtas från kontot](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) via Search, Social och Commerce. Mer information om hur du skapar shoppingannonser finns i [Implementera [!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).</p></li></ul> |
| [!UICONTROL Networks] | <p>Var annonserna ska placeras. Ange ett eller flera alternativ:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Sponsrade söklistor endast på Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: Sponsrade söklistor på Google sökpartners.</p></li><li><p><i>[!UICONTROL Content]</i>: Om du vill lägga bud för visningsnätverkslistorna.</p></li><li><p><i>[!UICONTROL All]</i> (standard för nya kampanjer): Målgruppssökningar, sökpartners och innehåll för Google.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Endast söknätverk, endast tillgängligt för expanderade dynamiska sökannonser) Rotdomänen (till exempel example.com) eller underdomänen (till exempel shoes.example.com) för webbplatsen vars innehåll annonsnätverket använder för att rikta dina dynamiska sökannonser.<br><br><b>Anteckningar:</b></p><ul><li><p>Utökade dynamiska sökannonser målar webbinnehåll i stället för nyckelord.</p></li><li><p>Din domän måste indexeras av annonsnätverkets organiska sökindex för att kunna anges som mål.</p></li><li><p>Om du inte anger någon domän måste du skapa dynamiska sökmål som är avsedda för alla dina webbplatssidor eller en delmängd av dem för varje annonsgrupp.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Endast söknätverk, endast tillgängligt för expanderade dynamiska sökannonser) Språket för den angivna webbplatsdomänen. <b>Obs!</b> Om domänen innehåller sidor på flera språk och du vill ha alla som mål, skapar du en separat kampanj för varje språk. |
| [!UICONTROL GDN Custom Bid Level] | (Kampanjer som endast riktar sig till visningsnätverket) Så här lägger du ett bud: av <i>[!UICONTROL Ad Group]</i> (standard), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (webbplats) eller <i>[!UICONTROL None]</i> (för att återställa det befintliga värdet). Andra dimensioner (<i>Ålder</i>, <i>Kön</i>, <i>Intresse och Lista</i>, <i>Ämne</i> och <i>Lodrätt</i>) är tillgängliga från gränssnittet [!DNL Google Ads]. Om du har använt gränssnittet [!DNL Google Ads] för att konfigurera budgivning med en annan dimension visas det värdet, men du kan inte välja eller ange de dimensionerna här.</p><p><b>Obs!</b></p><ul><li><p>När du lägger ett bud med nyckelord skapar du spårningsmallar på nyckelordsnivå. På samma sätt kan du skapa spårningsmallar på placeringsnivå när du lägger ett bud per placering. För alla andra dimensioner skapar du spårningsmallar på annonsnivå.</p></li><li><p>När du lägger ett bud i en dimension som inte stöds (ålder, kön, ränta och lista eller ämne) optimerar inte Search, Social och Commerce anbud för dimensionen och all attribuering tillämpas på annonsgruppen.</p></li><li><p>I annonser i söknätverket används alltid nyckelordsbud.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Endast köpkampanjer) Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt: <i>[!UICONTROL Low]</i> (standard för nya kampanjer), <i>[!UICONTROL Medium]</i> eller <i>[!UICONTROL High]</i>.</p><p>När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad. |
| [!UICONTROL Has EU Political Ads] | (Gäller för kampanjer som riktar sig till målgrupper i EU) Huruvida kampanjen innehåller politisk annonsering per krav för annonser som tjänstgör i EU enligt EU:s förordning 2024/90: <i>[!UICONTROL Yes]</i> eller <i>[!UICONTROL No]</i>. |
| [!UICONTROL Merchant ID] | (Kundkampanjer och målgruppskampanjer som endast är kopplade till en handlarfeed) Kund-ID för det handlarkonto vars produkter används för kampanjen. |
| [!UICONTROL Sales Country] | (Endast köpkampanjer; skrivskyddat för befintliga kampanjer) Det land där kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen. |
| [!UICONTROL Product Scope Filter] | (Kampanjer som endast använder shoppingnätverket [!DNL Google Ads]) De produkter i ditt [!DNL Google Merchant Center]-konto för vilka det går att skapa shoppingannonser för kampanjen. Du kan ange upp till sju produktdimensioner och attributkombinationer där du kan filtrera dina produkter med formatet dimension=attribut. Avgränsa flera filter med avgränsaren &quot;>>&quot;. En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanj](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.</p><p>Exempel: &quot;KategoriL1=djur>>KategoriL2=djurmaterial>>Varumärke=Ätdjursmaterial&quot;</p><p>Om du vill ta bort befintliga värden använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p> |
| [!UICONTROL Languages] | <p>(Endast sök- och visningsnätverk) Målspråken för annonser i kampanjen.</p><p>Om du inte anger något värde för antingen det här fältet eller fältet [!UICONTROL Geo Targeting] för en ny kampanj, avgör den valuta som anges för kontot standardspråken, förutom att kampanjer med valutor som inte är mappade till specifika språk (till exempel EUR) är riktade till alla språk. Om du inte anger något värde för det här fältet utan anger ett värde i fältet [!UICONTROL Geo Targeting] för en ny kampanj blir standardvärdet <i>[!UICONTROL All]</i>. Om du lämnar det här fältet tomt för en befintlig kampanj behålls det befintliga värdet.</p><p>Om du vill ange alla språk som mål anger du <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Om du vill ange särskilda språk som mål anger du värden som avgränsas med semikolon med antingen <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] språknamn </a> (till exempel <i>Engelska;Japanska</i> som ersätts med rätt numeriska koder) eller numeriska koder (till exempel <i>1000;1005</i>). Värdena är inte skiftlägeskänsliga.</p> |
| [!UICONTROL Location] | En geografisk plats där annonser, eller för vilken annonser, ska uteslutas, ska placeras för kampanjen. Om du inte anger några värden för det här fältet eller fältet Språk för en ny kampanj, avgör den valuta som anges för kontot standardplatserna, förutom att kampanjer med valutor som inte är mappade till specifika platser (till exempel EUR) är riktade till alla platser. Om du inte anger något värde för det här fältet men anger ett värde i fältet [!UICONTROL Languages] för en ny kampanj blir standardvärdet <i>[!UICONTROL All]</i>. Om du lämnar det här fältet tomt för en befintlig kampanj behålls det befintliga värdet.</p><p>Om du vill ange en specifik plats som mål använder du ett av [[!DNL Google Ads] platsnamn](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (som ersätts med rätt numerisk kod) eller platskoder:</p><ul><li><p>Länder/territorier: Ange namn på land/territorium (till exempel <i>USA;Japan</i>) eller numeriska koder (till exempel <i> 2840;2392</i>).</p></li><li><p>Stater/provinser/regioner: Ange namn på delstat/provins/region med relaterade förkortningar av land/territorium (t.ex. <i>Tokyo, JP;New York, US</i>) eller numeriska koder (t.ex. <i>20636;21167</i>).</p></li><li><p>Stater utanför USA: Ange namn på ort, stat/provins/region och förkortningar av land/territorium (t.ex. <i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i>) eller numeriska koder (t.ex. <i>1028850;1009293</i>)</p></li><li><p>Amerikanska tunnelbaneområden: Ange stadsnamn, delstatsnamn och landsförkortningar (t.ex. <i>Buffalo NY, US;New York NY, US</i>) eller numeriska koder (t.ex. <i>514;501</i>).</p></li></ul><p>Om du vill utesluta en plats skriver du ett minustecken (`-`) före platsnamnet eller koden, till exempel <i>-Japan </i>.</p><p><b>Obs!</b> Värdena är inte skiftlägeskänsliga.</p> |
| [!UICONTROL Location Type] | (När du inkluderar en plats) Platstypen [](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | En enhetstyp för vilken anbudsjusteringar görs på kampanj- eller annonsgruppsnivå: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> eller <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(När du inkluderar ett [!UICONTROL Location]-, [!UICONTROL Device]- eller [!UICONTROL RLSA]-mål) Om du vill justera annonserna för annonser på en viss plats, på en viss enhetstyp eller med ett visst målgruppsmål:</p><ul><li><p>Ange 0 om du vill använda nyckelordsbudskapet (differens på 0 %). För nya mål kan du också lämna detta tomt.</p></li><li><p>Om du vill använda ett annat bud för detta mål anger du den procentandel med vilken anbuden ska ökas eller minskas.</p></li><ul><li><p>För plats- och RLSA-mål är giltiga procenttal mellan -90 och 900.</p></li><li><p>Giltiga procentsatser för justeringar av enhetsbud är:</p></li><ul><li><p>(Campaigns)-100 (to not bid for ads on the device type) eller från -90 till 900.</p></li><li><p>(Annonsgrupper) -100 för smarttelefoner och surfplattor (men inte för enhetstypen) och från -90 till 900 för alla enhetstyper.</p></li></ul></ul><li><p>(Befintliga kampanjer och annonsgrupper) Om du vill använda den befintliga budjusteringen lämnar du detta tomt.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Ingår i genererade kalkylblad i informationssyfte) Den skrivskyddade budjustering som Adobe rekommenderar för ett platsmål på kampanjnivå eller en RLSA. Den beräknas bara när kampanjen finns i en portfölj med ett mål som använder viktade konverteringsvärden (inte [!UICONTROL Maximize Clicks]-målet) och kampanjen innehåller minst två platsmål eller RLSA med minst fem klick eller 5 USD i kostnad under de senaste 90 dagarna.</p><p>Om du vill redigera ett platsmål manuellt eller RLSA manuellt för att använda det rekommenderade värdet väntar du minst två veckor efter att du har skapat platsmålet eller RLSA för att tillåta tillräcklig datainsamling och ändrar inte värdet mer än en gång i veckan. |
| [!UICONTROL Device Targets] | <p>(Endast äldre kampanjtyper) De enheter där annonsen kan visas: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> eller <i>[!UICONTROL Tablets]</i>. För nya kampanjer är standardvärdet <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Gäller endast äldre kampanjtyper. Gäller när enhetsmålen omfattar &quot;Smartphones&quot; eller &quot;Tablets&quot;) De operativsystem där annonsen kan visas: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> eller <i>[!UICONTROL Palm]</i>. För nya kampanjer är standardvärdet <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Endast äldre kampanjtyper; gäller när [!UICONTROL Device Targets] innehåller [!UICONTROL All] eller [!UICONTROL Smartphones]) Mobilbärare som smarttelefonerna kan vara anslutna till: <i>[!UICONTROL All]</i>, eller en eller flera bärare som anges av &lt;c<i>transportföretagskod</i>>,&lt;<i>landskod</i>> (t.ex. T-Mobile, USA) med hjälp av listan <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">tillgängliga bärare och koder för [!DNL Google Ads]</a>. Avgränsa flera bärare med semikolon (t.ex. T-Mobile, US;T-Mobile, GB). För nya kampanjer är standardvärdet <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Det unika namn som identifierar en annonsgrupp. Maximala längden är 255 tecken. Efterföljande tomma tecken sparas inte (till exempel sparas&quot;Annonsgrupp 1&quot; som&quot;Annonsgrupp 1&quot;). Det här fältet gäller inte för sitelinks på kampanjnivå eller enhetsmål på kampanjnivå.</p> |
| [!UICONTROL Ad Group Type] | <p>Annonsgruppstypen: <i>[!UICONTROL Demand Gen]</i> (endast för efterfrågegenereringskampanjer), <i>[!UICONTROL Display]</i> (för displaykampanjer), <i>[!UICONTROL Search Dynamic]</i> (för expanderade dynamiska sökannonser), <i>[!UICONTROL Search Standard]</i> (för sökannonser), <i>[!UICONTROL Shopping Product]</i> (för butiksproduktannonser), <i>[!UICONTROL Shopping Showcase]</i> (skapande och redigering stöds inte) eller <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Endast CPC-kampanjer) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för ett reklamklick i annonsnätverket, med eller utan monetära symboler och interpunktion. Du kan ange värden för annonsgrupper och nyckelord, produktgrupper och dynamiska sökmål. Standardvärdet för ett nytt nyckelord ärvs från annonsgruppsnivån. För produktgrupper kan du ange värden för den lägsta produktgruppsnivån. Standardvärdet för en ny nivå ärvs från den överordnade nivån.</p><p>För befintliga produktgrupper och dynamiska sökmål i optimerade portföljer gäller uppdateringarna endast en dag och skrivs över under nästa optimeringscykel.</p> |
| [!UICONTROL Max Content CPC] | <p>(Endast CPC-kampanjer) Den maximala innehållskostnaden per klick (CPC), som är den högsta summan att betala för ett reklamklick från en webbplats för webbannonser, med eller utan monetära symboler och interpunktion. Ni kan ange och redigera värden på annonsgruppsnivå i kampanjer som inte är riktade mot någon placering.</p> |
| [!UICONTROL Audience Target Method] | <p>(Kampanjer endast i söknätverket och befintliga, skrivskyddade [!DNL Gmail]-kampanjer i visningsnätverket) Om du vill:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: Om du bara vill visa annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: Om du vill visa annonser även för personer som inte är associerade med målgrupper så länge de uppfyller andra annonsnivåmål.</p><p>Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.</p></li></ul> |
| [!UICONTROL Keyword] | Nyckelordssträngen. Maxlängden är 80 tecken och inte fler än 10 ord, och den kan endast innehålla bokstäver, siffror och följande specialtecken: blanksteg `# $ & _ - " [ ] ' + . / :`</p><p><b>Obs!</b></p><ul><li><p>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du [!UICONTROL Match Type] till <i>[!UICONTROL Negative]</i>. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas nyckelordet för hela kampanjen.</p></li><li><p>Om du ändrar ett [!DNL Google Ads]-nyckelord eller en matchningstyp tas det befintliga nyckelordet bort och ett nytt skapas.</p></li></ul> |
| [!UICONTROL Placement] | (Kampanjer som endast använder innehållsmatchning) En placering i det visningsnätverk där annonserna kan visas. Ange något av följande:</p><ul><li><p>Webbplats: Ange en giltig URL. Det kan vara en toppnivådomän, underdomän på första nivån eller domän med ett enda katalognamn. URL:en får inte innehålla ett frågetecken (?). Exempel:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>En annonsposition på en viss sida: Använd formatet `<URL> >> <location,sublocation>` (till exempel `finance.google.com >> Company pages,Top right`).</p></li><li><p>En ämneskategori: Använd syntaxen `<category::<category> > <subcategory>` och så vidare (till exempel `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Obs!</b> Om du vill exkludera en placering på annonsgrupps- eller kampanjnivå anger du [!UICONTROL Match Type] till <i>[!UICONTROL Negative]</i>. Om raden innehåller annonsgruppens namn exkluderas placeringen för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas placeringen för hela kampanjen.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Krävs när kampanjinställningen [!UICONTROL Use my website contents to target my ads] inte är aktiverad. Annars är det valfritt) Dynamiska sökmål för annonsgruppen.</p><p>Använd en asterisk för alla mål (*).</p><p>Om du vill ha upp till tre dynamiska sökvillkor använder du formatet `<category>=<target>`, där `<category>` kan inkludera någon av kategorierna nedan. Koppla samman flera mål för en enskild kategori med &quot;\[blanksteg\] och \[blanksteg\]&quot; och förena flera kategorier med &quot;[blanksteg] och [blanksteg]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med en specifik [!DNL Google Ads] innehållskategori.</p></li><li><p><i>[!UICONTROL URL]</i>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.</p></li><li><p><i>[!UICONTROL Page Title]</i>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med specifik text i sidrubriken.</p></li><li><p><i>[!UICONTROL Page Content]</i>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med specifikt innehåll.</p></li></ul><p>Exempel: url=shoes.example.com och page title=skos</p> |
| [!UICONTROL Parent Product Groupings] | Hierarkin för överordnade produktgrupper.<br><br>Exempel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Produktgruppen (till exempel&quot;brand=acme&quot; eller&quot;Alla produkter&quot;).</p><p><b>Obs!</b></p><ul><li><p>När en angiven produktgrupp inte finns i hierarkin [!UICONTROL Parent Product Groupings] skapar Search, Social och Commerce alla delar av hierarkin som behövs.</p></li><li><p>Search, Social och Commerce skapar automatiskt en [!UICONTROL All Products]-grupp när du skapar en annonsgrupp i en [!DNL Google Ads]-shoppingkampanj med ett standardbud som är inställt på annonsgruppens standardbud. Search, Social, &amp; Commerce skapar automatiskt en [!UICONTROL Everything Else]-grupp med annonsgruppens standardbud på varje nivå i produktgruppshierarkin. Du kan fortfarande explicit skapa dessa standardgrupper och antingen exkludera dem eller ändra deras bud.</p></li><li><p>Varje annonsgrupp kan innehålla upp till åtta nivåer av produktgrupper, inklusive [!UICONTROL All Products] och sju andra nivåer.</p></li></ul> |
| [!UICONTROL Partition Type] | Partitionstypen för produktgruppen: <i>subdivision</i> (när den har underordnade produktgrupper) eller <i>unit</i> (när den inte har några underordnade produktgrupper). |
| [!UICONTROL Match Type] | <p>För dynamiska sökmål eller produktgrupper: Nyckelordsmatchningsalternativet för det dynamiska sökmålet eller produktgruppen: <i>[!UICONTROL Dynamic Ad Target]</i> (standard för nya dynamiska sökmål), <i>[!UICONTROL Product Group]</i> (standard för nya produktgrupper) eller <i>[!UICONTROL Negative Product Group]</i> (utelämna en produktgrupp).</p><p>För nyckelord: Nyckelordsmatchningsalternativet för nyckelordet: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> eller <i>[!UICONTROL Negative]</i> (för att exkludera ett nyckelord eller en placering i visningsnätverket). Produktgrupper som används med shoppingannonser har matchningstypen <i>[!UICONTROL Product Group]</i>. Om du använder <i>[!UICONTROL Negative]</i> måste du även inkludera matchningstypen som ska uteslutas (till exempel &quot;Negativ fras&quot;).</p><p>För nya nyckelord är standardvärdet <i>[!UICONTROL Broad]</i>. Ett värde för matchningstypen eller nyckelords-ID krävs bara för att redigera ett nyckelord med flera matchningstyper.</p><p><b>Obs!</b></p><ul><li><p>Matchningstyper gäller inte för expanderade dynamiska sökannonser, som inte använder nyckelord.</p></li><li><p>Om du ändrar matchningstypen för ett [!DNL Google Ads]-nyckelord tas det befintliga nyckelordet bort och ett nytt skapas.</p></li><li><p>För Bred Match Modifier väljer du &quot;Broad&quot; och infogar ett + före ett ord i nyckelordet för vilket det krävs närliggande varianter (t.ex. &quot;+red +skor&quot; för att kräva närliggande varianter av både &quot;red&quot; och &quot;skor&quot;). <b>Obs!</b> Många matchningsmodifierare har nu samma matchande beteende som frasmatchning för vissa språk, och du har inte kunnat skapa nya breda matchningsmodifierarnyckelord sedan juli 2021. Mer information finns i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/7042511).</p> |
| [!UICONTROL First Page Bid] | (Ingår i genererade kalkylblad i informationssyfte) Det bud som krävs för att placera en annons på första sidan i sökresultaten. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL Quality Score] | (Ingår i genererade kalkylblad i informationssyfte) Det aktuella kvalitetsmoment som sökmotorn har tilldelat nyckelordet. Det här värdet är inte registrerat i annonsnätverket.) |
| [!UICONTROL Creative Preferred Devices] | (Textannonser, utökade dynamiska sökannonser och utökade sitelinks; valfritt) De enhetstyper som du föredrar att visa annonsen på: <i>[!UICONTROL All]</i> (standard) eller <i>[!UICONTROL Mobile]</i>. När <i>[!UICONTROL Mobile]</i> har angetts försöker nätverket visa annonsen för användare av mobila enheter i stället för för för användare på datorer eller surfplattor. I annat fall visas annonsen på alla enhetstyper i nätverket.</p><p><b>Obs!</b></p><ul><li><p>Endast användare med administratörsbehörighet och kontohanterare för [!DNL Adobe] kan redigera den här inställningen.</p></li><li><p>Nätverket garanterar inte att annonsen visas på den önskade enhetstypen.</p></li><li><p>Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Endast expanderade textannonser och responsiva sökannonser) Rubrikerna i en annons, avgränsade med ett vertikalt rör (&amp;vert;). Den maximala längden för varje annonstitelfält är 30 eller 15 dubbelbytetecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).</p><p>För responsiva sökannonser krävs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] och [!UICONTROL Ad Title 3], och alla andra annonsrubrikfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p><p>För responsiva sökannonser infogar du en annonsanpassare i följande format: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, till exempel <code>{CUSTOMIZER.Discount:10%}</code></p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser som [!DNL Google Ads] togs bort i juni 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Endast responsiva sökannonser; valfritt) En position där motsvarande annonsrubrik ska fästas: `[null]` (inget värde, vilket gör att annonsrubriken kan användas för alla positioner), <i></i>, <i>  eller </i> <i>3</i>. Om [!UICONTROL Ad Title Position] till exempel har värdet 1 visas bara annonsrubrik i position 1. Som standard är alla annonsrubriker null (saknar värden).</p><p>Om du vill ta bort det befintliga värdet använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p><p><b>Obs!</b> Du kan fästa flera annonsrubriker på samma plats. Annonsnätverket använder en av de annonstitlar som är fästa vid positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Utökade dynamiska sökannonser, utökade textannonser och responsiva sökannonser) Innehållet i en annons. Den maximala längden för varje beskrivningsfält är 90 eller 45 dubbelbytetecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).</p><p>För responsiva sökannonser infogar du en annonsanpassare med följande format: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, till exempel `{CUSTOMIZER.Discount:10%}`</p><p>Använd endast [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] för expanderade dynamiska sökannonser. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser som [!DNL Google Ads] togs bort i juni 2022.</p><p>För responsiva sökannonser krävs [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2], och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. Om du vill ta bort det befintliga värdet använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Endast responsiva sökannonser; valfritt) En position där motsvarande beskrivning ska fästas: `[null]` (inget värde, vilket gör beskrivningen giltig för alla positioner), <i></i>, <i> </i> eller <i>3</i>. Om [!UICONTROL Description 1 Position] till exempel har värdet 1 visas [!UICONTROL Description 1] bara i position 1. Som standard är inga beskrivningar fästa vid en position.</p><p>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna).</p><p><b>Obs!</b> Du kan fästa flera beskrivningar på samma plats. Annonsnätverket använder en av beskrivningarna som är fästa vid positionen. Beskrivningar som fästs vid position 2 kanske inte visas tillsammans med annonsen. |
| [!UICONTROL Display URL] | Den URL som ingår i annonsen.<br><br>För expanderade dynamiska sökannonser genererar [!DNL Google Ads] det här värdet dynamiskt från webbplatsdomänen och du behöver inte ange något värde.<br><br>För responsiva sökannonser behöver du inte ange något värde. Visnings-URL:en extraheras automatiskt från domänen i den slutliga URL:en. Du kan också anpassa URL-adressen med fälten Sökväg 1 och Sökväg 2.<br><br>Du kan inte skapa eller redigera, men du kan ta bort expanderade textannonser som [!DNL Google Ads] togs bort i juni 2022.<br><br><b>Obs!</b> (Konton med slutliga URL:er) Domännamnen i visnings-URL:en och den slutliga URL:en måste matcha.</p> |
| [!UICONTROL Display Path 1] | <p>(Endast expanderade textannonser <span> och responsiva sökannonser</span>)</p><p>(Valfritt) Text som läggs till i URL:en som automatiskt extraheras från den slutliga URL:en. Det föregås av ett snedstreck (/) i URL:en. En bana får inte innehålla snedstreck (/) eller radmatningstecken (\n). Maxlängden är 15 tecken eller 7 dubbelbyte-tecken.</p><p>Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`</p><p>Om [!UICONTROL Display Path 1] till exempel är &quot;erbjudanden&quot; är URL:en för visning &lt;<i>visa URL</i>>/erbjudanden, till exempel www.example.com/deals.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser som [!DNL Google Ads] togs bort i juni 2022.</p> |
| [!UICONTROL Display Path 2] | En andra visningssökväg. Se posten för [!UICONTROL Display Path 1].<br><br>Exempel: Om [!UICONTROL Display Path 1] är&quot;erbjudanden&quot; och [!UICONTROL Display Path 2] är&quot;lokal&quot; är visnings-URL:en &lt;<i>visa-URL</i>>/erbjudanden/lokal, till exempel www.example.com/deals/local.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser som [!DNL Google Ads] togs bort i juni 2022.</p> |
| [!UICONTROL Promotion Line] | (Endast produktlistannonser) En valfri kampanjrad som ska inkluderas i produktlistan i sökresultaten. Maximala längden är 45 tecken.</p><p>Kampanjraden kan visas på olika platser i förhållande till annonsen (t.ex. nedanför annonsen) beroende på var annonsen visas på sidan. |
| [!UICONTROL Link Name] | <p>Sitelink-texten. Den kan innehålla upp till 25 tecken.</p><p>För nya sitelinks måste du inkludera kampanjnamnet i sitelink-raden. För annonser på gruppnivå måste du även inkludera annonsgruppens namn.</p><p><b>Obs!</b> Befintlig text med 35 tecken visas fortfarande i annonser på datorer och surfplattor, men inte på mobila enheter.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Endast befintliga appinstallationer) Det operativsystem som mobilprogrammet körs på: <i>Android™</i> eller <i>iOS</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Endast befintliga appinstalleringsannonser) <p>Program-ID eller paketnamn. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Endast befintliga programinstallationer) Programmets namn. |
| [!UICONTROL Start Date] | <p>(Endast utökade sitelinks) Det första datum då anbud kan lämnas för sitelink, i annonsörens tidszon och i något av följande format: <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyy</i> eller <i>m-d-yy</i>. Standardinställningen för nya utökade sitelinks är den aktuella dagen.</p><p><b>Obs!</b> Nya förbättrade sitelinks kan bara skapas i kampanjer med befintliga utökade sitelinks eller utan sitelinks.</p> |
| [!UICONTROL End Date] | <p>(Endast utökade sitelinks) Det sista datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format:  <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i> eller <i>m-d-yy</i>. Standardvärdet är inget (inget slutdatum).</p><p><b>Obs!</b> Nya förbättrade sitelinks kan bara skapas i kampanjer med befintliga utökade sitelinks eller utan sitelinks.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Endast befintliga appinstalleringsannonser)</p><p>(Valfritt) Förhindrar att [!DNL Google Ads] visar annonsen för surfplatteanvändare. Värdena kan vara <i>yes</i> och <i>no</i>. |
| [!UICONTROL Landing Page Suffix] | Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Exempel: `param2=value1&param3=value2`<br><br>Se &quot;[Klicka-spårningsformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)&quot;.<br><br>Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Google Ads]-redigeraren. |
| [!UICONTROL Tracking Template] | Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårar parametrar och bäddar in den slutliga URL:en i en [!DNL ValueTrack]-parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet längst till granulerad) åsidosätter värdena på alla högre nivåer.<br><br>För Adobe Advertising-konverteringsspårning, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs automatiskt en egen omdirigerings- och spårningskod till när du sparar posten.<br><br>Ange ett värde för omdirigeringar och spårning från tredje part. En lista med [!DNL ValueTrack] parametrar som anger de slutliga URL:erna i spårningsmallar finns i parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängliga [!DNL ValueTrack]-parametrar&quot; i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/2375447).<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Base URL/Final URL] | Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas-/slutadresser på nyckelordsnivå åsidosätter de på annonsnivå och högre.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Destination URL] | (Ingår i genererade kalkylblad i informationssyfte, inte i sökmotorn) För konton med mål-URL:er är detta den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och Commerce. Om du genererade spårnings-URL:er baseras detta på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till parametrar som är specifika för sökmotorn kan de ersättas med motsvarande parametrar för Search, Social och Commerce.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som kolumnen Bas-URL/Slutlig URL. |
| [!UICONTROL Custom URL Param] | Data som ska ersätta den dynamiska variabeln `{custom_code}` när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL:en måste du överföra kalkylbladsfilen med alternativet Generera spårnings-URL:er. |
| [!UICONTROL Creative Type] | Annonsformatet: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (Carousel-annonser för flera bilder), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> och <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (inaktuell annonstyp), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (utgått), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (kundannonser) eller <i>[!UICONTROL Responsive search ad]</i>. Standardvärdet för nya annonser är <i>[!UICONTROL Text ad]</i>.<br><br>Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Param1] | <p>Det numeriska värdet för annonsparametern `{param1}`, som kan inkluderas i annonskopian eller visa URL:en för en annons i kalkylbladsfilen. Maxlängden är 25 tecken och du kan inkludera följande icke-numeriska tecken:</p><ul><li><p>Värdet kan föregås eller läggas till med en valutasymbol eller valutakod. `£2.000,00` och `2000GBP` är till exempel giltiga.</p></li><li><p>Värdet kan innehålla kommatecken (`,`) eller punkt (`.`) som avgränsare, med en valfri punkt (`.`) eller komma (`,`) för decimalvärden. `1,000.00` och `2.000,10` är till exempel giltiga.</p></li><li><p>Värdet kan prefixeras eller läggas till med ett procenttecken (`%`), plustecken (`+`) eller minustecken (`- `). Till exempel är `20%`, `208+` och `-42.32` giltiga.</p></li><li><p>Två tal kan bäddas in med ett snedstreck. `4/1` och `0.95/0.45` är till exempel giltiga.</p></li></ul><p>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna).</p> |
| [!UICONTROL Param2] | Det numeriska värdet för annonsparametern `{param2}`, som kan inkluderas i annonskopian eller visa URL:en för en annons i kalkylbladsfilen. Mer information finns under Param1. |
| [!UICONTROL Audience] | Återmarknadsföringslistan för sökannonser (RLSA) som riktar sig till målgrupp eller exkluderad publik för kampanjen eller annonsgruppen. Ange om det är ett mål eller undantag i fältet Måltyp. |
| [!UICONTROL Target Type] | (När en publik har angetts) Anger om den angivna målgruppen är en <i>inkludering</i> (mål) eller <i>Uteslutning</i>. |
| [!UICONTROL Campaign Status] | Visningsstatusen för kampanjen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (inte redigerbar) eller <i>[!UICONTROL Deleted]</i> (endast befintliga kampanjer). Standardvärdet för nya kampanjer är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | Annonsgruppens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonsgrupper). Standardvärdet för nya annonsgrupper är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet `Deleted`. |
| [!UICONTROL Keyword Status] | Visningsstatus för nyckelordet: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är [!UICONTROL Active]. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | Annonsens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (endast befintliga annonser), <i>[!UICONTROL Disapproved]</i> (inte redigerbara) eller <i>[!UICONTROL Paused]</i>. Standardvärdet för nya annonser är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annons anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | Status för webbplatsplaceringen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonser). Standardvärdet för nya webbplatser är <i>Aktiv.</i> Om du vill ta bort en aktiv eller pausad placering anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | Status för ett dynamiskt sökmål: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga mål). Standardvärdet för nya mål är <i>Aktiv.</i> Om du vill ta bort ett aktivt eller pausat mål anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | Produktgruppens visningsstatus: <i>[!UICONTROL Active]</i> <span>eller</span> <i>[!UICONTROL Deleted]</i> (endast befintliga produktgrupper). Standardvärdet för nya produktgrupper är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv produktgrupp anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | Visningsstatus för sitelink: <i>Aktiv eller Borttagen</i> (endast befintliga sitelinks). Standardvärdet för nya sitelinks är <i>[!UICONTROL Active]</i>. Ange värdet <i>[!UICONTROL Deleted]</i> om du vill ta bort en aktiv sitellänk. |
| [!UICONTROL Location Status] | Status för platsmålet: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga platser). Standardvärdet för nya platser är [!UICONTROL Active]. Om du vill ta bort en aktiv plats anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | Status för RLSA-mål eller -undantag på kampanjnivå eller annonsgruppsnivå: <i>[!UICONTROL Active]</i> eller [!UICONTROL Deleted]</i> (endast befintliga mål). Standardvärdet för nya mål eller undantag är <i>[!UICONTROL Active]</i>. Om du vill ta bort ett aktivt mål eller undantag anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>Status för enhetsmålet på kampanj- eller annonsnivå: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i>. För nya kampanjer och annonsgrupper är standardvärdet <i>[!UICONTROL Active]</i>.</p> |
| \[Advertiser-specific Label Classification\] | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden används för alla underordnade komponenter. Nya komponenter som läggs till senare associeras automatiskt med etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Varken klassificeringsnamnet eller klassificeringsvärdet är skiftlägeskänsliga. |
| [!UICONTROL Constraints] | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><b>>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL Campaign ID] | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för kampanjen. |
| [!UICONTROL Ad Group ID] | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för annonsgruppen. |
| [!UICONTROL Keyword ID] | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordet, såvida inte raden innehåller a) tillräckligt många egenskapskolumner för att identifiera nyckelordet eller b) ett [!UICONTROL AMO ID].&quot; |
| [!UICONTROL Ad ID] | <p>Det unika ID som identifierar en befintlig annons. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] För responsiva sökannonser krävs antingen annons-ID eller AMO-ID för att redigera eller ta bort annonsdata. För alla andra entitetstyper krävs bara annons-ID när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annons eller b) en [!UICONTROL AMO ID].&quot; Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna.</p><p><b>Obs!</b> Om du redigerar a) och egenskapskolumner förutom Status för en befintlig annons eller b) data för en responsiv sökannons, och du inkluderar varken [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], skapas en ny annons och den befintliga annonsen ändras inte.</p> |
| [!UICONTROL Placement ID] | Det unika ID som identifierar en webbplatsplacering. Krävs endast när du ändrar eller tar bort placeringen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera placeringen eller b) en [!UICONTROL AMO ID].&quot; |
| [!UICONTROL Target ID] | Det unika ID som identifierar ett befintligt automatiskt mål. Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL Product Group ID] | Det unika ID som identifierar en befintlig produktgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en [!UICONTROL AMO ID].&quot; |
| [!UICONTROL Sitelink ID] | Det unika ID som identifierar en befintlig platslänk. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort platslänken, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera platslänken eller b) en [!UICONTROL AMO ID].&quot; Om du däremot inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID] och egenskapskolumnerna matchar flera sitelinks ändras bara statusen för en av sitelinks.</p><p><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom status för en befintlig sitelink, och du varken inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL RLSA Target ID] | Det unika ID som identifierar ett befintligt RLSA-mål eller -undantag på kampanj- eller annonsgruppsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet eller undantaget, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL Device Target ID] | <p>Det unika ID som identifierar ett befintligt enhetsmål eller undantag på kampanjnivå eller annonsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet.</p> |
| [!UICONTROL AMO ID] | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar annons-ID:t. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| [!UICONTROL EF Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL EF Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL SE Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL SE Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL Exemption Request] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa namn och text för alla [!DNL Google Ads] annonspolicyer som en annons bryter mot. |
| [!UICONTROL Retail Hash] | (Ingår i informationssyfte i kalkylblad som genereras med avancerad kampanjhantering) En alfanumerisk hash-kod (till exempel f9639f40cdf56524b541e5dacf55a991) som anger att artikeln genererades i vyn Avancerat (ACM). |

[^1]: [!DNL Excel] konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

## Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent {#bulksheet-fields-per-component-google}

Följande avsnitt innehåller fält som är relevanta för specifika kontoenheter.

>[!NOTE]
>
>När ett fält inte kan användas för en åtgärd, ignoreras alla värden som anges i fältet.

### Kampanjfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Campaign Budget] | Krävs för att skapa en kampanj. |
| [!UICONTROL Delivery Method] | Krävs för att skapa en kampanj. |
| [!UICONTROL Channel Type] | Krävs för att skapa en kampanj. |
| [!UICONTROL Networks] | Krävs för att skapa en kampanj. |
| [!UICONTROL DSA Domain Name] | Krävs för att skapa en kampanj med dynamiska sökannonser i söknätverket. |
| [!UICONTROL DSA Domain Language] | Krävs för att skapa en kampanj med dynamiska sökannonser i söknätverket. |
| [!UICONTROL Campaign Priority] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Has EU Political Ads] | Krävs för att skapa en kampanj. |
| [!UICONTROL Merchant ID] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Sales Country] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Product Scope Filter] | (Kampanjer) Valfritt |
| [!UICONTROL Languages] | Valfritt |
| [!UICONTROL Device Targets] | Valfritt |
| [!UICONTROL Device Targets (Google Adwords)] | Valfritt |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Valfritt |
| [!UICONTROL Audience Target Method] | n/a |
| [!UICONTROL Landing Page Suffix] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Campaign Status] | Krävs endast för att ta bort en kampanj. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för kampanjen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Annonsgruppsfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Networks] | n/a |
| [!UICONTROL GDN Custom Bid Level] | Valfritt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Group Type] | Krävs för att skapa en annonsgrupp. |
| [!UICONTROL Max CPC] | Valfritt |
| [!UICONTROL Max Content CPC] | Valfritt |
| [!UICONTROL Audience Target Method] | Obligatoriskt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Ad Group Status] | Krävs endast för att ta bort en annonsgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Ad Group ID] | Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller [!UICONTROL AMO ID] för annonsgruppen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Nyckelordsfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Max CPC] | Valfritt |
| [!UICONTROL Keyword] | Obligatoriskt |
| [!UICONTROL Match Type] | Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper. |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Param1] | Valfritt |
| [!UICONTROL Param2] | Valfritt |
| [!UICONTROL Keyword Status] | Krävs endast för att ta bort ett nyckelord. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Keyword ID] | Krävs endast när du redigerar eller tar bort nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Placeringsfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Valfritt |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Valfritt |
| [!UICONTROL Placement] | Obligatoriskt |
| [!UICONTROL Match Type] | Obligatoriskt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Placement Status] | Krävs endast för att ta bort en placering. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Placement ID] | Krävs endast när du redigerar eller tar bort placeringen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera placeringen eller b) en [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Utökad dynamisk sökannons

Den här annonstypen kallas nu för&quot;dynamisk sökannons&quot; i [!DNL Google Ads]. Mer information om hur du skapar dynamiska sökannonser finns i [Implementera [!DNL Google Ads] dynamiska sökannonser](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html).

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Creative Preferred Devices] | Valfritt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Krävs för att skapa en annons eller redigera beskrivningen. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas. |
| [!UICONTROL Display URL] | Obligatoriskt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Creative Type] | Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsadressen eller b) en [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Produktlista/reklamfält

Mer information om hur du skapar shoppingannonser finns i [Implementera [!DNL Google Ads] shoppingkampanjer](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html).

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Promotion Line] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Creative Type] | Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsadressen eller b) en [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Reklamfält för responsiv sökning

Använd raden [!UICONTROL Responsive Search Ad] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | För responsiva sökannonser krävs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] och [!UICONTROL Ad Title 3] för att skapa en annons, och alla andra annonstitelfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Valfritt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | För responsiva sökannonser krävs [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] för att skapa en annons, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Valfritt |
| [!UICONTROL Display Path 1] | Valfritt |
| [!UICONTROL Display Path 2] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Krävs för att skapa en annons. |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Creative Type] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs för att redigera eller ta bort annonser såvida inte raden innehåller en [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort annonser såvida du inte inkluderar annons-ID:t. |

### Text och fält

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

>[!NOTE]
>
>Utökade textannonser togs bort i juni 2022. Du kan bara ta bort befintliga textannonser.

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Creative Preferred Devices] | Skrivskyddad |
| [!UICONTROL Ad Title], annonsrubrik 2-3 | Skrivskyddad |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Skrivskyddad |
| [!UICONTROL Display URL] | Skrivskyddad |
| [!UICONTROL Display Path 1] | Skrivskyddad |
| [!UICONTROL Display Path 2] | Skrivskyddad |
| [!UICONTROL Tracking Template] | Skrivskyddad |
| [!UICONTROL Base URL/Final URL] | Skrivskyddad |
| [!UICONTROL Custom URL Param] | Skrivskyddad |
| [!UICONTROL Creative Type] | Valfritt |
| [!UICONTROL Ad Status] | Obligatoriskt |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a&amp;rpar; tillräckligt många annonsegenskapskolumner för att identifiera annons- eller b&amp;rpar; och [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökmålfält (automatiskt mål)

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Max CPC] | Valfritt |
| [!UICONTROL Auto Target Expression] | Krävs endast när kampanjinställningen [!UICONTROL Use my website contents to target my ads] inte är aktiverad. |
| [!UICONTROL Match Type] | Valfritt |
| [!UICONTROL Target Status] | Krävs för att ta bort ett mål |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Target ID] | Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Fält för produktgrupp som köpts

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Max CPC] | Krävs för att skapa en produktgrupp. |
| [!UICONTROL Parent Product Groupings] | Obligatoriskt |
| [!UICONTROL Product Grouping] | Obligatoriskt |
| [!UICONTROL Partition Type] | Krävs för att skapa en produktgrupp. |
| [!UICONTROL Match Type] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Obligatoriskt |
| [!UICONTROL Product Group Status] | Krävs endast för att ta bort en produktgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Product Group ID] | Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Sitelink-fält på kampanjnivå och annonsnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Krävs för sitelinks på annonsnivå. Gäller inte för sitelinks på kampanjnivå. |
| [!UICONTROL Creative Preferred Devices] | Valfritt |
| [!UICONTROL Link Name] | Obligatoriskt |
| [!UICONTROL Start Date] | Valfritt |
| [!UICONTROL End Date] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Obligatoriskt |
| [!UICONTROL Sitelink Status] | Krävs endast för att ta bort en sitellänk. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Sitelink ID] | Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitelink eller b) en [!UICONTROL AMO ID]. Om du däremot inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID] och egenskapskolumnerna matchar flera sitelinks ändras bara statusen för en av sitelinks.<br><br><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom [!UICONTROL Status] för en befintlig sitelink och du inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID] skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Platsmål

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Location] | Obligatoriskt |
| [!UICONTROL Location Type] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Location Status] | Krävs endast för att ta bort ett platsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar [!UICONTROL Campaign ID].<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält på kampanjnivå och annonsgruppsnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Device] | Krävs för att skapa eller redigera ett enhetsmål. |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Ad Group Name] | Krävs för enhetsmål på annonsnivå. Gäller inte för enhetsmål på kampanjnivå. |
| [!UICONTROL Device Target Status] | Krävs endast för att ta bort ett enhetsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt; endast tillämpligt för enhetsmål på annonsgruppsnivå. |
| [!UICONTROL Device Target ID] | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhetens mål-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Mål-/exkluderingsfält för RLSA på kampanjnivå och annonsnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-google).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Ad Group Name] | Krävs för annonsnivåmål och undantag. Gäller inte för kampanjnivåmål och undantag. |
| [!UICONTROL Audience] | Krävs för att skapa ett nytt mål eller undantag. |
| [!UICONTROL Target Type] | Krävs för att skapa ett nytt mål eller undantag. |
| [!UICONTROL RLSA Target Status] | Krävs endast för att ta bort ett mål eller ett undantag. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt; endast tillämpligt för mål och undantag på annonsnivå. |
| [!UICONTROL RLSA Target ID] | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar mål-ID:t för RLSA.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

>[!MORELIKETHIS]
>
>* [Bilaga - fel i bulkark](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Mallfilformat som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överför en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
