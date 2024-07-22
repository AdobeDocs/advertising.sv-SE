---
title: Använda datafilter från en kolumnrubrikmeny
description: Lär dig filtrera siddata från en kolumnrubrikmeny.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Använda ett datafilter från en kolumnrubrikmeny

Du kan använda så många filter du vill för en kolumn, ett i taget. Alla filter förenas med operatorn AND. Om du vill lägga till mer än ett filter i taget med alla tillgängliga mätvärden läser du i &quot;[Använd datafilter från verktygsfältet](column-filter-apply-from-toolbar.md)&quot;.

1. Klicka på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-dropdown.png "Nedåtpil") till höger om kolumnrubriken och klicka sedan på **[!UICONTROL Add Filter]**.

1. Definiera filtret i kolumnen:

   * (Filter utan indatafält) Markera kryssrutorna intill varje värde som ska tas med och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

   * (Filter med indatafält) Välj en operator på den andra menyn, ange önskat värde och klicka sedan på ![Uppdatera filter](/help/search-social-commerce/assets/select.png "Uppdatera filter").

     Om du till exempel har markerat kolumnen [!UICONTROL Clicks] och bara vill returnera rader med fler än 100 klick, sedan väljer du *[!UICONTROL greater than]* och anger `100` i indatafältet Beroende på datatypen, kan tillgängliga operatorer inkludera *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]* , *[!UICONTROL after]* eller *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Textvärden är inte skiftlägeskänsliga. Om du till exempel filtrerar efter kampanjer med&quot;lån&quot; i namnet är resultatet&quot;konsumentlån&quot; och&quot;låneansökningar&quot;.
     >* Du kan bara använda ett enkelt numeriskt filter (till exempel [!UICONTROL Impressions] \> 100) per kolumn.
