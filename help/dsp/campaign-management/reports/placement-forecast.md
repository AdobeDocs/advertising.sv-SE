---
title: Visa prognosrapport för placering
description: Se hur många visningar, utgifter och optimalt maximalt bud som prognostiserats för en viss målinriktningsstrategi för en placering.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Visa prognosrapport för placering

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Verktyget för placeringsprognos visar prognostiserat antal visningar, utgifter och optimalt högsta bud för en viss målinriktningsstrategi. Prognosen beräknas utifrån det totala lagret som är tillgängligt för placeringen och de unika användare som är tillgängliga.

>[!NOTE]
>
>* Postnummer tas inte med i beräkningen av placeringsprognos.
>* Ingen prognos genereras för praktik med endast programmatisk målgruppsanpassning (PG) eftersom tillgänglighet och utgifter är deterministiska.

## Information i prognosen

Prognosen innehåller följande information:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** Den uppskattade kostnaden per tusen visningar (eCPM) som målinställningarna kan förvänta sig att nå.

   * **[!UICONTROL Budget]:** Den uppskattade budgeten för målinställningarna.

   * **[!UICONTROL Impression]:** Det uppskattade antalet visningar för målinställningarna.

* **[!UICONTROL Budget Yield Curve]:** Det uppskattade antalet visningar som placeringen kan leverera på olika budgetnivåer om alla andra målinriktningsinställningar är desamma.

* **[!UICONTROL Max Bid Yield Curve]:** Den uppskattade utgiften för placeringen på olika Max. Bid-nivåer, när alla andra målinställningar är desamma.

* **[!UICONTROL Message]:** Ger information om prognostiserade utdata, inklusive scenarier där prognosen inte kunde genereras. Eventuella målinriktningsinställningar som granskats men inte beaktats i det scenariot på grund av brist på data markeras också.

### Budgetberäkning

* För placeringar som inte är tilldelade ett paket används placeringsbudgeten för beräkningar. Inom en flygning beräknas samma totala budget.

* För placeringar i ett paket används den budget som är tilldelad placeringen för beräkningar. Under flygningen beräknas den budget som tilldelats placeringen och inkluderas i meddelandet.

* För placeringar som läggs till i ett paket under flygning delas budgeten upp lika baserat på antalet placeringar. När placeringen blir aktiv beräknas budgeten som tilldelats av paketet.

## Krav

* Minimiutgifter: 25 USD per dag eller motsvarande i lokal valuta per placering.

* Maximala utgifter: 15 000 USD per dag eller motsvarande i lokal valuta per placering.

* Minsta högsta bud, högsta högsta bud: Det finns ett lägsta högsta bud (för kurvan för budgeterad avkastning) och högsta bud (för kurvan för maximal budkapacitet) per placeringstyp. Dessa värden är globala och tar inte hänsyn till regionala variationer. Ibland kan dessa värden vara för höga eller för låga för målregionen.

* Historiska data: Placeringsprognosen är tillgänglig när det finns tillräckligt med historiska data. Nedan följer exempel på när otillräckliga historiska data kan finnas tillgängliga:

   * Placeringen har som mål en ny region för kampanjen.

   * Placeringen avser ett nytt lageravtal för kampanjen.

   * Placeringen använder en ny annonstyp för kampanjen.

     En placering är vanligtvis en samling med flera annonsmallar som definieras av plattformar på utbudssidan. Så även om placeringen har funnits länge, och om den underliggande annonsmallen är ny, kan prognosverktyget inte skapa en prognos.

## Öppna prognosrapporten för placering

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn och klicka sedan på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Leta reda på **[!UICONTROL Forecast]** i det övre högra hörnet. Klicka vid behov på ![Prognos](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Ibland kan prognosen vara otillgänglig på grund av webbläsarens cache. Om detta händer rensar du cacheminnet och försöker igen.

>[!MORELIKETHIS]
>
>* [Typer av prestandarapporter i Campaign Management-vyer](campaign-reports-about.md)
>* [Visa diagnostikrapporter för placering](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
