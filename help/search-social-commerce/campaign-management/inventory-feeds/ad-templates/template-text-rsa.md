---
title: Inställningar för textannonser och responsiva sökannonser för lagerflöden
description: Referera inställningarna för text och responsiva sökannonsmallar för lagerflöden.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# Inställningar för textannonser och responsiva sökannonser för lagerflöden


*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

>[!NOTE]
>
>* Följande tecken är reserverade för att ange kolumnnamn och modifieringsnamn i mallen och är därför inte tillåtna som text i alla attributfält: `[ ] < > `
>* I [!DNL Yandex templates] kan du bara använda de dynamiska parametrarna `{param1}` och `{param2}` i URL-adresser, och du kan inte använda dynamisk prisinfogning i annonsbeskrivningar.

## \[Ovanför alla flikar\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Vänster panel\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Valfritt) Mappar alla nya annonsgrupper (inte tillgängligt för [!DNL Yandex]), nyckelord och annonser till befintliga kampanjer, i stället för att skapa kampanjer. Om du aktiverar det här alternativet väljer du mappningsmetod.

Om du använder [!UICONTROL Map Only] på kampanjnivå krävs en befintlig kontostruktur som är nära kopplad till produkttaxonomin och som enkelt mappar till dataflödet.

**[!UICONTROL Map Method]:** (När [!UICONTROL Map Only] är aktiverat för kampanjen) Den metod som används för att mappa nya annonsgrupper (inte tillgängligt för [!DNL Yandex]), nyckelord och annonser till befintliga kampanjer:

* *[!UICONTROL Contains Anywhere]:* Lägger till data i en befintlig kampanj vars namn innehåller den angivna strängen, om den finns.

* *[!UICONTROL Contains Exactly]:* Lägger till data i en befintlig kampanj vars namn innehåller den angivna strängen, om den finns.

* *[!UICONTROL Exactly Matches]* (standardvärdet): Lägger till data i en befintlig kampanj med samma namn, om det finns.

Om ingen matchning hittas ignoreras alla data för kampanjen. Om det finns flera kampanjmatchningar mappas nyckelorden och annonserna till alla.

**[!UICONTROL Campaign Tracking Template]:** (Endast konton med slutliga/avancerade URL:er; valfritt) Spårningsmallen på kampanjnivå, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Det här värdet åsidosätter inställningen på kontonivå, men spårningsmallar på mer detaljnivå (med nyckelordet längst granulat) åsidosätter det här värdet.

* För spårning av konvertering av Adobe Advertising, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs kod för omdirigering och spårning automatiskt till när du sparar posten.

