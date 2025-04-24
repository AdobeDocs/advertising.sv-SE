---
title: Placeringsinställningar
description: Se beskrivningar av tillgängliga placeringsinställningar.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 3224adf97a1b32ee7b7abcbb1c6e7792bfed5c49
workflow-type: tm+mt
source-wordcount: '4039'
ht-degree: 0%

---

# Placeringsinställningar

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Placeringsnamnet.

>[!TIP]
>Använd en namnkonvention som passar ditt sätt att arbeta. En föreslagen namnkonvention är &quot;*\&lt;kampanjnamn\>: \&lt;annonsenhet\>: \&lt;Varaktighet\>: \&lt;Målgrupp\>*&quot;.

**[!UICONTROL Status]:** Placeringsstatus: *[!UICONTROL Active]* (standard) eller *[!UICONTROL Paused]*.

>[!TIP]
>Det bästa sättet är att pausa placeringen tills du är redo att starta den.

**[!UICONTROL Details]:** (skrivskyddad) Den tillämpliga annonstypen, kontot som skapar eller skapade placeringen samt den överordnade kampanjen. Klicka på **[!UICONTROL Show more]** om du vill se mer information.

**[!UICONTROL Templates]:** Öppnar en lista över befintliga placeringsmallar. Så här fyller du i målinriktningsinställningar automatiskt från en mall:

1. Gör något av följande:

   * Om du vill återanvända alla mål från en mall markerar du kryssrutan bredvid mallnamnet.

   * Om du vill återanvända enskilda måltyper från en mall expanderar du mallnamnet och markerar kryssrutan bredvid de måltyper som du vill återanvända.

1. Klicka på **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Endast videoannonsformat) Specifikationerna för annonsens varaktighet och/eller annonsen, som används för att beräkna prognosprojektionen till höger. Fälten varierar beroende på annonstyp.

**[!UICONTROL Environment]:** (endast Universal Video-annonsformat) Enhetsmiljöer (Skrivbord, Mobil, Ansluten TV) som ska inkluderas som mål i placeringen. Ange minst en.

I anpassade rapporter anger placeringsnivådimensionen &quot;Enhetsmiljö&quot; målmiljön.

**[!UICONTROL Placement tags]:** (Valfritt) Nyckelord eller smeknamn som hjälper dig att hitta den här placeringen.

## Mål

**[!UICONTROL Package]:** (Valfritt) Ett paket som placeringen är tilldelad till. Klicka på ![Redigera](/help/dsp/assets/edit.png) om du vill välja ett befintligt paket eller skapa ett paket. När du tilldelar placeringen till ett paket uppdateras avsnittet [!UICONTROL Goals] med flygdatum, leveransmål och budget från paketet.

**[!UICONTROL Flight Dates]:** Startdatum och slutdatum för placeringen. Godkända annonser kan köras under flygningen när placeringen är aktiv och tilldelats ett aktivt paket eller en aktiv kampanj.

Datumen för paketet (om tillämpligt) eller kampanjen fylls i automatiskt som standard.

>[!NOTE]
>
>* Flightdatumen måste ingå i kampanjflygdatumen och paketflygdatumen.

### Placeringar tilldelade paket med paketnivåpacing

**[!UICONTROL Placement Funding]:** Så här budgeterar du placeringen:

