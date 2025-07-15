---
title: Kör eller kör om en anpassad simulering
description: Lär dig hur du kör eller kör en anpassad simulering för en portfölj.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 1%

---

# Kör eller kör om en anpassad simulering

*Beta-funktion*

Du kan generera en anpassad simulering för en [optimerad eller aktiv](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)-portfölj. Du kan också ändra parametrarna för en befintlig simulering och återskapa simuleringen eller köra en befintlig simulering igen med de befintliga parametrarna.

[!UICONTROL Admin]- och [!UICONTROL Account Manager]-användare kan se simuleringar som skapats av andra användare. Alla andra användare kan bara se de anpassade simuleringar de skapar.

## Skapa en ny simulering

1. Klicka på **[!UICONTROL Plan]>[!UICONTROL Simulations]** på huvudmenyn.

1. Klicka på **[!UICONTROL Run Simulation]** ovanför datatabellen.

1. Välj portfölj:

   1. Klicka på **[!UICONTROL Select Portfolio]**.

   1. Välj portföljen.

      Om du vill söka efter portföljer som innehåller en viss textsträng börjar du med att ange textsträngen i sökfältet. Värden är inte skiftlägeskänsliga.

   1. Klicka på **[!UICONTROL Proceed]**.

1. Ange de [anpassade simuleringsinställningarna](#custom-simulation-settings):

   1. (Valfritt) Om du vill ändra portföljen som används för simuleringen klickar du på **[!UICONTROL Change Portfolio]** bredvid portföljnamnet, markerar portföljen och klickar sedan på **[!UICONTROL Proceed]**.

   1. På fliken [!UICONTROL Basic Settings]:

      1. Ange en unik **[!UICONTROL Simulation Name]**.

      1. (Valfritt) Ändra de grundläggande parametrarna för simuleringen.

   1. (Valfritt) Ändra de avancerade parametrarna för simuleringen på fliken [!UICONTROL Advanced Settings].

   De befintliga parametrarna för den valda portföljen anges som standard. Om du ändrar värdena visas resultatet som olika parametrar skulle ge utan att portföljens befintliga parametrar ändrades.

1. Klicka på **[!UICONTROL Next]**.

1. Granska inställningarna och redigera inställningarna efter behov.

1. Klicka på **[!UICONTROL Submit & Run]**.

När simuleringsrapporten är tillgänglig får du och andra angivna e-postmottagare ett meddelande med en länk för att hämta data i en ZIP-fil som innehåller en arbetsbok (XLSX-fil).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Redigera inställningarna för en befintlig simulering och kör den igen

1. Klicka på **[!UICONTROL Plan]>[!UICONTROL Simulations]** på huvudmenyn.

1. Markera kryssrutan bredvid simuleringen som ska genereras om.

1. Klicka på **[!UICONTROL Run Simulation]** ovanför datatabellen.

1. Ange de [anpassade simuleringsinställningarna](#custom-simulation-settings):

   1. (Valfritt) Om du vill ändra portföljen som används för simuleringen klickar du på **[!UICONTROL Change Portfolio]** bredvid portföljnamnet, markerar portföljen och klickar sedan på **[!UICONTROL Proceed]**.

   1. På fliken [!UICONTROL Basic Settings]:

      1. Ange en unik **[!UICONTROL Simulation Name]**.

      1. (Valfritt) Ändra de grundläggande parametrarna för simuleringen.

   1. (Valfritt) Ändra de avancerade parametrarna för simuleringen på fliken [!UICONTROL Advanced Settings].

   De befintliga parametrarna för den valda portföljen anges som standard. Om du ändrar värdena visas resultatet som olika parametrar skulle ge utan att portföljens befintliga parametrar ändrades.

1. Klicka på **[!UICONTROL Next]**.

1. Granska inställningarna och redigera inställningarna efter behov.

1. Klicka på **[!UICONTROL Submit & Run]**.

När simuleringsrapporten är tillgänglig får du och andra angivna e-postmottagare ett meddelande med en länk för att hämta data i en ZIP-fil som innehåller en arbetsbok (XLSX-fil).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Kör en simulering igen med de befintliga inställningarna

Du kan köra simuleringar som inte är köade igen.

1. Klicka på **[!UICONTROL Plan]>[!UICONTROL Simulations]** på huvudmenyn.

1. Markera kryssrutorna intill de simuleringar som du vill köra igen.

1. Klicka på ![Kör igen](/help/search-social-commerce/assets/rerun.png "Kör") i verktygsfältet ovanför datatabellen.

## Anpassade simuleringsinställningar {#custom-simulation-settings}

Mer information om anpassade simuleringsinställningar finns i Optimeringshandboken, som finns i Sök, Socialt och Commerce.

>[!MORELIKETHIS]
>
>* [Om simuleringar](simulation-about.md)
>* [Hämta simuleringar](simulation-download.md)
