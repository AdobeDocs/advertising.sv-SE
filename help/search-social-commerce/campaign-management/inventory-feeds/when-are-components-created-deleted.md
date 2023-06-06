---
title: När skapas eller tas kontokomponenter bort av lagerfeeds?
description: Lär dig vilka situationer som skapar och tar bort kontokomponenter när du bokför lagerfeeds.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# När skapas eller tas kontokomponenter bort av lagerfeeds?

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

När en lagerflödesfil sprids via en mall skapas och tas kontokomponenter bort enligt följande.

>[!NOTE]
>
>Dubblerade annonser skapas aldrig i en annonsgrupp.

| Scenario | Exempel | Åtgärd |
|----|----|----|
| Feed-data innehåller ett nytt värde för en kolumn som används i ett kampanjnamn, annonsgruppsnamn, nyckelord eller produktgrupp. | Tidigare filer:<br>Campaign=Hats<br>Campaign=Handskar<br><br>Ny fil:<br>Campaign=Shoes | En ny kampanj, annonsgrupp, nyckelord eller produktgrupp skapas om den inte finns i annonsnätverket. |
| Feed-data innehåller ett nytt värde för en kolumn som används i en annons. | Föregående fil: En annons med pris=20<br><br>Ny fil: För samma annons, price=10 | När annonskopia för [!DNL Microsoft® Advertising] expanderade textannonser, [!DNL Yahoo! Japan ads], eller [!DNL Yandex] annonser ändras, den befintliga annonsen tas bort och en ny skapas.<br><br>När annonskopia ändras för andra annonstyper eller när tillämplig kolumn används för en [!DNL Google Ads] annonsparametern ({param1} eller {param2}) i en annons, då uppdateras den befintliga annonsen. |
| Mallinställningarna för kampanjen, annonsgruppen, nyckelordet eller produktgruppen har ändrats sedan den senaste spridningen. | Föregående inställning:Nyckelord=[Nyckelord]<br><br>Ny inställning: Nyckelord=&lt;color>[Nyckelord] | En ny kampanj, annonsgrupp, nyckelord eller produktgrupp skapas om den inte finns i annonsnätverket. |
| Mallinställningarna för en annons har ändrats sedan den senaste spridningen. | Föregående inställning: Ad description=&quot;Buy [kategori] nu.&quot;<br><br>Ny inställning: Ad description=&quot;Buy [varumärke] nu.&quot; | När annonskopia för [!DNL Microsoft® Advertising] expanderade textannonser, [!DNL Yahoo! Japan ads], eller [!DNL Yandex] annonser ändras, den befintliga annonsen tas bort och en ny skapas.<br><br>När en annonskopia ändras för andra annonstyper eller när ändringen visar en ändring i kolumnen som används för en enskild [!DNL Google Ads] annonsparametern ({param1} eller {param2}) i en annons, då uppdateras den befintliga annonsen. |
| Nya flödesuppgifter innehåller inte någon rad för en befintlig kampanj eller annonsgrupp. | n/a | Befintliga kampanjer och annonsgrupper håller sig i befintligt skick. |
| Nya matningsdata inkluderar inte en rad för en befintlig annonsgrupp, annons, nyckelord eller produktgrupp. | n/a | Den befintliga annonsgruppen, annonsen, nyckelordet eller produktgruppen förblir som den är, är pausad eller tas bort enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). |
| Nya feed-data för en befintlig överordnad produktgrupp innehåller inte rader för sina befintliga underordnade produktgrupper. | n/a | Den befintliga överordnade produktgruppen förblir oförändrad eller tas bort enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). <b>Obs!</b> Om matningsdatainställningarna har konfigurerats för att pausa saknade radartiklar tas den överordnade produktgruppen fortfarande bort eftersom du inte kan pausa produktgrupper. |
| Nya matningsdata innehåller en rad för en annonsgrupp, annons, nyckelord eller produktgrupp som var a) i tidigare data men b) har utelämnats sedan dess och har pausats enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). | n/a | Den befintliga annonsgruppen, annonsen, nyckelordet eller produktgruppen återaktiveras utan att någon historik eller kvalitetspoäng går förlorad. |
| Nya matningsdata innehåller en rad för en annonsgrupp, annons, nyckelord eller produktgrupp som var a) i tidigare data men b) har uteslutits sedan dess och har tagits bort enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). | n/a | En ny annonsgrupp, annons, nyckelord eller produktgrupp skapas. |
| Du har inaktiverat alternativet på kampanj- eller annonsgruppnivå för att[!UICONTROL Delete negative keywords when omitted from list].&quot; | Listan med negativa nyckelord innehåller&quot;soffa&quot; och&quot;sportbil&quot;.<br><br>Annonsgruppen innehåller redan det negativa nyckelordet &quot;SUV&quot;. | Eventuella negativa nyckelord som inte finns med i listan behålls som de är. |
| Du har aktiverat alternativet på kampanj- eller annonsgruppnivå för att[!UICONTROL Delete negative keywords when omitted from list]och negativa nyckelord som inte finns med i listan finns. | Listan med negativa nyckelord innehåller&quot;soffa&quot; och&quot;sportbil&quot;.<br><br>Annonsgruppen innehåller redan det negativa nyckelordet &quot;SUV&quot;. | Alla ospecificerade negativa nyckelord som tidigare skapats med mallen tas bort när en feed-fil sprids via mallen. Alla ospecificerade negativa nyckelord som skapas på andra sätt (t.ex. i vanliga glödlampor, [!UICONTROL Campaigns] eller i annonsnätverkets annonsredigerare). |  | Det schemalagda slutdatumet för komponenterna i en bokförd feed-fil inträffar. | n/a | Befintliga kampanjer förblir i befintligt skick. Befintliga annonsgrupper, annonser och nyckelord förblir oförändrade, pausas eller tas bort enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). |
| Lagernivån för en artikel sjunker under ett minimum som anges i [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). | Föregående fil: stock=10<br><br>Ny fil: stock=0 | Befintliga kampanjer förblir i befintligt skick. Befintliga annonsgrupper, annonser, nyckelord och produktgrupper pausas eller tas bort enligt [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). |
| Lagernivån för en artikel går tillbaka över ett minimivärde som anges i [inställningar för feed-data](feed-settings-manage.md#feed-data-settings). | Föregående fil: stock=0<br><br> Ny fil: stock=10 | När de befintliga annonserna, nyckelorden eller produktgrupperna pausas återaktiveras de utan att någon historik eller kvalitetspoäng går förlorad. När det inte finns några annonser, nyckelord eller produktgrupper (om de till exempel togs bort tidigare eftersom lagernivån var under miniminivån) skapas nya. |

>[!MORELIKETHIS]
>
>* [Automatisera och hantera lagerflöden](inventory-feeds-about.md)
>* [Arbetsflöde för att hantera kampanjdata med lagerflöden](inventory-feeds-workflow.md)

