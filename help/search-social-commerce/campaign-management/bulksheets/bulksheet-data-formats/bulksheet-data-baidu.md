---
title: Obligatoriska kalkylbladsdata för  [!DNL Baidu] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för  [!DNL Baidu] konton.
exl-id: 9680cb37-50d4-4b4b-b359-ac54267cd5e6
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 0%

---

# Bilaga - Obligatoriska balansräkningsdata för [!DNL Baidu]-konton

Om du vill skapa och uppdatera [!DNL Baidu]-kampanjdata i grupp kan du använda skalkylbladsfiler för sökning, sociala medier och Commerce som är särskilt formaterade för [!DNL Baidu]-konton. Du kan antingen a) [generera bulkbladsfiler för befintliga konton](../bulksheet-download.md) i det filformat som krävs eller b) skapa dem manuellt (mer information om vilka filformat som stöds finns i [Filformat som stöds i bulkblad](bulksheet-file-formats.md)).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Location,Excluded IPs (Baidu), Ad Serving (Baidu),Ad Group Name,Max CPC,Keyword,Match Type,Ad Title,Description Line 1,Description Line 2,Display URL,Base URL,Destination URL,Custom URL Param,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Tillgängliga datafält

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>Följande tabell är bred. Använd vid behov rullningslisten längst ned i tabellen för att visa hela innehållet. Du kan också tillfälligt dölja innehållsförteckningen eller den högra rutan genom att klicka på ![Dölj den vänstra rutan](/help/search-social-commerce/assets/hide-left-pane.png "Dölj den vänstra rutan") högst upp i den vänstra rutan eller ![Dölj den högra rutan](/help/search-social-commerce/assets/hide-right-pane.png "Dölj den högra rutan") högst upp i den högra rutan.

