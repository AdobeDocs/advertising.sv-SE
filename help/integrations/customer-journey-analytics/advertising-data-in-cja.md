---
title: Adobe Advertising-statistik och -dimensioner i Customer Journey Analytics
description: Referera till de Adobe Advertising-mått och -mått som finns i Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: eddd9c997ada380d5624703b82bca189be90b893
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Adobe Advertising-statistik och -dimensioner i Customer Journey Analytics

*Annonsörer med endast Adobe Advertising-Customer Journey Analytics-integrering*

>[!NOTE]
>
>* Adobe Advertising skickar trafikstatistik och dimensioner till [!DNL Customer Journey Analytics] dagligen.
>* [!DNL Web SDK] fångar Adobe Advertising klickningar och genomgångar i realtid och skickar dem till Customer Journey Analytics.

## Adobe Advertising trafikstatistik

<!-- Verify column names -->

>[!NOTE]
>
>* 
>* &quot;XDM-fältnamn&quot; är fältnamnet i Adobe Experience Platform.
>* &quot;Visningsnamn för XDM-fält&quot; anger visningsnamnet i Customer Journey Analytics.

| Adobe Advertising fältnamn | XDM-fältnamn | Visningsnamn för XDM-fält | Source |
|------------------------------|----------------|------------------------|--------|
| Datum | Datum | Alla | |
| AMO-ID | skwcid | ADOBE ADVERTISING ID | Alla |
| AMO Impressions | adobe_advertising_imponsions | Adobe Advertising Impressions | Alla |
| AMO Clicks | adobe_advertising_clicks | Adobe Advertising Clicks | Alla |
| AMO-kostnad | adobe_advertising_cost | Adobe Advertising Cost | Alla |
| Valutakod | valuta | Valuta | Alla |
| AMO-vyer | adobe_advertising_views | Adobe Advertising-vyer | Ad Cloud DSP |
| AMO-vyer som är 25 % fullständiga | adobe_advertising_views_25_pct | Adobe Advertising Views 25 % Complete | Ad Cloud DSP |
| AMO-vyer 50 % klart | adobe_advertising_views_50_pct | Adobe Advertising Views 50 % Complete | Ad Cloud DSP |
| AMO-vyer som är 75 % fullständiga | adobe_advertising_views_75_pct | Adobe Advertising Views är 75 % färdigt | Ad Cloud DSP |
| AMO-vyer 100 % klart | adobe_advertising_views_100_pct | Adobe Advertising Views 100 % Complete | Ad Cloud DSP |
| Visade AMO-minuter | adobe_advertising_minutes_displayed | Adobe Advertising Minutes Viewed | Ad Cloud DSP |
| AMO Viewable Impressions | adobe_advertising_viewable_impressions | Adobe Advertising Viewable Impressions | Ad Cloud DSP |
| AMO-bilder som inte kan visas | adobe_advertising_not_viewable_impressions | Impressions som inte kan visas i Adobe Advertising | Ad Cloud DSP |
| AMO-mätbara exponeringar | adobe_advertising_measurable_impressions | Adobe Advertising Measurable Impressions | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising dimensioner

>[!NOTE]
>
>* &quot;XDM Field&quot; är fältnamnet i Adobe Experience Platform.
>* &quot;Visningsnamn för XDM-fält&quot; anger visningsnamnet i Customer Journey Analytics.

| Adobe Advertising fältnamn | XDM-fältnamn | Visningsnamn för XDM-fält | Source |
|------------------------------|----------------|------------------------|--------|
| Nyckel | skwcid | ADOBE ADVERTISING ID |
| Annonsplattform | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Konto | adobe_advertising_account | Adobe Advertising-konto |
| Campaign | adobe_advertising_campaign | Adobe Advertising Campaign |
| Annonsgrupp | adobe_advertising_ad_group | Adobe Advertising Ad Group |
| Nyckelord | adobe_advertising_keyword | Adobe Advertising-nyckelord |
| Annons | adobe_advertising_ad | Adobe Advertising Ad |
| Placement | adobe_advertising_placement | Adobe Advertising Placement |
| Matcha typ | adobe_advertising_match_type | Adobe Advertising Matchningstyp |
| Annonsrubrik | adobe_advertising_ad_title | Adobe Advertising Ad Title |
| Annonsbeskrivning | adobe_advertising_ad_description | Adobe Advertising Ad Description |
| Måladress för annons | adobe_advertising_ad_destination_url | Adobe Advertising Ad Destination URL |
| Webbadress för annonsvisning | adobe_advertising_ad_display_url | Adobe Advertising Ad Display URL |
| Enhet | adobe_advertising_device | Adobe Advertising Device |
| Matchningstyp för nyckelord | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |
| Nätverk | adobe_advertising_network | Adobe Advertising Network |
| Annonstyp | adobe_advertising_ad_type | Adobe Advertising Ad Type |
| Produktmål | adobe_advertising_product_target | Adobe Advertising Product Target |
| Landningstyp | adobe_advertising_landing_type | Adobe Advertising landningstyp |
| Optimering | adobe_advertising_optimization | Adobe Advertising Optimization |

>[!MORELIKETHIS]
>
>* [Översikt](overview.md)
>* [Förutsättningar](prerequisites.md)
>* [Adobe Advertising ID:n som används av [!DNL Customer Journey Analytics]](ids.md)
