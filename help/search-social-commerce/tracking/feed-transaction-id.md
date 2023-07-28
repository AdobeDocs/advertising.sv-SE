---
title: Konverteringsspårning med en transaktions-ID-feed
description: Lär dig mer om hur du använder ett transaktions-ID-flöde för konverteringsspårningsdata.
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Konverteringsspårning med en transaktions-ID-feed

När en annonsörer har både online- och offlinetransaktioner kan Adobe Advertising spåra onlinetransaktionerna via pixeln Adobe Advertising-konverteringsspårning, och annonsören kan spåra offlinetransaktionerna med ett transaktions-ID och leverera dem via en feed:

* För onlinetransaktioner spårar Adobe Advertising klickningarna på era annonser och de resulterande transaktionerna på er webbplats.

* Annonsören måste spåra offlinekonverteringar och skicka flödesfiler på transaktionsnivå till Adobe Advertising.

## Implementeringsöversikt

*Kontorsansvarig [!DNL Adobe] endast kontohanterare och administratörsanvändarroller*

1. Använd alternativen för konto- eller kampanjspårning &quot;[!UICONTROL EF Redirect]och &quot;[!UICONTROL Auto Upload]&quot; för att automatiskt generera en mål-URL eller en slutlig URL för varje nyckelord (för nyckelordsspårning) eller annons (för annonsnivåspårning) i kontot eller kampanjen.

1. Ställ in spårning av Adobe Advertising för onlinekonverteringar. Detta är samma process som för annonsörer med pixelbaserad konverteringsspårning i Adobe Advertising. Det är viktigt att generera konverteringstaggar som innehåller en parameter för ett unikt transaktions-ID (`ev_transid=<transid>`).

1. För offlinedelen av varje transaktion genererar annonsören samma transaktions-ID som användes i onlinedelen av transaktionen som ska inkluderas i flödesfilen.

1. Annonsören överför en fil med [obligatoriska konverteringsdata](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) till den angivna serverplatsen.

1. Technical Services tolkar konverteringsdata i de överförda filerna och överför sedan data till Adobe Advertising. Adobe Advertising spårar sedan data mot enskilda nyckelord, annonser och placeringar och skapar intäktsprognoser för varje.

1. Tekniska tjänster validerar bearbetade data mot feed-data och kontrollerar om det finns [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Datakrav för dataflöden som använder ett transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