* Så här bäddar du in den slutliga URL:en:

   * ([!DNL Google Ads] och endast [!DNL Microsoft Advertising]) En lista med parametrar som anger de slutliga URL:erna i spårningsmallar finns i [!DNL Microsoft Advertising]-dokumentationen [[!DNL Microsoft Advertising] eller ([!DNL Google Ads] endast) i parametrarna för spårningsmallen i avsnittet Tillgängliga [!DNL ValueTrack]-parametrar i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/6305348).](https://help.ads.microsoft.com/#apex/3/en/56799/2)

   * ([!DNL Yahoo! Japan Ads] endast) Använd parametern `!{unescapedurl}` för att ange landningssidans URL.

   * Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel `{lpurl}?matchtype={matchtype}&device={device}`.

* Ange ett värde för omdirigeringar och spårning från tredje part.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (I [!DNL Google Ads] och [!DNL Yandex] kampanjinställningar) De nätverk där annonser ska placeras:

* *[!UICONTROL Search]:* Om du vill lägga bud på listor med sponsrade sökningar.

  ([!DNL Google Ads] kampanjer) Markera kryssrutan intill **[!UICONTROL Search partners]** om du vill inkludera bud på listor för [!DNL Google Ads] sökpartner.

* *[!UICONTROL Content]:* Om du vill lägga bud på placeringar i nätverkslistorna för innehåll (visning). **Obs!** Du kan inte skapa placeringar med mallen. När du väljer det här alternativet skapar du placeringar för varje annonsgrupp och anger vilka sidor i visningsnätverket som ska användas som mål för varje annonsgrupp med hjälp av antingen <!-- insert link --> eller <!-- insert links -->- och placeringsinställningarna i [!UICONTROL Search] > [!UICONTROL Campaigns] -vyerna.

**[!UICONTROL Languages]:** ([!DNL Google Ads] endast sök- och visningsnätverk) Ett eller flera målspråk för annonser i kampanjen.

[!DNL Google Ads] bestämmer en användares språk utifrån användarens [!DNL Google]-språkinställning eller språket för sökfrågan, den aktuella sidan eller nyligen visade sidor på [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Endast konton med slutliga/avancerade URL:er) Spårningsmallen på annonsgruppsnivå, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter.

För spårning av konvertering av Adobe Advertising, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs kod för omdirigering och spårning automatiskt till när du sparar posten.

Ange ett värde för omdirigeringar och spårning från tredje part. Ange landningssidans URL:

* För Yahoo! Japanska annonskonton använder parametern {lpurl}.

* Tillgängliga parametrar för Microsoft Advertising- och Google Ads-konton finns i [[!DNL Microsoft Advertising] dokumentationen](https://help.ads.microsoft.com/#apex/3/en/56799) eller i&quot;Endast spårningsmallen&quot; i avsnittet&quot;Tillgängliga [!DNL ValueTrack]-parametrar&quot; i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/6305348).

Det här värdet åsidosätter inställningarna på konto- och kampanjnivå, men spårningsmallar på mer detaljnivå (med nyckelordet som mest detaljerat) åsidosätter det här värdet.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Nyckelord för den angivna annonsgruppen (eller kampanj för [!DNL Yandex]-konton), som kan bestå av valfri kombination av statisk text, kolumner i den angivna filen och modifierare. Kolumnnamn och modifierare ersätts med faktiska data när den angivna feed-filen sprids via mallen.

Om du vill infoga ett kolumnnamn eller en modifieringsgrupp som en dynamisk parameter, klickar du i indatafältet och sedan på ett kolumnnamn i kolumnlistan eller ett [modifierarnamn](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) i listan Modifierare. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Om du vill ange matchningstyp för nyckelord använder du följande matchningstypssyntax runt kolumnnamnet:

* För mallarna [!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads]:

   * För dynamiska parametrar: Bred matchning = `[keyword]`, Bred Match Modifier för den första termen i kolumnen [!UICONTROL Keyword] (t.ex. +blå suede-skor) = `+[keyword]`, Bred Match Modifier för varje term i nyckelordskolumnen (t.ex. +blue +suede +skor) = `+[keyword]+`, Phrase Match = `"[keyword]"`, Exakt matchning = `[[keyword]]`

   * För statiska nyckelord: Bred matchning = `keyword`, Bred matchningsmodifierare = `+keyword` eller Frasmatchning = `"keyword"`

     Du kan inte ange statiska nyckelord med exakt matchning och standardmatchningssyntax här eftersom de omges av hakparenteser (`[]`), som dynamiska parametrar.

* För [!DNL Yandex]-mallar:

   * För dynamiska parametrar: Infoga kolumnnamnet, till exempel `[keyword]`. Använd den [[!DNL Yandex]-specifika syntaxen ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) om du vill ange matchningstypen. **Obs!** Använd följande syntax för breda matchningstermer: Bred Match Modifier för den första termen i nyckelordskolumnen (till exempel +blå suede-skor) = `+[keyword]`, Bred Match Modifier för varje term i nyckelordskolumnen (till exempel +blue +suede +skor) = `+[keyword]+`

   * För statiska nyckelord: Endast söknyckelord stöds. Använd den [[!DNL Yandex]-specifika syntaxen ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) för nyckelordet. Parenteser (`[]`) för att ange ordordning stöds inte.

>[!NOTE]
>
>* Du kan inkludera flera modifieringsvärden manuellt i fältet Nyckelord genom att omsluta kommaseparerade värden inom parentes, antingen före eller efter en nyckelordsparameter (men inte på båda ställena). `(cheap, discount, affordable)[product]` skapar till exempel tre separata annonser för varje produkt.
>* Om du inte anger någon matchningstyp används standardmatchningstypen &quot;Bred&quot;.
>* Negativa matchningar stöds inte.
>* Google breda matchningsmodifierare har nu samma matchande beteende som frasmatchning för vissa språk, och du kan inte skapa nya breda matchningsmodifieringsnyckelord. Mer information finns i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/10286719).

**[!UICONTROL Map Only]:** Lägger till nya annonser i annonsgrupper (eller i kampanjer för [!DNL Yandex]-konton) där de angivna nyckelorden hittas, i stället för att skapa nya nyckelord. Markera kryssrutan om du vill aktivera det här alternativet. När det här alternativet är aktiverat gäller inte någon Param 1- eller Param 2-variabel i de angivna nyckelorden eftersom nyckelorden finns.

**[!UICONTROL Keyword Final URL]:** (Konton med slutliga/avancerade URL:er; valfritt) Landningssidans URL som annonsnätverksanvändare tas till när de klickar på annonsen. Den måste innehålla samma domän som visnings-URL:en, och alla parametrar i den slutliga URL:en måste matcha parametrarna i landningssidans URL efter annonsklicket. Den kan innehålla omdirigeringar inom landningssidans domän eller underdomän, men inga omdirigeringar utanför landningssidans domän.

Om du använder en [!DNL Google Merchant Center]-feed och inkluderar det här värdet i kolumnen [!DNL Link] infogar du den kolumnen i det här fältet.

>[!NOTE]
>
>* Om du genererar spårnings-URL:er när du bokför data som sprids via mallen, läggs spårningsparametrar till i det här värdet baserat på kontospårningsinställningarna.
>* ([!DNL Google Ads] konton) Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

**[!UICONTROL Keyword Tracking Template]:** (Konton med slutliga/avancerade URL:er; valfritt) Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårar parametrar och bäddar in den slutliga URL:en i en parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet som det mest granulerade) åsidosätter värden på alla andra nivåer.

