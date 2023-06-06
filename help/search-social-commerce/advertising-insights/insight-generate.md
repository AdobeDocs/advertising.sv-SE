---
title: Generera en [!DNL Advertising Insight]
description: Lär dig hur du skapar en [!DNL Advertising Insight].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Generera en [!DNL Advertising Insight]

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Klicka på insikten som du vill generera.

3. Ange inställningar för insikter:

   1. (Vissa rapporter; (valfritt) Ange datumintervall för insikten.

   2. (De flesta insikter) Välj den portfölj som ska analyseras.

      I allmänhet är alla optimerade och aktiva portfolior som innehåller aktiva kampanjer tillgängliga. För vissa insikter kan du filtrera portföljlistan så att den innehåller **[!UICONTROL Only Optimized Portfolios]**.

      För [!UICONTROL Day of Week] Det finns bara tillgängliga insikter, bara portfolior som har tillräckligt med pengar och som också spenderats för att nå ut de senaste två dagarna.

   3. ([!UICONTROL Event Path Beta] endast insight) Gör följande:

      1. Välj **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (för att ladda upp en [!UICONTROL Channel Assist Report] eller [!UICONTROL Campaign Assist Report] och klassificera användarhändelser i distinkta grupper för analys) eller *[!UICONTROL Analyze classified events]* (för att överföra händelsegrupper och använda dem för att generera insikterna).

      1. Klicka **[!UICONTROL Select]** för att hitta en fil i formatet XLSX och ZIP (komprimerad XLSX) och sedan klicka på **[!UICONTROL Upload]**.
   4. ([!UICONTROL Google Account Audit] endast insight) Gör följande:

      1. Ange **[!UICONTROL Advertiser Name]** och **[!UICONTROL Account Name]**.

      1. Välj **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* eller *[!UICONTROL United Kingdom]*) och **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]*, eller *[!UICONTROL German]*).

      1. Klicka **[!UICONTROL Select]** för att hitta kampanjrapporter, nyckelord och ändringshistorik som hämtats för kontot från [!DNL Google Ads] webbanvändargränssnitt och en kalkylbladsfil som laddats ned för kontot från [!DNL Google Ads Editor] program. Klicka sedan på **[!UICONTROL Upload]**.

         Alla filer måste vara i CSV-, TSV-, TXT- eller ZIP-format (komprimerad CSV-, TSV- eller TXT-format).
   5. ([!UICONTROL Location Target Performance] endast insikter, (valfritt) Om du vill samla in data dagligen istället för som en sammanfattning väljer du **[!UICONTROL Time Aggregation]** av *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] endast insight) Gör följande:

      1. I **[!UICONTROL Step]** anger du antalet målutgiftsnivåer, eller steg, som ska inkluderas i insikten. Värdet kan vara mellan tre (3) och 100.

      1. I **[!UICONTROL Type]** väljer du simuleringstyp:

         * *[!UICONTROL Optimized Multi-portfolio]*: Genererar en simulering över flera portföljer med samma mål och valuta.

         * *[!UICONTROL Individual Normalized]*: Genererar en individuell simulering för varje vald portfölj. Portföljerna kan ha olika mål och valutor.
   7. ([!UICONTROL Portfolio Launch] endast insikter, (valfritt) Om du vill ange ett startdatum i framtiden anger du ett datum i **[!UICONTROL Optional Date]** fält.

   8. ([!UICONTROL Quality Score] endast insight) Välj lämpligt annonsnätverk.

   9. ([!UICONTROL Query Cross Matching] (endast insight) I **[!UICONTROL Google Accounts]** väljer du kontot.




4. Klicka på **[!UICONTROL Generate Insight]**.

   Du får ett meddelande när jobbet har slutförts eller misslyckats baserat på din [konfigurerade meddelandeinställningar](/help/search-social-commerce/notifications/notification-edit.md) for [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Advertising Insights]](insight-about.md)
>* [Visa eller spara en [!DNL Advertising Insight]](insight-view-save.md)
>* [Ta bort en [!DNL Advertising Insight]](insight-delete.md)

