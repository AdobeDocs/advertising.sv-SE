---
title: '[!DNL Baidu] nyckelordsinställningar'
description: Referera inställningarna för  [!DNL Baidu] nyckelord.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Inställningar för nyckelord för [!DNL Baidu]

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden. Den maximala längden per nyckelord är 30 enkelbyte- eller 15 dubbelbyte-tecken

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader. Använd följande syntax:

* `keyword` för bred matchning
* `"keyword"` för frasmatchning
* `[keyword]` för exakt matchning

>[!NOTE]
>
>* [!DNL Baidu] tillåter bara en matchningstyp per nyckelord per annonsgrupp. Annonsgrupp 1 kan till exempel inte innehålla både `"keyword"` och `[keyword]`.
>* Du kan skapa negativa nyckelord från vyn [!UICONTROL Keywords] > [!UICONTROL Negatives] och i annonsgruppen och kampanjinställningarna.
>* Om du ändrar ett [!DNL Baidu]-nyckelord tas det befintliga nyckelordet bort och ett nytt skapas med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.

**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-alternativ

**[!UICONTROL Base URL]:** (Kampanjer med enbart nyckelordsnivåspårning, valfritt) Den URL till landningssidan som användarna tas till när de klickar på din annons. Den kan innehålla
omdirigering och spårningskod från tredje part. Om du anger ett värde åsidosätter det annonsens bas-URL.

När du har sparat posten innehåller bas-URL:en eventuella tilläggsparametrar som har konfigurerats för kampanjen eller kontot.

Om du använder tjänsten för spårning av Adobe Advertising-konvertering och kampanjinställningarna innehåller [!UICONTROL EF Redirect] och lägger till spårning på nyckelordsnivå, lägger Search, Social och Commerce automatiskt till en egen klickspårningskod.

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