* För spårning av konvertering av Adobe Advertising, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs kod för omdirigering och spårning automatiskt till när du sparar posten.

* Du kan även ange omdirigeringar och spårning från tredje part.

* Ange landningssidans URL:

   * ([!DNL Google Ads] och endast [!DNL Microsoft Advertising]) En lista med parametrar som anger de slutliga URL:erna i spårningsmallar finns i [!DNL Microsoft Advertising]-dokumentationen [[!DNL Microsoft Advertising] eller ([!DNL Google Ads] endast) i parametrarna för spårningsmallen i avsnittet Tillgängliga [!DNL ValueTrack]-parametrar i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/6305348).](https://help.ads.microsoft.com/#apex/3/en/56799)

   * ([!DNL Yahoo! Japan Ads] endast) Använd parametern `!{lpurl}` för att ange landningssidans URL.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] mallar\]:** ([!DNL Google Ads] endast mallar) Kolumnen i den angivna filen som representerar variabeln [!DNL Google Ads] `{param1}` eller `{param2}`, som du kan ta med i annonskopian eller visa URL:en för alla annonser som skapats från mallen. Om du vill infoga den dynamiska parametern klickar du i inmatningsfältet och sedan på ett kolumnnamn i kolumnlistan. Kolumnnamnet ersätts med faktiska data när feed-filen sprids via mallen.

Om du använder någon av parametrarna kan du välja att bara använda parametern för nya nyckelord eller att även uppdatera värdena för befintliga nyckelord som inte har skapats från mallen:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (standardvärdet): infogar bara värdet för parametern för nya nyckelord som skapas med mallen.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Förutom att skapa nya nyckelord från feeden uppdaterar Search, Social och Commerce även värdet på parametern för alla befintliga nyckelord i annonsgruppen som inte skapades med mallen. Ange ett numeriskt värde som används för alla dessa nyckelord. Mallen måste innehålla minst ett nyckelord.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Förutom att skapa nya nyckelord från feeden uppdaterar Search, Social och Commerce även värdet på parametern för alla befintliga nyckelord i annonsgruppen som inte skapades med mallen så länge feedsfilen innehåller numeriska värden för parametern, med upp till en decimalpunkt men utan kommatecken, valutasymboler eller koder, eller andra tecken. Det lägsta värdet för parametern i feed-filen används för alla befintliga nyckelord. Om till exempel matningsfilen har [!UICONTROL Param1] värden på 21500 och 22000 ändras [!UICONTROL Param1] -värdena för befintliga nyckelord till 21500. Mallen måste innehålla minst ett nyckelord. **Tips!** Använd bara det här alternativet om du har tätt sammansatta annonsgrupper så att det blir bra att ha samma värde för nyckelord.

