---
title: '[!DNL Microsoft Advertising] och gruppinställningar'
description: Referera inställningarna för  [!DNL Microsoft Advertising] annonsgrupper.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] och gruppinställningar

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ett annonsgruppsnamn som är unikt i kampanjen. Maximala längden är 128 tecken.

**[!UICONTROL Status]:** Annonsgruppens visningsstatus: *Aktiv* eller *Pausad*. Standardvärdet för nya annonsgrupper är *Aktiv*.

**[!UICONTROL Ad Language]:** (sökkampanjer) Målspråket för annonser.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (sökannonser) Placera annonser i annonsgruppen och var:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (standard): Om du vill lägga bud på annonser i söknätverket.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Att lägga bud på annonser på syndikerade partnerwebbplatser.

* *[!UICONTROL Content network]:* har tagits bort

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** har tagits bort

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (målgrupp och grupper) Om:

* *[!UICONTROL Target and Bid]:* Om du bara vill visa annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:* Så här visar du annonser även för personer som inte är associerade med målgrupper så länge de uppfyller andra annonsgruppsmål. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

För [!DNL Microsoft Advertising] annonsgrupper i målgruppsnätverket är budmodifierare för platsmål inte optimerade i standardportföljer med inställningen [!UICONTROL Auto-optimize Bid Adjustment Values].

**[!UICONTROL Genre]:** (Annonsgrupper i [!UICONTROL Audience CTV Video] kampanjer, tillgängliga i USA, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY och TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Målgenren, som avgör vilka program och kanaler annonserna visas på:

* *[!UICONTROL All genres]:* (Standard) Alla genrer anges som mål.

* *[!UICONTROL Select From Below List]:* Målar valda genrer. Välj i listan över alla tillgängliga genrer.

Annonsplacering via uppkopplad TV (CTV) beror på videons kvalitet och anbudsbelopp. Se de [tekniska kraven för CTV-reklam](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Audience ad groups; optional) Specific genders to include or exclude as target: *[!UICONTROL Male]*, *[!UICONTROL Female]*, and *[!UICONTROL Unknown]*. Som standard anges alla gendrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på den intilliggande cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje könsrelaterat mål.

* Om du vill utesluta ett värde klickar du två gånger på den intilliggande cirkeln så att en röd bock (![Uteslut](/help/search-social-commerce/assets/exclude.png "Uteslut")) visas.

**[!UICONTROL Age]:** (Audience ad groups; optional) Specific age categories to include or exclude as target: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, and *[!UICONTROL Unknown]*. Som standard anges alla åldrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på den intilliggande cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje målålder.

* Om du vill utesluta ett värde klickar du två gånger på den intilliggande cirkeln så att en röd bock (![Uteslut](/help/search-social-commerce/assets/exclude.png "Uteslut")) visas.

**[!UICONTROL Industry]:** (Audience ad groups; optional) Specifika branscher att inkludera eller exkludera som mål. Som standard är alla branscher målinriktade. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på den intilliggande cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje bransch som de riktar sig till.

* Om du vill utesluta ett värde klickar du två gånger på den intilliggande cirkeln så att en röd bock (![Uteslut](/help/search-social-commerce/assets/exclude.png "Uteslut")) visas.

**[!UICONTROL Job Function Targets]:** (Audience ad groups; optional) Specifika jobbfunktioner som ska inkluderas eller exkluderas som mål. Som standard anges alla jobbfunktioner som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på den intilliggande cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje jobbfunktion som du har som mål.

* Om du vill utesluta ett värde klickar du två gånger på den intilliggande cirkeln så att en röd bock (![Uteslut](/help/search-social-commerce/assets/exclude.png "Uteslut")) visas.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Valfritt) Antalet gånger som en kund kan få annonser från annonsgruppen. Ange ett värde och välj tidsenhet (*[!UICONTROL Hour]*, *[!UICONTROL Day]* eller *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Endast kampanjer på skärmen/i det ursprungliga nätverket; valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i [!DNL Microsoft Advertising]-hjälpen till [Förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Hantera annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