* *[!UICONTROL Optimize based on performance]:* Styr budgeten på paketnivå.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Gör att du kan ange en minsta och/eller högsta placeringsbudget. Ange minst en typ av budget:

   * *[!UICONTROL Maximum Budget]*: Ange ett värde och varaktighet (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: Den minsta budgeten som en procentandel av paketbudgeten. När en intervallgräns anges beräknas alltid det minsta budgetvärdet som en procentandel av intervallgränsen. I annat fall beräknas den som en procentandel av paketbudgeten.

**[!UICONTROL Max Bid]:** Det högsta beloppet som kan betalas för 1 000 visningar.

**[!UICONTROL Placement Pre-bid Filters]:** Upp till fem KPI-trösklar (till exempel ett minsta visningsvärde eller klickfrekvens) som måste uppfyllas för att budgivning ska ske. Ni kan använda filter före bud som optimeringsstrategier, men förstå att varje regel kan begränsa de möjligheter som den här placeringen kan erbjuda. Så här lägger du till eller redigerar filter:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Välj ett mått bredvid **[!UICONTROL Only bid if]** och ange sedan ett värde.
   * Om du vill ta bort ett filter klickar du på **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

Se beskrivningar av varje pre-bid-filter på &quot;[Pre-Bid Filters på placeringsnivå och Använda dem](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Alla andra placeringar

**[!UICONTROL Budget Goal]:** Bruttobudgettak och budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Placeringar i kampanjer med endast marginalhantering) Bruttobudgettak och budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på [Optimeringsmål och Använda dem](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Target Goal]:** Målmålet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Pace on]:** Grundläggande för paketering:

* **[!UICONTROL Budget goal]:** (Standard) Det här alternativet ger så många avtryck som möjligt inom den allokerade budgeten.

* **[!UICONTROL Impressions]:** Det här alternativet levererar avbildningar tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Det högsta beloppet som kan betalas för 1 000 visningar.

**[!UICONTROL Flight pacing]:** (Endast placeringar på placeringsnivå) Så här placerar och levererar du annonser:

* *[!UICONTROL Even]:* (Standardvärdet) Placerar leveransen enhetligt under varje flygning, med målet 50 % av leveransen under den första halvan av flygningen.

* *[!UICONTROL Slightly Ahead]:* (standard) Accelererar leveransen så att den är 55-65 % färdig halvvägs genom flygningens varaktighet.

* *[!UICONTROL Frontload]:* Accelererar leveransen så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Accelererar leveransen så att den är 75-85 % färdig halvvägs genom flygningen.

**[!UICONTROL Intraday pacing]:** (Endast placeringar på placeringsnivå) Så här placerar och levererar du varje dag i flygningen:

* *[!UICONTROL Even]:* (standard) Skalar leverans baserat på lagertillgänglighet. I allmänhet levereras fler annonser per timme under dagtid, när auktionsvolymen är högre och färre annonser levereras under kvällarna och morgnarna.

* *[!UICONTROL ASAP]:* (standard) Accelererar leveransen till dubbelt så hög hastighet som *Even*.

  >[!CAUTION]
  >
  >Det här alternativet kan påverka prestandan negativt. Använd det bara när ni prioriterar leverans och utgifter framför prestandaoptimering.

**[!UICONTROL Placement Pre-bid Filters]:** (valfritt) Upp till fem filter som måste uppfyllas för att budgivning ska ske. Du kan använda filter före bud som optimeringsstrategier, men tänk på att varje regel kan begränsa de möjligheter som den här placeringen kan ge. Så här lägger du till eller redigerar filter:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Välj ett mått bredvid **[!UICONTROL Only bid if]** och ange sedan ett värde.
   * Om du vill ta bort ett filter klickar du på **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Valfritt) Specifika platser där annonser ska inkluderas eller exkluderas i placeringen. Om du inte anger några platser anges alla platser som mål.

>[!NOTE]
>
>Ort och DMA-platser är inte tillgängliga för Roku-ersättningar.

Så här anger du platser:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Inkludera eller exkludera ett land, en stat, en stad, DMA, ett federala lagstiftningsdistrikt eller ett statligt lagstiftningsdistrikt:
      1. Välj platstyp i den vänstra kolumnen.
      1. (Vid behov) Klicka på en plats för att expandera den.
      1. Klicka på *[!UICONTROL Include]* bredvid platsen om du vill inkludera den som ett mål eller *[!UICONTROL Exclude]* om du vill utesluta den som ett mål.
   * Så här söker du efter ett postnummer och inkluderar eller exkluderar alla valda resultat:
      1. Klicka på **[!UICONTROL Search Postal Code]**.
      1. Välj land.
      1. Ange stadsnamnet och klicka sedan på ![Redigera](/help/dsp/assets/search.png).
      1. Klicka på rätt sökresultat.
      1. Klicka på *[!UICONTROL Include All]* om du vill inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Så här anger eller klistrar du in postnummer och inkluderar eller exkluderar dem alla:
      1. Klicka på **[!UICONTROL Paste Postal Code]**.
      1. Välj land.
      1. Ange eller klistra in upp till 1 000 postnummer.
