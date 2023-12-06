---
title: Om DSP
description: Lär dig mer om planeringsverktyget för att förutsäga den unika räckvidden för utplaceringar av uppkopplade TV-apparater (CTV) enligt angiven budget och målinriktningskriterier.
feature: DSP Planner
source-git-commit: 9799ff5464d48e6258026ec997c5d5091576b9c6
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# Om DSP

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Betafunktion*

Planeringsverktyget hjälper dig att förutsäga den unika räckvidden för CTV-placeringar (uppkopplad TV) på hushållsnivå enligt angiven budget och kriterier för målinriktning innan du börjar spendera på lagret. När du har utvärderat flera räckviddsplaner kan du implementera den plan som bäst överensstämmer med det önskade resultatet i dina paket och placeringar.

Planeringsverktyget använder historiska bud, intryck och data från de senaste 90 dagarna för att uppskatta den unika räckvidden, genomsnittliga CPM-värden, genomsnittlig frekvens och visningar för en plankonfiguration.

## Planeringsprognos

Varje prognos består av en prognoskurva för räckvidd-budget som visar hur stor räckvidd som kan uppnås med planinställningarna. För markören över visualiseringen för att se fler möjligheter med högre budget.

![Planeringsprognos](/help/dsp/assets/planner-forecast.png "Planeringsprognos")

Prognosresultatet innehåller även en [!UICONTROL Inventory Breakdown] som visar hur olika utgivare bidrar till en unik räckvidd och erbjuder värdefulla identifieringsmöjligheter.

>[!NOTE]
>
>* The [!UICONTROL Inventory Breakdown] -avsnittet visar endast data för privata och [!UICONTROL On Demand] lager.
>* Den uppskattade unika räckvidd som visas för två utgivare kan överlappa varandra.

## Planeringsvyn

I [!UICONTROL Planner] kan du visa dina befintliga CTV-räckviddsplaner och skapa nya.

Du kan också redigera, duplicera, exportera, arkivera eller generera om prognosen för alla planer.

## Vanliga frågor

+++Vilka typer av lager stöder planeringsverktyget?

Planeringsverktyget har stöd för alla typer av lager, inklusive programmatisk garanterad (PG), privat marknadsplats (PMP). [!UICONTROL On Demand]och offentligt. Ta med kontrakt med minst 50 000 visningar de senaste sju dagarna för att generera korrekta prognoser.

+++

+++Varför ser jag &quot;[!UICONTROL Unable to generate forecast]?&quot;

En av de vanligaste orsakerna till det här felet är en otillräcklig budget eller ett maximalt bud. För bästa resultat bör du använda en minimibudget på 5 000 USD. Om [!UICONTROL Connected TV] medietypen är vald, ange ett maximalt bud på minst 10 USD.

Se även till att de utgivare eller avtal som ingår är aktiva och att de nyligen har tittat på något.

+++

+++I byggde en placering baserat på prognosen, men den uppnådde inte den unika räckvidd som angavs i räckviddsprognosen. Varför?

Prognosen för räckvidd är bara en uppskattning, och de faktiska resultaten förväntas variera på grund av flera faktorer som ändras ofta, till exempel säsongsvariation, anbudskonkurrenskraft samt tillgång och efterfrågan. Det förväntas inte vara helt korrekt, men är mest användbart för riktade insikter i kampanjstrategier som kan ge de bästa resultaten.

+++

+++Kan planeraren generera olika prognosresultat med samma indatainställningar?

Planeraren genererar prognoser baserat på de senaste observerade data, så prognosen kan variera vid olika tidpunkter även om planinställningarna är desamma. Överväg att generera flera prognoser för samma plan och exportera resultaten för varje.

+++

+++Kan jag spara planeringens prognosresultat?

Ja, du kan exportera en prognos till en [!DNL Microsoft® Excel] kalkylblad genom att klicka **[!UICONTROL ...]** > **[!UICONTROL Export]** i det övre högra hörnet. I kalkylbladet hämtas den information som visas i den maximala budgetkurvan med hjälp av två datakolumner: [!UICONTROL Budget] och [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [Om DSP](planner-about.md)
>* [Skapa en uppkopplad TV-sändningsplan](planner-create.md)
>* [Duplicera en ansluten TV-sändningsplan](planner-duplicate.md)
>* [Redigera en plan för ansluten TV-räckvidd](planner-edit.md)
>* [Exportera ett uppkopplat TV-program](planner-export.md)
>* [Generera om prognosen för en plan för uppkopplad TV](planner-forecast.md)
>* [Arkivera ett uppkopplat program för tv-räckvidd](planner-archive.md)
>* [Inställningar för uppkopplade TV-program](planner-settings.md)
