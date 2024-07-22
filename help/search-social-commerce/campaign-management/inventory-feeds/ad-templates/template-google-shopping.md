---
title: '[!DNL Google Ads] inställningar för butiks- och mallinställningar för lagerfeeds'
description: Referera inställningarna för  [!DNL Google Ads] butiks- och annonsmallar för lagerflöden.
exl-id: 36cbe719-f984-4456-8575-94b9d3e6094e
feature: Search Inventory Feeds
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# [!DNL Google Ads] inställningar för butiks- och mallinställningar för lagerflöden

Använd mallar för shoppingannonser för att konfigurera shoppingannonser.

>[!NOTE]
>
>* Följande tecken är reserverade för att ange kolumnnamn och modifieringsnamn i mallen och är därför inte tillåtna som text i alla attributfält: `[ ] < > `

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

För spårning av Adobe Advertising-konvertering, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], använder du mallformatet [spårning för Google Ads-shoppingkampanjer](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Om hela kontot är avsett för shoppingannonser kan du i stället definiera en spårningsmall på kontonivån.

Ange ett värde för omdirigeringar och spårning från tredje part.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** Kund-ID för det handlarkonto vars produkter används för kampanjen.

**[!UICONTROL Sales Country]:** Det land där kampanjens produkter säljs. Eftersom produkter är associerade
med målländer avgör den här inställningen vilka produkter som annonseras i kampanjen.

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

**[!UICONTROL Networks]:** De nätverk där annonser ska placeras. *[!UICONTROL Search]* har redan valts. Om du vill inkludera bud på listor för [!DNL Google Ads] sökpartner markerar du kryssrutan bredvid **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** Prioriteten som kampanjen används med när flera kampanjer annonserar
samma produkt: *[!UICONTROL Low]* (standard för nya kampanjer), *[!UICONTROL Medium]* eller *[!UICONTROL High]* . När samma produkt ingår i mer än en kampanj använder annonsnätverket
kampanjprioriteten först för att avgöra vilken kampanj (och tillhörande bud) som är berättigad till annonsauktionen. När alla kampanjer har samma prioritet är kampanjen med det högsta anbudet berättigad.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Valfritt) En spårningsmall på annonsgruppsnivå, som anger alla icke-landningsdomäner omdirigerar och spårar parametrar och bäddar in den slutliga URL:en i en parameter. Det här värdet åsidosätter inställningarna på konto- och kampanjnivå, men spårningsmallar på mer detaljerad nivå åsidosätter det här värdet.

Du behöver inte ange något värde för spårning av konvertering för Adobe Advertising. Kampanjnivån räcker.

Ange ett värde för omdirigeringar och spårning från tredje part.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Standardproduktgruppen, [!UICONTROL All products], som innehåller alla komponenter. Du kan inte ta bort den här överordnade produktgruppen, men den tas automatiskt bort när alla lägre nivåer saknas i feeden.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Enheter utan underordnade produktgrupper; valfritt) Spårningsmallen för produkten
grupp, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar in den slutliga URL:en i en [!DNL ValueTrack] -parameter. Den här mallen åsidosätter mallar på högre nivåer.

Du behöver inte ange något värde för spårning av konvertering för Adobe Advertising. Kampanjnivån räcker.

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
>* [Om automatisering av annonshantering med lagerflöden](../inventory-feeds-about.md)
>* [Hantera modifierare](../modifiers-manage.md)
>* [Hantera lagerdataflödesfiler](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Sprid feed-data via mallar](../feed-data-propagate.md)
>* [Bokför kampanjdata från lagerfeeds till annonsnätverk](../propagated-data-post.md)