Inkludera ett postnummer per rad eller ange flera värden avgränsade med kommatecken eller tabbar.
      1. Klicka på *[!UICONTROL Include All]* om du vill inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Om du vill ta bort en plats från listan [!UICONTROL Included] eller [!UICONTROL Excluded] klickar du på **[!UICONTROL X]** bredvid platsen i den högra kolumnen.
1. Klicka på **[!UICONTROL Done]**.

>[!NOTE]
>
>* Alla länder har inte delstat, ort eller postnummer.
>* DMA (angivet marknadsområde), federala lagstiftningsdistrikt och statliga lagstiftningsdistrikt är endast tillgängliga i USA.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Lagerkällor som ska inkluderas eller exkluderas som mål. För de flesta placeringstyper inkluderas alla lagertyper och alla källor för varje typ som standard. För [!DNL Roku] placeringar måste du ange lagertyp och källor. Du kan välja mellan följande lagertyper:

* [!UICONTROL Public]: (Alla placeringstyper förutom Roku) Alla öppna valutalager som DSP har åtkomst till. Du kan inkludera och exkludera offentligt lager.

  Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödets namn, flödesknapp eller en vald egenskapstagg.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Dina befintliga privata avtal (eller befintliga privata [!DNL Roku] avtal för [!DNL Roku] praktik) med utgivare som du har konfigurerat i DSP. Du kan inkludera, men inte exkludera, offentligt lager.

  Du kan söka i listan efter nyckelord, nyckel, erbjudande-ID eller egen tagg.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Valfritt) Åsidosätter budprisalgoritmen för att lägga bud på minst de fasta och lägsta priserna för erbjudanden.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alla [ premiumerbjudanden, icke-garanterade [!UICONTROL On Demand] lager ](/help/dsp/inventory/on-demand-inventory-about.md) (eller [!UICONTROL On Demand] [!DNL Roku] erbjudanden för [!DNL Roku] praktik) som du prenumererar på [!DNL DSP]. Du kan inkludera och exkludera [!UICONTROL On Demand] lager.

  Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödesnamn, flödesknapp eller en vald utgivarregion, kategoritagg eller karakteristisk tagg.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Valfritt) Åsidosätter budprisalgoritmen för att lägga bud på minst de fasta och lägsta priserna för erbjudanden.

Så här anger du målinriktning för lager:

