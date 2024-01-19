---
title: Skapa negativa nyckelord
description: Lär dig skapa negativa nyckelord för sökkampanjer och annonsgrupper.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Skapa negativa nyckelord

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads]och befintlig [!DNL Baidu] endast konton*

Du kan skapa negativa nyckelord för en sök- och annonsgrupp eller kampanj som riktar sig till nätverket för sökning eller visning/inbyggt nätverk. Negativa nyckelord utlöser inte annonser.

>[!NOTE]
>Du kan också skapa och redigera negativa nyckelord i [och gruppinställningar](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) och [kampanjinställningar](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Om du vill skapa flera negativa nyckelord samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa")och klicka sedan på **[!UICONTROL Campaign]** för att skapa negativa nyckelord på kampanjnivå eller **[!UICONTROL Ad Group]** för att skapa negativa nyckelord på annonsnivå.

1. Välj annonsnätverket, kontot, kampanjen och (om det är relevant) annonsgruppen och klicka sedan på **[!UICONTROL Continue]**.

1. Ange negativa nyckelord. Använd följande syntax utan minustecken (`-`):

   * Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft® Advertising])

   * Negativ frasmatchning: `"keyword"`

   * Negativ exakt matchning: `[keyword]`

   Avgränsa flera värden med kommatecken eller ange dem på separata rader. Du kan ange eller klistra in upp till 2 000 negativa nyckelord i en åtgärd. Se även följande krav och begränsningar:

   * Maximal teckenlängd: [!DNL Baidu]: 30 enkelbyte eller 15 dubbelbyte; [!DNL Microsoft® Advertising]: 100 enkelbyte eller 50 dubbelbyte; [!DNL Google Ads] och [!DNL Yahoo! Japan Ads]: 80 enkelbyte eller 40 dubbelbyte.

   * [!DNL Baidu] tillåter endast en matchningstyp per nyckelord per annonsgrupp. Annonsgrupp 1 kan till exempel inte innehålla båda `"keyword"` och `[keyword]`.

   * [!DNL Google Ads]: Varje nyckelord får inte bestå av mer än 10 ord och får endast innehålla bokstäver, siffror och följande specialtecken: blanksteg `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Varje nyckelord kan ha högst sju ord, med undantag för stoppord. Varje [!DNL Yandex ad group] kan innehålla högst 200 nyckelord.

1. Klicka på **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Om nyckelord](keyword-about.md)
>* [Hantera anbudsnyckelord](keyword-manage.md)
>* [Ändra status för nyckelord och negativa nyckelord](keyword-status-edit.md)
