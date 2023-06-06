---
title: Synkronisering [!DNL Google Analytics] konverteringsmått
description: Läs om synkronisering [!DNL Google Analytics] konverteringsstatistik för optimering och rapportering.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Synkronisering [!DNL Google Analytics] konverteringsmått

Sökning, sociala medier och handel kan synkronisera konverteringsvärden för en viss [!DNL Google Analytics] kombination av konto, egenskap och vy för optimering och rapportering. [Sidvyer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessioner](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Studsfrekvens](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (beräknat som studsar/sessioner), och [Sessionsvaraktighet](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) ingår automatiskt. Du kan inkludera upp till 16 ytterligare mått per datakälla.

>[!NOTE]
>
>DSP kan använda konverteringsmåtten som anpassade mål och i rapporter.

All API-användning för dataöverföringar bedöms till ett projekt i tillämpliga [!DNL Google Analytics] konto. Du kan visa dina kvoter för det här projektet i [den [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Se [!DNL Google Analytics] om du vill ha mer information om [kvoter och anropsgränser för rapportering av API-begäranden](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

I följande steg beskrivs processen för synkronisering av konverteringsdata från [!DNL Google Analytics].

1. [Utför nödvändiga uppgifter](data-source-prerequisites.md)

   * Implementera en Adobe Advertising-token (`ef_id` frågesträngsparameter) på landningssidans URL:er för alla tillämpliga annonskonton.

   * Fånga reklamtoken för Adobe (`ef_id` frågesträngsparameter) i en [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Byråkontoadministratör, kontoansvarig för myndighet, [!DNL Adobe] kontohanteraren och endast administratörsanvändare) [Skapa en datakälla per [!DNL Google Analytics] kombination av konto, egenskap och vy](data-source-configure.md).

   Om du vill integrera mätvärden för flera egenskaper eller för flera vyer för en enda egenskap skapar du en separat datakälla för varje.

   När en datakälla har konfigurerats hämtar Search, Social, &amp; Commerce data varje dag, med början 05:00 i annonsörens tidszon. När mätvärdena är tillgängliga kan ni inkludera dem i vyer över kampanj- och portföljhantering och i rapporter, och använda dem i optimeringsmål efter behov.

>[!MORELIKETHIS]
>
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] visa som en datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgänglig [!DNL Google Analytics] mått](data-source-ga-metrics.md)