* Om du vill exkludera en lagertyp avmarkerar du kryssrutan bredvid namnet.
* Så här anger du en lagertyp som mål:
   1. Markera kryssrutan bredvid lagertypens namn.
   1. (Valfritt) Ändra källorna så att de omfattar:
      1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] och [!UICONTROL On Demand] lager) Klicka på **[!UICONTROL View by Source]** eller **[!UICONTROL View by Feed]** om du vill ändra hur källorna visas.
      1. (I tillämpliga fall) Filtrera lagret efter behov.
      1. Ange de källor som ska inkluderas och exkluderas:
         * Om du vill ta med en [!UICONTROL Public]- eller [!UICONTROL On Demand]-källa klickar du på **[!UICONTROL Include]** bredvid källnamnet.
         * Inkludera [!UICONTROL Private] källor:
            * Om du vill inkludera allt lager i ett avtal klickar du på **[!UICONTROL Include all]** bredvid avtalsnamnet.
            * Om du vill inkludera en enskild lagerkälla expanderar du avtalsnamnet och klickar sedan på kryssrutan bredvid källnamnet.
         * Om du vill exkludera en [!UICONTROL Public] eller [!UICONTROL On source] klickar du på **[!UICONTROL Exclude]** bredvid källnamnet.
   1. (Valfritt) Om du vill hämta en CSV-fil med målinformationen till hämtningsplatsen för din webbläsare klickar du på **[!UICONTROL Save & Export]**.
   1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>Om du prenumererade på [!UICONTROL On Demand]-lager men inte kan hitta de utgivare eller avtal som du vill rikta in dig på, kontrollerar du status för erbjudandena. Mer information om status finns i [Om [!DNL On Demand] Premiuminventering](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (endast videoplaceringar) Exkluderar trafik utanför strömmen.

Annonser utanför webben visas vanligtvis över innehållet som ett popup-fönster eller instoppat i innehåll (i den ursprungliga upplevelsen), i stället för som vanliga videoannonser i en videospelare.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** Typer av trafik som ska mål. Alternativen är **[!UICONTROL Websites]** och **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Kvaliteten på trafiken till målet. Nivåerna 1-3 är alla varumärkesskyddade och har godkänts av DSP kartteam.

* *[!UICONTROL Tier 1]:* Premium-webbplatser och -program som är nationellt identifierbara.

* *[!UICONTROL Tier 2]:* Målgrupp 1 samt kvalitetswebbplatser och program som är mindre kända än nivå 1.

* *[!UICONTROL Tier 3]:* Målgrupper för Tiers 1-2 plus legitima och varumärkessäkra webbplatser och program som passar en nischmålgrupp. Använd nivå 3 för målgruppsköp för räckvidd eller data.

* *[!UICONTROL All Sites or Apps]:* Målenheterna 1-3 och nytt lager som inte har säkerhetskontrollerats eller kategoriserats, som du kan använda för att nå.

>[!NOTE]
>
>Lagret är specifikt för annonsenheterna i placeringen.

>[!TIP]
>
>För prestandakampanjer är det bästa sättet att välja *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (Valfritt, tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatskategorier i de valda webbplatsnivåerna som antingen ska inkluderas eller exkluderas (men inte båda) som mål. Välj från lodräta listor över webbplatser som DSP har mappat baserat på ämne:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange de webbplatskategorier som ska inkluderas eller exkluderas:
   * Så här tar du med webbplatskategorier:
      1. Klicka på **[!UICONTROL Include categories]**.
      1. Markera kryssrutan bredvid varje kategori som du vill använda som mål.
   * Så här exkluderar du webbplatskategorier:
      1. Klicka på **[!UICONTROL Exclude categories]**.
      1. Markera kryssrutan bredvid varje kategori som ska uteslutas.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformationen till hämtningsplatsen för din webbläsare klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (Valfritt, tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatser som ska exkluderas. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Välj de webbplatser som ska uteslutas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid.
         * (När fler än 50 resultat är tillgängliga) Om du vill utesluta de första 50 resultaten klickar du på **[!UICONTROL Exclude these 50]**. Om du vill utesluta alla sökresultat klickar du på **[!UICONTROL Exclude these \<*N *\>]**.
   * Så här anger du domännamn:
      1. Klicka på **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Exclude All]**.
1. Klicka på **[!UICONTROL Done]** när du är klar.

>[!NOTE]
>
>* Listor med blockerade webbplatser på kontonivå och annonsörnivå används också, utöver DSP [globalt blockerade webbplatslista](/help/dsp/introduction/features/brand-safety-media-quality.md), som innehåller webbplatser som inte betraktas som säkra för annonser.
>* Blockerade webbplatslistor åsidosätter alltid målwebbplatslistor. Om en placering båda utesluter och innehåller samma mål för en annons, utesluts målet.

**[!UICONTROL Language]:** (Valfritt) Ett enda språk att rikta sig till.

**[!UICONTROL Site or App List Preview]:** (skrivskyddat) Alla målwebbplatser och blockerade webbplatser för placeringen.

Du kan också exportera listan med målwebbplatser och blockerade webbplatser som en kommaavgränsad värdefil (CSV). Om du vill exportera listan klickar du på **[!UICONTROL Export full site list]** och öppnar eller sparar sedan filen enligt webbläsarens normala procedur.

**[!UICONTROL Allow unscreened sites]:** (Endast standardbildskärmsplaceringar) Aktiverar annonsleverans på webbplatser som inte är granskade. När placeringen avser privat lager kan det här alternativet leverera annonser på blockerade webbplatser.

**[!UICONTROL Paste list of targeted sites]:** Gör att du bara kan ange specifika webbplatser som mål. När du aktiverar det här alternativet inaktiveras de andra alternativen för webbplatsanpassning.

**[!UICONTROL Sites]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL On]*) Webbplatser att rikta till. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Markera de webbplatser som ska inkluderas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid.
         * (När fler än 50 resultat är tillgängliga) Om du vill inkludera de första 50 resultaten klickar du på **[!UICONTROL Include these 50]**. Om du vill inkludera alla sökresultat klickar du på **[!UICONTROL Include these \<*N *\>]**.
   * Så här anger du domännamn:
      1. klicka på **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Include All]**.
