---
title: Om URL-format för klickspårning för tjänsten för spårning av konvertering i Adobe Advertising
description: Lär dig mer om de klickningsspårningsformat som stöds för annonsnätverk.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Om URL-format för klickspårning för tjänsten för spårning av konvertering i Adobe Advertising

Spårningsmallar, landningssidessuffix (sista URL-suffix) och mål-URL:er för annonskonton och kampanjer som använder Adobe Advertising-konverteringstjänsten har följande format:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

där:

* `http://pixel.everesttech.net` dirigerar om användaren till Adobe Advertising pixelservrar.

* `<advertiser_ID>` är en variabel för det unika användar-ID som tilldelats annonsören i Adobe Advertising.

* `<token passing parameter>` är en variabel för något av följande:

   * `cq?` eller `rq` anger att tokenöverföring är aktiverat.

   * `c?` eller `r` betecknar att överföring av token är inaktiverat.

* `<ad network ID>` är en variabel för det numeriska ID:t för det angivna annonsnätverket, till exempel ** för [!DNL Google Ads], *10* för [!DNL Microsoft Advertising], *45* för [!DNL Meta], *86* för [!DNL Yahoo! Display Network], *87* för [!DNL Naver], *16}88* för [!DNL Baidu], *90* för [!DNL Yandex], *94* för [!DNL Yahoo! Japan Ads], *105* för [!DNL Yahoo Native] (borttagen) eller *106* för [!DNL Pinterest] (borttagen).

* `<tracking ID>` är en variabel för en systemgenererad spårnings-ID-sträng som identifierar ett nyckelord, en annons eller en placering som är unik i kontot. Strängen varierar beroende på annonsnätverk.

* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till. För konton med mål-URL:er är det här värdet en URL. För konton med spårningsmallar är det här värdet en parameter (till exempel `{lpurl}`) som representerar den slutliga URL:en.

Se de separata sidorna som indikerar [[!DNL Baidu] formaten](formats-click-tracking-baidu.md), [[!DNL Google Ads] formaten](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formaten](formats-click-tracking-microsoft.md), [[!DNL Naver] formaten](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formaten](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formaten](formats-click-tracking-yahoo-japan.md) och [[!DNL Yandex] formaten](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Klickspårningsformat för sponsrade annonser på [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Klickspårningsformat för [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Klickspårningsformat för [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Naver]](formats-click-tracking-naver.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yandex]](formats-click-tracking-yandex.md)
