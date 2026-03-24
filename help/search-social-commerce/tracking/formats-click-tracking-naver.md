---
title: Klickspårningsformat för  [!DNL Naver]
description: Lär dig mer om knappspårningsformat för  [!DNL Naver] konton.
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '90'
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
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för Adobe Advertising-tjänsten för konvertering](formats-click-tracking-about.md)
>* [AMO ID-format](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