1. Klicka på **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alla målgrupper för placeringen, inklusive [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för alla valda segment och sparade målgrupper visas också. Du kan välja en befintlig målgrupp, skapa en målgrupp som du kan återanvända senare eller välja specifika målgruppssegment:

* Om du vill välja en befintlig målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) bredvid [!UICONTROL Included Audiences] och väljer målgrupp.
* Om du vill skapa en målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) bredvid [!UICONTROL Included Audiences] och väljer sedan **[!UICONTROL + Create Audience]**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md) med början från steg 3.
* Om du vill markera specifika målgruppssegment klickar du på **[!UICONTROL Select segments for this placement only]**. Välj segmentlogik. Instruktioner finns i steg 6 i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md). Klicka på **Spara** när du är klar.

**[!UICONTROL Excluded Audiences]:** Alla målgrupper som ska uteslutas för placeringen, inklusive målgrupper med [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för alla uteslutna målgrupper visas också. Du kan välja en befintlig målgrupp eller skapa en ny som du kan återanvända senare:

* Om du vill välja en befintlig målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) bredvid [!UICONTROL Excluded Audiences] och väljer målgrupp.

* Om du vill skapa en målgrupp klickar du på ![Markera](/help/dsp/assets/chevron-down.png) bredvid [!UICONTROL Excluded Audiences] och väljer sedan **+ Skapa målgrupp**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md) med början från steg 3.

**[!UICONTROL Targeting]:** De typer av användar-ID som ska anges som mål. Du kan inte ändra den här inställningen efter att placeringen är aktiv (det vill säga efter att flygningen har börjat).

När du väljer både äldre ID:n och universella ID:n ges budgivningsinställningar till universella ID:n.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (Standard) Målsätter användare baserat på deras cookies, ID:n för mobilannonsering eller CTV-ID:n (connected TV). ID:n väljs baserat på webbläsaren, appen eller CTV-inventeringen.

