---
title: Anpassade måttinställningar
description: Referera inställningarna för anpassade mått, som beräknas utifrån standardvärden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Anpassade måttinställningar

Anpassade måttinställningar är något annorlunda i olika delar av gränssnittet.

## Anpassade måttinställningar i kampanjhanteringsvyer

| Parameter/avsnitt | Beskrivning |
|----|----|
| Anpassat måttnamn | Namnet på måttet, som visas som kolumnnamn. <b>Tips:</b> Använd ett meningsfullt måttnamn, men tänk på att längre namn gör kolumnen bredare. |
| Infoga mått | Den matematiska formel som används för att beräkna det nya mätvärdet (t.ex. [Kostnad]/[Registreringar]:<ul><li>Om du vill infoga ett mätvärde från listan med trafik- och intäktsmått placerar du markören där du vill infoga mätvärdet och sedan antingen väljer du mätvärdet i listan eller anger det manuellt och omsluts av hakparenteser (till exempel `[CPC]`).</li><li>Om du vill infoga en operator placerar du markören där du vill infoga operatorn och klickar sedan på knappen eller anger symbolen manuellt. De tillgängliga matematiska operatorerna: `+ - * / ( ) ()`</li></ul><b>Obs!</b> Komplexa anpassade mätvärden tar längre tid att beräkna, och rapporter och vyer som innehåller dem - särskilt när de innehåller separata kolumner för klicknings- och genomskinlighetskonverteringar - tar längre tid att generera. |
| Format | Så här presenterar du data för det här måttet: *[!UICONTROL Currency]* (ett penningvärde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, eller *[!UICONTROL Percentage]* (ett procenttal med två decimaler).<br><br><b>Varning:</b> Om du skapar ett härlett mått med formatet [!UICONTROL Number w/out Decimal Points] (som visar data som heltal) och inkludera dem i en vy eller en rapport som använder en viktad konverteringsattribueringsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], eller [!UICONTROL Even Distribution]) visas utdata i heltal, inte i decimaler. Därför kan enskilda datafält vara felaktiga, även om summorna är korrekta. Om en ordning till exempel fördelas jämnt mellan tre händelser, fördelas en ordning (i stället för 0,33) på var och en av de tre händelserna. Du kan förhindra problemet genom att använda måttformatet [!UICONTROL Number to 2 Decimal Points]. |

## Anpassade måttinställningar i rapporter och rapportmallar och i [!UICONTROL Portfolios] vyer

| Parameter/avsnitt | Beskrivning |
|----|----|
| Anpassat måttnamn | Namnet på måttet, som visas som kolumnnamn. <b>Tips:</b> Använd ett meningsfullt måttnamn, men tänk på att längre namn gör kolumnen bredare. |
| Format | Så här presenterar du data för det här måttet: *[!UICONTROL Currency]* (ett penningvärde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, eller *[!UICONTROL Percentage]* (ett procenttal med två decimaler).<br><br><b>Varning:</b> Om du skapar ett härlett mått med formatet [!UICONTROL Number w/out Decimal Points] (som visar data som heltal) och inkludera dem i en vy eller en rapport som använder en viktad konverteringsattribueringsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], eller [!UICONTROL Even Distribution]) visas utdata i heltal, inte i decimaler. Därför kan enskilda datafält vara felaktiga, även om summorna är korrekta. Om en ordning till exempel fördelas jämnt mellan tre händelser, fördelas en ordning (i stället för 0,33) på var och en av de tre händelserna. Du kan förhindra problemet genom att använda måttformatet [!UICONTROL Number to 2 Decimal Points]. |
| Infoga mått | En lista med befintliga mätvärden som du kan använda för att skapa en formel.<br><br>Om du vill infoga ett mätvärde i formelinmatningsfältet placerar du markören där du vill infoga mätvärdet och väljer sedan mätvärdet i listan eller anger det manuellt och omsluts av hakparenteser (till exempel `[CPC]`). |
| Infoga operator | De tillgängliga matematiska operatorerna: `+ - x / ( )`<br><br>Om du vill infoga en operator i formelinmatningsfältet placerar du markören där du vill infoga operatorn och klickar sedan på knappen eller anger symbolen manuellt. |
| [Formelindatafält för måttet] | Den matematiska formel som används för att beräkna det nya måttet baserat på en eller flera befintliga egenskaper eller standardmått (t.ex. `[Cost]/[Registrations]`. Den kan innehålla vilken kombination av mätvärden och operatorer som helst.<br><br><b>Obs!</b> Komplexa anpassade mätvärden tar längre tid att beräkna, och rapporter och vyer som innehåller dem - särskilt när de innehåller separata kolumner för klicknings- och genomskinlighetskonverteringar - tar längre tid att generera. |

>[!MORELIKETHIS]
>
>* [Om anpassade mått](custom-metric-about.md)
>* [Skapa ett anpassat mått](custom-metric-create.md)
>* [Redigera ett anpassat mått](custom-metric-edit.md)
>* [Ta bort ett anpassat mått](custom-metric-delete.md)

