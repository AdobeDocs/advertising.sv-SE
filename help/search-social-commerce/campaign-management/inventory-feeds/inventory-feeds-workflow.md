---
title: Automatisera och hantera lagerflöden
description: Lär dig mer om arbetsflödet för att automatiskt hantera kontostrukturen och leverera dynamiska annonser baserade på data om produkt- eller serviceartikeln.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Arbetsflöde för att hantera kampanjdata med lagerflöden

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

Testa först minst en feed-fil eller ett konto och sedan kan du automatisera processen helt eller fortsätta att styra den i varje steg:

1. (Valfritt) Kontakta kontoteamet på Adobe för att skapa en FTP-katalog för insättning av datafiler.

   Om du använder FTP-katalogen söker flödestjänsten efter nya filer varannan timme.

   I annat fall kan du överföra filer manuellt i [!UICONTROL Advanced (ACM)] vy.

1. Ange [parametrar för bearbetning av feed-data](feed-settings-manage.md#feed-data-settings).

   Om du använder FTP ska du inte automatiskt lägga upp data i annonsnätverken från början. När du har verifierat utdata från den första filen och är nöjd med resultatet kan du ändra inställningarna.

1. Överför en datafil till FTP-katalogen, [överföra en datafil manuellt](feed-files-manage.md) i [!UICONTROL Advanced (ACM) view], eller [aktivera åtkomst till ett Google- eller Microsoft®-handelscentkonto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Om du vill överföra filer manuellt kan du vänta tills du skapar en mall som använder datafilen.

1. (Valfritt) Skapa grupper med [modifierare](modifiers-manage.md) som ska användas som variabler i olika datafält i flödesdatamallar.

1. [Skapa en eller flera mallar](ad-templates/ad-template-manage.md) som använder datakolumner för att skapa kampanjer, annonsgrupper, nyckelord och/eller annonskopior för ett specifikt annonsnätverkskonto.

1. [Sprida feed-data via mallar](feed-data-propagate.md), som ersätter kolumnnamnen i mallen med data i filen eller kontot. Beroende på mallalternativen skapar Search, Social och Commerce antingen en ny kontostruktur (kampanjer, annonsgrupper, nyckelord) för annonserna med standardinställningar eller mappar annonserna till den befintliga kontostrukturen.

1. (Valfritt) [Förhandsgranska utdata](propagated-data-view.md) i [!UICONTROL Advanced (ACM)] vyer, och om du vill kan du visa en sammanfattning av dataändringarna i [!UICONTROL Propagations] -fliken.

1. [Bokför data](propagated-data-post.md) till relevanta annonsnätverkskonton.

1. (Om du använder FTP eller ett handelscenterkonto för att överföra dina data; (valfritt) När du har validerat utdata från den första feed-filen, [redigera parametrarna](feed-settings-manage.md#feed-data-settings) att automatiskt sprida efterföljande data via tillhörande mallar och lägga upp dem i relevanta annonsnätverk.

1. (När du har nya datafiler) Om det behövs överför du nya filer, sprider data via mallar och publicerar data i det relevanta annonsnätverket. Du kan också sprida och publicera data i ett enda steg.

>[!MORELIKETHIS]
>
>* [Automatisera och hantera lagerflöden](inventory-feeds-about.md)
>* [När skapas eller tas kontokomponenter bort av lagerfeeds?](when-are-components-created-deleted.md)

