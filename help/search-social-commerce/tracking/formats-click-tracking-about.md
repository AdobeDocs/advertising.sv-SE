---
title: Om URL-format för klickspårning för tjänsten för spårning av konvertering i Adobe Advertising
description: Lär dig mer om de klickningsspårningsformat som stöds för annonsnätverk.
exl-id: 12148caf-fde6-4ac2-b8b4-222409895dd7
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '253'
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

* `<ad network ID>` är en variabel för det numeriska ID:t för det angivna annonsnätverket, till exempel *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (borttagen), eller *106* for [!DNL Pinterest] (föråldrat).

* `<tracking ID>` är en variabel för en systemgenererad spårnings-ID-sträng som identifierar ett nyckelord, en annons eller en placering som är unik i kontot. Strängen varierar beroende på annonsnätverk.

* `<the landing page>` är en variabel som representerar URL:en på din webbplats som slutanvändarna dirigeras till. För konton med mål-URL:er är det här värdet en URL. För konton med spårningsmallar är det här värdet en parameter (till exempel `{lpurl}`) som representerar den slutliga URL:en.

Se de separata sidorna som indikerar [[!DNL Baidu] format](formats-click-tracking-baidu.md), [[!DNL Google Ads] format](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] format](formats-click-tracking-microsoft.md), [[!DNL Naver] format](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] format](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] format](formats-click-tracking-yahoo-japan.md)och [[!DNL Yandex] format](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Klickspårningsformat för sponsrade annonser på [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Klickningsspårningsformat för [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Klickningsspårningsformat för [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Naver]](formats-click-tracking-naver.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Klickspårningsformat för sponsrade annonser på [!DNL Yandex]](formats-click-tracking-yandex.md)