Datafälten i matningsfilen får innehålla högst 25 tecken och får endast bestå av numeriska data med följande icke-numeriska tecken:

* (När du använder parametern [!UICONTROL Apply to Existing Keywords: Min]) Endast upp till en decimalpunkt.

* (När du inte använder parametern [!UICONTROL Apply to Existing Keywords: Min]):

   * Värdet kan föregås eller läggas till med en valutasymbol eller valutakod. Exempel: 2 000, 00 och 2 000 GBP är giltiga.

   * Värdet kan innehålla kommatecken (,) eller punkt (.) som avgränsare, med en valfri punkt (.) eller komma (,) för decimalvärden. Exempel: 1,000.00 och 2.000,10 är giltiga.

   * Värdet kan prefixeras eller läggas till med ett procenttecken (%), plustecken (+) eller minustecken (-). Till exempel är 20 %, 208+ och -42.32 giltiga.

   * Två tal kan bäddas in med ett snedstreck. 4/1 och 0.95/0.45 är till exempel giltiga.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] mallar\]:** ([!DNL Microsoft Advertising] endast mallar) Den sträng som ska användas som ersättningsvärde i en annons om titeln, texten, URL:en för visning eller den slutliga URL:en innehåller den dynamiska ersättningssträngen `{Param2}` . Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (en annonsrubrik kan till exempel innehålla upp till 25 tecken).

**[!UICONTROL Param 3]:** ([!DNL Microsoft Advertising] endast mallar) Den sträng som ska användas som ersättningsvärde i en annons om titeln, texten, URL:en eller den slutliga URL:en innehåller den dynamiska ersättningssträngen `{Param3}`. Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (en annonsrubrik kan till exempel innehålla upp till 25 tecken).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** Det inledande budet för varje nyckelord med den angivna matchningstypen eller annonstypen.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] och [!DNL Microsoft Advertising] endast kampanjer) Annonstypen: *[!UICONTROL Expanded Search Ads]* eller *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Valfritt) Fyller i alla alternativa fält och kopieringsfält med text från de ursprungliga kopieringsfälten.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Endast responsiva sökannonser) Annonspositionen där rubriken/rubriken måste inkluderas (till exempel [!UICONTROL Pinned at position 1]). Standardvärdet är [!UICONTROL Unpinned].

Det måste finnas minst en rubrik för varje position. Om du fäster flera titlar på samma plats, kommer den sista annonsen alltid att innehålla en av dessa titlar på den angivna positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (endast responsiva sökannonser) Annonsrubrikerna (rubriker). Varje annonsvariation måste innehålla minst tre, och upp till 15, annonsrubriker. Annonsnätverket visar annonser med upp till tre rubriker. Den maximala längden för varje rubrik är 30 tecken, inklusive all dynamisk text (t.ex. värdena för nyckelord och annonsanpassare).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Endast befintliga standardtextannonser i Microsoft Advertising, skrivskyddade) Rubriken, eller första raden, för en annons. Microsoft Advertising har ersatt framtagning och redigering av standardtexter.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] och [!DNL Yahoo! Japan Ads] endast utökade text- och mallar) Rubriken för en annons. Den maximala längden för varje rad (efter att alla dynamiska parametrar har ersatts) är 30 eller 15 dubbelbyte-tecken.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] enbart expanderade text- och mallar; valfritt) En tredje rubrik för en annons. Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 30 eller 15 dubbelbyte-tecken.

