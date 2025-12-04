---
title: '[!UICONTROL Campaign Assist Report]'
description: Läs mer om [!UICONTROL Campaign Assist Report].
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# [!UICONTROL Campaign Assist Report]

*Annonsörer med klickspårning i Sök, Socialt och Commerce och med konverteringsspårning från Adobe Advertising, Adobe Analytics (med integrering av [!DNL Analytics]) eller som tillhandahålls i feeds med en token (`ef_id`) endast*

[!UICONTROL Campaign Assist Report] visar vilka kampanjer som har hjälpt till med konverteringsprocessen. Rapporten visar hur varje kampanjmönster vars annonser ledde till en eller flera konverteringar har bidragit till era övergripande konverteringar. Du kan till exempel se hur många konverteringar som inträffade när användarna först såg en annons från Campaign A, sedan klickade på en annons från Campaign B och sedan lade en order. På samma sätt kan du se hur många konverteringar som har gjorts efter att användarna interagerat med annonser från mer än 10 kampanjer.

Rapportresultaten innehåller aggregerade data för varje mönster av kampanjer i konverteringssökvägen - upp till de N tidigaste kampanjerna - för händelser som inträffade i annonsörens [klickfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j). Om du till exempel väljer en sökvägsstorlek på fem (5) innehåller rapporten konverteringssökvägar som omfattar upp till de fem tidigaste kampanjerna, med en rad för varje mönster med kampanjer vars händelser spårades. Varje rad visar ett kampanjmönster, inklusive den första kampanjen i sökvägen och den sista kampanjen som resulterade i konverteringar (även om den sista kampanjen ligger utanför den angivna sökvägsstorleken). Som standard är raderna i stigande ordning efter antalet kampanjer i sökvägen.

Du kan också inkludera sammanställda konverteringsdata, inklusive anpassade värden, för varje rad. När du tar med kolumnerna för konverteringar/intäkter i rapporten visas varje konverteringstyp i fyra kolumner, som visar a) det totala antalet konverteringar, b) procentandelen av de totala konverteringarna som har tilldelats det kampanjmönstret, c) den genomsnittliga fördröjningen i dagar från den första händelsen (i den första kampanjen) till en konvertering och d) den genomsnittliga fördröjningen i dagar från den senaste händelsen (i den senaste kampanjen) till en konvertering. När konverteringsvägen omfattar fler kampanjer än den angivna sökvägsstorleken innehåller rapporten ytterligare rader som samlar data för konverteringar som är ett resultat av det högre antalet kampanjer (till exempel alla mönster som innehöll sex kampanjer).

Du kan även inkludera annonsnätverket och/eller händelsetypen efter kampanjnamnet, till exempel `<campaign name> (Google) click`.

Du kan visa data för de föregående 18 månaderna.

>[!TIP]
>
>Om era märkesnyckelord finns i en annan kampanj än era generiska nyckelord visar rapporten om era märkesnyckelord bidrar till konverteringarna.

## Tillgängliga kolumner

Följande kolumner är tillgängliga för varje rapport. Standardkolumnerna inkluderas automatiskt som standard. Du kan lägga till tillgängliga anpassade kolumner från avsnittet Kolumner i rapportinställningarna.

| Kolumn | Standard? | Beskrivning |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] till [!UICONTROL 5th Campaign] | Standard | De fem tidigaste kampanjerna i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsfönstret](/help/search-social-commerce/glossary.md#i-j).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter entitetsnamnet inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Google] [Account1] [impression]`). |
| [!UICONTROL Path Size] | Standard | Antalet kampanjer i konverteringssökvägen som inträffade i annonsörens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standard | Den första kampanjen i konverteringsvägen. |
| [!UICONTROL Last Campaign] | Standard | Den senaste kampanjen som resulterade i konverteringar (även om det sista nyckelordet ligger utanför den angivna sökvägsstorleken).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter entitetsnamnet inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Google] [Account1] [impression]`). |
| \[Advertiser-specifika anpassade (härledda) mätvärden\] | Egen | Värdet för ett anpassat mätvärde som du har skapat och som beräknas utifrån befintliga mätvärden. |
| \[Advertiser-specifika konverteringsvärden\] | Egen | Antalet konverteringar för ett angivet konverteringsmått eller webbplatsengagemangsmått. |
| [!UICONTROL % of Total] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje konverteringsmått som ingår) Antalet konverteringar för ett angivet konverteringsmått som ett resultat av kampanjmönstret. |
| [!UICONTROL 6th Campaign] till [!UICONTROL 20th Campaign] | Egen | Den sjätte till den 20:e kampanjen i konverteringssökvägen som inträffade i annonserarens [klickningsfönster](/help/search-social-commerce/glossary.md#c-d) och [visningsuppslagsfönster](/help/search-social-commerce/glossary.md#i-j).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter entitetsnamnet inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Baidu] [Account1] [click]`). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje konverteringsmått som ingår) Genomsnittlig fördröjning i dagar från den första händelsen (i den första kampanjen) till en konvertering. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[konverteringsmått\] | Automatisk | (Inte tillgängligt i rapportinställningar, men inkluderas automatiskt i rapportutdata) Genomsnittlig fördröjning i dagar från den senaste händelsen (i den senaste kampanjen) till en konvertering. |
| [!UICONTROL EF Campaign ID] | Egen | Det numeriska ID som tilldelas kampanjen av Search, Social och Commerce. |
| [!UICONTROL EF Portfolio Group ID] | Egen | Det numeriska ID:t för den portföljgrupp som portföljen tillhör. |
| [!UICONTROL EF Search Engine ID] | Egen | Det numeriska ID som tilldelas annonsnätverket <i>[!UICONTROL 3]</i> för [!DNL Google Ads], <i>[!UICONTROL 10]</i> för [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> för [!DNL Meta], <i>[!UICONTROL 86]</i> för [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> för [!DNL Naver], <i>[!UICONTROL 88]</i> för [!DNL Baidu], <i>[!UICONTROL 90]</i> för [!DNL Yandex], <i>[!UICONTROL 94]</i> för [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> för [!DNL Yahoo Native] (utgått) eller <i>[!UICONTROL 106]</i> för [!DNL Pinterest] (utgått). |
| [!UICONTROL Portfolio ID] | Egen | Numeriskt portfölj-ID. |
| [!UICONTROL User SE Account ID] | Egen | Det numeriska ID som tilldelas annonsnätverket av Search, Social och Commerce. |

>[!MORELIKETHIS]
>
>* [Om assistentrapporter](assist-report-about.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Inställningar för assistentrapport](assist-report-settings.md)
>* [Generera en hjälprapport](assist-report-generate.md)
