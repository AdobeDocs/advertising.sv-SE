---
title: Placeringsinställningar
description: Se beskrivningar av tillgängliga placeringsinställningar.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: e2eca3b77882716c15fc3cde331d211efcd3fb8a
workflow-type: tm+mt
source-wordcount: '3858'
ht-degree: 0%

---

# Placeringsinställningar

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Placeringsnamnet.

>[!TIP]
>Använd en namnkonvention som passar ditt sätt att arbeta. En föreslagen namnkonvention är &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** Placeringsstatus: *[!UICONTROL Active]* (standard) eller *[!UICONTROL Paused]*.

>[!TIP]
>Det bästa sättet är att pausa placeringen tills du är redo att starta den.

**[!UICONTROL Details]:** (Skrivskyddat) Den tillämpliga annonstypen, det konto som skapar eller skapade placeringen samt den överordnade kampanjen. Om du vill visa mer information klickar du på **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Öppnar en lista över befintliga placeringsmallar. Så här fyller du i målinriktningsinställningar automatiskt från en mall:

1. Gör något av följande:

   * Om du vill återanvända alla mål från en mall markerar du kryssrutan bredvid mallnamnet.

   * Om du vill återanvända enskilda måltyper från en mall expanderar du mallnamnet och markerar kryssrutan bredvid de måltyper som du vill återanvända.

1. Klicka på **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Endast videoannonsformat) Specifikationerna för annonsens varaktighet och/eller annonsen, som används för att beräkna prognosprojektionen till höger. Fälten varierar beroende på annonstyp.

**[!UICONTROL Environment]:** (Endast Universal Video-annonsformat) De enhetsmiljöer (stationär dator, mobil, ansluten TV) som ska ingå som mål i placeringen. Ange minst en.

I anpassade rapporter anger placeringsnivådimensionen &quot;Enhetsmiljö&quot; målmiljön.

**[!UICONTROL Placement tags]:** (Valfritt) Nyckelord eller smeknamn som hjälper dig att hitta den här placeringen.

## Mål

**[!UICONTROL Package]:** (Valfritt) Ett paket som placeringen är tilldelad till. Klicka ![Redigera](/help/dsp/assets/edit.png) om du vill välja ett befintligt paket eller skapa ett paket. När du tilldelar ett paket placeringen [!UICONTROL Goals] -avsnittet uppdateras med flygdatum, leveransmål och budget från paketet.

**[!UICONTROL Flight Dates]:** Startdatum och slutdatum för placeringen. Godkända annonser kan köras under flygningen när placeringen är aktiv och tilldelats ett aktivt paket eller en aktiv kampanj.

Datumen för paketet (om tillämpligt) eller kampanjen fylls i automatiskt som standard.

>[!NOTE]
>
>* Flightdatumen måste ingå i kampanjflygdatumen och paketflygdatumen.

### Placeringar tilldelade paket med paketnivåpacing

**[!UICONTROL Placement Funding]:** Så här budgeterar du placeringen:

* *[!UICONTROL Optimize based on performance]:* Styr budgeten på paketnivå.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Gör att du kan ange en minimal och/eller maximal placeringsbudget. Ange minst en typ av budget:

   * *[!UICONTROL Maximum Budget]*: Ange ett värde och längden (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: Den minsta budgeten som en procentandel av paketbudgeten. När en intervallgräns anges beräknas alltid det minsta budgetvärdet som en procentandel av intervallgränsen. I annat fall beräknas den som en procentandel av paketbudgeten.

**[!UICONTROL Max Bid]:** Maximalt för 1 000 visningar.

**[!UICONTROL Placement Pre-bid Filters]:** Upp till fem KPI-trösklar (t.ex. ett minsta visbarhetsmått eller klickfrekvens) som måste uppfyllas för att budgivning ska ske. Ni kan använda filter före bud som optimeringsstrategier, men förstå att varje regel kan begränsa de möjligheter som den här placeringen kan erbjuda. Så här lägger du till eller redigerar filter:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Nästa till **[!UICONTROL Only bid if]**, väljer ett mått och anger sedan ett värde.
   * Om du vill ta bort ett filter klickar du **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

Se beskrivningar av varje pre-bid-filter på &quot;[Pre-Bid-filter på placeringsnivå och Så här använder du dem](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Alla andra placeringar

**[!UICONTROL Budget Goal]:** Bruttobudgetens övre gräns och budgetintervallet (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Placeringar i kampanjer med endast marginalledning) Bruttobudgetens övre gräns och budgetintervallet (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på &quot;[Optimeringsmål och Så här använder du dem](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Målet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Pace on]:** Basen för pacing:

* **[!UICONTROL Budget goal]:** (Standard) Det här alternativet ger så många avtryck som möjligt inom den tilldelade budgeten.

* **[!UICONTROL Impressions]:** Det här alternativet ger avtryck tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Maximalt för 1 000 visningar.

**[!UICONTROL Flight pacing]:** (Placeringar med enbart placering på placeringsnivå) Så här lägger du ut annonser:

* *[!UICONTROL Even]:* (Standardvärdet) Gör leveransen enhetlig under varje flygning, med ett mål på 50 % av leveransen under den första halvan av flygningen.

* *[!UICONTROL Slightly Ahead]:* (Standard) Ökar leveranstiden så att den är 55-65 % färdig halvvägs genom hela flygtiden.

* *[!UICONTROL Frontload]:* Snabbare leverans så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Snabbare leverans så att den är 75-85 % klar halvvägs genom flygningen.

**[!UICONTROL Intraday pacing]:** (Endast placeringar med placeringsnivåpaketering) Så här använder du jämna mellanrum och leverans för varje dag i flygningen:

* *[!UICONTROL Even]:* (Standard) Skalar leverans baserat på lagertillgänglighet. I allmänhet levereras fler annonser per timme under dagtid, när auktionsvolymen är högre och färre annonser levereras under kvällarna och morgnarna.

* *[!UICONTROL ASAP]:* (Standard) Accelererar leveransen till dubbelt så snabbt som *Jämn*.

  >[!CAUTION]
  >
  >Det här alternativet kan påverka prestandan negativt. Använd det bara när ni prioriterar leverans och utgifter framför prestandaoptimering.

**[!UICONTROL Placement Pre-bid Filters]:** (Valfritt) Upp till fem filter måste uppfyllas för att budgivning ska ske. Du kan använda filter före bud som optimeringsstrategier, men tänk på att varje regel kan begränsa de möjligheter som den här placeringen kan ge. Så här lägger du till eller redigerar filter:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Nästa till **[!UICONTROL Only bid if]**, väljer ett mått och anger sedan ett värde.
   * Om du vill ta bort ett filter klickar du **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Valfritt) Specifika platser där annonser ska inkluderas eller exkluderas i placeringen. Om du inte anger några platser anges alla platser som mål.

>[!NOTE]
>
>Ort och DMA-platser är inte tillgängliga för Roku-ersättningar.

Så här anger du platser:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Inkludera eller exkludera ett land, en stat, en stad, DMA, ett federala lagstiftningsdistrikt eller ett statligt lagstiftningsdistrikt:
      1. Välj platstyp i den vänstra kolumnen.
      1. (Vid behov) Klicka på en plats för att expandera den.
      1. Klicka på bredvid platsen *[!UICONTROL Include]* för att inkludera det som ett mål eller *[!UICONTROL Exclude]* för att exkludera den som ett mål.
   * Så här söker du efter ett postnummer och inkluderar eller exkluderar alla valda resultat:
      1. Klicka på **[!UICONTROL Search Postal Code]**.
      1. Välj land.
      1. Ange stadsnamnet och klicka sedan på ![Redigera](/help/dsp/assets/search.png).
      1. Klicka på rätt sökresultat.
      1. Klicka *[!UICONTROL Include All]* för att inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Så här anger eller klistrar du in postnummer och inkluderar eller exkluderar dem alla:
      1. Klicka på **[!UICONTROL Paste Postal Code]**.
      1. Välj land.
      1. Ange eller klistra in upp till 1 000 postnummer.
Inkludera ett postnummer per rad eller ange flera värden avgränsade med kommatecken eller tabbar.
      1. Klicka *[!UICONTROL Include All]* för att inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Ta bort en plats från [!UICONTROL Included] eller [!UICONTROL Excluded] lista, klicka på **[!UICONTROL X]** bredvid platsen i den högra kolumnen.
1. Klicka på **[!UICONTROL Done]**.

>[!NOTE]
>
>* Alla länder har inte delstat, ort eller postnummer.
>* DMA (angivet marknadsområde), federala lagstiftningsdistrikt och statliga lagstiftningsdistrikt är endast tillgängliga i USA.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Lagerkällor som ska inkluderas eller exkluderas som mål. För de flesta placeringstyper inkluderas alla lagertyper och alla källor för varje typ som standard. För [!DNL Roku] placeringar måste du ange lagertyp och källor. Du kan välja mellan följande lagertyper:

* [!UICONTROL Public]: (Alla placeringstyper utom Roku) Alla öppna valutalager som DSP har tillgång till. Du kan inkludera och exkludera offentligt lager.

  Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödets namn, flödesknapp eller en vald egenskapstagg.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Befintliga privata avtal (eller befintliga privata avtal) [!DNL Roku] erbjudanden för [!DNL Roku] ) med utgivare som du har konfigurerat i DSP. Du kan inkludera, men inte exkludera, offentligt lager.

  Du kan söka i listan efter nyckelord, nyckel, erbjudande-ID eller egen tagg.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Valfritt) Åsidosätter budprisalgoritmen för att lägga bud på åtminstone de fasta och lägsta priserna för erbjudanden.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alla [premie, ej garanterad [!UICONTROL On Demand] lager](/help/dsp/inventory/on-demand-inventory-about.md) (eller [!UICONTROL On Demand] [!DNL Roku] erbjudanden för [!DNL Roku] platser) som du prenumererar på [!DNL DSP]. Du kan inkludera och exkludera [!UICONTROL On Demand] lager.

  Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödesnamn, flödesknapp eller en vald utgivarregion, kategoritagg eller karakteristisk tagg.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Valfritt) Åsidosätter budprisalgoritmen för att lägga bud på åtminstone de fasta och lägsta priserna för erbjudanden.

