---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Tier 2 - Tier 8-fält i butiks- och annonsmallar

**[!UICONTROL Tier  2 - Tier 8]:** (När du lägger till produktgruppsnivåer) En produktattributtyp som målprodukter ska tilldelas och kvalificeringskriterierna för den valda attributtypen (till exempel Brand=Acme eller Condition=New). Värdena används hierarkiskt för att avgöra vilka produkter som omfattas. Välj en attributtyp och ange kvalificeringskriterierna. Följande otillåtna tecken är: `[ ] < > >>` (två på varandra följande större än-tecken), som används för att ange kolumnnamn i mallen, modifierarnamn i mallen och skiktavgränsare i kolumnen [!UICONTROL Parent Product Grouping] i kalkylblad.

Du kan inkludera upp till åtta nivåer (nivåer) av produktgrupper, inklusive [!UICONTROL All Products] (nivå 1). Varje skikt kan innehålla flera produktgrupper, men de måste omfatta samma attributtyp (till exempel&quot;Villkor&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] endast) Möjliga värden för [!UICONTROL Channel] är [!UICONTROL Local] eller [!UICONTROL Online], och möjliga värden för [!UICONTROL ChannelExclusivity] är [!UICONTROL SingleChannel] och [!UICONTROL MultiChannel].
>* När du skapar en andra produktgrupp (underordnad) för en annonsgrupp på fliken [!UICONTROL Product Groups] i vyn [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] skapas en annan produktgrupp, som kallas [!UICONTROL Everything Else], automatiskt med standardanbudet för annonsgruppen. Lagerflödesmallar används, men [!UICONTROL Everything Else] produktgrupper exkluderas.
>* När du inkluderar flera lager och inget värde är tillgängligt för den sista (högst numrerade) nivån används den näst högsta nivån som produktgrupp som kan köpas. Om du t.ex. inkluderar fem lager och inget värde är tillgängligt för nivå 5, används nivå 4 som en prisvärd produktgrupp (enhet). Om inget värde är tillgängligt för ett mellanskikt ignoreras raden. Om du t.ex. inkluderar fem lager och nivå 5 har ett värde men nivå 4 inte har det, ignoreras rad 4.
