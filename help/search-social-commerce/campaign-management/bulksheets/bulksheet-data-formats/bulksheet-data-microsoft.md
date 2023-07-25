---
title: Obligatoriska kalkylbladsdata för [!DNL Microsoft Advertising] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för [!DNL Microsoft Advertising] konton.
exl-id: a3090962-49df-46b0-89f8-98b633c3ea7a
source-git-commit: e4901c1ac6e73f27886e315136c3fe9b865cdd48
workflow-type: tm+mt
source-wordcount: '6721'
ht-degree: 1%

---

# Bilaga - Obligatoriska data för kalkylblad för [!DNL Microsoft Advertising] konton

Skapa och uppdatera [!DNL Microsoft Advertising] kampanjdata i grupp kan du använda bulkbladsfiler för sökning, sociala medier och handel som är särskilt formaterade för [!DNL Microsoft Advertising] konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det önskade filformatet eller b) skapa dem manuellt (se &quot;[Filformat för bulkblad som stöds](bulksheet-file-formats.md)&quot; för allmän information om vilka filformat som stöds).

Varje blad måste innehålla rubrikfält och motsvarande datafält som krävs för [specifika åtgärder som du vill utföra](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (som att skapa en annons). När ett fält inte är obligatoriskt kan du utesluta det från rubriken och dataraderna. Alla anpassade kolumner tas bort när du överför bulkbladsfilen.

Nedan följer en tabell över alla tillgängliga datafält och ytterligare tabeller som anger vilka fält som krävs för att lägga till, redigera eller ta bort data för enskilda enheter (till exempel kampanjer och nyckelord).

## Alla tillgängliga datafält

I följande tabell visas alla tillgängliga datafält.

Information om de datafält som är relevanta för kontoentiteter finns i &quot;[Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent](#bulksheet-fields-per-component-microsoft).

| Fält | Beskrivning |
|----|----|
| [!UICONTROL Platform] | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Acct Name] | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Det unika namn som identifierar en kampanj för ett konto. Maximala längden är 128 tecken. |
| [!UICONTROL Campaign Budget] | Den dagliga eller månadsvisa kampanjbudgeten, med eller utan monetära symboler och interpunktion. Den får inte vara mindre än 0,05. |
| [!UICONTROL Channel Type] | Den typ av kanal som kampanjen har som mål: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i>, eller <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Endast kampanjer med daglig budget) Så här snabbt kan du visa annonser för kampanjen varje dag:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (standard för nya kampanjer): För att sprida annonsintrycket över hela dagen.</li><li><i>[!UICONTROL Accelerated]:</i> Visa era annonser så ofta som möjligt tills budgeten är nådd. Därför kanske era annonser inte visas senare under dagen.</li></ul> |
| [!UICONTROL Campaign Priority] | (Endast köpkampanjer) Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt: <i>[!UICONTROL Low]</i> (standard för nya kampanjer), <i>[!UICONTROL Medium]</i>, eller <i>[!UICONTROL High]</i>.<br><br>När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad. |
| [!UICONTROL Merchant ID] | (Kundkampanjer och målgruppskampanjer som endast är kopplade till en handlarfeed) Kund-ID för det handlarkonto vars produkter används för kampanjen. |
| [!UICONTROL Sales Country] | (Endast köpkampanjer. skrivskyddad för befintliga kampanjer) Det land där kampanjprodukterna säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen. |
| [!UICONTROL Product Scope Filter] | (Kampanjer som endast använder shoppingnätverket) De produkter på ert handelskonto för vilka produktannonser kan skapas för kampanjen. Du kan ange upp till sju produktdimensioner och attributkombinationer där du kan filtrera dina produkter med formatet dimension=attribut. Avgränsa flera filter med avgränsaren &quot;>>&quot;. En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanjer](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Exempel: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Om du vill ta bort de befintliga värdena använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL DSA Domain Name] | (Kampanjer av typ a)<i>[!UICONTROL DynamicSearchAds]</i>&quot; eller b) &quot;<i>[!UICONTROL Search]</i>&quot; när [!DNL ExperimentId] -element har inte angetts) Webbplatsens domännamn för dynamiska sökannonser. Maxlängden är 2 048 tecken. Om domännamnet innehåller `www`, trimmas och används inte.<br><br>För befintliga kampanjer kan du inte redigera domänen, men du måste inkludera den för att kunna uppdatera andra egenskaper. |
| [!UICONTROL DSA Domain Language] | (Kampanjer av typ a)<i>[!UICONTROL DynamicSearchAds]</i>&quot; eller b) &quot;<i>[!UICONTROL Search]</i>&quot; när [!DNL ExperimentId] -elementet är inte inställt) Webbplatssidornas språk för dynamiska sökannonser. De domänspråk som stöds är [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish]och [!UICONTROL Swedish].<br><br>För befintliga kampanjer kan du inte redigera språket, men du måste inkludera det för att kunna uppdatera andra egenskaper. |
| [!UICONTROL Ad Group Name] | Det unika namn som identifierar en annonsgrupp. Maximala längden är 128 tecken. Efterföljande tomma tecken sparas inte (till exempel sparas&quot;Annonsgrupp 1&quot; som&quot;Annonsgrupp 1&quot;). |
| [!UICONTROL Ad Group Type] | (Kampanjer i söknätverket). skrivskyddad för befintliga annonsgrupper) Annonsgruppstypen: <i>[!UICONTROL Audience]</i> (endast för målgruppskampanjer), <i>[!UICONTROL Search Dynamic]</i> (endast för dynamiska sökannonser) och <i>[!UICONTROL Search Standard]</i> (endast för responsiva sökannonser och befintliga expanderade textannonser). Vissa kampanjtyper kan innehålla flera typer av annonsgrupper. |
| [!UICONTROL Keyword] | (Endast kampanjer i söknätverket) Nyckelordssträngen. Maximala längden är 50 tecken.<br><br><b>Anteckningar:</b><ul><li>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du [!UICONTROL Match Type] till `Negative`. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas nyckelordet för hela kampanjen.</li><li>Ändra en [!DNL Microsoft Advertising] nyckelordet tar bort det befintliga nyckelordet och skapar ett nytt med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.</li></ul> |
| Placement | Föråldrat |
| [!UICONTROL Audience] | Återmarknadsföringslistan för sökannonser (RLSA) som riktar sig till målgruppen för kampanjen eller annonsgruppen. |
| [!UICONTROL Target Type] | (Endast RLSA-mål) Måltypen: <i>[!UICONTROL Inclusion]</i> eller <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamiska sökmål för annonsgruppen. Använd &quot;[!UICONTROL All Web Pages].&quot;<br><br>Om du vill ange upp till tre dynamiska sökvillkor använder du formatet `<category>=<target>`, där &lt;category> kan innehålla någon av kategorierna nedan. Koppla flera mål för en enskild kategori med`[blank space] and [blank space]`&quot; och koppla ihop flera kategorier med &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Kategori:</i> Så här visar du dynamiska sökannonser för indexerade sidor med en viss innehållskategori i Google.</li><li><i>URL:</i> Om du vill visa dynamiska sökannonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.</li><li><i>Sidrubrik:</i> Om du vill visa dynamiska sökannonser för indexerade sidor med specifik text i sidtiteln.</li><li><i>Sidinnehåll:</i> Så här visar du dynamiska sökannonser för indexerade sidor med specifikt innehåll.</li></ul>Exempel: url=skor.example.com och page title=skos<br>Exempel: Alla webbsidor |
| [!UICONTROL Location] | En geografisk plats där annonser för kampanjen eller annonsgruppen ska placeras. värdena inte är skiftlägeskänsliga. Om du inte anger några värden för kampanjen eller annonsgruppen anges alla platser som mål. Om du vill ange särskilda målplatser anger du platsen med [!DNL Microsoft Advertising] platskodformat. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. <b>Obs!</b> Om du vill utesluta en plats skriver du ett minustecken före platskoden (`-`), till exempel `-United States`. |
| [!UICONTROL Location Type] | Platstypen, till exempel Ort, Land, MetroArea, Postnummer och Delstat. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. |
| [!UICONTROL Match Type] | (Endast kampanjer i söknätverket) Nyckelordsmatchningsalternativ. Detta kan inkludera nyckelordsmatchningsalternativet för ett dynamiskt sökmål eller en produktgrupp. Värdena är: <i>[!UICONTROL Broad]</i> (standard för nya nyckelord), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (anges automatiskt för nyckelord när annonsgruppen har innehållsnätverket som mål), <i>[!UICONTROL Negative]</i> (för att utesluta ett nyckelord i innehållsnätverket), <i>[!UICONTROL Dynamic Ad Target]</i> (standard för nya dynamiska sökmål), <i>[!UICONTROL Product Group]</i> (standard för nya produktgrupper), eller <i>[!UICONTROL Negative Product Group]</i> (för att exkludera en produktgrupp).  Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper.<br><br>För Bred Match Modifier väljer du &quot;Broad&quot; och infogar en `+` före ett ord i nyckelordet som krävs (till exempel &quot;`+red +shoes`&quot; att kräva både&quot;röd&quot; och&quot;skor&quot;).<br><br>Ändra matchningstyp för en [!DNL Microsoft Advertising] nyckelordet tas inte bort. |
| [!UICONTROL Max CPC] | (Kampanjer i söknätverket) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för en annons baserat på nyckelordet, produktgruppen eller det dynamiska sökmålet, med eller utan monetära symboler och interpunktion.  För befintliga nyckelords- och produktgruppsposter i optimerade portföljer gäller uppdateringarna endast en dag och skrivs över under nästa optimeringscykel. <b>Obs!</b> Du kan inte ange anbud för negativa nyckelord. |
| [!UICONTROL Max Content CPC] | (Endast skrivskyddat för CPC-kampanjer som skapats innan innehållsnätverket togs bort 2017) Den maximala innehållskostnaden per klick (CPC), som är den högsta summan att betala för ett reklamklick från en webbplats i visningsnätverk, med eller utan monetära symboler och interpunktion. |
| [!UICONTROL Audience Target Method] | (Målgrupper och grupper) Om:<ul><li><i>[!UICONTROL Target and Bid]:</i> Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.</li><li><i>[!UICONTROL Bid Only]:</i>Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå.</li></ul> Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper. |
| [!UICONTROL Parent Product Groupings] | Hierarkin för överordnade produktgrupper.<br><br>Exempel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Produktgruppen (till exempel&quot;brand=acme&quot; eller&quot;Alla produkter&quot;).<br><br><b>Anteckningar:</b><ul><li>När en angiven produktgrupp inte finns i hierarkin för överordnade produktgrupper skapas de delar av hierarkin som behövs av sökningen, den sociala tjänsten och handeln.</li><li>Sökning, sociala medier och handel skapar automatiskt en[!UICONTROL All Products]&quot; när du skapar en annonsgrupp i en shoppingkampanj med ett standardbud satt till annonsgruppens standardbud. Sökning, sociala medier och handel skapar automatiskt en[!UICONTROL Everything Else]&quot; grupp med annonsgruppens standardbud på varje nivå i produktgruppshierarkin. Du kan fortfarande skapa dessa standardgrupper explicit och antingen exkludera dem eller ändra deras bud.</li><li>Varje annonsgrupp kan innehålla upp till åtta nivåer av produktgrupper, inklusive[!UICONTROL All Products]&quot; och sju andra nivåer.</li></ul> |
| [!UICONTROL Partition Type] | Partitionstypen för produktgruppen: <i>[!UICONTROL subdivision]</i> (när den har underordnade produktgrupper) eller <i>[!UICONTROL unit]</i> (när den inte har några underordnade produktgrupper). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Endast expanderade textannonser, multimediaannonser, responsiva annonser och responsiva sökannonser) Rubrikerna i en annons. Den maximala längden för varje annonstitelfält är 30 eller 15 dubbelbytetecken, inklusive all dynamisk text (t.ex. värdena för nyckelord, `{Param2}` och `{Param3}` dynamiska ersättningsvariabler och annonsanpassare).<br><br> För responsiva sökannonser infogar du en annonsanpassare med följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För expanderade textannonser krävs annonsrubrik och annonsrubrik 2. [!UICONTROL Ad Title 3] är valfritt. [!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]och [!UICONTROL Ad Title 3] är obligatoriska och alla andra annonsrubrikfält är valfria.<br><br>Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser).<br><br>För alla annonstyper utom för expanderade textannonser tas den befintliga annonsen bort om du ändrar annonsen och skapar en ny annons med samma egenskaper. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Endast responsiva sökannonser.) (valfritt) En position där motsvarande annonsrubrik ska fästas: `[null]` (inget värde, vilket gör att annonsrubriken kan användas för alla positioner), 1, 2 eller 3. Om [!UICONTROL Ad Title Position] har värdet 1, sedan [!UICONTROL Ad Title] visas bara i position 1. Som standard är alla annonsrubriker null (saknar värden). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Obs!</b> Du kan fästa flera annonsrubriker på samma plats. Annonsnätverket kommer att använda en av de annonstitlar som är fästa vid positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Endast textannonser, dynamiska sökannonser, multimediaannonser, responsiva sökannonser och förbättrade sitelinks på kampanjnivå) Innehållet i en annons eller en sitelink.<br><br>För sitelinks kan du använda båda [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] om du vill inkludera extra text som annonsnätverket kan visa under länktexten. Varje beskrivningsfält kan innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>För annonser är den maximala längden för varje beskrivningsfält 90 eller 45 dubbelbyte-tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).<br><br>För responsiva sökannonser infogar du en annonsanpassare med följande format, där Standardtext är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För textannonser och dynamiska sökannonser krävs Description Line 1 och [!UICONTROL Description Line 2] är valfritt.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser, [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] krävs, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Anteckningar:</b><ul><li>(Standardtextannonser) Den kombinerade titeln och texten måste vara minst tre ord.</li><li>(Utökade textannonser) Det här fältet kan även innehålla {Param2} och {Param3} dynamiska ersättningsvariabler. I så fall är annonstextens maximala längd 300 enkelbyte- eller 150 dubbelbyte-tecken. [!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li><li>(Dynamiska sökannonser) Dynamisk ersättningstext tillåts inte.</li><li>För alla annonstyper utom expanderade textannonser tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Endast responsiva sökannonser.) (valfritt) En position där motsvarande beskrivning ska fästas: `[null]` (inget värde, vilket gör att beskrivningen kan användas för alla positioner), 1, 2 eller 3. Om [!UICONTROL Description 1 Position] har värdet 1, så visas bara beskrivning 1 i position 1. Som standard är inga beskrivningar fästa vid en position.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser).<br><br><b>Obs!</b> Du kan fästa flera beskrivningar på samma plats. Annonsnätverket använder en av beskrivningarna som är fästa vid positionen. Beskrivningar som fästs vid position 2 kanske inte visas med annonsen. |
| [!UICONTROL Business Name] | (Endast multimediaannonser) Företagsnamnet, med högst 25 tecken. |
| [!UICONTROL Promotion Line] | (Endast produktlistade annonser) En unik kampanjrad som ska inkluderas i produktlistan i sökresultaten (till exempel&quot;Fraktfritt nu!). Maxlängden är 45 tecken.<br><br>Kampanjraden kan visas på olika platser i förhållande till annonsen (t.ex. nedanför annonsen) beroende på var annonsen visas på sidan. |
| [!UICONTROL Display URL] | Den URL som ingår i annonsen.<br><br>För expanderade dynamiska sökannonser genererar annonsnätverket det här värdet dynamiskt från webbplatsens domän, och du behöver inte ange något värde.<br><br>För expanderade textannonser och responsiva sökannonser behöver du inte ange något värde. Visnings-URL:en extraheras automatiskt från domänen i den slutliga URL:en. Du kan också anpassa URL-adressen med hjälp av fälten Sökväg 1 och Sökväg 2.<br><br><b>Anteckningar:</b><ul><li>(Konton med slutliga URL:er) Domännamnen i den URL som visas och den slutliga URL:en måste matcha.</li><li>[!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li></ul> |
| [!UICONTROL Display Path 1] | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) Text som läggs till i URL:en som automatiskt extraheras från den slutliga URL:en. Varje sökväg föregås av ett snedstreck (/) i URL:en. En bana får inte innehålla snedstreck (/) eller radmatningstecken (\n). Den maximala längden för varje bana är 15 tecken eller 7 dubbelbyte-tecken.<br><br>Om du vill infoga en annonsanpassare använder du följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`<br><br>Om [!UICONTROL Display Path 1] är&quot;erbjudanden&quot;, blir URL:en för displayen &lt;display url=&quot;&quot;>/deal, t.ex. www.example.com/deals.<br><br>[!DNL Microsoft Advertising] borttagna utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem. |
| [!UICONTROL Display Path 1] | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) En extra visningssökväg. se posten för [!UICONTROL Display Path 1].<br><br>Exempel: If [!UICONTROL Display Path 1] är&quot;erbjudanden&quot; och [!UICONTROL Display Path 2] är &quot;local&quot;, blir URL:en för visning &lt;<i>visa URL</i>>/deal/local, t.ex. www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Endast utökade sitelinks) Det första datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. Standardinställningen för nya utökade sitelinks är den aktuella dagen. <b>Obs!</b> Nya utökade sitelinks kan endast skapas i kampanjer med utökade sitelinks eller utan sitelinks. |
| [!UICONTROL End Date] | Det sista datumet då platshållaren kan visas med annonser, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny platshållare är standardvärdet `[blank]` (dvs. inget slutdatum). |
| [!UICONTROL Call To Action] | Anropet till åtgärd som ska ingå i annonsen. Se [API-referens för en lista över möjliga värden](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), men ange multiordsanrop för att fungera som flera ord (till exempel&quot;Bet Now&quot; i stället för&quot;BetNow&quot;) i kalkylblad. |
| [!UICONTROL Call To Action Language] | Språket för alternativen för att ringa upp till åtgärd. Se [API-referens för en lista över möjliga språk](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas-/slutadresser på nyckelordsnivå åsidosätter de på annonsnivå och högre.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Destination URL] | (Ingår i genererade kalkylblad för informationsändamål. inte publicerad i sökmotorn) För konton med mål-URL:er är detta den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och handel. Om du genererade spårnings-URL:er baseras detta på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till sökmotorspecifika parametrar kan de ersättas med motsvarande parametrar för Sök, Socialt och Handel.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som kolumnen Bas-URL/Slutlig URL. |
| [!UICONTROL Custom URL Param] | Data som ska ersätta `{custom_code}` dynamisk variabel när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL:en måste du överföra kalkylbladsfilen med alternativet Generera spårnings-URL:er. |
| [!UICONTROL Creative Type] | Annonsformatet: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (kundannonser), eller <i>[!UICONTROL Responsive Search Ad]</i>, eller <i>[!UICONTROL Text ad]</i>. Standardinställningen för nya annonser är <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Det första datum då anbud kan lämnas för annonskoncern, i annonserarens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet aktuellt datum. |
| [!UICONTROL Ad Group End Date] | Det sista datum då anbud kan lämnas för annonskoncern, i annonserarens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet [blank] (dvs. inget slutdatum). |
| [!UICONTROL Tracking Template] | (Valfritt) Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet längst till granulerad) åsidosätter värdena på alla högre nivåer.<br><br>För konverteringsspårning för annonsering i Adobe, som används när kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]&quot; och &quot;[!UICONTROL Auto Upload],&quot; Sök, Socialt och e-handel lägger automatiskt till omdirigerings- och spårningskod när du sparar posten.<br><br>Ange ett värde för omdirigeringar och spårning från tredje part.<br><br>En lista med parametrar som anger slutliga URL:er i spårningsmallar finns i [!DNL Microsoft Advertising] dokumentation.<br><br> Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Landing Page Suffix] | Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Exempel: `param2=value1&param3=value2`<br><br>Se &quot;[Klickningsspårningsformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Microsoft Advertising] redigerare. |
| Nätverksstatus för sökning | Om annonser ska placeras för annonsgruppen på olika element i söknätverket:<ul><li><i>Alla:</i> Om du vill placera annonser i alla Bing-söknätverk och syndikerade sökpartners.</li><li><i>OwnedAndOperatedOnly:</i>Lägg bara in annonser på Bing och Yahoo! webbplatser.</li><li><i>SyndicatedSearchOnly:</i> Lägg bara in annonser på Bing och Yahoo! syndikerade sökpartners.</li><li><i>Av:</i> Om du bara vill placera annonser i innehållsnätverket (inte i söknätverket).</li></ul> För nya annonsgrupper är standardvärdet På. |
| [!UICONTROL Content Network Status] | Föråldrat |
| [!UICONTROL Languages] | Målspråket för annonser i annonsgruppen: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish], eller [!UICONTROL Swedish]. Standardinställningen för nya kampanjer är [!UICONTROL English].<br><br>Den här inställningen avgör i vilka länder och regioner annonsen kan visas. Se till att välja ett språk som är kompatibelt med kampanjens platsmål. |
| [!UICONTROL Budget Type] | Om budgeten är <i>[!UICONTROL Daily]</i> (standard) eller <i>[!UICONTROL Monthly]</i>.<br><br>Obs! Om du tilldelar kampanjen till en optimerad portfölj ställs värdet automatiskt in på [!UICONTROL Daily]. |
| [!UICONTROL Device] | En enhetstyp för vilken anbudsjusteringar görs på kampanj- eller annonsgruppsnivå: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>, eller <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Börsjusteringen för en angiven måltyp. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för smarttelefoner är 50 %, är smarttelefonanbudet 1,50 USD. Som standard bjuds alla mål på nyckelordsnivå. Giltiga procenttal kan vara:<ul><li>Smarttelefoner och surfplattor: -100 (budg inte för enhetstypen) och från -90 till 900</li><li>Skrivbord: från 0 till 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | De enhetstyper som du föredrar att visa annonsen eller sitelink på: <i>[!UICONTROL All]</i> (standard) eller <i>[!UICONTROL Mobile]</i>. När Mobile anges försöker nätverket att visa annonsen eller platshållaren för användare av mobila enheter i stället för för dator- eller surfplatteanvändare. I annat fall visas annonsen eller platshållaren på alla enhetstyper i nätverket. <b>Obs!</b> Nätverket garanterar inte att annonsen visas på den önskade enhetstypen. |
| [!UICONTROL Param2] | Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller `{Param2}` dynamisk ersättningssträng. Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du vill använda den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Param3] | Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller `{Param3}` dynamisk ersättningssträng. Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du vill använda den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Link Name] | Sitelink-texten. Den måste vara unik i kampanjen. Om du anger Description1 och Description2 kan sitelink-texten innehålla upp till 25 enkelbyte- eller 12 dubbelbyte-tecken; I annat fall kan sitelänktexten innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>[!DNL Microsoft Advertising] kan visa två, fyra eller sex förbättrade sitelinks med beskrivningar, eller fyra eller sex sitelinks i en enda rad utan beskrivningar, med en annons.<br><br>Du kan bara skapa nya utökade sitelinks-länkar i kampanjer med utökade sitelinks-funktioner eller utan sitelinks-länkar. |
| [!UICONTROL Campaign Status] | Visningsstatus för kampanjen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga kampanjer). Standardinställningen för nya kampanjer är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet `Deleted`. |
| [!UICONTROL Ad Group Status] | Annonsgruppens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonsgrupper). Standardinställningen för nya annonsgrupper är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet `Deleted`. |
| [!UICONTROL Keyword Status] | Visningsstatus för nyckelordet: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är [!UICONTROL Active]. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet `Deleted`. <b>Obs!</b> Om du skapar spårnings-URL:er för ett nyckelord med flera matchningstyper måste nyckelordsstatusen för varje matchningstyp vara densamma. |
| [!UICONTROL Placement Status] | Föråldrat |
| [!UICONTROL Ad Status] | Annonsens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (endast befintliga annonser), <i>[!UICONTROL Disapproved]</i> (inte redigerbart), eller <i>[!UICONTROL Paused]</i>. Standardinställningen för nya annonser är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annons anger du värdet `Deleted`. |
| [!UICONTROL Target Status] | Status för ett dynamiskt sökmål: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga mål). Standardinställningen för nya mål är [!UICONTROL Active]. Om du vill ta bort ett aktivt eller pausat mål anger du värdet `Deleted`. |
| [!UICONTROL Sitelink Status] | Sitelänkens visningsstatus: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga sitelinks). Standardinställningen för nya sitelinks är [!UICONTROL Active]. Om du vill ta bort en aktiv platslänkar anger du värdet `Deleted`. |
| [!UICONTROL Location Status] | Status för platsmålet: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga platser). Standardinställningen för nya platser är [!UICONTROL Active]. Om du vill ta bort en aktiv plats anger du värdet `Deleted`. |
| [!UICONTROL Product Group Status] | Produktgruppens visningsstatus: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga produktgrupper). Standardvärdet för nya produktgrupper är [!UICONTROL Active]. Om du vill ta bort en aktiv produktgrupp anger du värdet `Deleted`. |
| [!UICONTROL Device Target Status] | Status för enhetsmålet på kampanj- eller annonsnivå: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i>. För nya kampanjer och annonsgrupper är standardvärdet [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Status för kampanj- eller annonsnivå-RLSA-målet eller (endast Google Ads)-undantaget: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga mål). Standardinställningen för nya mål eller undantag är [!UICONTROL Active]. Om du vill ta bort ett aktivt mål eller undantag anger du värdet `Deleted`. |
| \[Advertiser-specific Label Classification\] | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden tillämpas på alla underordnade komponenter. nya komponenter som läggs till senare kopplas automatiskt till etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Varken klassificeringsnamnet eller klassificeringsvärdet är skiftlägeskänsligt. |
| [!UICONTROL Constraints] | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><b>>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL Campaign ID] | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett[!UICONTROL AMO ID]&quot; för kampanjen. |
| [!UICONTROL Ad Group ID] | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett[!UICONTROL AMO ID]&quot; för annonsgruppen. |
| [!UICONTROL Placement ID] | Föråldrat |
| [!UICONTROL Keyword ID] | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>Det unika ID som identifierar en befintlig annons. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] För responsiva sökannonser krävs antingen annons-ID eller AMO-ID för att redigera eller ta bort annonsdata. För alla andra entitetstyper krävs AMO-ID bara när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsadressen eller b) och &quot;[!UICONTROL AMO ID]&quot;.&quot; Om du däremot inte inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], och annonsegenskapskolumnerna matchar flera annonser, så ändras status för endast en av annonserna.</p><p><b>Obs!</b> Om du redigerar a) och egenskapskolumner förutom Status för en befintlig annons eller b) data för en responsiv sökannons, och du inkluderar varken [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], skapas en ny annons och den befintliga annonsen ändras inte. </p> |
| [!UICONTROL Sitelink ID] | Det unika ID som identifierar en befintlig platslänk. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort platslänken, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera platslänken eller b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; Om du inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], och egenskapskolumnerna matchar flera sitelinks, ändras bara statusen för en av sitelinks.</p><p><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink och du inte inkluderar någon av [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL Product Group ID] | Det unika ID som identifierar en befintlig produktgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| Plats-ID | Unika [!DNL Microsoft Advertising] identifierare för platsmålet. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising] utvecklarportal med [!DNL Microsoft Advertising] autentiseringsuppgifter för annonskonto. Krävs endast när du ändrar eller tar bort platsmålet, såvida inte raden innehåller ett[!UICONTROL AMO ID]&quot; för målet. |
| [!UICONTROL Target ID] | Det unika ID som identifierar ett befintligt automatiskt mål. Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller ett &quot;[!UICONTROL AMO ID]&quot; för målet. |
| [!UICONTROL RLSA Target ID] | Det unika ID som identifierar ett befintligt RLSA-mål på kampanj- eller annonsgruppsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet eller undantaget, såvida inte raden innehåller ett &quot;[!UICONTROL AMO ID]&quot; för målet. |
| [!UICONTROL AMO ID] | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar annons-ID:t. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| [!UICONTROL EF Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden finns i [!UICONTROL EF Errors] filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL SE Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket avseende data på raden. felmeddelanden finns i [!UICONTROL SE Errors] filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL Exemption Request] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa namn och text för alla Google reklampolicyer som en annons bryter mot. |
| [!UICONTROL Retail Hash] | (Ingår i informationssyfte i kalkylblad som genererats med Advanced Campaign Management) En alfanumerisk hash-kod (t.ex. f9639f40cdf56524b541e5dacf55a991) som anger att objektet genererades i vyn Avancerat (ACM). |

<table style="table-layout:auto">

[^1]: [!DNL Excel] konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

## Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent {#bulksheet-fields-per-component-microsoft}

>[!NOTE]
>
>När ett fält inte kan användas för en åtgärd, ignoreras alla värden som anges i fältet.

### Kampanjfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Campaign Budget] | Krävs för att skapa en kampanj. | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| [!UICONTROL Channel Type] | Krävs för att skapa en kampanj. |
| [!UICONTROL Delivery Method] | Valfritt |
| [!UICONTROL Campaign Priority] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Merchant ID] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Sales Country] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Product Scope Filter] | (Shoppingkampanjer) Valfritt |
| [!UICONTROL DSA Domain Name] | Krävs för att skapa en kampanj av typen a) &quot;[!UICONTROL DynamicSearchAds]&quot; eller b) &quot;[!UICONTROL Search]&quot; när [!DNL ExperimentId] -element har inte angetts) |
| [!UICONTROL DSA Domain Language] | Krävs för att skapa en kampanj av typen a) &quot;[!UICONTROL DynamicSearchAds]&quot; eller b) &quot;[!UICONTROL Search]&quot; när [!DNL ExperimentId] -element har inte angetts) |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Landing Page Suffix] | <p>Valfritt |
| [!UICONTROL Budget Type] | Krävs för att skapa en kampanj. |
| [!UICONTROL Device] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Campaign Status] | Krävs endast för att ta bort en kampanj. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett[!UICONTROL AMO ID]&quot; för kampanjen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Annonsgruppsfält

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Group Type] | Krävs för att skapa en annonsgrupp. |
| [!UICONTROL Audience Target Method] | Krävs endast för att skapa målgrupps- och annonsgrupper. |
| [!UICONTROL Ad Group Start Date] | Valfritt |
| [!UICONTROL Ad Group End Date] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Search Network Status] | (Kampanjer endast i söknätverket) Valfritt |
| [!UICONTROL Languages] | Valfritt |
| [!UICONTROL Device] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Ad Group Status] | Krävs endast för att ta bort en annonsgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Ad Group ID] | Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller ett[!UICONTROL AMO ID]&quot; för annonsgruppen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Nyckelordsfält

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Keyword] | Obligatoriskt |
| [!UICONTROL Match Type] | Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper. |
| [!UICONTROL Max CPC] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Param1] | Valfritt |
| [!UICONTROL Param2] | Valfritt |
| [!UICONTROL Keyword Status] | Krävs endast för att ta bort ett nyckelord. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Keyword ID] | Krävs endast när du redigerar eller tar bort nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) en &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökannonsfält

>[!NOTE]
>
>Det går inte att skapa support.

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Krävs för att redigera beskrivningen. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| [!UICONTROL Display Path 1] | Krävs för att redigera fältet. |
| [!UICONTROL Display Path 2] | Krävs för att redigera fältet. |
| [!UICONTROL Creative Type] | Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Creative Preferred Devices] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annons eller b) en &quot;[!UICONTROL AMO ID].&quot; Om du däremot inte inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], och annonsegenskapskolumnerna matchar flera annonser, och statusen för endast en av annonserna ändras. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Produktfält (shoppingfält)

Mer information om hur du skapar shoppingannonser finns i &quot;[Implementera [!DNL Microsoft Advertising] shoppingkampanjer](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Promotion Line] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Creative Type] | Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annons eller b) en &quot;[!UICONTROL AMO ID].&quot; Om du däremot inte inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], och annonsegenskapskolumnerna matchar flera annonser, och statusen för endast en av annonserna ändras. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Responsiva (multimedia) och fält

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | För responsiva annonser [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]och [!UICONTROL Ad Title 3] krävs för att skapa annonser och alla andra annonsrubrikfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser). <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] krävs för att skapa annonser, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar en annons och skapar en ny. |
| [!UICONTROL Business Name] | Krävs för att skapa eller ta bort en annons. |
| [!UICONTROL Call To Action] | Krävs för att skapa en annons. |
| [!UICONTROL Call To Action Language] | Krävs för att skapa en annons. |
| [!UICONTROL Base URL/Final URL] | Krävs för att skapa en annons. |
| [!UICONTROL Creative Type] | Valfritt. |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annons eller b) en &quot;[!UICONTROL AMO ID].&quot; Om du däremot inte inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], och annonsegenskapskolumnerna matchar flera annonser, och statusen för endast en av annonserna ändras. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Reklamfält för responsiv sökning

Använd &quot;[!UICONTROL Responsive Search Ad]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | För responsiva sökannonser [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]och [!UICONTROL Ad Title 3] krävs för att skapa en annons och alla andra annonsrubrikfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Valfritt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | För responsiva sökannonser [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] krävs för att skapa en annons, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive hakparenteser). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Valfritt |
| [!UICONTROL Display Path 1] | Valfritt |
| [!UICONTROL Display Path 2] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Krävs för att skapa en annons. |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Creative Type] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs för att redigera eller ta bort annonser såvida inte raden innehåller en[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort annonser såvida du inte inkluderar annons-ID:t. |

### Text och fält

Använd &quot;[!UICONTROL Creative (except RSA)]&quot; i [!UICONTROL Download Bulksheet] -dialogrutan.

>[!NOTE]
>
>Utökade textannonser har tagits bort. Du kan bara ta bort befintliga textannonser.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Skrivskyddad |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Skrivskyddad |
| [!UICONTROL Display URL] | Skrivskyddad |
| [!UICONTROL Display Path 1] | Skrivskyddad |
| [!UICONTROL Display Path 2] | Skrivskyddad |
| [!UICONTROL Base URL/Final URL] | Skrivskyddad |
| [!UICONTROL Custom URL Param] | Skrivskyddad |
| [!UICONTROL Creative Type] | Valfritt |
| [!UICONTROL Tracking Template] | Skrivskyddad |
| [!UICONTROL Creative Preferred Devices] | Skrivskyddad |
| [!UICONTROL Ad Status] | Obligatoriskt |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller ett[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar annons-ID:t.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökmålfält (automatiskt mål)

>[!NOTE]
>
>Det går inte att skapa support.

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Auto Target Expression] | Obligatoriskt. |
| [!UICONTROL Match Type] | Valfritt |
| [!UICONTROL Max CPC] | Valfritt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Target Status] | Krävs för att ta bort ett mål |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Target ID] | Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller ett &quot;[!UICONTROL AMO ID]&quot; för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Fält för produktgrupp som köpts

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Match Type] | Krävs för att skapa en produktgrupp. |
| [!UICONTROL Max CPC] | Krävs för att skapa en produktgrupp. |
| [!UICONTROL Parent Product Groupings] | Obligatoriskt |
| [!UICONTROL Product Grouping] | Obligatoriskt |
| [!UICONTROL Partition Type] | Krävs för att skapa en produktgrupp. |
| [!UICONTROL Base URL/Final URL] | Obligatoriskt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Product Group Status] | Krävs endast för att ta bort en produktgrupp. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Product Group ID] | Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Webblänksfält på kampanjnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| Beskrivningsrad 1 | Valfritt |
| [!UICONTROL Description Line 2] | Valfritt |
| [!UICONTROL Start Date] | Valfritt |
| [!UICONTROL End Date] | Valfritt |
| [!UICONTROL Base URL/Final URL] | Obligatoriskt |
| [!UICONTROL Custom URL Param] | Valfritt |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Creative Preferred Devices] | Valfritt |
| [!UICONTROL Link Name] | Obligatoriskt |
| [!UICONTROL Sitelink Status] | Krävs endast för att ta bort en sitellänk. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Sitelink ID] | Krävs endast när du ändrar eller tar bort platslänken, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera platslänken eller b) en &quot;[!UICONTROL AMO ID].&quot; Om du inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID]  och egenskapskolumnerna matchar flera sitelinks ändras bara statusen för en av sitelinks.<br><br><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du inte inkluderar någon av [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för plats

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Location] | Obligatoriskt |
| [!UICONTROL Location Type] | Krävs för att skapa ett mål |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Location Status] | Krävs endast för att ta bort ett platsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data om du inte inkluderar kampanj-ID:t.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält på kampanjnivå och annonsgruppsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Device] | Krävs för att ta bort ett enhetsmål. |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Ad Group Name] | Krävs för enhetsmål på annonsnivå. Gäller inte för enhetsmål på kampanjnivå. |
| [!UICONTROL Device Target Status] | Krävs endast för att ta bort ett enhetsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt endast för enhetsmål på annonsnivå. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhetens mål-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för RLSA på kampanjnivå och annonsgruppsnivå

| Fält | Obligatoriskt? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller ett &quot;[!UICONTROL AMO ID]&quot; för enheten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Krävs för annonsnivåmål. Gäller inte för kampanjnivåmål. |
| [!UICONTROL Audience] | Krävs för att skapa ett nytt mål. |
| [!UICONTROL Target Type] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL RLSA Target Status] | Krävs för att ta bort ett mål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt Gäller endast för annonsnivåmål. |
| [!UICONTROL RLSA Target ID] | Krävs endast när du ändrar eller tar bort målet, såvida inte raden innehåller ett &quot;[!UICONTROL AMO ID]&quot; för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar mål-ID:t för RLSA.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

>[!MORELIKETHIS]
>
>* [Bilaga - Fallkalkylbladsfel](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Filformat för kalkylblad som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickningsspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överföra en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
