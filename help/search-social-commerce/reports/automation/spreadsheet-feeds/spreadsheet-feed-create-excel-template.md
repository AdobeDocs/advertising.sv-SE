---
title: Skapa en [!DNL Excel] mall för kalkylbladsrapportflöde
description: Lär dig hur du skapar specialformaterade kalkylbladsmallar.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Skapa en [!DNL Excel] mall för kalkylbladsrapportflöde

*Endast för grundläggande rapporter och modellnoggrannhetsrapporter*

Om du vill skapa kalkylbladsfeeds måste du först skapa särskilt formaterade [!DNL Microsoft® Excel] kalkylbladsmallar med regelbundna rapportmallar. Du kan också anpassa [!DNL Excel] kalkylblad som innehåller ytterligare spalter och diagram.

1. I **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, generera önskad rapporttyp med en [!UICONTROL Date Aggregation] enhet för &quot;[!UICONTROL Daily]&quot; och med alla andra dataparametrar som du vill ha sparar du rapporten som en mall.

   >[!NOTE]
   >
   > * Du kan skapa kalkylbladsfeeds för [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword]och [!UICONTROL Forecast Accuracy] rapporter. Om du använder [!UICONTROL Ad Group Report], begränsa antalet annonsgrupper som ingår för snabbare resultat.
   > * The [!UICONTROL Date Range] enheten som definierats i mallen används inte. Du definierar datumen som data ska uppdateras för när du konfigurerar kalkylbladsflödet senare.


1. När rapporten har skapats går du till **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** och exportera en TSV- eller XLS-version av rapportutdata till en fil.

1. I [!DNL Excel]skapar du en anpassad mall för rapporten:

   1. Öppna rapportfilen i [!DNL Excel].

   1. Förbered arbetsboken:

      1. Ta bort de översta raderna som visar rapportparametrarna. För XLS-filer tar du också bort[!UICONTROL Total]&quot;. Du kan även ta bort vissa datarader, men behålla a) datarubrikraden med alla kolumner i den ursprungliga ordningen och b) minst en datarad. Lägg inte till data manuellt.

         >[!NOTE]
         >
         > Den sista kolumnen måste innehålla värden som inte är noll.

      2. Sortera data efter startdatum i stigande ordning (från det äldsta till det senaste).

      3. Ändra namnet på kalkylbladsfliken från[!UICONTROL Sheet1]&quot; till &quot;[!UICONTROL RAW].&quot;

         Det här speciella fliknamnet gör att data kan uppdateras.

      4. (Valfritt) Lägg till anpassade kolumner till höger om kolumnerna från rapportmallen efter behov.
   1. (Valfritt) Skapa en pivottabell i ett separat kalkylblad. När du är klar högerklickar du i valfri cell i pivottabellen och väljer **[!UICONTROL Pivot Table Options]** klickar du på **[!UICONTROL Data]** och sedan välja **[!UICONTROL Refresh data when opening the file]**.

   1. Spara filen som en [!DNL Excel] kalkylblad i XLSX-format.


>[!MORELIKETHIS]
>
>* [Om rapportflöden för kalkylblad](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Redigera inställningar för matning av kalkylbladsrapporter](spreadsheet-feed-edit.md)
>* [Feed-inställningar för kalkylbladsrapport](spreadsheet-feed-settings.md)
>* [Visa eller spara en matningsfil för kalkylbladsrapport](spreadsheet-feed-view-or-save.md)
>* [Uppdatera kalkylbladsrapportfeeds manuellt](spreadsheet-feed-refresh.md)
>* [Ta bort rapportflöden för kalkylblad](spreadsheet-feed-delete.md)

