---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Text och mall - flödesfilter

**\[Foderfilter\]:** Vilka rader i feed-filen som ska spridas:

* *[!UICONTROL Propagate all rows found in feed:]* (Standard) Om du vill sprida data för alla rader.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Om du bara vill sprida data för rader som uppfyller upp till tio angivna villkor. Ange vilka filter som ska användas:

   1. Välj den booleska åtgärden som ska användas för alla filter:  **[!UICONTROL AND]** eller **[!UICONTROL OR]**.

   1. Välj ett kolumnnamn på den första menyn, välj en operator på den andra menyn och ange sedan tillämpliga värden eller lämna indatafältet tomt för att sprida data för rader utan villkor.

   Kolumnlistan innehåller alla tillgängliga kolumner i feeden.

   Tillgängliga operatorer inkluderar *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (är inte lika med), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* och *[!UICONTROL greater than]*. När du väljer operatorn &quot;[!UICONTROL in]&quot; kan du ange en kommaavgränsad lista med värden; om en post matchar något av de angivna värdena, sprids data för dessa rader. Ange bara ett värde för alla andra operatorer. Värden är inte skiftlägeskänsliga.

   Om du t.ex. markerade kolumnen &quot;product_type&quot; och bara vill returnera rader för produktnamn som innehåller &quot;skor&quot; väljer du &quot;**[!UICONTROL contains]**&quot; och ange `shoes` i indatafältet.

   1. (Om du vill använda upp till nio ytterligare filter) För varje ytterligare filter klickar du på **[!UICONTROL Add Condition]** och ange sedan det ytterligare filtret per steg 2.
