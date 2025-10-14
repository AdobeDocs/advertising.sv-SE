---
title: (Nytt användargränssnitt) Om mål
description: Lär dig mer om vilka mål du ska uppnå.
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nytt användargränssnitt) Om mål

*Beta-funktion*

Mål är mål som en annonsör sätter upp för att uppfylla sina affärsmål, t.ex. maximera vinsten eller uppnå ett visst försäljningsmål. Både Advertising Search, Social, Commerce och Advertising DSP har följande syften:

* Varje Search-, Social- och Commerce-portfölj måste ha ett mål så att optimeringsfunktionen kan skapa klicknings- och intäktsmodeller för portföljen.

* I DSP visas mål som anpassade mål för DSP-konton som är länkade till Search-, Social- och Commerce-konton. Varje paket som använder optimeringsmålen &quot;Highest Return on Ad Spend (ROAS)&quot; eller &quot;Lowest Cost per Acquisition (CPA)&quot; måste innehålla ett anpassat mål som hjälper till att uppnå det övergripande optimeringsmålet.

Ett mål består av de konverteringsmått som ska spåras och optimeras samt de relativa vikterna för dessa mätvärden. Anta t.ex. att en nättidskrift med två abonnemangsnivåer online och en abonnemangsnivå och målet &quot;maximera vinsten&quot; har tre mätvärden: &quot;grundläggande onlineabonnemang&quot; som värderas till 20 USD, &quot;premiumabonnemang online&quot; som värderas till 40 USD och &quot;prenumerationer&quot; som värderas till 30 USD. Om tidskriften vill ge tyngd i enlighet med det engångs-monetära värdet för prenumerationen, är den relativa vikten för måtten 1, 2 respektive 1,5.

För varje mätvärde i målet kan du:

* Konfigurera olika vikter för konverteringar från mobila enheter.

* Märk måttet som ett [!UICONTROL Goal]-mått eller ett [!UICONTROL Assist]-mått.

* Använd viktrekommendationer på mätvärdena.

>[!NOTE]
>* (Sök, Socialt och Commerce) Du kan associera ett mål med en portfölj när du [skapar portföljen](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) eller genom att [ändra portföljinställningarna](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md) senare.
>* (Annonsörer med DSP-konton som är länkade till konton för sökning, sociala medier och Commerce) I Advertising DSP kan du välja ett mål som ett [anpassat optimeringsmål](/help/dsp/campaign-management/packages/package-settings.md) för ett paket med paketnivåpaketering.
>* Du kan använda samma mål för flera söknings-, sociala och Commerce-portfolior och/eller flera DSP-paket.
>* Måtten för varje mål i vyn [!UICONTROL Objectives] innehåller inte data från DSP.

## Tillgängliga mått

Du kan inkludera något av följande i dina mål:

* Mätvärden som Adobe Advertising spårar med hjälp av [Adobe Advertising-konverteringsspårningspixel](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Advertiser-spårade mätvärden från konverteringsfeedfiler](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Annonsörer med [!DNL Adobe Analytics for Advertising]) [Konverterings- och webbplatsengagemangsmått synkroniserade från Adobe Analytics](/help/integrations/analytics/overview.md).

  I Search, Social och Commerce beaktas följande [webbplatsengagemangsmått](/help/integrations/analytics/analytics-data-in-advertising.md) automatiskt i algoritmerna för portföljbudgivning: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` och `bounces`.

* [!DNL Google] mått:<!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads]-spårade konverteringar &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) från synkroniserade [!DNL Google Ads]-konton.

   * (Annonsörer med [[!DNL Google Analytics] integreringar](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Sidvyer, sessioner, avhoppsfrekvens (beräknat som studsar/sessioner) och sessionsvaraktighet.

     I Search, Social och Commerce inkluderas dessa värden automatiskt i algoritmerna för portföljbudgivning.

## Möjlighet att överföra mål till annonsnätverken

Du kan [överföra målen för kontots portföljer till  [!DNL Google Ads]  och/eller [!DNL Microsoft Advertising] som konverteringar](/help/search-social-commerce/tools/objective-upload-to-networks.md) om du vill, så att du kan använda dem för optimering på kampanj- eller annonsnivå. När du aktiverar alternativet skickar Search, Social och Commerce viktade intäktsdata på nivån EF ID (klicka på ID) till annonsnätverket dagligen. Den utelämnar alla data som spåras i annonsnätverket.

>[!MORELIKETHIS]
>
>* [Skapa ett mål](objective-create.md)
>* [Redigera ett mål](objective-edit.md)
>* [Ta bort ett mål](objective-delete.md)
>* [Använd viktrekommendationer på ett mål](objective-apply-weight-recommendations.md)
>* [Målinställningar](objective-settings.md)
