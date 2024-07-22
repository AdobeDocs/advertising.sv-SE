---
title: Redigera kolumnfilter
description: Lär dig hur du redigerar kolumnfilter.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Redigera kolumnfilter

## Redigera en filteruppsättning

1. Klicka på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") i verktygsfältet.

1. Gör något av följande i filterinställningarna:

   * Om du vill lägga till ett filter klickar du på ![Lägg till filter](/help/search-social-commerce/assets/add.png "Lägg till filter") **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i indatafältet **[!UICONTROL ADD FILTER]**.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn, markera kryssrutorna intill varje värde som ska inkluderas och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

         * (Filter med indatafält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

           Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* eller *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

   * Om du vill redigera ett befintligt filter klickar du på filtret, ändrar filterdefinitionen och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * Om du vill ta bort ett befintligt filter klickar du på **[!UICONTROL X]** bredvid filterdefinitionen.

1. ([!UICONTROL Keywords] endast vy; valfritt) Markera eller avmarkera inställningen till [!UICONTROL Include rows with no performance data].

   >[!WARNING]
   >
   >Om du väljer det här alternativet ökar sidans inläsningstid.

1. Klicka på **[!UICONTROL Apply]**.

## Redigera ett enstaka filter

1. (Om det behövs) Utöka filteruppsättningen genom att klicka på ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer") i filteruppsättningen ovanför datatabellen.

1. Ovanför datatabellen klickar du på filterdefinitionen.

1. Redigera de filter som ska användas:

   1. (Valfritt) Redigera kolumnnamnet på kolumnmenyn.

   1. (Valfritt) Definiera om filtret i kolumnen:

      * (Filter utan inmatningsfält) Klicka på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn, markera kryssrutorna intill varje värde som ska inkluderas och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

      * (Filter med indatafält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

        Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet

        Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *mindre än*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *inte innehåller* eller *börjar med.*

        **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.