Så här anger du målinriktning för lager:

* Om du vill exkludera en lagertyp avmarkerar du kryssrutan bredvid namnet.
* Så här anger du en lagertyp som mål:
   1. Markera kryssrutan bredvid lagertypens namn.
   1. (Valfritt) Ändra källorna så att de omfattar:
      1. Klicka ![Redigera](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] och [!UICONTROL On Demand] lager) Klicka på **[!UICONTROL View by Source]** eller **[!UICONTROL View by Feed]** om du vill ändra hur källorna visas.
      1. (I tillämpliga fall) Filtrera lagret efter behov.
      1. Ange de källor som ska inkluderas och exkluderas:
         * Ta med en [!UICONTROL Public] eller [!UICONTROL On Demand] källa, klicka på **[!UICONTROL Include]** bredvid källnamnet.
         * Inkludera [!UICONTROL Private] källor:
            * Om du vill inkludera allt lager i ett avtal klickar du **[!UICONTROL Include all]** bredvid avtalsnamnet.
            * Om du vill inkludera en enskild lagerkälla expanderar du avtalsnamnet och klickar sedan på kryssrutan bredvid källnamnet.
         * Så här exkluderar du [!UICONTROL Public] eller [!UICONTROL On source], klicka **[!UICONTROL Exclude]** bredvid källnamnet.
   1. (Valfritt) Om du vill hämta en CSV-fil med målinformation till hämtningsplatsen för webbläsaren klickar du på **[!UICONTROL Save & Export]**.
   1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>Om du prenumererar på [!UICONTROL On Demand] inventera men inte hitta de utgivare eller avtal som ska målgruppsanpassas, och kontrollera sedan status för erbjudandena. Mer information om status finns i [Om [!DNL On Demand] Premiumlager](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Endast videopappningar) Utesluter trafik utanför strömmen.

Annonser utanför webben visas vanligtvis över innehållet som ett popup-fönster eller instoppat i innehåll (i den ursprungliga upplevelsen), i stället för som vanliga videoannonser i en videospelare.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** De typer av trafik som ska mål. Alternativen inkluderar **[!UICONTROL Websites]** och **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Kvaliteten på de webbplatser som ska målas. Nivåerna 1-3 är alla varumärkessäkra och har godkänts av DSP.

