---
title: Konverteringsspårning med en transaktions-ID-feed
description: Lär dig mer om hur du använder ett transaktions-ID-flöde för konverteringsspårningsdata.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Konverteringsspårning med en transaktions-ID-feed

När en annonsörer har både online- och offlinetransaktioner kan Adobe Advertising spåra onlinetransaktionerna via pixeln Adobe Advertising-konverteringsspårning, och annonsören kan spåra offlinetransaktionerna med ett transaktions-ID och leverera dem via en feed:

* För onlinetransaktioner spårar Adobe Advertising klickningarna på era annonser och de resulterande transaktionerna på er webbplats.

* Annonsören måste spåra offlinekonverteringar och skicka flödesfiler på transaktionsnivå till Adobe Advertising.

## Implementeringsöversikt

*Endast kontohanterare, [!DNL Adobe] kontohanterare och administratörsanvändarroller*

1. Använd alternativen [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] för konto- eller kampanjspårning för att automatiskt generera en mål-URL eller en slutlig URL för varje nyckelord (för nyckelordsspårning) eller annons (för annonsnivåspårning) i kontot eller kampanjen.

1. Ställ in spårning av Adobe Advertising för onlinekonverteringar. Detta är samma process som för annonsörer med pixelbaserad konverteringsspårning i Adobe Advertising. Det är viktigt att generera konverteringstaggar som innehåller en parameter för ett unikt transaktions-ID (`ev_transid=<transid>`).

1. För offlinedelen av varje transaktion genererar annonsören samma transaktions-ID som användes i onlinedelen av transaktionen som ska inkluderas i flödesfilen.

1. Annonsören överför en fil med [obligatoriska konverteringsdata](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) till den angivna serverplatsen.

1. Technical Services tolkar konverteringsdata i de överförda filerna och överför sedan data till Adobe Advertising. Adobe Advertising spårar sedan data mot enskilda nyckelord, annonser och placeringar och skapar intäktsprognoser för varje.

1. Tekniska tjänster validerar bearbetade data mot feed-data och söker efter [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Datakrav för dataflöden med ett transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
