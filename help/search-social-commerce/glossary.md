---
title: Ordlista
description: Se definitioner av nyckeltermer.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: 625bb9a466684993ac55d6358880b1ff3052d592
workflow-type: tm+mt
source-wordcount: '2240'
ht-degree: 0%

---

# Ordlista {#glossary}

## A-B {#a-b}

**annonsgrupp:** En uppsättning annonser och deras relaterade nyckelord, placeringar och produktgrupper för en kampanj.

**annonsvariation:** Alla annonser inom en annonsgrupp eller annonsstrategi.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id):** En spårningskod som gör att Adobe Advertising kan dela data om kampanjer med Adobe Analytics. Det börjar med `s_kwcid=`.

**anbudsenhet:** En söknings-, social- och Commerce-term för en enhet där bud placeras.

* För CPC-kampanjer är detta ett nyckelord och dess matchningstyp för en sök- eller innehållskampanj, en produktgrupp på enhetsnivå (den lägsta nivån av underindelning) för en shoppingkampanj eller ett dynamiskt sökmål för en dynamisk sök- och annonskampanj. När samma kombination av nyckelord och matchningstyp, samma produktgrupp eller samma dynamiska sökmål inträffar inom flera annonsgrupper i en och samma kampanj betraktas alla instanser som samma budenhet och har därmed samma bud.

* För kampanjer med utgiftsstrategierna [!DNL Maximize Clicks], [!DNL Maximize Conversion Value], [!DNL Maximize Conversions], [!DNL Target Cost Per Acquisition] eller [!DNL Target Return on Ad Spend] är varje kampanj en budenhet.

* För kampanjer på [!DNL Yahoo! Display Network], som inte använder nyckelord, har alla annonser i en annonsgrupp samma bud och betraktas som samma budenhet.

**BUD-enhetsbegränsning:** Se &quot;begränsning&quot;.

## C-D {#c-d}

**kampanj:** En uppsättning annonsgrupper i ett enda annonskonto som delar budget, tidsintervall, målgruppsinställningar och andra inställningar. **Obs!** [!DNL Baidu] har inte samma koncept som kampanjer, men Search, Social och Commerce skapar pseudokampanjer för varje uppsättning med relaterade annonsgrupper i befintliga [!DNL Baidu]-konton som synkroniseras i Search, Social och Commerce.

**skiftlägeskänsligt fält:** I ett skiftlägeskänsligt fält eller en fråga behandlas versaler (t.ex. C) annorlunda än gemener (t.ex. c). Bilen behandlas till exempel som ett annat värde än bilen.

**klicka:** En enskild användare klickar på eller i en onlineannons.

**klicka på uppslagsfönstret:** En inställning på annonsörnivå som anger antalet dagar efter ett betalt klick i en händelseserie där klickningen kan kopplas till en konvertering.

**klickningstid:** Den tidpunkt då en slutanvändare med en unik IP-adress först klickar på en annons i annonsnätverket.

**klickfrekvens:** (CTR) Antalet klick dividerat med antalet visningar för en annons. Annonser som är mest relevanta för sökfrågan har den högsta klickfrekvensen.

**klicknings-tracking-URL:** En spårningsmall eller en mål-URL med inbäddad kod för att spåra klick på ett nyckelord, en annonsvariation eller en placering.

**begränsning:** (annonsörer med portföljer; gäller endast för budenheter i standardportföljer) En regel för budgivning för ett specifikt nyckelord eller en viss annons. Det åsidosätter eventuella begränsningar på portföljnivå och den rekommenderade anbudsstrategin.

**konvertering:** Slutförande av en åtgärd efter att en slutanvändare har klickat på en annons, som vanligtvis fångas in som ett mått. Exempel är registreringar och inköp, och de kan representera antal eller monetära belopp. En konvertering kan bestå av en eller flera transaktionshändelser, men termerna &quot;konvertering&quot; och &quot;transaktion&quot; används ofta utan åtskillnad.

**konverteringsspårning:** Konverteringsspårning använder cookies för att spåra a) klickningar på en annonsörs annonser i annonsnätverket och b) de resulterande transaktionerna på annonsörens webbplats.

