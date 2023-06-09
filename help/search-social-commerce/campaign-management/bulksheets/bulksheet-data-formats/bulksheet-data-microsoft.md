---
title: Obligatoriska kalkylbladsdata för [!DNL Microsoft Advertising] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för [!DNL Microsoft Advertising] konton.
source-git-commit: 384515330bfb980e7549128a1aa890df8fa1c463
workflow-type: tm+mt
source-wordcount: '7579'
ht-degree: 1%

---

# Bilaga - Obligatoriska data för kalkylblad för [!DNL Microsoft Advertising] konton

Skapa och uppdatera [!DNL Microsoft Advertising] kampanjdata i grupp kan du använda bulkbladsfiler för sökning, sociala medier och handel som är särskilt formaterade för [!DNL Microsoft Advertising] konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det önskade filformatet eller b) skapa dem manuellt (se &quot;[Filformat för bulkblad som stöds](bulksheet-file-formats.md)&quot; för allmän information om vilka filformat som stöds).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alla tillgängliga datafält

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Fält | Beskrivning |
|----|----|
| Plattform | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kontonamn | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Det unika namn som identifierar en kampanj för ett konto. Maximala längden är 128 tecken. |
| Kampanjbudget | Den dagliga eller månadsvisa kampanjbudgeten, med eller utan monetära symboler och interpunktion. Den får inte vara mindre än 0,05. |
| Kanaltyp | Den typ av kanal som kampanjen har som mål: <i>Målgrupp</i>, <i>DynamicSearchAds</i>, <i>Sök</i>, eller <i>Shopping</i>. |
| Leveranssätt | (Endast kampanjer med daglig budget) Så här snabbt kan du visa annonser för kampanjen varje dag:<ul><li><i>Standard (distribuerad)</i> (standard för nya kampanjer): För att sprida annonsintrycket över hela dagen.</li><li><i>Accelererad:</i> Visa era annonser så ofta som möjligt tills budgeten är nådd. Därför kanske era annonser inte visas senare under dagen.</li></ul> |
| Kampanjprioritet | (Endast köpkampanjer) Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt: <i>Låg</i> (standard för nya kampanjer), <i>Medel</i>, eller <i>Hög</i>.<br><br>När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad. |
| Affärs-ID | (Kundkampanjer och målgruppskampanjer som endast är kopplade till en handlarfeed) Kund-ID för det handlarkonto vars produkter används för kampanjen. |
| Försäljningsland | (Endast köpkampanjer. skrivskyddad för befintliga kampanjer) Det land där kampanjprodukterna säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen. |
| Filter för produktomfång | (Kampanjer som endast använder shoppingnätverket) De produkter på ert handelskonto för vilka produktannonser kan skapas för kampanjen. Du kan ange upp till sju produktdimensioner och attributkombinationer där du kan filtrera dina produkter med formatet dimension=attribut. Avgränsa flera filter med avgränsaren &quot;>>&quot;. En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanjer](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Exempel: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Om du vill ta bort de befintliga värdena använder du värdet `[delete]` (inklusive hakparenteser). |
| DSA-domännamn | (Kampanjer av typ a)<i>DynamicSearchAds</i>&quot; eller b) &quot;<i>Sök</i>&quot; när elementet ExperimentId inte är inställt) Webbplatsens domännamn som mål för dynamiska sökannonser. Maxlängden är 2 048 tecken. Om domännamnet innehåller `www`, trimmas och används inte.<br><br>För befintliga kampanjer kan du inte redigera domänen, men du måste inkludera den för att kunna uppdatera andra egenskaper. |
| Domänspråk för DSA | (Kampanjer av typ a)<i>DynamicSearchAds</i>&quot; eller b) &quot;<i>Sök</i>&quot; när elementet ExperimentId inte är inställt) Språket för webbplatssidorna som ska användas för dynamiska sökannonser. De domänspråk som stöds är holländska, engelska, franska, tyska, italienska, spanska och svenska.<br><br>För befintliga kampanjer kan du inte redigera språket, men du måste inkludera det för att kunna uppdatera andra egenskaper. |
| Namn på annonsgrupp | Det unika namn som identifierar en annonsgrupp. Maximala längden är 128 tecken. Efterföljande tomma tecken sparas inte (till exempel sparas&quot;Annonsgrupp 1&quot; som&quot;Annonsgrupp 1&quot;). |
| Annonsgruppstyp | (Kampanjer i söknätverket). skrivskyddad för befintliga annonsgrupper) Annonsgruppstypen: <i>Målgrupp</i> (endast för målgruppskampanjer), <i>Sök dynamiskt</i> (endast för dynamiska sökannonser) och <i>Sökstandard</i> (endast för responsiva sökannonser och befintliga expanderade textannonser). Vissa kampanjtyper kan innehålla flera typer av annonsgrupper. |
| Nyckelord | (Endast kampanjer i söknätverket) Nyckelordssträngen. Maximala längden är 50 tecken.<br><br><b>Anteckningar:</b><ul><li>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du Matcha typ till `Negative`. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas nyckelordet för hela kampanjen.</li><li>Ändra en [!DNL Microsoft Advertising] nyckelordet tar bort det befintliga nyckelordet och skapar ett nytt med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.</li></ul> |
| Placement | Föråldrat |
| Målgrupp | Återmarknadsföringslistan för sökannonser (RLSA) som riktar sig till målgruppen för kampanjen eller annonsgruppen. |
| Måltyp | (Endast RLSA-mål) Måltypen: <i>Inkludering</i> eller <i>Uteslutning</i>. |
| Automatiskt måluttryck | Dynamiska sökmål för annonsgruppen. Använd Alla webbsidor för alla mål.<br><br>Om du vill ange upp till tre dynamiska sökvillkor använder du formatet `<category>=<target>`, där &lt;category> kan innehålla någon av kategorierna nedan. Koppla flera mål för en enskild kategori med`[blank space] and [blank space]`&quot; och koppla ihop flera kategorier med &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Kategori:</i> Så här visar du dynamiska sökannonser för indexerade sidor med en viss innehållskategori i Google.</li><li><i>URL:</i> Om du vill visa dynamiska sökannonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.</li><li><i>Sidrubrik:</i> Om du vill visa dynamiska sökannonser för indexerade sidor med specifik text i sidtiteln.</li><li><i>Sidinnehåll:</i> Så här visar du dynamiska sökannonser för indexerade sidor med specifikt innehåll.</li></ul>Exempel: url=skor.example.com och page title=skos<br>Exempel: Alla webbsidor |
| Plats | En geografisk plats där annonser för kampanjen eller annonsgruppen ska placeras. värdena inte är skiftlägeskänsliga. Om du inte anger några värden för kampanjen eller annonsgruppen anges alla platser som mål. Om du vill ange särskilda målplatser anger du platsen med [!DNL Microsoft Advertising] platskodformat. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. <b>Obs!</b> Om du vill utesluta en plats skriver du ett minustecken före platskoden (`-`), till exempel `-United States`. |
| Platstyp | Platstypen, till exempel Ort, Land, MetroArea, Postnummer och Delstat. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. |
| Matcha typ | (Endast kampanjer i söknätverket) Nyckelordsmatchningsalternativ. Detta kan inkludera nyckelordsmatchningsalternativet för ett dynamiskt sökmål eller en produktgrupp. Värdena är: <i>Bred</i> (standard för nya nyckelord), <i>Exakt</i>, <i>Fras</i>, <i>Innehåll</i> (anges automatiskt för nyckelord när annonsgruppen har innehållsnätverket som mål), <i>Negativ</i> (för att utesluta ett nyckelord i innehållsnätverket), <i>Dynamiskt annonsmål</i> (standard för nya dynamiska sökmål), <i>Produktgrupp</i> (standard för nya produktgrupper), eller <i>Negativ produktgrupp</i> (för att exkludera en produktgrupp).  Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper.<br><br>För Bred Match Modifier väljer du &quot;Broad&quot; och infogar en `+` före ett ord i nyckelordet som krävs (till exempel &quot;`+red +shoes`&quot; att kräva både&quot;röd&quot; och&quot;skor&quot;).<br><br>Ändra matchningstyp för en [!DNL Microsoft Advertising] nyckelordet tas inte bort. |
| Max CPC | (Kampanjer i söknätverket) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för en annons baserat på nyckelordet, produktgruppen eller det dynamiska sökmålet, med eller utan monetära symboler och interpunktion.  För befintliga nyckelords- och produktgruppsposter i optimerade portföljer gäller uppdateringarna endast en dag och skrivs över under nästa optimeringscykel. <b>Obs!</b> Du kan inte ange anbud för negativa nyckelord. |
| Max Content CPC | (Endast skrivskyddat för CPC-kampanjer som skapats innan innehållsnätverket togs bort 2017) Den maximala innehållskostnaden per klick (CPC), som är den högsta summan att betala för ett reklamklick från en webbplats i visningsnätverk, med eller utan monetära symboler och interpunktion. |
| Målmetod | (Målgrupper och grupper) Om:<ul><li><i>Mål och bud:</i> Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.</li><li><i>Endast bud:</i>Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå.</li></ul> Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper. |
| Överordnade produktgrupperingar | Hierarkin för överordnade produktgrupper.<br><br>Exempel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Produktgruppering | Produktgruppen (till exempel&quot;brand=acme&quot; eller&quot;Alla produkter&quot;).<br><br><b>Anteckningar:</b><ul><li>När en angiven produktgrupp inte finns i hierarkin för överordnade produktgrupper skapas de delar av hierarkin som behövs av sökningen, den sociala tjänsten och handeln.</li><li>Search, Social, &amp; Commerce skapar automatiskt en&quot;Alla produkter&quot;-grupp när du skapar en annonsgrupp i en Google Shopping-kampanj med ett standardbud som är inställt på annonsgruppens standardbud. Search, Social, &amp; Commerce skapar automatiskt en&quot;Allt annat&quot;-grupp med annonsgruppens standardbud på varje nivå i produktgruppshierarkin. Du kan fortfarande skapa dessa standardgrupper explicit och antingen exkludera dem eller ändra deras bud.</li><li>Varje annonsgrupp kan innehålla upp till åtta nivåer av produktgrupper, inklusive&quot;Alla produkter&quot; och sju andra nivåer.</li></ul> |
| Partitionstyp | Partitionstypen för produktgruppen: <i>deldivision</i> (när den har underordnade produktgrupper) eller <i>enhet</i> (när den inte har några underordnade produktgrupper). |
| Annonsrubrik, annonsrubrik 2-15 | (Endast expanderade textannonser, multimediaannonser, responsiva annonser och responsiva sökannonser) Rubrikerna i en annons. Den maximala längden för varje annonstitelfält är 30 eller 15 dubbelbytetecken, inklusive all dynamisk text (t.ex. värdena för nyckelord, `{Param2}` och `{Param3}` dynamiska ersättningsvariabler och annonsanpassare).<br><br> För responsiva sökannonser infogar du en annonsanpassare med följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För expanderade textannonser krävs annonsrubrik och annonsrubrik 2 och annonsrubrik 3 är valfritt. [!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser krävs annonsrubrik, annonsrubrik 2 och annonsrubrik 3, och alla andra annonstitelfält är valfria.<br><br>Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser).<br><br>För alla annonstyper utom för expanderade textannonser tas den befintliga annonsen bort om du ändrar annonsen och skapar en ny annons med samma egenskaper. |
| Annonsrubrik 1-15 - position | (Endast responsiva sökannonser.) (valfritt) En position där motsvarande annonsrubrik ska fästas: `[null]` (inget värde, vilket gör att annonsrubriken kan användas för alla positioner), 1, 2 eller 3. Om till exempel annonstitelposition har värdet 1 visas annonsrubrik bara i position 1. Som standard är alla annonsrubriker null (saknar värden). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Obs!</b> Du kan fästa flera annonsrubriker på samma plats. Annonsnätverket kommer att använda en av de annonstitlar som är fästa vid positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen. |
| Beskrivningsrad 1-4 | (Endast textannonser, dynamiska sökannonser, multimediaannonser, responsiva sökannonser och förbättrade sitelinks på kampanjnivå) Innehållet i en annons eller en sitelink.<br><br>För sitelinks kan du använda både Description Line 1 och Description Line 2 för att inkludera extra text som annonsnätverket kan visa under länktexten. Varje beskrivningsfält kan innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>För annonser är den maximala längden för varje beskrivningsfält 90 eller 45 dubbelbyte-tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).<br><br>För responsiva sökannonser infogar du en annonsanpassare med följande format, där Standardtext är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För textannonser och dynamiska sökannonser krävs Description Line 1 och Description Line 2 är valfri.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser krävs Description Line 1 och Description Line 2, och Description Line 3 och Description Line 4 är valfria.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Anteckningar:</b><ul><li>(Standardtextannonser) Den kombinerade titeln och texten måste vara minst tre ord.</li><li>(Utökade textannonser) Det här fältet kan även innehålla {Param2} och {Param3} dynamiska ersättningsvariabler. I så fall är annonstextens maximala längd 300 enkelbyte- eller 150 dubbelbyte-tecken. [!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li><li>(Dynamiska sökannonser) Dynamisk ersättningstext tillåts inte.</li><li>För alla annonstyper utom expanderade textannonser tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas.</li></ul> |
| Beskrivningsrad 1-4 position | (Endast responsiva sökannonser.) (valfritt) En position där motsvarande beskrivning ska fästas: `[null]` (inget värde, vilket gör att beskrivningen kan användas för alla positioner), 1, 2 eller 3. Om till exempel position för beskrivning 1 har värdet 1 visas bara beskrivning 1 i position 1. Som standard är inga beskrivningar fästa vid en position.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Obs!</b> Du kan fästa flera beskrivningar på samma plats. Annonsnätverket använder en av beskrivningarna som är fästa vid positionen. Beskrivningar som fästs vid position 2 kanske inte visas med annonsen. |
| Företagsnamn | (Endast multimediaannonser) Företagsnamnet, med högst 25 tecken. |
| Kampanjlinje | (Endast produktlistade annonser) En unik kampanjrad som ska inkluderas i produktlistan i sökresultaten (till exempel&quot;Fraktfritt nu!). Maxlängden är 45 tecken.<br><br>Kampanjraden kan visas på olika platser i förhållande till annonsen (t.ex. nedanför annonsen) beroende på var annonsen visas på sidan. |
| Visa URL | Den URL som ingår i annonsen.<br><br>För expanderade dynamiska sökannonser genererar annonsnätverket det här värdet dynamiskt från webbplatsens domän, och du behöver inte ange något värde.<br><br>För expanderade textannonser och responsiva sökannonser behöver du inte ange något värde. Visnings-URL:en extraheras automatiskt från domänen i den slutliga URL:en. Du kan också anpassa URL-adressen med hjälp av fälten Sökväg 1 och Sökväg 2.<br><br><b>Anteckningar:</b><ul><li>(Konton med slutliga URL:er) Domännamnen i den URL som visas och den slutliga URL:en måste matcha.</li><li>[!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li></ul> |
| Visningsbana 1 | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) Text som läggs till i URL:en som automatiskt extraheras från den slutliga URL:en. Varje sökväg föregås av ett snedstreck (/) i URL:en. En bana får inte innehålla snedstreck (/) eller radmatningstecken (\n). Den maximala längden för varje bana är 15 tecken eller 7 dubbelbyte-tecken.<br><br>Om du vill infoga en annonsanpassare använder du följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`<br><br>Om t.ex. Bildskärmssökväg 1 är &quot;erbjudanden&quot; blir visnings-URL:en &lt;display url=&quot;&quot;>/deal, t.ex. www.example.com/deals.<br><br>[!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem. |
| Visningsbana 1 | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) En extra visningssökväg. se posten för Visningssökväg 1.<br><br>Exempel: Om Display Path 1 är &quot;offers&quot; och Display Path 2 är &quot;local&quot;, är display URL &lt;<i>visa URL</i>>/deal/local, t.ex. www.example.com/deals/local. |
| Startdatum | (Endast utökade sitelinks) Det första datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. Standardinställningen för nya utökade sitelinks är den aktuella dagen. <b>Obs!</b> Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks. |
| Slutdatum | Det sista datumet då platshållaren kan visas med annonser, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny platshållare är standardvärdet `[blank]` (dvs. inget slutdatum). |
| Utlysning | Anropet till åtgärd som ska ingå i annonsen. Se [API-referens för en lista över möjliga värden](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), men ange multiordsanrop för att fungera som flera ord (till exempel&quot;Bet Now&quot; i stället för&quot;BetNow&quot;) i kalkylblad. |
| Anrop till åtgärdsspråk | Språket för alternativen för att ringa upp till åtgärd. Se [API-referens för en lista över möjliga språk](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| Bas-URL/slutlig URL | Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas-/slutadresser på nyckelordsnivå åsidosätter de på annonsnivå och högre.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Mål-URL | (Ingår i genererade kalkylblad för informationsändamål. inte publicerad i sökmotorn) För konton med mål-URL:er är detta den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och handel. Om du genererade spårnings-URL:er baseras detta på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till sökmotorspecifika parametrar kan de ersättas med motsvarande parametrar för Sök, Socialt och Handel.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som kolumnen Bas-URL/Slutlig URL. |
| Anpassad URL-parameter | Data som ska ersätta `{custom_code}` dynamisk variabel när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL:en måste du överföra kalkylbladsfilen med alternativet Generera spårnings-URL:er. |
| Kreativ typ | Annonsformatet: <i>Ad för dynamisk sökning</i>, <i>Utökad textannons</i>, <i>Utökad dynamisk sökannons</i>, <i>Multimediaannons</i>, <i>Produktannons</i> (kundannonser), eller <i>Ad för responsiv sökning</i>, eller <i>Text ad</i>. Standardinställningen för nya annonser är <i>Text ad</i>. |
| Startdatum för annonsgrupp | Det första datum då anbud kan lämnas för annonskoncern, i annonserarens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet aktuellt datum. |
| Slutdatum för annonsgrupp | Det sista datum då anbud kan lämnas för annonskoncern, i annonserarens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet [blank] (dvs. inget slutdatum). |
| Spårningsmall | (Valfritt) Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet längst till granulerad) åsidosätter värdena på alla högre nivåer.<br><br>För konverteringsspårning för annonsering i Adobe, som används när kampanjinställningarna innehåller &quot;EF Redirect&quot; och &quot;Auto Upload&quot;, lägger Search, Social och Commerce automatiskt till omdirigerings- och spårningskod när du sparar posten.<br><br>Ange ett värde för omdirigeringar och spårning från tredje part.<br><br>En lista med parametrar som anger slutliga URL:er i spårningsmallar finns i [!DNL Microsoft Advertising] dokumentation.<br><br> Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Landningssidesuffix | Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Exempel: `param2=value1&param3=value2`<br><br>Se &quot;[Klickningsspårningsformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Microsoft Advertising] redigerare. |
| Nätverksstatus för sökning | Om annonser ska placeras för annonsgruppen på olika element i söknätverket:<ul><li><i>Alla:</i> Om du vill placera annonser i alla Bing-söknätverk och syndikerade sökpartners.</li><li><i>OwnedAndOperatedOnly:</i>Lägg bara in annonser på Bing och Yahoo! webbplatser.</li><li><i>SyndicatedSearchOnly:</i> Lägg bara in annonser på Bing och Yahoo! syndikerade sökpartners.</li><li><i>Av:</i> Om du bara vill placera annonser i innehållsnätverket (inte i söknätverket).</li></ul> För nya annonsgrupper är standardvärdet På. |
| Nätverksstatus för innehåll | Föråldrat |
| Språk | Målspråket för annonser i annonsgruppen: Engelska, franska, finska, tyska, norska, spanska eller svenska. Standardinställningen för nya kampanjer är engelska.<br><br>Den här inställningen avgör i vilka länder och regioner annonsen kan visas. Se till att välja ett språk som är kompatibelt med kampanjens platsmål. |
| Budgettyp | Om budgeten är <i>Dagligen</i> (standard) eller <i>Månadsvis</i>.<br><br>Obs! Om du tilldelar kampanjen till en optimerad portfölj ställs det här värdet automatiskt in på Daily. |
| Enhet | En enhetstyp för vilken anbudsjusteringar görs på kampanj- eller annonsgruppsnivå: <i>smartphone</i>, <i>surfplatta</i>, eller <i>desktop</i>. |
| Anpassa via bud | Börsjusteringen för en angiven måltyp. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för smarttelefoner är 50 %, är smarttelefonanbudet 1,50 USD. Som standard bjuds alla mål på nyckelordsnivå. Giltiga procenttal kan vara:<ul><li>Smarttelefoner och surfplattor: -100 (budg inte för enhetstypen) och från -90 till 900</li><li>Skrivbord: från 0 till 900</li></ul> |
| Creative Preferred Devices | De enhetstyper som du föredrar att visa annonsen eller sitelink på: <i>Alla</i> (standard) eller <i>Mobil</i>. När Mobile anges försöker nätverket att visa annonsen eller platshållaren för användare av mobila enheter i stället för för dator- eller surfplatteanvändare. I annat fall visas annonsen eller platshållaren på alla enhetstyper i nätverket. <b>Obs!</b> Nätverket garanterar inte att annonsen visas på den önskade enhetstypen. |
| Param2 | Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller `{Param2}` dynamisk ersättningssträng. Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du vill använda den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Param3 | Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller `{Param3}` dynamisk ersättningssträng. Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du vill använda den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Länknamn | Sitelink-texten. Den måste vara unik i kampanjen. Om du anger Description1 och Description2 kan sitelink-texten innehålla upp till 25 enkelbyte- eller 12 dubbelbyte-tecken; I annat fall kan sitelänktexten innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>[!DNL Microsoft Advertising] kan visa två, fyra eller sex förbättrade sitelinks med beskrivningar, eller fyra eller sex sitelinks i en enda rad utan beskrivningar, med en annons.<br><br>Du kan bara skapa nya utökade sitelinks-länkar i kampanjer med utökade sitelinks-funktioner eller utan sitelinks-länkar. |
| Kampanjstatus | Visningsstatus för kampanjen: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga kampanjer). Standardinställningen för nya kampanjer är Aktiv. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet `Deleted`. |
| Annonsgruppsstatus | Annonsgruppens visningsstatus: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga annonsgrupper). Standardvärdet för nya annonsgrupper är Aktiv. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet `Deleted`. |
| Nyckelordsstatus | Visningsstatus för nyckelordet: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är Aktiv. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet `Deleted`. <b>Obs!</b> Om du skapar spårnings-URL:er för ett nyckelord med flera matchningstyper måste nyckelordsstatusen för varje matchningstyp vara densamma. |
| Placeringsstatus | Föråldrat |
| Annonsstatus | Annonsens visningsstatus: <i>Aktiv</i>, <i>Borttagen</i> (endast befintliga annonser), <i>Avvisad</i> (inte redigerbart), eller <i>Pausad</i>. Standardinställningen för nya annonser är Aktiv. Om du vill ta bort en aktiv eller pausad annons anger du värdet `Deleted`. |
| Målstatus | Status för ett dynamiskt sökmål: <i>Aktiv</i>, <i>Pausad</i>, eller <i>Borttagen</i> (endast befintliga mål). Standardvärdet för nya mål är Aktiv. Om du vill ta bort ett aktivt eller pausat mål anger du värdet `Deleted`. |
| Status för webbplatslänkar | Sitelänkens visningsstatus: <i>Aktiv</i> eller <i>Borttagen</i> (endast befintliga sitelinks). Standardvärdet för nya sitelinks är Aktiv. Om du vill ta bort en aktiv platslänkar anger du värdet `Deleted`. |
| Platsstatus | Status för platsmålet: <i>Aktiv</i> eller <i>Borttagen</i> (endast befintliga platser). Standardvärdet för nya platser är Aktiv. Om du vill ta bort en aktiv plats anger du värdet `Deleted`. |
| Produktgruppstatus | Produktgruppens visningsstatus: <i>Aktiv</i> eller <i>Borttagen</i> (endast befintliga produktgrupper). Standardvärdet för nya produktgrupper är Aktiv. Om du vill ta bort en aktiv produktgrupp anger du värdet `Deleted`. |
| Status för enhetsmål | Status för enhetsmålet på kampanj- eller annonsnivå: <i>Aktiv</i> eller <i>Borttagen</i>. För nya kampanjer och annonsgrupper är standardvärdet Aktiv. |
| RLSA-målstatus | Status för kampanj- eller annonsnivå-RLSA-målet eller (endast Google Ads)-undantaget: <i>Aktiv</i> eller <i>Borttagen</i> (endast befintliga mål). Standardvärdet för nya mål eller undantag är Aktiv. Om du vill ta bort ett aktivt mål eller undantag anger du värdet `Deleted`. |
| \[Advertiser-specific Label Classification\] | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden tillämpas på alla underordnade komponenter. nya komponenter som läggs till senare kopplas automatiskt till etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Varken klassificeringsnamnet eller klassificeringsvärdet är skiftlägeskänsligt. |
| Begränsningar | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><b>>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| Kampanj-ID | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| Annonsgrupp-ID | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| Placement-ID | Föråldrat |
| Nyckelords-ID | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| Annons-ID | <p>Det unika ID som identifierar en befintlig annons. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] För responsiva sökannonser krävs antingen annons-ID eller AMO-ID för att redigera eller ta bort annonsdata. För alla andra entitetstyper krävs AMO-ID bara när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsannonsen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna.</p><p><b>Obs!</b> Om du redigerar a) och egenskapskolumner förutom Status för en befintlig annons eller b) data för en responsiv sökannons, och du varken inkluderar ID:t eller ID:t för AMO, skapas en ny annons och den befintliga annonsen ändras inte. </p> |
| Platslänks-ID | Det unika ID som identifierar en befintlig platslänk. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitellänken eller b) ett AMO-ID.&quot; Om du däremot inte inkluderar något platslänks-ID eller AMO-ID, och egenskapskolumnerna matchar flera sitelinks, ändras statusen för endast en av sitelinks.</p><p><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du varken inkluderar Sitelink ID eller AMO ID, skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| Produktgrupp-ID | Det unika ID som identifierar en befintlig produktgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) ett AMO-ID. |
| Plats-ID | Unika [!DNL Microsoft Advertising] identifierare för platsmålet. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. Krävs endast när du ändrar eller tar bort platsmålet, såvida inte raden innehåller ett AMO-ID för målet. |
| Mål-ID | Det unika ID som identifierar ett befintligt automatiskt mål. Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller ett AMO-ID för målet. |
| Mål-ID för RLSA | Det unika ID som identifierar ett befintligt RLSA-mål på kampanj- eller annonsgruppsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet eller undantaget, såvida inte raden innehåller ett AMO-ID för målet. |
| AMO-ID | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar annons-ID:t. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| EF-felmeddelande | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden finns i EF-felfiler. Det här värdet är inte registrerat i annonsnätverket. |
| SE-felmeddelande | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden ingår i SE-felfiler. Det här värdet är inte registrerat i annonsnätverket. |
| Begäran om undantag | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa namn och text för alla Google reklampolicyer som en annons bryter mot. |
| Butikshash | (Ingår i informationssyfte i kalkylblad som genererats med Advanced Campaign Management) En alfanumerisk hash-kod (t.ex. f9639f40cdf56524b541e5dacf55a991) som anger att objektet genererades i vyn Avancerat (ACM). |

<table style="table-layout:auto">

[^1]: [!DNL Excel] konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

## Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent

### Kampanjfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| Kampanjbudget | Krävs för att skapa en kampanj. | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| Kanaltyp | Krävs för att skapa en kampanj. |
| Leveranssätt | Valfritt |
| Kampanjprioritet | Krävs för att skapa en shoppingkampanj. |
| Affärs-ID | Krävs för att skapa en shoppingkampanj. |
| Försäljningsland | Krävs för att skapa en shoppingkampanj. |
| Filter för produktomfång | (Shoppingkampanjer) Valfritt |
| DSA-domännamn | Krävs för att skapa en kampanj av typen a)&quot;DynamicSearchAds&quot; eller b)&quot;Search&quot; när elementet ExperimentId inte har angetts) |
| Domänspråk för DSA | Krävs för att skapa en kampanj av typen a)&quot;DynamicSearchAds&quot; eller b)&quot;Search&quot; när elementet ExperimentId inte har angetts) |
| Spårningsmall | Valfritt |
| Landningssidesuffix | <p>Valfritt |
| Budgettyp | Krävs för att skapa en kampanj. |
| Enhet | Valfritt |
| Anpassa via bud | Valfritt |
| Kampanjstatus | Krävs endast för att ta bort en kampanj. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Annonsgruppsfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Annonsgruppstyp | Krävs för att skapa en annonsgrupp. |
| Målmetod | Krävs endast för att skapa målgrupps- och annonsgrupper. |
| Startdatum för annonsgrupp | Valfritt |
| Slutdatum för annonsgrupp | Valfritt |
| Spårningsmall | Valfritt |
| Nätverksstatus för sökning | (Kampanjer endast i söknätverket) Valfritt |
| Språk | Valfritt |
| Enhet | Valfritt |
| Anpassa via bud | Valfritt |
| Annonsgruppsstatus | Krävs endast för att ta bort en annonsgrupp. |
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
| Nyckelord | Obligatoriskt |
| Matcha typ | Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper. |
| Max CPC | Valfritt |
| Bas-URL/slutlig URL | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Spårningsmall | Valfritt |
| Param1 | Valfritt |
| Param2 | Valfritt |
| Nyckelordsstatus | Krävs endast för att ta bort ett nyckelord. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Nyckelords-ID | Krävs endast när du redigerar eller tar bort nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökannonsfält

>[!NOTE]
>
>Det går inte att skapa support.

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Beskrivningsrad 1-2 | Krävs för att redigera beskrivningen. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| Visningsbana 1 | Krävs för att redigera fältet. |
| Visningsbana 2 | Krävs för att redigera fältet. |
| Kreativ typ | Krävs för att skapa eller redigera status för en produktannons. |
| Creative Preferred Devices | Valfritt |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Produktfält (shoppingfält)

Mer information om hur du skapar shoppingannonser finns i &quot;[Implementera [!DNL Microsoft Advertising] shoppingkampanjer](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Kampanjlinje | Valfritt |
| Bas-URL/slutlig URL | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Kreativ typ | Krävs för att skapa eller redigera status för en produktannons. |
| Spårningsmall | Valfritt |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) ett AMO-ID. Om du däremot varken inkluderar annons-ID eller AMO-ID och annonsegenskapskolumnerna matchar flera annonser, ändras status för endast en av annonserna. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Responsiva (multimedia) och fält

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Annonsrubrik, annonsrubrik 2-15 | För responsiva annonser krävs annonstitel, annonstitel 2 och annonstitel 3 för att skapa annonser, och alla andra annonstitelfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser). <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| Beskrivningsrad 1-4 | Description Line 1 and Description Line 2 are required to create ads, and Description Line 3 and Description Line 4 are optional. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| Företagsnamn | Krävs för att skapa eller ta bort en annons. |
| Utlysning | Krävs för att skapa en annons. |
| Anrop till åtgärdsspråk | Krävs för att skapa en annons. |
| Bas-URL/slutlig URL | Krävs för att skapa en annons. |
| Kreativ typ | Valfritt. |
| Spårningsmall | Valfritt |
| Annonsstatus | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
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
| Annonsrubrik, annonsrubrik 2-15 | För responsiva sökannonser krävs annonsrubrik, annonsrubrik 2 och annonsrubrik 3 för att skapa en annons, och alla andra annonstitelfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser). |
| Annonsrubrik 1-15 - position | Valfritt |
| Beskrivningsrad 1-4 | För responsiva sökannonser krävs Description Line 1 och Description Line 2 för att skapa en annons, och Description Line 3 och Description Line 4 är valfria. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| Beskrivningsrad 1-4 position | Valfritt |
| Visningsbana 1 | Valfritt |
| Visningsbana 2 | Valfritt |
| Bas-URL/slutlig URL | Krävs för att skapa en annons. |
| Anpassad URL-parameter | Valfritt |
| Kreativ typ | Valfritt |
| Spårningsmall | Valfritt |
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
>Utökade textannonser har tagits bort. Du kan bara ta bort befintliga textannonser.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Annonsrubrik, annonsrubrik 2-3 | Skrivskyddad |
| Beskrivningsrad 1-2 | Skrivskyddad |
| Visa URL | Skrivskyddad |
| Visningsbana 1 | Skrivskyddad |
| Visningsbana 2 | Skrivskyddad |
| Bas-URL/slutlig URL | Skrivskyddad |
| Anpassad URL-parameter | Skrivskyddad |
| Kreativ typ | Valfritt |
| Spårningsmall | Skrivskyddad |
| Creative Preferred Devices | Skrivskyddad |
| Annonsstatus | Obligatoriskt |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Annons-ID | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar annons-ID:t.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökmålfält (automatiskt mål)

>[!NOTE]
>
>Det går inte att skapa support.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Obligatoriskt |
| Automatiskt måluttryck | Obligatoriskt. |
| Matcha typ | Valfritt |
| Max CPC | Valfritt |
| Anpassad URL-parameter | Valfritt |
| Målstatus | Krävs för att ta bort ett mål |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
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
| Matcha typ | Krävs för att skapa en produktgrupp. |
| Max CPC | Krävs för att skapa en produktgrupp. |
| Överordnade produktgrupperingar | Obligatoriskt |
| Produktgruppering | Obligatoriskt |
| Partitionstyp | Krävs för att skapa en produktgrupp. |
| Bas-URL/slutlig URL | Obligatoriskt |
| Spårningsmall | Valfritt |
| Produktgruppstatus | Krävs endast för att ta bort en produktgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| Begränsningar | Valfritt |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt |
| Produktgrupp-ID | Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) ett AMO-ID. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Webblänksfält på kampanjnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Beskrivningsrad 1 | Valfritt |
| Beskrivningsrad 2 | Valfritt |
| Startdatum | Valfritt |
| Slutdatum | Valfritt |
| Bas-URL/slutlig URL | Obligatoriskt |
| Anpassad URL-parameter | Valfritt |
| Spårningsmall | Valfritt |
| Creative Preferred Devices | Valfritt |
| Länknamn | Obligatoriskt |
| Status för webbplatslänkar | Krävs endast för att ta bort en sitellänk. |
| Kampanj-ID | Valfritt |
| Platslänks-ID | Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitellänken eller b) ett AMO-ID.&quot; Om du däremot varken inkluderar Sitelinks-ID eller AMO-ID och egenskapskolumnerna matchar flera sitelinks, ändras statusen för endast en av sitelinks.<br><br><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du inte inkluderar vare sig Sitelink ID eller AMO ID, skapas en ny sitelink och den befintliga sitelink ändras inte. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för plats

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Plats | Obligatoriskt |
| Platstyp | Krävs för att skapa ett mål |
| Anpassa via bud | Valfritt |
| Platsstatus | Krävs endast för att ta bort ett platsmål. |
| Kampanj-ID | Valfritt |
| AMO-ID | Krävs för att redigera eller ta bort data om du inte inkluderar kampanj-ID:t.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält på kampanjnivå och annonsgruppsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Enhet | Krävs för att ta bort ett enhetsmål. |
| Anpassa via bud | Valfritt |
| Namn på annonsgrupp | Krävs för enhetsmål på annonsnivå. Gäller inte för enhetsmål på kampanjnivå. |
| Status för enhetsmål | Krävs endast för att ta bort ett enhetsmål. |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt endast för enhetsmål på annonsnivå. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhetens mål-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för RLSA på kampanjnivå och annonsgruppsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| Kontonamn | Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| Kampanjnamn | Obligatoriskt |
| Namn på annonsgrupp | Krävs för annonsnivåmål. Gäller inte för kampanjnivåmål. |
| Målgrupp | Krävs för att skapa ett nytt mål. |
| Måltyp | Valfritt |
| Anpassa via bud | Valfritt |
| RLSA-målstatus | Krävs för att ta bort ett mål. |
| Kampanj-ID | Valfritt |
| Annonsgrupp-ID | Valfritt Gäller endast för annonsnivåmål. |
| Mål-ID för RLSA | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller ett AMO-ID för målet. |
| AMO-ID | Krävs för att redigera eller ta bort data såvida du inte inkluderar mål-ID:t för RLSA.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

>[!MORELIKETHIS]
>
>* [Bilaga - Fallkalkylbladsfel](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Filformat för kalkylblad som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickningsspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överföra en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
