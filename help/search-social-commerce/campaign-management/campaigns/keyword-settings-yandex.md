---
title: "[!DNL Yandex] nyckelordsinställningar"
description: Referera inställningarna för [!DNL Yandex] nyckelord.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] nyckelordsinställningar

Yandex-nyckelord används både för söknings- och visningsnätverk (innehåll).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelordsfraser, inklusive [Syntax för Yandex-matchningstyp](https://yandex.com/support/direct/keywords/symbols-and-operators.html) för nyckelord. Varje nyckelord kan ha högst sju ord, med undantag för stoppord.

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Ändra en [!DNL Yandex] nyckelord eller matchningstyp tar bort det befintliga nyckelordet och skapar ett nytt.
>* Varje Yandex-annonsgrupp kan innehålla högst 200 nyckelord.


**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Värdet för `{param1}` och `{param2}` substitutionsvariabler, som ersätts med instanser av {param1} och {param2} i bas-URL:en för annonser och sitelinks när nyckelordet används för att visa annonsen. Maximala längden är 255 byte.

Specialtecken kodas automatiskt i UTF-8. Om den associerade annonsen till exempel har bas-URL:en http://www.example.com/{param1} och nyckelordsvärdet {param1} är shoes/flats.html, leder annonsen till http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

