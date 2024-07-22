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
>Fakturerbara avgifter visas i måttet [!UICONTROL Net CPM].

Du kan åsidosätta inställningen på paketnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (skrivskyddat för befintliga paket) På vilken nivå placeras plats och ändpunkter i paketet:

* **[!UICONTROL Package level pacing]:** Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar placeras och fästs som en *grupp*. Denna strategi säkerställer att alla placeringar i ett givet paket optimeras helhetsbaserat på prestanda och skalning till utvalda nyckeltal (KPI).

* **[!UICONTROL Placement level pacing]:** Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar placeras och fästs *individuellt*. Det bästa sättet är att endast använda denna strategi för att genomföra garanterade privata marknadsplatserbjudanden.

**[!UICONTROL Flight Dates]:** Paketets totala startdatum och slutdatum. Flightdatumen måste inkluderas i kampanjens flygdatum.

>[!NOTE]
>
>* Flightdatumen för alla placeringar som är tilldelade detta paket måste inkluderas inom dessa datum.
> * Du kan inte redigera paketets startdatum när anpassad ljussättning aktiveras.

**[!UICONTROL Activate Custom Flighting]:** Gör att du kan skapa icke-jämna mellanrum för paketet i avsnittet [!UICONTROL Flighting] nedan. När du har aktiverat anpassad felsökning och sparat paketet kan du inte inaktivera anpassad felsökning eller redigera paketets startdatum.

**[!UICONTROL Budget]:** (Endast paket med paketnivåpacing) Budgettak brutto och budgetintervall.

För paket med anpassad felsökning är budgetintervallet alltid *[!UICONTROL All time]*. För paket utan anpassad felsökning anger du budgetintervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paket med enbart paketering och dynamisk marginalhantering på paketnivå) Bruttobudgettak för paketets varaktighet.

**[!UICONTROL Optimization Goal]:** (Endast paket med paketnivåpacing) Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på [Optimeringsmål och Använda dem](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Endast paket med optimeringsmålen [!UICONTROL Highest Return on Ad Spend] och [!UICONTROL Lowest Cost per Acquisition]) Ett [anpassat mål](/help/dsp/optimization/custom-goal.md) som innehåller de intäkt- eller konverteringshändelser som används för att beräkna CPA- eller ROAS-måttet. Det anpassade målet kan även omfatta ytterligare viktade övre tratthändelser (t.ex. sidbesök och kundvagnstillägg) som ska användas utöver CPA- eller ROAS-mätvärdena för paketoptimering. Mer information om anpassade mål, inklusive de bästa sätten att skapa för anpassade mål och kampanjer som använder dem, finns i [Anpassade mål](/help/dsp/optimization/custom-goal.md) och [Bästa metoder för att konfigurera prestandakampanjer](/help/dsp/optimization/campaign-best-practices-performance.md).<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->.

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Valfritt; paket med optimeringsmålen [!UICONTROL Highest Return on Ad Spend] och [!UICONTROL Lowest Cost per Acquisition]) Anger att optimeringsmodellen endast ska lära sig av klickbaserade konverteringar. I annat fall lär sig optimeringsmodellen av både klicknings- och inställningsbaserade konverteringar.

**[!UICONTROL Conversion Metric]:** (Valfritt; paket med optimeringsmålen [!UICONTROL Highest Return on Ad Spend] och [!UICONTROL Lowest Cost per Acquisition]) Den slutliga konverteringshändelsen (till exempel registreringar) eller intäktshändelsen/försäljningsbeloppet (till exempel köp- och inköpsvärden) som ska användas för att beräkna avkastningen på annonskostnaderna eller kostnaden per förvärv. Välj i en lista över alla primära händelser (&quot;målmått&quot;) mappade till det valda anpassade målet. Om listan är tom redigerar du det anpassade målet så att minst en av de underliggande händelserna inkluderas som målmått.