* *[!UICONTROL Tier 1]:* Premium-sajter och -tillämpningar som är nationellt igenkännbara.

* *[!UICONTROL Tier 2]:* Målgrupper, nivå 1 samt webbplatser och tillämpningar av lägre kvalitet än nivå 1.

* *[!UICONTROL Tier 3]:* Målgrupper för Tiers 1-2 plus legitima och varumärkessäkra webbplatser och applikationer som passar en nischmålgrupp. Använd nivå 3 för målgruppsköp för räckvidd eller data.

* *[!UICONTROL All Sites]:* Målenheterna nivå 1-3 och nytt lager som inte har säkerhetskontrollerats eller kategoriserats, som du kan använda för att nå.

>[!NOTE]
>
>Lagret är specifikt för annonsenheterna i placeringen.

>[!TIP]
>
>För prestandakampanjer är det bästa sättet att välja *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Valfritt), tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatskategorier i de valda webbplatsnivåerna som antingen ska inkluderas eller exkluderas (men inte båda) som mål. Välj från lodräta listor med webbplatser som DSP har mappat utifrån ämne:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange de webbplatskategorier som ska inkluderas eller exkluderas:
   * Så här tar du med webbplatskategorier:
      1. Klicka på **[!UICONTROL Include categories]**.
      1. Markera kryssrutan bredvid varje kategori som du vill använda som mål.
   * Så här exkluderar du webbplatskategorier:
      1. Klicka på **[!UICONTROL Exclude categories]**.
      1. Markera kryssrutan bredvid varje kategori som ska uteslutas.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformation till hämtningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Valfritt), tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatser som ska uteslutas. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Välj de webbplatser som ska uteslutas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid.
         * (När fler än 50 resultat är tillgängliga) Om du vill utesluta de första 50 resultaten klickar du på **[!UICONTROL Exclude these 50]**. Om du vill utesluta alla sökresultat klickar du på **[!UICONTROL Exclude these \<*NN *\>]**.
   * Så här anger du domännamn:
      1. Klicka på **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Exclude All]**.
1. Klicka **[!UICONTROL Done]** när du är klar.

>[!NOTE]
>
>* Listor över blockerade webbplatser på kontonivå och annonsörnivå används också, utöver DSP [globalt blockerad webbplatslista](/help/dsp/introduction/features/brand-safety-media-quality.md), som innehåller webbplatser som inte anses säkra för annonser.
>* Blockerade webbplatslistor åsidosätter alltid målwebbplatslistor. Om en placering båda utesluter och innehåller samma mål för en annons, utesluts målet.

**[!UICONTROL Language]:** (Valfritt) Ett enda målspråk.

**[!UICONTROL Site List Preview]:** (Skrivskyddat) Alla målwebbplatser och blockerade webbplatser för placeringen.

Du kan också exportera listan med målwebbplatser och blockerade webbplatser som en kommaavgränsad värdefil (CSV). Om du vill exportera listan klickar du **[!UICONTROL Export full site list]** och sedan öppna eller spara filen enligt webbläsarens normala procedur.

**[!UICONTROL Allow unscreened sites]:** (Endast standardbildskärmsplaceringar) Aktiverar annonsleverans på webbplatser som inte är granskade. När placeringen avser privat lager kan det här alternativet leverera annonser på blockerade webbplatser.

**[!UICONTROL Paste list of targeted sites]:** Gör att du bara kan ange specifika webbplatser som mål. När du aktiverar det här alternativet inaktiveras de andra alternativen för webbplatsanpassning.

**[!UICONTROL Sites]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL On]*) Webbplatser att rikta sig till. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Markera de webbplatser som ska inkluderas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid.
         * (När det finns fler än 50 resultat) Om du vill ta med de första 50 resultaten klickar du på **[!UICONTROL Include these 50]**. Om du vill inkludera alla sökresultat klickar du på **[!UICONTROL Include these \<*NN *\>]**.
   * Så här anger du domännamn:
      1. klicka **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Include All]**.
