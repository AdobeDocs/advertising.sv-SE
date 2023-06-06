---
title: Klickningsspårningsformat för [!DNL Baidu]
description: Läs mer om klickningsspårningsformaten för [!DNL Baidu] konton.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Klickspårningsformat för sponsrade annonser på [!DNL Baidu]

Följande URL-format för basdestinationen gäller för sponsrade annonser:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `<campaignID>` är en variabel för det numeriska kampanj-ID:t.
>
>* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.


>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för konverteringstjänsten Adobe](formats-click-tracking-about.md)
>* [Format för s\_kwcid-spårningskod](skwcid-tracking-parameter.md)

