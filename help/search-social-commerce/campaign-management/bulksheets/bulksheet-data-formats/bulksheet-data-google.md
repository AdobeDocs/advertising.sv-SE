---
title: Obligatoriska kalkylbladsdata för [!DNL Google Ads] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för [!DNL Google Ads] konton.
source-git-commit: 6c1e9bffd072979975a933fceb1c6e1253399373
workflow-type: tm+mt
source-wordcount: '8631'
ht-degree: 1%

---

# Bilaga - Obligatoriska data för kalkylblad för [!DNL Google Ads] konton

Skapa och uppdatera [!DNL Google Ads] kampanjdata i grupp kan du använda bulkbladsfiler för sökning, sociala medier och handel som är särskilt formaterade för [!DNL Google Ads] konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det önskade filformatet eller b) skapa dem manuellt (se &quot;[Filformat för bulkblad som stöds](bulksheet-file-formats.md)&quot; för allmän information om vilka filformat som stöds).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alla tillgängliga datafält

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Fält | Beskrivning |
| ---- | ---- |
| Plattform | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kontonamn | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Det unika namn som identifierar en kampanj för ett konto. |
| Kampanjbudget | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| Leveranssätt | <p>Så här visar du annonser för kampanjen varje dag:</p><ul><li><p><i>Standard (distribuerad)</i> (standard för nya kampanjer): För att sprida annonsintrycket över hela dagen.</p></li><li><p><i>Accelererad:</i> (Borttaget i oktober 2019) Visa dina annonser så ofta som möjligt tills din budget är nådd. Därför kanske era annonser inte visas senare under dagen.</p></li></ul> |
| Kanaltyp | <p>De kanaler där annonser ska placeras. Ange ett eller flera alternativ:</p><ul><li class="p"><p><span style="font-style: italic;"><i>Sök</i></span> (standard för nya kampanjer): Om du vill placera annonser i Google söknätverk (inklusive Google sökningar och Google sökpartnerwebbplatser) och eventuellt även i Google visningsnätverk. <b>Obs!</b> Kampanjer som riktar sig till både söknätverket och visningsnätverket kan inte läggas till i en portfölj för anbudsoptimering.</p></li><li class="p"><p><span style="font-style: italic;"><i>Visa</i></span>: Om du bara vill placera annonser i Google bildskärmsnätverk.</p></li><li class="p"><p><span style="font-style: italic;"><i>Shopping</i></span>: Så här lägger du ut shoppingannonser på Google Shopping (i vissa länder) och i Google söknätverk (inklusive Google Search och Google Search Partner-webbplatser). Om du vill skapa shoppingannonser måste du ha produkter på ett Google Merchant Center-konto och [tillåt att Search, Social och Commerce hämtar data från kontot](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Se &quot;[Implementera [!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; om du vill ha mer information om processen att skapa shoppingannonser.</p></li></ul> |
| Nätverk | <p>Var annonserna ska placeras. Ange ett eller flera alternativ:</p><ul><li class="p"><p><span style="font-style: italic;"><i>Google Search</i></span>: Sponsrade söklistor endast på Google Search Network.</p></li><li class="p"><p><span style="font-style: italic;"><i>Sökpartners</i></span>: Sponsrade söklistor om Google sökpartners.</p></li><li class="p"><p><span style="font-style: italic;"><i>Innehåll</i></span>: Så här lägger du bud på listor över visningsnätverk.</p></li><li class="p"><p><span style="font-style: italic;"><i>Alla</i></span> (standard för nya kampanjer): Målgrupper för Google Search, Search Partners och Content.</p></li></ul> |
| DSA-domännamn | <p>(Endast söknätverk; gäller endast för expanderade dynamiska sökannonser) Rotdomänen (till exempel example.com) eller underdomänen (till exempel skor.example.com) för den webbplats vars innehåll annonsnätverket använder för att rikta dina dynamiska sökannonser.<br><br><b>Anteckningar:</b></p><ul><li><p>Utökade dynamiska sökannonser målar webbinnehåll i stället för nyckelord.</p></li><li><p>Din domän måste indexeras av annonsnätverkets organiska sökindex för att kunna anges som mål.</p></li><li><p>Om du inte anger någon domän måste du skapa dynamiska sökmål som är avsedda för alla dina webbplatssidor eller en delmängd av dem för varje annonsgrupp.</p></li></ul> |
| Domänspråk för DSA | (Endast söknätverk; gäller endast för expanderade dynamiska sökannonser) Språket för den angivna webbplatsdomänen. <b>Obs!</b> Om domänen innehåller sidor på flera språk och du vill ha alla som mål, skapar du en separat kampanj för varje språk. |
| Anpassad GDN-anbudsnivå | (Kampanjer som endast riktar sig till visningsnätverket) Så här lägger du ett bud: av <span style="font-style: italic;"><i>Annonsgrupp</i></span> (standard), <span style="font-style: italic;"><i>Nyckelord</i></span>, <span style="font-style: italic;"><i>Placement</i></span> (webbplats), eller <span style="font-style: italic;"><i>Ingen</i></span> (för att återställa det befintliga värdet). Andra dimensioner (<span style="font-style: italic;"><i>Ålder</i></span>, <span style="font-style: italic;"><i>Kön</i></span>, <span style="font-style: italic;"><i>Intresse och lista</i></span>, <span style="font-style: italic;"><i>Ämne</i></span>och <span style="font-style: italic;"><i>Lodrätt</i></span>) finns i Google Ads-gränssnittet. Om du har använt Google Ads-gränssnittet för att konfigurera budgivning med en annan dimension visas det värdet, men du kan inte välja eller ange dessa dimensioner här.</p><p><b>Obs!</b></p><ul><li><p>När du lägger ett bud med nyckelord skapar du spårningsmallar på nyckelordsnivå. På samma sätt kan du skapa spårningsmallar på placeringsnivå när du lägger ett bud per placering. För alla andra dimensioner skapar du spårningsmallar på annonsnivå.</p></li><li><p>När du lägger ett bud i en dimension som inte stöds (ålder, kön, ränta och lista eller ämne) optimeras inte erbjudandena för dimensionen i Sök, Socialt och Commerce, och all attribuering tillämpas på annonsgruppen.</p></li><li><p>I annonser i söknätverket används alltid nyckelordsbud.</p></li></ul> |
| Kampanjprioritet | <p>(Endast köpkampanjer) Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt:  <span style="font-style: italic;"><i>Låg</i></span> (standard för nya kampanjer), <span style="font-style: italic;"><i>Medel</i></span>, eller <span style="font-style: italic;"><i>Hög</i></span>.</p><p>När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad. |
| Affärs-ID | (Kundkampanjer och målgruppskampanjer som endast är kopplade till en handlarfeed) Kund-ID för det handlarkonto vars produkter används för kampanjen. |  |
| Försäljningsland | (Endast köpkampanjer. skrivskyddad för befintliga kampanjer) Det land där kampanjprodukterna säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen. |
| Filter för produktomfång | (Kampanjer endast med Google shoppingnätverk) De produkter i ditt Google Merchant Center-konto för vilka det går att skapa shoppingannonser för kampanjen. Du kan ange upp till sju produktdimensioner och attributkombinationer där du kan filtrera dina produkter med formatet dimension=attribut. Avgränsa flera filter med avgränsaren &quot;>>&quot;. En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanjer](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Exempel: &quot;Kategori L1=djur>>Kategori L2=djurmaterial>>Varumärke=Ätbara husdjur&quot;</p><p>Om du vill ta bort de befintliga värdena använder du värdet <span class="Code">[delete]</span> (inklusive hakparenteser).</p> |
| Språk | <p>(Endast sök- och visningsnätverk) Målspråken för annonser i kampanjen.</p><p>Om du inte anger något värde för antingen det här fältet eller fältet Geo Targeting för en ny kampanj avgör den valuta som anges för kontot standardspråken, förutom att kampanjer med valutor som inte är mappade till specifika språk (till exempel EUR) är riktade till alla språk. Om du inte anger ett värde för det här fältet utan anger ett värde i fältet Geo-målning för en ny kampanj, blir standardvärdet <span style="font-style: italic;"><i>Alla</i></span>. Om du lämnar det här fältet tomt för en befintlig kampanj behålls det befintliga värdet.</p><p>Om du vill ange alla språk som mål anger du <span style="font-style: italic;"><i>Alla</i></span>. Om du vill ange särskilda språk som mål anger du värden avgränsade med semikolon med antingen <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">Google språknamn</a> (till exempel <span style="font-style: italic;"><i>Engelska;japanska</i></span>, som ersätts med rätt numeriska koder) eller numeriska koder (t.ex. <span style="font-style: italic;"><i>1000;1005</i></span>). Värdena är inte skiftlägeskänsliga.</p> |
| Plats | En geografisk plats där annonser, eller för vilken annonser, ska uteslutas, ska placeras för kampanjen. Om du inte anger några värden för det här fältet eller fältet Språk för en ny kampanj, avgör den valuta som anges för kontot standardplatserna, förutom att kampanjer med valutor som inte är mappade till specifika platser (till exempel EUR) är riktade till alla platser. Om du inte anger något värde för det här fältet utan anger ett värde i [!UICONTROL Languages] fält för en ny kampanj, då är standardvärdet <i>Alla</i>. Om du lämnar det här fältet tomt för en befintlig kampanj behålls det befintliga värdet.</p><p>Använd någon av [Google platsnamn](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (som ersätts med rätt numerisk kod) eller platskoder:</p><ul><li><p>Länder/territorier: Ange namn på land/territorium (t.ex. <span style="font-style: italic;"><i>USA;Japan</i></span>) eller de numeriska koderna (t.ex. <span style="font-style: italic;"><i>2840;2392</i></span>).</p></li><li><p>Stater/provinser/regioner: Ange delstatens/regionens/regionens namn med motsvarande förkortningar av land/territorium (t.ex. <span style="font-style: italic;"><i>Tokyo, JP;New York, US</i></span>) eller de numeriska koderna (sådana <span style="font-style: italic;"><i>20636;21167</i></span>).</p></li><li><p>Städer utanför USA: Ange stadsnamn, namn på stat/provins/region och förkortningar av land/territorium (t.ex. <span style="font-style: italic;"><i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i></span>) eller de numeriska koderna (t.ex. <span style="font-style: italic;"><i>1028850;1009293</i></span>)</p></li><li><p>Amerikanska tunnelbaneområden: Ange namn på ort, delstat och land (t.ex. <span style="font-style: italic;"><i>Buffalo NY, USA;New York NY, USA</i></span>) eller de numeriska koderna (t.ex. <span style="font-style: italic;"><i>514;501</i></span>).</p></li></ul><p>Om du vill utesluta en plats skriver du ett minustecken (-) före platsnamnet eller koden, till exempel <span style="font-style: italic;"><i>-Japan</i></span>.</p><p><b>Obs!</b> Värdena är inte skiftlägeskänsliga.</p> |
| Platstyp | (När du inkluderar en plats) [platstyp](https://developers.google.com/google-ads/api/data/geotargets). |
| Enhet | En enhetstyp för vilken anbudsjusteringar görs på kampanj- eller annonsgruppsnivå: <i>smartphone</i>, <i>surfplatta</i>, eller <i>desktop</i>. |
| Anpassa via bud | <p>(När du inkluderar ett mål för Location, Device eller RLSA) Om du vill justera anbuden för annonser på en viss plats, på en viss enhetstyp eller med ett visst målgruppsmål:</p><ul><li><p>Ange 0 om du vill använda nyckelordsbudskapet (differens på 0 %). För nya mål kan du också lämna detta tomt.</p></li><li><p>Om du vill använda ett annat bud för detta mål anger du den procentandel med vilken anbuden ska ökas eller minskas.</p></li><ul><li><p>För plats- och RLSA-mål är giltiga procenttal mellan -90 och 900.</p></li><li><p>Giltiga procentsatser för enhetsanbudsjusteringar är:</p></li><ul><li><p>(Campaigns)-100 (to not bid for ads on the device type) eller från -90 till 900.</p></li><li><p>(Annonsgrupper) -100 för smarttelefoner och surfplattor (men inte för enhetstypen) och från -90 till 900 för alla enhetstyper.</p></li></ul></ul><li><p>(Befintliga kampanjer och annonsgrupper) Om du vill använda den befintliga budjusteringen lämnar du detta tomt.</p></li></ul> |
| Adobe Rec Bid-justering | (Ingår i genererade kalkylblad i informationssyfte) Den skrivskyddade budjustering som Adobe rekommenderar för kampanjnivåmål eller en RLSA. Den beräknas endast när kampanjen är i en portfölj med ett viktat intäktsmål (inte målet Maximera klickningar) och kampanjen innehåller minst två lokaliseringsmål eller RLSA-avtal med minst fem klick eller 5 USD i kostnad under de senaste 90 dagarna.</p><p>Om du vill redigera ett platsmål manuellt eller RLSA manuellt för att använda det rekommenderade värdet väntar du minst två veckor efter att du har skapat platsmålet eller RLSA för att tillåta tillräcklig datainsamling och ändrar inte värdet mer än en gång i veckan. |
| Enhetsmål | <p>(Gäller endast äldre kampanjtyper) De enheter där annonsen kan visas: <span style="font-style: italic;"><i>Alla</i></span>, <span style="font-style: italic;"><i>Datorer</i></span>, <span style="font-style: italic;"><i>Smartphones</i></span>, eller <span style="font-style: italic;"><i>Tabletter</i></span>. För nya kampanjer är standardvärdet <span style="font-style: italic;"><i>Alla</i></span>.</p> |
| Operativsystemmål för enhet (Google Adwords) | (Endast äldre kampanjtyper) Gäller när enhetsmålen omfattar&quot;Smartphones&quot; eller&quot;Tablets&quot;) De operativsystem där annonsen kan visas: <span style="font-style: italic;"><i>Alla</i></span>, <span style="font-style: italic;"><i>Android</i></span>, <span style="font-style: italic;"><i>iOS</i></span>, eller <span style="font-style: italic;"><i>Palm</i></span>. För nya kampanjer är standardvärdet <span style="font-style: italic;"><i>Alla</i></span>.</p> |
| Mobiloperatörer (Google Adwords) | <p>(Endast äldre kampanjtyper) Gäller när enhetsmålen är&quot;Alla&quot; eller&quot;Smartphones&quot;) Mobilbärare som smarttelefonerna kan vara anslutna till: <span style="font-style: italic;"><i>Alla</i></span>eller en eller flera transportföretag som anges av &lt;c span=&quot;&quot; id=&quot;2&quot; translate=&quot;no&quot; />transportföretagskod</i></span>>,&lt;<span style="font-style: italic;"><i>landskod</i></span>> (t.ex. T-Mobile, USA) med hjälp av listan över <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">tillgängliga operatörer och koder för Google Ads</a>. <span style="font-style: italic;"><i> Avgränsa flera bärare med semikolon (t.ex. T-Mobile, US;T-Mobile, GB). För nya kampanjer är standardvärdet <span style="font-style: italic;"><i>Alla</i></span>.</p> |
| Namn på annonsgrupp | <p>Det unika namn som identifierar en annonsgrupp. Maximala längden är 255 tecken; efterföljande tomma tecken sparas inte (t.ex. sparas&quot;Annonsgrupp 1&quot; som&quot;Annonsgrupp 1&quot;). Det här fältet gäller inte för sitelinks på kampanjnivå eller enhetsmål på kampanjnivå.</p> |
| Annonsgruppstyp | <p>Annonsgruppstypen: <span class="Option">Identifiering</span> (endast för identifieringskampanjer), <span class="Option">Visa</span> (för displaykampanjer), <span class="Option">Sök dynamiskt</span> (för expanderade dynamiska sökannonser), <span class="Option">Sökstandard</span> (för sökannonser), <span class="Option">Shoppingprodukt</span> (för produktannonser), <span class="Option">Shopping Showcase</span> (skapande och redigering stöds inte), eller <span class="Option">Okänd</span>.</p> |
| Max CPC | <p>(Endast CPC-kampanjer) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för ett reklamklick i annonsnätverket, med eller utan monetära symboler och interpunktion. Du kan ange värden för annonsgrupper och nyckelord, produktgrupper och dynamiska sökmål. Standardvärdet för ett nytt nyckelord ärvs från annonsgruppsnivån. För produktgrupper kan du ange värden för den lägsta produktgruppsnivån. standardvärdet för en ny nivå ärvs från den överordnade nivån.</p><p>För befintliga produktgrupper och dynamiska sökmål i optimerade portföljer gäller uppdateringarna endast en dag och skrivs över under nästa optimeringscykel.</p><p><b>Obs!</b> Använd fältet Max placement CPC för placeringar.</p> |
| Max Content CPC | <p>(Endast CPC-kampanjer) Den maximala innehållskostnaden per klick (CPC), som är den högsta summan att betala för ett reklamklick från en webbplats för webbannonser, med eller utan monetära symboler och interpunktion. Ni kan ange och redigera värden på annonsgruppsnivå i kampanjer som inte är riktade mot någon placering.</p> |
| Målmetod | <p>(Kampanjer endast i söknätverket och befintliga skrivskyddade Gmail-kampanjer i visningsnätverket) Om du vill:</p><ul><li><p><span style="font-style: italic;"><i>Mål och bud</i></span>: Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.</p></li><li><p><span style="font-style: italic;"><i>Endast bud</i></span>: Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå.</p><p>Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.</p></li></ul> |
| Nyckelord | Nyckelordssträngen. Maxlängden är 80 tecken och högst 10 ord, och den får endast innehålla bokstäver, siffror och följande specialtecken: space `# $ & _ - " [ ] ' + . / :`</p><p><b>Obs!</b></p><ul><li><p>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du Matcha typ till <span style="font-style: italic;"><i>Negativ</i></span>. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas nyckelordet för hela kampanjen.</p></li><li><p>Om du ändrar ett Google Ads-nyckelord eller en matchningstyp tas det befintliga nyckelordet bort och ett nytt skapas.</p></li></ul> |
| Placement | (Kampanjer som endast använder innehållsmatchning) En placering i det visningsnätverk där annonserna kan visas. Ange något av följande:</p><ul><li class="p"><p>Webbplats: Ange en giltig URL. Det kan vara en toppnivådomän, underdomän på första nivån eller domän med ett enda katalognamn. URL:en får inte innehålla ett frågetecken (?). Exempel:<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>En annonsposition på en viss sida: Använd formatet `<URL> >> <location,sublocation>` (till exempel `finance.google.com >> Company pages,Top right`).</p></li><li class="p"><p>En ämneskategori: Använd syntaxen `<category::<category> > <subcategory>` och så vidare (som `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Obs!</b> Om du vill exkludera en placering på annonsgruppen eller kampanjnivån anger du Matcha typ till <span style="font-style: italic;"><i>Negativ</i></span>. Om raden innehåller annonsgruppens namn kommer placeringen att exkluderas för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas placeringen för hela kampanjen.</p> |
| Automatiskt måluttryck | <p>(Krävs om kampanjinställningen &quot;Använd mitt webbplatsinnehåll för att rikta mina annonser&quot; inte är aktiverad. (i annat fall) Dynamiska sökmål för annonsgruppen.</p><p>Använd en asterisk för alla mål (*).</p><p>Om du vill ange upp till tre dynamiska sökvillkor använder du formatet `<category>=<target>`, där `<category>` kan innehålla någon av kategorierna nedan. Koppla samman flera mål för en enskild kategori med &quot;\[blanksteg\] och \[blanksteg\]&quot; och förena flera kategorier med &quot;[tomt utrymme] och [tomt utrymme]&quot;.</p><ul><li class="p"><p><span style="font-style: italic;"><i>Kategori</i></span>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med en specifik Google-innehållskategori.</p></li><li class="p"><p><span style="font-style: italic;"><i>URL</i></span>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.</p></li><li class="p"><p><span style="font-style: italic;"><i>Sidrubrik</i></span>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med specifik text i sidrubriken.</p></li><li class="p"><p><span style="font-style: italic;"><i>Sidinnehåll</i></span>: Om du vill visa expanderade dynamiska sökannonser för indexerade sidor med specifikt innehåll.</p></li></ul><p>Exempel: url=skor.example.com och page title=skos</p> |
| Överordnade produktgrupperingar | Hierarkin för överordnade produktgrupper.<br><br>Exempel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Produktgruppering | <p>Produktgruppen (till exempel&quot;brand=acme&quot; eller&quot;Alla produkter&quot;).</p><p><b>Obs!</b></p><ul><li><p>När en angiven produktgrupp inte finns i hierarkin för överordnade produktgrupper skapas de delar av hierarkin som behövs av sökningen, den sociala tjänsten och handeln.</p></li><li><p>Search, Social, &amp; Commerce skapar automatiskt en&quot;Alla produkter&quot;-grupp när du skapar en annonsgrupp i en Google Shopping-kampanj med ett standardbud som är inställt på annonsgruppens standardbud. Search, Social, &amp; Commerce skapar automatiskt en&quot;Allt annat&quot;-grupp med annonsgruppens standardbud på varje nivå i produktgruppshierarkin. Du kan fortfarande skapa dessa standardgrupper explicit och antingen exkludera dem eller ändra deras bud.</p></li><li><p>Varje annonsgrupp kan innehålla upp till åtta nivåer av produktgrupper, inklusive&quot;Alla produkter&quot; och sju andra nivåer.</p></li></ul> |
| Partitionstyp | Partitionstypen för produktgruppen: <i>deldivision</i> (när den har underordnade produktgrupper) eller <i>enhet</i> (när den inte har några underordnade produktgrupper). |
| Matcha typ | <p>För dynamiska sökmål eller produktgrupper: Nyckelordsmatchningsalternativet för det dynamiska sökmålet eller produktgruppen: <i>Dynamiskt annonsmål</i> (standard för nya dynamiska sökmål), <i>Produktgrupp</i> (standard för nya produktgrupper) eller <i>Negativ produktgrupp</i> (för att exkludera en produktgrupp).</p><p>För nyckelord: Nyckelordsmatchningsalternativet för nyckelordet: <span style="font-style: italic;"><i>Bred</i></span>, <span style="font-style: italic;"><i>Fras</i></span>, <span style="font-style: italic;"><i>Exakt</i></span>, eller <span style="font-style: italic;"><i>Negativ</i></span> (att utesluta ett nyckelord eller en placering i visningsnätverket), produktgrupper som ska användas med shoppingannonser har en matchande typ av <span style="font-style: italic;"><i>Produktgrupp</i></span>. Om du använder <span style="font-style: italic;"><i>Negativ</i></span>måste du också inkludera matchningstypen som ska uteslutas (till exempel &quot;Negativ fras&quot;).</p><p>För nya nyckelord är standardvärdet <span style="font-style: italic;"><i>Bred</i></span>. Ett värde för matchningstypen eller nyckelords-ID krävs bara för att redigera ett nyckelord med flera matchningstyper.</p><p><b>Obs!</b></p><ul><li><p>Matchningstyper gäller inte för expanderade dynamiska sökannonser, som inte använder nyckelord.</p></li><li><p>Om du ändrar matchningstypen för ett Google Ads-nyckelord tas det befintliga nyckelordet bort och ett nytt skapas.</p></li><li><p>För Bred Match Modifier väljer du &quot;Broad&quot; och infogar ett + före ett ord i nyckelordet för vilket det krävs närliggande varianter (t.ex. &quot;+red +skor&quot; för att kräva närliggande varianter av både &quot;red&quot; och &quot;skor&quot;). <b>Obs!</b> Många matchningsmodifierare har nu samma matchande beteende som frasmatchning för vissa språk, och du har inte kunnat skapa nya breda matchningsmodifieringsnyckelord sedan juli 2021. Se [Google-dokumentation](https://support.google.com/google-ads/answer/7042511) för mer information.</p> |
| Första sidanbudet | (Ingår i genererade kalkylblad i informationssyfte) Det bud som krävs för att placera en annons på första sidan i sökresultaten. Det här värdet är inte registrerat i annonsnätverket. |
| Kvalitetspoäng | (Ingår i genererade kalkylblad i informationssyfte) Det aktuella kvalitetsmoment som sökmotorn har tilldelat nyckelordet. Det här värdet är inte registrerat i annonsnätverket.) |
| Creative Preferred Devices | (Textannonser, utökade dynamiska sökannonser och utökade sitelinks; (valfritt) De enhetstyper som du föredrar att visa annonsen på: <span style="font-style: italic;"><i>Alla</i></span> (standard) eller <i>Mobil</i>. När <i>Mobil</i> anges försöker nätverket att visa annonsen för användare av mobila enheter i stället för för användare på datorer eller surfplattor. I annat fall visas annonsen på alla enhetstyper i nätverket.</p><p><b>Obs!</b></p><ul><li><p>Endast administratör och [!DNL Adobe] kontohanteraranvändare kan redigera den här inställningen.</p></li><li><p>Nätverket garanterar inte att annonsen visas på den önskade enhetstypen.</p></li><li><p>Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks.</p></li></ul> |
| Annonsrubrik, annonsrubrik 2-15 | (Endast expanderade textannonser och responsiva sökannonser) Rubrikerna i en annons, var och en avgränsade med ett vertikalt vertikalt vertikalt streck ( | ). Den maximala längden för varje annonstitelfält är 30 eller 15 dubbelbytetecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).</p><p>För responsiva sökannonser krävs annonsrubrik, annonsrubrik 2 och annonsrubrik 3, och alla andra annonsrubrikfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p><p>För responsiva sökannonser infogar du en annonsanpassare med följande format:</p><ul><li><p>Google Ads: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, till exempel `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:default text}`, till exempel `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser, som Google Ads tog bort i juni 2022. |
| Annonsrubrik 1-15 - position | <p>(Endast responsiva sökannonser.) (valfritt) En position där motsvarande annonsrubrik ska fästas: `[null]` (inget värde, vilket gör att annonsens titel kan användas för alla positioner), <i>1</i>, <i>2</i>, eller <i>3</i>. Om till exempel annonsrubrikens position har värdet 1 visas annonsrubriken bara i position 1. Som standard är alla annonsrubriker null (saknar värden).</p><p>Om du vill ta bort det befintliga värdet använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p><p><b>Obs!</b> Du kan fästa flera annonsrubriker på samma plats. Annonsnätverket använder en av de annonstitlar som är fästa vid positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen.</p> |
| Beskrivningsrad 1-4 | <p>(Utökade dynamiska sökannonser, utökade textannonser och responsiva sökannonser) Innehållet i en annons. Den maximala längden för varje beskrivningsfält är 90 eller 45 dubbelbytetecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).</p><p>För responsiva sökannonser infogar du en annonsanpassare med följande format:</p><ul><li><p>Google Ads: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, till exempel `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:default text}`, till exempel `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>Använd endast Description Line 1 och Description Line 2 för expanderade dynamiska sökannonser. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser, som Google Ads tog bort i juni 2022.</p><p>För responsiva sökannonser krävs Description Line 1 och Description Line 2, och Description Line 3 och Description Line 4 är valfria. Om du vill ta bort det befintliga värdet använder du värdet <code>[delete]</code> (inklusive hakparenteser).</p> |
| Beskrivningsrad 1-4 position | (Endast responsiva sökannonser.) (valfritt) En position där motsvarande beskrivning ska fästas: `[null]` (inget värde, vilket gör att beskrivningen kan användas för alla positioner), <i>1</i>, <i>2</i>, eller <i>3</i>. Om position för beskrivning 1 till exempel har värdet 1 visas bara position 1. Som standard är inga beskrivningar fästa vid en position.</p><p>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).</p><p><b>Obs!</b> Du kan fästa flera beskrivningar på samma plats. Annonsnätverket använder en av beskrivningarna som är fästa vid positionen. Beskrivningar som fästs vid position 2 kanske inte visas med annonsen. |
| Visa URL | Den URL som ingår i annonsen.<br><br>För expanderade dynamiska sökannonser genererar Google Ads det här värdet dynamiskt från webbplatsdomänen, och du behöver inte ange något värde.<br><br>För responsiva sökannonser behöver du inte ange något värde. Visnings-URL:en extraheras automatiskt från domänen i den slutliga URL:en. Du kan också anpassa URL-adressen med hjälp av fälten Sökväg 1 och Sökväg 2.<br><br>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser, som Google Ads tog bort i juni 2022.<br><br><b>Obs!</b> (Konton med slutliga URL:er) Domännamnen i den URL som visas och den slutliga URL:en måste matcha.</p> |
| Visningsbana 1 | <p>(Utökade textannonser<span> och responsiva sökannonser</span> endast)</p><p>(Valfritt) Text som läggs till i URL:en som automatiskt extraheras från den slutliga URL:en. Det föregås av ett snedstreck (/) i URL:en. En bana får inte innehålla snedstreck (/) eller radmatningstecken (\n). Maxlängden är 15 tecken eller 7 dubbelbyte-tecken.</p><p>Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde som ska infogas när din feed-fil inte innehåller ett giltigt värde:</p><ul><li><p>Google Ads: `{CUSTOMIZER.AdCustomizerName:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`</p></li><li><p>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`</p></li></ul><p>Om t.ex. Bildskärmssökväg 1 är &quot;erbjudanden&quot;, blir URL:en för visning &lt;<i>visa URL</i>>/deal, t.ex. www.example.com/deals.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser, som Google Ads tog bort i juni 2022.</p> |
| Visningsbana 2 | En andra visningsbana. se posten för Visningssökväg 1.<br><br>Exempel: Om Display Path 1 är &quot;offers&quot; och Display Path 2 är &quot;local&quot;, är display URL &lt;<i>visa URL</i>>/deal/local, t.ex. www.example.com/deals/local.</p><p>Du kan inte skapa eller redigera, men du kan ta bort utökade textannonser, som Google Ads tog bort i juni 2022.</p> |
| Kampanjlinje | (Endast Google produktlistningsannonser) En valfri kampanjrad som ska inkluderas i produktlistan i sökresultaten. Maxlängden är 45 tecken.</p><p>Kampanjraden kan visas på olika platser i förhållande till annonsen (t.ex. nedanför annonsen) beroende på var annonsen visas på sidan. |
| Länknamn | <p>Sitelink-texten. Den kan innehålla upp till 25 tecken.</p><p>För nya sitelinks måste du inkludera kampanjnamnet i sitelink-raden. För annonser på gruppnivå måste du även inkludera annonsgruppens namn.</p><p><b>Obs!</b> Befintlig text med 35 tecken visas fortfarande i annonser på datorer och surfplattor, men inte på mobila enheter.</p> |
| Mobilappsplattform (Google Adwords) | (Endast befintliga programinstallationer) Det operativsystem som mobilprogrammet körs på: <i>Android™</i> eller <i>ios</i>. |
| ID för mobilapp (Google Adwords) | (Endast befintliga appinstalleringsannonser) <p>Program-ID eller paketnamn. |
| Namn på mobilapp (Google Adwords) | (Endast befintliga programinstallationer) Programmets namn. |
| Startdatum | <p>(Endast utökade sitelinks) Det första datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format: <span style="font-style: italic;"><i>m/d/yyyy</i></span>, <span style="font-style: italic;"><i>m/d/yy</i></span>, <span style="font-style: italic;"><i>m-d-yyyy</i></span>, eller <span style="font-style: italic;"><i>m-d-yy</i></span>. Standardinställningen för nya utökade sitelinks är den aktuella dagen.</p><p><b>Obs!</b> Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks.</p> |
| Slutdatum | <p>(Endast utökade sitelinks) Det sista datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format:  <span style="font-style: italic;"><i>m/d/yyyy</i></span>, <span style="font-style: italic;"><i>m/d/yy</i></span>, <span style="font-style: italic;"><i>m-d-yyyy</i></span>, eller <span style="font-style: italic;"><i>m-d-yy</i></span>. Standardvärdet är inget (inget slutdatum).</p><p><b>Obs!</b> Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks.</p> |
| Exkludera surfplatta (Google Adwords) | (Endast befintliga appinstalleringsannonser)</p><p>(Valfritt) Hindrar Google Ads från att visa annonsen för surfplatteanvändare. Värdena kan innehålla <i>ja</i> och <i>no</i>. |
| Landningssidesuffix | Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Exempel: `param2=value1&param3=value2`<br><br>Se &quot;[Klickningsspårningsformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br>Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du Google Ads Editor. |
| Spårningsmall | Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårar parametrar och bäddar in den slutliga URL:en i en ValueTrack-parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet längst till granulerad) åsidosätter värdena på alla högre nivåer.<br><br>För spårning av konvertering av Adobe Advertising, som används när kampanjinställningarna innehåller &quot;EF-omdirigering&quot; och &quot;Automatisk överföring&quot;, läggs i Search, Social och Commerce automatiskt till en egen omdirigerings- och spårningskod när du sparar posten.<br><br>Ange ett värde för omdirigeringar och spårning från tredje part. En lista med ValueTrack-parametrar som anger de slutliga URL:erna i spårningsmallar finns i parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängliga ValueTrack-parametrar&quot; i dialogrutan <a href="https://support.google.com/google-ads/answer/2375447?hl=en" target="_blank">Google Ads-dokumentation</a>.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Bas-URL/slutlig URL | Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas-/slutadresser på nyckelordsnivå åsidosätter de på annonsnivå och högre.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Mål-URL | (Ingår i genererade kalkylblad för informationsändamål. inte publicerad i sökmotorn) För konton med mål-URL:er är detta den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och handel. Om du genererade spårnings-URL:er baseras detta på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till sökmotorspecifika parametrar kan de ersättas med motsvarande parametrar för Sök, Socialt och Handel.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som kolumnen Bas-URL/Slutlig URL. |
| Anpassad URL-parameter | Data som ska ersätta `{custom_code}` dynamisk variabel när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL:en måste du överföra kalkylbladsfilen med alternativet Generera spårnings-URL:er. |
| Kreativ typ | Annonsformatet: <i>Text ad</i>, <i>Utökad text och</i>, <i>Dynamisk sökannons</i> (inaktuell annonstyp), <i>Utökad dynamisk sökning och</i>, <i>Visa annons</i>, <i>App Install-annons</i> (borttagen), <i>Bild</i> <i>Produktannons</i> (kundannonser), eller <i>Responsiv sökannons</i>. Standardinställningen för nya annonser är <i>Text ad</i>.<br><br>Krävs för att skapa eller redigera status för en produktannons. |
| Param1 | <p>Det numeriska värdet för `{param1}` ad-parameter, som kan inkluderas i annonskopian eller visa URL för valfri annons i kalkylbladsfilen. Maxlängden är 25 tecken och du kan inkludera följande icke-numeriska tecken:</p><ul><li><p>Värdet kan föregås eller läggas till med en valutasymbol eller valutakod. Till exempel: `£2.000,00` och `2000GBP` är giltiga.</p></li><li><p>Värdet kan innehålla ett komma (`,`) eller punkt (`.`) som avgränsare, med en valfri punkt (`.`) eller komma (`,`) för decimalvärden. Till exempel: `1,000.00` och `2.000,10` är giltiga.</p></li><li><p>Värdet kan prefixeras eller läggas till med ett procenttecken (`%`), plustecken (`+`), eller minustecken (`- `). Till exempel: `20%`, `208+`och `-42.32` är giltiga.</p></li><li><p>Två tal kan bäddas in med ett snedstreck. Till exempel: `4/1` och `0.95/0.45` är giltiga.</p></li></ul><p>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).</p> |
| Param2 | Det numeriska värdet för `{param2}` ad-parameter, som kan inkluderas i annonskopian eller visa URL för valfri annons i kalkylbladsfilen. Mer information finns under Param1. |
| Målgrupp | Återmarknadsföringslistan för sökannonser (RLSA) som riktar sig till målgrupp eller exkluderad publik för kampanjen eller annonsgruppen. Ange om det är ett mål eller undantag i fältet Måltyp. |
| Måltyp | (När en publik anges) Anger om den angivna målgruppen är en <i>Inkludering</i> (target) eller <i>Uteslutning</i>. |
| Kampanjstatus | Visningsstatus för kampanjen: <i>Aktiv</i>, <i>Pausad</i>, <i>Avslutade</i> (inte redigerbart), eller <i>Borttagen</i> (endast befintliga kampanjer). Standardinställningen för nya kampanjer är <i>Aktiv</i>. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet <i>Borttagen</i>. |
| Annonsgruppsstatus | Annonsgruppens visningsstatus: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga annonsgrupper). Standardvärdet för nya annonsgrupper är Aktiv. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet `Deleted`. |
| Nyckelordsstatus | Visningsstatus för nyckelordet: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är Aktiv. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet <i>Borttagen</i>. |
| Annonsstatus | Annonsens visningsstatus: <i>Aktiv</i>, <i>Borttagen</i> (endast befintliga annonser), <i>Avvisad</i> (inte redigerbart), eller <i>Pausad</i>. Standardinställningen för nya annonser är Aktiv. Om du vill ta bort en aktiv eller pausad annons anger du värdet <i>Borttagen</i>. |
| Placeringsstatus | Status för webbplatsplaceringen: <span style="font-style: italic;"><i>Aktiv</i></span>, <span style="font-style: italic;"><i>Pausad</i></span>, eller <span style="font-style: italic;"><i>Borttagen</i></span> (endast befintliga annonser). Standardinställningen för nya webbplatser är <span style="font-style: italic;"><i>Aktiv.</i></span> Om du vill ta bort en aktiv eller pausad placering anger du värdet <span style="font-style: italic;"><i>Borttagen</i></span>. |
| Målstatus | Status för ett dynamiskt sökmål: <span style="font-style: italic;"><i>Aktiv</i></span>, <span style="font-style: italic;"><i>Pausad</i></span>, eller <span style="font-style: italic;"><i>Borttagen</i></span> (endast befintliga mål). Standardinställningen för nya mål är <span style="font-style: italic;"><i>Aktiv.</i></span> Om du vill ta bort ett aktivt eller pausat mål anger du värdet <span style="font-style: italic;"><i>Borttagen</i></span>. |
| Produktgruppstatus | Produktgruppens visningsstatus: <span style="font-style: italic;"><i>Aktiv</i></span> <span>eller</span> <span style="font-style: italic;"><i>Borttagen</i></span> (endast befintliga produktgrupper). Standardvärdet för nya produktgrupper är <span style="font-style: italic;"><i>Aktiv</i></span>. Om du vill ta bort en aktiv produktgrupp anger du värdet <span style="font-style: italic;"><i>Borttagen</i></span>. |
| Status för webbplatslänkar | Sitelänkens visningsstatus: <span style="font-style: italic;"><i>Aktiv eller borttagen</i></span> (endast befintliga sitelinks). Standardinställningen för nya sitelinks är <span style="font-style: italic;"><i>Aktiv</i></span>. Om du vill ta bort en aktiv platslänkar anger du värdet <span style="font-style: italic;"><i>Borttagen</i></span>. |
| Platsstatus | Status för platsmålet: <i>Aktiv</i> eller <i>Borttagen</i> (endast befintliga platser). Standardvärdet för nya platser är Aktiv. Om du vill ta bort en aktiv plats anger du värdet <i>Borttagen</i>. |
| RLSA-målstatus | Status för kampanj- eller annonsnivå-RLSA-målet eller (endast Google Ads)-undantaget: <span style="font-style: italic;"><i>Aktiv eller borttagen</i></span> (endast befintliga mål). Standardinställningen för nya mål eller undantag är <span style="font-style: italic;"><i>Aktiv</i></span>. Om du vill ta bort ett aktivt mål eller undantag anger du värdet <span style="font-style: italic;"><i>Borttagen</i></span>. |
| Status för enhetsmål | <p>Status för enhetsmålet på kampanj- eller annonsnivå: <span class="Option">Aktiv</span> eller <span class="Option">Borttagen</span>. För nya kampanjer och annonsgrupper är standardvärdet <span class="Option">Aktiv</span>.</p> |
| \[Advertiser-specific Label Classification\] | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden tillämpas på alla underordnade komponenter. nya komponenter som läggs till senare kopplas automatiskt till etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Varken klassificeringsnamnet eller klassificeringsvärdet är skiftlägeskänsligt. |
| Begränsningar | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><b>>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| Kampanj-ID | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| Annonsgrupp-ID | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| Nyckelords-ID | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| Annons-ID | <p>Det unika ID som identifierar en befintlig annons. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] För responsiva sökannonser krävs antingen annons-ID eller AMO-ID för att redigera eller ta bort annonsdata. För alla andra entitetstyper krävs annons-ID bara när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna.</p><p><b>Obs!</b> Om du redigerar a) och egenskapskolumner förutom Status för en befintlig annons eller b) data för en responsiv sökannons, och du varken inkluderar ID:t eller ID:t för AMO, skapas en ny annons och den befintliga annonsen ändras inte.</p> |
| Placement-ID | Det unika ID som identifierar en webbplatsplacering. Krävs endast när du ändrar eller tar bort placeringen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera placeringen eller b) ett AMO-ID. |
| Mål-ID | Det unika ID som identifierar ett befintligt automatiskt mål. Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller ett AMO-ID för målet. |
| Produktgrupp-ID | Det unika ID som identifierar en befintlig produktgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) ett AMO-ID. |
| Platslänks-ID | Det unika ID som identifierar en befintlig platslänk. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitellänken eller b) ett AMO-ID.&quot; Om du däremot inte inkluderar något platslänks-ID eller AMO-ID, och egenskapskolumnerna matchar flera sitelinks, ändras bara statusen för en av sitelinks.</p><p><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du varken inkluderar Sitelink ID eller AMO ID, skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| Mål-ID för RLSA | Det unika ID som identifierar ett befintligt RLSA-mål på kampanj- eller annonsnivå eller (endast Google Ads)-undantag. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet eller undantaget, såvida inte raden innehåller ett AMO-ID för målet. |
| Målenhets-ID | <p>Det unika ID som identifierar ett befintligt enhetsmål eller undantag på kampanjnivå eller annonsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller ett AMO-ID för målet.</p> |
| AMO-ID | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar annons-ID:t. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| EF-felmeddelande | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden finns i EF-felfiler. Det här värdet är inte registrerat i annonsnätverket. |
| SE-felmeddelande | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden ingår i SE-felfiler. Det här värdet är inte registrerat i annonsnätverket. |
| Begäran om undantag | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa namn och text för alla Google reklampolicyer som en annons bryter mot. |
| Butikshash | (Ingår i informationssyfte i kalkylblad som genererats med Advanced Campaign Management) En alfanumerisk hash-kod (t.ex. f9639f40cdf56524b541e5dacf55a991) som anger att objektet genererades i vyn Avancerat (ACM). |

