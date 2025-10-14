---
title: Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad
description: Lär dig hur du använder kalkylblad för att tilldela klassificeringsvärden till kontokomponenter.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad

Du kan associera etikettklassificeringar med värden för följande sökentiteter med hjälp av kalkylblad: kampanj, annonsgrupp, nyckelord, annons, placering, produktgrupp på enhetsnivå och dynamiskt sökmål. Varje etikettklassificering kan ha upp till 2 000 värden.

Varje entitet kan ha ett etikettvärde per klassificering. Exempel: Shoes_Campaign kan ha färgvärdet &quot;red&quot; och det geografiska värdet &quot;Los Angeles&quot;, men det kan inte ha flera värden för Color eller Geo.

Etikettvärden ärvs av underordnade entiteter, så ange inte värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena.

>[!NOTE]
>
>Dina nyckelord och din annonskopia för vissa annonsnätverk och kampanjtyper är [inte ändringsbara](/help/search-social-commerce/campaign-management/faqs-campaigns.md), vilket innebär att om du redigerar dem tas den befintliga entiteten bort och en ny skapas. När en befintlig enhet tas bort på det här sättet tilldelas inte etikettklassificeringen till den nya enheten.

1. [Hämta ett kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) som innehåller entiteterna som du vill tilldela etikettklassificeringsvärden till:

   * Expandera listan [!UICONTROL Campaign] i rutan [!UICONTROL Bulksheet Columns] på fliken [!UICONTROL Rows and Columns].

   * Expandera listan [!UICONTROL Label Classification].

   * Markera varje klassificering som du vill ta med en kolumn i kalkylbladsfilen för.

     Om du till exempel inkluderar etiketterna Färg och Geo innehåller kalkylbladet kolumnerna Färg och Geo.

1. Öppna filen i en redigerare och lägg till etikettvärden i etikettklassificeringskolumnerna för de entiteter som de ska associeras med. Värdet får innehålla högst 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

   Se exempelvärdena i nästa avsnitt.

   Förutom att lägga till värden kan du även ta bort befintliga värden genom att ta bort dem från relevanta rader. Om du vill ta bort värden från både en överordnad enhet och dess underordnade enheter, kan du antingen a) ta med endast den överordnade enhetsraden och ta bort det befintliga klassificeringsvärdet eller b) ta med både den överordnade enheten och dess underordnade enheter och ta bort det befintliga klassificeringsvärdet från alla överordnade och underordnade rader.

1. [Överför filen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) för att skapa associationerna.

De överförda etikettvärdena visas i de relevanta enhetsvyerna.

## Exempel på etikettklassificeringsvärden som ska överföras i kalkylblad

Det här exemplet innehåller kolumner för etiketterna &quot;Color&quot; och &quot;Geo&quot;. För dina egna kalkylblad, ersätt kolumner med dina egna etikettklassificeringsnamn.

| Konto | Campaign | Annonsgrupp | Nyckelord | Annons | Placement | Etiketter | Färg | Geo |
|---|---|---|---|---|---|---|---|---|
| Konto1 | C1 | | | | | | Grön | |
| Konto1 | C1 | AG1 | | | | | | |
| Konto1 | C1 | AG1 | K1 | | | | | Storbritannien |
| Konto1 | C1 | AG1 | K2 | | | | Röd | AU |
| Konto1 | C1 | AG1 | K3 | | | | Blå | DE |
| Konto1 | C1 | AG1 | | A1 | | | | |
| Konto1 | C1 | AG1 | | A1 | | | Röd | |
| Konto1 | C1 | AG1 | | | P1 | | Röd | AU |
| Konto1 | C1 | AG1 | | | P2 | | Blå | DE |

>[!MORELIKETHIS]
>
>* [Om etikettklassificeringar](classification-about.md)
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer](classification-values-assign-campaign-management.md)
>* [Ta bort etikettklassificeringsvärden från kontokomponenter](classification-values-remove.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)