* *[!UICONTROL Universal ID Beta]*: Målgruppsinriktade ID:n för användarintegritet. Välj en ID-typ. De tillgängliga alternativen bestäms av de valda geografiska målen i avsnittet [!UICONTROL Geo-Targeting]. Använd med [[!DNL RampID] segment som importerats direkt till DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segment för vilka DSP konverterar din PII till universella ID](/help/dsp/audiences/sources/source-about.md) eller [anpassade segment som spårar universella ID](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: Mål för [!DNL ID5]-ID:n har skapats med sannolikhet från e-postadresser och andra signaler.<!-- What countries/geos are these available for? Everywhere?--> ID5-ID:n är tillgängliga utan kostnad. **Obs!** Tredjepartssegment från [!DNL Eyeota] kan innehålla ID5-ID:n.

   * *[!UICONTROL RampID]*: Målgrupper [!DNL LiveRamp] [!DNL RampIDs] för användare som har loggat in på webbplatsen med sina e-postadresser.<!-- Verify --> [!DNL RampIDs] är tillgängligt för användare i Nordamerika, Australien och Nya Zeeland.

   * *[!UICONTROL Unified ID2.0]*: Mål-ID [!DNL Unified ID2.0] (UID2) för användare som är inloggade på webbplatsen med sina e-postadresser.<!-- Verify -->[!DNL UID2 IDs] är inte tillgängligt för användare i EES och vissa andra länder. Se [listan över förbjudna länder](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: Villkoren i serviceavtalet för användning av universella ID:n. Du eller en annan användare på DSP-kontot måste acceptera villkoren en gång innan du kan konvertera data till en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren för din organisations räkning. Om du vill läsa villkoren klickar du på **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Tillgängligt när kampanjen [är konfigurerad för personbaserad målinriktning mellan enheter](/help/dsp/campaign-management/campaigns/campaign-settings.md), du anger endast äldre ID:n (inte universella ID:n) som mål och du väljer minst ett segment eller en målgrupp. Gör att du kan utöka målanpassningen för alla kända enheter (enligt enhetsdiagrammet som anges i kampanjinställningarna), även enheter som inte finns i de angivna segmenten. Avgifterna kan tillkomma beroende på vilket diagram som har angetts för kampanjen. Enhetsdiagramdata är bara tillgängliga i Nordamerika.

**[!UICONTROL Placement Cap]:** (Valfritt) Det antal gånger som en unik enhet, ett universellt ID eller en person (beroende på den angivna [!UICONTROL Cross Device Level] för kampanjen och placeringens [!UICONTROL Targeting]-inställning) kan hanteras annonser från placeringen. Alternativen är *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Secondary Cap]:** (Valfritt, tillgängligt när du inkluderar en numerisk [!UICONTROL Placement Cap]) En ytterligare begränsning inom gränserna för den primära placeringshöljet. Välj antalet visningar och tidsperioden (t.ex. 3 per 12 timmar).

**[!UICONTROL Day Parting]:** (Valfritt) Specifika dagar i veckan och vid vilken tidpunkt annonserna kan köras. Så här anger du dagdelningsintervall:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Välj tillämplig tidszon.
1. Ange intervallen:
   * Om du vill välja ett förinställt intervall klickar du på någon av intervallknapparna. Alternativen är *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* eller *[!UICONTROL Prime]* (primetime).
   * Om du vill markera ett intervall manuellt klickar du inuti en cell och väljer intervallet genom att dra.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Valfritt, tillgängligt för annonsörer som konfigurerats med [!DNL Proximic by Comscore] segment) Specifika segmentnamn eller ID:n från [!DNL Proximic by Comscore] som ska inkluderas som mål. Ytterligare avgifter kan tillkomma för den här funktionen. Om du vill aktivera den här funktionen och konfigurera ämnessegment kontaktar du ditt Adobe-kontoteam.

Så här anger du målinriktning:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange de segment som ska målas:
   1. I den vänstra kolumnen väljer du partner: (*[!UICONTROL Comscore]*).
   1. Ange segmentnamnen eller segmentens ID:n i indatafältet.
