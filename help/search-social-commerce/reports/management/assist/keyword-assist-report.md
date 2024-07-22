---
title: '[!UICONTROL Keyword Assist Report]'
description: Läs mer om [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Keyword Assist Report]

*Annonsörer med klickspårning i Sök, Socialt och Commerce och med konverteringsspårning från Adobe Advertising, Adobe Analytics (med integrering av [!DNL Analytics]) eller som tillhandahålls i feeds med en token (`ef_id`) endast*

[!UICONTROL Keyword Assist Report] indikerar vilka nyckelord eller placeringar som kör klickningar. Rapporten visar varje mönster med betalda söknyckelord eller placeringar som har fått klickningar i en konverteringsbana och visar hur mönstret har bidragit till dina totala konverteringar. Du kan till exempel se hur många konverteringar som inträffade när användarna först klickade på en annons som är ett resultat av en nyckelordssökning efter&quot;läderskor&quot;, sedan klickade på en annons efter en nyckelordssökning efter&quot;suede skor&quot; och sedan gjorde en beställning. Du kan också se hur många konverteringar som gjordes efter att användarna klickade på annonser som är ett resultat av mer än 10 nyckelord.

Rapportresultaten innehåller aggregerade data för upp till de N tidigaste betalda söknyckelorden eller placeringsklickningarna i konverteringssökvägen som inträffade i annonserarens
klicka på fönster för uppslag och visningssökning. Om du till exempel väljer en banstorlek på fem (5) består rapporten av konverteringssökvägar som innehåller upp till de fem tidigaste nyckelorden eller placeringarna som fick klickningar, med en rad för varje mönster med klickningar spårade. Varje rad innehåller det första nyckelordet eller den första placeringen i sökvägen och det sista nyckelordet eller den sista placeringen som resulterade i konverteringar (även om det sista nyckelordet ligger utanför den angivna sökvägsstorleken). Som standard är raderna i stigande ordning efter antalet händelser i sökvägen.

>[!NOTE]
>
>Om rapporten innehåller placeringar från innehållsaktiverade sökkampanjer (som inte innehåller nyckelord), visar kolumnen [!UICONTROL Keyword] tillämpliga annonsgruppsnamn, t.ex. &quot;(adgroup-innehåll) Ditt annonsgruppsnamn.&quot;

Du kan också inkludera sammanställningskonverteringsdata för varje rad. När du tar med konverterings-/intäktskolumner i rapporten visas varje konverteringstyp i fyra kolumner, som visar a) det totala antalet konverteringar, b) procentandelen av de totala konverteringarna som har tilldelats det nyckelordsmönstret, c) den genomsnittliga fördröjningen i dagar från den första händelsen (för det första nyckelordet) till en konvertering och d) den genomsnittliga fördröjningen i dagar från den sista händelsen (för det sista nyckelordet) till en konvertering. När konverteringssökvägen innehåller fler nyckelord än den angivna sökvägsstorleken, innehåller rapporten ytterligare rader som samlar data för konverteringar som är ett resultat av det högre antalet nyckelord (till exempel alla mönster som innehöll klick på sex nyckelord).

Du kan visa data för de föregående 18 månaderna.

## Tillgängliga kolumner

Följande kolumner är tillgängliga för varje rapport. Standardkolumnerna inkluderas automatiskt som standard. Du kan lägga till tillgängliga anpassade kolumner från avsnittet Kolumner i rapportinställningarna.

| Kolumn | Standard? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] till [!UICONTROL 5th Keyword] | Standard | De fem tidigaste betalsöknyckelorden eller placeringsklickningarna i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönstret](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Obs!</b> Om rapporten innehåller placeringar från innehållsaktiverade sökkampanjer (som inte innehåller nyckelord), visar de här kolumnerna tillämpliga annonsgruppsnamn, till exempel &quot;(adgroup content) Ditt annonsgruppsnamn&quot; istället. |
| [!UICONTROL Path Size] | Standard | Antalet nyckelord och/eller placeringar i konverteringssökvägen som inträffade i annonsörens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Standard | Det första nyckelordet eller den första placeringen i konverteringssökvägen. |
| [!UICONTROL Last Keyword] | Standard | Det sista nyckelordet eller den placering som resulterade i konverteringar (även om det sista nyckelordet är utanför den angivna sökvägsstorleken). |
| \[Advertiser-specifika anpassade (härledda) mätvärden\] | Egen | Värdet för ett anpassat mätvärde som du har skapat och som beräknas utifrån befintliga mätvärden. |
| \[Advertiser-specifika konverteringsvärden\] | Egen | Antalet konverteringar för ett angivet konverteringsmått eller webbplatsengagemangsmått. |
| [!UICONTROL % of Total] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje konverteringsmått som ingår) Procentandelen av dina totala konverteringar mellan portföljer som tilldelats nyckelordet och/eller placeringsmönstret. |
| [!UICONTROL 6th Keyword] till [!UICONTROL 10th Keyword] | Egen | Det sjätte till tionde betalda söknyckelordet eller placeringsklickningen i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönstret](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Obs!</b> Om rapporten innehåller placeringar från innehållsaktiverade sökkampanjer (som inte innehåller nyckelord), visar de här kolumnerna tillämpliga annonsgruppsnamn, till exempel &quot;(adgroup content) Ditt annonsgruppsnamn&quot; istället. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje konverteringsmått som ingår) Genomsnittlig fördröjning i dagar från den första händelsen (på det första nyckelordet eller placeringen) till en konvertering. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningar, men inkluderas automatiskt i rapportutdata) Den genomsnittliga fördröjningen i dagar från den senaste händelsen (på det sista nyckelordet eller den sista placeringen) till en konvertering. |
| [!UICONTROL Path Frequency] | Egen | Antalet gånger som sökvägen för den här raden inträffade före konverteringen. |

>[!MORELIKETHIS]
>
>* [Om assistentrapporter](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Inställningar för assistentrapport](assist-report-settings.md)
>* [Generera en hjälprapport](assist-report-generate.md)