<table style="table-layout:auto">

## Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent

### Kampanjfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| Kampanjbudget | Obligatoriskt: Skapa<br><br>>Valfritt: Redigera eller ta bort | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| Leveranssätt | Obligatoriskt: Skapa<br><br>Valfritt: Redigera eller ta bort |
| Kanaltyp | Obligatoriskt: Skapa<br><br>Valfritt: Redigera eller ta bort |
| Nätverk | Obligatoriskt: Skapa<br><br>Valfritt: Redigera eller ta bort |
| DSA-domännamn | Obligatoriskt: Skapa<br><br>Valfritt: Redigera eller ta bort |
| Domänspråk för DSA | Obligatoriskt: Skapa<br><br>Valfritt: Redigera eller ta bort |
| Kampanjprioritet | Obligatoriskt/valfritt: Skapa<br><br>Valfritt/ej tillämpligt: Redigera eller ta bort |
| Affärs-ID | Obligatoriskt/valfritt: Skapa<br><br>Valfritt/ej tillämpligt: Redigera eller ta bort |
| Försäljningsland | Obligatoriskt/valfritt: Skapa<br><br>Valfritt/ej tillämpligt: Redigera eller ta bort |
| Filter för produktomfång | Valfritt |
| Språk | Valfritt |
| Enhetsmål | Valfritt |
| Operativsystemmål för enhet (Google Adwords) | Valfritt |
| Mobiloperatörer (Google Adwords) | Valfritt |
| Målmetod | n/a |
| Landningssidesuffix | <p>Valfritt |
| Spårningsmall | Valfritt |
| Kampanjstatus | Valfritt: Skapa eller redigera<br><br>Obligatoriskt: Ta bort |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Annonsgruppsfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Nätverk | n/a |
| Anpassad GDN-anbudsnivå | Valfritt |
| Namn på annonsgrupp | Obligatoriskt |
| Annonsgruppstyp | Obligatoriskt |
| Max CPC | Valfritt |
| Max Content CPC | Valfritt |
| Målmetod | Obligatoriskt |
| Spårningsmall | Valfritt |
| Annonsgruppsstatus | Valfritt: Skapa eller redigera<br><br>Obligatoriskt: Ta bort |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Annonsgrupp-ID | Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Nyckelordsfält

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Max CPC | Valfritt |
| Nyckelord | Obligatoriskt |
| Matcha typ | Valfritt: Skapa<br><br>Obligatoriskt/valfritt: Redigera eller ta bort |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Param1 | Valfritt |
| Param2 | Valfritt |
| Nyckelordsstatus | Valfritt: Skapa eller redigera<br><br>Obligatoriskt: Ta bort |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Nyckelords-ID | Krävs endast när du redigerar eller tar bort nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Placeringsfält

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Max Placement CPC (Google Adwords) | Valfritt |
| Max Placement CPM (Google Adwords) | Valfritt |
| Placement | Obligatoriskt |
| Matcha typ | Obligatoriskt |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Placeringsstatus | Valfritt: Skapa eller redigera<br><br>Obligatoriskt: Ta bort |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Placement-ID | Krävs endast när du redigerar eller tar bort placeringen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera placeringen eller b) ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Utökad dynamisk sökannons

