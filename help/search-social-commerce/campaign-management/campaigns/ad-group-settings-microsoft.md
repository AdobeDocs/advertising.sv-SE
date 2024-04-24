---
title: '''[!DNL Microsoft® Advertising] och gruppinställningar'
description: Referera inställningarna för [!DNL Microsoft® Advertising] annonsgrupper.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 7339af39250f0328bc6e8d530a2d7f04286132e5
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] och gruppinställningar

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ett annonsgruppsnamn som är unikt i kampanjen. Maximala längden är 128 tecken.

**[!UICONTROL Status]:** Annonsgruppens visningsstatus: *Aktiv* eller *Pausad*. Standardinställningen för nya annonsgrupper är *Aktiv*.

**[!UICONTROL Ad Language]:** (Sökkampanjer) Målspråket för annonser.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Sök annonser) Placera annonser inom annonsgruppen och hur de ska placeras:

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* (standard): Om du vill lägga bud på annonser i söknätverket.

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* Att lägga bud på annonser på syndikerade partnerwebbplatser.

* *[!UICONTROL Content network]:* Föråldrat

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Föråldrat

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Målgrupper och grupper) Om:

* *[!UICONTROL Target and Bid]:* Visa endast annonser för användare som är kopplade till målgrupper som också uppfyller andra mål för annonsgruppen.

* *[!UICONTROL Bid Only]:* Visa annonser även för personer som inte är kopplade till målgrupper så länge de uppfyller andra mål på annonsgruppsnivå. Ni kan dock öka chanserna att annonser visas för specifika målgrupper genom att ange högre bud för dessa målgrupper.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

För [!DNL Microsoft® Advertising] annonser i målgruppsnätverket optimeras inte budmodifierare för platsmål i standardportföljer med &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Annonsgrupper i [!UICONTROL Audience CTV Video] -kampanjer, tillgängliga i USA, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY och TH<!-- should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Målgenren, som avgör vilka program och kanaler annonserna visas på:

* *[!UICONTROL All genres]:* (Standardvärdet) Målsätter alla genrer.

* *[!UICONTROL Select From Below List]:* Målar valda genrer. Välj i listan över alla tillgängliga genrer.

Annonsplacering via uppkopplad TV (CTV) beror på videons kvalitet och anbudsbelopp. Se [tekniska krav för CTV-reklam](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Målgrupper och grupper; valfritt) Specifika genrer som ska inkluderas eller exkluderas som mål: *[!UICONTROL Male]*, *[!UICONTROL Female]* och *[!UICONTROL Unknown]*. Som standard anges alla gendrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje könsrelaterat mål.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Age]:** (Målgrupper och grupper; valfritt) Specifika ålderskategorier som ska inkluderas eller exkluderas som mål: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* och *[!UICONTROL Unknown]*. Som standard anges alla åldrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje målålder.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Industry]:** (Målgrupper och grupper; valfritt) Specifika branscher att inkludera eller utesluta som mål. Som standard är alla branscher målinriktade. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje bransch som de riktar sig till.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Job Function Targets]:** (Målgrupper och grupper; valfritt) Specifika jobbfunktioner som ska inkluderas eller exkluderas som mål. Som standard anges alla jobbfunktioner som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje jobbfunktion som du har som mål.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Valfritt) Det antal gånger en kund får annonser från annonskoncern. Ange ett värde och välj tidsenhet (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, eller *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Kampanjer endast på displayen/det ursprungliga nätverket, valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i [!DNL Microsoft® Advertising] hjälp att[Förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Hantera annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
