---
title: Bästa metoder för att konfigurera resultatkampanjer
description: Lär dig de bästa sätten att skapa prestandainriktade kampanjer, som bland annat innehåller placeringar som är optimerade för det lägsta CPA-värdet eller det högsta ROAS-värdet.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Bästa metoder för att konfigurera resultatkampanjer

DSP kan optimera era prestandainriktade kampanjer. Se följande metodtips för prestandakampanjer:

* Steg 1 - Definiera ditt mål
* Steg 2 - Definiera er strategi
* Steg 3 - Skapa paket
* Steg 4 - Skapa placeringsstruktur
* Steg 5 - Använd rätt kreativa Assets

## Steg 1 - Definiera ditt mål

Det är viktigt att förstå kampanjens mål, till exempel att uppnå högsta möjliga avkastning på investerat kapital eller lägsta möjliga CPA. Prestandakampanjer har [optimeringsmålen](/help/dsp/optimization/optimization-goals.md) [!UICONTROL Highest Return on Ad Spend (ROAS)"] eller [!UICONTROL Lowest Cost per Acquisition (CPA)]. Ange optimeringsmålet för varje paket i kampanjen utifrån detta.

![optimeringsmål](/help/dsp/assets/optimization-goals.png)

Du måste också identifiera de framgångshändelser som leder till det övergripande målet och skapa anpassade mål utifrån detta. Ange ett anpassat mål för varje paket som ska användas med det övergripande optimeringsmålet för rapportering och algoritmisk optimering med [!DNL Adobe Sensei]. Mer information om hur du skapar anpassade mål, inklusive bästa praxis, finns i [Anpassade mål](custom-goal.md).

## Steg 2 - Definiera er strategi

### Prospecting Strategies

Paket med huvudtratt omfattar praktik med mycket bred målinriktning för att nå ut till nya konsumenter.

#### Rekommenderade placeringsstrategier för potentiell kund

* Hitta nya målgrupper som kan konvertera med hjälp av följande taktiker:

   * Look-alike-modellering från en datahanteringsplattform (DMP), som Adobe Audience Manager.
   * Beteendeanpassning med hjälp av data från tredje part.
   * Sammanhangsbaserad målinriktning.
   * Målinriktning för webbplats/kategori.

* Använd RON-målinriktning (Run of Network): Det är viktigt att inkludera en mängd nätverksplaceringar utan målgruppsinriktning och med bred målinriktning för inventering. Detta gör att algoritmen [!DNL Adobe Sensei] kan hitta värdefulla användare som kan ha nyare cookies som ännu inte har kategoriserats till en målgrupp.

### Återmarknadsföringsstrategier

Lägre trattpaket innehåller placeringar som riktar sig till användare som redan har varit på annonsörens webbsida eller för vilka annonsören har CRM-data.

#### Rekommenderade placeringsstrategier för återmarknadsföring

* Om annonsören är kund hos Adobe Analytics eller Adobe Audience Manager kan ni skapa förstahandssegment (som besökare på hemsidan, produktsidor eller övergivna varukorgar) och använda dem som placeringsmål i DSP.

* Undvik att tilldela för mycket budget till en målgruppsanpassad placering. Generellt gäller att du budgeterar 30 USD per 1 000 användare per månad.

## Steg 3 - Skapa paket

Det bästa sättet är att skapa separata paket för prospektering med övre kanalen och för återmarknadsföring med lägre kanal. Optimering sker på paketnivå, så att prestandadata från alla placeringar i ett paket samlas. Därför bör du gruppera placeringar i paket med liknande förväntade prestanda.

![exempel på separata paket för prospektering och återmarknadsföring](/help/dsp/assets/p-r.png)

Använd även följande inställningar.

### Mål och budget

* **Pacing &amp; Capping:** Om du vill välja ett mål för CPA- eller ROAS-optimering måste pacing på paketnivå användas. Detta garanterar att alla placeringar i paketet optimeras för att distribuera utgifter baserat på prestanda och skalas efter de valda målen.

* **Flight Dates:** (Prospecting packages) Använd funktionen [!UICONTROL Activate Custom Flighting] när kampanjen pågår längre än 25 dagar. Först ställer du in en anpassad flygning för de första 10 dagarna på ungefär 75 % av den nödvändiga dagliga budgeten för att minska utgifterna under *inlärningsfasen*. Ange sedan en andra anpassad flygning för resten av budgeten.

  Om du till exempel har 100 000 USD att spendera på 30 dagar anger du budgeten för Flight 1 (Dagar 1-10) till 25 000 USD (75 % x $100 000/30 dagar = $2 500 per dag). Använd den återstående budgeten på 75 000 USD för Flight 2 (Dagarna 11-30).

* **Budget:** DSP försöker alltid allokera 100 % av paketbudgeten jämnt mellan alla placeringar i ett paket. Om en placering har låga utgifter eller inga utgifter rekommenderar vi att placeringen begränsas så att mer av budgeten kan allokeras till utplaceringar i stor skala. Tillåt 24-48 timmar för budgetändringar att kalibrera.

* **Optimeringsmål:** Använd ett av de två prestationsoptimeringsmålen, *[!UICONTROL Highest Return on Ad Spend]* eller *[!UICONTROL Lowest Cost per Acquisition]*, beroende på paketets mål. Dessa mål optimerar paketet automatiskt mot den högsta ROAS- respektive den lägsta CPA-placeringen.

* **Anpassade mål:**
   * Om ett nytt paket har samma mål som ett befintligt paket kan du länka det befintliga paketet så att algoritmen kan använda befintliga maskininlärningsdata.
   * Ange lämplig [!UICONTROL Target CPA] eller [!UICONTROL Target ROAS].

* **Flight Pacing och Intraday Pacing:** För båda typerna av pacing väljer du *[!UICONTROL Even]* för att maximera dina prestandamål genom att paketera enhetligt under varje dag och under hela flygningen.

  >[!CAUTION]
  >
  >Använd bara *[!UICONTROL FrontLoad]* och *[!UICONTROL Aggressive Front Load]* för flightpacing och *[!UICONTROL ASAP]* pacing för intraday-pacing när du helt prioriterar leverans och utgifter framför prestandaoptimering eftersom dessa strategier kan påverka dina önskade nyckeltal för prestanda negativt.

## Steg 4 - Skapa placeringsstruktur

Mindre är mer. Om du kan ställa in färre än sex placeringar per paket kan den tillgängliga budgeten dynamiskt flyttas till de mest effektiva placeringarna.

Se även till att du lägger till varje placering i ett paket med måltypen *[!UICONTROL Prospecting]* eller *[!UICONTROL Retargeting]* för ett paket.

Nedan följer de rekommenderade placeringsinställningarna för prestandakampanjer.

### Mål

Du måste konfigurera CPA- eller ROAS-optimering på paketnivå (se Steg 3 - Skapa paket), men du kan lägga till ytterligare inställningar på placeringsnivå.

* **Max. bud:**
   * Använd ett lågt maximalt bud ($5) för prospekteringsplaceringar.
   * Använd ett högt maximalt bud ($12) för återmarknadsföring.

* **Förbudsfilter:** Minimera, eller helst undvik, genom att ange aggressiva förbudsfilter, vilket förhindrar att placeringen når skalan. De bästa sätten är följande:

   * Använd ett (1) förbudsfilter per placering. Om du använder flera förbudsfilter måste båda vara uppfyllda, vilket minskar skalan.

   * Överväg att ställa in mindre strikta förbudsfilter om ytterligare målgruppsanpassning (som målgruppsanpassning, geolokalisering och webbplatsanpassning) tillämpas.

Se beskrivningar av när varje pre-bid-filter ska användas på [Placement-level Pre-Bid Filters och How to Use Them](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Lager

Använd [!UICONTROL Public] (Open Exchange) och [!UICONTROL On Demand] lager om du vill maximera skalan.

### Webbplatsmål

* **[!UICONTROL Traffic Type]**: endast [!UICONTROL Websites]
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Målgruppsanpassning

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * För prospekteringsplaceringar kan du gruppera liknande målgruppskategorier och liknande målgruppsstorlekar på en och samma plats. Gör sedan något av följande beroende på prestanda:
      * Ta bort underpresterande målgrupper från befintliga placeringar.
      * Flytta högpresterande målgrupper till en separat plats för bättre budgetkontroll.
   * För återannonsplaceringar bör du helst inkludera ett målgruppssegment per placering för att enkelt kunna styra anbud och budget.

>[!NOTE]
>
>Dina annonser fungerar bäst om en användare bara kan nås på en plats. Betydande överlappning mellan användare på olika platser kan leda till konkurrens, vilket leder till en cykel med ständigt ökande bud, vilket ökar kostnaden per användare. Om du inkluderar flera målgrupper måste du därför se till att de inte består av överlappande användare/målgruppsmedlemmar.
>
> Ni kan undvika överlappande målgrupper genom att skapa era målgrupper i lager så att ni kan utelämna de högre, mer omfattande nivåerna från placeringar efter behov.

* **[!UICONTROL Frequency Capping]:**
   * För prospekteringsplaceringar ska du använda täta frekvensändar (ett intryck per dag).
   * För retargetingplaceringar ställer du in det primära placeringshöljet på 6-10 visningar per dag och det sekundära locket på ett intryck per timme.

* **[!UICONTROL Device Targeting]**:
   * Inkludera [!UICONTROL Computer], [!UICONTROL Mobile] och [!UICONTROL Tablet].
   * Använd inte [!UICONTROL Firefox] och [!UICONTROL Safari] som mål på grund av begränsningar för målinriktning och mätning. Kontakta kontoteamet på Adobe för mer information om [!DNL Adobe]-stöd för [!DNL Safari ITP].
   * Om du har en mobil webbtrafik som mål inaktiverar du alla webbläsare utom [!UICONTROL Chrome] och [!UICONTROL Edge].

### Varumärkessäkerhet och mediakvalitet

Genom att använda kontextuell filtrering, blockering av bedrägeri före bud och/eller [!UICONTROL Ads.txt]-filtrering begränsas skalan för dina placeringar, men de används vid behov.

## Steg 5 - Använd rätt kreativa Assets

* Det bästa sättet är att inkludera så många unika annonsstorlekar som möjligt för att maximera räckvidden. Med den universella visningsmallen kan du överföra alla standardstorlekar för visning och visning.
* Kontrollera att alla placeringar innehåller *minst* alla primära bildskärmar och storlekar (300x250, 728x90, 160x600, 300x600, 320x50 och 300x50).
* Uppdatera kreatörerna ofta för att förhindra kreativ trötthet.

>[!MORELIKETHIS]
>
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Så här optimerar DSP era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Pre-Bid-filter på placeringsnivå och Så här använder du dem](optimization-pre-bid-filters.md)
>* [Checklista för kampanjstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
