---
title: "[!DNL Microsoft Advertising] annonsgruppsinställningar"
description: Referera inställningarna för [!DNL Microsoft Advertising] annonsgrupper.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] och gruppinställningar

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ett annonsgruppsnamn som är unikt i kampanjen. Maximala längden är 128 tecken.

**[!UICONTROL Status]:** Annonsgruppens visningsstatus: *Aktiv* eller *Pausad*. Standardinställningen för nya annonsgrupper är *Aktiv*.

**[!UICONTROL Ad Language]:** Målspråket för annonser.<!-- Which campaign types? Not there for audience image-based ad groups. -->

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** Placera annonser inom annonsgruppen hur och var:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (standard): Om du vill lägga bud på annonser i söknätverket.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Att lägga bud på annonser på syndikerade partnerwebbplatser.

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

För [!DNL Microsoft Advertising] annonser i målgruppsnätverket optimeras inte budmodifierare för platsmål i standardportföljer med &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Målgrupper och grupper; (valfritt) Specifika genrer som ska inkluderas eller exkluderas som mål: *[!UICONTROL Male]*, *[!UICONTROL Female]* och *[!UICONTROL Unknown]*. Som standard anges alla gendrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje könsrelaterat mål.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Age]:** (Målgrupper och grupper; (valfritt) Specifika åldersgrupper som ska inkluderas eller exkluderas som mål: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* och *[!UICONTROL Unknown]*. Som standard anges alla åldrar som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje målålder.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Industry]:** (Målgrupper och grupper; (valfritt) Specifika branscher att inkludera eller exkludera som mål. Som standard är alla branscher målinriktade. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje bransch som de riktar sig till.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

**[!UICONTROL Job Function Targets]:** (Målgrupper och grupper; (valfritt) Specifika jobbfunktioner som ska inkluderas eller exkluderas som mål. Som standard anges alla jobbfunktioner som mål. Undantag åsidosätter alltid inkluderingar.

* Om du vill ange alla värden som mål ska du inte markera några värden.

* Om du vill ta med ett värde klickar du en gång på cirkeln så att en blå bock (![Inkludera](/help/search-social-commerce/assets/include.png "Inkludera")) visas. Du kan också öka eller minska anbuden med en angiven procentandel för varje jobbfunktion som du har som mål.

* Om du vill exkludera ett värde klickar du två gånger på cirkeln så att en röd bock (![Exkludera](/help/search-social-commerce/assets/exclude.png "Exkludera")) visas.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Endast kampanjer i displayen/det egna nätverket). (valfritt) Webbplatser i visningsnätverket där du inte vill att dina annonser ska visas. Ange en giltig URL, till exempel www.example.com. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader.

Mer information om tillgänglighet finns i Microsoft Advertising-hjälpen för &quot;[Förhindra att annonser visas på specifika webbplatser](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Hantera annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

