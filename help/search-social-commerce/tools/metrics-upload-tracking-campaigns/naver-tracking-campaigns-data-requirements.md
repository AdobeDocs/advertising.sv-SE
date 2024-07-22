---
title: Datakrav för trafik- och konverteringsstatistik för  [!DNL Naver] spårningskonton som endast är tillgängliga
description: Referera dataöverföringskraven för  [!DNL Naver] konton med endast spårning.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Krav för måttdata för [!DNL Naver]-konton med endast spårning

Nedan följer datakraven för [!DNL Naver]-trafik och konverteringsmått för konton med enbart spårning.

Datafiler måste vara i TSV-, CSV- eller TXT-format.

Följande rubrikfält är obligatoriska och valfria. Varje datarad måste innehålla ett dagligt aggregerat värde för minst ett mätfält.

| Rubrikfält/kolumnnamn | Typ | Beskrivning |
| ---- | ---- | ---- |
| Period | DateTime | Datumet som data gäller, i formatet `YYYY.MM.DD.` (till exempel `2019.11.15.`, med en punkt efter dagen). |
| Campaign | Skiftlägeskänslig sträng | Kampanjnamnet. |
| Adgroup (som ett ord) | Skiftlägeskänslig sträng | Annonsgruppens namn. |
| Nyckelord | Skiftlägeskänslig sträng | (Nyckelordsannonser) Nyckelordet som genererade annonsen. |
| [Mått] | Heltal | (Valfritt) Antalet [oavsett vilket mätvärde som används är ].</br><br>Standardvärden är Impressions, Cost och Click. Ni kan inkludera ytterligare mätvärden från annonsnätverket. Inkludera varje mätvärde i en separat kolumn.<br><br><b>Anteckningar:</b><ul><li>Kolumnrubriken för Kostnad måste vara &quot;Kostnad (KRW)&quot;.</li><li>Om du vill inkludera Kostnad (KRW) för varumärkesannonser delar du den fasta månadskostnaden manuellt efter dag på annonsgruppsnivå.</li><li>Ta bort alla kommatecken från standardmätvärden. Använd till exempel 1 000 i stället för 1 000.</li><li>Använd 0 för null-värden.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementera [!DNL Naver] konton med endast spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Bilaga - obligatoriska kalkylbladsdata för  [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Överför trafik- och konverteringsstatistik för [!DNL Naver] konton med endast spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
