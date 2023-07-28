---
title: Använda datafilter från en kolumnrubrikmeny
description: Lär dig filtrera siddata från en kolumnrubrikmeny.
exl-id: ad745599-fd98-4f34-b181-085070adb685
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Använda ett datafilter från en kolumnrubrikmeny

Du kan använda så många filter du vill för en kolumn, ett i taget. Alla filter förenas med operatorn AND. Om du vill lägga till mer än ett filter i taget med alla tillgängliga mätvärden, se &quot;[Använda datafilter från verktygsfältet](column-filter-apply-from-toolbar.md).&quot;

1. Klicka på till höger om kolumnrubriken ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-dropdown.png "Nedåtpil")och klicka sedan på **[!UICONTROL Add Filter]**.

1. Definiera filtret i kolumnen:

   * (Filter utan inmatningsfält) Markera kryssrutorna intill varje värde som ska inkluderas och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * (Filter med inmatningsfält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

     Om du t.ex. har valt[!UICONTROL Clicks]&quot; och bara vill returnera rader med fler än 100 klick, välj sedan *[!UICONTROL greater than]*&quot; och ange `100` i indatafältet Beroende på datatypen kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, eller *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Textvärden är inte skiftlägeskänsliga. Om du till exempel filtrerar efter kampanjer med&quot;lån&quot; i namnet är resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.
     >* Du kan bara använda ett enkelt numeriskt filter (till exempel [!UICONTROL Impressions] \> 100) per kolumn.
