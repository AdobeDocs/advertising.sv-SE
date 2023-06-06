---
title: Datakrav för dataflöden som använder ett transaktions-ID
description: Referera datakraven för dataflöden med ett transaktions-ID.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Datakrav för dataflöden som använder ett transaktions-ID

Här följer rubrikfälten och motsvarande datafält som krävs för varje typ av feed-fil.

>[!NOTE]
>* Rubrikerna kan placeras i vilken ordning som helst så länge som data i efterföljande rader följer samma ordning. Om du inte inkluderar någon rubrik måste dataradernas ordning vara konsekvent med varje matningsfil.
>* Varje rad i matningsfilen måste innehålla data för en transaktion, och transaktionen måste identifieras med ett transaktions-ID.


| Rubrikfält/kolumnnamn | Typ | Beskrivning |
| ---- | ---- | ---- |
| Transaktions-ID (ev_transid) | Skiftlägeskänslig sträng | Den annonserargenererade identifierare som är associerad med transaktionen. Eftersom konverteringsspårningstaggen för Adobe Advertising används för onlinedelarna av transaktionen måste detta vara samma som transaktions-ID:t (ev_transid) som Adobe Advertising tillhandahöll för den tidigare delen av transaktionen. Detta innebär att konverteringstaggen för onlinedelen av transaktionen måste innehålla en egenskap för ett unikt transaktions-ID.<br><br>**Obs!** Adobe Advertising använder ID:t för att hitta gamla transaktionsdata och uppdatera dem i enlighet med ett överenskommet infogningsläge (t.ex. för att ersätta befintliga data eller förstärka dem med nya data). |
| Transaktionsdatum | DateTime | Datum för transaktionen. Formatet måste vara konsekvent för varje transaktion. |
| Klientspecifik konvertering | Sträng | En konvertering som spåras (till exempel transaktionstyp eller belopp). Diskutera de konverteringar som ska ingå i implementeringsteamet för Adobe Advertising innan du påbörjar feeden. |

## Exempel

Följande exempelfil innehåller data för två transaktionsegenskaper (Produkt och Intäkter).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Konverteringsspårning med en transaktions-ID-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)

