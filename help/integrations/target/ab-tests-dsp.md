---
title: Konfigurera A/B-tester för Adobe Advertising DSP annonser i Adobe Target
description: Lär dig hur du ställer in ett A/B-test i [!DNL Target] för era DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7ffa5d3e9f1aae0f9d66d87c74807e491e818daa
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Konfigurera A/B-tester i Adobe Target för annonsering DSP annonser

*Annonsörer med endast DSP*

Adobe Advertising och Adobe Target gör det ännu enklare för marknadsförare att leverera en personaliserad och uppkopplad upplevelse i betalda medier och på-plats-meddelanden. Genom att dela signaler mellan produkterna kan du

* Minska antalet fall på webbplatsen genom att länka kundernas exponering från DSP till deras upplevelser på plats.

* Upprätta A/B-tester genom att spegla webbplatsupplevelser med annonsmeddelanden med hjälp av Adobe Audience Manager exponeringsdata och click-to-feed [!DNL Target] målgrupper.

* Mät effekten av enhetliga meddelanden på ett visst mål med enkla visualiseringar i Adobe Analytics för [!DNL Target].

I följande avsnitt finns information om krav och instruktioner för att ställa in klicknings- och genomskinlighetsspårning, implementera signaldelning mellan DSP och [!DNL Target] och konfigurera en A/B-testaktivitet och konfigurera [!DNL Analytics] Analysis Workspace för att visa testdata.

Kontakta adcloud_support@adobe.com om du har ytterligare frågor.

## Förutsättningar

Det här användningsexemplet kräver följande produkter och integreringar:

* [!DNL Target]

* [[!DNL Analytics] för annonsering](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (krävs endast för genomsiktstestning)

## Steg 1: Konfigurera Click-through Framework {#click-through-framework}

![Genomklickningsramverk](/help/integrations/assets/target-ct-framework.png)

När du lägger till DSP makron i en klicknings-URL (den URL som visas när en användare klickar på en annons och når landningssidan), DSP automatiskt placeringsnyckeln genom att inkludera `${TM_PLACEMENT_ID}` i klickbara URL:er. Det här makrot hämtar den alfanumeriska placeringsnyckeln och inte det numeriska placerings-ID:t.

![Genomklicknings-URL tillagd till landningssidans URL](/help/integrations/assets/target-ct-url.jpg)

### (Endast DSP) Lägg till DSP makron till klicknings-URL:er

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Uppdatera klicknings-URL:en för varje annons manuellt i Google Campaign Manager 360, så att den innehåller de makron som krävs för att hämta AMO ID-variabler. AMO ID-variablerna används för att skicka klickdata till Adobe Analytics och för att dela placeringsnycklar för A/B-testning. Instruktioner finns på följande sidor:

* [Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar](/help/integrations/analytics/macros-flashtalking.md)

* [Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md)

Kontakta kontoteamet på Adobe och Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) för att hämta den placeringsnyckel som krävs och slutföra konfigurationen, och för att se till att varje klicknings-URL är ifylld med placeringsnyckeln.

## Steg 2: Konfigurera visningsramverket med Audience Manager {#view-through-framework}

![Genomskinligt ramverk](/help/integrations/assets/targetr-vt-framework.png)

Genom att lägga till en händelsepixel för Audience Manager-intrycket i dina annonstaggar och placeringsinställningar kan du skapa ett testsegment för ytterligare visningsmöjligheter.