Den här annonstypen kallas nu&quot;dynamisk sökannons&quot; i [!DNL Google Ads]. Mer information om hur du skapar dynamiska sökannonser finns i &quot;[Implementera [!DNL Google Ads] dynamiska sökannonser](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html?lang=en).&quot;

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Creative Preferred Devices | Valfritt |
| Beskrivningsrad 1-2 | Krävs för att skapa en annons eller redigera beskrivningen. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| Visa URL | Obligatoriskt |
| Spårningsmall | Valfritt |
| Kreativ typ | Krävs för att skapa eller redigera status för en produktannons. |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Produktlista/reklamfält

Mer information om hur du skapar shoppingannonser finns i &quot;[Implementera Google Ads shoppingkampanjer](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html?lang=en).&quot;

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Kampanjlinje | Valfritt |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Kreativ typ | Krävs för att skapa eller redigera status för en produktannons. |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Reklamfält för responsiv sökning

Använd &quot;[!UICONTROL Responsive Search Ad]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt | |
| Annonsrubrik, annonsrubrik 2-15 | För responsiva sökannonser krävs annonsrubrik, annonsrubrik 2 och annonsrubrik 3, och alla andra annonsrubrikfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser). |
| Annonsrubrik 1-15 - position | Valfritt |
| Beskrivningsrad 1-4 | För responsiva sökannonser krävs Description Line 1 och Description Line 2, och Description Line 3 och Description Line 4 är valfria. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Beskrivningsrad 1-4 position | Valfritt |
| Visningsbana 1 | Valfritt |
| Visningsbana 2 | Valfritt |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Krävs för att skapa en annons. |
| Anpassad URL-parameter | Valfritt |
| Kreativ typ | Valfritt |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs för att redigera eller ta bort annonser såvida inte raden innehåller ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort annonser såvida du inte inkluderar annons-ID:t. |

