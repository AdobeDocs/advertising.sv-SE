---
title: Klickningsspårningsformat för [!DNL Microsoft Advertising]
description: Läs mer om klickningsspårningsformaten för [!DNL Microsoft Advertising] konton.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Klickningsspårningsformat för [!DNL Microsoft Advertising]

Nedan följer basspårningsmallens och landningssidans suffix (sista URL-suffix) format som Search, Social och Commerce kräver för [!DNL Microsoft Advertising].

## Spåra mallformat

### Sök- och målgruppsnätverk (utom sitelinks)

Följande format gäller för alla spårbara annonstyper i sök- och målgruppsnätverk.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).
>
>* `{adextensionid}` används inte.
>
>* (Sitelinks) Du kan se vilka konverteringar som har gjorts genom att klicka på en sitellänk genom att skapa en [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] kolumnvärdet för en sitelink är `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.

### Shoppingnätverk

Följande format gäller för shoppingannonser i shoppingnätverk. Du kan ange en spårningsmall på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).
>
>* (Valfritt) I stället för att ange spårningsmallar på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå kan du lägga till spårnings-URL:en till produktinformationen i [!DNL Microsoft Merchant Center] konto. Om du vill göra det tar du med spårnings-URL:en tillsammans med värdet i`link`&quot; eller &quot;`mobile_link`&quot;, beroende på vad som är tillämpligt, i en anpassad kolumn &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; i produktflödet. Värdet i`bingads_redirect`&quot; ersätter värdena i &quot;`link`och &quot;`mobile_link`&quot; fält. URL-adresser som skapas med den här metoden innehåller inte spårningsparametrar som anges i inställningarna för kontot Sök, Socialt &amp; Commerce eller för kampanjen.

## Format för landningssidans suffix (sista URL-suffix)

>[!NOTE]
>
>Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

### Sök- och målgruppsnätverk

Konton som använder Adobe Advertising-konverteringsspårning måste innehålla annonsnätverkets klickningsidentifierare (`msclkid` for [!DNL Microsoft Advertising]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla följande:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

  `&ev_efid={msclkid}:G:s`

### Shoppingnätverk

Konton som använder Adobe Advertising-konverteringsspårning måste innehålla annonsnätverkets klickningsidentifierare (`msclkid` for [!DNL Microsoft Advertising]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla följande:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för tjänsten för spårning av konvertering i Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-format](/help/integrations/analytics/ids.md#amo-id-formats)
