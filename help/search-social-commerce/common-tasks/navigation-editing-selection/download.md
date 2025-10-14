---
title: Hämta data från en kampanjhanteringsvy
description: Lär dig hur du hämtar data från de flesta vyer för kampanjhantering.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# (Äldre användargränssnitt) Hämta data från en kampanjhanteringsvy

*Äldre användargränssnitt*

Du kan hämta data från vyerna [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] förutom vyerna [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] och [!UICONTROL Extensions]. Du kan hämta antingen:

* En rapport i formatet [!DNL XLSM] (makroaktiverat [!DNL Microsoft Excel]-kalkylblad). Om du markerar specifika rader i vyn innehåller rapporten en rad för varje markerad rad. Om du inte markerar några rader skapas en rad för varje rad i vyn.

* En kalkylbladsfil i TXT-format som innehåller alla relevanta underordnade enheter. Om du väljer rader för entiteter i flera annonsnätverk skapas en fil för varje relevant annonsnätverk. Om du inte markerar några rader skapas en fil för varje annonsnätverk som visas i vyn. Bulkbladsfiler som genereras för olika annonsnätverk innehåller olika datakolumner.

  Om du genererar data för flera kampanjer och de kombinerade data består av över 500 000 rader, delas data ytterligare upp efter kampanj i två eller flera filer, om det behövs, med namnen `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt` och så vidare.

  Alla kalkylbladsfiler på panelen [!UICONTROL Downloads] visas också i vyn [!UICONTROL Bulksheets]. När filen skapas får du ett e-postmeddelande med en länk från vilken du kan hämta filen. Beroende på mängden data som kompileras kan meddelandet ta flera minuter eller mer. Om det däremot inte går att generera filen visas en felfil i vyn Bulksheets och du får ett e-postmeddelande med en länk till felfilen. Om du tar bort en kalkylbladsfil från panelen [!UICONTROL Download] eller fliken [!UICONTROL Bulksheets] tas den bort från båda platserna.

>[!NOTE]
>
>Se även hjälpen om hur du hämtar data i det nya användargränssnittet från [[!UICONTROL Portfolios]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md), [[!UICONTROL Campaigns]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md) och [[!UICONTROL Ad Groups]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md).

1. (Valfritt) Markera enskilda rader som ska inkluderas i filen.

   I annat fall inkluderas alla data i vyn.

1. Klicka på ![Rapportera hämtning](/help/search-social-commerce/assets/download.png "Rapportera hämtning") till höger om verktygsfältet.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") **[!UICONTROL Create]**, lägg till filnamnet om du vill och klicka sedan på antingen **[!UICONTROL Report]** eller **[!UICONTROL Bulksheet]**.

1. (Valfritt) När rapportjobbet är klart klickar du på ![Rapporthämtning](/help/search-social-commerce/assets/download.png "Rapporthämtning") för att visa panelen [!UICONTROL Available Reports] och hämtar eller tar sedan bort rapporten:

   * Om du vill öppna eller spara filen enligt webbläsarens normala procedur klickar du på ![Hämta kalkylblad](/help/search-social-commerce/assets/download-spreadsheet.png "Hämta kalkylblad").

     Mer information om webbläsarproceduren finns i webbläsarens onlinehjälp.

   * Klicka på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort") om du vill ta bort filen.

>[!MORELIKETHIS]
>
>* [(Äldre användargränssnitt) Ta bort en rapport eller en kalkylbladsfil för prestanda från [!UICONTROL Downloads]-menyn &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [(Nytt användargränssnitt) Hantera datavyrapporter från [!UICONTROL Portfolios]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)
>* [(Nytt användargränssnitt) Hantera datavyrapporter från [!UICONTROL Campaigns]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)
>* [(Nytt användargränssnitt) Hantera datavyrapporter från [!UICONTROL Ad Groups]-vyn &#x200B;](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)
