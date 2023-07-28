---
title: Filformat för kalkylblad som stöds
description: Se de allmänna filkraven för kalkylblad.
exl-id: b14aaf11-e2e9-4f7c-b6bc-831f668b93a6
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Filformat för kalkylblad som stöds

## Filformat

Du kan hämta, överföra och publicera kalkylbladsfiler för annonsnätverk som stöds i något av följande format:

* CSV (kommaavgränsade värden)
* TSV (tabbseparerade värden)
* TXT (Unicode-text), avgränsad med kommatecken eller tabbar
* ZIP (komprimerad) som innehåller en fil i CSV-format, TSV-format eller TXT-format avgränsat med kommatecken eller tabbar

När du skapar/hämtar ett kalkylblad skapas det i det angivna filformatet med alla relevanta data som finns i filen. Använd följande information om du vill redigera data i filen eller skapa ett eget kalkylblad manuellt.

## Grundläggande innehåll i ett kalkylblad

Den första posten (raden) i en kalkylbladsfil innehåller en uppsättning specifika kolumnnamn, gemensamt kända som <i>header</i>. Kolumnnamnen i rubriken är i en angiven ordning och motsvarar vart och ett av fälten i efterföljande dataposter. Kolumnnamnen som krävs i rubriken varierar beroende på annonsnätverk.

Varje efterföljande post (rad) innehåller data, med fält som innehåller värden (eller inga värden) för varje kolumn i rubriken.

## Maximal filstorlek

Bulkbladsfiler kan vara upp till 2,5 GB, vilket är ungefär 2,5 miljoner rader.

>[!NOTE]
>
>När du genererar ett kalkylblad för flera kampanjer och de kombinerade data består av över 500 000 rader, delas data upp efter kampanj i två eller flera filer, med namnet `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`och så vidare.

## Formateringskrav för olika filtyper

Datafält som avgränsas av tabbar och kommatecken kräver olika formatering.

### TSV-filer och TXT-filer avgränsade med tabbar

Datafält i TSV-filer och TXT-filer som är avgränsade med tabbar måste formateras enligt följande:

* Fälten i varje post avgränsas med tabbtecken. Om du vill utelämna ett värde för ett fält använder du bara tabbtecknet.

  Exempel: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Fält får inte innehålla inbäddade tabbtecken.

### CSV-filer och TXT-filer avgränsade med kommatecken

Datafält i CSV-filer och TXT-filer avgränsade med kommatecken måste formateras enligt följande:

* Fälten i en post avgränsas med kommatecken. Om du vill utesluta ett värde för ett fält använder du bara kommatecken.

  Exempel: `Cruises,5000,Caribbean,,,`

* Alla fält kan omslutas av citattecken (`""`).

  Exempel:  `"Cruises","5000","Caribbean",`

* Fält med inbäddade kommatecken måste omslutas av citattecken (`""`).

  Exempel: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Fält med inbäddade dubbla citattecken måste omslutas med dubbla citattecken (`""`).

  Exempel: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Fält med inledande eller avslutande blanksteg måste omslutas av citattecken (`""`).

  Exempel: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](../bulksheet-about.md)
>* [Åtgärder som du kan utföra i kalkylblad](bulksheet-operations.md)
>* [Bilaga - Fel i bulkark](../bulksheet-errors.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
