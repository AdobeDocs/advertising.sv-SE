---
title: Obligatoriska kalkylbladsdata för [!DNL Naver] konton
description: Referera till obligatoriska rubrikfält och datafält i kalkylblad för [!DNL Naver] konton.
exl-id: bd6e3dab-47b0-428a-825d-bd9c21494fb0
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# Bilaga - Obligatoriska data för kalkylblad för [!DNL Naver] konton

Fyll i [!DNL Naver] konton i sökningar, sociala medier och handel genom att generera en kalkylbladsfil i [!DNL Naver]och sedan ladda upp det till Search, Social och Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Tillgängliga datafält

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Fält | Campaign | Annonsgrupp | Nyckelord | Beskrivning |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Acct Name] | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Obligatoriskt/valfritt | Det unika namn som identifierar ett annonsnätverkskonto. Obligatoriskt såvida inte varje rad innehåller ett AMO-ID för entiteten. |
| [!UICONTROL Campaign Name] | Obligatoriskt | Obligatoriskt | Obligatoriskt | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Ad Group Name] | n/a | Obligatoriskt | Obligatoriskt | Det unika namn som identifierar en annonsgrupp. |
| [!UICONTROL Keyword] | n/a | n/a | Obligatoriskt | Nyckelordssträngen. |
| [!UICONTROL Base URL] | n/a | n/a | Valfritt | URL:en till landningssidan som slutanvändarna tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot.<br><br>Bas/slutliga URL:er på nyckelordsnivå åsidosätter URL:er på annonsnivå och högre. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte, inte i annonsnätverket) För konton med mål-URL:er är det här värdet den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och handel. Om du genererade spårnings-URL:er baseras det här värdet på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till nätverksspecifika parametrar kan de ersättas med motsvarande parametrar för Sök, Socialt och Handel.<br><br>För konton med slutliga URL:er visar den här kolumnen samma värde som [!UICONTROL Base URL/Final URL column]. |
| \[Advertiser-specific Label Classification\] | Valfritt | Valfritt | Valfritt | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. Du kan bara inkludera ett värde per klassificering per enhet (till exempel&quot;red&quot; för etikettklassificeringen&quot;Color&quot; för kampanj A). Maxlängden är 100 tecken och värdet kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.<br><br>Etikettklassificeringar och deras etikettvärden används för alla underordnade komponenter. Nya komponenter som läggs till senare kopplas automatiskt till etiketten. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).<br><br>Klassificeringsnamnet och klassificeringsvärdet är inte skiftlägeskänsliga. |
| [!UICONTROL Constraints] | Valfritt | Valfritt | Valfritt | En begränsning som är tilldelad entiteten. Du kan bara tilldela en begränsning per enhet.<br><br>Begränsningar ärvs av underordnade entiteter, så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. |
| [!UICONTROL Campaign Status] | Valfritt: Skapa eller redigera<br>Obligatoriskt: Ta bort | n/a | n/a | Visningsstatus för kampanjen: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga kampanjer). Standardinställningen för nya kampanjer är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv eller pausad kampanj anger du värdet[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | n/a | Valfritt: Skapa eller redigera<br>Obligatoriskt: Ta bort | n/a | Annonsgruppens visningsstatus: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga annonsgrupper). Standardinställningen för nya annonsgrupper är <i>[!UICONTROL Active]</i>. Om du vill ta bort en aktiv eller pausad annonsgrupp anger du värdet[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | n/a | n/a | Valfritt: Skapa eller redigera<br>Obligatoriskt: Ta bort | Visningsstatus för nyckelordet: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, eller <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord). Standardvärdet för nya nyckelord är <i>[!UICONTROL Active]</i>. Om du vill ta bort ett aktivt eller pausat nyckelord anger du värdet[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | Ej tillämpligt: Skapa<br>Obligatoriskt/valfritt: Redigera eller ta bort | Valfritt | Valfritt | Det unika ID som identifierar en befintlig kampanj. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar kampanjnamnet, såvida inte raden innehåller ett AMO-ID för kampanjen. |
| [!UICONTROL Ad Group ID] | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/valfritt: Redigera eller ta bort | Valfritt | Det unika ID som identifierar en befintlig annonsgrupp. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar annonsgruppens namn, såvida inte raden innehåller ett AMO-ID för annonsgruppen. |
| [!UICONTROL Keyword ID] | n/a | n/a | Ej tillämpligt: Skapa<br>Obligatoriskt/valfritt: Redigera<br>Obligatoriskt: Ta bort | Det unika ID som identifierar ett befintligt nyckelord. I CSV- och TSV-filer måste det föregås av ett enkelt citattecken (&#39;).[^1] Krävs endast när du ändrar nyckelordsnamnet, såvida inte raden innehåller a) tillräckliga egenskapskolumner för att identifiera nyckelordet eller b) ett AMO-ID. |
| [!UICONTROL AMO ID] | Ej tillämpligt: Skapa<br>Valfritt: Redigera eller ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera eller ta bort | Ej tillämpligt: Skapa<br>Valfritt: Redigera eller ta bort | (I genererade kalkylblad) [!DNL Adobe]-genererad unik identifierare för en synkroniserad entitet. För responsiva sökannonser krävs AMO-ID:t för att redigera eller ta bort annonser, såvida du inte inkluderar [!UICONTROL Ad ID]. Om du vill redigera data för alla andra entitetstyper med ett AMO-ID måste AMO-ID:t redigera eller ta bort data, såvida du inte inkluderar enhets-ID och överordnat enhets-ID.<br><br>Sökning, sociala medier och handel använder värdet för att fastställa rätt identitet för redigering, men skickar inte ID:t till annonsnätverket. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från Sök, Social och Commerce gällande data på raden. Felmeddelanden ingår i [!UICONTROL EF Errors] filer. Det här värdet är inte registrerat i annonsnätverket. |
| [!UICONTROL SE Error Message] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från annonsnätverket med avseende på data i raden. Felmeddelanden ingår i [!UICONTROL SE Errors] filer. Det här värdet är inte registrerat i annonsnätverket. |

<table style="table-layout:auto">

[^1]: Excel konverterar stora tal till vetenskaplig notation (till exempel 2.12E+09 för 2115585666) när filen öppnas. Om du vill visa siffror i standardnotationen markerar du en cell i kolumnen och klickar inuti formelfältet.

>[!MORELIKETHIS]
>
>* [Bilaga - Fel i bulkark](../bulksheet-errors.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Filformat för kalkylblad som stöds](bulksheet-file-formats.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
>* [Klickningsspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Överföra en kalkylbladsfil eller korrigerad felfil](../bulksheet-upload.md)
>* [Implementera [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
