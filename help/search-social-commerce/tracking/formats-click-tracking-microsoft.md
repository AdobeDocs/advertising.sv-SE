---
title: Klickspårningsformat för  [!DNL Microsoft Advertising]
description: Lär dig mer om knappspårningsformat för  [!DNL Microsoft Advertising] konton.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# Klickspårningsformat för [!DNL Microsoft Advertising]

Nedan följer basspårningsmallen och landningssidans suffix (det sista URL-suffixet) som krävs för Search, Social och Commerce för [!DNL Microsoft Advertising].

## Spåra mallformat

### Sök- och målgruppsnätverk (utom sitelinks)

Följande format gäller för alla spårbara annonstyper i sök- och målgruppsnätverk.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).
>
>* `{adextensionid}` används inte.
>
>* (Sitelinks) Du kan se vilka konverteringar som har gjorts genom att klicka på en sitellänk genom att generera en [!UICONTROL Transaction Report]. Kolumnvärdet [!UICONTROL Link Type] för en sitelink är `sl:<Sitelink text>`, till exempel `sl:See Current Offers`.

### Shoppingnätverk

Följande format gäller för shoppingannonser i shoppingnätverk. Du kan ange en spårningsmall på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `{TargetId}` representerar ID:t för a) antingen nyckelordet eller b) nyckelordet och återmarknadsföringslistan (publik) som utlöste annonsen (till exempel &quot;kwd-123:aud-456&quot; för både ett nyckelord och en återmarknadsföringslista eller &quot;kwd-123&quot; för enbart nyckelord).
>
>* (Valfritt) I stället för att ange spårningsmallar på konto-, kampanj-, annonsgruppsnivå eller produktgruppsnivå kan du lägga till spårnings-URL:en till produktdata i [!DNL Microsoft Merchant Center]-kontot. Om du vill göra det inkluderar du spårnings-URL:en, tillsammans med värdet i fältet `link` eller `mobile_link`, beroende på vad som är lämpligt, i en anpassad kolumn, [bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0), i produktflödet. Värdet i fältet `bingads_redirect` ersätter värdena i fälten `link` och `mobile_link`. URL-adresser som skapas med den här metoden innehåller inte spårningsparametrar som anges i inställningarna för kontot Sök, Socialt &amp; Commerce eller för kampanjen.

## Format för landningssidans suffix (sista URL-suffix)

>[!NOTE]
>
>Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

### Sök- och målgruppsnätverk

Konton som använder Adobe Advertising-konverteringsspårning måste inkludera annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla följande:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

  `&ev_efid={msclkid}:G:s`

### Shoppingnätverk

Konton som använder Adobe Advertising-konverteringsspårning måste inkludera annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]) i suffixet:

* När annonsören har en Adobe Analytics-integrering måste suffixet innehålla följande:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* När annonsören inte har någon Adobe Analytics-integrering måste suffixet innehålla följande:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för Adobe Advertising-tjänsten för konvertering](formats-click-tracking-about.md)
>* [AMO ID-format](https://experienceleague.adobe.com/sv/docs/analytics/components/dimensions/amo-id#dimension-items)