1. Klicka på **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alla målgrupper för placeringen, inklusive [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för alla valda segment och sparade målgrupper visas också. Du kan välja en befintlig målgrupp, skapa en målgrupp som du kan återanvända senare eller välja specifika målgruppssegment:

* Om du vill välja en befintlig målgrupp klickar du ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Included Audiences]och sedan välja målgrupp.
* Om du vill skapa en målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Included Audiences]och sedan markera **[!UICONTROL + Create Audience]**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md), från steg 3.
* Om du vill markera specifika målgruppssegment klickar du på **[!UICONTROL Select segments for this placement only]**. Välj segmentlogik. Instruktioner finns i steg 6 i &quot;[Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md).&quot; När du är klar klickar du **Spara**.

**[!UICONTROL Excluded Audiences]:** Alla målgrupper som ska uteslutas för placeringen, inklusive målgrupper med [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för alla uteslutna målgrupper visas också. Du kan välja en befintlig målgrupp eller skapa en ny som du kan återanvända senare:

* Om du vill välja en befintlig målgrupp klickar du ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Excluded Audiences]och sedan välja målgrupp.

* Om du vill skapa en målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Excluded Audiences]och sedan markera **+ Skapa publik**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md), från steg 3.

**[!UICONTROL Targeting]:** De typer av användar-ID som ska anges som mål. Du kan inte ändra den här inställningen efter att placeringen är aktiv (det vill säga efter att flygningen har börjat).

När du väljer både äldre ID:n och universella ID:n ges budgivningsinställningar till universella ID:n.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (Standard) Målsätter användare baserat på deras cookies, ID:n för mobilannonsering eller CTV-ID:n (connected TV). ID:n väljs baserat på webbläsaren, appen eller CTV-inventeringen.

* *[!UICONTROL Universal ID Beta]*: Målgruppsinriktade ID:n för användarintegritet; välj en ID-typ. De tillgängliga alternativen avgörs av de valda geografiska målen i [!UICONTROL Geo-Targeting] -avsnitt. Använd med [[!DNL RampID] segment som importeras direkt till DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segment för vilka DSP konverterar din PII till universella ID](/help/dsp/audiences/sources/source-about.md), eller [anpassade segment som spårar universella ID:n](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: Målgrupper [!DNL ID5] ID:n har skapats med sannolikhet från e-postadresser och andra signaler.<!-- What countries/geos are these available for? Everywhere?--> ID5-ID:n är kostnadsfria. **Obs!** Tredjepartssegment från [!DNL Eyeota] kan innehålla ID5-ID.

   * *[!UICONTROL RampID]*: Målgrupper [!DNL LiveRamp] [!DNL RampIDs] av användare som är inloggade på webbplatsen med sina e-postadresser.<!-- Verify --> [!DNL RampIDs] är tillgängliga för användare i Nordamerika, Australien och Nya Zeeland.

   * *[!UICONTROL Unified ID2.0]*: Målgrupper [!DNL Unified ID2.0] (UID2) ID:n för användare som är inloggade på webbplatsen med sina e-postadresser.<!-- Verify -->[!DNL UID2 IDs] är inte tillgängliga för användare i Europeiska ekonomiska samarbetsområdet och vissa andra länder. Se [förteckning över förbjudna länder](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: Villkor för serviceavtal för användning av universella ID:n. Du eller en annan användare på DSP måste acceptera villkoren en gång innan du kan konvertera data till en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren å din organisations vägnar. Om du vill läsa villkoren klickar du **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Tillgängligt när [kampanjen är konfigurerad för personbaserad målinriktning på olika enheter](/help/dsp/campaign-management/campaigns/campaign-settings.md)målgruppsanpassas endast äldre ID:n (inte universella ID:n) och du väljer minst ett segment eller en målgrupp. Gör att du kan utöka målanpassningen för alla kända enheter (enligt enhetsdiagrammet som anges i kampanjinställningarna), även enheter som inte finns i de angivna segmenten. Avgifterna kan tillkomma beroende på vilket diagram som har angetts för kampanjen. Enhetsdiagramdata är bara tillgängliga i Nordamerika.

**[!UICONTROL Placement Cap]:** (Valfritt) Antalet gånger som en unik enhet, ett universellt ID eller person (beroende på den angivna [!UICONTROL Cross Device Level] för kampanjen och placeringen [!UICONTROL Targeting] inställning) kan hanteras med annonser från placeringen. Alternativen inkluderar *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Secondary Cap]:** (Valfritt; tillgängligt när du inkluderar en numerisk [!UICONTROL Placement Cap]) En ytterligare begränsning inom gränserna för det primära placeringsskyddet. Välj antalet visningar och tidsperioden (t.ex. 3 per 12 timmar).

**[!UICONTROL Day Parting]:** (Valfritt) Specifika veckodagar och klockslag då annonserna kan köras. Så här anger du dagdelningsintervall:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Välj tillämplig tidszon.
1. Ange intervallen:
   * Om du vill välja ett förinställt intervall klickar du på någon av intervallknapparna. Alternativen är *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, eller *[!UICONTROL Prime]* (primetime).
   * Om du vill markera ett intervall manuellt klickar du inuti en cell och väljer intervallet genom att dra.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Valfritt) tillgängligt för annonsörer som konfigurerats med [!DNL Proximic by Comscore] och [!DNL Oracle Data Cloud] segment) Specifika segmentnamn eller ID:n från [!DNL Proximic by Comscore] och [!DNL Oracle Data Cloud] (tidigare [!DNL Grapeshot]) som ska inkluderas som mål. Ytterligare avgifter kan tillkomma för den här funktionen. Om du vill aktivera den här funktionen och konfigurera ämnessegment kontaktar du kontoteamet på Adobe.

