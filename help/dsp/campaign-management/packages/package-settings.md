---
title: Paketinställningar
description: Se beskrivningar av tillgängliga paketinställningar.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: cb57ada624bdc810a0d6921e89deba832a2b16d9
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Paketinställningar

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Paketnamnet. Maxlängden är 60 tecken.

**[!UICONTROL Description]:** (Valfritt) En beskrivning av paketet.

**[!UICONTROL 3rd Party Billed Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad:

>[!NOTE]
>
>Faktureringsbara avgifter återspeglas i [!UICONTROL Net CPM] mätvärden.
>
* **[!UICONTROL CPM]:** Kostnaden per 1 000 visningar (CPM).

* **[!UICONTROL CPM Description]:** En beskrivning av CPM-avgiften.

Du kan åsidosätta inställningen på paketnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Skrivskyddat för befintliga paket) På vilken nivå placeras och fästas placeringarna i paketet:

* **[!UICONTROL Package level pacing]:** Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar paketeras och kapas som en *grupp*. Denna strategi säkerställer att alla placeringar i ett givet paket optimeras helhetsbaserat på prestanda och skalning till utvalda nyckeltal (KPI).

* **[!UICONTROL Placement level pacing]:**  Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar paketeras och fästs *individuellt*. Det bästa sättet är att endast använda denna strategi för att genomföra garanterade privata marknadsplatserbjudanden.

**[!UICONTROL Flight Dates]:** Paketets startdatum och slutdatum.

Om du vill skapa icke-jämna mellanrum för paketet väljer du *[!UICONTROL *Activate Custom Flighting]** och konfigurera anpassade flygningar i [!UICONTROL Flighting] nedan. När du har aktiverat anpassad belysning och sparat paketet kan du inte inaktivera anpassad belysning.

>[!NOTE]
>
>* Flightdatumen måste inkluderas i kampanjens flygdatum. Dessutom måste flygdatum för alla placeringar som är tilldelade detta paket inkluderas i dessa datum.
> * Du kan inte redigera paketets startdatum när anpassad ljussättning aktiveras.

**[!UICONTROL Budget]:** (Paket med enbart paketnivåpaketering) Bruttobudgetens övre gräns och budgetintervallet.

För paket med anpassad felsökning är budgetintervallet alltid *[!UICONTROL All time]*. För paket utan anpassad felsökning anger du budgetintervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paket med enbart paketnivåpaketering och dynamisk marginalhantering) Bruttobudgettaket för paketets varaktighet.

**[!UICONTROL Optimization Goal]:** (Paket med enbart paketnivåpaketering) Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på [Optimeringsmål och Så här använder du dem](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Paket med[!UICONTROL Highest Return on Ad Spend]och &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; (endast optimeringsmål) A [anpassat mål](/help/dsp/optimization/custom-goal-about.md) som omfattar de intäkter eller konverteringshändelser som används för att beräkna CPA- eller ROAS-mätningen. Det anpassade målet kan även omfatta ytterligare viktade övre tratthändelser (t.ex. sidbesök och kundvagnstillägg) som ska användas utöver CPA- eller ROAS-mätvärdena för paketoptimering. Mer information om de bästa metoderna för anpassade mål och kampanjer som använder dem finns i  [Bästa metoder för att skapa ett anpassat mål](/help/dsp/optimization/custom-goal-best-practices.md) och [Bästa metoder för att konfigurera resultatkampanjer](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Valfritt): paket med &quot;[!UICONTROL Highest Return on Ad Spend]och &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;endast optimeringsmål) Anger att optimeringsmodellen endast ska lära sig av klickbaserade konverteringar. I annat fall lär sig optimeringsmodellen av både klicknings- och inställningsbaserade konverteringar.

**[!UICONTROL Conversion Metric]:** (Valfritt): paket med &quot;[!UICONTROL Highest Return on Ad Spend]och &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; enbart optimeringsmål) Den slutliga konverteringshändelsen (som registreringar) eller intäktshändelsen/försäljningsbeloppet (som köp- och inköpsvärden) som ska användas för att beräkna avkastningen på annonskostnaderna eller kostnaden per förvärv. Välj i en lista över alla primära händelser (&quot;målmått&quot;) mappade till det valda anpassade målet. Om listan är tom redigerar du det anpassade målet så att minst en av de underliggande händelserna inkluderas som målmått.

**[!UICONTROL Package Goal Type]:** (Paket med enbart anpassade optimeringsmål) Paketets syfte. Med den här inställningen kan du avgöra hur paketet ska optimeras:

* *[!UICONTROL Prospecting]:* Prospekterande paket fokuserar på att köpa nya kunder.

* *[!UICONTROL Retargeting]:* Återmarknadsföring av paket fokuserar på att återexponera tidigare besökare eller kunder.

* *[!UICONTROL Other]:* Alla andra syften.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Endast paket med anpassade optimeringsmål) Ett annat paket vars tidigare data används som indata för optimering av paketet.

**[!UICONTROL Target]:** (Paket med enbart paketnivåpaketering) Målet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Frequency Cap]:** (Paket med enbart paketnivåpaketering) Antal gånger en unik enhet eller person (beroende på den angivna [!UICONTROL Cross Device Level] för kampanjen) kan få annonser från paketet. Alternativen inkluderar *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
>* Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.
>* Det bästa sättet är att ange frekvensgränser för både prospektering och återmarknadsföring på paketnivå.
> * Högre frekvenshål ger högre utgifter och större intryck men lägre räckvidd. Lägre frekvenshål ger lägre kostnader och större intryck men större räckvidd.

**[!UICONTROL Pace on]:** (Paket med enbart paketnivåpaketering) Vilken paketering baseras på:

* *[!UICONTROL Budget]:* (Standard) Det här alternativet ger så många avtryck som möjligt inom den tilldelade paketbudgeten.

* *[!UICONTROL Impressions]:* Det här alternativet ger avtryck tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *Alltid,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Paket med enbart paketnivåpaketering) Hur ni lägger ut och levererar under hela flygningen:

* *[!UICONTROL Even]:* Leverans sker på ett enhetligt sätt under varje flygning, med ett mål på 50 % av leveranstiden under första hälften av flygningen.

* *[!UICONTROL Slightly Ahead]:* (Standard) Ökar leveranstiden så att den är 55-65 % färdig halvvägs genom hela flygtiden.

* *[!UICONTROL Frontload]:* Snabbare leverans så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Snabbare leverans så att den är 75-85 % klar halvvägs genom flygningen.

**[!UICONTROL Intraday pacing]:** (Paket med enbart paketnivåpaketering) Så här använder du jämna mellanrum och leverans för varje dag i flygningen:

* *[!UICONTROL Even]:* (Standard) Skalar leverans baserat på lagertillgänglighet. I allmänhet levereras fler annonser per timme under dagtid, när auktionsvolymen är högre och färre annonser levereras under kvällarna och morgnarna.

* *[!UICONTROL ASAP]:* Ger snabbare leverans än någonsin *Jämn*.

  >[!CAUTION]
  >
  >Det här alternativet kan påverka prestandan negativt. Använd det bara när ni prioriterar leverans och utgifter framför prestandaoptimering.

## [!UICONTROL Flighting]

(Paket med pachelagring på paketnivå och med[!UICONTROL Activate Custom Flighting]&quot; aktiverat) Anpassade flygperioder inom det övergripande [!UICONTROL Flight Dates] som anges i [!UICONTROL Goals & Budget] -avsnitt.

Ange startdatum, slutdatum och målantal visningar för varje flygning. Klicka på **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Koppla en placering till ett paket](package-attach-placement.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Frågor och svar om Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
