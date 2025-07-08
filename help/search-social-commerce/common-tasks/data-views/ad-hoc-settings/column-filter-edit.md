---
title: Redigera kolumnfilter
description: Lär dig hur du redigerar kolumnfilter.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Redigera kolumnfilter

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

## (Nytt användargränssnitt) Redigera en filteruppsättning i en hanteringsvy

1. Klicka på ![Filter](/help/search-social-commerce/assets/filter-new.png "Filter") i verktygsfältet.

1. Gör något av följande i filterinställningarna:

   * Om du vill lägga till ett filter klickar du på **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i indatafältet **[!UICONTROL ADD FILTER]**.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka på ![nedpilen](/help/search-social-commerce/assets/arrow-down-expand.png "nedpilen") bredvid den andra menyn och markera sedan kryssrutorna intill varje värde som ska inkluderas.

         * (Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde.

           Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. filtrerar efter kampanjer med&quot;lån&quot; i namnet blir resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

   * Om du vill redigera ett befintligt filter klickar du på filtret och ändrar sedan filterdefinitionen.

   * Om du vill ta bort ett befintligt filter klickar du på **[!UICONTROL -]** bredvid filterdefinitionen.

## (Äldre användargränssnitt) Redigera en filteruppsättning i en kampanjhanteringsvy

1. Klicka på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") i verktygsfältet.

1. Gör något av följande i filterinställningarna:

   * Om du vill lägga till ett filter klickar du på ![Lägg till filter](/help/search-social-commerce/assets/add.png "Lägg till filter") **[!UICONTROL ADD FILTER]** och gör sedan följande:

      1. (Valfritt) Om du vill filtrera kolumnnamnen efter textsträng anger du söksträngen i indatafältet **[!UICONTROL ADD FILTER]**.

      1. Välj ett kolumnnamn på kolumnmenyn.

      1. Definiera filtret i kolumnen:

         * (Filter utan inmatningsfält) Klicka på ![nedpilen](/help/search-social-commerce/assets/arrow-down-expand.png "nedpilen") bredvid den andra menyn och markera sedan kryssrutorna intill varje värde som ska inkluderas.

         * (Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde.

           Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet.

           Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* eller *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* eller *[!UICONTROL no date].*

           **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

   * Om du vill redigera ett befintligt filter klickar du på filtret och ändrar sedan filterdefinitionen.

   * Om du vill ta bort ett befintligt filter klickar du på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort") bredvid filterdefinitionen.

1. ([!UICONTROL Keywords] endast vy; valfritt) Markera eller avmarkera inställningen till [!UICONTROL Include rows with no performance data].

   >[!WARNING]
   >
   >Om du väljer det här alternativet ökar sidans inläsningstid.

1. Klicka på **[!UICONTROL Apply]**.

## Redigera ett filter i en hanteringsvy

1. Ovanför datatabellen klickar du på filterdefinitionen.

1. Definiera om filtret i kolumnen:

   * (Filter utan inmatningsfält) Klicka på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") bredvid den andra menyn och markera kryssrutorna intill varje värde som ska inkluderas.

   * (Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde.

     Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet.

     Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *mindre än*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *inte innehåller* eller *börjar med.*

     **Obs!** Textvärden är inte skiftlägeskänsliga. Om du t.ex. söker efter kampanjer med&quot;lån&quot; i namnet innehåller resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.

>[!MORELIKETHIS]
>
>* [Använd ett datafilter från en kolumnrubrikmeny](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [Använd datafilter från verktygsfältet](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Ta bort ett kolumnfilter]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
