---
title: Automatisera och hantera lagerflöden
description: Lär dig mer om avancerad kampanjhantering, som gör att ni automatiskt kan hantera kontostrukturen och leverera dynamiska annonser baserade på data om er produkt- eller serviceartikeln.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Automatisera och hantera lagerflöden

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

The [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] för avancerad kampanjhantering kan ni automatiskt skapa och uppdatera kontostrukturen för annonsnätverk och leverera dynamiska annonser baserade på data om er produkt- eller servicearkiv. Du kan överföra nya filer med produktdata dagligen eller så ofta du vill, eller länka direkt till en [!DNL Google] eller [!DNL Microsoft®] handlant center-konto. Använd funktionen för att:

* Skapa nya kampanjer från beställda datakällor.

* Dynamisk uppdatering av text och responsiva sökannonser, [!DNL Google Ads] shoppingannonser, eller [!DNL Microsoft® Advertising] shoppingannonser när nya data bearbetas, med hjälp av dynamiska variabler för ändringsbara dataelement (som pris eller kvantitet). Varje gång du ändrar data tas befintliga annonser bort och nya skapas.

* Pausa eller ta bort annonsgrupper, nyckelord och annonser automatiskt när Stock går under en viss nivå enligt ett visst slutdatum eller när en befintlig komponent utelämnas från matningsdata.

Om du vill konfigurera dina annonser skapar du lagerflödesmallar som innehåller variabler (platshållare) och ersätter variablerna med faktiska datakolumner från en överförd fil eller en [Google- eller Microsoft®-handlarcenterkonto som synkroniseras](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Variablerna kan även innehålla modifieringsgrupper som du ställer in i en fil eller enskilda rader i filen för att skapa flera annonser, nyckelord, kampanjer eller annonsgrupper för varje tillämplig rad i datafilen. Om du till exempel använder en modifierargruppvariabel i en annonsrubrik och modifierargruppen innehåller två modifierare (&quot;för billigt&quot; och&quot;för rabatt&quot;) skapas två separata annonser för varje produkt - en för varje modifierare. För [!DNL Google Ads] och [!DNL Microsoft® Advertising] dynamiska sökannonser kan du även inkludera värden för annonsanpassare.

| [!UICONTROL Ad Variation] Avsnitt i mall | Modifierare inom sökning, sociala medier och handel | Feed Contents | Resulterande annonser |
|----|----|----|----|
| Titel: Köp avancerad \{<i>Produktkategori</i>\} &lt;<i>CheapList</i>>.<br><br>Beskrivning 1: Mycket stora lager av \{<i>Produktnamn</i>\}.<br><br>Beskrivning 2: Finns på \{<i>Rabattprocent</i>\} % rabatt. | Värden för modifierargruppen &quot;CheapList&quot;:<br><br>&quot;för billigt&quot;<br><br>&quot;till rabatterat pris&quot; | Produktkategori,produktnamn,rabattprocent<br>elektronik, iPod, 10<br><br>kläder,sköldpaddor,15<br><br><b>Obs!</b> Du kan separera värden med kommatecken eller tabbar. | <u>Köp avancerad elektronik till ett lågt pris.</u><br>Omfattande inventering av surfplattor. 10 % rabatt.<br><br><u>Köp avancerad elektronik till rabatterat pris.</u><br>Omfattande inventering av surfplattor. 10 % rabatt.<br><br><u>Köp avancerade kläder till ett lågt pris.</u><br>Enorma skjortor. 15 % rabatt.<br><br><u>Köp avancerade kläder till rabatterat pris.</u><br>Enorma skjortor. 15 % rabatt. |

När ni har skapat annonserna kan ni granska dem och sedan lägga upp dem i annonsnätverket.

>[!NOTE]
>Om du vill skapa eller redigera kampanjdata i grupp med kalkylbladsfiler, se &quot;[Hantera kampanjdata med hjälp av kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Arbetsflöde för att hantera kampanjdata med lagerflöden](inventory-feeds-workflow.md)
>* [När skapas eller tas kontokomponenter bort av lagerfeeds?](when-are-components-created-deleted.md)

