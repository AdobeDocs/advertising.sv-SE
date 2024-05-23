---
title: Hantera budmultiplikationer för praktik
description: Lär dig hur du skapar och redigerar budmultiplikatorer för dina placeringsmål.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: c23da6494c6d4ce89735f3f63f89f5320ca02a40
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 2%

---

# Hantera budmultiplikationer för praktik

Du kan skapa och hantera budmultiplikatorer, som ett bud multipliceras med för att öka eller minska anbudet, för dina befintliga placeringsmål på [måltyper](#bid-multiplier-by-target). Du kan antingen redigera budmultiplikatorvärden manuellt eller överföra ett kalkylblad med värden.

Som standard är budmultiplikatorn för ett mål 1,00, vilket innebär att anbudet inte justeras för det målet. Värdena kan ligga mellan 0,10 och 10,00. En budmodifierare på 0,5 minskar till exempel ett USD 6-bud till USD 3 (0,5 x 6). När en auktion kvalificerar sig för flera budmodifierare multipliceras alla tillämpliga budmodifierare. Anbudsmodifierare ökar aldrig anbudet till mer än det högsta anbudet.

Du kan ange budmultiplikatorer (med andra värden än 1,00) för en [begränsat antal mål](#bid-multiplier-limits-by-target).

Den här funktionen fungerar med dina befintliga placeringsmål. Information om hur du ändrar de valda målen för dina placeringar finns i &quot;[Redigera placeringar](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Justera budmultiplikaterna för giltiga mål:

   * Om du vill justera budmultiplikatorvärdena manuellt går du till varje [målspecifik flik](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]och [!UICONTROL Brand Safety]) och redigera de befintliga värdena för placeringsmålen.

     De flesta målkategorierna listar underkategorier till vänster. Klicka på en underkategori för att hantera budmultiplikatorer för den underkategorin, beroende på vad som är tillämpligt.

   * Så här överför du en CSV-fil med budmultiplikatorvärden för att skriva över befintliga värden:

      1. Klicka **[!UICONTROL CSV File Edit]** i det övre högra hörnet.

      1. Antingen a) klickar du **[!UICONTROL Download Template]** och ange målen med samma syntax som visas i användargränssnittet och motsvarande budmultiplikatorvärden eller b) redigera en mall som laddats ned tidigare med samma information. Spara den redigerade filen på enheten eller i nätverket.

      1. Klicka **[!UICONTROL Next]** för att gå till [!UICONTROL Upload File] och antingen a) dra och släpp den redigerade filen i rutan eller b) klicka inuti rutan för att välja filen från enheten eller nätverket.

      1. Verifiera överförda data i [!UICONTROL Review & Submit] och klicka sedan på **[!UICONTROL Save]**.

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
>* [Redigera placeringar](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
