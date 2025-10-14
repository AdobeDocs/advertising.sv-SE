---
title: Redigera data som genererats från feeds
description: Lär dig hur du redigerar data som genereras från lagerdataflöden.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Redigera data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

När du sprider feed-data utan att samtidigt publicera dem i annonsnätverket kan du redigera data på något av följande sätt. Du kan senare [publicera data](propagated-data-post.md) från båda platserna till de relevanta annonsnätverken om du vill:

* Om du använde alternativet för [!UICONTROL Propagate and Preview] kan du redigera den genererade kalkylbladsfilen (med namnet `<feed file name>_<template name>`) genom att hämta den från vyn [!UICONTROL Bulksheets], redigera filen och överföra den igen. Det finns inga data på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

* Om du använde alternativet för [!UICONTROL Propagate only] kan du redigera genererade data för komponenter med [[!UICONTROL New] status &#x200B;](propagated-data-status.md) i en kampanjhierarkivy från flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

  Vyerna för kampanjhierarkin visar bara data som genererats från feedfilen, inte de befintliga kontokomponenterna. När data för en komponent och alla dess underkomponenter har publicerats i annonsnätverket visas den inte längre i kampanjhierarkin.

   1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

   1. (Valfritt) Om du bara vill visa kampanjkomponenter som skapats för en viss mall:

      1. Klicka på mallnamnet.

      1. Expandera annonsnätverkets nod och noden för annonsnätverket på menyn [!UICONTROL Accounts] i det vänstra navigeringsfönstret och markera sedan kryssrutan bredvid mallnamnet.

   1. Klicka på fliken **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** eller **[!UICONTROL Ads]**, beroende på vilka komponenter du vill visa.

      >[!NOTE]
      >
      >* Såvida du inte visar data för en viss mall visar flikarna [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads] alla annonsgrupper, nyckelord och annonser som har skapats från alla mallar och feeds. Produktgrupper som används för [!DNL Google Ads] shoppingannonser visas på fliken [!UICONTROL Keywords].
      >* Om du bara vill visa underkomponenterna för en viss kampanj börjar du med att visa fliken [!UICONTROL Campaigns]. Om du bara vill visa underkomponenterna för en viss annonsgrupp börjar du med att visa fliken [!UICONTROL Ad Groups].

   1. (Valfritt; om du bara vill redigera annonsgrupper, nyckelord eller annonser) Filtrera listan så att den endast innehåller underkomponenterna för en viss kampanj eller annonsgrupp:

      * Om du vill visa alla annonsgrupper i en kampanj klickar du på kampanjnamnet.

      * Om du vill visa alla nyckelord i en annonsgrupp klickar du på annonsgruppens namn.

      * Om du vill visa alla som i en annonsgrupp klickar du på annonsgruppens namn och sedan på fliken [!UICONTROL Ads].

   1. Klicka på ikonen [Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Ikon för Visa/redigera inställningar") bredvid kampanjens, annonsgruppens, nyckelordets eller annonsens namn.

   1. Redigera inställningarna och klicka sedan på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](inventory-feeds-about.md)
>* [Visa data som har genererats från feeds](propagated-data-view.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
