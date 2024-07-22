---
title: Använda datafilter från verktygsfältet
description: Lär dig filtrera siddata från verktygsfältet.
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Använda datafilter från verktygsfältet

Du kan använda så många filter du vill i en vy. Alla filter förenas med operatorn AND.

1. Klicka på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") i verktygsfältet.

1. Gör något av följande i filterinställningarna:

   * Om du vill lägga till ett filter klickar du på ![Lägg till filter](/help/search-social-commerce/assets/add.png "Lägg till filter") **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i indatafältet **[!UICONTROL ADD FILTER]**.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka på ![nedpilen](/help/search-social-commerce/assets/arrow-down-expand.png "nedpilen") bredvid den andra menyn och markera sedan kryssrutorna intill varje värde som ska inkluderas.

         * (Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde.

           Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. filtrerar efter kampanjer med&quot;lån&quot; i namnet blir resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements] och [!UICONTROL Auto Targets] endast vyer; valfritt) Ändra inställningen till [!UICONTROL Include rows with performance data only].

           **Varning!** Om du avmarkerar alternativet och vyn innehåller många entiteter utan prestandadata tar det längre tid att visa data.

   * Om du vill redigera ett befintligt filter klickar du på filtret, ändrar filterdefinitionen och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * Om du vill ta bort ett befintligt filter klickar du på **[!UICONTROL X]** bredvid filterdefinitionen.

1. Klicka på **[!UICONTROL Apply]**.