| Fält | Campaign | Annonsgrupp | Nyckelord | Text Ad | Platsmål | Beskrivning |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Acct Name] | Obligatoriskt/valfritt | R/O | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Obligatoriskt/valfritt | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt | Obligatoriskt | Obligatoriskt | Obligatoriskt | Obligatoriskt | Det unika namnet som identifierar en kampanj för ett konto. |
| [!UICONTROL Campaign Budget] | Obligatoriskt: Create<br>Optional: Edit or Delete | n/a | inte aktuellt | inte aktuellt | inte aktuellt | En daglig utgiftsgräns för kampanjen, med eller utan monetära symboler och interpunktion. Det här värdet åsidosätter, men kan inte överskrida kontobudgeten. |
| [!UICONTROL Location] | inte aktuellt | n/a | n/a | n/a | Obligatoriskt | En geografisk plats där annonser för kampanjen ska placeras. Om du vill exkludera en plats anger du ett minustecken (`-`) för platsen. Om du inte anger specifika värden för kampanjen anges alla platser som mål. |
| [!UICONTROL Excluded IPs (Baidu)] | Valfritt | n/a | n/a | n/a | n/a | IP-adresser för webbplatser där annonserna inte ska visas. Avgränsa flera värden med kommatecken. |
| [!UICONTROL Ad Serving (Baidu)] | Valfritt | n/a | n/a | n/a | n/a | Hur ofta kan ni leverera era aktiva annonser i relation till varandra inom en annonsgrupp?<ul><li><i>Rotera</i> (standard för nya kampanjer): Var och en av dina annonser går in i annonsauktionen ungefär lika många gånger, vilket gör att Search, Social och Commerce kan poängsätta annonserna inte bara med klickfrekvens utan även med konverteringar.</li><li><i>Optimera:</i> Annonsnätverket prioriterar annonser som har en kombination av en hög klickfrekvens och en hög kvalitet. Dessa annonser kommer in på annonsauktionen oftare, och med tiden prioriteras en enskild annons. Resultatet kan vara inkonsekvent med era affärs- och optimeringsmål.</li></ul> |
| [!UICONTROL Ad Group Name] | n/a | Obligatoriskt | Obligatoriskt | Obligatoriskt | n/a | Det unika namn som identifierar en annonsgrupp. |
| [!UICONTROL Max CPC] | n/a | O | O | n/a | n/a | Den maximala kostnaden per klick (CPC), som är det högsta beloppet att betala för en annons som klickats på söknätverket, med eller utan monetära symboler och interpunktion. Du kan ange värden för annonsgrupper och nyckelord. Standardvärdet för ett nytt nyckelord ärvs från annonsgruppsnivån. |
| [!UICONTROL Keyword] | Valfri/ingen/a | Valfri/ingen/a | Obligatoriskt | n/a | n/a | Nyckelordssträngen.<br><br>Om du vill exkludera ett nyckelord på annonsgruppen eller kampanjnivån anger du [!UICONTROL Match Type] till [!UICONTROL Negative]. Om raden innehåller annonsgruppens namn exkluderas nyckelordet för annonsgruppen. Om raden inte innehåller annonsgruppens namn utesluts nyckelordet för hela kampanjen.<br><br><b>Obs!</b>Om du ändrar ett Baidu-nyckelord tas det befintliga nyckelordet bort och ett nytt med ett nytt nyckelord-ID skapas. Du kan dock ändra matchningstypen utan att ta bort det befintliga nyckelordet. |
| [!UICONTROL Match Type] | Valfritt/ej aktuellt | Valfri/ingen/a | Valfritt: Skapa<br>krävs/Valfritt: Redigera eller ta bort | n/a | n/a | Nyckelordsmatchningsalternativet för nyckelordet: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Negative Broad]</i> eller <i>[!UICONTROL Negative Exact]</i>. Definiera negativa nyckelord på kampanjnivå eller annonsgruppnivå.<br><br>För nya nyckelord är standardvärdet <i>[!UICONTROL Broad]</i>. Ett värde för matchningstypen eller nyckelords-ID krävs bara för att redigera ett nyckelord med flera matchningstyper.<br><br><b>Obs!</b>Du kan ändra matchningstypen för ett [!DNL Baidu]-nyckelord utan att ta bort det befintliga nyckelordet. |
| [!UICONTROL Ad Title] | inte aktuellt | inte aktuellt | n/a | Obligatoriskt | inte aktuellt | Annonsens rubrik. Maxlängden är 14 dubbelbyte- eller 28 enkelbyte-tecken.<br><br><b>Obs!</b> Om du ändrar annonskopian tas den befintliga annonsen bort och en ny annons med samma egenskaper skapas. |
| [!UICONTROL Description Line 1] | n/a | n/a | n/a | Obligatoriskt | n/a | Den första raden i en annons innehåll. Minsta längd är fyra dubbelbyte- eller åtta enkelbyte-tecken, och den maximala längden är 20 dubbelbyte- eller 40 enkelbyte-tecken.<br><br><b>Obs!</b> Om du ändrar annonskopian tas den befintliga annonsen bort och en ny annons med samma egenskaper skapas. |
| [!UICONTROL Description Line 2] | n/a | n/a | n/a | Obligatoriskt | n/a | Den andra raden i en annons innehåll. Minsta längd är fyra dubbelbyte- eller åtta enkelbyte-tecken, och den maximala längden är 20 dubbelbyte- eller 40 enkelbyte-tecken.<br><br><b>Obs!</b> Om du ändrar annonskopian tas den befintliga annonsen bort och en ny annons med samma egenskaper skapas. |
| [!UICONTROL Display URL] | n/a | n/a | n/a | Obligatoriskt | n/a | Den URL som visas i en annons. Den maximala längden är 35 tecken med en byte. |
| [!UICONTROL Base URL] | n/a | n/a | Valfritt | Obligatoriskt | n/a | URL:en till landningssidan som slutanvändarna tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot.<br><br>Bas/slut-URL:er på nyckelordsnivå åsidosätter URL:er på annonsnivå och högre. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte, inte i annonsnätverket) För konton med mål-URL:er är det här värdet den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och Commerce. Om du genererade spårnings-URL:er baseras det här värdet på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till nätverksspecifika parametrar kan de ersättas med motsvarande parametrar för Search, Social och Commerce.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som [!UICONTROL Base URL/Final URL column]. |
| [!UICONTROL Custom URL Param] | n/a | n/a | Valfritt | Valfritt | n/a | Data som ska ersätta den dynamiska variabeln `{custom_code}` när variabeln inkluderas i spårningsparametrarna för sökkontot eller kampanjinställningarna. Om du vill infoga det anpassade värdet i spårnings-URL överför du kalkylbladsfilen med alternativet [!UICONTROL Generate Tracking URLs]. |
| [!UICONTROL Campaign Status] | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | inte aktuellt | inte aktuellt | inte aktuellt | Visningsstatus för kampanjen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga kampanjer). Standardvärdet för nya kampanjer är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet [!UICONTROL Deleted]. |
| [!UICONTROL Ad Group Status] | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | n/a | n/a | Annonsgruppens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonsgrupper). Standardvärdet för nya annonsgrupper är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet [!UICONTROL Deleted]. |
| [!UICONTROL Keyword Status] | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | n/a | Visningsstatus för nyckelordet: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord), <i>[!UICONTROL Inactive]</i> (inte redigerbara), <i>[!UICONTROL Paused]</i> (endast befintliga nyckelord) eller <i>[!UICONTROL Pending]</i> (inte redigerbara). Standardvärdet för nya nyckelord är <i>[!UICONTROL Active]</i>.<br><br>Om du vill ta bort ett nyckelord anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | n/a | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | n/a | Annonsens visningsstatus: <i>[!UICONTROL Active]</i> (standard för nya annonser), <i>[!UICONTROL Deleted]</i> (endast befintliga annonser), <i>[!UICONTROL Disapproved]</i> (inte redigerbara), <i>[!UICONTROL Inactive]</i> (inte redigerbara), <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Pending (not editable)]</i>.<br><br>Om du vill ta bort en annons anger du värdet <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | n/a | n/a | n/a | n/a | Valfritt: Skapa eller redigera<br>krävs: Ta bort | Status för platsmålet: <i>[!UICONTROL Active]</i> eller <i>[!UICONTROL Deleted] (endast befintliga platser). Standardvärdet för nya platser är <i>[!UICONTROL Active]. Om du vill ta bort en aktiv plats anger du värdet <i>[!UICONTROL Deleted]. |
| \[Advertiser-specific Label Classification\] | Valfritt | Valfritt | Valfritt | Valfritt | n/a | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden används för alla underordnade komponenter. Nya komponenter som läggs till senare associeras automatiskt med etiketten. <br><br>Klassificeringsnamnet och klassificeringsvärdet är inte skiftlägeskänsliga. |
| [!UICONTROL Constraints] | Valfritt | Valfritt | Valfritt | n/a | n/a | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><br>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL Campaign ID] | Ej tillämpligt: Skapa<br>Obligatoriskt/Valfritt: Redigera och ta bort | Valfritt | Valfritt | Valfritt | n/a | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| [!UICONTROL Ad Group ID] | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/Valfritt: Redigera och ta bort | Valfritt | Valfritt | n/a | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| [!UICONTROL Keyword ID] | n/a | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/Valfritt: Redigera och ta bort | n/a | n/a | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordsnamnet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| [!UICONTROL Ad ID] | n/a | n/a | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/Valfritt: Redigera och ta bort | n/a | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordsnamnet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| [!UICONTROL AMO ID] | Ej tillämpligt: Skapa<br>Valfritt: Redigera och ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera och ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera och ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera och ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera och ta bort | (I genererade kalkylblad) En [!DNL Adobe]-genererad unik identifierare för en synkroniserad entitet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar [!UICONTROL Ad ID]. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Search, Social och Commerce använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från Sök, Social och Commerce gällande data på raden. Felmeddelanden ingår i [!UICONTROL EF Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL SE Error Message] | n/a | n/a | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL SE Errors]-filer. Det här värdet är inte registrerat i annonsnätverket. |

[^1]: I Excel konverteras stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

>[!MORELIKETHIS]
>
>* [Bilaga - fel i bulkark](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Mallfilformat som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överför en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
