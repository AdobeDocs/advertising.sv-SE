---
title: Konfigurera A/B-tester för Adobe Advertising DSP Ads i Adobe Target
description: Lär dig hur du ställer in ett A/B-test i [!DNL Target] för dina DSP-annonser.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Konfigurera A/B-tester i Adobe Target för Advertising DSP-annonser

*Annonsörer med endast Advertising DSP*

Adobe Advertising och Adobe Target gör det ännu enklare för marknadsförare att leverera en personaliserad och uppkopplad upplevelse i betalda medier och på-plats-meddelanden. Genom att dela signaler mellan produkterna kan du

* Minska antalet genomströmningar genom att länka kundernas exponering från DSP-kampanjer till deras webbplatsupplevelser.

* Upprätta A/B-tester genom att spegla webbplatsupplevelser med annonseringsmeddelanden med hjälp av Adobe Audience Manager exponeringsdata och klicka-för-feed [!DNL Target]-målgrupper.

* Mät effekten av enhetliga meddelanden på en mållyft på plats med enkla visualiseringar i Adobe Analytics för [!DNL Target].

I följande avsnitt finns information om krav och instruktioner för att ställa in klicknings- och genomskinlighetsspårning, implementera signaldelning mellan DSP och [!DNL Target] och ställa in en A/B-testaktivitet samt konfigurera [!DNL Analytics] Analysis Workspace för att visa testdata.

Kontakta adcloud_support@adobe.com om du har ytterligare frågor.

## Förutsättningar

Det här användningsexemplet kräver följande produkter och integreringar:

* [!DNL Target]

