---
title: Rapportkolumner för grundläggande och avancerade rapporter
description: Lär dig mer om tillgängliga datakolumner för grundläggande och avancerade rapporter.
exl-id: 649cdfa0-e6f2-4881-9f9d-8217e2547d99
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: 817c8ab0dce5412e4b3a235c3c032e5691d235ba
workflow-type: tm+mt
source-wordcount: '3806'
ht-degree: 0%

---

# Rapportkolumner för grundläggande och avancerade rapporter

| Kolumn | Beskrivning |
| ---- | ---- |
| \[Advertiser-specifika anpassade (härledda) mätvärden\] | Värdet för ett [anpassat mätvärde som du har skapat](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) som beräknas utifrån befintliga mätvärden. |
| \[Annonsspecifika etikettklassificeringar\] | Etikettklassificeringar som för närvarande används på enheten på entitetsnivå. Flera etikettklassificeringar avgränsas med kommatecken (,). |
| \[Advertiser-specifika konverteringsvärden\] | Antalet konverteringar för ett angivet konverteringsmått eller webbplatsengagemangsmått. |
| \[Google-spårade konverteringar\] | Se posten för &quot;GGL\*, GGL_CT\* och GGL_XD_CT\*.&quot; |
| [!UICONTROL 7-Day Click Accuracy] | ([!UICONTROL Portfolio Report]) Genomsnittlig noggrannhet för klickprognosen för de senaste sju dagarna, exklusive den aktuella dagen (och inte för rapportens angivna datumintervall), uttryckt i procent. |
| [!UICONTROL 7-Day Cost Accuracy] | ([!UICONTROL Portfolio Report]) Genomsnittlig noggrannhet för kostnadsprognosen för de föregående sju dagarna, exklusive den aktuella dagen (och inte för rapportens angivna datumintervall), uttryckt i procent. |
| [!UICONTROL 7-Day Revenue Accuracy] | ([!UICONTROL Portfolio Report]) Den genomsnittliga exaktheten i intäktsprognosen för de föregående sju dagarna, exklusive den aktuella dagen (och inte för rapportens angivna datumintervall), uttryckt i procent. |
| [!UICONTROL Account] | Kontonamnet. |
| [!UICONTROL Account Status] | Kontots status i Sök, Socialt och Commerce: <ul><li><i>[!UICONTROL Enabled]:</i> (Standard) För synkroniserade annonsnätverk kan Search, Social och Commerce logga in på annonsnätverkskontot för att hämta kampanjdata, och andra tillämpliga funktioner som optimering och spårningsgenerering är aktiverade.<br><br>För annonsnätverk som inte är synkroniserade finns det funktioner som optimering och/eller spårningsgenerering.</li><li><i>[!UICONTROL Disabled]:</i> För synkroniserade annonsnätverk loggar inte Search, Social och Commerce in på annonsnätverkskontot och hämtar därför inte kampanjdata, och andra tillämpliga funktioner som optimering och spårningsgenerering är inaktiverade. Data som samlas in medan kontot var aktiverat lagras fortfarande, men alla kampanjhanteringsvyer och alla rapporter som du skapar i framtiden inkluderar inte data för den tidsperiod under vilken kontot är inaktiverat.<br><br>För annonsnätverk som inte är synkroniserade är funktioner som optimering och/eller spårning inte tillgängliga.</li></ul> |
| [!UICONTROL Active Ad Groups] | Antalet aktiva annonsgrupper. |
| [!UICONTROL Active Ads/Creatives] | Antalet aktiva annonser/kreatörer. |
| [!UICONTROL Active Campaigns] | Antalet aktiva kampanjer. |
| [!UICONTROL Active Keywords] | Antalet aktiva nyckelord. |
| [!UICONTROL Ad Group] | Annonsgruppen. |
| [!UICONTROL Ad Group ID] | Det unika ID som identifierar en befintlig annonsgrupp. |
| [!UICONTROL Ad Group Status] | Annonsgruppens status: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Type] | Annonsgruppstypen, till exempel <i>[!UICONTROL Audience]</i> (endast för målgruppskampanjer), <i>[!UICONTROL Demand Gen]</i> (endast för efterfrågegångskampanjer), <i>[!UICONTROL Display]</i> (endast för displaykampanjer), <i>[!UICONTROL Search Dynamic]</i> (endast för dynamiska sökannonser), <i>[!UICONTROL Search Standard]</i> (endast för responsiva sökannonser och befintliga utökade textannonser), <i>[!UICONTROL Shopping Showcase]</i>, <i>[!UICONTROL Shopping Product]</i> (endast för standardshoppingkampanjer) eller <i>[!UICONTROL Shopping Smart]</i> (för smarta shoppingkampanjer). För vissa kampanjtyper kan en enda kampanj innehålla flera annonstyper. |
| [!UICONTROL Ad Groups] | Antalet annonsgrupper som etikettvärdet tilldelas till. |
| [!UICONTROL AD Name] | Annonsgruppens namn; samma värde som [!UICONTROL Ad Group]. |
| [!UICONTROL Ad Recall Lift] | ([!DNL Meta] kampanjer) Det uppskattade antalet personer som kommer ihåg din annons inom två dagar. |
| [!UICONTROL Ad Recall Rate] | ([!DNL Meta] kampanjer) Det uppskattade antalet personer som kommer ihåg din annons inom två dagar delat med det antal personer som du har nått, som en procentandel. |
| [!UICONTROL Ad Size] | Annonsens dimensioner. |
| [!UICONTROL AD Strength] | ([!DNL Google Ads] responsiva sökannonser) Annonsens effektivitet: <i>[!UICONTROL average]</i>, <i>[!UICONTROL excellent]</i>, <i>[!UICONTROL good]</i>, <i>[!UICONTROL no_ads]</i>, <i>[!UICONTROL pending]</i>, <i>[!UICONTROL poor]</i>, <i>[!UICONTROL unknown]</i> eller <i>[!UICONTROL unspecified]</i>. |
| [!UICONTROL Adgroup MBA] | ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] kampanjer) Aktuell mobilbudsjustering på annonsgruppsnivå, som avgör hur buden justeras när annonsen visas på en mobil enhet. |
| [!UICONTROL AI Max Bundling Required] | (Kampanjer som endast riktar sig till söknätverket, kampanjer med funktionen AI Max aktiverad, skrivskyddad) Om paketering krävs: *[!UICONTROL REQUIRED]*, *[!UICONTROL NOT_REQUIRED]*, *[!UICONTROL UNSPECIFIED]* eller null. |
| [!UICONTROL AI Max Enabled] | Om [[!UICONTROL AI Max]-funktionen ](https://support.google.com/google-ads/answer/15910366) är aktiverad: [!UICONTROL true]*, *[!UICONTROL false]* eller null. |
| [!UICONTROL AI Max Search Term Matching] | (Kampanjer som riktar sig till söknätverket och för vilka funktionen [AI Max](https://support.google.com/google-ads/answer/15910366) och söktermmatchningen på kampanjnivå är aktiverad; skrivskyddad) Om söktermmatchning på ad gruppnivå är aktiverad: *[!UICONTROL true]*, *[!UICONTROL false]* eller null. |
| [!UICONTROL Advertiser] | Annonsörens namn. |
| [!UICONTROL Advertiser ID] | Det numeriska ID:t för annonsörens konto Search, Social och Commerce. |
| [!UICONTROL Avg Position] | Den genomsnittliga positionen för annonserna under det angivna datumintervallet.<br><br>För [!DNL Google Ads]- och [!DNL Yahoo! Japan Ads]-kampanjer är dessa data bara tillgängliga till och med september 2019. För [!DNL Microsoft Advertising] är dessa data bara tillgängliga till och med den 22 januari 2021. |
| [!UICONTROL Base URL] | Bas-URL för nyckelordet, inklusive eventuella tilläggsparametrar som har konfigurerats för kampanjen eller kontot. Den innehåller ingen kod för omdirigering av sökningar, sociala medier och Commerce samt spårning. |
| [!UICONTROL Bid Strategy] | (De flesta annonsnätverk) För kampanjer eller kampanjkomponenter är detta kampanjens anbudsstrategi. För annonsnätverkskonton som är länkade till ett chefskonto är det här en strategi för bud mellan konton. Vilka värden som är tillgängliga varierar beroende på annonsnätverk. |
| [!UICONTROL Business Name] | ([!DNL Microsoft Advertising] responsiva annonser) Affärsnamnet. |
| [!UICONTROL Call to Action] | ([!DNL Microsoft Advertising] responsiva annonser och multimediaannonser) call to action ingår i annonsen. |
| [!UICONTROL Campaign] | Kampanjen. |
| [!UICONTROL Campaign Budget] | Kampanjbudgeten. |
| [!UICONTROL Campaign MBA] | ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] kampanjer) Aktuell mobilbudsjustering på kampanjnivå, som avgör hur buden justeras när annonsen visas på en mobil enhet. |
| [!UICONTROL Campaign Product Scope Filter] | (Kampanjer som endast använder shoppingnätverket) De produkter på ert handelskonto för vilka produktannonser kan skapas för kampanjen. |
| [!UICONTROL Campaign Start Date] | Den första dagen då anbud lämnades/delgavs kampanjen. |
| [!UICONTROL Campaign Status] | Kampanjstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> eller <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Campaign Type] | Kampanjtypen, till exempel <i>[!UICONTROL Audience (Ctv Video)]</i><i>[!UICONTROL Audience (Feed)]</i>, <i>[!UICONTROL Audience (Image)]</i>, <i>[!UICONTROL Audience (Video)]</i>, <i>[!UICONTROL Brand Shopping]</i>, <i>[!UICONTROL Demand Gen]</i>, <i>[!UICONTROL Search and Display]</i>, <i>[!UICONTROL Standard Display]</i>, <i>[!UICONTROL Standard Performance Max]</i>, <i>[!UICONTROL Standard Search]</i>, <i>[!UICONTROL Standard Shopping]</i>, <i>[!UICONTROL Store Ad]</i>, <i>[!UICONTROL Video]</i> eller <i>[!UICONTROL Others]</i>. |
| [!UICONTROL Channel Type] | Typen av marknadsföringskanal: <i>[!UICONTROL Search]</i> eller <i>[!UICONTROL Content]</i>. Den här kolumnen inkluderas inte när rapportens [!UICONTROL Search/Content]-inställning i rapportinställningarna är [!UICONTROL Combined]. |
| [!UICONTROL City] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Transaction Report]) En stad som klickningarna härstammar från. Den avgörs av användarens IP-adress. |
| [!UICONTROL Click Match Type] | Nyckelordsmatchningstypen för den annons som klickades. Detta är detsamma som [!UICONTROL Listing Match Type] förutom för [!DNL Microsoft Advertising]-nyckelord med flera matchningstyper. För nyckelord av typen [!DNL Microsoft Advertising] är detta den matchningstyp som användaren faktiskt klickade på. |
| [!UICONTROL Click Value] | ([!UICONTROL Portfolio Report]) Klickvärdet som har angetts för portföljens mål. |
| [!UICONTROL Click/Impression Time] | ([!UICONTROL Transaction Report]) Den tid då klickningen eller intrycket som orsakade konverteringen inträffade. |
| [!UICONTROL Clicks] | Antalet klick på annonser under det angivna datumintervallet. |
| [!UICONTROL Client ID1], [!UICONTROL Client Id 1] | ([!UICONTROL Keyword Report], [!UICONTROL Ad Variation Report] och [!UICONTROL Transaction Report]; implementeringar av flödesbaserad spårning) Ett klientspecifikt spårnings-ID för nyckelordet eller annonsen, som skickades i matningsfilen. |
| [!UICONTROL Client Id 2] | ([!UICONTROL Keyword Report] och [!UICONTROL Transaction Report]; implementeringar av flödesbaserad spårning) Ett klientspecifikt spårnings-ID för nyckelordet eller annonsen, som skickades i matningsfilen. |
| [!UICONTROL Client Transaction ID] | ([!UICONTROL Transaction Report]) Det unika transaktions-ID:t. |
| [!UICONTROL Constraint End Date] | ([!UICONTROL Constraint Report]) Den sista dagen som begränsningen är aktiv. |
| [!UICONTROL Constraint Name] | ([!UICONTROL Constraint Report]) Begränsningens namn. |
| [!UICONTROL Constraint Start Date] | ([!UICONTROL Constraint Report]) Den första dagen som begränsningen är aktiv. |
| [!UICONTROL Constraint Status] | ([!UICONTROL Constraint Report]) Begränsningens status: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Paused]</i>. |
| [!UICONTROL Constraint Type] | ([!UICONTROL Constraint Report]) Begränsningstypen: <i>[!UICONTROL Bid/Pos Constraint]</i>, <i>[!UICONTROL Bid Shift]</i>, <i>[!UICONTROL Campaign Budget]</i>, <i>[!UICONTROL Context Sensitive Bid]</i>, <i>[!UICONTROL Incremental Bidding]</i>, <i>[!UICONTROL Max CPA]</i>, <i>[!UICONTROL Min Margin]</i>, <i>[!UICONTROL Variable Bid Position]</i>, <i>[!UICONTROL Search Engine Min Bid]</i> eller <i>[!UICONTROL Variable Position]</i>. |
| [!UICONTROL Constraints] | Namnen på eventuella tillämpliga begränsningar för enheten, avgränsade med kommatecken. |
| [!UICONTROL Content IS] | Antalet visningar du fått för annonser på skärmen/målgruppsnätverket dividerat med det uppskattade antalet visningar som du var berättigad att ta emot. I [!DNL Microsoft Advertising] kallas detta [!UICONTROL Audience IS]. |
| [!UICONTROL Content IS Lost (budget)] | Den uppskattade procentandel av intryck som era annonser i nätverket för visning/målgrupper inte fick på grund av att er dagliga eller månadsvisa budget var för låg. I [!DNL Microsoft Advertising] kallas detta [!UICONTROL Audience lost IS (budget)]. |
| [!UICONTROL Content IS Lost (rank)] | Den uppskattade procentandel av visningar som era annonser i ert nätverk inte kunde visas på grund av dålig annonsrankning. I [!DNL Microsoft Advertising] kallas detta [!UICONTROL Audience lost IS (rank)]. |
| [!UICONTROL Conversion Type] | ([!UICONTROL Transaction Report]) De åtgärder som föregick konverteringen:<ul><li><i>[!UICONTROL Click:]</i> Minst en betald klickning inträffade före konverteringen.</li><li><i>[!UICONTROL Impression:]</i> Inga betalda klick inträffade före konverteringen, så konverteringen var ett resultat av en genomgång (utan några betalda klick).</li></ul> |
| [!UICONTROL Cost] | Den totala kostnaden för annonser under det angivna datumintervallet. |
| [!UICONTROL Country] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) Ett land som klickningarna härstammar från. Den avgörs av användarens IP-adress. |
| [!UICONTROL CPC] | Kostnaden per klick (CPC) för annonser under det angivna datumintervallet. |
| [!UICONTROL Creative Base URL] | Bas-URL:en för annonsen, inklusive eventuella tilläggsparametrar som har konfigurerats för kampanjen eller kontot. Den innehåller ingen kod för omdirigering av sökningar, sociala medier och Commerce samt spårning. |
| [!UICONTROL Creative Destination URL] | Den slutliga URL:en eller mål-URL:en (inklusive eventuella spårningsparametrar) för annonsen. |
| [!UICONTROL Creative Name] | ([!DNL Yahoo! Japan] endast) Annonsbildens namn. |
| [!UICONTROL Creative Title], [!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | Annonsens rubriker. Olika typer har olika antal obligatoriska och valfria rubrikrader. Om du vill visa [!UICONTROL Creative Title4] och högre kolumner i [!DNL Microsoft Advertising] responsiva annonser eller multimediaannonser tar du med kolumnen [!UICONTROL Creative Titles] i rapportinställningarna. |
| [!UICONTROL Creative Titles] | (Endast för multimedia och responsiva sökannonser) Lägger till en kolumn för var och en av annonsens korta rubriker (&quot;[!UICONTROL Creative Title]&quot; till &quot;[!UICONTROL Creative Title15]&quot;). När du tar med den här kolumnen behöver du inte ta med de andra [!UICONTROL Creative Title] kolumnerna, utan redigera avsnittet [!UICONTROL Order Results/Limit Rows By] för att sortera efter [!UICONTROL Creative Titles] i stället för [!UICONTROL Creative Title]. |
| [!UICONTROL Creative Type] | Annonsformatet. Följande är möjliga värden: <i>[!UICONTROL App Install Ad]</i>, <i>[!UICONTROL Call Only Ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (Carousel-annonser för flera bilder), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> och <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Display Ad]</i>, <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Legacy Text Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i>, <i>[!UICONTROL Responsive Ad]</i>, <i>[!UICONTROL Responsive Search Ad]</i> eller <i>[!UICONTROL Text Ad]</i>. |
| [!UICONTROL CTR] | Klickfrekvensen, som är antalet klick delat med antalet visningar för de annonser som ingår. |
| [!UICONTROL Currency] | Den tillämpliga valutatypen (t.ex. USD eller GBP).<br><br><b>Obs!</b> Om rapporten innehåller data för konton med olika valutor är alla [!UICONTROL Total]-monetära värden bara summan av alla tal i kolumnen, oavsett valuta. |
| [!UICONTROL Current Bid] | Aktuellt bud för målet. |
| [!UICONTROL Current First Page Bid] | (Endast [!DNL Google Ads] kampanjer) Det beräknade CPC-offert (cost-per-click) som krävs för att annonsen ska placeras på den första sidan i sökresultatet när en [!DNL Google] -sökfråga matchar nyckelordet.<br><br>För en enskild kombination av nyckelord och matchningstyp är det här värdet den första sidan som krävs för den kombinationen. När samma kombination av nyckelord och matchningstyp används i flera kampanjer är det här värdet det minsta anbudet på första sidan som för närvarande krävs för alla instanser. |
| [!UICONTROL Current Quality Score] | ([!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer) Aktuell kvalitetspoäng för nyckelordet eller budenheten, enligt annonsnätverkets beskrivning. Den varierar från 1 (låg) till 10 (perfekt). För en kombination av nyckelord och matchningstyp är det här värdet den aktuella poängen för den kombinationen. När samma kombination av nyckelord och matchningstyp används i flera kampanjer är det här värdet den högsta aktuella poängen bland alla instanser.<br><br>Annonsnätverken använder kvalitetspoängen för att fastställa budpriser och annonsposition. Det beräknas utifrån många faktorer, bland annat nyckelordets relevans för den associerade annonsen och användarens sökfråga och landningssidans kvalitet. För nyckelord i [!DNL Google Ads] beaktas även nyckelordets klickfrekvens, och för nyckelord i [!DNL Microsoft Advertising] beaktas även användarupplevelsen som tillhandahålls av landningssidan. |
| [!UICONTROL Custom Bid Level] | (Google-kampanjer som endast riktar sig till visningsnätverket) På vilken nivå budskapen ska placeras: av <i>[!UICONTROL Ad Group]</i>, <i>[!UICONTROL Age]</i>, <i>[!UICONTROL Gender]</i>, <i>[!UICONTROL Interest and List]</i>, <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i>, <i>[!UICONTROL Vertical]</i>, <i>[!UICONTROL None]</i> eller <i>[!UICONTROL Unknown]</i>. |
| [!UICONTROL Description1] - [!UICONTROL Description4] | Annonsens brödtext. Olika typer har olika antal obligatoriska och valfria beskrivningsrader. Om du vill visa [!UICONTROL Description3] och [!UICONTROL Description4] kolumner i [!DNL Microsoft Advertising] responsiva annonser eller multimediaannonser tar du med kolumnen [!UICONTROL Descriptions] i rapportinställningarna. |
| [!UICONTROL Descriptions] | ([!DNL Microsoft Advertising] responsiva annonser och multimediaannonser) Lägger till en kolumn för var och en av annonsens beskrivningsrader (&quot;[!UICONTROL Description1]&quot; till &quot;[!UICONTROL Description4]&quot;). När du tar med den här kolumnen behöver du inte ta med de andra [!UICONTROL Description] kolumnerna. |
| [!UICONTROL Device] | ([!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads] och [!DNL Yahoo Native] kampanjer) Enhetstypen som annonserna visades på: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> eller <i>[!UICONTROL N/A]</i> (inget värde). Rader för andra annonsnätverk har värden för N/A.<br><br>Om spårningsmallarna eller mål-URL:erna för nyckelorden, annonserna och/eller annontilläggen innehåller parametrar för att spåra data per enhet (`&ev_dvc={device}&ev_dvm={devicemodel}`) vid den tidpunkt då annonsen klickades, inkluderas även konverteringsdata på raden för varje enhetstyp. Annars, om konverteringsdata inte kan tilldelas en enhetstyp, aggregeras de i en separat rad med värdet [!UICONTROL Device] för [!UICONTROL N/A]. |
| [!UICONTROL Display Path 1] | ([!DNL Google Ads] utökad text lägger endast till) Den första visningssökvägen efter annonsens bas-URL. |
| [!UICONTROL Display Path 2] | ([!DNL Google Ads] utökad text lägger endast till) Den andra visningssökvägen efter annonsens bas-URL. |
| [!UICONTROL Display Type] | Föråldrad |
| [!UICONTROL Display URL] | Webbadressen för annonsen, vilket är vad slutanvändarna ser i annonsen. |
| [!UICONTROL DMA] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) Ett numeriskt, angivet marknadsområde som klickningarna härstammar från (till exempel 751 för Denver). Den avgörs av användarens IP-adress. |
| [!UICONTROL Domain] | ([!UICONTROL Domain Referral Report], [!UICONTROL Keyword Report]) Domännamnet som klickningarna härstammar från. |
| [!UICONTROL eCPM] | Den faktiska CPM-kostnaden, eller den genomsnittliga kostnaden per 1 000 visningar under ett visst datumintervall. eCPM-värden beräknas för antingen CPM- eller CPC-kampanjer. |
| [!UICONTROL EF Campaign ID] | Det numeriska ID som tilldelas kampanjen av Search, Social och Commerce. |
| [!UICONTROL EF ID] | ([!UICONTROL Transaction Report]) (Annonsörer med Adobe Advertising-tjänsten för konverteringsspårning och spårningsmetoden [!UICONTROL EF Redirect] med en token) Token för klickningen eller konverteringen.<ul><li>För [!DNL Google Ads] sökannonser är EF-ID `{gclid}:G:s`, som innehåller Google Click ID (GCLID) och nätverkstypen (&quot;s&quot; för sökning).</li><li> För [!DNL Microsoft Advertising] sökannonser är EF-ID `{msclkid}:G:s`, som innehåller Microsoft Click ID (MSCLKID) och nätverkstypen (&quot;s&quot; för sökning).</li><li>För sökannonser i andra annonsnätverk innehåller EF-id:t surfer-ID, klickningstid och nätverkstyp.</li><li>För displayannonser innehåller EF-ID:t surfer-ID, klicknings- eller intryckstidpunkt samt nätverkstyp.</li></ul> |
| [!UICONTROL EF Pixel Location ID] | ([!UICONTROL Geo Distribution Report]; endast för Search, Social och Commerce) Ett internt ID för geografisk plats, som används för att normalisera data. |
| [!UICONTROL EF Portfolio Group ID] | Det numeriska ID:t för den portföljgrupp som portföljen tillhör. |
| [!UICONTROL EF Search Engine ID] | Det numeriska ID som tilldelas annonsnätverket <i>[!UICONTROL 3]</i> för [!DNL Google Ads], <i>[!UICONTROL 10]</i> för [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> för [!DNL Meta], <i>[!UICONTROL 86]</i> för [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> för [!DNL Naver], <i>[!UICONTROL 88]</i> för [!DNL Baidu], <i>[!UICONTROL 90]</i> för [!DNL Yandex], <i>[!UICONTROL 94]</i> för [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> för [!DNL Yahoo Native] (utgått) eller <i>[!UICONTROL 106]</i> för [!DNL Pinterest] (utgått). |
| [!UICONTROL End Date] | Den sista dagen som rapporterades. |
| [!UICONTROL Engagement Rate] | (Videoannonser) Antalet ärenden delat med det antal gånger din annons visades. |
| [!UICONTROL Engagements] | (Videoannonser) Antalet gånger som användarna har tittat på din annons i minst 10 sekunder, eller hela annonsen om den är kortare än 10 sekunder. |
| [!UICONTROL Est. Clicks] | ([!UICONTROL Geo Distribution Report]; endast sök- och displaykampanjer) Det uppskattade antalet klick för kombinationen annonsgrupp/kampanj/portfölj. Detta värde kan skilja sig från värdet som anges av annonsnätverken. |
| [!UICONTROL Estimated Cost] | Den totala uppskattade kostnaden för associerade annonser som Search, Social och Commerce har spårat. Detta värde kan skilja sig från värdet som anges av annonsnätverken. |
| [!UICONTROL Estimated Impressions] | (Endast displaykampanjer) Det uppskattade antalet annonsvisningar som Search, Social och Commerce har spårat. Det här värdet kan skilja sig från värdet för kolumnen [!UICONTROL Impressions] (om det är tillgängligt), som visar värdet som tillhandahålls av annonsnätverken. |
| [!UICONTROL Exclude (yes/no)] | Om budgivning är exkluderat (<i>[!UICONTROL Yes]</i>) eller om budgivning är tillåtet (<i>[!UICONTROL No]</i>) för annonser för matchande produkter. |
| [!UICONTROL First Page CPC] | (Endast Google-kampanjer) Kostnaden per klick (CPC) för annonser som visas på den första sidan i sökresultaten under det angivna datumintervallet. |
| [!UICONTROL Frequency] | ([!DNL Meta] endast kampanjer) Det genomsnittliga antalet gånger någon såg din annons. |
| `GGL*`, `GGL_CT*` och `GGL_XD_CT*` [[!DNL Google Ads] spårade konverteringar] | ([!DNL Google Ads] kampanjer i sök- och köpnätverk) [!DNL Google Ads]-spårade konverteringar, med upp till tre separata mått för varje konvertering:<ul><li>`GGL*` — (När du spårar det) Konverteringsvärdet för nyckelordet, med början med GL-prefixet (till exempel GL Purchase).</li><li>`GGL_CT*` - Antal konverteringar (antal), med början med prefixet &quot;GGL_CT&quot; (till exempel GGL_CT_Purchase).</li><li>`GGL_XD_CT*` — (När det är tillgängligt för konverteringstypen, när du spårar dem) Antalet (antalet) konverteringar mellan enheter, mätt med [!DNL Google Ads] som börjar med prefixet &quot;GGL_XD_CT_&quot; (till exempel GGL_XD_CT_Purchase).</li></ul><br>Varje konvertering registreras av anbudsenhet och klickdatum. Den är inte tillgänglig på händelsenivå. Mer information om [!DNL Google Ads]-spårade konverteringar finns i [[!DNL Google Ads] konverteringsdata i Sök, Socialt och Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md). |
| [!UICONTROL Impr. (Abs. Top) %] | ([!DNL Google Ads] endast) Procentandelen annonser som visas som första annons över resultaten av den organiska sökningen. |
| [!UICONTROL Impr. (Top) %] | ([!DNL Google Ads] endast) Procentandelen annonser som visas ovanför de organiska sökresultaten. |
| [!UICONTROL Impressions] | Antal annonsvisningar under det angivna datumintervallet. |
| [!UICONTROL Interaction Rate] | (Videoannonser) Antalet interaktioner dividerat med antalet gånger som annonsen (video- och miniatyrbilder) visades. |
| [!UICONTROL Interactions] | (Videoannonser) Antal gånger som folk tittade på din annons. |
| [!UICONTROL Is_Click_Objectives] | ([!UICONTROL Portfolio Report]) <i>true</i> när portföljen innehåller kampanjer med anbudsstrategin [!UICONTROL Maximize Clicks], i annat fall <i>false</i>. |
| [!UICONTROL Keyword] | Nyckelordet.<br><br><b>Obs!</b> Om rapporten innehåller data från annonsgrupper i innehållsanpassade sökkampanjer, innehåller den här kolumnen tillämpliga annonsgruppsnamn som &quot;(adgroup content) Ditt annonsgruppsnamn.&quot; Den här kolumnen har inget värde för en webbplatsriktad placering i en sökkampanj. |
| [!UICONTROL Keyword ID] | Det unika ID som identifierar ett befintligt nyckelord. |
| [!UICONTROL Keyword Status] | Status för det nyckelord som söktermen matchades mot: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Deleted]</i> eller <i>[!UICONTROL Disapproved]</i>. |
| [!UICONTROL Label Classification] | ([!UICONTROL Label Classification Report] och [!UICONTROL Label Value Report]) Etikettklassificeringen. |
| [!UICONTROL Label Value] | ([!UICONTROL Label Classification Report] och [!UICONTROL Label Value Report]) Ett värde för etikettklassificeringen. |
| [!UICONTROL Language] | (Visningskampanjer) Målgruppens språk. |
| [!UICONTROL Link Type] | ([!UICONTROL Keyword Report]; [!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer endast; data är bara tillgängliga när den attribueringsregel som har angetts för rapporten är &quot;Last Event&quot;) När raden rapporterar en konvertering som ett resultat av ett klick på ett annonstillägg (i stället för på själva annonsen) eller på en produkt/shoppingannons, visar den här kolumnen typ och rubrik för en länk som du klickade på:<ul><li>`pla:*` - Produktannonser listas som `pla:<product ID>`, till exempel&quot;pla:8525822&quot;.</li><li>`sl:*` - Webbplatslänkar visas som `sl:<Sitelink text>`, till exempel&quot;sl:See Aktuella erbjudanden&quot;.</li></ul> |
| [!UICONTROL Listing Match Type] | Nyckelordsmatchningstypen för annonslistan, <i>[!UICONTROL Content]</i> för en annons i en innehållsanpassad kampanj eller <i>[!UICONTROL Sitecpc]</i> för en placering i en webbplatsanpassad kampanj. För nyckelord av typen [!DNL Microsoft Advertising] kan detta innehålla flera matchningstyper (till exempel [!UICONTROL Broad],[!UICONTROL Exact]). |
| [!UICONTROL Location] | (Visningskampanjer) Målgruppsplatser. |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | (I slutförda rapportrader för [!DNL Microsoft Advertising] responsiva annonser och multimediaannonser) De långa rubrikerna i annonsen. Om du vill visa de här kolumnerna inkluderar du kolumnen [!UICONTROL Long Creative Titles] i rapportinställningarna. |
| [!UICONTROL Long Creative Titles] | (För [!DNL Microsoft Advertising] responsiva annonser och multimediaannonser) Lägger till en kolumn för varje annons långa titlar (&quot;[!UICONTROL Long Creative Title1]&quot; till &quot;[!UICONTROL Long Creative Title5]&quot;). |
| [!UICONTROL Market Type] | Marknadstypen: <i>[!UICONTROL search]</i> eller <i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | (Kampanjer i portföljer med [!UICONTROL ROI], [!UICONTROL CPT] eller [!UICONTROL Marginal Cost per Transaction] utgiftsstrategier) Det maximala dagliga budgetmålet för portföljen. |
| [!UICONTROL Max Spend (%)] | ([!UICONTROL Network Constraint Report]) Den maximala procentandel av portföljens utgifter som har konfigurerats för annonsnätverket. För portföljer som använder begränsningstypen [!UICONTROL Min-Max] är detta [!UICONTROL Max %]-värdet. För portföljer som använder begränsningstypen [!UICONTROL Target Spend] är detta [!UICONTROL Target Spend]-värdet. |
| [!UICONTROL Method ID] | ([!UICONTROL Portfolio Report]) |
| [!UICONTROL Metro Code] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) En numerisk tunnelbanekod från vilken visningar eller klickningar härstammar (till exempel us-751 för Denver). Det bestäms av sökanvändarens IP-adress. |
| [!UICONTROL Min Spend (%)] | ([!UICONTROL Network Constraint Report]) Den minsta procentandel av portföljens utgifter som har konfigurerats för annonsnätverket. För portföljer som använder begränsningstypen [!UICONTROL Min-Max] är detta [!UICONTROL Min %]-värdet, om [!UICONTROL Min %] är konfigurerat. För portföljer som använder begränsningstypen [!UICONTROL Target Spend] är detta [!UICONTROL Target Spend]-värdet. |
| [!UICONTROL Network Account ID] | Konto-ID som tilldelats av nätverket. |
| [!UICONTROL Network Ad Group ID] | Annonsgrupps-ID som tilldelats av nätverket. |
| [!UICONTROL Network Campaign ID] | Kampanj-ID som tilldelats av nätverket. |
| [!UICONTROL Network Campaign Objective] | ([!DNL Meta] kampanjer) Målet för kampanjen. |
| [!UICONTROL Objective Name] | Portföljens mål. |
| [!UICONTROL Objective Value] | Den totala viktade konverteringen enligt portföljens aktuella mål. |
| [!UICONTROL Objective Value Calculation] | Den beräkning som används för att härleda målvärdet. |
| [!UICONTROL Outbound Clicks] | ([!DNL Meta] kampanjer) Antalet klick på länkar i annonser som tar bort personer som tillhör [!DNL Meta]. |
| [!UICONTROL Parent Product Groupings] | Den fullständiga hierarkin för de överordnade produktgrupperna, med `>>` mellan skikt (till exempel `All Products>>CategoryL1=Animals`), om tillämpligt. |
| [!UICONTROL Partition Type] | Typen av produktgrupp: <i>[!UICONTROL Sub-Division]</i> (överordnade produktgrupper) eller <i>[!UICONTROL Unit]</i> (den lägsta nivån av underordnade produktgrupper, som har ett bud). |
| [!UICONTROL Path Position] | ([!UICONTROL Transaction Report]) Händelsens position i konverteringssökvägen. |
| [!UICONTROL Path Total] | ([!UICONTROL Transaction Report]) Det totala antalet händelser för sökvägspositionen. |
| [!UICONTROL Portfolio] | Portföljen. |
| [!UICONTROL Portfolio Count] | ([!UICONTROL Portfolio Report]) Antalet portföljer som är associerade med ett mål. <!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | Namnet på den portföljgrupp som portföljen tillhör. |
| [!UICONTROL Portfolio ID] | Numeriskt portfölj-ID. |
| [!UICONTROL Portfolio Spend Strategy] | ([!UICONTROL Portfolio Report]) Utgiftsstrategin för portföljen: <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly]</i>, <i>[!UICONTROL Monthly]</i>, <i>[!UICONTROL ROI]</i>, <i>[!UICONTROL Day of week]</i>, <i>[!UICONTROL Day of month]</i>, <i>[!UICONTROL CPT]</i>, <i>[!UICONTROL Marginal CPT]</i>, <i>[!UICONTROL Google Target CPA]</i> eller <i>[!UICONTROL Google Target ROAS]</i>. |
| [!UICONTROL Portfolio Status] | Portföljens status:<ul><li><i>[!UICONTROL Optimize]:</i> Optimeringsfunktionen samlar in klicknings- och intäktsdata för relevanta kampanjer, modellerar data som används för optimering och optimerar bud, kampanjbudgetar och strategiska mål för kampanjbud (beroende på optimeringstyp och anbudsstrategier).</li><li><i>[!UICONTROL Active]:</i> Optimeringsfunktionen samlar in klicknings- och intäktsdata för relevanta kampanjer och modellerar data, men optimerar inte offerter eller kampanjbudgetar.</li><li><i>[!UICONTROL Inactive]:</i> Optimeringsfunktionen samlar in klickdata för relevanta kampanjer i rapporteringssyfte, men den modellerar inte data och optimerar inte offerter eller kampanjbudgetar.</li></ul> |
| [!UICONTROL Portfolio Target] | ([!UICONTROL Portfolio Report]) Det dagliga målet för portföljens utgiftsstrategi. För varje dag/månad och dag i vecka/månad visas den aktuella dagens mål. |
| [!UICONTROL Preferred Devices] | ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] kampanjer) Om annonsinställningarna ger företräde åt <i>[!UICONTROL Mobile ads]</i> eller <i>[!UICONTROL All ads]</i>. |
| [!UICONTROL Product Group ID] | Det numeriska ID som annonsnätverket tilldelar produktgruppen. |
| [!UICONTROL Product Group Name] | Produktgruppens namn. |
| [!UICONTROL Product Group Status] | Produktgruppens status. |
| [!UICONTROL Product Groupings] | Den överordnade produktgruppen. |
| [!UICONTROL Product ID] | ([!UICONTROL Keyword Report]; [!DNL Google Ads] produktlistor annonserar) Produkt-ID för produkten som visas med annonsen.<br><br><b>Obs!</b> ID:t registreras bara när produktlistan innehåller spårningsparametern `ev_plx=<GMC product ID>` som du måste lägga till i [!DNL Google Merchant Center]. |
| [!UICONTROL Raw Transaction Data] | ([!UICONTROL Transaction Report]) Inkomsterna för konverteringsmåttet (till exempel 1 för en registrering eller 12 för en 12 USD-order). Om flera budenheter har samma transaktions-ID delas intäkten för spårnings-ID upp efter antalet klick på det angivna klickdatumet (när klickdata är tillgängliga). |
| [!UICONTROL Reach] | ([!DNL Meta] endast kampanjer) Antalet personer som såg dina annonser minst en gång. Obs! [!DNL Meta] deduplicerar sträcker sig dagligen för användarprofiler, så de siffror som rapporteras av [!DNL Meta] och av Search, Social och Commerce kan skilja sig åt. |
| [!UICONTROL Region] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) En region eller delstat i USA/Kanada där visningar eller klickningar har sitt ursprung. Den avgörs av användarens IP-adress. |
| [!UICONTROL SE Creative ID] | Det annons-ID som tilldelats av nätverket. |
| [!UICONTROL Search (Abs. Top) IS] | ([!DNL Google Ads] och [!DNL Microsoft Advertising]) De avbildningar du har fått på den absolut översta platsen (den första och över resultaten av organiska sökningar) dividerat med det uppskattade antalet visningar du var berättigad att ta emot på den översta platsen. Procenttal under 10 % anges som `<10%` eller `0.0999`. |
| [!UICONTROL Search (Top) IS] | ([!DNL Google Ads] och [!DNL Microsoft Advertising]) De avbildningar du har fått på de översta platserna (ovanför resultaten av den organiska sökningen) dividerat med det uppskattade antalet visningar du var berättigad att ta emot på de översta platserna. Procenttal under 10 % anges som `<10%` eller `0.0999`. |
| [!UICONTROL Search Engine] | Annonsnätverket. |
| [!UICONTROL Search exact match IS] | Antalet visningar du fått för sökningar som exakt matchade ditt nyckelord delat med det uppskattade antalet exakta matchningsavbildningar som du var berättigad till. Om det här antalet är lågt kan det bero på att ditt bud är för lågt eller att annonskvaliteten eller relevansen är låg. |
| [!UICONTROL Search impr. share] | ([!DNL Google Ads] endast) De avbildningar du har fått divideras med det beräknade antalet visningar du har fått. Procenttal under 10 % anges som &lt;10 %&quot; och procenttal över 90 % anges som `>90%`. |
| [!UICONTROL Search lost abs. top IS (budget)] | ([!DNL Google Ads] och [!DNL Microsoft Advertising]) Den procentandel av tiden som dina annonser inte var de allra första annonserna ovanför resultaten av organiska sökningar eftersom din dagliga eller månadsvisa budget var för låg. För Google-annonskampanjer anges procenttal över 90 % som `>90%` eller `0.9001`. |
| [!UICONTROL Search lost abs. top IS (rank)] | ([!DNL Google Ads] och [!DNL Microsoft Advertising]) Den procentandel av tiden som dina annonser inte var de första annonserna ovanför de organiska sökresultaten på grund av dålig annonsrankning. För Google-annonskampanjer anges procenttal över 90 % som `>90%` eller `0.9001`. |
| [!UICONTROL Search lost IS (budget)] | ([!DNL Google Ads] endast) Den procentandel av tiden som dina annonser inte visades eftersom din dagliga eller månadsvisa budget var för låg. Det här måttet är endast tillgängligt på kampanjnivå. Procenttal över 90 % anges som `>90%` eller `0.9001`. |
| [!UICONTROL Search lost IS (rank)] | ([!DNL Google Ads] endast) Den procentandel av tiden som dina annonser inte visades på grund av dålig annonsrankning. Procenttal över 90 % anges som `>90%` eller `0.9001`. |
| [!UICONTROL Search lost top IS (budget)] | ([!DNL Google Ads] och [!DNL Microsoft Advertising]) Den procentandel av tiden som dina annonser inte visades ovanför de organiska sökresultaten eftersom din dagliga eller månadsvisa budget var för låg. För [!DNL Google Ads] kampanjer anges procentsatser över 90 % som `>90%` eller `0.9001`. |
| [!UICONTROL Search lost top IS (rank)] | ([!DNL Google Ads] och [!DNL [!DNL Microsoft Advertising]]) Den procentandel av tiden som dina annonser inte visades ovanför de organiska sökresultaten på grund av dålig annonsrankning. För Google-annonskampanjer anges procenttal över 90 % som `>90%` eller `0.9001`. |
| [!UICONTROL Search Term] | ([!UICONTROL Transaction Report]) Sökordet som användaren frågade efter. |
| [!UICONTROL SETrackingOnly] | Om du spårar kontot men inte placerar bud: <i>[!UICONTROL TRUE]</i> eller <i>[!UICONTROL FALSE]</i>. |
| [!UICONTROL Site] | (Domänreferensrapport och [!UICONTROL Keyword Report]; webbplatsriktade placeringar) Den webbplats som klickningarna härstammar från. |
| [!UICONTROL Start Date] | Första dagen som rapporterades. |
| [!UICONTROL State] | (Geo-distributionsrapport, [!UICONTROL Keyword Report]) Ett tillstånd som transaktionen härstammar från. Den avgörs av användarens IP-adress. |
| [!UICONTROL Surfer ID] | ([!UICONTROL Transaction Report]) ID:t för användaren som slutförde transaktionen. |
| [!UICONTROL Thru Plays] | (Endast [!DNL Meta] kampanjer) Antalet visningar som tittade på annonsen i sin helhet. |
| [!UICONTROL Top of Page CPC] | (Endast Google-kampanjer) Kostnaden per klick (CPC) för annonser som visas högst upp på sökresultatsidorna under det angivna datumintervallet. |
| [!UICONTROL Tracking URL] | (Endast sökriktade nyckelord) Spårningsmallen eller mål-URL:en som är inbäddad med (om tillämpligt) Sökning-, Socialkod och spårningskod för Commerce. |
| [!UICONTROL Transaction Property Name] | ([!UICONTROL Transaction Report]) Det annonsörspecifika konverteringsmått som transaktionen krediteras till. |
| [!UICONTROL Transaction Time] | ([!UICONTROL Transaction Report]) Den tidpunkt då det angivna konverteringsmåttet krediterades. |
| [!UICONTROL Two Second Continuous Video Plays] | (Endast [!DNL Meta] kampanjer) Antalet gånger som videon spelades upp i minst två sammanhängande sekunder. |
| [!UICONTROL User Account Type] | Föråldrad |
| [!UICONTROL User SE Account ID] | Det numeriska ID som tilldelas annonsnätverket av Search, Social och Commerce. |
| [!UICONTROL Video Average Play Time] | (Endast [!DNL Meta] kampanjer) Genomsnittlig tid för uppspelning av en video, inklusive den tid som användes för att spela upp videon, för ett enda intryck. |
| [!UICONTROL Video Plays] | (Endast [!DNL Meta] kampanjer) Antalet gånger som videon börjar spelas upp, exklusive återspelningar. |
| [!UICONTROL Video Played at 25 Percent Count], [!UICONTROL Video Played at 50 Percent Count], [!UICONTROL Video Played at 75 Percent Count] och [!UICONTROL Video Played at 100 Percent Count] | (Videoannonser) Antalet videor som spelades upp 25 %, 50 %, 75 % eller 100 % av vägen igenom. |
| [!UICONTROL VideoQuartile25Rate], [!UICONTROL VideoQuartile50Rate], [!UICONTROL VideoQuartile75Rate] och [!UICONTROL VideoQuartile100Rate] | (Videoannonser) Procentandel videor som spelades upp 25 %, 50 %, 75 % eller 100 % av vägen igenom. |
| [!UICONTROL View Rate] | (Videoannonser) Antalet visningar eller engagemang delat med antalet gånger som annonsen (video- och miniatyrbilder) visades. |
| [!UICONTROL Views] | (Videoannonser) Antal gånger som personer har tittat på eller deltagit i annonsen. |
| [!UICONTROL ViewThroughConversions] | (Annonser i målgruppsnätverket) Antalet konverteringar som är resultatet av en eller flera visningar, men utan klick. |

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [Om grundläggande och avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Generera en enkel eller avancerad rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Grundläggande och avancerade rapportinställningar](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
