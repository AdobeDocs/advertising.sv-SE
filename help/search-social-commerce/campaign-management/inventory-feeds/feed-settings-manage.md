---
title: Konfigurera inställningar för feed-data
description: Lär dig hur du konfigurerar inställningar som styr hur feed-data bearbetas.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Konfigurera inställningar för feed-data

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Du kan konfigurera hur annonsgrupper, nyckelord och annonser ska hanteras i feed-datafiler och hur data i FTP-filer ska bearbetas specifikt via feed-inställningarna.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på **[!UICONTROL Settings]** i verktygsfältet ovanför datatabellen.

1. Ange [feed-datainställningarna](#feed-data-settings):

   1. Välj information i fälten i avsnittet [!UICONTROL Obsolete Item Auto-Processing].

   1. (Annonsörer som överför data via FTP eller via en direktlänk till ett handlarcenterkonto) I avsnittet [!UICONTROL FTP/GMC Account Auto-Processing] väljer du information i fälten.

   1. Välj information i fälten i avsnittet [!UICONTROL Miscellaneous Auto-Processing].

1. Klicka på **[!UICONTROL Save]**.

## Inställningar för matningsdata {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Tillämpar alla [!UICONTROL Obsolete Item Auto-processing]-inställningar på:

* *[!UICONTROL Ad Groups Only]:* Endast föråldrade annonsgrupper.

* *[!UICONTROL Keywords Only]:* Endast inaktuella nyckelord och produktgrupper.

* *[!UICONTROL Ad Variations Only]* (standard): Endast föråldrade annonser.

* *[!UICONTROL Keywords and Ad Variations]:* Både inaktuella nyckelord/produktmål/produktgrupper och inaktuella annonser.

>[!NOTE]
>
>* För [!DNL Google Ads] shoppingannonser påverkas bara den lägsta produktgruppen.
>* För [!DNL Yandex]-konton utförs alltid föråldrade uppgifter för automatisk bearbetning av objekt på annonsvariationer, oavsett den här inställningen.

**[!UICONTROL When the Scheduled End Date is reached]:** (Endast manuellt bokförda data) Vad du ska göra med radartiklar i en feed-fil som har publicerats med ett angivet slutdatum och sluttid när sluttiden är inne:

* *[!UICONTROL Delete]* (standardvärdet): Ta bort alla relevanta komponenter när den angivna sluttiden anländer. Du kan inte ångra den här åtgärden.

* *[!UICONTROL Pause]:* Pausa alla relevanta komponenter när den angivna sluttiden anländer. Du kan återaktivera komponenterna senare om det behövs.

* *[!UICONTROL None]:* Ändra inte status för relevanta komponenter.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Så här gör du med befintliga objekt när de inte ingår i en ny feed-fil som har överförts manuellt eller när de inte mappar till befintliga kampanjer eller annonsgrupper enligt inställningarna för Endast karta i mallen:

* *[!UICONTROL Delete]:* Ta bort befintliga komponenter.

* *[!UICONTROL Pause]:* Pausa befintliga komponenter. De återaktiveras om en ny feed-fil innehåller något av samma radobjekt och de behåller sin historik och sina kvalitetspoäng. **Obs!** Om alla underordnade produktgrupper för en överordnad produktgrupp saknas tas den överordnade produktgruppen bort eftersom du inte kan pausa produktgrupper.

* *[!UICONTROL None]* (standard): Ändra inte befintliga komponenter.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Vad du ska göra med befintliga objekt när 1) de inte ingår som a) i en ny feed-fil som har överförts till en FTP-katalog eller b) i ett handlarcenterkonto nästa gång som Search, Social, &amp; Commerce synkroniseras med den, eller 2) när de inte mappar till befintliga kampanjer eller annonsgrupper enligt [!UICONTROL Map Only] -inställningarna i mallen.

* *[!UICONTROL Delete]:* Ta bort befintliga komponenter.

* *[!UICONTROL Pause]:* Pausa befintliga komponenter. De återaktiveras om nya data innehåller något av samma radobjekt och de behåller sin historik och kvalitetspoäng. **Obs!** Om alla underordnade produktgrupper för en överordnad produktgrupp saknas tas den överordnade produktgruppen bort eftersom du inte kan pausa produktgrupper.

* *[!UICONTROL None]* (standard): Ändra inte befintliga komponenter.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Vad du ska göra med radobjekt som innehåller en lagernivå när:

* (För flöden med numeriska värden för stockar i den angivna kolumnen) Lagernivån är på eller under en angiven kvantitet. Standardkvantiteten är noll (0).