* [[!DNL Analytics] för Advertising](/help/integrations/analytics/overview.md)-integrering<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integrering av [[!DNL Analytics] för [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=sv-SE)

* Audience Manager (krävs endast för genomskinlighetstestning)

## Steg 1: Konfigurera Click-through Framework {#click-through-framework}

![Genomklickningsramverk](/help/integrations/assets/target-ct-framework.png)

När du lägger till DSP-makron i en klicknings-URL (den URL som visas när en användare klickar på en annons och når landningssidan), hämtar DSP automatiskt placeringsnyckeln genom att inkludera `${TM_PLACEMENT_ID}` i klicknings-URL:en. Det här makrot hämtar den alfanumeriska placeringsnyckeln och inte det numeriska placerings-ID:t.

![Genomklicknings-URL tillagd till landningssidans URL](/help/integrations/assets/target-ct-url.jpg)

### (Endast DSP) Lägg till DSP-makron i Klicka-genom-URL:er

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Uppdatera klicknings-URL:en för varje annons manuellt i [!DNL Flashtalking] eller Google Campaign Manager 360 för att inkludera de makron som krävs för att hämta AMO ID-variabler. AMO ID-variablerna används för att skicka klickdata till Adobe Analytics och för att dela placeringsnycklar för A/B-testning. Instruktioner finns på följande sidor:

* [Lägg till [!DNL Analytics for Advertising] makron i [!DNL Flashtalking] Lägg till taggar](/help/integrations/analytics/macros-flashtalking.md). **Obs!** Den här proceduren är inte nödvändig om din organisation har ett direkt samarbete med [!DNL Flashtalking] och du använder datappassmakron för att spåra parametrarna `s_kwcid` och `ef_id` enligt [!DNL Flashtalking] supportdokumentationen på [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) .

* [Lägg till  [!DNL Analytics for Advertising] makron i  [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md)

Kontakta Adobe Account Team och Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) om du vill hämta den placeringsnyckel som krävs och slutföra konfigurationen, och se till att varje klicknings-URL är ifylld med placeringsnyckeln.

## Steg 2: Konfigurera View-through Framework med Audience Manager {#view-through-framework}

![Genomskinligt ramverk](/help/integrations/assets/targetr-vt-framework.png)

Genom att lägga till en händelsepixel för Audience Manager-intryck i dina annonstaggar och placeringsinställningar kan du skapa ett testsegment för ytterligare möjligheter till genomskinliga tester.

1. Implementera en händelsepixel för Audience Manager-intrycket i era annonstaggar och DSP placeringsinställningar.

   Instruktioner finns i &quot;[Samla in medieexponeringsdata från Advertising DSP Campaigns](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Se till att du lägger till [DSP-makron](/help/dsp/campaign-management/macros.md) för att samla in alla data som du vill att visningshändelsepixeln ska skicka tillbaka, inklusive `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

   >[!NOTE]
   >
   >Klickspårnings-URL:er innehåller makrot `${TM_PLACEMENT_ID}` för den alfanumeriska placeringsnyckeln i stället för `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

1. Konfigurera ett Audience Manager-segment från DSP-visningsdata:

   1. Kontrollera att segmentdata är tillgängliga:

      1. [Sök efter signalen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html?lang=sv-SE) för [nyckel/värde-paret](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html?lang=sv-SE) som avgör på vilken nivå segmentanvändarna grupperas.

         Använd en [stödd ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=sv-SE)-nyckel med ett värde som motsvarar ett makro som du har lagt till i Audience Manager-inställningshändelsens pixel.

         Om du till exempel vill gruppera användare för en viss placering använder du tangenten `d_placement`. Använd ett numeriskt placerings-ID (till exempel 2501853) som hämtas av DSP-makrot `${TM_PLACEMENT_ID_NUM}` för värdet. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Om sökresultaten visar att användaren räknar nyckelvärdepar, vilket anger att pixeln placerades korrekt och att data flödar, fortsätter du till nästa steg.

   1. [Skapa en regelbaserad trait](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=sv-SE) för att skapa segment i Audience Manager.

      * Namnge egenskapen så att den är lätt att identifiera inom testaktiviteterna. Spara egenskaperna i den mapp du föredrar.

      * Välj `Ad Cloud` som **[!UICONTROL Data Source]**.

      * Använd `d_event` som **[!UICONTROL Key]** och `imp` som **[!UICONTROL Value]** för trait-uttrycket.

   1. [Konfigurera ett testsegment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html?lang=sv-SE) för den nya egenskapen i Audience Manager och välj `Ad Cloud` som **[!UICONTROL Data Source]**.

      Audience Manager delar automatiskt upp segmentet i en kontrollgrupp som får standardupplevelsen på landningssidan och en testgrupp som fått en personaliserad upplevelse på plats.

## Steg 3: Konfigurera en A/B-testaktivitet i [!DNL Target] för DSP

I följande anvisningar finns information om DSP användning.

1. [Logga in på Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=sv-SE).

1. [Skapa ett A/B-test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=sv-SE):

   1. I fältet **[!UICONTROL Enter Activity URL]** anger du landningssidans URL för testet.

      >[!NOTE]
      >
      >Du kan använda flera URL:er för att testa en genomskinlig webbplatspost. Mer information finns i [Flersidig aktivitet](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html?lang=sv-SE). Du kan enkelt identifiera de viktigaste posterna via sid-URL genom att skapa en [platspostrapport](https://experienceleague.adobe.com/sv/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) i Analytics (Analyser).

   1. Ange framgångsmåttet för testet i fältet **[!UICONTROL Goal]**.

      >[!NOTE]
      >
      >Kontrollera att [!DNL Analytics] är aktiverat som en datakälla i [!DNL Target] och att rätt rapportserie har valts.

   1. Ange **[!UICONTROL Priority]** till `High` eller `999` för att förhindra konflikter när användare i testsegmentet får en felaktig upplevelse på plats.

   1. I **[!UICONTROL Reporting Settings]** väljer du **[!UICONTROL Company Name]** och **[!UICONTROL Report Suite]** som är anslutna till ditt DSP-konto.

      Fler tips om rapportering finns i [Rapportera bästa praxis och felsökning](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=sv-SE).

   1. Ange lämpliga start- och slutdatum för testet i fältet **[!UICONTROL Date Range]**.

   1. Lägg till målgrupper i aktiviteten:

      1. Välj det [segment som du tidigare skapade i Audience Manager för att testa genomskinliga målgrupper](#view-through-framework).

      1. Välj **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** och ange DSP-placeringsnyckeln i fältet **[!UICONTROL Value]** för att använda Target-frågesträngsparametrarna för klickbara målgrupper.

   1. För **[!UICONTROL Traffic Allocation Method]** väljer du **[!UICONTROL Manual (Default)]** och delar målgruppen 50/50.

   1. Spara aktiviteten.

1. Använd [Visual Experience Composer som mål](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=sv-SE) om du vill göra designändringar i A/B-testsidmallen.

   * Upplevelse A: Redigera inte eftersom det är standardupplevelsen/styrningen av landningssidan utan personalisering.

   * Upplevelse B: Använd användargränssnittet [!DNL Target] för att anpassa landningssidmallen baserat på de resurser som ingår i testet (t.ex. rubriker, kopiering, knappplacering och kreatörer).

   >[!NOTE]
   >
   >Exempel på användningsfall för kreativa tester kan du kontakta Adobe Account Team.

## Steg 4: Konfigurera din [!DNL Analytics for Target] Analysis Workspace i [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) är en integrering med flera lösningar som gör att annonsörer kan skapa [!DNL Target]-aktiviteter baserat på konverteringsstatistik för [!DNL Analytics] och målgruppssegment och sedan mäta resultatet med [!DNL Analytics] som rapportkälla. All rapportering och segmentering för den aktiviteten baseras på datainsamling [!DNL Analytics].

Mer information om [!DNL Analytics for Target], inklusive en länk till implementeringsanvisningar, finns i [Adobe Analytics som rapportkälla för Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=sv-SE).

### Konfigurera panelen [!DNL Analytics for Target]

Konfigurera [!DNL Analytics for Target panel] i Analysis Workspace för att analysera dina [!DNL Target]-aktiviteter och -upplevelser. Tänk på följande viktiga pekare och information om dina rapporter.

#### Mått

* Skapa en panel på arbetsytan som är specifik för den Adobe Advertising-kampanj, det paket eller den placering som testet kördes för. Använd sammanfattningsvisualiseringar för att visa Adobe Advertising-mått i samma rapport som testprestandan [!DNL Target].

* Prioritera med hjälp av statistik på plats (t.ex. besök och konverteringar) för att mäta prestanda.

* Förstå att aggregerade mediemått från Adobe Advertising (som visningar, klick och kostnader) inte kan matchas mot [!DNL Target]-värden.

#### Dimensioner

Följande dimensioner gäller [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Namn på A/B-testet

* **[!UICONTROL Target Experiences]**: Namn på landningssidans upplevelser som används i aktiviteten

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: Aktivitetsnamnet och upplevelsenamnet på samma rad

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
* [A/B-testöversikt](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=sv-SE) - Beskriver A/B-testaktiviteter som du kan använda med DSP-annonser.
* [Erfarenheter och erbjudanden](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html?lang=sv-SE) - Beskriver [!DNL Target] verktyg för att fastställa vilket innehåll på webbplatsen som DSP testanvändare exponeras för.
* [Signaler, egenskaper och segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=sv-SE) - Definierar några av Audience Manager-verktygen som kan användas vid DSP-genomskinlighetstestning.
* [Översikt över Analytics för Advertising](/help/integrations/analytics/overview.md) - Här presenteras Analytics för Advertising, som gör att du kan spåra klicknings- och genomskinlighetsinteraktioner på din Analytics-instans.

>[!MORELIKETHIS]
>
>* [Konfigurera A/B-tester i Adobe Target för Advertising Search, Social och Commerce Ads](ab-tests-search.md)
