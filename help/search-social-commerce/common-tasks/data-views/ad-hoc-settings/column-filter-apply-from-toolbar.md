---
title: Använda datafilter från verktygsfältet
description: Lär dig filtrera siddata från verktygsfältet.
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Använda datafilter från verktygsfältet

Du kan använda så många filter du vill i en vy. Alla filter förenas med operatorn AND.

1. Klicka på i verktygsfältet ![Filter](/help/search-social-commerce/assets/filter.png "Filter").

1. Gör något av följande i filterinställningarna:

   * Klicka på om du vill lägga till ett filter ![Lägg till filter](/help/search-social-commerce/assets/add.png "Lägg till filter") **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i dialogrutan **[!UICONTROL ADD FILTER]** indatafält.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn och markera sedan kryssrutorna intill varje värde som ska inkluderas.

         * (Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde.

           Om du t.ex. har valt[!UICONTROL Clicks]&quot; och bara vill returnera rader med fler än 100 klick, välj sedan *[!UICONTROL greater than]*&quot; och ange `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du till exempel filtrerar efter kampanjer med&quot;lån&quot; i namnet kommer resultatet att vara&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements]och [!UICONTROL Auto Targets] endast vyer; valfritt) Ändra inställningen till[!UICONTROL Include rows with performance data only].&quot;

           **Varning:** Om du avmarkerar alternativet och vyn innehåller många enheter utan prestandadata tar det längre tid att visa data.

   * Om du vill redigera ett befintligt filter klickar du på filtret, ändrar filterdefinitionen och klickar sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * Om du vill ta bort ett befintligt filter klickar du **[!UICONTROL X]** bredvid filterdefinitionen.

1. Klicka på **[!UICONTROL Apply]**.
