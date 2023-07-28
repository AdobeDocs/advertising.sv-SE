---
title: Redigera data som genererats från feeds
description: Lär dig hur du redigerar data som genereras från lagerdataflöden.
exl-id: 5f866557-e44b-4fd9-9683-f7fbaf6d308b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Redigera data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

När du sprider feed-data utan att samtidigt publicera dem i annonsnätverket kan du redigera data på något av följande sätt. Du kan välja senare [data](propagated-data-post.md) från båda ställena till de relevanta annonsnätverken:

* Om du använde alternativet för att &quot;[!UICONTROL Propagate and Preview]kan du redigera den genererade kalkylbladsfilen (med namnet &quot;`<feed file name>_<template name>`&quot;) genom att ladda ned den från [!UICONTROL Bulksheets] visa, redigera filen och överföra den igen. Det finns inga data på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar.

* Om du använde alternativet för att &quot;[!UICONTROL Propagate only]&quot; kan du redigera genererade data för komponenter med [[!UICONTROL New] status](propagated-data-status.md) i en kampanjhierarkivy från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar.

  Vyerna för kampanjhierarkin visar bara data som genererats från feedfilen, inte de befintliga kontokomponenterna. När data för en komponent och alla dess underkomponenter har publicerats i annonsnätverket visas den inte längre i kampanjhierarkin.

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

   1. (Valfritt) Om du bara vill visa kampanjkomponenter som skapats för en viss mall:

      1. Klicka på mallnamnet.

      1. I [!UICONTROL Accounts] i den vänstra navigeringsrutan expanderar du annonsnätverkets nod och annonsnätverkets kontonod och markerar sedan kryssrutan bredvid mallnamnet.

   1. Klicka på **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, eller **[!UICONTROL Ads]** , beroende på vilka komponenter du vill visa.

      >[!NOTE]
      >
      >* Om du inte visar data för en viss mall kan du [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] På flikarna visas alla annonsgrupper, nyckelord och annonser som har skapats från alla mallar och feed-filer. Produktgrupper som används för [!DNL Google Ads] shoppingannonser visas på [!UICONTROL Keywords] -fliken.
      >* Om du bara vill visa underkomponenterna för en viss kampanj börjar du med att visa [!UICONTROL Campaigns] -fliken. Om du bara vill visa underkomponenterna i en viss annonsgrupp börjar du med att visa [!UICONTROL Ad Groups] -fliken.

   1. (Valfritt; om du bara vill redigera annonsgrupper, nyckelord eller annonser) Filtrera listan så att den endast innehåller underkomponenterna för en viss kampanj eller annonsgrupp:

      * Om du vill visa alla annonsgrupper i en kampanj klickar du på kampanjnamnet.

      * Om du vill visa alla nyckelord i en annonsgrupp klickar du på annonsgruppens namn.

      * Om du vill visa alla som i en annonsgrupp klickar du på annonsgruppens namn och sedan på knappen [!UICONTROL Ads] -fliken.

   1. Klicka [Ikon för Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Ikon för Visa/redigera inställningar") bredvid kampanjens namn, annonsgrupp, nyckelord eller annonsnamn.

   1. Redigera inställningarna och klicka sedan på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Om lagerflöden](inventory-feeds-about.md)
>* [Visa data som genererats från feeds](propagated-data-view.md)
>* [Posta kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
