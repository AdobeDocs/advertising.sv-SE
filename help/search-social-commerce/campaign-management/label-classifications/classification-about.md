---
title: Etikettklassificeringar
description: Lär dig hur du använder etikettklassificeringar för att gruppera dina kontokomponenter.
exl-id: 3ec4b111-225e-4272-b3dc-4f6f9c711779
feature: Search Label Classifications
source-git-commit: 82710ffc246e1d3bc9547bf6b6df3320c80c4eb1
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Etikettklassificeringar

Med Label-klassificeringar kan du gruppera dina kontokomponenter i meningsfulla uppsättningar. Du kan till exempel skapa en överordnad etikettklassificering med namnet&quot;Geo&quot;, skapa ett eget etikettvärde för varje geografisk region (till exempel&quot;Storbritannien&quot; och&quot;Japan&quot;) i klassificeringen och sedan tilldela etikettvärdena till dina [budenheter](/help/search-social-commerce/glossary.md#a-b) eller överordnade kampanjer. Du kan sedan ta med ett valfritt etikettvärde som en separat kolumn i dina vyer och rapporter och skicka rapporter till olika klassificeringsgrupper och värden.

## Etikettklassificeringar

Alla annonsörer kan ha upp till 30 etikettklassificeringar, som är kategorier på den högsta nivån.

## Etikettvärden

Varje etikettklassificering kan ha upp till 2 000 värden. När du har skapat specifika etikettvärden för en klassificering kan du tilldela dem till kampanjer, annonsgrupper, nyckelord, annonser, placeringar och produktgrupper [ från kampanjhanteringsvyer](classification-values-assign-campaign-management.md) eller [med hjälp av kalkylblad](classification-values-assign-bulksheets.md).

Varje godkänd enhet kan ha etikettvärden för flera klassificeringar, men bara ett etikettvärde per klassificering. Etikettvärden ärvs av underordnade entiteter men kan åsidosättas. Värdet som tilldelas på den lägsta nivån åsidosätter alltid värden som tilldelas på överordnade nivåer.

## Vyn Etikettklassificeringar

I det äldre användargränssnittet är vyn [!UICONTROL Labels Classifications] vid [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Labels Classifications]. I det nya användargränssnittet är vyn [!UICONTROL Labels Classifications] på [!UICONTROL Reports] > [!UICONTROL Labels Classifications].

Vyn [!UICONTROL Labels Classifications] innehåller [!UICONTROL Classifications] och [!UICONTROL Label Values] undervyer. Du kan visa data för dina etikettklassificeringar, [skapa](classification-create.md)- och [ta bort](classification-delete.md)-etikettklassificeringar och visa data för dina etikettklassificeringsvärden. Som standard visas data för etikettklassificeringar och -värden på nyckelordsnivå, men du kan även visa data för dina klassificeringar och -värden på ad-nivå.

I det nya användargränssnittet

>[!MORELIKETHIS]
>
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer](classification-values-assign-campaign-management.md)
>* [Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad](classification-values-assign-bulksheets.md)
>* [Ta bort etikettklassificeringsvärden från kontokomponenter](classification-values-remove.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)