**kostnadseffektivitet:** (annonsörer med portföljer) Den faktiska utgiften för en portfölj dividerat med de prognostiserade utgifterna. [Modellnoggrannhetsrapporter](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indikerar noggrannheten för de kostnadsmodeller som används för optimering, och [[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) innehåller mer information förutom rekommendationer för att förbättra modellnoggrannheten.

**kostnadsmodell:** (annonsörer med portföljer) Search-, Social- och Commerce-teknik som förutser kostnadsvolym, vilket bud som krävs för att vinna varje position eller placering samt CPC (sökning) eller CPM (visning) för varje budenhet med hjälp av historiska data och matematiska prognostekniker.

**täckningsgrad för kostnadsmodell:** (annonsörer med portföljer) Antal och/eller procentandel av anbudsenheter i CPC- eller eCPC-kampanjer som har fått minst ett intryck de senaste sju dagarna så att optimeringsfunktionen kan skapa kostnadsmodeller. Inte alla budenheter har kostnadsmodeller; budenheterna med kostnadsmodeller räknas in i kostnadsmodellens täckning.

**halveringstid för kostnadsmodell:** (annonsörer med portföljer) Antal dagar före det aktuella datumet för vilket kostnadsdata anses vara nyare och därför mer relevanta för kostnadsmodeller.

**kostnad per 1 000 visningar:** (CPM) Kostnaden för en annons för varje tusen visningar. Annonsörer som använder en CPM-prismodell betalar med visningar i stället för med klick.

**kostnad per förvärv:** (CPA) Kostnaden för en annons dividerat med antalet konverteringar. Kallas också kostnad per transaktion (CPT) eller kostnad per order (CPO).

**kostnad per klick:** (CPC) 1) Kostnaden för en annons dividerat med det totala antalet klick för annonsen. Om du till exempel spenderar 100 USD för ett annonsintryck och annonsen genererar 10 klick blir kostnaden per klick 100 USD/10=10 USD per klick. 2) En prismodell där annonsörer debiteras för varje reklamklick.

**kostnad per order:** (CPO) Kostnaden för en annons dividerat med antalet order. Kallas också kostnad per förvärv (CPA) eller kostnad per transaktion (CPT).

**kostnad per transaktion:** (CPT) Kostnaden för en annons dividerat med antalet transaktioner. Kallas också kostnad per förvärv (CPA).

**CPA:** Se&quot;kostnad per förvärv&quot;.

**CPC:** Se&quot;kostnad per klick&quot;.

**CPM:** Se&quot;kostnad per 1 000 visningar&quot;.

**CPO:** Se&quot;kostnad per order&quot;.

**CPT:** Se&quot;kostnad per transaktion&quot;.

**CSV:** Ett filformat som består av kommaavgränsade värden (CSV).

**CTR:** Se klickfrekvens.

## E-F {#e-f}

**eCPM:** Den effektiva CPM-modulen, eller den genomsnittliga kostnad som betalas per 1 000 visningar under ett angivet datumintervall. eCPM-värden kan beräknas för CPM- eller CPC-kampanjer.

## G-H {#g-h}

**halveringstid:** Den tid som krävs för en kvantitet att minska till hälften av det ursprungliga värdet. För varje portfölj kan du ange halveringstider för att ange hur lång information som är relevant för kostnadsmodeller och intäktsmodeller.
Se&quot;kostnadsmodellens halveringstid&quot; och&quot;intäktsmodellens halveringstid&quot;.

## I-J {#i-j}

**intryck:** En enskild annonsvisning på en webbsida, i en mobilapp eller i ett annat leveransmedium. Användaren behöver inte visa eller klicka på annonsen för att den ska räknas som ett intryck.

**visningsfönstret:** (Endast för displaykampanjer och sociala kampanjer) En inställning på annonsnivå som anger antalet dagar efter att ett annonsintryck inträffar som gör att intrycket kan tillskrivas en konvertering.

**visningsåsidosättningsvikt:** En angiven procentandel av ett konverteringsvärde som ska tilldelas till avbildningar som inträffar i klientens visningsfönster när konverteringen föregås av både betalda klick och visningar. När en konvertering föregås av endast visningar används annonsörens genomsiktsvikt, i stället för att tryckningen åsidosätter vikten, på tryckningarna.

## K-L {#k-l}

**nyckelord:** Ett ord eller en fras som är associerad med en annons.

**nyckelordsbegränsning:** Se &quot;begränsning&quot;.

