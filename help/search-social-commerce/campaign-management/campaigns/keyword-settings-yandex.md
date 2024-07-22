---
title: '[!DNL Yandex] nyckelordsinställningar'
description: Referera inställningarna för  [!DNL Yandex] nyckelord.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Inställningar för nyckelord för [!DNL Yandex]

Yandex-nyckelord används både för söknings- och visningsnätverk (innehåll).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Nyckelordsfraser, inklusive all [Yandex-matchningstypssyntax ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) för nyckelord. Varje nyckelord kan ha högst sju ord, med undantag för stoppord.

Du kan ange eller klistra in upp till 2 000 nyckelord. Avgränsa flera nyckelord med kommatecken eller ange dem på separata rader.

>[!NOTE]
>
>* Om du ändrar ett [!DNL Yandex]-nyckelord eller en matchningstyp tas det befintliga nyckelordet bort och ett nytt skapas.
>* Varje Yandex-annonsgrupp kan innehålla högst 200 nyckelord.

**[!UICONTROL Status]:** Visningsstatus för nyckelordet: *Aktiv* eller *Pausad*. Standardvärdet för nya nyckelord är *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platshållare

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Värdet för variablerna `{param1}` och `{param2}`, som ersätts av instanser av {param1} och {param2} i bas-URL:en för annonser och sitelinks när nyckelordet används för att visa annonsen. Maximala längden är 255 byte.

Specialtecken kodas automatiskt i UTF-8. Om den associerade annonsen till exempel har bas-URL:en http://www.example.com/{param1} och nyckelordsvärdet {param1} är shoes/flats.html, leder annonsen till http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
