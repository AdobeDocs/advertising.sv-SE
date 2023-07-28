---
title: '''[!DNL Google Ads] nyckelordsinställningar'
description: Referera inställningarna för [!DNL Google Ads] nyckelord.
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] nyckelordsinställningar

Du kan skapa nyckelord för kampanjer som använder sök- och visningsnätverk.

Se hjälpen för Google Ads för [nyckelordsbegränsningar per konto](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden, inklusive [!DNL Google Ads] matchar syntaxen för nyckelord och platshållare. [!DNL Google Ads] konton kräver nyckelord med följande attribut:

* Den maximala längden per nyckelord är 80 tecken och inte mer än 10 ord.
* Nyckelordet får endast innehålla bokstäver, siffror och följande specialtecken: blanksteg `# $ & _ - " [] ' + . / :`

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Du kan skapa negativa nyckelord från [!UICONTROL Keywords] > [!UICONTROL Negatives] i annonsgruppen och kampanjinställningarna.
>* Ändra en [!DNL Google Ads] nyckelord eller matchningstyp tar bort det befintliga nyckelordet och skapar ett nytt.

**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param1]:** Strängen som ska användas som ersättningsvärde om bas-URL:en eller spårningsmallen innehåller [den `{param1}`](https://support.google.com/google-ads/answer/6305348) dynamisk ersättningssträng.

**[!UICONTROL Param2]:** Strängen som ska användas som ersättningsvärde om bas-URL:en eller spårningsmallen innehåller [den `{param2}`](https://support.google.com/google-ads/answer/6305348) dynamisk ersättningssträng.

## URL-alternativ

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
