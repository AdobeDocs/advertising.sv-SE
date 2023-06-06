---
title: Filtrera data efter datumintervall
description: Lär dig hur du använder det globala datumintervallfiltret.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Filtrera data efter datumintervall

Samma globala datumintervallfilter tillämpas på de flesta av era kampanjdatavyer, för alla era annonsörer, förutom för standardvyer och anpassade vyer för vilka ni har sparat specifika datumintervall. Systemets standarddatumintervall för kampanjhanteringsvyer är&quot;I går&quot;.

Inställningarna för datumintervall sparas i en webbläsarspecifik cookie, så alla ändringar i datumintervallfiltret används för alla dina annonsörer varje gång du loggar in med samma webbläsarprogram tills du ändrar filtret eller tar bort cookien. Varje webbläsarprogram som du använder lagrar filterinställningar för datumintervall i en egen cookie.

När du sparar ett visst datumintervall för en standardvy eller anpassad vy används det intervallet när du använder vyn, oavsett vilket webbläsarprogram du använder.

>[!NOTE]
>
>* Du kan visa data för de senaste 13 månaderna, men befintliga anpassade vyer kan endast innehålla data för upp till de föregående 180 dagarna.
>* Om du vill visa tidigare data går du till [[!UICONTROL Reports] visa](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) och kör en grundläggande rapport.
>* Du kan också spara ett datumintervall för en [standardvy eller anpassad vy](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).


## Ändra det globala datumfiltret i kampanjvyer

1. Klicka på det aktuella datumintervallet ovanför en datatabell i Sök \> kampanjer \> Kampanjer.

1. I **[!UICONTROL Date Range]** anger du intervallet:

   * För ett förinställt intervall: Välj i listan över vanliga tidssteg, från *[!UICONTROL Today]* till *[!UICONTROL Last 180 Days]*. Standardvärdet är *[!UICONTROL Yesterday]*.

   * För ett visst intervall: Välj **[!UICONTROL Custom Date Range]** och ange sedan startdatum och slutdatum.

      Ange datum i formatet MM/DD/ÅÅÅÅ eller MM-DD-ÅÅÅÅ, eller klicka ![Kalenderikon](/help/search-social-commerce/assets/calendar.png "Kalenderikon") intill varje fält för att öppna kalendern och välja ett datum.

1. (Valfritt) Jämför data för det angivna datumintervallet med data för ett andra datumintervall:

   1. Flytta **[!UICONTROL Comparison]** skjutreglage till *[!UICONTROL On]*.

      När du väljer det här alternativet läggs ytterligare två kolumner till för varje vanlig datakolumn. I stället för att bara ta med en kolumn för &quot;[!UICONTROL Impressions],&quot; innehåller tabellen kolumner för &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot; och &quot;[!UICONTROL Impressions Diff].&quot;  Om du exporterar data skrivs samma kolumner ut som &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; och &quot;[!UICONTROL Impressions Difference].&quot;

   1. Ange det andra datumintervallet.

   1. Välj hur du vill uttrycka skillnaden mellan data i de två valda datumintervallen i &quot;\[_Datafält_\] Differens&quot; kolumn:

      * *[!UICONTROL Variance]* (standard): Visar skillnaden som ett numeriskt värde.

      * *[!UICONTROL % Change]:*  Visar skillnaden i procent.

1. Klicka på **[!UICONTROL Apply]**.
