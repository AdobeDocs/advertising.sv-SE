---
title: '[!DNL Adobe] [!DNL Audience Analytics] för kunder i Adobe Advertising'
description: Lär dig hur du använder  [!DNL Adobe] [!DNL Audience Analytics] för annonseringsanvändningsfall
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] för Adobe Advertising-kunder

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) är en integrering mellan Adobe Audience Manager och Adobe Analytics som gör det möjligt för Audience Manager-kunder att skicka segment till [!DNL Analytics] för bättre insikter om webbplatsaktivitet.

Adobe Advertising-kunder kan dra nytta av [!DNL Audience Analytics]. Integreringen gör att du kan:

* Skicka exponeringsdata för Adobe Advertising direkt till [!DNL Analytics] för att fastställa påverkan av aktiviteten för den övre tratten på webbplatsaktiviteten längre fram i kedjan.

* Bestäm marknadsföringskanaler och ingångspunkter för sajter utifrån exponeringsannonser i den övre tratten.

* Layer the integration with [!DNL Analytics for Advertising] to include third-party population from [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising] data for more insights about user profiles.

  [!DNL Audience Marketplace] ger åtkomst till datafeeds från tredje part med prenumerationsmodeller för aktivering, som gör att köpare kan skicka data till ett mål. Om data används inom ett [!DNL Analytics]-mål tillämpas inte aktiveringsavgifter.

* (Annonsörer med Advertising DSP) Lägg till ytterligare exponeringssegment för att få en helhetsbild av hanteringen.

  Advertising DSP kan skicka exponeringsdata till Audience Manager som användbara signaler genom att implementera pixlar för antingen Adobe Experience Platform eller Audience Manager. Om samma data vidarebefordras till [!DNL Analytics] aktiveras avancerad dataanalys. Mer information finns i [Översikt över Adobe Advertising Media Data Integration med Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md).

Mer information om [!DNL Audience Analytics], inklusive dess förutsättningar och arbetsflöde, finns i [Audience Analytics översikt](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).

## Exempel på hur du använder [!DNL Audience Analytics]-data med Adobe Advertising-data

Nedan följer exempel på hur du kan använda kombinerade data i [!DNL Analytics] [!DNL Analysis Workspace].

### Se effekten av Övre trattaktivitet på nedströmsaktivitet

Använd exponeringssegment i Audience Manager för att se hur aktiviteten på den övre delen av arbetsytan påverkar webbplatsaktiviteten nedströms. Inkludera makro-ID:n från Adobe Advertising eller tredje part i spårningspixlarna för att spåra påverkan på en detaljerad nivå, från kampanjnivå till nivån för den webbplats där användaren exponerades.

Huvudsakliga fördelar:

* Spåra exponering med tratt/annonstyper och använd [!DNL Audience Analytics] för att fastställa ingångshastigheter och överlappa nästa fas av kundresan.

* Fastställ effekten av den övre trattaktiviteten på aktiviteter längre fram i kedjan.

* Anslut [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> och [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> för att fastställa en helhetsresa till webbplatsen.

Följande är exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Se effekten av aktiviteten i den övre tratten på aktivitet i den underordnade platsen](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Använd [!DNL Audience Analytics] segmentdata från tredje part för analys av användarprofiler

Använd Audience Manager-segment från tredje part för att få en djupare analys av hur användare interagerar med webbplatsen. Ni kan använda informationen för att avgöra vilka nya målgrupper från tredje part som medierna ska aktiveras för, baserat på hur profiler från tredjepartssegmenten interagerar med viktiga resultatindikatorer för mediekampanjernas webbplatser.

>[!TIP]
> Använd måtten Audience Manager `Audiences ID` och `Audiences Name` i hela [!DNL Analytics], precis som andra dimensioner som [!DNL Analytics] samlar in.

Följande är exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Använda segment från tredje part för att förbättra användarprofilanalysen](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrering av Adobe Advertising med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
