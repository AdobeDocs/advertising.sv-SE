---
title: Klickningsspårningsformat för [!DNL Yandex]
description: Läs mer om klickningsspårningsformaten för [!DNL Yandex] konton.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Klickspårningsformat för sponsrade annonser på [!DNL Yandex]

Följande URL-format för basdestinationen gäller för sponsrade annonser:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.
>
>* `source_type`  är matchningstypen.
>
>* `source` är om annonsen visades på en sök- eller innehållsbaserad webbplats.
>
>* `position` är positionsnumret för annonsen i blocket. För icke-söktrafik är värdet &quot;0&quot;.
>
>* `position_type` är blocket där annonsen visades på [!DNL Yandex]. Möjliga värden: &quot;premium&quot; (top block), &quot;other&quot; (right block) eller &quot;none&quot; (non-search trafik).


>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för konverteringstjänsten Adobe](formats-click-tracking-about.md)
>* [Format för s\_kwcid-spårningskod](skwcid-tracking-parameter.md)

