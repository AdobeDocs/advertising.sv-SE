---
title: Konfigurera inställningar för feed-data
description: Lär dig hur du konfigurerar inställningar som styr hur feed-data bearbetas.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# Konfigurera inställningar för feed-data

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

Du kan konfigurera hur annonsgrupper, nyckelord och annonser ska hanteras i feed-datafiler och hur data i FTP-filer ska bearbetas specifikt via feed-inställningarna.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Settings]**.

1. Ange [inställningar för feed-data](#feed-data-settings):

   1. I [!UICONTROL Obsolete Item Auto-Processing] väljer du information i fälten.

   1. (Annonsörer som överför data via FTP eller via en direktlänk till ett handlarcenterkonto) På [!UICONTROL FTP/GMC Account Auto-Processing] väljer du information i fälten.

   1. I [!UICONTROL Miscellaneous Auto-Processing] väljer du information i fälten.

1. Klicka på **[!UICONTROL Save]**.

## Inställningar för matningsdata {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Använder alla [!UICONTROL Obsolete Item Auto-processing] inställningar till:

* *[!UICONTROL Ad Groups Only]:* Endast föråldrade annonsgrupper.

* *[!UICONTROL Keywords Only]:* Föråldrade nyckelord och produktgrupper.

* *[!UICONTROL Ad Variations Only]* (standard): Endast föråldrade annonser.

* *[!UICONTROL Keywords and Ad Variations]:* Både föråldrade nyckelord/produktmål/produktgrupper och föråldrade annonser.

>[!NOTE]
>
>* För [!DNL Google Ads] shoppingannonser, påverkas bara den lägsta produktgruppen.
>* För [!DNL Yandex] konton, föråldrade automatiska artikelbearbetningsuppgifter utförs alltid på annonsvariationer, oavsett den här inställningen.


**[!UICONTROL When the Scheduled End Date is reached]:** (Endast manuellt bokförda data) Vad du ska göra med radobjekt i en feed-fil som publicerats med ett angivet slutdatum och sluttid när sluttiden är inne:

* *[!UICONTROL Delete]* (standard): Ta bort alla relevanta komponenter när den angivna sluttiden anländer. Du kan inte ångra den här åtgärden.

* *[!UICONTROL Pause]:* Pausa alla relevanta komponenter när den angivna sluttiden anländer. Du kan återaktivera komponenterna senare om det behövs.

* *[!UICONTROL None]:* Ändra inte status för de relevanta komponenterna.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Vad du ska göra med befintliga objekt när de inte ingår i en ny feed-fil som har överförts manuellt eller när de inte mappar till befintliga kampanjer eller annonsgrupper enligt inställningarna för Endast karta i mallen:

* *[!UICONTROL Delete]:* Ta bort befintliga komponenter.

* *[!UICONTROL Pause]:* Pausa de befintliga komponenterna. De återaktiveras om en ny feed-fil innehåller något av samma radobjekt och de behåller sin historik och sina kvalitetspoäng. **Obs!** Om alla underordnade produktgrupper för en överordnad produktgrupp saknas tas den överordnade produktgruppen bort eftersom du inte kan pausa produktgrupper.

* *[!UICONTROL None]* (standard): Ändra inte befintliga komponenter.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Vad du ska göra med befintliga objekt när 1) de inte tas med a) i en ny feed-fil som har överförts till en FTP-katalog eller b) i ett handlarcenterkonto nästa gång som Sök, Socialt, &amp; Commerce synkroniseras med den, eller 2) när de inte mappar till befintliga kampanjer eller annonsgrupper per [!UICONTROL Map Only] inställningar i mallen.

* *[!UICONTROL Delete]:* Ta bort befintliga komponenter.

* *[!UICONTROL Pause]:* Pausa de befintliga komponenterna. De återaktiveras om nya data innehåller något av samma radobjekt och de behåller sin historik och kvalitetspoäng. **Obs!** Om alla underordnade produktgrupper för en överordnad produktgrupp saknas tas den överordnade produktgruppen bort eftersom du inte kan pausa produktgrupper.

* *[!UICONTROL None]* (standard): Ändra inte befintliga komponenter.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Så här gör du med radobjekt som innehåller en lagernivå:

* (För flöden med numeriska värden för stockar i den angivna kolumnen) Lagernivån är på eller under en angiven kvantitet. Standardkvantiteten är noll (0).

* (För feeds med textvärden i den angivna kolumnen) Värdet för [!UICONTROL Availability] är &quot;[!UICONTROL out of stock]&quot;; värdet inte är skiftlägeskänsligt. **Obs!** **Ange textbaserade spalter på Stock-nivå med kryssrutan för &quot;[!UICONTROL This column has non-numeric values].&quot;

