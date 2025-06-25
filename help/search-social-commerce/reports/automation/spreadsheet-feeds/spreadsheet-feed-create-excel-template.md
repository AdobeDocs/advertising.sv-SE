---
title: Skapa en  [!DNL Excel] mall för en kalkylbladsrapportfeed
description: Lär dig hur du skapar specialformaterade kalkylbladsmallar.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Skapa en [!DNL Excel]-mall för ett kalkylbladsrapportflöde

*Endast för grundläggande rapporter och modellnoggrannhetsrapporter*

Om du vill skapa kalkylbladsfeeds måste du först skapa särskilt formaterade [!DNL Microsoft Excel] kalkylbladsmallar med hjälp av vanliga rapportmallar. Du kan också anpassa kalkylbladet [!DNL Excel] så att det innehåller ytterligare kolumner och diagram.

1. Generera önskad rapporttyp i **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** med en [!UICONTROL Date Aggregation] enhet av [!UICONTROL Daily] och med alla andra dataparametrar som du vill ha, och spara rapporten som en mall.

   >[!NOTE]
   >
   > * Du kan skapa kalkylbladsfeeds för [!UICONTROL Portfolio]-, [!UICONTROL Search Engine]-, [!UICONTROL Search Engine Account]-, [!UICONTROL Campaign]-, [!UICONTROL Ad Group]-, [!UICONTROL Ad Variation]-, [!UICONTROL Keyword]- och [!UICONTROL Forecast Accuracy]-rapporter. Om du använder [!UICONTROL Ad Group Report] bör du begränsa antalet annonsgrupper som ingår för att få snabbare resultat.
   > * Enheten [!UICONTROL Date Range] som definierats i mallen används inte. Du definierar datumen som data ska uppdateras för när du konfigurerar kalkylbladsflödet senare.

1. När rapporten har skapats går du till **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** och exporterar en TSV- eller XLS-version av rapportutdata till en fil.

1. Skapa en anpassad mall för rapporten i [!DNL Excel]:

   1. Öppna rapportfilen i [!DNL Excel].

   1. Förbered arbetsboken:

      1. Ta bort de översta raderna som visar rapportparametrarna. För XLS-filer tar du även bort raden [!UICONTROL Total]. Du kan även ta bort vissa datarader, men behålla a) datarubrikraden med alla kolumner i den ursprungliga ordningen och b) minst en datarad. Lägg inte till data manuellt.

         >[!NOTE]
         >
         > Den sista kolumnen måste innehålla värden som inte är noll.

      2. Sortera data efter startdatum i stigande ordning (från det äldsta till det senaste).

      3. Ändra kalkylbladsflikens namn från [!UICONTROL Sheet1] till [!UICONTROL RAW].

         Det här speciella fliknamnet gör att data kan uppdateras.

      4. (Valfritt) Lägg till anpassade kolumner till höger om kolumnerna från rapportmallen efter behov.

   1. (Valfritt) Skapa en pivottabell i ett separat kalkylblad. När du är klar högerklickar du i en cell i pivottabellen och väljer **[!UICONTROL Pivot Table Options]**, klickar på fliken **[!UICONTROL Data]** och väljer sedan **[!UICONTROL Refresh data when opening the file]**.

   1. Spara filen som ett [!DNL Excel]-kalkylblad i XLSX-format.

>[!MORELIKETHIS]
>
>* [Om tabellrapportfeeds](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Redigera inställningar för kalkylbladsrapportfeed](spreadsheet-feed-edit.md)
>* [Inställningar för kalkylbladsrapportfeed](spreadsheet-feed-settings.md)
>* [Visa eller spara en kalkylbladsrapportfeed-fil](spreadsheet-feed-view-or-save.md)
>* [Uppdatera kalkylbladsrapportfeeds manuellt](spreadsheet-feed-refresh.md)
>* [Ta bort tabellrapportfeeds](spreadsheet-feed-delete.md)
