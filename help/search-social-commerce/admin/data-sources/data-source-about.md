---
title: Synkronisera  [!DNL Google Analytics] konverteringsmått
description: Lär dig mer om synkronisering av  [!DNL Google Analytics] konverteringsmått för optimering och rapportering.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Synkroniserar konverteringsmått för [!DNL Google Analytics]

I Sök, Socialt och Commerce kan du synkronisera konverteringsvärden för ett specifikt [!DNL Google Analytics]-konto, en specifik egenskap och en visningskombination för optimering och rapportering. [Sidvyer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [sessioner](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Studsfrekvens](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (beräknat som studsar/sessioner) och [Sessionsvaraktighet](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) inkluderas automatiskt. Du kan inkludera upp till 16 ytterligare mått per datakälla.

>[!NOTE]
>
>Advertising DSP-användare kan använda konverteringsmåtten som anpassade mål och i rapporter.

All API-användning för dataöverföringar utvärderas till ett projekt i det tillämpliga [!DNL Google Analytics]-kontot. Du kan visa dina kvoter för det här projektet i [den [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Mer information om [kvoter och anropsgränser för att rapportera API-begäranden](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) finns i dokumentationen för [!DNL Google Analytics].

I följande steg beskrivs processen för synkronisering av konverteringsdata från [!DNL Google Analytics].

1. [Utför nödvändiga uppgifter](data-source-prerequisites.md)

   * Implementera en Adobe Advertising-token (`ef_id` frågesträngsparameter) i URL:erna för landningssidan för alla tillämpliga annonskonton.

   * Hämta Adobe Advertising-token (`ef_id` frågesträngsparameter) i en [!DNL Custom Dimension] i [!DNL Google Analytics].

1. (Endast kontoadministratör, agentkontohanterare, kontohanterare [!DNL Adobe] och administratörsanvändare) [Skapa en datakälla per [!DNL Google Analytics] konto, egenskap och visningskombination](data-source-configure.md).

   Om du vill integrera mätvärden för flera egenskaper eller för flera vyer för en enda egenskap skapar du en separat datakälla för varje.

   När en datakälla har konfigurerats hämtar Search, Social och Commerce data dagligen med början 05:00 i annonsörens tidszon. När mätvärdena är tillgängliga kan ni inkludera dem i vyer över kampanj- och portföljhantering och i rapporter, och använda dem i optimeringsmål efter behov.

>[!MORELIKETHIS]
>
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] vy som datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgängliga [!DNL Google Analytics] mått](data-source-ga-metrics.md)
