---
title: Visa data som genererats från feeds
description: Lär dig hur du visar data som genererats från lagerdataflöden.
exl-id: 961155ac-a9d3-42e4-904b-b968e9f3383b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Visa data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

När du sprider feed-data utan att samtidigt publicera dem i annonsnätverket kan du förhandsgranska data på något av följande sätt. Du kan välja senare [data](propagated-data-post.md) från båda ställena till de relevanta annonsnätverken.

* Om du använde alternativet för att &quot;[!UICONTROL Propagate and Preview],&quot; visas det genererade kalkylbladet (med namnet &quot;`<feed file name>_<template name>`&quot;) från [!UICONTROL Bulksheets] vy. Det finns inga data på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar. Med det här alternativet kan du [validera landningssidorna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) som är kopplade till annonserna och nyckelorden innan du publicerar data.

* Om du använde alternativet för att &quot;[!UICONTROL Propagate only],&quot; och sedan visa genererade data i en kampanjhierarkivy från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar.

  Vyerna för kampanjhierarkin visar bara data som genererats från feedfilen, inte de befintliga kontokomponenterna. När data för en komponent och alla dess underkomponenter har publicerats i annonsnätverket visas den inte längre i kampanjhierarkivyn.

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

   1. (Valfritt) Om du bara vill visa kampanjkomponenter som skapats för en viss mall:

      1. Klicka på mallnamnet.

      1. I [!UICONTROL Accounts] i den vänstra navigeringsrutan expanderar du annonsnätverkets nod och annonsnätverkets kontonod och markerar sedan kryssrutan bredvid mallnamnet.

   1. Klicka på **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, eller **[!UICONTROL Ads]** , beroende på vilka komponenter du vill visa.

      >[!NOTE]
      >
      >* Om du inte visar data för en viss mall kan du [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] På flikarna visas alla annonsgrupper, nyckelord och annonser som har skapats från alla mallar och feed-filer. Produktgrupper som används för [!DNL Google Ads] shoppingannonser visas på [!UICONTROL Keywords] -fliken.
      >* Om du bara vill visa underkomponenterna för en viss kampanj börjar du med att visa [!UICONTROL Campaigns] -fliken. Om du bara vill visa underkomponenterna i en viss annonsgrupp börjar du med att visa [!UICONTROL Ad Groups] -fliken.

   1. (Valfritt) Om du vill visa mer information gör du något av följande:

      * Om du vill visa inställningarna för en kampanj, annonsgrupp, nyckelord eller annons klickar du på [Ikon för Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Ikon för Visa/redigera inställningar") bredvid namnet.

      * Så här visar du underkomponenterna för en kampanj eller annonsgrupp:

         * Om du vill visa alla annonsgrupper i en kampanj klickar du på kampanjnamnet.

         * Om du vill visa alla nyckelord eller produktmål i en annonsgrupp klickar du på annonsgruppens namn.

         * Om du vill visa alla annonser i en annonsgrupp klickar du på annonsgruppens namn och sedan på knappen [!UICONTROL Ads] -fliken.

>[!MORELIKETHIS]
>
>* [Om lagerflöden](inventory-feeds-about.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Posta kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
