---
title: "[!DNL Microsoft Advertising] nyckelordsinställningar"
description: Referera inställningarna för [!DNL Microsoft Advertising] nyckelord.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] nyckelordsinställningar

Du kan skapa nyckelord för kampanjer som använder sök- och visningsnätverk.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden, inklusive [!DNL Microsoft Advertising] matchar syntax och platshållare. Den maximala längden per nyckelord är 100 tecken.

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Du kan skapa negativa nyckelord från [!UICONTROL Keywords] > [!UICONTROL Negatives] i annonsgruppen och kampanjinställningarna.
>* Ändra en [!DNL Microsoft Advertising] nyckelordet tar bort det befintliga nyckelordet och skapar ett nytt med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.


**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param2]:** Den sträng som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller [den `{Param2}` dynamisk ersättningssträng](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken).

**[!UICONTROL Param3]:** Den sträng som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens titel, beskrivning eller bas-URL innehåller [den `{Param3}` dynamisk ersättningssträng](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Den maximala längden är 70 tecken, men tänk på den maximala längden för det annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken).

## URL-alternativ

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Det här fältet kan även innehålla `{Param2}` och `{Param3}` dynamiska ersättningsvariabler.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

