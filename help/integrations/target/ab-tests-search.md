---
title: Konfigurera A/B-tester för Adobe Advertising Search, Social och Commerce Ads i Adobe Target
description: Lär dig hur du ställer in ett A/B-test i [!DNL Target] för dina [!DNL Google Ads] och [!DNL Microsoft Advertising] annonser i Sök, Socialt och Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Konfigurera A/B-tester i Adobe Target för Advertising Search, Social och Commerce Ads

*Endast annonsörer med Advertising Search, Social och Commerce*

Endast *[!DNL Google Ads]och [!DNL Microsoft Advertising] konton*

Med Adobe Advertising och Adobe Target är det enkelt att konfigurera A/B-tester för landningssidor för digital reklamtrafik [!DNL Google Ads] och [!DNL Microsoft Advertising] för att:

* Förbättra konverteringsgraden (CVR) och effektivitetsåtgärderna för förvärv (såsom CPA, CPL och CAC).

* Leverera en mer personaliserad landningssida som är relevant för annonsen (t.ex. matchning av bild-/videoredigeringssignal, kopia, nyckelord eller annan annonssignal till landningssidan).

Du kan också kombinera de inbyggda [[!DNL Analytics]  för Advertising](/help/integrations/analytics/overview.md) och [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=sv-SE) integreringsrapporteringsdimensionerna som är integrerade i Adobe Analytics för att mäta och visualisera testdata med [!DNL Analytics] mätvärden och lyckade händelser.

I följande avsnitt finns information om krav, anvisningar om hur du ställer in A/B-tester i [!DNL Target] för klickbar trafik från annonser i Search, Social och Commerce samt tips om hur du mäter och visualiserar dina tester i [!DNL Analytics].

## Förutsättningar

### Nödvändiga produkter

* Search, Social, &amp; Commerce
* [!DNL Target]

### Rekommenderade produkter och integreringar

* [!DNL Analytics]

