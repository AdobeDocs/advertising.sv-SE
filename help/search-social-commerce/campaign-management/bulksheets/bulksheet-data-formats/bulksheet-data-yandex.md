---
title: Obligatoriska kalkylbladsdata för  [!DNL Yandex] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för  [!DNL Yandex] konton.
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# Bilaga - Obligatoriska balansräkningsdata för [!DNL Yandex]-konton

Om du vill skapa och uppdatera [!DNL Yandex]-kampanjdata i grupp kan du använda skalkylbladsfiler för sökning, sociala medier och Commerce som är särskilt formaterade för [!DNL Yandex]-konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det filformat som krävs eller b) skapa dem manuellt (mer information om vilka filformat som stöds finns i [Filformat som stöds i bulkblad](bulksheet-file-formats.md)).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Tillgängliga datafält

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>Följande tabell är bred. Om du vill utöka visningsområdet kan du tillfälligt dölja innehållsförteckningen och den högra rutan genom att klicka på ![Dölj den vänstra rutan](/help/dsp/assets/hide-left-pane.png "Dölj den vänstra rutan") högst upp i den vänstra rutan och ![Dölj den högra rutan](/help/dsp/assets/hide-right-pane.png "Dölj den högra rutan") längst upp i den högra rutan. Du kan också använda rullningslisten längst ned i tabellen för att visa hela innehållet.

