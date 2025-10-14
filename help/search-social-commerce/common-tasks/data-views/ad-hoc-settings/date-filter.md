---
title: Filtrera data efter datumintervall
description: Lär dig använda det globala datumintervallfiltret.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Filtrera data efter datumintervall

<!-- The same in new UI and legacy CM views -->

Samma globala datumintervallfilter tillämpas på de flesta av dina datavyer, för alla dina annonsörer, förutom för standardvyer och anpassade vyer som du har sparat specifika datumintervall för. Systemets standarddatumintervall för kampanjhanteringsvyer är&quot;I går&quot;.

Inställningarna för datumintervall sparas i en webbläsarspecifik cookie, så alla ändringar i datumintervallfiltret används för alla dina annonsörer varje gång du loggar in med samma webbläsarprogram tills du ändrar filtret eller tar bort cookien. Varje webbläsarprogram som du använder lagrar inställningar för datumintervallfilter i en annan cookie.

När du sparar ett visst datumintervall för en standardvy eller anpassad vy används det intervallet när du använder vyn, oavsett vilket webbläsarprogram du använder.

>[!NOTE]
>
>* Du kan visa data för de senaste 13 månaderna, men befintliga anpassade vyer kan endast innehålla data för upp till de föregående 180 dagarna.
>* Om du vill visa tidigare data går du till [[!UICONTROL Reports]-vyn &#x200B;](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) och kör en grundläggande rapport.
>* Du kan också spara ett datumintervall för en [standardvy eller anpassad vy](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Ändra det globala datumfiltret i kampanjvyer

1. Klicka på det aktuella datumintervallet ovanför en datatabell i Sök \> kampanjer \> Kampanjer.

1. Ange intervallet i fältet **[!UICONTROL Date Range]**:

   * För ett förinställt intervall: Välj i listan över vanliga tidssteg, från *[!UICONTROL Today]* till *[!UICONTROL Last 180 Days]*. Standardvärdet är *[!UICONTROL Yesterday]*.

   * För ett visst intervall: Välj **[!UICONTROL Custom Date Range]** och ange sedan start- och slutdatum.

     Ange datum i formatet MM/DD/ÅÅÅÅ eller MM-DD-ÅÅÅÅ, eller klicka på ![kalenderikonen](/help/search-social-commerce/assets/calendar.png "kalenderikonen") bredvid varje fält för att öppna kalendern och välja ett datum.

1. (Valfritt) Jämför data för det angivna datumintervallet med data för ett andra datumintervall:

   1. Flytta skjutreglaget **[!UICONTROL Comparison]** till&quot;på&quot;-positionen.

      När du väljer det här alternativet läggs ytterligare två kolumner till för varje vanlig datakolumn. I stället för att bara inkludera en kolumn för [!UICONTROL Impressions], innehåller tabellen kolumner för [!UICONTROL Impressions R1], [!UICONTROL Impressions R2] och [!UICONTROL Impressions Diff].  Om du exporterar data stavas samma kolumner ut som [!UICONTROL Impressions Range 1], [!UICONTROL Impressions Range 2] och [!UICONTROL Impressions Difference].

   1. Ange det andra datumintervallet.

   1. Välj hur du vill uttrycka skillnaden mellan data i de två valda datumintervallen i kolumnen &quot;\[_Datafält_\] Differens&quot;:

      * *[!UICONTROL Variance]* (standard): Visar skillnaden som ett numeriskt värde.

      * *[!UICONTROL % Change]:* Visar skillnaden i procent.

1. Klicka på **[!UICONTROL Apply]**.