Så här anger du målinriktning:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange de segment som ska målas:
   1. Välj partner i den vänstra kolumnen (*[!UICONTROL Comscore]* eller *[!UICONTROL Grapeshot]*).
   1. Ange segmentnamnen eller segmentens ID:n i indatafältet.
1. (Valfritt) Om du vill hämta en CSV-fil med ämnesinformationen till din webbläsares hämtningsplats klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>* Ämnesinriktningen begränsar det lager där placeringen kan offereras, så använd Ämnesanpassning för endast en liten andel av hela köpet.
>
>* Ställ in negativ målgruppsanpassning inom segmentet på [!DNL Proximic by Comscore] eller [!DNL Oracle Data Cloud] (tidigare [!DNL Grapeshot]).

**[!UICONTROL Device Targeting]:** (Valfritt) Specifik enhetsinformation, inklusive enhetstyper, tillverkare, operativsystem, webbläsare och anslutningstyper, som ska inkluderas och exkluderas som mål. Så här anger du målinriktning:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange den enhetsinformation som ska inkluderas och exkluderas:
   1. Välj kategori i den vänstra kolumnen.
   1. Ange mål:
      * Om du vill ta med ett värde klickar du **[!UICONTROL Include]** bredvid värdenamnet.
      * Om du vill exkludera ett värde klickar du **[!UICONTROL Exclude]** bredvid värdenamnet.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformation för enheten till nedladdningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Valfritt) Specifika internetleverantörer (ISP) kan antingen inkludera eller exkludera (men inte båda) som mål. Så här anger du ISP-mål:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange vilka Internet-leverantörer som ska inkluderas eller exkluderas:
   * Inkludera Internet-leverantörer:
      1. Klicka på **[!UICONTROL Include ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska användas som mål.
   * Så här exkluderar du Internet-leverantörer:
      1. Klicka på **[!UICONTROL Exclude ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska uteslutas.
1. (Valfritt) Om du vill ladda ned en CSV-fil med information om internetleverantörens mål till nedladdningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Typer av [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39] kontextuella filter som ska användas. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerkontext som ska blockeras som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]:

   * **Målplatser som är:** (Valfritt) En eller flera typer av lagerattribut att rikta som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL ComScore]:

   * **Blockera webbplatser som är:** (Valfritt) En eller flera typer av lagerattribut att blockera som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Valfritt) Graden av vuxeninnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Alcohol Content]:** (Valfritt) Den alkoholhalt som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Pre-bid fraud blocking]:** Typer av webbplatser som ska blockeras baserat på bedräglig trafik och misstänkta aktiviteter som mäts via [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39]. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Som standard blockeras all 100 % ogiltig trafik, inklusive trafik på kapade enheter, för nya placeringar. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Also block sites with]:** (Valfritt) Ytterligare en nivå av bedrägeri och ogiltig trafik som gör att DSP blockerar annonser som standard:  *[!UICONTROL None]* (standard, som inte blockerar ytterligare trafik), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, eller *[!UICONTROL >25% Average Fraud/IVT levels]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av bedrägeri som får DSP att blockera annonser som standard: *[!UICONTROL Fraud]* (som blockerar alla webbplatser med bedrägeri), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* och/eller *[!UICONTROL Fraud: Zero Ads]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En typ av misstänkt webbplats- eller appaktivitet som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar annonser som baseras på misstänkt aktivitet), *[!UICONTROL Suspicious Activity - High Risk]*, eller *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Ads.txt filtering]:**

