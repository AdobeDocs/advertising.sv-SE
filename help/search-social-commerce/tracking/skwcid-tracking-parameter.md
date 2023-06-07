---
title: s_kwcid tracking-parametern
description: Lär dig mer om spårningsparametern som används för att dela Adobe-annonsdata med Adobe Analytics.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# s_kwcid tracking-parametern

*Annonsörer med enbart integrering mellan Adobe Advertising och Adobe Analytics*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertising delar data om era kampanjer med Adobe Analytics via `s_kwcid` append-parameter, som består av annonskanaler och annonser för nätverksspecifika element. Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas<!--; the only option for Advertising DSP-->) Funktionen s_kwcid på serversidan är implementerad.

   För [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] inställning aktiverad för kontot eller kampanjen lägger pixelservern automatiskt till parametern s_kwcid i landningssidans suffix när en slutanvändare klickar på en annons <!-- click a search ad or views a display ad --> med Adobe Advertising pixel.

   för andra annonsnätverk, eller [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] om inställningen är inaktiverad lägger du till parametern manuellt i tilläggsparametrarna på kontonivån, som läggs till i bas-URL:erna.

* <!-- (Search, Social, & Commerce only) -->Funktionen s_kwcid på serversidan är inte implementerad och du måste lägga till parametern s_kwcid manuellt i ([!DNL Google Ads] och [!DNL Microsoft Advertising]) landningssidessuffix eller (andra annonsnätverk) tilläggsparametrar på kontonivå.

Om du vill implementera funktionen s_kwcid på serversidan, eller fastställa det bästa alternativet för ditt företag, pratar du med ditt Adobe-kontoteam.

## `s_kwcid` format för annonser DSP annonser

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

där:

* `AC` anger visningskanalen.

* `{TM_AD_ID}` är den alfanumeriska annonstangenten.

* `{TM_PLACEMENT_ID}` är den alfanumeriska placeringsnyckeln.

## `s_kwcid` format för sök-, sociala och kommersiella annonser

Parametrarna varierar beroende på annonsnätverk, men följande parametrar är gemensamma för alla:

* `AL` anger sökkanalen. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` är ett unikt användar-ID som tilldelats annonsören.

* `{sid}` ersätts med det numeriska ID:t för annonsören och annonsnätverkskontot: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (borttagen), eller *106* for [!DNL Pinterest] (föråldrat).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Detta inkluderar shoppingkampanjer som använder [!DNL Google Merchant Center].

* Konton som använder det senaste s_kwcid-formatet, som har stöd för kampanj- och annonsgruppsrapportering för maximala resultatkampanjer samt utkast och experimentkampanjer:

   `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alla andra konton:

   `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* För dynamiska sökannonser fylls {keyword} i med det automatiska målet.
>* När du genererar spårning för [!DNL Google] shoppingannonser, en produkt-ID-parameter, `{adwords_producttargetid}`infogas före nyckelordsparametern. Produkt-ID-parametern visas inte i [!DNL Google Ads] spårningsparametrar på kontonivå och kampanjnivå.
>* Mer information om hur du använder den senaste s_kwcid-spårningskoden finns i &quot;[Uppdatera s_kwcid-spårningskoden för en [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;


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

* Målgruppsnätverkskampanjer:

   `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
>* [Hantera och nätverkskonton](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Inställningar för Baidu-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampanjinställningar för Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Inställningar för Microsoft Advertising-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Inställningar för japanska annonskampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Inställningar för Yandex-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
