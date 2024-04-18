---
title: Hantera budmultiplikationer för praktik
description: Lär dig hur du skapar och redigerar budmultiplikatorer för angivna placeringsmål.
feature: DSP Placements
source-git-commit: b3932c066e0ecd29e57152f0654ee4b0d9e0dda1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---

# Hantera budmultiplikationer för praktik

Du kan ändra budmultiplikaterna för dina befintliga placeringsmål med den här funktionen. Du kan hantera budmultiplikatorer för en placering i taget.<!-- remove that line once we can edit multiple -->

Information om hur du ändrar de valda målen för dina placeringar finns i &quot;[Redigera en placering](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Flytta till varje [målspecifik flik](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]och [!UICONTROL Brand Safety]) och redigera de befintliga värdena för placeringsmålen. De flesta målkategorierna listar underkategorier till vänster. Klicka på en underkategori om du vill hantera budmultiplikatorer för den underkategorin, när den är tillämplig.

   Som standard är budmultiplikatorn för ett mål 1,00, vilket innebär att anbudet inte justeras för det målet. Värdena kan ligga mellan 0,10 och 10,00. En budmodifierare på 0,5 minskar till exempel ett USD 6-bud till USD 3 (0,5 x 6). Anbudsmodifierare ökar aldrig anbudet till mer än det högsta anbudet.

   När en auktion kvalificerar sig för flera budmodifierare multipliceras alla tillämpliga budmodifierare.

   Du kan ange budmultiplikatorer (med andra värden än 1,00) för en [begränsat antal mål](#bid-multiplier-limits-by-target).

1. Klicka på uppe till höger **[!UICONTROL Save]**.

## Måltyper som är berättigade för budmultiplikatorer {#bid-multiplier-by-target}

Du kan bara konfigurera budmodifierare för inkluderade mål, inte exkluderade mål.

* **Geografiska mål**: geografi (länder, delstater och städer), postnummer och DMA

* **Lagermål**: källor och flöden för offentliga inventeringar och [!UICONTROL On Demand] lager

* **Webbplatsmål:** riktade (men inte exkluderade) webbplatser/appar, webbplatskategorier

* **Målgrupper:** segment, dagdelar och ämnen

* **ads.txt target:** (När du avanmäler dig från ads.txt, som gör att du kan köpa lager från alla säljare), annonser.txt-säljare, annonser.txt-direktförsäljare och annonser.txt-säljare plus webbplatser utan annonser.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Maximalt antal buddelsemultiplikatorer per måltyp {#bid-multiplier-limits-by-target}

Du kan ange budmultiplikatorer (med andra värden än 1,00) för ett begränsat antal mål. Du kan t.ex. ange budmultiplikatorer för upp till 20 landsmål. Det högsta antalet mål för varje måltyp som kan ha budmultiplikatorer anges nedan.

| Kategori | Parameter | Högsta antal |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Läge | 100 |
| Geo | Ort | 100 |
| Geo | Metro | 100 |
| Geo | Postnummer | 100 |
| Lager | Källor | 100 |
| Lager | Feeds | 100 |
| Webbplatser | Platskategori | 100 |
| Webbplatser | Webbplatser/appar | 100 |
| Målgrupp | Segment | 500 |
| Målgrupp | Ämnen | 100 |
| Säker varumärkesexponering | Ads.txt | Ej tillämpligt |

>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Redigera en placering](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
