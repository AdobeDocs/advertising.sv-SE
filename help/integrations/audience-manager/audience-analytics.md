---
title: '[!DNL Adobe] [!DNL Audience Analytics] för Adobe Advertising-kunder'
description: Lär dig hur du använder  [!DNL Adobe] [!DNL Audience Analytics] för annonseringsanvändningsfall
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] för Adobe Advertising-kunder

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=sv-SE) är en integrering mellan Adobe Audience Manager och Adobe Analytics som gör att Audience Manager-kunder kan skicka segment till [!DNL Analytics] för att få bättre insikter om webbplatsaktivitet.

Adobe Advertising-kunder kan dra nytta av [!DNL Audience Analytics]. Integreringen gör att du kan:

* Skicka Adobe Advertising exponeringsdata direkt till [!DNL Analytics] för att avgöra vilken påverkan den övre funnel-aktiviteten har på webbplatsaktiviteter längre fram i kedjan.

* Bestäm marknadsföringskanaler och startpunkter för webbplatser utifrån de övre exponeringsannonserna för funnel.

* Layer the integration with [!DNL Analytics for Advertising] to include third-party population from [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html?lang=sv-SE) with [!DNL Analytics for Advertising] data for more insights about user profiles.

  [!DNL Audience Marketplace] ger åtkomst till datafeeds från tredje part med prenumerationsmodeller för aktivering, som gör att köpare kan skicka data till ett mål. Om data används inom ett [!DNL Analytics]-mål tillämpas inte aktiveringsavgifter.

* (Annonsörer med Advertising DSP) Lägg till ytterligare exponeringssegment för att få en helhetsbild av hanteringen.

  Advertising DSP kan skicka exponeringsdata till Audience Manager som användbara signaler genom implementering av antingen Adobe Experience Platform eller Audience Manager pixlar för visningsspårning. Om samma data vidarebefordras till [!DNL Analytics] aktiveras avancerad dataanalys. Mer information finns i [Översikt över hur du skickar exponeringsdata för DSP-medier till Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md).

Mer information om [!DNL Audience Analytics], inklusive dess förutsättningar och arbetsflöde, finns i [Audience Analytics - översikt](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=sv-SE).

## Exempel på hur du använder [!DNL Audience Analytics]-data med Adobe Advertising-data

Nedan följer exempel på hur du kan använda kombinerade data i [!DNL Analytics] [!DNL Analysis Workspace].

### Se hur den övre funnel-aktiviteten påverkar nedströmsaktiviteten

Använd Audience Manager exponeringssegment för att se hur den övre funnel webbplatsaktiviteten påverkar webbplatsaktiviteten längre fram i kedjan. Inkludera makro-ID:n från Adobe Advertising eller tredje part i spårningspixlarna för att spåra påverkan på en detaljerad nivå, från kampanjnivå till nivån på webbplatsen där användaren exponerades.

Huvudsakliga fördelar:

* Spåra exponering av funnel/annonstyper och använd [!DNL Audience Analytics] för att fastställa ingångshastigheten och överlappa nästa fas av kundresan.

* Bestäm vilken påverkan den övre funnel-aktiviteten har på webbplatsaktiviteten längre fram i kedjan.

* Anslut [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->- och [!DNL Audience Analytics]-data för att fastställa en helhetsresa till webbplatsen.

<!-- (which includes the user's last exposure event) -->

Följande är exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Se effekten av den övre funnel-aktiviteten på webbplatsaktiviteter längre fram i kedjan](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Använd [!DNL Audience Analytics] segmentdata från tredje part för användarprofilanalys

Använd Audience Manager-segment från tredje part för att få en djupare analys av hur användarna interagerar med er webbplats. Ni kan använda informationen för att avgöra vilka nya målgrupper från tredje part som medierna ska aktiveras för, baserat på hur profiler från tredjepartssegmenten interagerar med viktiga resultatindikatorer för mediekampanjernas webbplatser.

>[!TIP]
> Använd Audience Manager `Audiences ID`- och `Audiences Name`-dimensionerna i hela [!DNL Analytics], precis som andra dimensioner som [!DNL Analytics] samlar in.

Följande är exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Använda segment från tredje part för att förbättra användarprofilanalysen](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising-integreringar med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
