---
source-git-commit: 2b719e00418010b1f8e21b8956ad55b2ffc7dee1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO-ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för dataklassificering av [!DNL Analytics] och Customer Journey Analytics samt för inmatning av reklamstatistik (som visningar, klick och kostnader) från Adobe Advertising.

För [!DNL Analytics] lagras AMO-ID:t i en [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) - eller rVar-dimension (AMO-ID).

För Customer Journey Analytics lagras AMO-ID:t i egenskapen `trackingCode` för objektet `conversionDetails`, som är en del av [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

AMO-ID:t kallas även `s_kwcid`, som ibland uttalas som [!DNL squid].

### AMO ID-format {#amo-id-formats}

#### AMO ID-format för [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

där:

* `AC` anger visningskanalen.

* `{TM_AD_ID}` är den Adobe Advertising-genererade alfanumeriska annonstangenten. Den används som en unik identifierare för en annons och fungerar som en nyckel för översättning av Adobe Advertising entitetsmetadata till läsbara [!DNL Analytics]- och Customer Journey Analytics-dimensioner.

* `{TM_PLACEMENT_ID}` är den Adobe Advertising-genererade alfanumeriska placeringsnyckeln. Den används som en unik identifierare för en placering och fungerar som en nyckel för översättning av Adobe Advertising-entitetsmetadata till läsbara [!DNL Analytics]- och Customer Journey Analytics-dimensioner.

Exempel på AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID-format för sök-, sociala och Commerce-annonser {#amo-id-format-search}

Parametrarna varierar beroende på annonsnätverk, men följande parametrar är gemensamma för alla:

* `AL` anger sökkanalen. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` är ett unikt användar-ID som tilldelats annonsören.

* `{sid}` ersätts med det numeriska ID:t för annonserarens annonsnätverkskonto: **&#x200B; för [!DNL Google Ads], &#x200B;** [!DNL Microsoft Advertising] för *,* 45[!DNL Meta] för *, 86* för [!DNL Yahoo! Display Network], *87* för [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (utgått) eller *106*  för [!DNL Pinterest] (borttagen).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{placement}` är den webbplats där annonsen klickades.
* `{keywordid}` är annonsnätverkets unika numeriska ID för nyckelordet som utlöste annonsen.

##### [!DNL Google Ads]

Detta inkluderar shoppingkampanjer som använder [!DNL Google Merchant Center].

* Konton som använder det senaste AMO ID-formatet, som har stöd för kampanjrapportering och rapportering på annonsnivå för maximala prestandakampanjer samt utkast och experimentkampanjer:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alla andra konton:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

där:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` är det [!DNL Google Ads] unika numeriska ID:t för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `e` för exakt, `p` för fras eller `b` för bred.
* `{placement}` är domännamnet för den webbplats där annonsen klickades. Det finns ett värde för annonser i riktade kampanjer och för annonser i kampanjer riktade mot nyckelord som visas på innehållswebbplatser.
* `{network}` anger nätverket som klickningen inträffade från: `g` för [!DNL Google]-sökning (endast för nyckelordsriktade annonser), `s` för en sökpartner (endast för nyckelordsriktade annonser) eller `d` för visningsnätverket (antingen för nyckelordsriktade eller placeringsriktade annonser).
* `{product_partition_id}` är annonsnätverkets unika numeriska ID för produktgruppen som används med produktannonser.
* `{keyword}` är antingen det specifika nyckelord som utlöste din annons (på sökwebbplatser) eller det bästa matchande nyckelordet (på innehållswebbplatser).
* `{campaignid}` är annonsnätverkets unika numeriska ID för kampanjen.
* `{adgroupid}` är annonsnätverkets unika numeriska ID för annonsgruppen.

>[!NOTE]
>
>* För dynamiska sökannonser har {keyword} fyllts i med det automatiska målet.
>* När du genererar spårning för [!DNL Google] shoppingannonser infogas en produkt-ID-parameter, `{adwords_producttargetid}`, före nyckelordsparametern. Produkt-ID-parametern visas inte i parametrarna [!DNL Google Ads] på kontonivå och kampanjnivå.
>* Information om hur du använder den senaste spårningskoden för AMO-ID finns i [Uppdatera spårningskoden för AMO-ID för ett [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md). <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Alla kampanjtyper:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

där:

* `{AdId}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{OrderItemId}` är annonsnätverkets numeriska ID för nyckelordet.
* `{CampaignId}` är annonsnätverkets unika numeriska ID för kampanjen.
* `{AdGroupId}` är annonsnätverkets unika numeriska ID för annonsgruppen.

>[!NOTE]
>
> För konton med kampanjer utan alternativet [!UICONTROL Auto Upload] för spårning som inte redan har migrerats till det nya formatet måste du manuellt uppdatera varje landningssidesuffix så att det innehåller ovanstående format.
> &#x200B;>Under tiden fungerar de äldre formaten enligt följande:
>* Sökkampanjer:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shoppingkampanjer (med [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Målgruppskampanjer:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

där:

* `{creative}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen: `be` för exakt, `bp` för fras eller `bb` för bred.
* `{network}` anger nätverket som klickningen inträffade från: `n` för internt eller `s` för sökning.
* `{keyword}` är nyckelordet som utlöste din annons.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

där:

* `{ad_id}` är annonsnätverkets unika numeriska ID för den kreativa.
* `{source_type}` är den typ av webbplats där annonsen har visats: *b* för sökning, *c* för kontext (innehåll) eller *ct* för kategori.
* `{phrase_id}` är annonsnätverkets numeriska ID för nyckelordet.