1. (Valfritt) Klicka på **[!UICONTROL Export]** om du vill hämta en CSV-fil med ämnesinformationen till hämtningsplatsen för din webbläsare.
1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>* Ämnesinriktningen begränsar det lager där placeringen kan offereras, så använd Ämnesanpassning för endast en liten andel av hela köpet.
>
>* Ställ in negativ målinriktning inom segmentet på [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (Valfritt) Specifik enhetsinformation, inklusive enhetstyper, tillverkare, operativsystem, webbläsare och anslutningstyper, som ska inkluderas och exkluderas som mål. Typerna varierar beroende på placeringstyp. Så här anger du målinriktning:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange den enhetsinformation som ska inkluderas och exkluderas:
   1. Välj kategori i den vänstra kolumnen.
   1. Ange mål:
      * Om du vill ta med ett värde klickar du på **[!UICONTROL Include]** bredvid värdenamnet.
      * Om du vill exkludera ett värde klickar du på **[!UICONTROL Exclude]** bredvid värdenamnet.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformation för enheten till hämtningsplatsen för din webbläsare klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Valfritt) Specifika Internetleverantörer (ISP) som antingen ska inkluderas eller exkluderas (men inte båda) som mål. Så här anger du ISP-mål:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Ange vilka Internet-leverantörer som ska inkluderas eller exkluderas:
   * Inkludera Internet-leverantörer:
      1. Klicka på **[!UICONTROL Include ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska användas som mål.
   * Så här exkluderar du Internet-leverantörer:
      1. Klicka på **[!UICONTROL Exclude ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska uteslutas.
1. (Valfritt) Klicka på **[!UICONTROL Export]** om du vill hämta en CSV-fil med målinformation från Internet-leverantören till nedladdningsplatsen för din webbläsare.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Valfritt; endast [!DNL DoubleVerify] kunder; endast tillgängligt för pre-roll-dator, standard- och click-to-play-visning och inbyggda visnings- och videopresentationer; stöds inte för [standardplaceringar för programmatiska erbjudanden](/help/dsp/inventory/programmatic-guaranteed-about.md)) Ett [!DNL DoubleVerify Authentic Brand Safety] segment-ID som är associerat med organisationens [!DNL DoubleVerify]-konto som ska användas för placeringen. Om du anger ett ID-block hämtas efter bud med hjälp av anpassade varumärkessäkerhetsregler som konfigurerats för det angivna segment-ID:t. DSP debiterar ditt konto för användning av segment-ID.

ID:t måste börja med &quot;51&quot; och bestå av åtta siffror. Som standard anges ett segment-ID i inställningarna för annonserarkontot, men du kan ändra ID:t så att det använder ett annat segment eller ta bort ID:t för att inaktivera funktionen.

**[!UICONTROL Contextual filtering]:** (Gäller för webbreklam för datorer och mobila enheter, inbyggda annonser och videoannonser) Typer av [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39] kontextfilter som ska användas. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerkontext som ska blockeras som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]:

   * **Målplatser som är:** (valfritt) En eller flera typer av lagerattribut att ange som mål som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL ComScore]:

   * **Blockera platser som är:** (valfritt) En eller flera typer av lagerattribut att blockera som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Valfritt) Graden av vuxeninnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]* eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Alcohol Content]:** (Valfritt) Den grad av alkoholinnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]* eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Pre-bid fraud blocking]:** Typer av webbplatser som ska blockeras baserat på bedräglig trafik och misstänkta aktiviteter som mäts via [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39]. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