| Fält | Campaign | Annonsgrupp | Nyckelord | Text Ad | Webblänk | Beskrivning |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Acct Name] | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Obligatoriskt/valfritt | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt | Obligatoriskt | Obligatoriskt | Obligatoriskt | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Campaign Start Date] | Obligatoriskt: Skapa<br>Valfritt: Redigera eller ta bort | n/a | n/a | n/a | n/a | Det första datum då anbud kan lämnas för en kampanj, i annonsörens tidszon och i något av följande format: m/d/yyyy, m/d/yy, m-d-yyyy eller m-d-yy. Standardinställningen för nya kampanjer är den aktuella dagen. |
| [!UICONTROL Campaign Budget] | Obligatoriskt: Skapa<br>Valfritt: Redigera eller ta bort | n/a | n/a | n/a | n/a | En gräns för kampanjens livslängd, med eller utan monetära symboler och interpunktion. |
| [!UICONTROL Delivery Method] | Obligatoriskt: Skapa<br>Valfritt: Redigera eller ta bort | n/a | n/a | n/a | n/a | Så här visar du annonser för kampanjen varje dag:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (standard för nya kampanjer): För att sprida annonsintrycken över dagen.</li><li><i>[!UICONTROL Accelerated]:</i> Om du vill visa dina annonser så ofta som möjligt tills din budget är nådd. Därför kanske era annonser inte visas senare under dagen.</li></ul> |
| [!UICONTROL Ad Group Name] | n/a | Obligatoriskt | Obligatoriskt | Obligatoriskt | n/a | Annonsgruppen. |
| [!UICONTROL Ad Title] | n/a | n/a | n/a | Obligatoriskt | n/a | Banderollens rubrik (ad). Maxlängden är 33 tecken och ett ord får inte innehålla fler än 23 tecken.<br><br><b>Obs!</b> Om du ändrar annonskopian tas den befintliga annonsen bort och en ny skapas. |
| [!UICONTROL Ad Description] | n/a | n/a | n/a | Obligatoriskt | n/a | Banderollens brödtext (ad). Maxlängden är 75 tecken och ett ord får inte vara längre än 22 tecken.<br><br><b>Obs!</b> Om du ändrar annonskopian tas den befintliga annonsen bort och en ny skapas. |
| [!UICONTROL Base URL] | n/a | n/a | Valfritt | Obligatoriskt | n/a | URL:en till landningssidan som slutanvändarna tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Maximala längden är 1 024 tecken, inklusive protokollet.<br><br>Bas/slut-URL:er på nyckelordsnivå åsidosätter URL:er på annonsnivå och högre. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte, inte i annonsnätverket) För konton med mål-URL:er är det här värdet den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och Commerce. Om du genererade spårnings-URL:er baseras det här värdet på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till nätverksspecifika parametrar kan de ersättas med motsvarande parametrar för Search, Social och Commerce. |
| [!UICONTROL SiteLink Title] | n/a | n/a | n/a | n/a | Obligatoriskt | Sitelink-texten. För nya sitelinks inkluderar du kampanjnamnet i sitelink-raden. För sitelinks på annonsgruppnivå eller annonsnivå ska även annonsgruppens namn eller annonsens rubrik och text anges.<br><br><b>Obs!</b> Du kan ha upp till fyra sitelinks. |
| [!UICONTROL SiteLink Base URL] | n/a | n/a | n/a | n/a | Obligatoriskt | Bas-URL:en för en sitelink. Den måste vara bannerns bas-URL. Se [!UICONTROL Base URL]. |
| [!UICONTROL SiteLink Destination URL] | n/a | n/a | n/a | n/a | n/a | Mål-URL:en för en sitelink. Den måste vara mål-URL:en för banderollen. Se [!UICONTROL Destination URL]. |
| [!UICONTROL Keyword] | Valfri/ingen/a | n/a | Obligatoriskt | n/a | n/a | Frasen (nyckelordssträng). En annons måste ha minst en fras. Varje nyckelord kan ha högst sju ord, med undantag för stoppord.<br><br><b>Anteckningar:</b><ul><li>Om du vill exkludera en fras på kampanjnivå anger du [!UICONTROL Match Type] till [!UICONTROL Negative].</li><li>Om du ändrar en fras tas den befintliga frasen bort och en ny skapas.</li><li>Om du ändrar en [!DNL Yandex]-nyckelordsfras eller matchningstyp tas den befintliga nyckelordsfrasen bort och en ny skapas.</li></ul> |
| [!UICONTROL Max CPC] | n/a | Obligatoriskt: Skapa<br>Valfritt: Redigera eller ta bort | Valfritt | n/a | n/a | Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för en banderoll (och) klicka på söknätverket, med eller utan monetära symboler och interpunktion. Du kan ange värden för annonsgrupper och nyckelord. Standardvärdet för ett nytt nyckelord ärvs från annonsgruppsnivån. |
| [!UICONTROL Match Type] | Valfri/ingen/a | n/a | Valfritt: Skapa<br>krävs/Valfritt: Redigera eller ta bort | n/a | n/a | Nyckelordsmatchningsalternativet för frasen: <i>[!UICONTROL Content]</i> eller <i>[!UICONTROL Search]</i>. Definiera negativa nyckelord med kolumnen [!UICONTROL Negative Keywords].<br><br><b>Obs!</b> Om du ändrar en [!DNL Yandex] -nyckelordsfras eller matchningstyp tas den befintliga nyckelordsfrasen bort och en ny skapas. |
| [!UICONTROL Search Network Status] | Valfritt | n/a | n/a | n/a | n/a | Om annonser ska placeras i söknätverket: <i>[!UICONTROL Yes]</i> (standard) eller <i>[!UICONTROL No]</i>. |
| Nätverksstatus för innehåll | Valfritt | n/a | n/a | n/a | n/a | Anger om annonser ska placeras i [!DNL Yandex]-annonsnätverket: <i>[!UICONTROL Yes]</i> (standard) eller <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | n/a | n/a | Valfritt | n/a | n/a | Negativa nyckelord (fraser) som delas av alla fraser i en annonsgrupp, föregånget av ett minustecken (till exempel `-mykeyword`). Om ett negativt nyckelord matchar ett nyckelord i en fras används inte det negativa nyckelordet i frasen. |
| [!UICONTROL Param1 (Yandex)] | n/a | n/a | Valfritt | n/a | n/a | Värdet för substitutionsvariabeln `{param1}`. Den kan innehålla upp till 255 byte. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Param2 (Yandex)] | n/a | n/a | Valfritt | n/a | n/a | Värdet för substitutionsvariabeln `{param2}`. Den kan innehålla upp till 255 byte. Om du vill ta bort det befintliga värdet använder du värdet `[delete]` (inklusive parenteserna). |
| [!UICONTROL Campaign Status] | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | n/a | n/a | n/a | Visningsstatus för kampanjen: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i> eller <i>[!UICONTROL stop]</i> (pausad). Standardvärdet för nya kampanjer är <i>[!UICONTROL active]</i>.<br><br><b>Anteckningar:</b><ul></li>Om en kampanj någonsin har varit aktiv kan du inte ta bort den. Arkivera den istället.</li><li>I vissa situationer kan kampanjer automatiskt arkiveras eller tas bort.</li><li>Du kan inte ange status manuellt till <i>[!UICONTROL disapproved]</i> eller <i>[!UICONTROL pending]</i>, eller ändra dessa statusvärden.</li></ul> |
| [!UICONTROL Ad Group Status] | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | n/a | n/a | Annonsgruppens visningsstatus: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i> eller <i>[!UICONTROL stop]</i> (pausad). Standardvärdet för nya annonsgrupper är <i>[!UICONTROL active]</i>.<br><br><b>Anteckningar:</b><ul></li>Om en annonsgrupp någonsin har varit aktiv kan du inte ta bort den. Arkivera den istället.</li><li>Du kan inte ange status manuellt till <i>[!UICONTROL disapproved]</i> eller <i>[!UICONTROL pending]</i>, eller ändra dessa statusvärden.</li></ul> |
| [!UICONTROL Ad Status] | n/a | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | Banderollens (annons) visningsstatus: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i> eller <i>[!UICONTROL stop]</i> (pausad). Standardvärdet för nya banderoller är <i>[!UICONTROL active]</i>.<br><br><b>Obs! Du kan inte ange status manuellt till <i>[!UICONTROL disapproved]</i> eller <i>[!UICONTROL pending]</i>, eller ändra dessa statusvärden. |
| [!UICONTROL Keyword Status] | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | n/a | Visningsstatus för frasen (nyckelord): <i>[!UICONTROL active]</i>. Standardvärdet för nya fraser är <i>[!UICONTROL active]</i>.<br><br><b>Obs! Du kan inte ange status manuellt till <i>[!UICONTROL disapproved]</i> eller <i>[!UICONTROL pending]</i>, eller ändra dessa statusvärden. |
| [!UICONTROL SiteLink Status] | n/a | n/a | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | Visningsstatus för sitelink: <i>[!UICONTROL * Aktiv]</i> eller <i>[!UICONTROL * pausad]</i>. Standardvärdet för nya sitelinks är <i>[!UICONTROL * Active]</i>. |
| [!UICONTROL Campaign ID] | Ej tillämpligt: Skapa<br>krävs/Valfritt: Redigera<br>Valfritt: Ta bort | Valfritt | Valfritt | Valfritt | Valfritt | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| [!UICONTROL Ad Group ID] | n/a | Ej tillämpligt: Skapa<br>krävs/Valfritt: Redigera<br>Valfritt: Ta bort | Valfritt | Valfritt | n/a | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| [!UICONTROL Ad ID] | n/a | n/a | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/Valfritt: Redigera eller ta bort | n/a | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordsnamnet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| [!UICONTROL Keyword ID] | n/a | n/a | Ej tillämpligt: Skapa<br>krävs/Valfritt: Redigera<br>krävs: Ta bort | n/a | n/a | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordsnamnet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | n/a | n/a | (I genererade kalkylblad) En [!DNL Adobe]-genererad unik identifierare för en synkroniserad entitet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar [!UICONTROL Ad ID]. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| \[Advertiser-specific Label Classification\] | Valfritt | Valfritt | Valfritt | Valfritt | n/a | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden används för alla underordnade komponenter. Nya komponenter som läggs till senare associeras automatiskt med etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Klassificeringsnamnet och klassificeringsvärdet är inte skiftlägeskänsliga. |
| [!UICONTROL Constraints] | Valfritt | Valfritt | Valfritt | n/a | n/a | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><br>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från Sök, Social och Commerce gällande data på raden. Felmeddelanden ingår i [!UICONTROL EF Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |

[^1]: I Excel konverteras stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

>[!MORELIKETHIS]
>
>* [Bilaga - fel i bulkark](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Mallfilformat som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överför en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
