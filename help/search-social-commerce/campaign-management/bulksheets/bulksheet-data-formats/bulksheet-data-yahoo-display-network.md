---
title: Masskalkylbladsdata för  [!DNL Yahoo! Display Network] konton
description: Referera rubrikfälten och datafälten i hämtade kalkylblad för  [!DNL Yahoo! Display Network] konton.
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Bilaga - Bulkbladsdata för [!DNL Yahoo! Display Network]-konton

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Du kan hämta data för [!DNL Yahoo! Display Network]-konton i bulk men inte överföra eller posta kalkylblad till annonsnätverket.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Tillgängliga datafält

| Fält | Campaign | Annonsgrupp | Annons | Beskrivning |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Annonsplattformen. |
| [!UICONTROL Acct  Name] | Om ingår | Om ingår | Om ingår | Det unika namn som identifierar ett annonsnätverkskonto. |
| [!UICONTROL Campaign Name] | Om ingår | Om ingår | Om ingår | Det unika namn som identifierar en kampanj för ett konto. |
| [!UICONTROL Ad Group Name] | n/a | Om ingår | Om ingår | Det unika namn som identifierar en annonsgrupp. |
| [!UICONTROL Ad Name] | n/a | n/a | Om ingår | Det unika namn som identifierar annonsen inom en annonsgrupp. Maximala längden är 50 tecken. |
| [!UICONTROL Ad Title] | n/a | n/a | Om ingår | Annonsens rubrik. |
| [!UICONTROL Description Line 1] | n/a | n/a | Om ingår | Den första raden i en annons innehåll. |
| [!UICONTROL Description Line 2] | n/a | n/a | Om ingår | Den andra raden i en annons innehåll. |
| [!UICONTROL Base URL/Final URL] | n/a | n/a | Om ingår | URL:en till landningssidan som slutanvändarna tas till när de klickar på annonsen, inklusive eventuella tilläggsparametrar som konfigurerats för kampanjen eller kontot. Bas/slutliga URL:er på nyckelordsnivå åsidosätter URL:er på annonsnivå och högre. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte, inte i annonsnätverket) För konton med mål-URL:er är det här värdet den URL som länkar en annons till en bas-URL/landningssida på annonsörens webbplats (ibland via en annan webbplats som spårar klickningen och sedan dirigerar om användaren till landningssidan). Den innehåller eventuella tilläggsparametrar som har konfigurerats för kampanj eller konto för sökning, sociala medier och Commerce. Om du genererade spårnings-URL:er baseras det här värdet på spårningsparametrarna i dina kontoinställningar och kampanjinställningar. Om du har lagt till nätverksspecifika parametrar kan de ersättas med motsvarande parametrar för Search, Social och Commerce. |
| \[Advertiser-specific Label Classification\] | Om ingår | Om ingår | Om ingår | (Namngiven för en annonsörspecifik etikettklassificering, t.ex. &quot;Färg&quot; för en etikettklassificering som kallas Färg) Ett värde för den angivna klassificeringen som är associerad med entiteten. |
| [!UICONTROL Constraints] | Om ingår | Om ingår | n/a | En begränsning som är tilldelad entiteten. |
| [!UICONTROL Campaign Status] | Om ingår | n/a | n/a | Visningsstatus för kampanjen: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/a | Om ingår | n/a | Annonsgruppens visningsstatus: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/a | n/a | Om ingår | Visningsstatus för nyckelordet: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> eller <i>[!UICONTROL Deleted]</i> (endast befintliga nyckelord). |
| [!UICONTROL Campaign ID] | Om ingår | Om ingår | Om ingår | Det unika ID som identifierar en befintlig kampanj. |
| [!UICONTROL Ad Group ID] | n/a | Om ingår | Om ingår | Det unika ID som identifierar en befintlig annonsgrupp. |
| [!UICONTROL Keyword ID] | n/a | n/a | Om ingår | Det unika ID som identifierar ett befintligt nyckelord. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | (I genererade kalkylblad) En Adobe-genererad unik identifierare för en synkroniserad enhet. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Ingår i genererade kalkylblad i informationssyfte) Platshållare för att visa felmeddelanden från Sök, Social och Commerce gällande data på raden. Felmeddelanden ingår i [!UICONTROL EF Errors]-filer. |

>[!MORELIKETHIS]
>
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
