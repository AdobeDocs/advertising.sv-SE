---
title: Frågor och svar om kampanjhantering
description: Lär dig mer om kampanjhantering, inklusive latensperioden för ändringar och vad som händer när du gör budgetändringar under en flygning.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Frågor och svar om kampanjhantering

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Fördröjning för inställningsändringar

* När du ändrar en placering eller paketinställning, när träder ändringen i kraft?

  Inställningarna börjar oftast gälla omedelbart, men kan ta upp till 12 timmar.

  Om det är sista leveransdagen kan du göra ändringar tidigt så att DSP hinner omkalibrera paketet baserat på ändringarna. Om du till exempel ändrar från jämna mellanrum till förhandslastpacing måste DSP omvärdera hur utgifterna ska fördelas under resten av flygningen. Gör inte den sortens förändring om du bara har en timma kvar att leverera på flygningens sista dag.

## Budgetuppdateringar efter avslut

* Hur lång tid tar det för DSP att omfördela paketbudgeten när du ändrar en placering?

  Budgettilldelningen baseras på placeringsprestanda, som utvärderas med ett 14-dagars genomsnitt. Ändringar av en placering resulterar endast i ändringar i budgettilldelningen när de orsakar prestandaförändringar under 14-dagarsgenomsnittet.

  När prestandaförändringar inträffar omfördelar DSP paketbudgeten bland enheterna i enlighet med detta under nästa budgetoptimeringscykel, som inträffar vid ungefär midnatt (00:00) i kampanjens tidszon.

* Hur omfördelas budgeten när en placering tas bort från ett paket och läggs till i ett annat paket?

  En placerings hela utgiftshistorik bifogas till placeringen och följer med från paket till paket.

  När du tar bort en placering från ett paket har paketet inte längre någon historik över placeringens utgifter. Paketbudgeten blir (paketbudget - borttagen placeringsbudget)/tidsintervall återstår. Paketbudgeten tilldelas sedan de återstående placeringarna i paketet.

  På samma sätt gäller att om du lägger till samma placering i ett annat paket, kommer DSP att ta hänsyn till placeringens utgiftshistorik när den allokerar budget för alla placeringar i det nya paketet.

* Hur förändras paketeringen på den sista dagen av en flygning?

  På flygningens sista dag förkortas dagen från 24 till 23 timmar så att paketbudgeten inte överskrids. Paketets paketeringsfyllningsstrategi ändras automatiskt till [!UICONTROL Frontload], även om den är inställd på [!UICONTROL even]. Detta innebär att 65 % av den dagliga budgeten ska ha nått 11:30 kl. 13.00 EST.

>[!MORELIKETHIS]
>
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Bästa metoder för att konfigurera prestandakampanjer](/help/dsp/optimization/campaign-best-practices-performance.md)
