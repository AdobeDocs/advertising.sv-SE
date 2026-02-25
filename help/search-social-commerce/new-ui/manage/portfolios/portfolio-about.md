---
title: (Nytt användargränssnitt) Om portföljer
description: Läs om portfolior.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: de3c527bd359e0d5285b90e54278983104a2a5b5
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# (Nytt användargränssnitt) Om portföljer

*Beta-funktion*

Ni kan hantera era annonskampanjer tillsammans med portföljer (liknande investeringsportföljer). En portfölj är en uppsättning annonskampanjer eller annonsuppsättningar, inklusive tillhörande nyckelord och annonser, som optimeras för ett enda affärsmål. Ett mål kan omfatta flera viktade konverteringar och ett enda budget- eller prestationsmål (t.ex. en månadsbudget eller ett mål för avkastning). Eftersom enskilda kampanjer/annonsuppsättningar, nyckelord och annonser kan fungera annorlunda än varandra (t.ex. kan de spendera olika belopp eller uppnå olika avkastning), använder optimeringsfunktionen AI-drivna modeller för att styra hela portföljen så att den tillsammans uppnår målet. Alla kampanjer i en portfölj använder samma valuta.

Vissa användarroller kan skapa och konfigurera portföljer. Beroende på portföljtyp kan portföljinställningarna omfatta portföljmålet, de tilldelade kampanjerna, utgiftsstrategin, eventuella anbudsbegränsningar på portföljnivå samt modellerings- och optimeringsparametrarna. När du är redo för sökningar, sociala medier och Commerce för att börja optimera en portfölj ändrar du statusen till&quot;optimerad&quot;.

Du kan också gruppera portföljer i [portföljgrupper](portfolio-group-manage.md) så att du kan visa sammansatta data för hela gruppen.

Beroende på din roll kan du kanske generera prestandamuleringar, som använder prediktiv modellering för att identifiera den optimala utgiftspunkten och detaljerade prognosnoggrannhetsrapporter.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Optimeringsstöd per anbudsstrategi {#optimization-by-bid-strategy}

Kampanjer är berättigade till optimering baserat på kampanjens eller annonsgruppens anbudsstrategi.

>[!NOTE]
>
>&quot;Smart budgivning&quot; och&quot;automatiserad budgivning&quot; används ofta utan åtskillnad, men de är inte samma sak. Smart budgivning refererar endast till [!DNL Google Ads] och [!DNL Microsoft Advertising] automatiserade budgivningsstrategier där auktionsbudgivning används, vilket innebär att annonsnätverket optimerar för konverteringar eller konverteringsvärden vid tidpunkten för varje auktion.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Anbudsstrategi | Smart Bidding? | Nyckelord-/produktgruppsnivå - bud? | Supportnivå | Måltyp | Anbudsenhet | Vad ställer Adobe in? | Vad innehåller annonsnätverket? |
|---|---|---|---|---|---|---|---|
| Manuell CPC ([!DNL Google Ads]-endast alternativ) | — | Ja | Skapa, redigera, optimera | Enskilt eller fleregenskapsmål med valfritt viktvärde | Nyckelord + matchningstyp + kampanj | Nyckelordsbud, kampanjbudget, värden för anbudsjustering | n/a |
| ECPC (Enhanced CPC) | Ja | Ja | Skapa, redigera, optimera | Enskilt eller fleregenskapsmål med valfritt viktvärde | Nyckelord + matchningstyp + kampanj | Nyckelordsbud, kampanjbudget | Justerar bud i realtid |
| Maximera klick[^1] | — | — | Skapa, redigera, optimera | Ingen; optimerar endast mot klickningar | Campaign | Kampanjbudget | Justerar bud i realtid för att maximera klickningar inom budgeten |
| Maximera konverteringar<br> (med eller utan TCPA) | Ja | — | Skapa, redigera, optimera | Enkelt egenskapsmål med en vikt på 1 | Kampanj eller annonsgrupp ([!DNL Google Ads])<br>Endast kampanj ([!DNL Microsoft Advertising]) | Kampanjbudget, mål-CPA när den anges<br>TCPA kan vara en fristående anbudsstrategi i [!DNL Microsoft Advertising]) | Justerar anbud i realtid för att maximera order/leads inom budgeten, vilket uppfyller ett CPA-mål när målet är angett |
| Maximera konverteringsvärde <br> (med eller utan TROAS) | Ja | — | Skapa, redigera, optimera | Fleregenskapsmål med valfritt viktvärde, eller mål med en egenskap med ett viktvärde som är större än 1 (som representerar ett monetärt värde) | Kampanj eller annonsgrupp ([!DNL Google Ads])<br>Endast kampanj ([!DNL Microsoft Advertising]) | Campaign budget, Target ROAS när den anges<br>TROAS kan vara en fristående anbudsstrategi i [!DNL Microsoft Advertising]) | Justerar anbud i realtid för att maximera intäkter/vinst inom budgeten och uppfylla ett ROAS-mål när målet har ställts in |
| Delning av måltryck | — | — | Skapa, redigera | n/a | n/a | n/a - kan inte tilldelas till en portfölj | Justerar offerterna i realtid för att nå ett mål för visningsdelning |

[^1]: Inställningen för anbudsstrategi [!UICONTROL Maximize Clicks] i annonsnätverket är inte densamma som för Search, Social och Commerce [!UICONTROL Maximize Clicks] . Om anbudsstrategin är [!UICONTROL Maximize Clicks] bör du bara tilldela den till en portfölj med optimering på kampanjnivå eller annonsnivå, inte en portfölj med optimering på nyckelordsnivå.

## Portfolio-status {#portfolio-status}

En portfölj kan ha följande status:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## Vyn [!UICONTROL Portfolios]

Vyn [!UICONTROL Portfolios] visar dina befintliga portföljer med anpassningsbara prestandadata. Du kan [anpassa kolumnerna i vyn](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) och filtrera data så att de inkluderar specifika portföljer [ från verktygsfältet](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) eller från [kolumnrubriken](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

Ovanför datatabellen kan du öppna ett resultatdiagram med upp till tre värden som summeras för alla portföljer i vyn för det angivna datumintervallet.

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Tillgängliga åtgärder

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Skapa en portfölj](portfolio-create.md)

* [Duplicera en portfölj](portfolio-duplicate.md)

* [Redigera portföljinställningar](portfolio-edit.md)

* [Redigera portföljinställningar gruppvis med hjälp av kalkylbladsfiler](portfolio-bulksheets.md)

* [Visa ett resultatdiagram över alla portföljer i vyn](portfolio-view-performance-graph.md)

* [Visa information om portföljresultat](portfolio-details.md)

* [Hämta data i [!UICONTROL Portfolios]-vyn](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Skapa en portfölj](portfolio-create.md)
>* [Duplicera en portfölj](portfolio-duplicate.md)
>* [Redigera en portfölj](portfolio-edit.md)
>* [Hantera datavyrapporter från [!UICONTROL Portfolios]-vyn ](portfolio-view-report.md)