1. Implementera en händelsepixel för Audience Manager-intryckning i dina annonstaggar och inställningar för DSP.

   Instruktioner finns i &quot;[Samla in data om medieexponering från annonskampanjer DSP kampanjer](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Se till att du lägger till [DSP makron](/help/dsp/campaign-management/macros.md) för att samla in alla data som du vill att bilden ska skickas tillbaka, inklusive `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

   >[!NOTE]
   >
   >Klickspårnings-URL:er innehåller `${TM_PLACEMENT_ID}` makro för den alfanumeriska placeringsnyckeln i stället för `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

1. Konfigurera ett Audience Manager-segment utifrån DSP:

   1. Kontrollera att segmentdata är tillgängliga:

      1. [Sök efter signalen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) för [nyckelvärdepar](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) som avgör på vilken nivå segmentanvändarna grupperas.

         Använd en [nyckel som stöds](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) med ett värde som motsvarar ett makro som du har lagt till i Audience Manager-visningshändelsepixeln.

         Om du till exempel vill gruppera användare för en viss placering använder du `d_placement` -tangenten. För värdet använder du ett numeriskt placerings-ID (till exempel 2501853) som fångas av det DSP makrot `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Om sökresultaten visar att användaren räknar nyckelvärdepar, vilket anger att pixeln placerades korrekt och att data flödar, fortsätter du till nästa steg.

   1. [Skapa ett regelbaserat varumärke](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) för att skapa segment i Audience Manager.

      * Namnge egenskapen så att den är lätt att identifiera inom testaktiviteterna. Spara egenskaperna i den mapp du föredrar.

      * Välj `Ad Cloud` som **[!UICONTROL Data Source]**.

      * Använd för trait-uttrycket `d_event` som **[!UICONTROL Key]** och `imp` som **[!UICONTROL Value]**.

   1. [Konfigurera ett testsegment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) för det nya traktet i Audience Manager, välja `Ad Cloud` som **[!UICONTROL Data Source]**.

      Audience Manager delar automatiskt upp segmentet i en kontrollgrupp som tar emot standardupplevelsen på landningssidan och en testgrupp som fått en personaliserad upplevelse på plats.

## Steg 3: Konfigurera en A/B-testaktivitet i [!DNL Target] för DSP

I följande anvisningar markeras information om DSP.

1. [Logga in på Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Skapa ett A/B-test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. I **[!UICONTROL Enter Activity URL]** anger du landningssidans URL för testet.

      >[!NOTE]
      >
      >Du kan använda flera URL:er för att testa en genomskinlig webbplatspost. Mer information finns i &quot;[Flersidig aktivitet](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Du kan enkelt identifiera de översta posterna per sid-URL genom att skapa en [Platsens anmälningsrapport](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) i Analytics.

   1. I **[!UICONTROL Goal]** anger du framgångsmåttet för testet.

      >[!NOTE]
      >
      >Se till att [!DNL Analytics] aktiveras som en datakälla i [!DNL Target]och att rätt rapportsvit har valts.

   1. Ange **[!UICONTROL Priority]** till `High` eller `999` för att förhindra konflikter när användare i testsegmentet får en felaktig upplevelse på plats.

   1. Inom **[!UICONTROL Reporting Settings]** väljer du **[!UICONTROL Company Name]** och **[!UICONTROL Report Suite]** som är ansluten till ditt DSP.

      Ytterligare rapportips finns i &quot;[Rapportera bästa praxis och felsökning](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. I **[!UICONTROL Date Range]** anger du lämpliga start- och slutdatum för testet.

   1. Lägg till målgrupper i aktiviteten:

      1. Välj [segment som du tidigare skapat i Audience Manager för att testa genomsiktliga målgrupper](#view-through-framework).

      1. Välj **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** och ange DSP placeringsnyckel i dialogrutan **[!UICONTROL Value]** om du vill använda Target-frågesträngsparametrarna för klickbara målgrupper.

   1. För **[!UICONTROL Traffic Allocation Method]**, markera **[!UICONTROL Manual (Default)]** och dela publiken 50/50.

   1. Spara aktiviteten.

1. Använd [Aktivera Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) för att göra konstruktionsändringar i A/B-testsidans mall för landningssidor.

   * Upplevelse A: Redigera inte eftersom det är standardupplevelsen/styrningen av landningssidan utan personalisering.

   * Upplevelse B: Använd [!DNL Target] användargränssnitt för att anpassa landningssidans mall baserat på de tillgångar som ingår i testet (t.ex. rubriker, text, knappplacering och kreatörer).

   >[!NOTE]
   >
   >Exempel på användningsfall för kreativa tester kan du kontakta ditt Adobe-kontoteam.

## Steg 4: Konfigurera [!DNL Analytics for Target] ANALYSIS WORKSPACE i [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) är en integrerad lösning som gör att annonsörer kan skapa [!DNL Target] verksamhet som bygger på [!DNL Analytics] konverteringsstatistik och målgruppssegment och sedan mäta resultatet med [!DNL Analytics] som rapportkälla. All rapportering och segmentering för den aktiviteten baseras på [!DNL Analytics] datainsamling.

Mer information om [!DNL Analytics for Target], med en länk till implementeringsanvisningar, se&quot;[Adobe Analytics som rapportkälla för Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Konfigurera [!DNL Analytics for Target] Panel

I Analysis Workspace konfigurerar du [!DNL Analytics for Target panel] för att analysera [!DNL Target] aktiviteter och upplevelser. Tänk på följande viktiga pekare och information om dina rapporter.

#### Mått

* Skapa en panel på arbetsytan som är specifik för den kampanj, det paket eller den placering som testet kördes för. Använd sammanfattningsvisualiseringar för att visa Adobe Advertising-statistik i samma rapport som [!DNL Target] testprestanda.

* Prioritera med hjälp av statistik på plats (t.ex. besök och konverteringar) för att mäta prestanda.

* Förstå att aggregerade mediemått från Adobe Advertising (som visningar, klick och kostnader) inte kan matchas mot [!DNL Target] mätvärden.

#### Dimensioner

Följande dimensioner gäller för [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Namn på A/B-testet

* **[!UICONTROL Target Experiences]**: Namn på landningssidans upplevelser som används inom aktiviteten

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: Aktivitetsnamnet och upplevelsenamnet på samma rad

### Felsökningsanalys för [!DNL Target] Data

Om du inom Analysis Workspace märker att data om aktivitet och upplevelser är minimala eller inte är ifyllda gör du så här:

* Verifiera att samma [!UICONTROL Supplemental Data ID] (SDID) används för båda [!DNL Target] och [!DNL Analytics]. Du kan verifiera SDID-värdena med [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) på landningssidan som kampanjen driver användarna till.

[SDID-värden (Additional Data ID) i Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* På samma landningssida kontrollerar du att a) [!UICONTROL Hostname] som visas i Adobe Debugger under [!UICONTROL Solutions] > [!UICONTROL Target] matchar b) [!UICONTROL Tracking Server] visas i [!DNL Target] för aktiviteten (under [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] kräver [!DNL Analytics] spårningsserver som ska skickas i samtal från [!DNL Target] till [!DNL Modstats] datainsamlingsserver för Analytics.<!-- just "to Analytics?"-->

[Värdnamnsvärde i Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Spårningsservervärde i mål](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Ytterligare läsning

* [Integrera Target med Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Beskriver hur du konfigurerar [!DNL Target] i Analysis Workspace.
* [A/B-testöversikt](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beskriver A/B-testaktiviteter, som du kan använda med DSP annonser.
* [Erfarenheter och erbjudanden](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Förklaringar [!DNL Target] verktyg för att avgöra vilket innehåll på plats som DSP testanvändare exponeras för.
* [Signaler, egenskaper och segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definierar några av Audience Manager-verktygen som kan användas för DSP-genomskinlighetstestning.
* [Översikt över Analytics for Advertising](/help/integrations/analytics/overview.md) - introducerar Analytics for Advertising, som gör att ni kan spåra klicknings- och genomskinlighetsinteraktioner på webbplatsen i era Analytics-instanser.

>[!MORELIKETHIS]
>
>* [Konfigurera A/B-tester i Adobe Target för annonseringsannonser för sökning, sociala medier och handel](ab-tests-search.md)
