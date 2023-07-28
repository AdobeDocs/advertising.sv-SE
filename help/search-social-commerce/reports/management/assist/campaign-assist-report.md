---
title: '[!UICONTROL Campaign Assist Report]'
description: Läs mer om [!UICONTROL Campaign Assist Report].
exl-id: 7fbc9c17-c77d-485b-8d51-5e5a153d7a2b
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# The [!UICONTROL Campaign Assist Report]

*Annonsörer med klickspårning i sökmotorkampanjer, sociala kampanjer och handelsklickningar och konverteringsspårning från Adobe Advertising, Adobe Analytics (med en [!DNL Analytics] integrering), eller tillhandahålls i feeds med en token (`ef_id`) only*

The [!UICONTROL Campaign Assist Report] anger vilka kampanjer som har hjälpt konverteringsprocessen. Rapporten visar hur varje kampanjmönster vars annonser ledde till en eller flera konverteringar har bidragit till era övergripande konverteringar. Du kan till exempel se hur många konverteringar som inträffade när användarna först såg en annons från Campaign A, sedan klickade på en annons från Campaign B och sedan lade en order. På samma sätt kan du se hur många konverteringar som har gjorts efter att användarna interagerat med annonser från mer än 10 kampanjer.

Rapportresultaten innehåller aggregerade data för varje kampanjmönster i konverteringsvägen - upp till N tidigaste kampanjer - för händelser som inträffat inom annonsören [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j). Om du till exempel väljer en sökvägsstorlek på fem (5) innehåller rapporten konverteringssökvägar som omfattar upp till de fem tidigaste kampanjerna, med en rad för varje mönster med kampanjer vars händelser spårades. Varje rad visar ett kampanjmönster, inklusive den första kampanjen i sökvägen och den sista kampanjen som resulterade i konverteringar (även om den sista kampanjen ligger utanför den angivna sökvägsstorleken). Som standard är raderna i stigande ordning efter antalet kampanjer i sökvägen.

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
| [!UICONTROL 1st Campaign] till [!UICONTROL 5th Campaign] | Standard | De fem tidigaste kampanjerna i konverteringsprocessen som inträffade inom annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter enhetsnamnet, inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Standard | Antalet kampanjer i konverteringsvägen som inträffade i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standard | Den första kampanjen i konverteringsvägen. |
| [!UICONTROL Last Campaign] | Standard | Den senaste kampanjen som resulterade i konverteringar (även om det sista nyckelordet ligger utanför den angivna sökvägsstorleken).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter enhetsnamnet, inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Advertiser-specifika anpassade (härledda) mätvärden\] | Egen | Värdet för ett anpassat mätvärde som du har skapat och som beräknas utifrån befintliga mätvärden. |
| \[Advertiser-specifika transaktionsegenskaper\] | Egen | Antalet konverteringar för en angiven transaktionsegenskap eller webbplatsengagemangsmått. |
| [!UICONTROL % of Total] \[transaktionsegenskap\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje transaktionsegenskap som ingår) Antalet konverteringar för en angiven transaktionsegenskap som är ett resultat av kampanjmönstret. |
| [!UICONTROL 6th Campaign] till [!UICONTROL 20th Campaign] | Egen | Den sjätte till den 20:e kampanjen i konverteringsprocessen som gjordes inom annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j).<br><br>Om du inkluderade något av rapportalternativen för att ange annonsnätverket, kontonamnet eller händelsetypen efter enhetsnamnet, inkluderas den informationen efter kampanjnamnet (till exempel `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[transaktionsegenskap\] | Automatisk | (Inte tillgängligt i rapportinställningarna, men inkluderas automatiskt i rapportutdata för varje transaktionsegenskap som ingår) Genomsnittlig fördröjning i dagar från den första händelsen (i den första kampanjen) till en konvertering. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[transaktionsegenskap\] | Automatisk | (Inte tillgängligt i rapportinställningar, men inkluderas automatiskt i rapportutdata) Genomsnittlig fördröjning i dagar från den senaste händelsen (i den senaste kampanjen) till en konvertering. |
| [!UICONTROL EF Campaign ID] | Egen | Det numeriska ID som tilldelas kampanjen av Search, Social och Commerce. |
| [!UICONTROL EF Portfolio Group ID] | Egen | Det numeriska ID:t för den portföljgrupp som portföljen tillhör. |
| [!UICONTROL EF Search Engine ID] | Egen | Det numeriska ID som tilldelas annonsnätverket i Search, Social och Commerce: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (borttagen), eller <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (föråldrat). |
| [!UICONTROL Portfolio ID] | Numeriskt portfölj-ID. |
| [!UICONTROL User SE Account ID] | Det numeriska ID som tilldelas annonsnätverket i Search, Social och Commerce. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Hjälp-rapporter](assist-report-about.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Inställningar för assistentrapporter](assist-report-settings.md)
>* [Generera en assistentrapport](assist-report-generate.md)
