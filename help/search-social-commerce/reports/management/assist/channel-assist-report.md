---
title: '[!UICONTROL Channel Assist Report]'
description: Läs mer om [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# [!UICONTROL Channel Assist Report]

*Annonsörer med klickspårning i Sök, Socialt och Commerce och med konverteringsspårning från Adobe Advertising, Adobe Analytics (med integrering av [!DNL Analytics]) eller som tillhandahålls i feeds med en token (`ef_id`) endast*

[!UICONTROL Channel Assist Report] visar hur olika marknadsföringskanaler (sökning eller sociala kanaler från Search, Social och Commerce, eller visning eller video från Advertising DSP) har hjälpt konverteringsprocessen. Rapporten visar hur varje mönster med händelsetyper som ledde till en eller flera konverteringar har bidragit till dina totala konverteringar. Du kan t.ex. se hur många konverteringar som gjordes när användarna först såg ett visningsannons och sedan klickade på en sökannons och sedan gjorde en beställning. Du kan också se hur många konverteringar som gjordes efter att användarna interagerade med mer än 10 annonser. Händelsetyper är bland annat klickningar, visningar och klickningar, videovisningar och klickningar samt andra trycksaker och klickningar. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Rapportresultaten innehåller aggregerade data för varje mönster med händelsetyper i konverteringssökvägen - upp till de N tidigaste händelsetyperna - som inträffade i annonsörens [klickfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j). Om du t.ex. väljer en banstorlek på fem (5) innehåller rapporten konverteringssökvägar som innehåller upp till de fem tidigaste händelserna, med en rad för varje mönster med händelsetyper som spåras (t.ex.&quot;sökklickning&quot; och sedan&quot;visningsintryck&quot;). Varje rad visar ett händelsemönster, inklusive den första händelsen i sökvägen och den sista händelsen som resulterade i konverteringar (även om den sista händelsen ligger utanför den angivna sökvägsstorleken). Som standard är raderna i stigande ordning efter antalet händelser i sökvägen.

Du kan också inkludera sammanställningskonverteringsdata för varje rad. När du tar med kolumnerna för konverteringar/intäkter i rapporten visas varje konverteringstyp i fyra kolumner, som visar a) det totala antalet konverteringar, b) procentandelen av de totala konverteringarna som var kopplade till det händelsemönstret, c) den genomsnittliga fördröjningen i dagen från den första händelsen till en konvertering och d) den genomsnittliga fördröjningen i dagar från den senaste händelsen till en konvertering. När konverteringssökvägen innehåller fler händelser än den angivna sökvägsstorleken, innehåller rapporten ytterligare rader som samlar data för konverteringar som är ett resultat av det högre antalet händelser (t.ex. alla mönster som innehöll sex händelsetyper).

Du kan visa data för de föregående 18 månaderna.

## Tillgängliga kolumner

Nedan visas de kolumner som är tillgängliga för varje rapport. Standardkolumnerna inkluderas automatiskt som standard. Du kan lägga till tillgängliga anpassade kolumner från avsnittet Kolumner i rapportinställningarna.

| Kolumn | Standard? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] till [!UICONTROL 5th Event] | Standard | De fem tidigaste händelsetyperna i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönstret](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Standard | Antalet händelsetyper i konverteringssökvägen som inträffade i annonsörens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Standard | Händelsetypen för den första (tidigaste) händelsen i konverteringssökvägen. |
| [!UICONTROL Last Event Type] | Standard | Händelsetypen för den senaste händelsen som resulterade i konverteringar (även om den sista händelsen ligger utanför den angivna sökvägsstorleken). |
| \[Advertiser-specifika anpassade (härledda) mätvärden\] | Egen | Värdet för ett anpassat mätvärde som du har skapat och som beräknas utifrån befintliga mätvärden. |
| \[Advertiser-specifika konverteringsvärden\] | Egen | Antalet konverteringar för ett angivet konverteringsmått eller webbplatsengagemangsmått. |
| [!UICONTROL % of Total] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna men automatiskt inkluderat i rapportutdata för varje konverteringsmått som ingår) Procentandelen av dina totala konverteringar mellan portföljer som tillskrevs händelsemönstret. |
| [!UICONTROL 6th Event] till [!UICONTROL 30th Event] | Egen | Den sjätte till den 30:e händelsetypen i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje konverteringsmått som ingår) Genomsnittlig fördröjning i dagar från den första händelsen till en konvertering. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningar, men inkluderas automatiskt i rapportutdata) Genomsnittlig fördröjning i dagar från den senaste händelsen till en konvertering. |
| [!UICONTROL Path Frequency] | Egen | Antalet gånger som sökvägen för den här raden inträffade före konverteringen. |

>[!MORELIKETHIS]
>
>* [Om assistentrapporter](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Inställningar för assistentrapport](assist-report-settings.md)
>* [Generera en hjälprapport](assist-report-generate.md)
