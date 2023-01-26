---
title: Hur DSP optimerar era kampanjer
description: Lär dig hur DSP optimerar paketen i era kampanjer.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Hur annonsering DSP optimerar era kampanjer

På den här sidan beskrivs hur den DSP optimeringsmotorn som drivs av [!DNL Adobe Sensei], optimerar paketen i era kampanjer. Om du vill ha tips och råd om hur ni optimerar kampanjer manuellt kontaktar du [!DNL Adobe] kontoteam. <!-- add link to trading playbook if we add it to help -->

Paketoptimeringsmålen fungerar på två nivåer:

* För varje paket: DSP allokerar budget till varje placering i paketet baserat på placeringens prestanda jämfört med den valda KPI:n.

* För varje placering/auktion i paketet: DSP beräknar det ekonomiska KPI-värdet i realtid för varje auktion per placering och använder sedan detta värde för att fastställa anbudet.

   >[!NOTE]
   >
   >Det ekonomiska värdet kan vägas kraftigt baserat på hur väl en placering är utgiven. Om en placering ligger bakom utgiftsmålet får man köpa auktioner med lägre kvalitet. Om en placering lätt kan uppnå sitt utgiftsmål kommer den att fokusera på auktioner med högre kvalitet.

## Paketoptimering

DSP kan optimera leveransen på två grundläggande sätt, med 20 olika varianter tillgängliga som passar just ditt prestationsmål. Du kan välja att:

* Prioritera prestandahastigheten

* Prioritera balansering av kostnadseffektivitet med prestandahastighet

Se [Optimeringsmål och Så här använder du dem](optimization-goals.md) för att avgöra vilket optimeringsmål som hjälper dig att uppnå dina nyckeltal.

### Paket som prioriterar prestandahastigheten

För optimeringsmål som prioriterar prestandakursen förutser DSP resultatet för varje auktion och alltid offerter vid det högsta anbudet. Exempel på tillämpliga optimeringsmål är [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]och så vidare.

Det här optimeringsläget fungerar bra om:

* Du känner redan till den effektiva/godtagbara CPM-nivån (till exempel ett historiskt riktmärke).

* Du kan justera [!UICONTROL Max Bid] för varje placering om du har problem med skalning.

* Du prioriterar skala framför effektivitet.

#### Mellanrumslogik {#pacing-logic-performance}

* Om ni spenderar pengar i takt med detta blir budgivningen mer selektiv, så att ni bara kan lägga bud på auktioner som förväntas ha höga prestationsnivåer.

* Om ni ligger efter kommer budgivningen att bli mindre selektiv, så att ni kan lägga bud på auktioner som förväntas ha lägre prestationsnivåer för att hinna ikapp målsättningen.

#### Rensa pris/budskugga {#clearing-price-performance}

När den har exekverat paketeringslogiken, kör DSP det föreslagna anbudet genom en modell för att beräkna clearingpriset. Om prognosen visar att anbudet kan sänkas med minimal minskning till vinsträntan, sänks anbudet enligt prognosen.

### Paket som prioriterar balansering av kostnadseffektivitet med prestandahastighet

För vissa optimeringsmål förutser DSP resultatet för varje auktion och justerar budpriserna automatiskt, utan att överskrida en placerings [!UICONTROL Max Bid]. Exempel på tillämpliga optimeringsmål är [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]och så vidare.

#### Paketlogik {#pacing-logic-balanced}

* Om utgifterna är i takt med detta blir DSP mer priskänslig och lägger lägre belopp för att kompensera vinsten med paketplanen.

* Om ett prestandamått också balanseras (alla mål utom [!UICONTROL Lowest CPM]), blandas den förväntade KPI:n med beloppet som är anbudet. Ni lägger därför ett högre bud på auktioner som förutspås bli mer presterande på&quot;kostnad per&quot;-basis.

* Om utgiftsnivån ligger efter blir DSP mindre priskänslig och offrar högre belopp, upp till [!UICONTROL Max Bid], för att sälja in vinsten med paketplanen.

#### Rensa pris/budskugga {#clearing-price-balanced}

När den har exekverat paketeringslogiken, kör DSP det föreslagna anbudet genom en modell för att beräkna clearingpriset. Om prognosen visar att anbudet kan sänkas med minimal minskning till vinsträntan, sänks anbudet enligt prognosen.

## Placeringsoptimering

Placering av filter före bud är det enklaste sättet att säkerställa höga prestanda. DSP använder filter före bud strategiskt för olika annonstyper för att uppnå prestandamål på alla platser i varje paket. Du kan använda filter före bud samtidigt med optimering på paketnivå eller oberoende av varandra.

>[!NOTE]
>
>Vilka filter som är tillgängliga för förbud varierar beroende på annonstyp. För en standardplacering kan du till exempel filtrera genom klickfrekvens och visningsbarhet, men inte efter slutförandegrad.

Se [Pre-Bid-filter på placeringsnivå och Så här använder du dem](optimization-pre-bid-filters.md) för att avgöra vilket föranbudsfilter som hjälper dig att uppnå dina KPI:er.

>[!MORELIKETHIS]
>
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Pre-Bid-filter på placeringsnivå och Så här använder du dem](optimization-pre-bid-filters.md)
>* [Felsökningsprestanda](/help/dsp/optimization/troubleshooting-performance.md)

