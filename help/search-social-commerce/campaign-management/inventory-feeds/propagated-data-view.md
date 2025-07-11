---
title: Visa data som genererats från feeds
description: Lär dig hur du visar data som genererats från lagerdataflöden.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Visa data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

När du sprider feed-data utan att samtidigt publicera dem i annonsnätverket kan du förhandsgranska data på något av följande sätt. Du kan senare [publicera data](propagated-data-post.md) från båda platserna till de relevanta annonsnätverken om du vill.

* Om du använde alternativet för [!UICONTROL Propagate and Preview] kan du visa det genererade kalkylbladet (med namnet `<feed file name>_<template name>`) från vyn [!UICONTROL Bulksheets]. Det finns inga data på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads]. Med det här alternativet kan du [validera landningssidorna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) som är kopplade till annonserna och nyckelorden innan du publicerar data.

* Om du använde alternativet för [!UICONTROL Propagate only] kan du visa genererade data i en kampanjhierarkivy från flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

  Vyerna för kampanjhierarkin visar bara data som genererats från feedfilen, inte de befintliga kontokomponenterna. När data för en komponent och alla dess underkomponenter har publicerats i annonsnätverket visas den inte längre i kampanjhierarkivyn.

   1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

   1. (Valfritt) Om du bara vill visa kampanjkomponenter som skapats för en viss mall:

      1. Klicka på mallnamnet.

      1. Expandera annonsnätverkets nod och noden för annonsnätverket på menyn [!UICONTROL Accounts] i det vänstra navigeringsfönstret och markera sedan kryssrutan bredvid mallnamnet.

   1. Klicka på fliken **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** eller **[!UICONTROL Ads]**, beroende på vilka komponenter du vill visa.

      >[!NOTE]
      >
      >* Såvida du inte visar data för en viss mall visar flikarna [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads] alla annonsgrupper, nyckelord och annonser som har skapats från alla mallar och feeds. Produktgrupper som används för [!DNL Google Ads] shoppingannonser visas på fliken [!UICONTROL Keywords].
      >* Om du bara vill visa underkomponenterna för en viss kampanj börjar du med att visa fliken [!UICONTROL Campaigns]. Om du bara vill visa underkomponenterna för en viss annonsgrupp börjar du med att visa fliken [!UICONTROL Ad Groups].

   1. (Valfritt) Om du vill visa mer information gör du något av följande:

      * Om du vill visa inställningarna för en kampanj, annonsgrupp, nyckelord eller annons klickar du på ikonen [Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Ikon för Visa/redigera inställningar") bredvid namnet.

      * Så här visar du underkomponenterna för en kampanj eller annonsgrupp:

         * Om du vill visa alla annonsgrupper i en kampanj klickar du på kampanjnamnet.

         * Om du vill visa alla nyckelord eller produktmål i en annonsgrupp klickar du på annonsgruppens namn.

         * Om du vill visa alla annonser i en annonsgrupp klickar du på annonsgruppens namn och sedan på fliken [!UICONTROL Ads].

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](inventory-feeds-about.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
