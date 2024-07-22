---
title: Generera en [!DNL Advertising Insight]
description: Lär dig hur du skapar en  [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Generera en [!DNL Advertising Insight]

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]** på huvudmenyn.

2. Klicka på insikten som du vill generera.

3. Ange inställningar för insikter:

   1. (Vissa rapporter, valfritt) Ange datumintervall för insikten.

   2. (De flesta insikter) Välj den portfölj som ska analyseras.

      I allmänhet är alla optimerade och aktiva portfolior som innehåller aktiva kampanjer tillgängliga. För vissa insikter kan du filtrera portföljlistan så att den innehåller **[!UICONTROL Only Optimized Portfolios]**.

      För [!UICONTROL Day of Week] insikter är bara portföljer som har tillräckligt med pengar och som också har använts för att rikta in sig de senaste två dagarna tillgängliga.

   3. ([!UICONTROL Event Path Beta] endast insight) Gör följande:

      1. Välj **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (om du vill överföra en [!UICONTROL Channel Assist Report] eller [!UICONTROL Campaign Assist Report] och klassificera användarhändelserna i distinkta grupper för analys) eller *[!UICONTROL Analyze classified events]* (om du vill överföra händelsegrupper och använda dem för att generera insikten).

      1. Klicka på **[!UICONTROL Select]** för att hitta en fil i formatet XLSX och ZIP (komprimerad XLSX) och klicka sedan på **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] endast insight) Gör följande:

      1. Ange **[!UICONTROL Advertiser Name]** och **[!UICONTROL Account Name]**.

      1. Markera **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* eller *[!UICONTROL United Kingdom]*) och **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* eller *[!UICONTROL German]*).

      1. Klicka på **[!UICONTROL Select]** för att hitta kampanj-, nyckelord- och ändringshistorikrapporter som hämtats för kontot från webbanvändargränssnittet i [!DNL Google Ads] och en kalkylbladsfil som hämtats för kontot från programmet [!DNL Google Ads Editor]. Klicka sedan på **[!UICONTROL Upload]**.

         Alla filer måste vara i CSV-, TSV-, TXT- eller ZIP-format (komprimerad CSV-, TSV- eller TXT-format).

   5. ([!UICONTROL Location Target Performance] insight only; optional) Om du vill samla in data dagligen i stället för som en sammanfattning väljer du **[!UICONTROL Time Aggregation]** av *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] endast insight) Gör följande:

      1. I fältet **[!UICONTROL Step]** anger du antalet målutgiftsnivåer, eller steg, som ska inkluderas i insikten. Värdet kan vara mellan tre (3) och 100.

      1. Välj simuleringstyp i fältet **[!UICONTROL Type]**:

         * *[!UICONTROL Optimized Multi-portfolio]*: Genererar en simulering över flera portföljer med samma mål och valuta.

         * *[!UICONTROL Individual Normalized]*: Genererar en individuell simulering för varje vald portfölj. Portföljerna kan ha olika mål och valutor.

   7. ([!UICONTROL Portfolio Launch] insight only; optional) Om du vill ange ett startdatum i framtiden anger du ett datum i fältet **[!UICONTROL Optional Date]**.

   8. ([!UICONTROL Quality Score] insight only) Välj det tillämpliga annonsnätverket.

   9. ([!UICONTROL Query Cross Matching] insight only) Välj kontot på menyn **[!UICONTROL Google Accounts]**.

4. Klicka på **[!UICONTROL Generate Insight]**.

   Du får ett meddelande när jobbet har slutförts eller misslyckats baserat på dina [konfigurerade meddelandeinställningar](/help/search-social-commerce/notifications/notification-edit.md) för [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Advertising Insights]](insight-about.md)
>* [Visa eller spara en [!DNL Advertising Insight]](insight-view-save.md)
>* [Ta bort en [!DNL Advertising Insight]](insight-delete.md)
