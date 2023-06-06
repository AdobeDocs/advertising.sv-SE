---
title: Hämta data från en kampanjhanteringsvy
description: Lär dig hur du hämtar data från de flesta vyer för kampanjhantering.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Hämta data från en kampanjhanteringsvy

Du kan hämta data från [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] andra vyer än [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences]och [!UICONTROL Extensions] vyer. Du kan hämta antingen:

* En rapport i [!DNL XLSM] (makroaktiverat) [!DNL Microsoft® Excel] kalkylblad). Om du markerar specifika rader i vyn innehåller rapporten en rad för varje markerad rad. Om du inte markerar några rader skapas en rad för varje rad i vyn.

* En kalkylbladsfil i TXT-format som innehåller alla relevanta underordnade enheter. Om du väljer rader för entiteter i flera annonsnätverk skapas en fil för varje relevant annonsnätverk. Om du inte markerar några rader skapas en fil för varje annonsnätverk som visas i vyn. Bulkbladsfiler som genereras för olika annonsnätverk innehåller olika datakolumner.

   Om ni genererar data för flera kampanjer och de kombinerade data består av över 500 000 rader, delas data upp ytterligare efter kampanj i två eller flera filer, efter behov, med namnet `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`och så vidare.

   Varje kalkylbladsfil i [!UICONTROL Downloads] visas även på [!UICONTROL Bulksheets] vy. När filen har skapats får du ett e-postmeddelande med en länk där du kan hämta filen; Beroende på mängden data som sammanställs kan det ta flera minuter eller mer att skicka meddelandet. Om det inte går att generera filen visas en felfil i vyn Bulksheets och du får ett e-postmeddelande med en länk till felfilen. Ta bort en kalkylbladsfil från [!UICONTROL Download] eller [!UICONTROL Bulksheets] tas bort från båda platserna.

1. (Valfritt) Markera enskilda rader som ska inkluderas i filen.

   Annars inkluderas alla data i vyn.

1. Klicka på till höger om verktygsfältet ![Ladda ned rapport](/help/search-social-commerce/assets/download.png "Ladda ned rapport").

1. Klicka ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") **[!UICONTROL Create]** kan du lägga till filnamnet och sedan klicka på **[!UICONTROL Report]** eller **[!UICONTROL Bulksheet]**.

1. (Valfritt) När rapportjobbet är klart klickar du på ![Ladda ned rapport](/help/search-social-commerce/assets/download.png "Ladda ned rapport") för att visa [!UICONTROL Available Reports] och hämta eller ta bort rapporten:

   * Om du vill öppna eller spara filen enligt webbläsarens normala procedur klickar du på ![Ladda ned kalkylblad](/help/search-social-commerce/assets/download-spreadsheet.png "Ladda ned kalkylblad").

      Mer information om webbläsarproceduren finns i webbläsarens onlinehjälp.

   * Om du vill ta bort filen klickar du på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort").

>[!MORELIKETHIS]
>
>[Ta bort en rapport eller ett kalkylbladsdokument från [!UICONTROL Downloads] meny](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
