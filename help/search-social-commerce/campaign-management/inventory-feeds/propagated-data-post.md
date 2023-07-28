---
title: Posta kampanjdata som genererats från feeds till annonsnätverk
description: Lär dig hur du bokför data som genererats från lagerdataflöden till annonsnätverk.
exl-id: 14ce377c-9b71-48ac-8ead-cada9c06d52f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Posta kampanjdata som genererats från feeds till annonsnätverk

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

Du kan publicera kampanjdata som genereras från en feed när du sprider data via de associerade mallarna eller som en separat process. När du skickar data tas alla befintliga spridda data bort från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] listor.

För en framgångsrik bokföring måste alla annonsgrupper tilldelas till kampanjer, alla nyckelord och annonser måste tilldelas annonsgrupper och all nödvändig information måste inkluderas utan några längdöverträdelser.

* Om du använde alternativet för att &quot;[!UICONTROL Propagate and Preview], sedan [publicera den genererade kalkylbladsfilen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (med namnet &quot;`<feed file name>_<template name>`&quot;) från [!UICONTROL Bulksheets] vy.

  Om du inte gjorde det tidigare [validera dina landningssidor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)kan du göra det innan du skickar filen.

* Om du använde alternativet för att &quot;[!UICONTROL Propagate only]kan du publicera genererade data för komponenter med [[!UICONTROL New] status](propagated-data-status.md) i en kampanjhierarkivy från [!UICONTROL Templates] -fliken.

  >[!NOTE]
  >
  >Aktiva eller borttagna komponenter kan innehålla underkomponenter som är nya och underkomponenterna kan bokföras om data är giltiga.

  >[!TIP]
  >
  >Om du inte validerade dina landningssidor tidigare och vill göra det, [sprida data och förhandsgranska dem](feed-data-propagate.md) från [!UICONTROL Bulksheets] i stället för att lägga upp det i annonsnätverket. Då kan du [validera URL:erna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) innan filen publiceras i annonsnätverket manuellt.

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

   1. Markera kryssrutan bredvid mallen.

   1. Klicka på i verktygsfältet **[!UICONTROL Post]**.

   1. Ange eller välj information i fälten i bokföringsinställningarna och klicka sedan på **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Vilka kontokomponenter bokförs.

      * **[!UICONTROL Scheduling]:** När filen ska skickas:

         * *[!UICONTROL Post to search engine now]* (standard): Skapar en bulkbladsfil av de spridda flödesuppgifterna och börjar publicera dem direkt.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Skapar en kalkylbladsfil och skickar den senare. Ange följande:

            * **[!UICONTROL Start Time]:** Ett framtida datum och en tidpunkt då kalkylbladsfilen ska bokföras i annonsnätverket. Som standard skickas filen kl. 00.00 (kl. 12.00) nästa dag. **Obs!** För stora filer som kräver längre bearbetning är de publicerade uppgifterna inte tillgängliga direkt i kampanjhanteringsvyerna eller inom nätverkets annonshanterare.

            * **[!UICONTROL End Time]:** Ett framtida datum och en framtida tidpunkt då de bokförda annonserna kan pausas eller tas bort baserat på [inställning för feed-data](feed-settings-manage.md#feed-data-settings) for &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Som standard är sluttiden 00:00 (12:00) 30 dagar från idag. Välj **[!UICONTROL None]** om du vill att data ska förbli aktiva i oändlighet (eller tills du sprider nya data för mallen) eller ange ett datum och en tid.

              Om du vill ange ett datum använder du formatet DD/MM/ÅÅÅÅ eller D/M/ÅÅÅÅ eller klickar [Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") för att öppna kalendern och [välj ett datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Om du vill ändra en tid anger du tiden i 24-timmarsformat, HH/MM eller H/M, eller väljer en tid (i 30-minutersintervall) i listan.

         * *[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Skapar en bulkbladsfil som är tillgänglig från [!UICONTROL Search] > [!UICONTROL Bulksheets] vy. Du kan också publicera filen därifrån.

           När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

      * **[!UICONTROL Generate Tracking URLs]:** Om spårnings-URL:er för nyckelord och annonsvariationer ska inkluderas i kalkylbladsfilen: *[!UICONTROL Yes]* (standard) eller *[!UICONTROL No]*.

        Om du väljer *[!UICONTROL Yes]*, genereras URL:erna från bas-URL:erna för nyckelorden och annonserna enligt [!UICONTROL Tracking Methods] parametrarna i [kontoinställningar](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) eller, om ni mappar data till befintliga kampanjer, till [!UICONTROL Tracking Methods] parametrar i den befintliga [kampanjinställningar](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Om det finns spårnings-URL:er för de relevanta objekten, genereras de inte om de inte behövs (till exempel om nyckelordens matchningstyp, den kreativa texten eller kontots spårningsparametrar har ändrats).

      * **[!UICONTROL Bulksheet Name]:** Namnet på den kalkylbladsfil som ska skapas från de spridda flödesuppgifterna. Som standard får filen ett namn `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Du kan ändra namn på filen som du vill, men det måste sluta med något av följande filtillägg: `.tsv` (för tabbseparerade värden), `.txt` (för ASCII-text), `.csv` (för kommaavgränsade värden), eller `.zip` (för en komprimerad TSV-fil). Använd formatet TSV eller TXT för data som innehåller internationella tecken.

        Den publicerade filen är tillgänglig i [!UICONTROL Bulksheets] i 30 dagar, oavsett om du har lagt ut det i annonsnätverket eller inte.

The &quot;[!UICONTROL Last Prop. Status]&quot;kolumn visar jobbstatus för tillämpliga mallar.

När kalkylbladet skapas visas det i [!UICONTROL Bulksheets] vy. När filen har skickats skickas ett e-postmeddelande med en länk till filen. Om alla eller vissa data inte kan registreras visas en felfil i [!UICONTROL Bulksheets] och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>* Oavsett vilket schemaläggningsalternativ du har valt tas de angivna data bort från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] listor.
>* Stora mängder data tar längre tid att behandla. Du kan följa förloppet för filen under processen.
>* Alla bokförda data är underställda nätverkets redaktionella process.
>* Innan en kalkylbladsfil har bokförts kan du [avbryt bokföringen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Om lagerflöden](inventory-feeds-about.md)
>* [Visa data som genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