Välj åtgärd för båda fallen:

* *[!UICONTROL Delete]* (standard) Ta bort komponenterna.

* *[!UICONTROL Pause]:* Pausa komponenterna. När data uppdateras återaktiveras komponenterna om de numeriska värdena för stocken ligger över den angivna kvantiteten eller om [!UICONTROL Availability] är &quot;[!UICONTROL in stock]&quot; eller &quot;[!UICONTROL preorder]&quot;. Komponenterna behåller sin historik och kvalitetspoäng.

Lagernivån för varje radobjekt kommer från en kolumn i feed-filen, enligt specifikationen i &quot;[!UICONTROL Stock Level]&quot; för varje mall.

>[!TIP]
>
>* För produkter och tjänster som du förväntar dig att återställa eller öka tillgängligheten för bör du pausa annonsgrupper, nyckelord och annonser i stället för att ta bort dem och återskapa dem. Genom att pausa kan de behålla sina kvalitetspoäng.
>* Om du aktiverar föråldrad automatisk bearbetning för annonsgrupper, och nya data innehåller en lagernivå för annonsgruppen, är det bra att ta bort eller pausa annonsgruppen endast när den angivna lagernivån finns på kategorinivån i stället för på varumärkes-/artikelnivå. Om du t.ex. har en annonsgrupp som&quot;konvertiblar&quot;, ska aktienivån för annonsgruppen vara summan för alla enskilda konvertibla modeller som representeras i annonsgruppen.


**[!UICONTROL Propagate feed data through all applicable templates]:** (Annonsörer som överför datafiler via FTP eller ett handlarcenterkonto) sprider automatiskt nya data via tillämpliga mallar. Alternativet är markerat som standard. Om du inaktiverar alternativet kan du fortfarande sprida data manuellt för alla feedsfiler, -konton eller -mallar.

>[!NOTE]
>
>* För FTP-filer söker flödestjänsten efter uppdateringar i FTP-katalogen varannan timme (jämnt numrerade timmar i PST-tidszonen). Med det här alternativet bearbetas alla filer som har överförts sedan den senaste kontrollen.
>* För handlarcenterkonton synkroniseras Search, Social och Commerce med kontot varje dag, ungefär 06:00 i annonsörens tidszon. Med det här alternativet bearbetas alla data som har uppdaterats sedan den senaste synkroniseringen.
>* Spridda data är tillgängliga från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] tills data har skickats till annonsnätverket eller till [!UICONTROL Bulksheets] vy.


**[!UICONTROL Post to the SE]:** (Annonsörer som överför datafiler via FTP eller ett handlande center-konto) Skapar automatiskt kalkylbladsfiler i rätt format för de relevanta annonsnätverken när nya data sprids via tillämpliga mallar. Det här alternativet tar även bort data från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar, såvida inte några underkomponenter har fel.

Det här alternativet är inaktiverat som standard. Om du vill aktivera det här alternativet markerar du kryssrutan och anger sedan om du vill publicera kalkylbladsfiler till annonsnätverken:

* *[!UICONTROL Immediately]* (standard): Skickar bulkbladsfilerna till relevanta annonsnätverk efter att data har spridits via mallarna. Mallartsfilerna är fortfarande tillgängliga i [!UICONTROL Bulksheets] i 30 dagar.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Bokför inte kalkylbladsfilerna i relevanta annonsnätverk utan visar dem i dialogrutan [!UICONTROL Bulksheets] där du kan publicera dem senare. Mallartsfilerna är fortfarande tillgängliga i [!UICONTROL Bulksheets] i 30 dagar. När kalkylbladsfilen är större än 10 MB men mindre än 2 GB är filen i ZIP-format. behöver du inte packa upp filen för att publicera den. **Tips:** Om du inte har validerat dina landningssidor tidigare kan du använda det här alternativet för att validera dem från [!UICONTROL Bulksheets] innan du skickar data till annonsnätverket.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Inkluderar publicering av nyckelordsfraser med fler än ett angivet antal ord till annonsnätverket. När det här alternativet är markerat sprids nyckelordsfraser med fler än det maximala antalet ord och visas på [!UICONTROL Keywords] men de bokförs inte när du försöker publicera data.

Det här alternativet är inaktiverat som standard så att alla nyckelord är publicerade, oavsett hur många ord frasen innehåller. Om du väljer det här alternativet väljer du det maximala antalet ord som ska bokföras (från 3-10).

>[!MORELIKETHIS]
>
>* [Om lagerflöden](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Sprida feed-data via mallar](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Posta kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)

