---
title: Obligatoriska kalkylbladsdata för  [!DNL Microsoft Advertising] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för  [!DNL Microsoft Advertising] konton.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Bilaga - Obligatoriska balansräkningsdata för [!DNL Microsoft Advertising]-konton

Om du vill skapa och uppdatera [!DNL Microsoft Advertising]-kampanjdata i grupp kan du använda skalkylbladsfiler för sökning, sociala medier och Commerce som är särskilt formaterade för [!DNL Microsoft Advertising]-konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det filformat som krävs eller b) skapa dem manuellt (mer information om vilka filformat som stöds finns i [Filformat som stöds i bulkblad](bulksheet-file-formats.md)).

Varje kalkylblad måste innehålla rubrikfält och motsvarande datafält som krävs för de [specifika åtgärder som du vill utföra](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (till exempel skapa en annons). När ett fält inte är obligatoriskt kan du utesluta det från rubriken och dataraderna. Alla anpassade kolumner tas bort när du överför bulkbladsfilen.

Nedan följer en tabell över alla tillgängliga datafält och ytterligare tabeller som anger vilka fält som krävs för att lägga till, redigera eller ta bort data för enskilda enheter (till exempel kampanjer och nyckelord).

## Alla tillgängliga datafält {#bulksheet-fields-all-microsoft}

I följande tabell beskrivs alla tillgängliga datafält.

Information om de datafält som är relevanta för kontoentiteter finns i [Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent](#bulksheet-fields-per-component-microsoft).

| Fält | Beskrivning |
|----|----|
| [!UICONTROL Platform] | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Acct Name] | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Det unika namn som identifierar en kampanj för ett konto. Maximala längden är 128 tecken. |
| [!UICONTROL Campaign Budget] | Den dagliga eller månadsvisa kampanjbudgeten, med eller utan monetära symboler och interpunktion. Den får inte vara mindre än 0,05. |
| [!UICONTROL Channel Type] | Den kanaltyp som kampanjen har som mål: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> eller <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Endast kampanjer med daglig budget) Så här snabbt kan du visa annonser för kampanjen varje dag:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (standard för nya kampanjer): För att sprida annonsintrycken över dagen.</li><li><i>[!UICONTROL Accelerated]:</i> Om du vill visa dina annonser så ofta som möjligt tills din budget är nådd. Därför kanske era annonser inte visas senare under dagen.</li></ul> |
| [!UICONTROL Campaign Priority] | (Endast köpkampanjer) Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt: <i>[!UICONTROL Low]</i> (standard för nya kampanjer), <i>[!UICONTROL Medium]</i> eller <i>[!UICONTROL High]</i>.<br><br>När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad. |
| [!UICONTROL Merchant ID] | (Kundkampanjer och målgruppskampanjer som endast är kopplade till en handlarfeed) Kund-ID för det handlarkonto vars produkter används för kampanjen. |
| [!UICONTROL Sales Country] | (Endast köpkampanjer; skrivskyddat för befintliga kampanjer) Det land där kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen. |
| [!UICONTROL Product Scope Filter] | (Kampanjer som endast använder shoppingnätverket) De produkter på ert handelskonto för vilka produktannonser kan skapas för kampanjen. Du kan ange upp till sju produktdimensioner och attributkombinationer där du kan filtrera dina produkter med formatet dimension=attribut. Avgränsa flera filter med avgränsaren &quot;>>&quot;. En lista över tillgängliga produktdimensioner finns i &quot;[Produktfilter för köpkampanj](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.<br><br> Exempel: `CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies` <br><br> Om du vill ta bort de befintliga värdena använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL DSA Domain Name] | (Kampanjer av typen a) <i>[!UICONTROL DynamicSearchAds]</i> eller b) <i>[!UICONTROL Search]</i> när elementet [!DNL ExperimentId] inte har angetts) Domännamnet för webbplatsen som mål för dynamiska sökannonser. Maxlängden är 2 048 tecken. Om domännamnet innehåller `www` trimmas det och används inte.<br><br>För befintliga kampanjer kan du inte redigera domänen, men du måste inkludera den för att kunna uppdatera andra egenskaper. |
| [!UICONTROL DSA Domain Language] | (Kampanjer av typen a) <i>[!UICONTROL DynamicSearchAds]</i> eller b) <i>[!UICONTROL Search]</i> när elementet [!DNL ExperimentId] inte har angetts) Webbplatssidornas språk som mål för dynamiska sökannonser. De domänspråk som stöds är [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] och [!UICONTROL Swedish].<br><br>För befintliga kampanjer kan du inte redigera språket, men du måste inkludera det för att kunna uppdatera andra egenskaper. |
| [!UICONTROL Ad Group Name] | Det unika namn som identifierar en annonsgrupp. Maximala längden är 128 tecken. Efterföljande tomma tecken sparas inte (till exempel sparas&quot;Annonsgrupp 1&quot; som&quot;Annonsgrupp 1&quot;). |
| [!UICONTROL Ad Group Type] | (Kampanjer i söknätverket, skrivskyddade för befintliga annonsgrupper) Annonsgruppstypen: <i>[!UICONTROL Audience]</i> (endast för målgruppskampanjer), <i>[!UICONTROL Search Dynamic]</i> (endast för dynamiska sökannonser) och <i>[!UICONTROL Search Standard]</i> (endast för responsiva sökannonser och befintliga utökade textannonser). Vissa kampanjtyper kan innehålla flera typer av annonsgrupper. |
| [!UICONTROL Keyword] | (Endast kampanjer i söknätverket) Nyckelordssträngen. Maximala längden är 50 tecken.<br><br><b>Anteckningar:</b><ul><li>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du [!UICONTROL Match Type] till `Negative`. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn exkluderas nyckelordet för hela kampanjen.</li><li>Om du ändrar ett [!DNL Microsoft Advertising]-nyckelord tas det befintliga nyckelordet bort och ett nytt skapas med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.</li></ul> |
| Placement | Föråldrat |
| [!UICONTROL Audience] | Återmarknadsföringslistan för sökannonser (RLSA) som riktar sig till målgruppen för kampanjen eller annonsgruppen. |
| [!UICONTROL Target Type] | (Endast RLSA-mål) Måltypen: <i>[!UICONTROL Inclusion]</i> eller <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamiska sökmål för annonsgruppen. Använd [!UICONTROL All Web Pages] för alla mål.<br><br>Om du vill ha upp till tre dynamiska sökvillkor använder du formatet `<category>=<target>`, där &lt;category> kan inkludera någon av kategorierna nedan. Koppla flera mål för en enskild kategori med `[blank space] and [blank space]` och förena flera kategorier med `[blank space] and [blank space]`.<br><ul><li><i>Kategori:</i> Så här visar du dynamiska sökannonser för indexerade sidor med en specifik Google-innehållskategori.</li><li><i>URL:</i> Om du vill visa dynamiska sökannonser för indexerade sidor med en specifik URL-adress, där värdet kan inkluderas var som helst i URL-adressen.</li><li><i>Sidrubrik:</i> Så här visar du dynamiska sökannonser för indexerade sidor med specifik text i sidrubriken.</li><li><i>Sidinnehåll:</i> Så här visar du dynamiska sökannonser för indexerade sidor med visst innehåll.</li></ul>Exempel: url=shoes.example.com och page title=skos<br>Exempel: Alla webbsidor |
| [!UICONTROL Location] | En geografisk plats där annonser för kampanjen eller annonsgruppen ska placeras. Värdena är inte skiftlägeskänsliga. Om du inte anger några värden för kampanjen eller annonsgruppen anges alla platser som mål. Om du vill ange specifika platser som mål anger du platsen med hjälp av platskodformaten [!DNL Microsoft Advertising]. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising]-utvecklarportalen med autentiseringsuppgifterna för ditt [!DNL Microsoft Advertising]-annonskonto. <b>Obs!</b> Om du vill utesluta en plats skriver du ett minustecken (`-`) före platskoden, till exempel `-United States`. |
| [!UICONTROL Location Type] | Platstypen, till exempel Ort, Land, MetroArea, Postnummer och Delstat. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising]-utvecklarportalen med autentiseringsuppgifterna för ditt [!DNL Microsoft Advertising]-annonskonto. |
| [!UICONTROL Match Type] | (Endast kampanjer i söknätverket) Nyckelordsmatchningsalternativ. Detta kan inkludera nyckelordsmatchningsalternativet för ett dynamiskt sökmål eller en produktgrupp. Värdena är: <i>[!UICONTROL Broad]</i> (standard för nya nyckelord), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (anges automatiskt för nyckelord när annonskoncern har innehållsnätverket som mål), <i>[!UICONTROL Negative]</i> (för att utesluta ett nyckelord i innehållsnätverket), <i>[!UICONTROL Dynamic Ad Target]</i> (standard för nya dynamiska sökmål), <i>[!UICONTROL Product Group]</i> (standard för nya produktgrupper) eller <i>[!UICONTROL Negative Product Group]</i> (för att exkludera en produktgrupp).  Ett värde för matchningstypen eller nyckelords-ID krävs för att redigera eller ta bort ett nyckelord med flera matchningstyper.<br><br>För Brett matchningsmodifierare väljer du &quot;Bred&quot; och infogar `+` före ett ord i nyckelordet som krävs (till exempel &quot;`+red +shoes`&quot; för att kräva både &quot;red&quot; och &quot;skor&quot;).<br><br>Om du ändrar matchningstypen för ett [!DNL Microsoft Advertising]-nyckelord tas inte det befintliga nyckelordet bort. |
| [!UICONTROL Max CPC] | (Kampanjer i söknätverket) Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för en annons baserat på nyckelordet, produktgruppen eller det dynamiska sökmålet, med eller utan monetära symboler och interpunktion.  För befintliga nyckelords- och produktgruppsposter i optimerade portföljer gäller uppdateringarna endast en dag och skrivs över under nästa optimeringscykel. <b>Obs!</b> Du kan inte ange anbud för negativa nyckelord. |
| [!UICONTROL Max Content CPC] | (Endast skrivskyddat för CPC-kampanjer som skapats innan innehållsnätverket togs bort 2017) Den maximala innehållskostnaden per klick (CPC), som är den högsta summan att betala för ett reklamklick från en webbplats i visningsnätverk, med eller utan monetära symboler och interpunktion. |
| [!UICONTROL Audience Target Method] | (Målgrupper och grupper) Om:<ul><li><i>[!UICONTROL Target and Bid]:</i> Om du bara vill visa annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.</li><li><i>[!UICONTROL Bid Only]:</i>Visa annonser även för personer som inte är associerade med målgrupper så länge de uppfyller andra annonsgruppsmål.</li></ul> Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper. |
| [!UICONTROL Parent Product Groupings] | Hierarkin för överordnade produktgrupper.<br><br>Exempel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Produktgruppen (till exempel&quot;brand=acme&quot; eller&quot;Alla produkter&quot;).<br><br><b>Anteckningar:</b><ul><li>När en angiven produktgrupp inte finns i hierarkin för överordnade produktgrupper skapar Search, Social och Commerce alla delar av hierarkin som behövs.</li><li>Search, Social, &amp; Commerce skapar automatiskt en [!UICONTROL All Products]-grupp när du skapar en annonsgrupp i en shoppingkampanj med ett standardbud som är inställt på annonsgruppens standardbud. Search, Social, &amp; Commerce skapar automatiskt en [!UICONTROL Everything Else]-grupp med annonsgruppens standardbud på varje nivå i produktgruppshierarkin. Du kan fortfarande explicit skapa dessa standardgrupper och antingen exkludera dem eller ändra deras bud.</li><li>Varje annonsgrupp kan innehålla upp till åtta nivåer av produktgrupper, inklusive [!UICONTROL All Products] och sju andra nivåer.</li></ul> |
| [!UICONTROL Partition Type] | Partitionstypen för produktgruppen: <i>[!UICONTROL subdivision]</i> (när den har underordnade produktgrupper) eller <i>[!UICONTROL unit]</i> (när den inte har några underordnade produktgrupper). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Endast expanderade textannonser, multimediaannonser, responsiva annonser och responsiva sökannonser) Rubrikerna i en annons. Den maximala längden för varje annonstitelfält är 30 eller 15 dubbelbytetecken, inklusive all dynamisk text (till exempel värdena för nyckelord, `{Param2}` och `{Param3}` dynamiska ersättningsvariabler samt annonsanpassare).<br><br> För responsiva sökannonser infogar du en annonsanpassare med följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För expanderade textannonser krävs annonsrubrik och annonsrubrik 2 och [!UICONTROL Ad Title 3] är valfritt. [!DNL Microsoft Advertising] föråldrade utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser krävs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] och [!UICONTROL Ad Title 3] och alla andra annonsrubrikfält är valfria.<br><br>Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive parenteserna).<br><br>För alla annonstyper utom för expanderade textannonser tas den befintliga annonsen bort om du ändrar annonsen och skapar en ny annons med samma egenskaper. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Endast responsiva sökannonser; valfritt) En position där motsvarande annonsrubrik ska fästas: `[null]` (inget värde, vilket gör annonsrubriken giltig för alla positioner), 1, 2 eller 3. Om [!UICONTROL Ad Title Position] till exempel har värdet 1 kan [!UICONTROL Ad Title] bara visas i position 1. Som standard är alla annonsrubriker null (saknar värden). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna).<br><br><b>Obs!</b> Du kan fästa flera annonsrubriker på samma plats. Annonsnätverket använder en av de annonstitlar som är fästa vid positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Endast textannonser, dynamiska sökannonser, multimediaannonser, responsiva sökannonser och förbättrade sitelinks på kampanjnivå) Innehållet i en annons eller en sitelink.<br><br>För sitelinks kan du använda både [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] för att inkludera extra text som annonsnätverket kan visa under länktexten. Varje beskrivningsfält kan innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>För annonser är den maximala längden för varje beskrivningsfält 90 eller 45 dubbelbyte-tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).<br><br>För responsiva sökannonser infogar du en annonsanpassare med följande format, där standardtext är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>För textannonser och dynamiska sökannonser krävs Description Line 1 och [!UICONTROL Description Line 2] är valfritt.<br><br>För multimediaannonser, responsiva annonser och responsiva sökannonser krävs [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2], och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna).<br><br><b>Anteckningar:</b><ul><li>(Standardtextannonser) Den kombinerade titeln och texten måste vara minst tre ord.</li><li>(Utökade textannonser) Det här fältet kan innehålla variablerna {Param2} och {Param3} dynamiskt. I så fall är annonstextens maximala längd 300 enkelbyte- eller 150 dubbelbyte-tecken. [!DNL Microsoft Advertising] föråldrade utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li><li>(Dynamiska sökannonser) Dynamisk ersättningstext tillåts inte.</li><li>För alla annonstyper utom expanderade textannonser tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Endast responsiva sökannonser; valfritt) En position där motsvarande beskrivning ska fästas: `[null]` (inget värde, vilket gör beskrivningen berättigad för alla positioner), 1, 2 eller 3. Om [!UICONTROL Description 1 Position] till exempel har värdet 1 kan Beskrivning 1 bara visas i Position 1. Som standard är inga beskrivningar fästa vid en position.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna).<br><br><b>Obs!</b> Du kan fästa flera beskrivningar på samma plats. Annonsnätverket använder en av beskrivningarna som är fästa vid positionen. Beskrivningar som fästs vid position 2 kanske inte visas tillsammans med annonsen. |
| [!UICONTROL Business Name] | (Endast multimediaannonser) Företagsnamnet, med högst 25 tecken. |
| [!UICONTROL Promotion Line] | (Endast produktlistade annonser) En unik kampanjrad som ska inkluderas i produktlistan i sökresultaten (till exempel&quot;Fraktfritt nu!). Maximala längden är 45 tecken.<br><br>Kampanjraden kan visas på olika platser i förhållande till annonsen (till exempel nedanför annonsen) beroende på var annonsen visas på sidan. |
| [!UICONTROL Display URL] | Den URL som ingår i annonsen.<br><br>För expanderade dynamiska sökannonser genererar annonsnätverket det här värdet dynamiskt från webbplatsdomänen, och du behöver inte ange något värde.<br><br>För expanderade textannonser och responsiva sökannonser behöver du inte ange något värde. Visnings-URL:en extraheras automatiskt från domänen i den slutliga URL:en. Du kan också anpassa URL-adressen med fälten Sökväg 1 och Sökväg 2.<br><br><b>Anteckningar:</b><ul><li>(Konton med slutliga URL:er) Domännamnen i den URL som visas och den slutliga URL:en måste matcha.</li><li>[!DNL Microsoft Advertising] föråldrade utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem.</li></ul> |
| [!UICONTROL Display Path 1] | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) Text som läggs till i URL:en som automatiskt extraheras från den slutliga URL:en. Varje sökväg föregås av ett snedstreck (/) i URL:en. En bana får inte innehålla snedstreck (/) eller radmatningstecken (\n). Den maximala längden för varje bana är 15 tecken eller 7 dubbelbyte-tecken.<br><br>Om du vill infoga en annonsanpassare använder du följande format, där&quot;Standardtext&quot; är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`<br><br>Om [!UICONTROL Display Path 1] är&quot;erbjudanden&quot;, är visnings-URL:en &lt;display URL>/erbjudanden, till exempel www.example.com/deals.<br><br>[!DNL Microsoft Advertising] föråldrade utökade textannonser i augusti 2022, och du kan nu bara rapportera om och ta bort dem. |
| [!UICONTROL Display Path 1] | (Endast expanderade textannonser, dynamiska sökannonser och responsiva sökannonser) En extra visningssökväg. Se posten för [!UICONTROL Display Path 1].<br><br>Exempel: Om [!UICONTROL Display Path 1] är&quot;erbjudanden&quot; och [!UICONTROL Display Path 2] är&quot;lokal&quot; är visnings-URL:en &lt;<i>visa-URL</i>>/erbjudanden/lokal, till exempel www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Endast utökade sitelinks) Det första datum då anbud får lämnas för sitelink, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyyy eller m-d-yy. Standardinställningen för nya utökade sitelinks är den aktuella dagen. <b>Obs!</b> Nya förbättrade sitelinks kan bara skapas i kampanjer med befintliga utökade sitelinks eller utan sitelinks. |
| [!UICONTROL End Date] | Det sista datum då sitelänken kan visas med annonser, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny sitelink är standardvärdet `[blank]` (det vill säga inget slutdatum). |
| [!UICONTROL Call To Action] | Uppmaningen att ta med i annonsen. I [API-referensen finns en lista med möjliga värden](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), men du kan ange flera ord för att kunna utföra åtgärder som flera ord (till exempel &quot;Bet Now&quot; i stället för &quot;BetNow&quot;) i kalkylblad. |
| [!UICONTROL Call To Action Language] | Språket för alternativen för att ringa upp till åtgärd. I [API-referensen finns en lista över möjliga språk](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | Den URL till landningssidan som sökmotoranvändare tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas-/slutadresser på nyckelordsnivå åsidosätter de på annonsnivå och högre.<br><br>Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Destination URL] | (Ingår i genererade kalkylblad i informationssyfte, inte i sökmotorn) För konton med mål-URL:er är detta den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och Commerce. Om du genererade spårnings-URL:er baseras detta på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till parametrar som är specifika för sökmotorn kan de ersättas med motsvarande parametrar för Search, Social och Commerce.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som kolumnen Bas-URL/Slutlig URL. |
| [!UICONTROL Custom URL Param] | Data som ska ersätta den dynamiska variabeln `{custom_code}` när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL:en måste du överföra kalkylbladsfilen med alternativet Generera spårnings-URL:er. |
| [!UICONTROL Creative Type] | Annonsformatet: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (kundannonser), <i>[!UICONTROL Responsive Search Ad]</i> eller <i>[!UICONTROL Text ad]</i>. Standardvärdet för nya annonser är <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Det första datum då anbud kan lämnas för annonskoncern, i annonsören tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet aktuellt datum. |
| [!UICONTROL Ad Group End Date] | Det sista datum då anbud kan lämnas för annonsgruppen, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. För en ny annonsgrupp är standardvärdet [blank] (det vill säga inget slutdatum). |
| [!UICONTROL Tracking Template] | (Valfritt) Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet längst till granulerad) åsidosätter värdena på alla högre nivåer.<br><br>För spårning av Adobe Advertising-konvertering, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs kod för omdirigering och spårning automatiskt till när du sparar posten.<br><br>Ange ett värde för omdirigeringar och spårning från tredje part.<br><br>En lista över parametrar som anger de slutliga URL:erna i spårningsmallar finns i [!DNL Microsoft Advertising] -dokumentationen.<br><br> Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Landing Page Suffix] | Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Exempel: `param2=value1&param3=value2`<br><br>Se &quot;[Klicka-spårningsformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)&quot;.<br><br>Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Microsoft Advertising]-redigeraren. |
| Nätverksstatus för sökning | Om annonser ska placeras för annonsgruppen på olika element i söknätverket:<ul><li><i>Alla:</i> Om du vill placera annonser i alla Bing-söknätverk och syndikerade sökpartners.</li><li><i>OwnedAndOperatedOnly:</i>Om du bara vill placera annonser på Bing och Yahoo! webbplatser.</li><li><i>SyndicatedSearchOnly:</i> Om du bara vill placera annonser på Bing och Yahoo! syndikerade sökpartners.</li><li><i>Av:</i> Om du bara vill placera annonser i innehållsnätverket (inte i söknätverket).</li></ul> För nya annonsgrupper är standardvärdet På. |
| [!UICONTROL Content Network Status] | Föråldrat |
| [!UICONTROL Languages] | Målspråket för annonser i annonsgruppen: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] eller [!UICONTROL Swedish]. Standardvärdet för nya kampanjer är [!UICONTROL English].<br><br>Den här inställningen avgör i vilka länder och regioner annonsen kan visas. Se till att välja ett språk som är kompatibelt med kampanjens platsmål. |
| [!UICONTROL Budget Type] | Anger om budgeten är <i>[!UICONTROL Daily]</i> (standard) eller <i>[!UICONTROL Monthly]</i>.<br><br>Obs! Om du tilldelar kampanjen till en optimerad portfölj ställs det här värdet automatiskt in på [!UICONTROL Daily]. |
| [!UICONTROL Device] | En enhetstyp för vilken anbudsjusteringar görs på kampanj- eller annonsgruppsnivå: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> eller <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Börsjusteringen för en angiven måltyp. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för smarttelefoner är 50 %, är smarttelefonanbudet 1,50 USD. Som standard bjuds alla mål på nyckelordsnivå. Giltiga procenttal kan vara:<ul><li>Smarttelefoner och surfplattor: -100 (köp inte för enhetstypen) och från -90 till 900</li><li>Stationär dator: från 0 till 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | De enhetstyper som du föredrar att visa annonsen eller sitelink på: <i>[!UICONTROL All]</i> (standard) eller <i>[!UICONTROL Mobile]</i>. När Mobile anges försöker nätverket att visa annonsen eller platshållaren för användare av mobila enheter i stället för för för dator- eller surfplatteanvändare. I annat fall visas annonsen eller platshållaren på alla enhetstyper i nätverket. <b>Obs!</b> Nätverket garanterar inte att annonsen visas på den önskade enhetstypen. |
| [!UICONTROL Param2] | Den sträng som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens rubrik, beskrivning eller bas-URL innehåller den dynamiska `{Param2}`-ersättningssträngen. Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Param3] | Den sträng som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens rubrik, beskrivning eller bas-URL innehåller den dynamiska `{Param3}`-ersättningssträngen. Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken). Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Link Name] | Sitelink-texten. Den måste vara unik i kampanjen. Om du anger Description1 och Description2 kan sitelink-texten innehålla upp till 25 enkelbyte- eller 12 dubbelbyte-tecken. I annat fall kan sitelink-texten innehålla upp till 35 enkelbyte- eller 17 dubbelbyte-tecken.<br><br>[!DNL Microsoft Advertising] kan visa två, fyra eller sex förbättrade sitelinks med beskrivningar, eller fyra eller sex sitelinks i en enda rad utan beskrivningar, med en annons.<br><br>Du kan bara skapa nya förbättrade sitelinks i kampanjer med befintliga utökade sitelinks eller utan sitelinks. |
| [!UICONTROL Campaign Status] | Visningsstatus för kampanjen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga kampanjer). Standardvärdet för nya kampanjer är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet `Deleted`. |
| [!UICONTROL Ad Group Status] | Annonsgruppens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonsgrupper). Standardvärdet för nya annonsgrupper är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet `Deleted`. |
| [!UICONTROL Keyword Status] | Visningsstatus för nyckelordet: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är [!UICONTROL Active]. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet `Deleted`. <b>Obs!</b> Om du skapar spårnings-URL:er för ett nyckelord med flera matchningstyper måste nyckelordsstatusen för varje matchningstyp vara densamma. |
| [!UICONTROL Placement Status] | Föråldrat |
| [!UICONTROL Ad Status] | Annonsens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (endast befintliga annonser), <i>[!UICONTROL Disapproved]</i> (inte redigerbara) eller <i>[!UICONTROL Paused]</i>. Standardvärdet för nya annonser är [!UICONTROL Active]. Om du vill ta bort en aktiv eller pausad annons anger du värdet `Deleted`. |
| [!UICONTROL Target Status] | Status för ett dynamiskt sökmål: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga mål). Standardvärdet för nya mål är [!UICONTROL Active]. Om du vill ta bort ett aktivt eller pausat mål anger du värdet `Deleted`. |
| [!UICONTROL Sitelink Status] | Visningsstatus för sitelink: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga sitelinks). Standardvärdet för nya sitelinks är [!UICONTROL Active]. Ange värdet `Deleted` om du vill ta bort en aktiv sitellänk. |
| [!UICONTROL Location Status] | Status för platsmålet: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga platser). Standardvärdet för nya platser är [!UICONTROL Active]. Om du vill ta bort en aktiv plats anger du värdet `Deleted`. |
| [!UICONTROL Product Group Status] | Produktgruppens visningsstatus: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga produktgrupper). Standardvärdet för nya produktgrupper är [!UICONTROL Active]. Om du vill ta bort en aktiv produktgrupp anger du värdet `Deleted`. |
| [!UICONTROL Device Target Status] | Status för enhetsmålet på kampanj- eller annonsnivå: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i>. För nya kampanjer och annonsgrupper är standardvärdet [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Status för RLSA-målet på kampanjnivå eller annonsnivå eller (endast Google Ads) undantag: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga mål). Standardvärdet för nya mål eller undantag är [!UICONTROL Active]. Om du vill ta bort ett aktivt mål eller undantag anger du värdet `Deleted`. |
| \[Advertiser-specific Label Classification\] | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden används för alla underordnade komponenter. Nya komponenter som läggs till senare associeras automatiskt med etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Varken klassificeringsnamnet eller klassificeringsvärdet är skiftlägeskänsliga. |
| [!UICONTROL Constraints] | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><b>>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL Campaign ID] | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för kampanjen. |
| [!UICONTROL Ad Group ID] | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för annonsgruppen. |
| [!UICONTROL Placement ID] | Föråldrat |
| [!UICONTROL Keyword ID] | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordet, såvida inte raden innehåller a) tillräckligt många egenskapskolumner för att identifiera nyckelordet eller b) ett [!UICONTROL AMO ID].&quot; |
| [!UICONTROL Ad ID] | <p>Det unika ID som identifierar en befintlig annons. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] För responsiva sökannonser krävs antingen annons-ID eller AMO-ID för att redigera eller ta bort annonsdata. För alla andra entitetstyper krävs AMO-ID bara när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga ad-egenskapskolumner för att identifiera annonsannons eller b) en [!UICONTROL AMO ID].&quot; Om du däremot varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna.</p><p><b>Obs!</b> Om du redigerar a) och egenskapskolumner förutom Status för en befintlig annons eller b) data för en responsiv sökannons, och du inkluderar varken [!UICONTROL Ad ID] eller [!UICONTROL AMO ID], skapas en ny annons och den befintliga annonsen ändras inte. </p> |
| [!UICONTROL Sitelink ID] | Det unika ID som identifierar en befintlig platslänk. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort platslänken, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera platslänken eller b) en [!UICONTROL AMO ID].&quot; Om du däremot inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID] och egenskapskolumnerna matchar flera sitelinks ändras bara statusen för en av sitelinks.</p><p><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom status för en befintlig sitelink, och du varken inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL Product Group ID] | Det unika ID som identifierar en befintlig produktgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en [!UICONTROL AMO ID].&quot; |
| Plats-ID | Den unika identifieraren [!DNL Microsoft Advertising] för platsmålet. Om du vill hämta en platslista loggar du in på [!DNL Microsoft Advertising]-utvecklarportalen med autentiseringsuppgifterna för ditt [!DNL Microsoft Advertising]-annonskonto. Krävs endast när du ändrar eller tar bort platsmålet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL Target ID] | Det unika ID som identifierar ett befintligt automatiskt mål. Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL RLSA Target ID] | Det unika ID som identifierar ett befintligt RLSA-mål på kampanj- eller annonsgruppsnivå. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar eller tar bort målet eller undantaget, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL AMO ID] | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar annons-ID:t. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| [!UICONTROL EF Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL EF Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL SE Error Message] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL SE Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL Exemption Request] | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa namn och text för alla Google reklampolicyer som en annons bryter mot. |
| [!UICONTROL Retail Hash] | (Ingår i informationssyfte i kalkylblad som genererats med Advanced Campaign Management) En alfanumerisk hash-kod (t.ex. f9639f40cdf56524b541e5dacf55a991) som anger att objektet genererades i vyn Avancerat (ACM). |

[^1]: [!DNL Excel] konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

## Fält som krävs för att skapa, redigera eller ta bort varje kontokomponent {#bulksheet-fields-per-component-microsoft}

Följande avsnitt innehåller fält som är relevanta för specifika kontoenheter.

>[!NOTE]
>
>När ett fält inte kan användas för en åtgärd, ignoreras alla värden som anges i fältet.

### Kampanjfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Campaign Budget] | Krävs för att skapa en kampanj. | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter men kan inte överskrida kontobudgeten. |
| [!UICONTROL Channel Type] | Krävs för att skapa en kampanj. |
| [!UICONTROL Delivery Method] | Valfritt |
| [!UICONTROL Campaign Priority] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Merchant ID] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Sales Country] | Krävs för att skapa en shoppingkampanj. |
| [!UICONTROL Product Scope Filter] | (Kampanjer) Valfritt |
| [!UICONTROL DSA Domain Name] | Krävs för att skapa en kampanj av typen a) [!UICONTROL DynamicSearchAds] eller b) [!UICONTROL Search] när elementet [!DNL ExperimentId] inte har angetts) |
| [!UICONTROL DSA Domain Language] | Krävs för att skapa en kampanj av typen a) [!UICONTROL DynamicSearchAds] eller b) [!UICONTROL Search] när elementet [!DNL ExperimentId] inte har angetts) |
| [!UICONTROL Tracking Template] | Valfritt |
| [!UICONTROL Landing Page Suffix] | <p>Valfritt |
| [!UICONTROL Budget Type] | Krävs för att skapa en kampanj. |
| [!UICONTROL Device] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Campaign Status] | Krävs endast för att ta bort en kampanj. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Constraints] | Valfritt |
| [!UICONTROL Campaign ID] | Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller [!UICONTROL AMO ID] för kampanjen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Annonsgruppsfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Ad Group ID] | Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller [!UICONTROL AMO ID] för annonsgruppen. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Nyckelordsfält

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Keyword ID] | Krävs endast när du redigerar eller tar bort nyckelordet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökannonsfält

>[!NOTE]
>
>Det går inte att skapa support.

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] krävs för att redigera beskrivningen. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas. |
| [!UICONTROL Display Path 1] | Krävs för att redigera fältet. |
| [!UICONTROL Display Path 2] | Krävs för att redigera fältet. |
| [!UICONTROL Creative Type] | Krävs för att skapa eller redigera status för en produktannons. |
| [!UICONTROL Creative Preferred Devices] | Valfritt |
| [!UICONTROL Ad Status] | Krävs för att ta bort en annons. |
| \[Advertiser-specific Label Classification\] | Valfritt |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt |
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsadressen eller b) en [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Produktfält (shoppingfält)

Mer information om hur du skapar shoppingannonser finns i [Implementera [!DNL Microsoft Advertising] shoppingkampanjer](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html?lang=sv-SE).

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsadressen eller b) en [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Responsiva (multimedia) och fält

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | För responsiva annonser krävs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] och [!UICONTROL Ad Title 3] för att skapa annonser, och alla andra annonstitelfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive parenteserna). <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] krävs för att skapa annonser, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. <b>Obs!</b> För den här annonstypen tas den befintliga annonsen bort om du ändrar och kopierar den och en ny skapas. |
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
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller a) tillräckliga annonsegenskapskolumner för att identifiera annonsadressen eller b) en [!UICONTROL AMO ID]. Men om du varken inkluderar [!UICONTROL Ad ID] eller [!UICONTROL AMO ID] och annonsegenskapskolumnerna matchar flera annonser, ändras statusen för endast en av annonserna. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Reklamfält för responsiv sökning

Använd raden [!UICONTROL Responsive Search Ad] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Obligatoriskt | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | För responsiva sökannonser krävs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] och [!UICONTROL Ad Title 3] för att skapa en annons, och alla andra annonstitelfält är valfria. Om du vill ta bort det befintliga värdet för ett icke obligatoriskt fält använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Valfritt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | För responsiva sökannonser krävs [!UICONTROL Description Line 1] och [!UICONTROL Description Line 2] för att skapa en annons, och [!UICONTROL Description Line 3] och [!UICONTROL Description Line 4] är valfria. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
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
| [!UICONTROL Ad ID] | Krävs för att redigera eller ta bort annonser såvida inte raden innehåller en [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort annonser såvida du inte inkluderar annons-ID:t. |

### Text och fält

Använd raden [!UICONTROL Creative (except RSA)] i dialogrutan [!UICONTROL Download Bulksheet] för den här annonstypen.

>[!NOTE]
>
>Utökade textannonser har tagits bort. Du kan bara ta bort befintliga textannonser.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Ad ID] | Krävs endast när du ändrar annonsstatus, såvida inte raden innehåller [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar annons-ID:t.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Dynamiska sökmålfält (automatiskt mål)

>[!NOTE]
>
>Det går inte att skapa support.

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Target ID] | Krävs endast när du ändrar eller tar bort det automatiska målet, såvida inte raden innehåller [!UICONTROL AMO ID] för målet. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Fält för produktgrupp som köpts

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Product Group ID] | Krävs endast när du ändrar eller tar bort produktgruppen, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera produktgruppen eller b) en [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Webblänksfält på kampanjnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
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
| [!UICONTROL Sitelink ID] | Krävs endast när du ändrar eller tar bort sitelink, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera sitelink eller b) en [!UICONTROL AMO ID]. Om du däremot inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID] och egenskapskolumnerna matchar flera sitelinks ändras bara statusen för en av sitelinks.<br><br><b>Obs!</b> Om du redigerar sitelink-egenskapskolumner förutom Status för en befintlig sitelink, och du inte inkluderar [!UICONTROL Sitelink ID] eller [!UICONTROL AMO ID], skapas en ny sitelink och den befintliga sitellänken ändras inte. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för plats

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Location] | Obligatoriskt |
| [!UICONTROL Location Type] | Krävs för att skapa ett mål |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Location Status] | Krävs endast för att ta bort ett platsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data om du inte inkluderar kampanj-ID:t.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält på kampanjnivå och annonsgruppsnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Device] | Krävs för att ta bort ett enhetsmål. |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL Ad Group Name] | Krävs för enhetsmål på annonsnivå. Gäller inte för enhetsmål på kampanjnivå. |
| [!UICONTROL Device Target Status] | Krävs endast för att ta bort ett enhetsmål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt; endast tillämpligt för enhetsmål på annonsgruppsnivå. |
| [!UICONTROL AMO ID] | Krävs för att redigera eller ta bort data såvida du inte inkluderar enhetens mål-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |

### Målfält för RLSA på kampanjnivå och annonsnivå

En beskrivning av varje datafält finns i [Alla tillgängliga datafält](#bulksheet-fields-all-microsoft).

| Fält | Obligatoriskt? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoriskt om inte varje rad innehåller [!UICONTROL AMO ID] för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt |
| [!UICONTROL Ad Group Name] | Krävs för annonsnivåmål. Gäller inte för kampanjnivåmål. |
| [!UICONTROL Audience] | Krävs för att skapa ett nytt mål. |
| [!UICONTROL Target Type] | Valfritt |
| [!UICONTROL Bid Adjustment] | Valfritt |
| [!UICONTROL RLSA Target Status] | Krävs för att ta bort ett mål. |
| [!UICONTROL Campaign ID] | Valfritt |
| [!UICONTROL Ad Group ID] | Valfritt; endast tillämpligt för annonsnivåmål. |
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
