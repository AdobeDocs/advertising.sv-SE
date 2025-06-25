---
title: Posta kampanjdata som genererats från feeds till annonsnätverk
description: Lär dig hur du bokför data som genererats från lagerdataflöden till annonsnätverk.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Posta kampanjdata som genererats från feeds till annonsnätverk

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Du kan publicera kampanjdata som genereras från en feed när du sprider data via de associerade mallarna eller som en separat process. När du skickar data tas alla befintliga spridda data bort från listorna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

För en framgångsrik bokföring måste alla annonsgrupper tilldelas till kampanjer, alla nyckelord och annonser måste tilldelas annonsgrupper och all nödvändig information måste inkluderas utan några längdöverträdelser.

* Om du använde alternativet för [!UICONTROL Propagate and Preview] skickar du [den genererade kalkylbladsfilen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (med namnet `<feed file name>_<template name>`) från vyn [!UICONTROL Bulksheets].

  Om du inte [validerade dina landningssidor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) tidigare kan du göra det innan du publicerar filen.

* Om du använde alternativet för [!UICONTROL Propagate only] kan du publicera genererade data för komponenter med [[!UICONTROL New] status ](propagated-data-status.md) i en kampanjhierarkivy på fliken [!UICONTROL Templates].

  >[!NOTE]
  >
  >Aktiva eller borttagna komponenter kan innehålla underkomponenter som är nya och underkomponenterna kan bokföras om data är giltiga.

  >[!TIP]
  >
  >Om du inte validerade dina landningssidor tidigare och vill göra det [sprider du data och förhandsgranskar dem](feed-data-propagate.md) från [!UICONTROL Bulksheets]-vyn i stället för att publicera dem i annonsnätverket. Du kan sedan [validera URL:erna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) innan du manuellt skickar filen till annonsnätverket.

   1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

   1. Markera kryssrutan bredvid mallen.

   1. Klicka på **[!UICONTROL Post]** i verktygsfältet.

   1. Ange eller välj information i fälten i bokföringsinställningarna och klicka sedan på **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Vilka kontokomponenter bokförs.

      * **[!UICONTROL Scheduling]:** När filen ska skickas:

         * *[!UICONTROL Post to search engine now]* (standard): Skapar en bulkbladsfil från de spridda flödesuppgifterna och börjar publicera den omedelbart.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Skapar en kalkylbladsfil och skickar den senare. Ange följande:

            * **[!UICONTROL Start Time]:** Ett framtida datum och en framtida tidpunkt då kalkylbladsfilen ska bokföras i annonsnätverket. Som standard skickas filen kl. 00.00 (kl. 12.00) nästa dag. **Obs!** För stora filer som kräver längre bearbetning är de publicerade data inte tillgängliga direkt i kampanjhanteringsvyerna eller i nätverkets annonshanterare.

            * **[!UICONTROL End Time]:** Ett framtida datum och en framtida tidpunkt då de bokförda annonserna kan pausas eller tas bort baserat på [feed-datainställningen](feed-settings-manage.md#feed-data-settings) för [!UICONTROL When the Scheduled End Date is reached]. Som standard är sluttiden 00:00 (12:00) 30 dagar från idag. Välj **[!UICONTROL None]** om du vill att data ska förbli aktiva i oändlighet (eller tills du sprider nya data för mallen), eller ange ett datum och en tid.

              Om du vill ange ett datum använder du formatet DD/MM/ÅÅÅÅ eller D/M/ÅÅÅÅ eller klickar på ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") för att öppna kalendern och [väljer ett datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Om du vill ändra en tid anger du tiden i 24-timmarsformat, HH/MM eller H/M, eller väljer en tid (i 30-minutersintervall) i listan.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Skapar en bulkbladsfil som är tillgänglig från vyn [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]. Du kan också publicera filen därifrån.

           När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

      * **[!UICONTROL Generate Tracking URLs]:** Om spårnings-URL:er för nyckelord och annonsvariationer ska inkluderas i kalkylbladsfilen: *[!UICONTROL Yes]* (standard) eller *[!UICONTROL No]*.

        Om du väljer *[!UICONTROL Yes]* genereras URL:erna från bas-URL:erna för nyckelorden och annonserna enligt [!UICONTROL Tracking Methods] -parametrarna i [kontoinställningarna](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) eller, om du mappar data till befintliga kampanjer, till [!UICONTROL Tracking Methods]-parametrarna i de befintliga [kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Om det finns spårnings-URL:er för de relevanta objekten, genereras de inte om de inte behövs (till exempel om nyckelordens matchningstyp, den kreativa texten eller kontots spårningsparametrar har ändrats).

      * **[!UICONTROL Bulksheet Name]:** Namnet på den kalkylbladsfil som ska skapas från de spridda flödesuppgifterna. Som standard har filen namnet `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Du kan ändra namn på filen som du vill, men det måste sluta med något av följande filtillägg: `.tsv` (för tabbavgränsade värden), `.txt` (för ASCII-text), `.csv` (för kommaseparerade värden) eller `.zip` (för en komprimerad TSV-fil). Använd formatet TSV eller TXT för data som innehåller internationella tecken.

        Den publicerade filen är tillgänglig i vyn [!UICONTROL Bulksheets] i 30 dagar, oavsett om du bokför den i annonsnätverket eller inte.

Kolumnen [!UICONTROL Last Prop. Status] visar jobbstatus för tillämpliga mallar.

När kalkylbladet skapas visas det i vyn [!UICONTROL Bulksheets]. När filen har skickats skickas ett e-postmeddelande med en länk till filen. Om det inte går att publicera alla eller vissa data visas en felfil i [!UICONTROL Bulksheets]-vyn och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>* Oavsett vilket schemaläggningsalternativ du valde tas de angivna data bort från listorna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].
>* Stora mängder data tar längre tid att behandla. Du kan följa förloppet för filen under processen.
>* Alla bokförda data är underställda nätverkets redaktionella process.
>* Innan en kalkylbladsfil bokförs kan du [avbryta bokföringen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](inventory-feeds-about.md)
>* [Visa data som har genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
