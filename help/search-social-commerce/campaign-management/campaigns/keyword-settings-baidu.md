---
title: "[!DNL Baidu] nyckelordsinställningar"
description: Referera inställningarna för [!DNL Baidu] nyckelord.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] nyckelordsinställningar

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden. Den maximala längden per nyckelord är 30 enkelbyte- eller 15 dubbelbyte-tecken

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader. Använd följande syntax:

* `keyword` för bred matchning
* `"keyword"` för frasmatchning
* `[keyword]` för exakt matchning

>[!NOTE]
>
>* [!DNL Baidu] tillåter endast en matchningstyp per nyckelord per annonsgrupp. Annonsgrupp 1 kan till exempel inte innehålla båda `"keyword"` och `[keyword]`.
>* Du kan skapa negativa nyckelord från [!UICONTROL Keywords] > [!UICONTROL Negatives] i annonsgruppen och kampanjinställningarna.
>* Ändra en [!DNL Baidu] nyckelordet tar bort det befintliga nyckelordet och skapar ett nytt med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.


**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-alternativ

**[!UICONTROL Base URL]:** (Kampanjer med enbart nyckelordsspårning. (valfritt) Den URL till landningssidan som användarna tas till när de klickar på annonsen. Den kan innehålla omdirigering från tredje part och spårningskod. Om du anger ett värde åsidosätter det annonsens bas-URL.

När du har sparat posten innehåller bas-URL:en eventuella tilläggsparametrar som har konfigurerats för kampanjen eller kontot.

Om du använder Adobe Advertising conversion service och kampanjinställningarna inkluderar [!UICONTROL EF Redirect] och lägger till spårning på nyckelordsnivå lägger sedan Search, Social och Commerce automatiskt till en egen klickspårningskod.

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