### Text och fält

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

>[!NOTE]
>
>Utökade textannonser togs bort i juni 2022. Du kan bara ta bort befintliga textannonser.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Creative Preferred Devices | Skrivskyddad |
| Annonsrubrik, annonsrubrik 2-3 | Skrivskyddad |
| Beskrivningsrad 1-2 | Skrivskyddad |
| Visa URL | Skrivskyddad |
| Visningsbana 1 | Skrivskyddad |
| Visningsbana 2 | Skrivskyddad |
| Spårningsmall | Skrivskyddad |
| Bas-URL/slutlig URL | Skrivskyddad |
| Anpassad URL-parameter | Skrivskyddad |
| Kreativ typ | Valfritt |
| Annonsstatus | Obligatoriskt |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökmålfält (automatiskt mål)

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Max CPC | Valfritt |
| Automatiskt måluttryck | Krävs när kampanjinställningen &quot;Använd mitt webbplatsinnehåll för att rikta mina annonser&quot; inte är aktiverad. annars valfritt. |
| Matcha typ | Valfritt |
| Målstatus | Krävs för att ta bort ett mål |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Mål-ID | Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller ett AMO-ID för målet. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Fält för produktgrupp som köpts

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Max CPC | Krävs för att skapa en produktgrupp. |
| Överordnade produktgrupperingar | Obligatoriskt |
| Produktgruppering | Obligatoriskt |
| Partitionstyp | Krävs för att skapa en produktgrupp. |
| Matcha typ | Valfritt |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Obligatoriskt |
| Produktgruppstatus | Krävs endast för att ta bort en produktgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Produktgrupp-ID | Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Sitelink-fält på kampanjnivå och annonsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Krävs för sitelinks på annonsnivå. Gäller inte för sitelinks på kampanjnivå. |
| Creative Preferred Devices | Valfritt |
| Länknamn | Obligatoriskt |
| Startdatum | Valfritt |
| Slutdatum | Valfritt |
| Spårningsmall | Valfritt |
| Bas-URL/slutlig URL | Obligatoriskt |
| Status för webbplatslänkar | Krävs endast för att ta bort en sitellänk. |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Platslänks-ID | Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitellänken eller b) ett AMO-ID.&quot; Om du däremot varken inkluderar Sitelinks-ID eller AMO-ID och egenskapskolumnerna matchar flera sitelinks, ändras statusen för endast en av sitelinks.<br><br><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du inte inkluderar vare sig Sitelink ID eller AMO ID, skapas en ny sitelink och den befintliga sitelink ändras inte. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för plats

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Plats | Krävs för att skapa eller redigera ett platsmål. |
| Platstyp | Valfritt |
| Anpassa via bud | Valfritt |
| Platsstatus | Krävs endast för att ta bort ett platsmål. |
| Kampanj-ID | Valfritt |
| AMO-ID | Krävs för att redigera eller ta bort data om du inte inkluderar kampanj-ID:t.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

