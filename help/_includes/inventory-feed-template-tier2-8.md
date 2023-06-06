---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Tier 2 - Tier 8-fält i butiks- och annonsmallar

**[!UICONTROL Tier  2 - Tier 8]:** (När du lägger till nivåer av produktgrupper) En produktattributtyp som målprodukter ska tilldelas och kvalificeringskriterierna för den valda attributtypen (till exempel Brand=Acme eller Condition=New). Värdena används hierarkiskt för att avgöra vilka produkter som omfattas. Välj en attributtyp och ange kvalificeringskriterierna. Följande tecken är förbjudna: `[ ] < > >>` (två på varandra följande&quot;större än&quot;-tecken) som används för att ange kolumnnamn i mallen, modifieringsnamn i mallen och skiktavgränsare i [!UICONTROL Parent Product Grouping] i kalkylblad.

Du kan inkludera upp till åtta nivåer (nivåer) av produktgrupper, inklusive &quot;[!UICONTROL All Products]&quot; (nivå 1). Varje skikt kan innehålla flera produktgrupper, men de måste omfatta samma attributtyp (till exempel&quot;Villkor&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] endast) Möjliga värden för [!UICONTROL Channel] är &quot;[!UICONTROL Local]&quot; eller &quot;[!UICONTROL Online]och möjliga värden för [!UICONTROL ChannelExclusivity] är &quot;[!UICONTROL SingleChannel]&quot; och &quot;[!UICONTROL MultiChannel].&quot;
>* När du skapar en andra skiktets (underordnad) produktgrupp för en annonsgrupp från [!UICONTROL Product Groups] i [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view, another product group, called &quot;[!UICONTROL Everything Else],&quot; skapas automatiskt med standardanbudet för annonsgrupper. Använda lagerflödesmallar[!UICONTROL Everything Else]&quot; ingår inte.
>* När du inkluderar flera lager och inget värde är tillgängligt för den sista (högst numrerade) nivån används den näst högsta nivån som produktgrupp som kan köpas. Om du t.ex. inkluderar fem lager och inget värde är tillgängligt för nivå 5, används nivå 4 som en prisvärd produktgrupp (enhet). Om inget värde är tillgängligt för ett mellanskikt ignoreras raden. Om du t.ex. inkluderar fem lager och nivå 5 har ett värde men nivå 4 inte har det, ignoreras rad 4.

