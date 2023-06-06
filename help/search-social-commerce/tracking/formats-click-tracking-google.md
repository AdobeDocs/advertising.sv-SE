---
title: Klickningsspårningsformat för [!DNL Google Ads]
description: Läs mer om klickningsspårningsformaten för [!DNL Google Ads] konton.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Klickningsspårningsformat för [!DNL Google Ads]

Nedan följer basspårningsmallens och landningssidans suffixformat (det sista URL-suffixet) som Sök, Socialt, &amp; Commerce kräver för [!DNL Google Ads].

## Spåra mallformat

### Sök/visa nätverk, inklusive sitelinks

Följande format gäller för alla spårbara annonstyper i sök- och visningsnätverk samt för sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exempel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* The [!DNL ValueTrack] parametrar för att ange slutliga URL:er i spårningsmallar måste vara antingen `{lpurl}` eller `!{unescapedurl}`.
>
>* (Textannonser) Parametern `ev_pl` (för placements) saknar värde. När du lägger bud `ev_ln` (för nyckelord) har inget värde. När du lägger ett bud per annonsgrupp eller någon annan dimension, båda `ev_ln` och `ev_pl` har inga värden.
>
>* (Dynamiska sökannonser) `{keyword}` anger måluttrycket för den dynamiska sökningen, till exempel `_cat:[VALUE]` eller `_url:[VALUE]`.
>
>* (Dynamiska sökannonser) [!DNL Google Ads] bestämmer den slutliga URL:en dynamiskt, så du behöver inte ange en.
>
>* (Sitelinks) Du kan se vilka konverteringar som har gjorts genom att klicka på en sitellänk genom att skapa en [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] kolumnvärdet för en sitelink är `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.


### Shoppingnätverk

Följande format gäller för shoppingannonser och produktgrupper i shoppingnätverk. Du kan ange en spårningsmall på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exempel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* The [!DNL ValueTrack] parametrar för att ange slutliga URL:er i spårningsmallar måste vara antingen `{lpurl}` eller `!{unescapedurl}`.
>
>* [!DNL Google Ads] använder URL:er i Google Merchant Center-flödet som de slutliga URL:erna, så du behöver inte ange slutgiltiga URL:er för dina produktdata eller produktgrupper.
>
>* Du kan se vilka konverteringar som har gjorts genom att klicka på en shoppingannons genom att skapa en [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] kolumnvärdet för en produkt och är pla:`<product ID>`, till exempel `pla:8525822`.


## Format för landningssidans suffix (sista URL-suffix)

Konton som använder konverteringsspårning för annonsering i Adobe måste innehålla annonsnätverkets klickidentifierare (`gclid` for [!DNL Google Ads]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla något av följande:

   * [!DNL Google Ads] konton som använder de senaste `s_kwcid` som stöder kampanjrapporter och rapporter på annonsnivå för maximala resultatkampanjer samt utkast och experimentkampanjer:

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

      Om kontot har en s_kwcid-implementering på serversidan och konto- eller kampanjinställningen &quot;[!UICONTROL Auto Upload]&quot; är aktiverat läggs parametern till automatiskt. Annars måste du lägga till det manuellt.

   * Alla andra [!DNL Google Ads] konton:

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

   `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.
>
>* (Dynamiska sökannonser; annonsörer med Adobe Analytics och utan spårning på serversidan) När du vill ta med spårning för omvänd feed från Adobe Advertising till Analytics, lägger du till `s_kwcid` Spårningskod till slutet av landningssidans suffix på kontonivå.


>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för konverteringstjänsten Adobe](formats-click-tracking-about.md)
>* [Format för s\_kwcid-spårningskod](skwcid-tracking-parameter.md)

