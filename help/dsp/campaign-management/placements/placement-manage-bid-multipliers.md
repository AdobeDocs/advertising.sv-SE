---
title: Hantera budmultiplikatorer för placeringar
description: Lär dig skapa och redigera budmultiplikatorer för dina placeringsmål.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Hantera budmultiplikatorer för placeringar

Du kan skapa och hantera budmultiplikatorer, som multiplicerar ett algoritmiskt beräknat bud för att öka eller minska budet, för dina befintliga placeringsmål på [kvalificerade måltyper](#bid-multiplier-by-target). Du kan antingen redigera budmultiplikatorvärden för en placering manuellt eller överföra ett kalkylblad med värden för en eller flera placeringar.

Som standard är budmultiplikatorn för ett mål 1,00, vilket innebär att anbudet inte justeras för det målet. Värdena kan ligga mellan 0,10 och 10,00. En budmultiplikator på 0,5 minskar till exempel ett USD 6-bud till USD 3 (0,5 x 6). När en auktion kvalificerar sig för flera budmodifierare multipliceras alla tillämpliga budmultiplikatorer. Om Kalifornien till exempel har en budmultiplikator på 2 och San Francisco har en budmultiplikator på 3, är den sista budmultiplikatorn för annonser som körs i San Francisco 6.

>[!NOTE]
>
>Anbudsmultiplikatorer ökar aldrig anbudet till mer än det högsta anbudet.

Du kan ange budmultiplikatorer (med andra värden än 1,00) för ett [begränsat antal mål](#bid-multiplier-limits-by-target).

Den här funktionen fungerar med dina befintliga placeringsmål. Information om hur du ändrar de valda målen för dina placeringar finns i [Redigera placeringar](/help/dsp/campaign-management/placements/placement-edit.md).

## Hantera budmultiplikatorer för en enda placering

Du kan antingen redigera värden manuellt eller överföra ett kalkylblad för en enstaka placering.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]** på undermenyn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]** bredvid placeringsnamnet.

1. Justera budmultiplikaterna för giltiga mål:

   * Om du vill justera värdena för budmultiplikatorn manuellt går du till varje [målspecifik flik](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] och [!UICONTROL Brand Safety]) och redigerar de befintliga värdena för placeringsmålen.

     De flesta målkategorierna listar underkategorier till vänster. Klicka på en underkategori för att hantera budmultiplikatorer för den underkategorin, beroende på vad som är tillämpligt.

   * Så här överför du en CSV-fil med budmultiplikatorvärden för att skriva över alla befintliga värden:

      1. Klicka på **[!UICONTROL CSV File Edit]** uppe till höger.

      1. Antingen a) klickar du på **[!UICONTROL Download Template]** och redigerar filen eller så redigerar du en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

         Hämtade kalkylblad innehåller ett ark för varje måltyp (t.ex. Land, Källa och Webbplatskategori). Endast befintliga budmultiplikatorer med värden &lt; 1,0 eller > 1,0 inkluderas.

         * Om du vill lägga till en budmultiplikator för ett befintligt mål anger du målet med samma syntax som visas i användargränssnittet och motsvarande budmultiplikatorvärde.

         * Om du vill ta bort en budmodifierare ställer du in värdet för budmultiplikatorn till 1,0 eller tar bort all information för raden.

         ![Exempelrad i en fil med flera offertkalkylblad](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exempelrad i en fil med flera anbud")

      1. Klicka på **[!UICONTROL Next]** om du vill gå till avsnittet [!UICONTROL Upload File] och antingen a) dra och släppa den redigerade filen i rutan eller b) klicka inuti rutan för att välja filen från enheten eller nätverket.

      1. Verifiera överförda data i avsnittet [!UICONTROL Review & Submit] och klicka sedan på **[!UICONTROL Save]**.

## Ladda upp dubbla utskrifter för en eller flera utplaceringar

Ladda upp ett kalkylblad om du vill använda samma värden på alla markerade placeringar.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]** på undermenyn.

1. Markera kryssrutan bredvid varje placering vars budmultiplikatorer du vill hantera.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]** i verktygsfältet för gruppåtgärder.

1. Överför en CSV-fil med budmultiplikatorvärden om du vill skriva över alla befintliga värden för alla valda placeringar.

   1. Antingen a) klickar du på **[!UICONTROL Download Template]** och redigerar filen eller så redigerar du en mall som hämtats tidigare. Spara den redigerade filen på enheten eller i nätverket.

      Nedladdade kalkylblad innehåller ett ark för varje måltyp (t.ex. Land, Källor och Platskategori). Endast befintliga budmultiplikatorer med värden &lt; 1.0 eller > 1.0 inkluderas.

      * Om du vill lägga till en budmultiplikator för ett befintligt mål anger du målet med samma syntax som visas i användargränssnittet och motsvarande budmultiplikatorvärde.

      * Om du vill ta bort en budmodifierare anger du multiplikatorvärdet 1.0 eller tar bort all information för raden.

      ![Exempelrad i en fil med flera offertkalkylblad](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exempelrad i en fil med flera anbud")

   1. Klicka på **[!UICONTROL Next]** för att gå till avsnittet [!UICONTROL Upload File] och antingen a) dra och släpp den redigerade filen i rutan eller b) klicka i rutan för att välja filen från enheten eller nätverket.

   1. Verifiera överförda data i avsnittet [!UICONTROL Review & Submit] och klicka sedan på **[!UICONTROL Save]**.

## Måltyper som är berättigade till budmultiplikatorer {#bid-multiplier-by-target}

Du kan endast konfigurera budmodifierare för inkluderade mål, inte exkluderade mål.

* **Geomål**: geografi (länder, stater och städer), postnummer och DMA:er

* **Lagermål**: källor och flöden för offentligt lager och [!UICONTROL On Demand] lager

* **Webbplatsmål:** riktade (men inte exkluderade) webbplatser/appar, webbplatskategorier

* **Målgrupper:** segment, dagdelar och ämnen

* **ads.txt-mål:** (När du avanmäler dig från ads.txt, vilket gör att du kan köpa lager från alla säljare), annonser.txt-säljare, annonser.txt-säljare och annonser.txt-säljare plus webbplatser utan annonser.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Maximalt antal buddelsemultiplikatorer per måltyp {#bid-multiplier-limits-by-target}

Du kan ange budmultiplikatorer (med andra värden än 1,00) för ett begränsat antal mål. Du kan till exempel ange anbudsmultiplikatorer för upp till 20 landsmål. Det högsta antalet mål för varje måltyp som kan ha budmultiplikatorer anges nedan.

| Kategori | Parameter | Högsta antal |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Tillstånd | 100 |
| Geo | Ort | 100 |
| Geo | Metro | 100 |
| Geo | Postnummer | 100 |
| Lager | Källor | 100 |
| Lager | Feeds | 100 |
| Webbplatser | Platskategori | 100 |
| Sites | Webbplatser/appar | 100 |
| Målgrupp | Segment | 500 |
| Målgrupp | Ämnen | 100 |
| Säker varumärkesexponering | Ads.txt | Ej tillämpligt |

>[!MORELIKETHIS]
>
>* [Om placeringshantering](placement-about.md)
>* [Redigera placeringar](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Monteringsinställningar](placement-settings.md)