* [!UICONTROL DoubleVerify]: (Gäller för webb- och mobilskärmar, inbyggda annonser och videoannonser) <!-- native, video, and standard connected TV ads -->

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Som standard blockerar all 100 % ogiltig trafik, inklusive trafik på kapade enheter, för nya platser. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Also block sites with]:** (Valfritt) En extra nivå av bedrägeri och ogiltig trafik som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar ytterligare trafik), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* eller *[!UICONTROL >25% Average Fraud/IVT levels]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]: (Gäller för webb- och mobilskärmar, inbyggda annonser och videoannonser)

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av bedrägeri som gör att DSP blockerar annonser som standard: *[!UICONTROL Fraud]* (som blockerar alla webbplatser med bedrägeri), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* och/eller *[!UICONTROL Fraud: Zero Ads]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]: (Gäller för webb- och mobilskärmar, inbyggda annonser och videoannonser)

   * **[!UICONTROL Block sites that are]:** (Valfritt) En typ av misstänkt webbplats- eller appaktivitet som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar annonser baserat på misstänkt aktivitet), *[!UICONTROL Suspicious Activity - High Risk]* eller *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Pre-bid viewability]:** (Gäller för webb-, webb-, webb- och videoannonser på datorer och mobila enheter) Vilka visningsfilter före bud som ska användas av [!DNL DoubleVerify] och [!DNL Integral Ad Science] för placeringen. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Ads.txt filtering]:** (Gäller för webb-, webb-, video- och ljudannonser på datorer och mobila enheter) Vilken nivå av förfiltrering av [Ads.txt](https://iabtechlab.com/ads-txt-about/) som ska användas genom att tillämpa varje utgivares lista över auktoriserade digitala säljare. Standardvärdet på annonsörnivå är valt för nya placeringar, men du kan ändra inställningarna:

* *[!UICONTROL Opt out of ads.txt (default)]*: Om du vill köpa lager från alla säljare.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: För att prioritera inköp av lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Om du bara vill köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Om du bara vill köpa lager från en domäns auktoriserade direktförsäljare.

**[!UICONTROL Attention Targeting]:** (Gäller för webb- och mobilskärmar, video och vanliga anslutna TV-annonser) [!DNL Adelaide] Målgrupper med en specifik prioritetsnivå (hög, medel eller låg) baserat på den angivna webbplatsen, formatet och annonsstorleken. Segmenten uppdateras varje vecka. **Obs!** Om du använder [!DNL Adelaide] segment för målinriktning debiteras en CPM-avgift för varje intryck som skickas med [!DNL Adelaide] uppmärksamhet riktad mot. Den här avgiften är separat från avgifterna för [målinriktningen](/help/dsp/campaign-management/campaigns/campaign-settings.md). För interaktiva före-rollplaceringar debiteras du endast för VAST-visningar.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] placeringar) Tredjepartsspårningsleverantörer som godkänts av [!DNL Roku] omfattar [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] och [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Valfritt) Tredjepartspixlar för händelsespårning som ska bifogas som standard till alla nya annonser i placeringen. Så här anger du händelsepixlar:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Pixel name]:** Pixelnamnet. Den maximala längden är 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Pixel event fires on]:** Händelsen som utlöser pixeln att utlösa. Vilka händelser som är tillgängliga varierar beroende på annonstyp.
         * **[!UICONTROL Pixel type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil), *[!UICONTROL HTML]* eller *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Pixelbildens URL.
      1. Klicka på **[!UICONTROL Create and attach]**.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Valfritt) Konverteringsspårningspixlar som ska bifogas som standard till alla nya annonser i placeringen. Så här anger du konverteringspixlar:

1. Klicka på ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Conversion pixel name]:** Pixelnamnet. Den maximala längden är 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Conversion category]:** Typ av konvertering.
         * **[!UICONTROL Impression conversion window]:** Det antal dagar efter att ett annonsintryck inträffar där intrycket kan tillskrivas en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Click conversion window]:** Det antal dagar efter en annonsklickning som klickningen kan tilldelas till en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Notes]:** (Valfritt) En beskrivning eller annan information om pixeln.
      1. Klicka på **[!UICONTROL Create and attach]**.
      1. Implementera konverteringspixeln på relevanta webbsidor:
         1. Gå till **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]** på huvudmenyn.
         1. Klicka på **[!UICONTROL edit]** i pixelraden.
         1. Kopiera värdena i fälten [!UICONTROL HTML Tag] och [!UICONTROL Flash Tag] efter behov för att förse annonsören eller webbplatskontakten.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per 1 000 visningar. Standardvärdet på paketnivå används automatiskt för nya placeringar, om det är tillämpligt, såvida du inte anger ett annat värde.

>[!NOTE]
>
>Fakturerbara avgifter visas i måttet [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [Om placeringshantering](placement-about.md)
>* [Skapa en placering](placement-create.md)
>* [Redigera placeringar](placement-edit.md)
>* [Hantera aktivitetsmultiplikatorer för placeringar](placement-manage-bid-multipliers.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Kortkommandon](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Vanliga frågor om kampanjhantering](/help/dsp/campaign-management/faq-campaign-management.md)