**etikettklassificering:** Ett sätt att gruppera dina kontokomponenter i meningsfulla uppsättningar. En etikettklassificering kan innehålla flera etikettvärden, som anger attribut. En&quot;Geo&quot;-etikettklassificering kan till exempel innehålla värden för olika geografiska regioner.

**label-värde:** Ett element i en etikettklassificering. Den kan tilldelas som en tagg för annonskampanjer och kampanjentiteter så att ni kan filtrera resultatdata och rapporter efter etikett eller konfigurera valfria begränsningar för budenheter som är kopplade till etiketten.

**URL för landningssida:** URL:en för annonserarens webbsida som öppnas när slutanvändaren klickar på en annons.

## M-N {#m-n}

**marginalkostnad:** Förändringen i totalkostnad när kvantiteten ändras med en enhet.

**marginalvärde för kostnad-till-mål:** Den kostnadsförändring som krävs för att öka det objektiva värdet med ett (1). Detta har samma värde som den gamla kolumnen Marginal Cost-to-Revenue.

**matchningstyp:** Ett alternativ som anger hur söktermer matchas mot annonser. Alternativen varierar beroende på annonsnätverk.

**minsta bud:** 1) Det minsta belopp som ska betalas per intryck eller per 1 000 visningar. 2) För söknyckelord, det minsta bud som krävs för ett visst nyckelord baserat på dess kvalitetspoäng. Det lägsta anbudet är vanligtvis det minsta belopp som du kan betala per klick för att visa annonser för nyckelordet.

**modellprecision:** (annonsörer med portföljer) Procentandelen noggrannhet för de kostnadsmodeller och intäktsmodeller som används för att optimera anbud, kampanjbudgetar och anbudsstrategimål för en portfölj. Se&quot;kostnadsmodell&quot;,&quot;kostnadsnoggrannhet&quot;,&quot;intäktsmodell&quot; och&quot;intäktsnoggrannhet&quot;.  [Modellnoggrannhetsrapporter](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) anger att kostnads- och intäktsmodellerna är korrekta.

## O-P {#o-p}

**mål:** (annonsörer med portföljer) Ett mål som en kund ställer in för att uppfylla sitt affärsmål för en viss portfölj eller en annonskampanj, till exempel för att maximera vinsten eller för att uppfylla ett visst försäljningsmål. Ett mål består av de konverteringsmått som ska spåras och optimeras för portföljen samt de relativa vikterna för dessa mätvärden. De totala viktade konverteringarna för portföljen beräknas som &quot;objektivt värde&quot;.

**objektivt värde:** (annonsörer med portföljer) Den totala viktade konverteringen enligt portföljens aktuella mål, inklusive:

* alla konverteringar, med beaktande av a) de vikter som tilldelats varje konvertering i portföljens mål och, i tillämpliga fall, b) genomsynvikten för hela visningen.

* alla klick, som optimeringsfunktionen anser vara en enda konvertering och viktas enligt klickvärdet för målet.

Detta har samma värde som den äldre kolumnen&quot;Viktad intäkt&quot;.

**optimeringsfunktion:** (annonsörer med portföljer) Nyckelordsbudgivningsteknik för sökning, sociala medier och Commerce, som avgör den optimala budgivnings- och budgethanteringsstrategin för en portfölj baserat på dess affärsmål.

**Överbliven transaktion:** En transaktionshändelse som inte kan associeras med ett visst nyckelord eller en viss annons.

**pixel:** En genomskinlig bild med en pixel i taget som är inbäddad på en webbsida för spårningsändamål. Taggar för spårning av konvertering mellan Adobe Advertising omfattar antingen en bildpixel i HTML eller JavaScript för att spåra klick och deras resulterande transaktioner.

**placering:** En plats i ett visningsnätverk där dina annonser kan visas. Det kan vara en hel webbplats, en delmängd av en webbplats eller en annonsposition på en viss sida.

**portfölj:** En uppsättning annonskampanjer och deras associerade budenheter, som är optimerade för ett enda affärsmål och ett prestationsmål.

**Kassaflöde:** procent av utgiften

**PPC:** Se&quot;Betala per klick&quot;.

**egenskap:** Se &quot;konverteringsmått&quot;.

**egenskapstid:** Den tidpunkt då en enskild konverteringshändelse inträffar. När en händelse innehåller relaterade uppföljningshändelser (som att kunden först registrerar sig för en kostnadsfri provperiod och senare prenumererar på en betaltjänst) har varje händelse en egen ägandetid.