Vilken nivå av [Ads.txt](https://iabtechlab.com/ads-txt-about/) förfiltrera genom att tillämpa respektive utgivares lista över auktoriserade digitala säljare. Standardvärdet på annonsörnivå är valt för nya placeringar, men du kan ändra inställningarna:

* *[!UICONTROL Opt out of ads.txt (default)]*: För att köpa lager från alla säljare.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Att prioritera inköp av lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare.

**[!UICONTROL Attention Targeting]:** (Bildskärm, video, mobiler och vanliga TV-utplaceringar) Målgrupper [!DNL Adelaide] förbudssegment med en viss prioritetsnivå (hög, medel eller låg) baserat på den angivna platsen, formatet och annonsstorleken. Segmenten uppdateras varje vecka. **Obs!** Använda [!DNL Adelaide] segment för målinriktning får en CPM-avgift för varje intryck som levereras med [!DNL Adelaide] målinriktning; denna avgift är separat från avgifter för [noggrannhetsmätning](/help/dsp/campaign-management/campaigns/campaign-settings.md). För interaktiva före-rollplaceringar debiteras du endast för VAST-visningar.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Annonsörer konfigurerade med [!UICONTROL DoubleVerify Authentic Brand Safety] option) Aktiverar [!DNL DoubleVerify Authentic Brand Safety], som blockerar visningar efter bud med hjälp av anpassade varumärkessäkerhetsregler som konfigurerats för det angivna segment-ID:t. DSP fakturerar ditt konto för användning av det segment-ID som anges i annonserarens inställningar.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] placements) Tredjepartsleverantörer för spårning som godkänts av [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]och [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Valfritt) Pixlar för händelsespårning från tredje part som ska bifogas som standard till alla nya annonser i placeringen. Så här anger du händelsepixlar:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Pixel name]:** Pixelnamnet. Den maximala längden är 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Pixel event fires on]:** Den händelse som utlöser pixeln som utlöses. Vilka händelser som är tillgängliga varierar beroende på annonstyp.
         * **[!UICONTROL Pixel type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Pixelbildens URL.
      1. Klicka på **[!UICONTROL Create and attach]**.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Valfritt) Pixlar för konverteringsspårning som ska bifogas som standard till alla nya annonser i placeringen. Så här anger du konverteringspixlar:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Conversion pixel name]:** Pixelnamnet. Den maximala längden är 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Conversion category]:** Typ av konvertering.
         * **[!UICONTROL Impression conversion window]:** Det antal dagar efter det att ett annonsintryck inträffar där intrycket kan tillskrivas en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Click conversion window]:** Det antal dagar efter att ett annonsklick inträffar där klickningen kan kopplas till en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Notes]:** (Valfritt) En beskrivning eller annan information om pixeln.
      1. Klicka på **[!UICONTROL Create and attach]**.
      1. Implementera konverteringspixeln på relevanta webbsidor:
         1. Gå till huvudmenyn **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Klicka på **[!UICONTROL edit]**.
         1. Kopiera värdena i [!UICONTROL HTML Tag] och [!UICONTROL Flash Tag] fält, efter behov, som ska tillhandahållas annonsören eller webbplatskontakten.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per 1 000 visningar. Standardvärdet på paketnivå används automatiskt för nya placeringar, om det är tillämpligt, såvida du inte anger ett annat värde.

>[!NOTE]
>
>Faktureringsbara avgifter återspeglas i [!UICONTROL Net CPM] mätvärden.

>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Skapa en placering](placement-create.md)
>* [Redigera placeringar](placement-edit.md)
>* [Hantera budmultiplikationer för praktik](placement-manage-bid-multipliers.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Kortkommandon](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Frågor och svar om Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
