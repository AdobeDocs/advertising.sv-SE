---
title: Klickspårningsformat för  [!DNL Google Ads]
description: Lär dig mer om knappspårningsformat för  [!DNL Google Ads] konton.
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Klickspårningsformat för [!DNL Google Ads]

Nedan följer basspårningsmallen och landningssidans suffix (det sista URL-suffixet) som krävs för Search, Social och Commerce för [!DNL Google Ads].

## Spåra mallformat

### Sök/visa nätverk, inklusive sitelinks

Följande format gäller för alla spårbara annonstyper i sök- och visningsnätverk samt för sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exempel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* Parametrarna [!DNL ValueTrack] för att ange slutliga URL:er i spårningsmallar måste vara antingen `{lpurl}` eller `!{unescapedurl}`.
>
>* (Textannonser) När du lägger ett bud med nyckelord har parametern `ev_pl` (för placeringar) inget värde. När du lägger ett bud har `ev_ln` (för nyckelord) inget värde. När du lägger ett bud per annonsgrupp eller någon annan dimension har både `ev_ln` och `ev_pl` inga värden.
>
>* (Annonser för dynamiska sökningar) `{keyword}` anger det dynamiska sökmåluttrycket, till exempel `_cat:[VALUE]` eller `_url:[VALUE]`.
>
>* (Annonser för dynamiska sökningar) [!DNL Google Ads] fastställer den slutliga URL:en dynamiskt, så du behöver inte ange en.
>
>* (Sitelinks) Du kan se vilka konverteringar som har gjorts genom att klicka på en sitellänk genom att generera en [!UICONTROL Transaction Report]. Kolumnvärdet [!UICONTROL Link Type] för en sitelink är `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.

### Shoppingnätverk

Följande format gäller för shoppingannonser och produktgrupper i shoppingnätverk. Du kan ange en spårningsmall på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exempel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* Parametrarna [!DNL ValueTrack] för att ange slutliga URL:er i spårningsmallar måste vara antingen `{lpurl}` eller `!{unescapedurl}`.
>
>* [!DNL Google Ads] använder produkt-URL:er i Google Merchant Center-flödet som de slutliga URL:erna, så du behöver inte ange slutliga URL:er för dina produktdata eller produktgrupper.
>
>* Du kan se vilka konverteringar som har gjorts genom att klicka på en shoppingannons genom att generera en [!UICONTROL Transaction Report]. Kolumnvärdet [!UICONTROL Link Type] för en produktannons är pla:`<product ID>`, till exempel `pla:8525822`.

## Format för landningssidans suffix (sista URL-suffix)

Konton som använder Adobe Advertising-konverteringsspårning måste inkludera annonsnätverkets klickidentifierare (`gclid` för [!DNL Google Ads]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla något av följande:

   * [!DNL Google Ads]-konton som använder det senaste [AMO ID-formatet](/help/integrations/analytics/ids.md#amo-id-formats) (som börjar med `s_kwcid`), som stöder kampanjrapportering och rapportering på annonsnivå för maximala prestandakampanjer samt utkast och experimentkampanjer:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Om kontot har en AMO ID-implementering på serversidan och konto- eller kampanjinställningen [!UICONTROL Auto Upload] är aktiverad, läggs parametern till automatiskt. I annat fall måste du lägga till det manuellt. Se [Adobe Advertising ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement).

   * Alla andra [!DNL Google Ads]-konton:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.
>
>* (Dynamiska sökannonser, annonsörer med Adobe Analytics och utan spårning på serversidan) När du vill inkludera spårning för omvänd feed från Adobe Advertising till Analytics, lägger du sedan till spårningskoden för AMO ID i slutet av landningssidans suffix på kontonivå.

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för tjänsten för spårning av konvertering av Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-format](/help/integrations/analytics/ids.md#amo-id-formats)