## Målfält på kampanjnivå och annonsgruppsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Enhet | Krävs för att skapa eller redigera ett enhetsmål. |
| Anpassa via bud | Valfritt |
| Namn på annonsgrupp | Krävs för enhetsmål på annonsnivå. Gäller inte för enhetsmål på kampanjnivå. |
| Status för enhetsmål | Krävs endast för att ta bort ett enhetsmål. |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt endast för enhetsmål på annonsnivå. |
| Målenhets-ID | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller ett AMO-ID för målet. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhetens mål-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

## Mål-/exkluderingsfält för RLSA på kampanjnivå och annonsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Anpassa via bud | Valfritt |
| Namn på annonsgrupp | Krävs för annonsnivåmål och undantag. Gäller inte för kampanjnivåmål och undantag. |
| Målgrupp | Krävs för att skapa ett nytt mål eller undantag. |
| Måltyp | Krävs för att skapa ett nytt mål eller undantag. |
| RLSA-målstatus | Krävs endast för att ta bort ett mål eller ett undantag. |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt Gäller endast för mål och undantag på annonsnivå. |
| Mål-ID för RLSA | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller ett AMO-ID för målet. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar mål-ID:t för RLSA.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

[^1]: [!DNL Excel] konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

>[!MORELIKETHIS]
>
>* [Bilaga - Fallkalkylbladsfel](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Filformat för kalkylblad som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickningsspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överföra en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
