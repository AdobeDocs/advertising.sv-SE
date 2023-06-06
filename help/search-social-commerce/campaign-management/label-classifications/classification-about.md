---
title: Etikettklassificeringar
description: Lär dig hur du använder etikettklassificeringar för att gruppera dina kontokomponenter.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Etikettklassificeringar

Med Label-klassificeringar kan du gruppera dina kontokomponenter i meningsfulla uppsättningar. Du kan t.ex. skapa en överordnad etikettklassificering med namnet&quot;Geo&quot;, skapa olika etikettvärden för varje geografisk region (t.ex.&quot;Storbritannien&quot; och&quot;Japan&quot;) i klassificeringen och sedan tilldela etikettvärdena till [mängdenheter](/help/search-social-commerce/glossary.md#a-b) eller överordnade kampanjer. Du kan sedan ta med ett valfritt etikettvärde som en separat kolumn i dina vyer och rapporter och skicka rapporter till olika klassificeringsgrupper och värden.

## Etikettklassificeringar

Alla annonsörer kan ha upp till 30 etikettklassificeringar, som är kategorier på den högsta nivån.

## Etikettvärden

Varje etikettklassificering kan ha upp till 2 000 värden. När du har skapat specifika etikettvärden för en klassificering kan du tilldela dem till kampanjer, annonsgrupper, nyckelord, annonser, placeringar och produktgrupper [från kampanjhanteringsvyer](classification-values-assign-campaign-management.md) eller [med glödlampor](classification-values-assign-bulksheets.md).

Varje godkänd enhet kan ha etikettvärden för flera klassificeringar, men bara ett etikettvärde per klassificering. Etikettvärden ärvs av underordnade entiteter men kan åsidosättas. Värdet som tilldelas på den lägsta nivån åsidosätter alltid värden som tilldelas på överordnade nivåer.

## Vyn Etikettklassificeringar

The [!UICONTROL Labels Classifications] visa i [!UICONTROL Search] > [!UICONTROL Campaigns] menyer innehåller [!UICONTROL Classifications] och [!UICONTROL Label Values] undervyer. Du kan visa data för dina etikettklassificeringar, [skapa](classification-create.md) och [delete](classification-delete.md) klassificeringar av etiketter och visa data för etikettens klassificeringsvärden. Som standard visas data för etikettklassificeringar och -värden på nyckelordsnivå, men du kan även visa data för dina klassificeringar och -värden på ad-nivå.

>[!MORELIKETHIS]
>
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer](classification-values-assign-campaign-management.md)
>* [Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad](classification-values-assign-bulksheets.md)
>* [Ta bort etikettklassificeringsvärden från kontokomponenter](classification-values-remove.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)

