---
title: Spårningsparametern för AMO-ID (s_kwcid)
description: Läs mer om spårningsparametern som används för att dela data från Adobe Advertising med Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 47cb00bc456601ef943c37de14a2047220f756f1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Spårningsparametern för AMO-ID (s_kwcid)

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising delar data om era kampanjer med Adobe Analytics med hjälp av tilläggsparametern AMO ID, som också kallas `s_kwcid` -parameter, som består av annonskanaler och annonsspecifika element.

<!-- add everything below to IDs page -->

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) Funktionen för infogning på serversidan implementeras.

  För [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] inställning aktiverad för kontot eller kampanjen lägger pixelservern automatiskt till AMO ID-parametern i landningssidans suffix när en slutanvändare klickar på en annons <!-- click a search ad or views a display ad --> med Adobe Advertising-pixeln.

  för andra annonsnätverk, eller [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] om inställningen är inaktiverad lägger du manuellt till parametern AMO ID i dina tilläggsparametrar på kontonivå, som lägger till den i dina bas-URL:er.

* <!-- (Search, Social, & Commerce only) -->Serversidesinfogningsfunktionen är inte implementerad och du måste lägga till AMO ID-parametern manuellt i ([!DNL Google Ads] och [!DNL Microsoft Advertising]) landningssidessuffix eller (andra annonsnätverk) tilläggsparametrar på kontonivå.

Om du vill implementera infogningsfunktionen på serversidan eller fastställa det bästa alternativet för din verksamhet kan du tala med ditt Adobe-kontoteam.

## AMO ID-format för annonser DSP annonser

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

där:

* `AC` anger visningskanalen.

* `{TM_AD_ID}` är den alfanumeriska annonstangenten.

* `{TM_PLACEMENT_ID}` är den alfanumeriska placeringsnyckeln.

## AMO ID-format för sök-, sociala och kommersiella annonser

Parametrarna varierar beroende på annonsnätverk, men följande parametrar är gemensamma för alla:

* `AL` anger sökkanalen. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` är ett unikt användar-ID som tilldelats annonsören.

* `{sid}` ersätts med det numeriska ID:t för annonsören och annonsnätverkskontot: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (borttagen), eller *106* for [!DNL Pinterest] (föråldrat).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Detta inkluderar shoppingkampanjer som använder [!DNL Google Merchant Center].

* Konton som använder det senaste AMO ID-formatet, som har stöd för kampanjrapportering och rapportering på annonsnivå för maximala prestandakampanjer samt utkast och experimentkampanjer:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alla andra konton:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* För dynamiska sökannonser {keyword} fylls i med det automatiska målet.
>* När du genererar spårning för [!DNL Google] shoppingannonser, en produkt-ID-parameter, `{adwords_producttargetid}`infogas före nyckelordsparametern. Produkt-ID-parametern visas inte i [!DNL Google Ads] spårningsparametrar på kontonivå och kampanjnivå.
>* Information om hur du använder den senaste spårningskoden för AMO-ID finns i &quot;[Uppdatera spårningskoden för AMO ID för en [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Sökkampanjer:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Shoppingkampanjer (med [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Målgruppskampanjer:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Hantera och nätverkskonton](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Inställningar för Baidu-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampanjinställningar för Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Inställningar för Microsoft Advertising-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Inställningar för japanska annonskampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Inställningar för Yandex-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
