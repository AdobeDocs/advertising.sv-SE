---
title: Paketinställningar
description: Se beskrivningar av tillgängliga paketinställningar.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: ab3118901b7cd88776f7c0ce8038b928118a7555
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Paketinställningar

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Paketnamnet. Maxlängden är 60 tecken.

**[!UICONTROL Description]:** (Valfritt) En beskrivning av paketet.

**[!UICONTROL 3rd Party Billed Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad:

* **[!UICONTROL CPM]:** Kostnaden per 1 000 visningar (CPM).

* **[!UICONTROL Description]:** En beskrivning av CPM-avgiften.

>[!NOTE]
>
>Faktureringsbara avgifter återspeglas i [!UICONTROL Net CPM] mätvärden.

Du kan åsidosätta inställningen på paketnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Skrivskyddat för befintliga paket) På vilken nivå placeras och fästas placeringarna i paketet:

* **[!UICONTROL Package level pacing]:** Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar paketeras och kapas som en *grupp*. Denna strategi säkerställer att alla placeringar i ett givet paket optimeras helhetsbaserat på prestanda och skalning till utvalda nyckeltal (KPI).

* **[!UICONTROL Placement level pacing]:**  Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar paketeras och fästs *individuellt*. Det bästa sättet är att endast använda denna strategi för att genomföra garanterade privata marknadsplatserbjudanden.

**[!UICONTROL Flight Dates]:** Paketets totala startdatum och slutdatum. Flightdatumen måste inkluderas i kampanjens flygdatum.

>[!NOTE]
>
>* Flightdatumen för alla placeringar som är tilldelade detta paket måste inkluderas inom dessa datum.
> * Du kan inte redigera paketets startdatum när anpassad ljussättning aktiveras.

**[!UICONTROL Activate Custom Flighting]:** Gör att du kan skapa icke-jämna mellanrum för paketet i [!UICONTROL Flighting] nedan. När du har aktiverat anpassad felsökning och sparat paketet kan du inte inaktivera anpassad felsökning eller redigera paketets startdatum.

**[!UICONTROL Budget]:** (Paket med enbart paketnivåpaketering) Bruttobudgetens övre gräns och budgetintervallet.

För paket med anpassad felsökning är budgetintervallet alltid *[!UICONTROL All time]*. För paket utan anpassad felsökning anger du budgetintervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paket med enbart paketnivåpaketering och dynamisk marginalhantering) Bruttobudgettaket för paketets varaktighet.

**[!UICONTROL Optimization Goal]:** (Paket med enbart paketnivåpaketering) Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på [Optimeringsmål och Så här använder du dem](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Paket med[!UICONTROL Highest Return on Ad Spend]och &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; (endast optimeringsmål) A [anpassat mål](/help/dsp/optimization/custom-goal.md) som omfattar de intäkter eller konverteringshändelser som används för att beräkna CPA- eller ROAS-mätningen. Det anpassade målet kan även omfatta ytterligare viktade övre tratthändelser (t.ex. sidbesök och kundvagnstillägg) som ska användas utöver CPA- eller ROAS-mätvärdena för paketoptimering. Mer information om anpassade mål, inklusive de bästa sätten att skapa för anpassade mål och kampanjer som använder dem, finns i &quot;[Anpassade mål](/help/dsp/optimization/custom-goal.md)och &quot;[Bästa metoder för att konfigurera resultatkampanjer](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

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

**[!UICONTROL Frequency Cap]:** (Paket med enbart paketnivåpaketering) Antal gånger en unik enhet, ett universellt ID eller en person (beroende på angivet [!UICONTROL Cross Device Level] för kampanjen och placeringen [!UICONTROL Targeting] inställning) kan hanteras med annonser från paketet. Alternativen inkluderar *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

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

(Paket med paketnivåpaketering) Paketets flygperioder, inklusive eventuella anpassade flygperioder inom det övergripande [!UICONTROL Flight Dates] för paketet. Du kan bara konfigurera anpassade flygningar när [!UICONTROL Activate Custom Flighting] är aktiverat i [!UICONTROL Goals & Budget] -avsnitt.

**[!DNL Flight N]:** (Endast tillgängligt när [!UICONTROL Activate Custom Flighting] är aktiverat) För varje flygning anger du startdatum, slutdatum och målutgiftsmål. Klicka på **[!UICONTROL Add Flight]**.

För befintliga paket kan du även ange ett värde i [!UICONTROL Rollover] kolumn för en flygning för att lägga till eventuell oanvänd budget till nästa flygning. Projicerat värde i [!UICONTROL Adjusted Goal (Goal + Rollover)] -kolumnen ändras därefter.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Koppla en placering till ett paket](package-attach-placement.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Frågor och svar om Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