**[!UICONTROL Title]:** ([!DNL Yandex] endast) Rubriken, eller första raden, för en annons. Maximalt 33 tecken.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (endast utökade textannonser i Microsoft Advertising) Rubriken för en annons. Den maximala längden för varje rad (efter att alla dynamiska parametrar har ersatts) är 30 eller 15 dubbelbyte-tecken.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Endast utökade textannonser i Microsoft Advertising) En annons brödtext. Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 80 eller 40 dubbelbyte-tecken (till exempel kinesiska, japanska och koreanska).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Annonsens brödtext.

* (Google Ads expanderad text och mallar) Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 90 eller 45 dubbelbyte-tecken.

* (Yahoo! Japan Ads-mallar) Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 80 eller 40 dubbelbyte-tecken.

* (Yandex-mallar) Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 75 tecken och ett ord får inte innehålla fler än 22 tecken.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Endast responsiva sökannonser) Den annonsposition som beskrivningen måste inkluderas vid (till exempel [!UICONTROL Pinned at position 1]). Standardvärdet är [!UICONTROL Unpinned]. Minst en beskrivning måste finnas tillgänglig för varje position.

Om du fäster flera beskrivningar på samma plats, kommer den sista annonsen alltid att innehålla en av dessa beskrivningar på den angivna positionen. Beskrivningar som fästs vid position 2 kanske inte visas tillsammans med annonsen.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (endast responsiva sökannonser) Annonsbeskrivningarna. Varje annonsändring måste innehålla minst två och upp till fyra annonsbeskrivningar. Annonsnätverket visar annonser med upp till två beskrivningar. Ange minst två. Den maximala längden för varje beskrivning är 90 tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (endast utökade text- och mallar för Google, valfritt) En andra rad i annonsen. Den maximala längden (efter att alla dynamiska parametrar har ersatts) är 90 eller 45 dubbelbyte-tecken.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Endast expanderad text och responsiva sökannonser; valfritt) En eller två URL-sökvägar som ska inkluderas efter bas-URL:en. De bör beskriva produkten eller tjänsten i annonsen mer ingående. Om du till exempel lägger till [!UICONTROL Display Path 1] av &quot;Shoes&quot; och [!UICONTROL Display Path 2] av &quot;Outdoor&quot; i bas-URL:en www.example.com, är URL:en www.example.com/Shoes/Outdoor. Den maximala längden (efter att alla dynamiska parametrar har ersatts) för varje fält är 15 eller 7 dubbelbyte-tecken.

