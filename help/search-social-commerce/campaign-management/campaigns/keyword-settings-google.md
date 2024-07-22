---
title: '[!DNL Google Ads] nyckelordsinställningar'
description: Referera inställningarna för  [!DNL Google Ads] nyckelord.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Inställningar för nyckelord för [!DNL Google Ads]

Du kan skapa nyckelord för kampanjer som använder sök- och visningsnätverk.

Se hjälpen för Google Ads för [nyckelordsbegränsningar per konto](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelorden, inklusive eventuell [!DNL Google Ads]-matchningssyntax för nyckelord och platshållare. [!DNL Google Ads]-konton kräver nyckelord med följande attribut:

* Den maximala längden per nyckelord är 80 tecken och inte mer än 10 ord.
* Nyckelordet får bara innehålla bokstäver, siffror och följande specialtecken: blanksteg `# $ & _ - " [] ' + . / :`

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Du kan skapa negativa nyckelord från vyn [!UICONTROL Keywords] > [!UICONTROL Negatives] och i annonsgruppen och kampanjinställningarna.
>* Om du ändrar ett [!DNL Google Ads]-nyckelord eller en matchningstyp tas det befintliga nyckelordet bort och ett nytt skapas.

**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param1]:** Den sträng som ska användas som ersättningsvärde om bas-URL:en eller spårningsmallen innehåller [den dynamiska `{param1}`](https://support.google.com/google-ads/answer/6305348)-ersättningssträngen.

**[!UICONTROL Param2]:** Den sträng som ska användas som ersättningsvärde om bas-URL:en eller spårningsmallen innehåller [den dynamiska `{param2}`](https://support.google.com/google-ads/answer/6305348)-ersättningssträngen.

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
