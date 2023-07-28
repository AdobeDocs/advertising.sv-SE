---
title: Redigera kolumnfilter
description: Lär dig hur du redigerar kolumnfilter.
exl-id: 6e42e006-089b-44b9-b9b1-66835b680413
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Redigera kolumnfilter

## Redigera en filteruppsättning

1. Klicka ![Filter](/help/search-social-commerce/assets/filter.png "Filter") i verktygsfältet.

1. Gör något av följande i filterinställningarna:

   * Klicka på om du vill lägga till ett filter ![Lägg till filter](/help/search-social-commerce/assets/add.png "Lägg till filter") **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i dialogrutan **[!UICONTROL ADD FILTER]** indatafält.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn markerar du kryssrutorna intill varje värde som ska inkluderas och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

         * (Filter med inmatningsfält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

           Om du t.ex. har valt[!UICONTROL Clicks]&quot; och bara vill returnera rader med fler än 100 klick, välj sedan *[!UICONTROL greater than]*&quot; och ange `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, eller *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

   * Om du vill redigera ett befintligt filter klickar du på filtret, ändrar filterdefinitionen och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * Om du vill ta bort ett befintligt filter klickar du **[!UICONTROL X]** bredvid filterdefinitionen.

1. ([!UICONTROL Keywords] endast visa; valfritt) Markera eller avmarkera inställningen till[!UICONTROL Include rows with no performance data].&quot;

   >[!WARNING]
   >
   >Om du väljer det här alternativet ökar sidans inläsningstid.

1. Klicka på **[!UICONTROL Apply]**.

## Redigera ett enstaka filter

1. (Om det behövs) Klicka på i filteruppsättningen ovanför datatabellen ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer") för att expandera filteruppsättningen.

1. Ovanför datatabellen klickar du på filterdefinitionen.

1. Redigera de filter som ska användas:

   1. (Valfritt) Redigera kolumnnamnet på kolumnmenyn.

   1. (Valfritt) Definiera om filtret i kolumnen:

      * (Filter utan inmatningsfält) Klicka ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn markerar du kryssrutorna intill varje värde som ska inkluderas och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

      * (Filter med inmatningsfält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

        Om du t.ex. har valt[!UICONTROL Clicks]&quot; och bara vill returnera rader med fler än 100 klick, välj sedan *[!UICONTROL greater than]*&quot; och ange `100` i indatafältet

        Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *mindre än*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *innehåller inte*, eller *börjar med.*

        **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.
