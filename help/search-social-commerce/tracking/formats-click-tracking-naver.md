---
title: Klickningsspårningsformat för [!DNL Naver]
description: Läs mer om klickningsspårningsformaten för [!DNL Naver] konton.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Klickspårningsformat för sponsrade annonser på [!DNL Naver]

Följande URL-format för basdestinationen gäller för sponsrade annonser:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID inom Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om tokenöverföring är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>

* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för konverteringstjänsten Adobe](formats-click-tracking-about.md)
>* [Format för s\_kwcid-spårningskod](skwcid-tracking-parameter.md)