## Q-R {#q-r}

**kvalitetspoäng:** Ett poängtal som ett annonsnätverk tilldelar något av dina nyckelord för att fastställa dess budpris och annonsposition. Det beräknas utifrån nyckelordets relevans för den associerade annonsen och användarens sökfråga, nyckelordets klickfrekvens och andra faktorer.

**omdirigerings-URL:** Del av en mål-URL som skickar användaren till en annan server före, eller i stället för, annonsörens landningssida.

**avkastning på investering:** (ROI) Intäkter minus kostnader.

**intäktsnoggrannhet:** (Annonsörer med portföljer) Den faktiska intäkten för en portfölj dividerat med den prognostiserade intäkten. [Modellens noggrannhetsrapporter](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) anger noggrannheten för intäktsmodellerna som används för optimering.

**intäktsmodell:** (annonsörer med portföljer) Search-, Social- och Commerce-teknik som beräknar konverteringsgraden och den beräknade avkastningen för varje budenhet, baserat på klickdata (sökdata och sociala medier) eller visningsdata (displaydata) och annonsörens konverteringsdata.

**intäktsmodelltäckning:** (annonsörer med portföljer) Antal och/eller procentandel av budenheter i en portfölj med intäktsmodeller. Anbudsenheterna kan ha intäktsmodeller även om de inte har fått några intäkter utan fått intäktsvisningar.

**halveringstid för intäktsmodell:** (annonsörer med portföljer) Det antal dagar före det aktuella datumet för vilket intäktsinformationen anses vara nyare och därför mer relevant för intäktsmodeller.

**ROI:** Se &quot;räntabilitet&quot;.

## S-T {#s-t}

**simulering:** (annonsörer med portföljer) Portfolio-modellering som uppskattar antalet klick och konverteringar som en portfölj kan förvänta sig för olika utgiftsnivåer och motsvarande dagliga budgetar, med hjälp av historiska data.

**utgiftsstrategi:** (annonsörer med portföljer) Den strategi som valts för att optimera budgivning via nyckelord/annonser för en portfölj.

**`s_kwcid`:** Se &quot;AMO ID&quot;.

**spårnings-URL:** En spårningsmall eller en mål-URL med extra parametrar tillagda för att spåra information om klickningar på annonsen. Den kan innehålla en omdirigerings-URL för att först skicka användare till en spårningsserver innan de dirigeras om till annonsörens landningssida.

**transaktion:** Alla spårbara händelser som inträffar online eller offline. Flera transaktionshändelser kan spåras tillsammans som en del av samma transaktion eller konvertering. Till exempel kan en onlinebegäran om information plus en resulterande beställning per telefon betraktas som en del av ett köp. Termerna &quot;transaktion&quot; och &quot;konvertering&quot; används ofta utan åtskillnad. En transaktion representeras av ett transaktions-ID och har en eller flera egenskaper kopplade till sig.

**transaktions-ID:** Ett annonsörspecificerat ID som identifierar en transaktion. När en transaktion innehåller flera händelser har alla samma transaktions-ID.

**transaktionsegenskap:** Se &quot;konvertering&quot;.

**transaktionstid:** Den tid då ett klick eller ett intryck konverteras till en transaktion. När en transaktion består av flera transaktionshändelser (t.ex. när en kund först registrerar sig för en kostnadsfri provperiod och senare prenumererar på en betaltjänst), kommer transaktionstiden från den första händelsen i kedjan (registrerar sig för den kostnadsfria provperioden).

**TSV:** Ett filformat som består av tabbseparerade värden (CSV).

## U-V {#u-v}

**visa-genom:** (annonser och annonser i sociala medier) Ett annonsintryck (eller en sträng med visningar) som resulterar i en konvertering utan att användaren klickar på en annons.

**genomsynlig vikt:** (endast för visnings- och sociala kampanjer) En inställning på annonsörnivå som anger vikten som ska tilldelas en genomsynskonvertering i förhållande till den vikt som tilldelats en klickbaserad konvertering, i procent.

## B-X {#w-x}

**viktat mål:** Se &quot;mål&quot;.

**viktad intäkt:** Se &quot;objektivt värde&quot;.

**XLS** eller **XLSX**: Ett binärt filformat för [!DNL Microsoft Office Excel]-arbetsböcker.

## Y-Z {#y-z}
