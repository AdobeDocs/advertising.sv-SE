---
title: Automatisera och hantera lagerflöden
description: Lär dig mer om avancerad kampanjhantering, som gör att ni automatiskt kan hantera kontostrukturen och leverera dynamiska annonser baserade på data om er produkt- eller serviceartikeln.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Automatisera och hantera lagerflöden

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Med vyn [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] för avancerad kampanjhantering kan du automatiskt skapa och uppdatera strukturen för annonsnätverkskonton och leverera dynamiska annonser baserade på data om produkten eller tjänsteinventeringen. Du kan överföra nya filer med produktdata dagligen eller så ofta du vill, eller länka direkt till ett [!DNL Google]- eller [!DNL Microsoft]-handelscenterkonto. Använd funktionen för att:

* Skapa nya kampanjer från beställda datakällor.

* Uppdatera text och responsiva sökannonser, [!DNL Google Ads] shoppingannonser eller [!DNL Microsoft Advertising] shoppingannonser dynamiskt när nya data bearbetas, med hjälp av dynamiska variabler för ändringsbara dataelement (som pris eller kvantitet). Varje gång du ändrar data tas befintliga annonser bort och nya skapas.

* Pausa eller ta bort annonsgrupper, nyckelord och annonser automatiskt när Stock går under en viss nivå enligt ett visst slutdatum eller när en befintlig komponent utelämnas från matningsdata.

Om du vill konfigurera dina annonser skapar du lagerflödesmallar som innehåller variabler (platshållare) och ersätter variablerna med faktiska datakolumner från en överförd fil eller ett [Google- eller Microsoft-handelscenterkonto som synkroniseras](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Variablerna kan även innehålla modifieringsgrupper som du ställer in i en fil eller enskilda rader i filen för att skapa flera annonser, nyckelord, kampanjer eller annonsgrupper för varje tillämplig rad i datafilen. Om du till exempel använder en modifierargruppvariabel i en annonsrubrik och modifierargruppen innehåller två modifierare (&quot;för billigt&quot; och&quot;för rabatt&quot;) skapas två separata annonser för varje produkt - en för varje modifierare. För [!DNL Google Ads] och [!DNL Microsoft Advertising] dynamiska sökannonser kan du även inkludera värden för annonsanpassare.

| [!UICONTROL Ad Variation]-avsnitt i mallen | Modifierare i Search, Social och Commerce | Feed Contents | Resulterande annonser |
|----|----|----|----|
| Titel: Köp avancerad \<i>produktkategori</i>\&rbrace; &lt;<i>CheapList</i>>.<br><br>Beskrivning 1: Mycket stort lager av \<i>Produktnamn</i>\&rbrace;.<br><br>Beskrivning 2: Finns i \<i>Rabattprocent</i>\&rbrace;% rabatt. | Värden för modifieringsgruppen CheapList:<br><br> för billig <br><br> till rabatt | Produktkategori,Produktnamn,Rabattprocent<br>elektronik,iPod,10<br><br>kläder,Leveranser,15<br><br><b>Obs!</b> Du kan separera värden med kommatecken eller tabbar. | <u>Köp avancerad elektronik till ett lågt pris.</u><br>Omfattande inventering av surfplattor. 10 % rabatt.<br><br><u>Köp avancerad elektronik till rabatterat pris.</u><br>Omfattande inventering av surfplattor. 10 % rabatt.<br><br><u>Köp avancerade kläder till ett lågt pris.</u><br>Omfattande antal skjortor. 15 % rabatt.<br><br><u>Köp avancerade kläder till rabatterat pris.</u><br>Omfattande antal skjortor. 15 % rabatt. |

När ni har skapat annonserna kan ni granska dem och sedan lägga upp dem i annonsnätverket.

>[!NOTE]
>Mer information om hur du skapar eller redigerar kampanjdata i grupp med kalkylbladsfiler finns i [Hantera kampanjdata med hjälp av kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

## Arbetsflöde för att hantera kampanjdata med lagerflöden

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Testa först minst en feed-fil eller ett konto och sedan kan du automatisera processen helt eller fortsätta att styra den i varje steg:

1. (Valfritt) Kontakta kontoteamet på Adobe för att skapa en FTP-katalog för insättning av datafiler.

   Om du använder FTP-katalogen söker flödestjänsten efter nya filer varannan timme.

   I annat fall kan du överföra filer manuellt i vyn [!UICONTROL Advanced (ACM)].

1. Ange [parametrar för bearbetning av feed-data](feed-settings-manage.md#feed-data-settings).

   Om du använder FTP ska du inte automatiskt lägga upp data i annonsnätverken från början. När du har verifierat utdata från den första filen och är nöjd med resultatet kan du ändra inställningarna.

1. Överför en datafil till FTP-katalogen, [överför en datafil manuellt](feed-files-manage.md) i [!UICONTROL Advanced (ACM) view] eller [aktiverar åtkomst till ett handelscentkonto för Google eller Microsoft](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Om du vill överföra filer manuellt kan du vänta tills du skapar en mall som använder datafilen.

1. (Valfritt) Skapa grupper med [modifierare](modifiers-manage.md) som ska användas som variabler i olika datafält i flödesdatamallar.

1. [Skapa en eller flera mallar](ad-templates/ad-template-manage.md) som använder datakolumnerna för att skapa kampanjer, annonsgrupper, nyckelord och/eller annonskopior för ett specifikt annonsnätverkskonto.

1. [Sprid feed-data via mallarna](feed-data-propagate.md), som ersätter kolumnnamnen i mallen med data i filen eller kontot. Beroende på mallalternativen skapar Search, Social och Commerce antingen en ny kontostruktur (kampanjer, annonsgrupper, nyckelord) för annonserna med standardinställningar eller mappar annonserna till den befintliga kontostrukturen.

1. (Valfritt) [Förhandsgranska utdata](propagated-data-view.md) i [!UICONTROL Advanced (ACM)]-vyerna och eventuellt visa en sammanfattning av dataändringarna på fliken [!UICONTROL Propagations].

1. [Bokför data](propagated-data-post.md) på relevanta annonsnätverkskonton.

1. (Om du använder FTP eller ett handlarcenterkonto för att överföra dina data (valfritt) När du har validerat utdata från den första feeden [redigerar du parametrarna](feed-settings-manage.md#feed-data-settings) för att automatiskt sprida efterföljande data via de associerade mallarna och publicerar dem i relevanta annonsnätverk.

1. (När du har nya datafiler) Om det behövs överför du nya filer, sprider data via mallar och publicerar data i det relevanta annonsnätverket. Du kan också sprida och publicera data i ett enda steg.

>[!MORELIKETHIS]
>
>* [När skapas eller tas kontokomponenter bort av lagerfeeds?](when-are-components-created-deleted.md)
