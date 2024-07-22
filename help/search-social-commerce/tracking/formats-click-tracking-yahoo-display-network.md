---
title: Klickspårningsformat för  [!DNL Yahoo! Display Network]
description: Lär dig mer om knappspårningsformat för  [!DNL Yahoo! Display Network] konton.
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# Klickspårningsformat för sponsrade annonser på [!DNL Yahoo! Display Network]

Följande URL-format för basdestinationen gäller för sponsrade annonser:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Exempel:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` är en variabel för annonsörens unika ID i Adobe Advertising.
>
>* Det här formatet anger att tokenöverföring är aktiverat för kampanjen (standard). Om överföring av token är inaktiverat ersätter du `cq?` efter `<advertiser_ID>` med `c?`.
>
>* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till.

>[!MORELIKETHIS]
>
>* [Om URL-format för klickspårning för tjänsten för spårning av konvertering av Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-format](/help/integrations/analytics/ids.md#amo-id-formats)