* [[!DNL Analytics] för Advertising](/help/integrations/analytics/overview.md)-integrering<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integrering av [[!DNL Analytics] för [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=sv-SE)

## Steg 1: Skapa en A/B-testaktivitet i [!DNL Target] för sökning, sociala medier och Commerce

I följande anvisningar finns information om användningen av sökningar, sociala medier och Commerce.

1. [Logga in på Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=sv-SE).

1. [Skapa ett A/B-test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=sv-SE):

   1. I fältet **[!UICONTROL Enter Activity URL]** anger du landningssidans URL för testet.

   1. Ange framgångsmåttet för testet i fältet **[!UICONTROL Goal]**.

      >[!NOTE]
      >
      >Kontrollera att [!DNL Analytics] är aktiverat som en datakälla i [!DNL Target] och att rätt rapportserie har valts.

   1. Ange **[!UICONTROL Priority]** till `High` eller `999` för att förhindra konflikter när användare i testsegmentet får en felaktig upplevelse på plats.


   1. I **[!UICONTROL Reporting Settings]** väljer du **[!UICONTROL Company Name]** och **[!UICONTROL Report Suite]** som är anslutna till ditt Search-, Social- och Commerce-konto.

      Fler tips om rapportering finns i [Rapportera bästa praxis och felsökning](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=sv-SE).

   1. Ange lämpliga start- och slutdatum för testet i fältet **[!UICONTROL Date Range]**.

   1. Välj **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. I fältet **[!UICONTROL Value]** anger du [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] eller [!UICONTROL Network Ad ID] för den relevanta annonsnätverksenheten i Sök, Socialt och Commerce. Detta gör att du kan använda frågesträngsparametrarna [!DNL Target] för klickbara målgrupper för entiteten.

      Du kan hitta ID:t genom att [lägga till den relevanta ID-kolumnen i entitetsvyn](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      kolumnen ![[!UICONTROL Network Account ID] i kolumnen [!UICONTROL Accounts] view ](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] i [!UICONTROL Accounts] view ")

      Samarbeta med kontoteamet på Adobe om du behöver hjälp.

   1. För **[!UICONTROL Traffic Allocation Method]** väljer du **[!UICONTROL Manual (Default)]** och delar målgruppen 50/50.

   1. Spara aktiviteten.

1. Använd [Visual Experience Composer som mål](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=sv-SE) om du vill göra designändringar i A/B-testsidmallen.

   * Upplevelse A: Redigera inte eftersom det är standardupplevelsen/styrningen av landningssidan utan personalisering.

   * Upplevelse B: Använd användargränssnittet [!DNL Target] för att anpassa landningssidmallen baserat på de resurser som ingår i testet (t.ex. rubriker, kopiering, knappplacering och kreatörer).

   >[!NOTE]
   >
   >Exempel på användningsfall för kreativa tester kan du kontakta Adobe Account Team.

## Steg 2: Konfigurera din [!DNL Analytics for Target] Analysis Workspace i [!DNL Analytics]

[!DNL Analytics for Target] (A4T) är en integrering med flera lösningar som gör att annonsörer kan skapa [!DNL Target]-aktiviteter baserat på konverteringsstatistik för [!DNL Analytics] och målgruppssegment och sedan mäta resultatet med [!DNL Analytics] som rapportkälla. All rapportering och segmentering för den aktiviteten baseras på datainsamling [!DNL Analytics].

Mer information om [!DNL Analytics for Target], inklusive en länk till implementeringsanvisningar, finns i [Adobe Analytics som rapportkälla för Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=sv-SE).

### Konfigurera panelen [!DNL Analytics for Target]

Konfigurera [!DNL Analytics for Target panel] i Analysis Workspace för att analysera dina [!DNL Target]-aktiviteter och -upplevelser. Tänk på följande viktiga pekare och information om dina rapporter.

#### Mått

* Skapa en panel på arbetsytan som är specifik för det Adobe Advertising-konto, den kampanj eller den annonskoncern <!-- only applicable entities? --> som testet kördes för. Använd sammanfattningsvisualiseringar för att visa Adobe Advertising-mått i samma rapport som testprestandan [!DNL Target].

* Prioritera med hjälp av statistik på plats (t.ex. besök och konverteringar) för att mäta prestanda.

* Förstå att aggregerade mediemått från Adobe Advertising (som visningar, klick och kostnader) inte kan matchas mot [!DNL Target]-värden.

#### Dimensioner

Följande dimensioner gäller [!DNL Analytics for Target]:

* **Målaktiviteter**: Namn på A/B-testet

* **Målupplevelser**: Namn på landningssidans upplevelser som används i aktiviteten

* **Målaktivitet** > **Upplevelse**: Aktivitetsnamnet och upplevelsenamnet på samma rad

### Felsökning av analyser för [!DNL Target]-data

Om du inom Analysis Workspace märker att data om aktivitet och upplevelser är minimala eller inte är ifyllda gör du så här:

* Kontrollera att samma [!UICONTROL Supplemental Data ID] (SDID) används för både [!DNL Target] och [!DNL Analytics]. Du kan verifiera SDID-värdena med hjälp av [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=sv-SE) på landningssidan som kampanjen driver användare till.

[SDID-värden (Additional Data ID) i Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* På samma landningssida kontrollerar du att a) [!UICONTROL Hostname] som visas i Adobe Debugger under [!UICONTROL Solutions] > [!UICONTROL Target] matchar b) [!UICONTROL Tracking Server] som visas i [!DNL Target] för aktiviteten (under [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] kräver att en [!DNL Analytics]-spårningsserver skickas i anrop från [!DNL Target] till datainsamlingsservern [!DNL Modstats] för Analytics.<!-- just "to Analytics?"-->

[Värdnamnsvärde i Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Spårningsservervärde i mål](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Ytterligare läsning

* [Integrera mål med analys](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=sv-SE) - Beskriver hur du konfigurerar [!DNL Target]-rapportering i Analysis Workspace.
* [A/B-testöversikt](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=sv-SE) - Beskriver A/B-testaktiviteter, som du kan använda med reklam för sökningar, sociala medier och Commerce.
* [Översikt över Analytics för Advertising](/help/integrations/analytics/overview.md) - Här presenteras Analytics för Advertising, som gör att du kan spåra klicknings- och genomskinlighetsinteraktioner på din Analytics-instans.

>[!MORELIKETHIS]
>
>* [Konfigurera A/B-tester i Adobe Target för Advertising DSP Ads](ab-tests-dsp.md)
