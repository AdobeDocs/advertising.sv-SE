---
title: "[!DNL Microsoft® Ads] webb- och mallinställningar för lagerflöden"
description: Referera inställningarna för [!DNL Microsoft® Ads] shoppingannonsmallar för lagerflöden.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft® Ads] inställningar för butiks- och mallinställningar för lagerflöden

Använd mallar för shoppingannonser för att konfigurera shoppingannonser.

>[!NOTE]
>
>* Följande tecken är reserverade för att ange kolumnnamn och modifieringsnamn i mallen och är därför inte tillåtna som text i alla attributfält:  `[ ] < > `


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

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Valfritt för mallar för klientflödesfiler) Spårningsmallen på kampanjnivå, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Det här värdet åsidosätter inställningen på kontonivå, men spårningsmallar på mer detaljnivå (med nyckelordet längst granulat) åsidosätter det här värdet.

* För konverteringsspårning för annonsering i Adobe, som används när kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]&quot; och &quot;[!UICONTROL Auto Upload],&quot; gör något av följande&quot;:

   * (Rekommenderas) Använd [spåra mallformat för Microsoft®-shoppingkampanjer](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Om hela kontot är avsett för shoppingannonser kan du i stället definiera en spårningsmall på kontonivån.

   * Om du i stället tar med ett värde för varje produkt i feeden med hjälp av[!DNL bingads_redirect]&quot; (med [korrekt format](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)) och sedan ange parametern `{lpurl}`. Du kan lägga till omdirigeringar och spårning från tredje part i `{lpurl}` parameter.

* Ange ett värde för omdirigeringar och spårning från tredje part.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** Kund-ID för det handlarkonto vars produkter används för kampanjen.

**[!UICONTROL Sales Country]:** Det land där kampanjens produkter säljs. Eftersom produkter är kopplade till målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

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

**[!UICONTROL Campaign Priority]:** Prioriteten som kampanjen används med när flera kampanjer annonserar samma produkt: *[!UICONTROL Low]* (standard för nya kampanjer), *[!UICONTROL Medium]*, eller *[!UICONTROL High]*. När samma produkt ingår i mer än en kampanj använder annonsnätverket först kampanjprioriteten för att avgöra vilken kampanj (och tillhörande bud) som är berättigad för annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Valfritt) En spårningsmall på annonsgruppsnivå, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en parameter. Det här värdet åsidosätter inställningarna på konto- och kampanjnivå, men spårningsmallar på mer detaljerad nivå åsidosätter det här värdet.

För konverteringsspårning för annonsering i Adobe behöver du inte ange något värde. Kampanjnivån räcker.

Ange ett värde för omdirigeringar och spårning från tredje part.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Standardproduktgruppen, inklusive alla, &quot;[!UICONTROL All products].&quot; Du kan inte ta bort den här överordnade produktgruppen, men den tas automatiskt bort när alla lägre nivåer saknas i feeden.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Enheter utan underordnade produktgrupper, valfritt) Spårningsmallen för produktgruppen, som anger alla omdirigeringar och spårningsparametrar utanför landningsdomänen och bäddar in den slutliga URL:en i en [!DNL ValueTrack] parameter. Den här mallen åsidosätter mallar på högre nivåer.

För konverteringsspårning för annonsering i Adobe behöver du inte ange något värde. Kampanjnivån räcker.

Ange ett värde för omdirigeringar och spårning från tredje part.

**[!UICONTROL Initial Bid]:** Det inledande anbudet för varje annons.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Automatisera och hantera lagerflöden](../inventory-feeds-about.md)
>* [Hantera modifierare](../modifiers-manage.md)
>* [Hantera lagerdataflödesfiler](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Sprida feed-data via mallar](../feed-data-propagate.md)
>* [Posta kampanjdata från lagerfeeds till annonsnätverk](../propagated-data-post.md)