* (För feeds med textvärden i den angivna kolumnen) Värdet för [!UICONTROL Availability] är [!UICONTROL out of stock]. Värdet är inte skiftlägeskänsligt. **Obs!** **I feedelsmallar anger du textbaserade Stock-nivåkolumner med kryssrutan för [!UICONTROL This column has non-numeric values].

Välj åtgärd för båda fallen:

* *[!UICONTROL Delete]* (standard) Ta bort komponenterna.

* *[!UICONTROL Pause]:* Pausa komponenterna. När data uppdateras återaktiveras komponenterna om de numeriska börsvärdena överstiger den angivna kvantiteten eller om [!UICONTROL Availability] är [!UICONTROL in stock] eller [!UICONTROL preorder]. Komponenterna behåller sin historik och kvalitetspoäng.

Lagernivån för varje radobjekt kommer från en kolumn i feed-filen, enligt vad som anges i fältet [!UICONTROL Stock Level] för varje mall.

>[!TIP]
>
>* För produkter och tjänster som du förväntar dig att återställa eller öka tillgängligheten för bör du pausa annonsgrupper, nyckelord och annonser i stället för att ta bort dem och återskapa dem. Genom att pausa kan de behålla sina kvalitetspoäng.
>* Om du aktiverar föråldrad automatisk bearbetning för annonsgrupper, och nya data innehåller en lagernivå för annonsgruppen, är det bra att ta bort eller pausa annonsgruppen endast när den angivna lagernivån finns på kategorinivån i stället för på varumärkes-/artikelnivå. Om du t.ex. har en annonsgrupp som&quot;konvertiblar&quot;, ska aktienivån för annonsgruppen vara summan för alla enskilda konvertibla modeller som representeras i annonsgruppen.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Advertisers överför datafiler via FTP eller ett handlancenter-konto) Sprider automatiskt nya data via tillämpliga mallar. Alternativet är markerat som standard. Om du inaktiverar alternativet kan du fortfarande sprida data manuellt för alla feedsfiler, -konton eller -mallar.

>[!NOTE]
>
>* För FTP-filer söker flödestjänsten efter uppdateringar i FTP-katalogen varannan timme (jämnt numrerade timmar i PST-tidszonen). Med det här alternativet bearbetas alla filer som har överförts sedan den senaste kontrollen.
>* För handlarcenterkonton synkroniseras Search, Social och Commerce med kontot varje dag, ungefär 06:00 i annonsörens tidszon. Med det här alternativet bearbetas alla data som har uppdaterats sedan den senaste synkroniseringen.
>* Spridda data är tillgängliga från flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads] tills data har publicerats i annonsnätverket eller i vyn [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (Advertisers överför datafiler via FTP eller ett handlancenter-konto) Skapar automatiskt kalkylbladsfiler i rätt format för relevanta annonsnätverk efter att nya data har spridits via tillämpliga mallar. Det här alternativet tar också bort data från flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads], såvida inte några underkomponenter innehåller fel.

Det här alternativet är inaktiverat som standard. Om du vill aktivera det här alternativet markerar du kryssrutan och anger sedan om du vill publicera kalkylbladsfiler till annonsnätverken:

* *[!UICONTROL Immediately]* (standard): Skickar satsbladsfilerna till relevanta annonsnätverk efter att data har spridits via mallarna. Kolumnmallsfilerna är fortfarande tillgängliga i vyn [!UICONTROL Bulksheets] i 30 dagar.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Bokför inte kalkylbladsfilerna i relevanta annonsnätverk, men visar dem i vyn [!UICONTROL Bulksheets], som du kan publicera dem från senare. Kolumnmallsfilerna är fortfarande tillgängliga i vyn [!UICONTROL Bulksheets] i 30 dagar. När kalkylbladsfilen är större än 10 MB men mindre än 2 GB är filen i ZIP-format. Du behöver inte packa upp filen för att kunna publicera den. **Tips!** Om du inte tidigare har validerat dina landningssidor kan du använda det här alternativet för att validera dem från [!UICONTROL Bulksheets]-vyn innan du publicerar data i annonsnätverket.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Inkluderar publicering av nyckelordsfraser med fler än ett angivet antal ord till annonsnätverket. När det här alternativet är markerat sprids och visas nyckelordsfraser med fler än det maximala antalet ord på fliken [!UICONTROL Keywords], men de registreras inte när du försöker publicera data.

Det här alternativet är inaktiverat som standard så att alla nyckelord är publicerade, oavsett hur många ord frasen innehåller. Om du väljer det här alternativet väljer du det maximala antalet ord som ska bokföras (från 3-10).

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Sprid feed-data via mallar](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
