---
title: Implementera [!DNL Microsoft Advertising] utökade konverteringar för offlinekonverteringar
description: Lär dig mer om arbetsflödet för att konfigurera  [!DNL Microsoft Advertising] förbättrade konverteringar för offlinekonverteringar.
feature: Search Campaign Management, Conversions
source-git-commit: 8f87e5bdab25aa527e72d7e9c75411267fe63780
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Implementera [!DNL Microsoft Advertising] utökade konverteringar för offlinekonverteringar

Endast *[!DNL Microsoft Advertising]konton*

Med [[!DNL Microsoft Advertising] förbättrade konverteringar](https://help.ads.microsoft.com/#apex/ads/en/60178) kan du mappa användare till offlinekonverteringar med hjälp av dina egna konverteringsdata. Använd förbättrade konverteringar i miljöer där klicknings-ID:n inte är tillgängliga, till exempel för att spåra telefonförsäljning eller e-postförsäljning som är ett resultat av webbleads.

I Search, Social och Commerce kan du

* Visa dina befintliga förbättrade konverteringar för offlinekonverteringar.

  Search, Social, &amp; Commerce synkroniserar dina befintliga förbättrade konverteringar dagligen kl. 05:00 i annonsörens tidszon.

* Ladda upp konverteringsdata från första part, offline för att mappa till era befintliga förbättrade konverteringsmål.

* Inkludera era förbättrade konverteringar som mätvärden i rapporter och som viktade mätvärden i mål för optimering.

Utför följande steg om du vill använda den här funktionen.

1. Följ alla krav i hjälpen för [!DNL Microsoft Advertising] om [Förbättrade konverteringar](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. [Konfigurera ett förbättrat konverteringsmål inom [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Ladda upp egna data, inklusive hash-kodade e-postadresser eller telefonnummer, och tilldela konverteringen för ett visst konto så ofta det behövs. Du kan slutföra det här steget från antingen [Sök, Social och Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) eller inifrån [!DNL Microsoft Advertising].

   * I Search, Social och Commerce kan du hämta en mall i [!DNL Microsoft Excel]-format, ange konverteringsdata och spara filen lokalt och sedan överföra den redigerade filen.

     Alla överförda data synkroniseras i realtid till [!DNL Microsoft Advertising].

   * Mer information om hur du överför data inom [!DNL Microsoft Advertising] finns i avsnittet Konfigurera förbättrade konverteringar för offlinekonverteringar i hjälpen för [!DNL Microsoft Advertising] om [Förbättrade konverteringar](https://help.ads.microsoft.com/#apex/ads/en/60178).

>[!MORELIKETHIS]
>
>* [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
