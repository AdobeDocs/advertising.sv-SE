---
title: När skapas eller tas kontokomponenter bort av lagerfeeds?
description: Lär dig vilka situationer som skapar och tar bort kontokomponenter när du bokför lagerfeeds.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# När skapas eller tas kontokomponenter bort av lagerfeeds?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

När en lagerflödesfil sprids via en mall skapas och tas kontokomponenter bort enligt följande.

>[!NOTE]
>
>Dubblerade annonser skapas aldrig i en annonsgrupp.

| Scenario | Exempel | Åtgärd |
|----|----|----|
| Feed-data innehåller ett nytt värde för en kolumn som används i ett kampanjnamn, annonsgruppsnamn, nyckelord eller produktgrupp. | Tidigare filer:<br>Campaign=Hats<br>Campaign=GLove<br><br>Ny fil:<br>Campaign=Shoes | En ny kampanj, annonsgrupp, nyckelord eller produktgrupp skapas om den inte finns i annonsnätverket. |
| Feed-data innehåller ett nytt värde för en kolumn som används i en annons. | Tidigare fil: En annons innehöll price=20<br><br>Ny fil: För samma annons, price=10 | När annonskopian för [!DNL Microsoft Advertising] expanderade textannonser, [!DNL Yahoo! Japan ads] eller [!DNL Yandex] annonser ändras, tas den befintliga annonsen bort och en ny skapas.<br><br>När annonskopia ändras för andra annonstyper eller när den tillämpliga kolumnen används för en [!DNL Google Ads] ad-parameter ({param1} eller {param2}) i en annons uppdateras den befintliga annonsen. |
| Mallinställningarna för kampanjen, annonsgruppen, nyckelordet eller produktgruppen har ändrats sedan den senaste spridningen. | Föregående inställning:Keyword=[Nyckelord]<br><br>Ny inställning: Nyckelord=&lt;Färg>[Nyckelord] | En ny kampanj, annonsgrupp, nyckelord eller produktgrupp skapas om den inte finns i annonsnätverket. |
| Mallinställningarna för en annons har ändrats sedan den senaste spridningen. | Föregående inställning: Ad description=&quot;Köp [kategori] nu.&quot;<br><br>Ny inställning: Ad description=&quot;Köp [brand] nu.&quot; | När annonskopian för [!DNL Microsoft Advertising] expanderade textannonser, [!DNL Yahoo! Japan ads] eller [!DNL Yandex] annonser ändras, tas den befintliga annonsen bort och en ny skapas.<br><br>När annonskopia ändras för andra annonstyper eller när ändringen reflekterar en ändring i kolumnen som används för en enskild [!DNL Google Ads] ad-parameter ({param1} eller {param2}) i en annons, uppdateras den befintliga annonsen. |
| Nya flödesuppgifter innehåller inte någon rad för en befintlig kampanj eller annonsgrupp. | n/a | Befintliga kampanjer och annonsgrupper håller sig i befintligt skick. |
| Nya matningsdata inkluderar inte en rad för en befintlig annonsgrupp, annons, nyckelord eller produktgrupp. | n/a | Den befintliga annonsgruppen, annonsen, nyckelordet eller produktgruppen förblir som den är, pausas eller tas bort enligt [feeddatainställningarna](feed-settings-manage.md#feed-data-settings). |
| Nya feed-data för en befintlig överordnad produktgrupp innehåller inte rader för dess befintliga underordnade produktgrupper. | n/a | Den befintliga överordnade produktgruppen behålls som den är eller tas bort enligt [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). <b>Obs!</b> Om feed-datainställningarna har konfigurerats för att pausa saknade radobjekt tas den överordnade produktgruppen fortfarande bort eftersom du inte kan pausa produktgrupper. |
| Nya feed-data innehåller en rad för en annonsgrupp, annons, nyckelord eller produktgrupp som var a) i tidigare data men b) har utelämnats sedan dess och pausats enligt [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). | n/a | Den befintliga annonsgruppen, annonsen, nyckelordet eller produktgruppen återaktiveras utan att någon historik eller kvalitetspoäng går förlorad. |
| Nya feed-data innehåller en rad för en annonsgrupp, annons, nyckelord eller produktgrupp som var a) i tidigare data men b) har uteslutits sedan dess och har tagits bort enligt [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). | n/a | En ny annonsgrupp, annons, nyckelord eller produktgrupp skapas. |
| Du har inaktiverat alternativet på kampanj- eller annonsgruppnivå till [!UICONTROL Delete negative keywords when omitted from list]. | Listan med negativa nyckelord innehåller&quot;soffa&quot; och&quot;sportbil&quot;.<br><br>Annonsgruppen innehåller redan det negativa nyckelordet SUV. | Eventuella negativa nyckelord som inte finns med i listan behålls som de är. |
| Du har aktiverat alternativet på kampanj- eller annonsgruppnivå till [!UICONTROL Delete negative keywords when omitted from list], och negativa nyckelord som inte finns med i listan finns. | Listan med negativa nyckelord innehåller&quot;soffa&quot; och&quot;sportbil&quot;.<br><br>Annonsgruppen innehåller redan det negativa nyckelordet SUV. | Alla ospecificerade negativa nyckelord som tidigare skapats med mallen tas bort när en feed-fil sprids via mallen. Alla ospecificerade negativa nyckelord som har skapats på andra sätt (till exempel i oformaterade kalkylblad, [!UICONTROL Campaigns]-vyer eller i annonsnätverkets annonsredigerare) behålls som de är. |
| Det schemalagda slutdatumet för komponenterna i en bokförd feed-fil inträffar. | n/a | Befintliga kampanjer förblir i befintligt skick. De befintliga annonsgrupperna, annonserna och nyckelorden förblir som de är, pausas eller tas bort enligt [feeddatainställningarna](feed-settings-manage.md#feed-data-settings). |
| Lagernivån för ett objekt sjunker under ett minimum som anges i [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). | Föregående fil: stock=10<br><br>Ny fil: stock=0 | Befintliga kampanjer förblir i befintligt skick. Befintliga annonsgrupper, annonser, nyckelord och produktgrupper pausas eller tas bort enligt [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). |
| Lagernivån för ett objekt går tillbaka över ett minimum som anges i [feed-datainställningarna](feed-settings-manage.md#feed-data-settings). | Föregående fil: stock=0<br><br> Ny fil: stock=10 | När de befintliga annonserna, nyckelorden eller produktgrupperna pausas återaktiveras de utan att någon historik eller kvalitetspoäng går förlorad. När det inte finns några annonser, nyckelord eller produktgrupper (om de till exempel togs bort tidigare eftersom lagernivån var under miniminivån) skapas nya. |

>[!MORELIKETHIS]
>
>* [Om automatisering av annonshantering med lagerflöden](inventory-feeds-about.md)