**[!UICONTROL Package Goal Type]:** (Endast paket med anpassade optimeringsmål) Paketets syfte. Med den här inställningen kan du avgöra hur paketet ska optimeras:

* *[!UICONTROL Prospecting]:* Prospekteringspaket fokuserar på att skaffa nya kunder.

* *[!UICONTROL Retargeting]:* Återmarknadsföring av paket fokuserar på att återexponera tidigare besökare eller kunder.

* *[!UICONTROL Other]:* Alla andra syften.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Endast paket med anpassade optimeringsmål) Ett annat paket vars historikdata används som indata för optimering av paketet.

**[!UICONTROL Target]:** (Endast paket med paketnivåpacing) Målet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Frequency Cap]:** (Endast paket på paketnivå) Det antal gånger som en unik enhet, ett universellt ID eller en person (beroende på den angivna [!UICONTROL Cross Device Level] för kampanjen och placeringens [!UICONTROL Targeting]-inställning) kan hanteras annonser från paketet. Alternativen är *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
>* Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.
>* Det bästa sättet är att ange frekvensgränser för både prospektering och återmarknadsföring på paketnivå.
> * Högre frekvenshål ger högre utgifter och större intryck men lägre räckvidd. Lägre frekvenshål ger lägre kostnader och större intryck men större räckvidd.

**[!UICONTROL Pace on]:** (Endast paket med paketnivåpacing) Vilken pacing baseras på:

* *[!UICONTROL Budget]:* (Standard) Det här alternativet ger så många avtryck som möjligt inom den allokerade paketbudgeten.

* *[!UICONTROL Impressions]:* Det här alternativet levererar avbildningar tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *All time,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Endast paket med paketnivåpacing) Så här använder du plats för och leverans i hela flygningen:

* *[!UICONTROL Even]:* Levereras enhetligt under varje flygning, med ett mål på 50 % av leveransen under den första halvan av flygningen.

* *[!UICONTROL Slightly Ahead]:* (standard) Accelererar leveransen så att den är 55-65 % färdig halvvägs genom flygningens varaktighet.

* *[!UICONTROL Frontload]:* Accelererar leveransen så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Accelererar leveransen så att den är 75-85 % klar halvvägs genom flygningen.

**[!UICONTROL Intraday pacing]:** (Endast paket med paketnivåpacing) Så här använder du plats för och leverans för varje dag i flygningen:

* *[!UICONTROL Even]:* (standard) Skalar leverans baserat på lagertillgänglighet. I allmänhet levereras fler annonser per timme under dagtid, när auktionsvolymen är högre och färre annonser levereras under kvällarna och morgnarna.

* *[!UICONTROL ASAP]:* Accelererar leveransen till dubbelt så snabb som *Even*.

  >[!CAUTION]
  >
  >Det här alternativet kan påverka prestandan negativt. Använd det bara när ni prioriterar leverans och utgifter framför prestandaoptimering.

## [!UICONTROL Flighting]

(Paket med paketnivåpaketering) Paketets flygperioder, inklusive eventuella anpassade flygperioder inom paketets övergripande [!UICONTROL Flight Dates]. Du kan bara konfigurera anpassade flygningar när alternativet [!UICONTROL Activate Custom Flighting] är aktiverat i avsnittet [!UICONTROL Goals & Budget].

**[!DNL Flight N]:** (Endast tillgängligt när alternativet [!UICONTROL Activate Custom Flighting] är aktiverat) För varje flygning anger du startdatum, slutdatum och mål för utgift. Klicka på **[!UICONTROL Add Flight]** om du vill lägga till en annan flight.

För befintliga paket kan du om du vill ange ett värde i kolumnen [!UICONTROL Rollover] för en flygning för att lägga till eventuell oanvänd budget till nästa flygning. Det projicerade värdet i kolumnen [!UICONTROL Adjusted Goal (Goal + Rollover)] ändras i enlighet med detta.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Koppla en placering till ett paket](package-attach-placement.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Frågor och svar om Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
