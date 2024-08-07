---
title: Datakrav för dataflöden som använder EF-ID:n
description: Referera datakraven för dataflöden med hjälp av EF-ID:n.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Datakrav för dataflöden som använder EF-ID:n

Här följer rubrikfälten och motsvarande datafält som krävs för varje typ av feed-fil.

>[!NOTE]
>* Rubrikerna kan placeras i vilken ordning som helst så länge som data i efterföljande rader följer samma ordning. Om du inte inkluderar någon rubrik måste dataradernas ordning vara konsekvent med varje matningsfil.
>* Varje rad i matningsfilen måste innehålla data för en transaktion, och transaktionen måste identifieras med ett Adobe Advertising-genererat ef_id (token).

| Rubrikfält/kolumnnamn | Typ | Beskrivning |
| ---- | ---- | ---- |
| EF ID | Skiftlägeskänslig sträng | ef_id (token) som du fångade vid klickningen för transaktionen, som består av surfer-ID, klickningstid och nätverkstyp. Ändra inte värdet. |
| Transaktions-ID | Skiftlägeskänslig sträng | (Valfritt men rekommenderas) Det annonsörer-genererade transaktions-ID:t. Det bästa sättet är att inkludera detta för varje transaktion även om ef_id används för att spåra transaktionen vid tidpunkten för omdirigeringen. |
| Transaktionsdatum | DateTime | Datum för transaktionen. Formatet måste vara konsekvent för varje transaktion. |
| Klientspecifik konvertering | Sträng | En konvertering som spåras (till exempel transaktionstyp eller belopp). Diskutera de konverteringar som ska ingå i implementeringsteamet för Adobe Advertising innan du påbörjar feeden. |

## Exempel

Följande exempelfil innehåller data för två konverteringsmått (Produkt och Intäkter).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Konverteringsspårning med en EF ID-feed](/help/search-social-commerce/tracking/feed-efid.md)
