---
title: Datakrav för trafik- och konverteringsstatistik för [!DNL Naver] konton med enbart spårning
description: Referera dataöverföringskraven för [!DNL Naver] konton med enbart spårning.
exl-id: 6f79730b-f8d6-4a7f-9d31-f42fe63e6b5d
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Krav för mätdata för [!DNL Naver] konton med enbart spårning

Följande är datakraven för [!DNL Naver] trafik- och konverteringsstatistik för konton med enbart spårning.

Datafiler måste vara i TSV-, CSV- eller TXT-format.

Följande rubrikfält är obligatoriska och valfria. Varje datarad måste innehålla ett dagligt aggregerat värde för minst ett mätfält.

| Rubrikfält/kolumnnamn | Typ | Beskrivning |
| ---- | ---- | ---- |
| Period | DateTime | Datumet som uppgifterna gäller, i formatet `YYYY.MM.DD.` (till exempel `2019.11.15.`, med en punkt efter dagen). |
| Campaign | Skiftlägeskänslig sträng | Kampanjnamnet. |
| Adgroup (som ett ord) | Skiftlägeskänslig sträng | Annonsgruppens namn. |
| Nyckelord | Skiftlägeskänslig sträng | (Nyckelordsannonser) Nyckelordet som genererade annonsen. |
| [Mått] | Heltal | (Valfritt) Antal [vad mätvärdet än mäter].</br><br>Standardvärden är Impressions, Cost och Click. Ni kan inkludera ytterligare mätvärden från annonsnätverket. Inkludera varje mätvärde i en separat kolumn.<br><br><b>Anteckningar:</b><ul><li>Kolumnrubriken för Kostnad måste vara &quot;Kostnad (KRW)&quot;.</li><li>Om du vill inkludera Kostnad (KRW) för varumärkesannonser delar du den fasta månadskostnaden manuellt efter dag på annonsgruppsnivå.</li><li>Ta bort alla kommatecken från standardmätvärden. Använd till exempel 1 000 i stället för 1 000.</li><li>Använd 0 för null-värden.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementera [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Bilaga - Obligatoriska data för kalkylblad för [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Ladda upp trafik- och konverteringsstatistik för [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
