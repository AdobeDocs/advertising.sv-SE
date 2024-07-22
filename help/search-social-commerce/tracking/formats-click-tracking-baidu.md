---
title: Klickspårningsformat för  [!DNL Baidu]
description: Lär dig mer om knappspårningsformat för  [!DNL Baidu] konton.
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Klickspårningsformat för sponsrade annonser på [!DNL Baidu]

Följande URL-format för basdestinationen gäller för sponsrade annonser:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `<campaignID>` är en variabel för det numeriska kampanj-ID:t.
>
>* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för tjänsten för spårning av konvertering av Adobe Advertising](formats-click-tracking-about.md)
>* [AMO-ID-format](/help/integrations/analytics/ids.md#amo-id-formats)
