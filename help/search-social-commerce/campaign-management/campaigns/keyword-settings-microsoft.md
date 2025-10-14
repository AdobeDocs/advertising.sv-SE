---
title: '[!DNL Microsoft Advertising] nyckelordsinställningar'
description: Referera inställningarna för  [!DNL Microsoft Advertising] nyckelord.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Inställningar för nyckelord för [!DNL Microsoft Advertising]

Du kan skapa nyckelord för kampanjer som använder sök- och visningsnätverk.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden, inklusive eventuell [!DNL Microsoft Advertising]-matchningssyntax och platshållare. Den maximala längden per nyckelord är 100 tecken.

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Du kan skapa negativa nyckelord från vyn [!UICONTROL Keywords] > [!UICONTROL Negatives] och i annonsgruppen och kampanjinställningarna.
>* Om du ändrar ett [!DNL Microsoft Advertising]-nyckelord tas det befintliga nyckelordet bort och ett nytt skapas med ett nytt nyckelords-ID. Om du ändrar matchningstypen tas dock inte det befintliga nyckelordet bort.

**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param2]:** Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens rubrik, beskrivning eller bas-URL innehåller [&#x200B; den `{Param2}` dynamiska ersättningssträngen &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken).

**[!UICONTROL Param3]:** Strängen som ska användas som ersättningsvärde om nyckelordets bas-URL eller annonsens rubrik, beskrivning eller bas-URL innehåller [&#x200B; den `{Param3}` dynamiska ersättningssträngen &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Den maximala längden är 70 tecken, men tänk på den maximala längden för de annonselement som du använder den i (t.ex. kan kombinationen av Rubrik 1 och Rubrik 2 innehålla högst 76 tecken).

## URL-alternativ

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Det här fältet kan även innehålla variablerna `{Param2}` och `{Param3}` för dynamisk ersättning.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