För responsiva sökannonser infogar du en annonsanpassare med följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, till exempel `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Endast befintliga [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] standardtextannonser, skrivskyddade) Den URL som visas i en annons.

[!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] har ersatt skapande och redigering av standardtextannonser.

**[!UICONTROL Base URL]:** (Endast konton med mål-URL:er) Den sida som användarna ska tas till. Den kan innehålla omdirigerings- och spårningskod från tredje part. Om du använder tjänsten för spårning av Adobe Advertising-konvertering och kampanjinställningarna innehåller [!UICONTROL EF Redirect] och lägger till spårning på annonsnivå, lägger Search, Social och Commerce automatiskt till en egen omdirigerings- och spårningskod i annonsen.

Om du vill infoga ett kolumnnamn eller en modifieringsgrupp som en dynamisk parameter, klickar du i indatafältet och sedan på ett kolumnnamn i kolumnlistan eller ett [modifierarnamn](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) i listan [!UICONTROL Modifiers] .

**[!UICONTROL Final URL]:** (Konton med slutliga/avancerade URL:er) Den URL till landningssidan som användarna tas till när de klickar på annonsen. Den måste innehålla samma domän som visnings-URL:en, och alla parametrar i den slutliga URL:en måste matcha parametrarna i landningssidans URL efter annonsklicket. Den kan innehålla omdirigeringar inom landningssidans domän eller underdomän, men inga omdirigeringar utanför landningssidans domän.

Om du använder en [!DNL Google Merchant]-centerfeed och inkluderar det här värdet i kolumnen [!UICONTROL Link] infogar du den kolumnen i det här fältet.

>[!NOTE]
>
>* Om du genererar spårnings-URL:er när du bokför data som sprids via mallen läggs spårningsparametrar till i det här värdet baserat på kontospårningsinställningarna.
>* ([!DNL Google Ads] konton) Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

**[!UICONTROL Tracking Template]:** (Konton med slutliga/avancerade URL:er; valfritt) Spårningsmallen, som anger alla icke-landningsdomäner, omdirigerar och spårar parametrar och bäddar in den slutliga URL:en i en parameter. Spårningsmallen på den mest detaljerade nivån (med nyckelordet som det mest granulerade) åsidosätter värden på alla andra nivåer.

För spårning av konvertering av Adobe Advertising, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], läggs kod för omdirigering och spårning automatiskt till när du sparar posten.

Ange ett värde för omdirigeringar och spårning från tredje part. Ange landningssidans URL:

* För Yahoo! Japanska annonskonton använder parametern {lpurl}.

* Tillgängliga parametrar för Microsoft Advertising- och Google Ads-konton finns i [[!DNL Microsoft Advertising] dokumentationen](https://help.ads.microsoft.com/#apex/3/en/56799) eller i&quot;Endast spårningsmallen&quot; i avsnittet&quot;Tillgängliga [!DNL ValueTrack]-parametrar&quot; i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/6305348).

**\[Alternativa annonseringsfält nedanför de ursprungliga annonseringsfälten\]:** (Valfritt) En alternativ uppsättning annonskopior för en annons, som kan användas om någon av raderna i den ursprungliga annonskopian överskrider den högsta tillåtna längden när alla dynamiska parametrar fylls i med data under spridningen.

>[!NOTE]
>
>* Om alternativet [!UICONTROL Prefill] är markerat är de alternativa fälten förifyllda med originalfälten och du kan redigera dem efter behov.
>* Endast de reklamkopieringsfält som överskrider maxlängden ersätts med det alternativa värdet. Om t.ex. bara en originalrubrik eller -titel är för lång, används den alternativa rubriken eller titeln och de ursprungliga beskrivningarna för den genererade annonsvarianten. Se därför till att den alternativa annonskopian passar när den kombineras med den ursprungliga annonskopian.
>* Om den ursprungliga annonskopian uppfyller sökmotorns krav på längd, ignoreras den alternativa annonskopian.

**\[Component\] [!UICONTROL Ad Label Classifications] > \[Label Classification and Value\]:** (Valfritt) Värden för upp till fem befintliga etikettklassificeringar som ska tilldelas annonsvariationerna som skapas eller redigeras med mallen. För varje kampanjkomponent som du vill tilldela etikettklassificeringar till:

1. Klicka i kryssrutan.

1. Konfigurera etikettklassificeringsvärden för annonsvariantmallen:

   * För varje etikettklassificering och värde som ska tilldelas komponenten gör du följande:

      1. Klicka på **[!UICONTROL Add Label Classification]**.

      1. Välj den befintliga etikettklassificeringen och välj sedan ett befintligt värde eller ange ett nytt värde.

         Värdet får innehålla högst 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

         Om du vill infoga ett kolumnnamn som en dynamisk parameter för ett etikettklassificeringsvärde klickar du i indatafältet (det andra fältet) och sedan på ett kolumnnamn i kolumnlistan.

         Du kan bara inkludera ett värde per klassificering och kampanjkomponent. En kampanj kan till exempel ha Color=Red men inte Color=Red och Color=Blue.

         * Om du vill ändra ett befintligt etikettklassificeringsvärde markerar eller anger du ett nytt värde.

         * Om du vill ta bort ett befintligt etikettklassificeringsvärde klickar du på **[!UICONTROL X]** bredvid värdet.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Om automatisering av annonshantering med lagerflöden](../inventory-feeds-about.md)
>* [Hantera modifierare](../modifiers-manage.md)
>* [Hantera lagerdataflödesfiler](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Sprid feed-data via mallar](../feed-data-propagate.md)
>* [Bokför kampanjdata från lagerfeeds till annonsnätverk](../propagated-data-post.md)
