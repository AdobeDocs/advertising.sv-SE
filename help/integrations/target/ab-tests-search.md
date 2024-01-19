---
title: Konfigurera A/B-tester för Adobe Advertising Search, Social och Commerce Ads i Adobe Target
description: Lär dig hur du ställer in ett A/B-test i [!DNL Target] för [!DNL Google Ads] och [!DNL Microsoft® Advertising] annonser i sökningar, sociala medier och handel.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Konfigurera A/B-tester i Adobe Target för annonseringsannonser för sökning, sociala medier och handel

*Annonsörer med endast annonssökning, sociala medier och handel*

*[!DNL Google Ads]och [!DNL Microsoft® Advertising] endast konton*

Adobe Advertising och Adobe Target gör det enkelt att skapa A/B-tester för landningssidor för digital reklamtrafik [!DNL Google Ads] och [!DNL Microsoft® Advertising] till:

* Förbättra konverteringsgraden (CVR) och effektivitetsåtgärderna för förvärv (såsom CPA, CPL och CAC).

* Leverera en mer personaliserad landningssida som är relevant för annonsen (t.ex. matchning av bild-/videoredigeringssignal, kopia, nyckelord eller annan annonssignal till landningssidan).

Du kan också kombinera det inbyggda [[!DNL Analytics] för annonsering](/help/integrations/analytics/overview.md) och [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integreringsrapporteringsdimensioner som är integrerade i Adobe Analytics för att mäta och visualisera testdata med [!DNL Analytics] mätvärden och framgångshändelser.

I följande avsnitt finns information om krav, anvisningar för hur du ställer in A/B-tester i [!DNL Target] för klickbar trafik från annonser i sökmotorkampanjer, sociala kampanjer och e-handel, samt tips om hur du mäter och visualiserar dina tester i [!DNL Analytics].

## Förutsättningar

### Nödvändiga produkter

* Sökning, sociala medier och handel
* [!DNL Target]

### Rekommenderade produkter och integreringar

* [!DNL Analytics]

* [[!DNL Analytics] för annonsering](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

## Steg 1: Skapa en A/B-testaktivitet i [!DNL Target] för sökning, sociala medier och handel

I följande anvisningar finns information om användningen av sökningar, sociala medier och handel.

1. [Logga in på Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Skapa ett A/B-test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. I **[!UICONTROL Enter Activity URL]** anger du landningssidans URL för testet.

   1. I **[!UICONTROL Goal]** anger du framgångsmåttet för testet.

      >[!NOTE]
      >
      >Se till att [!DNL Analytics] aktiveras som en datakälla i [!DNL Target]och att rätt rapportsvit har valts.

   1. Ange **[!UICONTROL Priority]** till `High` eller `999` för att förhindra konflikter när användare i testsegmentet får en felaktig upplevelse på plats.


   1. Inom **[!UICONTROL Reporting Settings]** väljer du **[!UICONTROL Company Name]** och **[!UICONTROL Report Suite]** är kopplat till ditt konto för sökning, sociala medier och handel.

      Ytterligare rapportips finns i &quot;[Rapportera bästa praxis och felsökning](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. I **[!UICONTROL Date Range]** anger du lämpliga start- och slutdatum för testet.

   1. Välj **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. I **[!UICONTROL Value]** fält, ange [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], eller [!UICONTROL Network Ad ID] för den relevanta annonsnätverksenheten inom sökning, sociala medier och handel. På så sätt kan du använda [!DNL Target] frågesträngsparametrar för klickbara målgrupper för entiteten.

      Du kan hitta ditt ID med [lägga till relevant ID-kolumn i entitetsvyn](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] kolumn i [!UICONTROL Accounts] visa](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] kolumn i [!UICONTROL Accounts] visa")

      Samarbeta med kontoteamet på Adobe om du behöver hjälp.

   1. För **[!UICONTROL Traffic Allocation Method]**, markera **[!UICONTROL Manual (Default)]** och dela publiken 50/50.

   1. Spara aktiviteten.

1. Använd [Aktivera Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) för att göra konstruktionsändringar i A/B-testsidans mall för landningssidor.

   * Upplevelse A: Redigera inte eftersom det är standardupplevelsen/styrningen av landningssidan utan personalisering.

   * Upplevelse B: Använd [!DNL Target] användargränssnitt för att anpassa landningssidans mall baserat på de tillgångar som ingår i testet (t.ex. rubriker, text, knappplacering och kreatörer).

   >[!NOTE]
   >
   >Exempel på användningsfall för kreativa tester kan du kontakta ditt Adobe-kontoteam.

## Steg 2: Konfigurera [!DNL Analytics for Target] ANALYSIS WORKSPACE i [!DNL Analytics]

[!DNL Analytics for Target] (A4T) är en integrerad lösning som gör att annonsörer kan skapa [!DNL Target] verksamhet som bygger på [!DNL Analytics] konverteringsstatistik och målgruppssegment och sedan mäta resultatet med [!DNL Analytics] som rapportkälla. All rapportering och segmentering för den aktiviteten baseras på [!DNL Analytics] datainsamling.

Mer information om [!DNL Analytics for Target], med en länk till implementeringsanvisningar, se&quot;[Adobe Analytics som rapportkälla för Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Konfigurera [!DNL Analytics for Target] Panel

I Analysis Workspace konfigurerar du [!DNL Analytics for Target panel] för att analysera [!DNL Target] aktiviteter och upplevelser. Tänk på följande viktiga pekare och information om dina rapporter.

#### Mått

* Skapa en panel i arbetsytan som är specifik för Adobe Advertising, konto, kampanj eller annonsgrupp<!-- only applicable entities? --> som testet kördes för. Använd sammanfattningsvisualiseringar för att visa Adobe Advertising-statistik i samma rapport som [!DNL Target] testprestanda.

* Prioritera med hjälp av statistik på plats (t.ex. besök och konverteringar) för att mäta prestanda.

* Förstå att aggregerade mediemått från Adobe Advertising (som visningar, klick och kostnader) inte kan matchas mot [!DNL Target] mätvärden.

#### Dimensioner

Följande dimensioner gäller för [!DNL Analytics for Target]:

* **Verksamheter**: Namn på A/B-testet

* **Målgrupper**: Namn på landningssidans upplevelser som används inom aktiviteten

* **Verksamhetens syfte?** > **Upplevelse**: Aktivitetsnamnet och upplevelsenamnet på samma rad

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
* [A/B-testöversikt](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beskriver A/B-testaktiviteter, som du kan använda med sök-, sociala och Commerce-annonser.
* [Översikt över Analytics for Advertising](/help/integrations/analytics/overview.md) - introducerar Analytics for Advertising, som gör att ni kan spåra klicknings- och genomskinlighetsinteraktioner på webbplatsen i era Analytics-instanser.

>[!MORELIKETHIS]
>
>* [Konfigurera A/B-tester i Adobe Target för annonsering DSP annonser](ab-tests-dsp.md)
