---
title: Feed-inställningar för kalkylbladsrapport
description: Lär dig mer om inställningarna för kalkylbladsfeeds.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Feed-inställningar för kalkylbladsrapport

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Feed Name] | Ett namn för kalkylarksfeeden. |
| [!UICONTROL Report Template] | Rapportmallen som anger vilka rapportdata som krävs. Välj den som du använde för att skapa mallen [!DNL Excel]. Alla grundläggande rapportmallar visas.<br><br><b>Obs!</b> Om du ändrar rapportmallen som används för rapporten eller uppdaterar kolumnerna i mallen måste du skapa och överföra en ny [!DNL Excel]-mall. |
| [!UICONTROL Excel Template] | Den [!DNL Excel]-mall som du har skapat i XLSX-format, som används för data som anges i rapportmallen. Ange den fil som ska överföras antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på <b>[!UICONTROL Browse]</b> för att leta reda på filen på enheten eller i nätverket. |
| [!UICONTROL Back Fill From] | Startdatumet för vilket befintliga data på fliken [!UICONTROL RAW] uppdateras, vilket representeras av ett antal dagar tidigare. Ange ett värde på upp till 90 dagar. Standardvärdet är sju (7) dagar.<br><br>Om värdet till exempel är 7 och idag är 7 mars uppdateras befintliga data på fliken [!UICONTROL RAW] med början från 1 mars (fram till slutdatumet som anges av parametern [!UICONTROL Back Fill Until]). Befintliga datarader för datum före 1 mars tas inte bort, men de uppdateras inte. |
| [!UICONTROL Back Fill Until] | Slutdatumet för vilket befintliga data på fliken [!UICONTROL RAW] uppdateras, vilket representeras av ett antal dagar tidigare. Standardvärdet är en (1) dag.<br><br>Om det här värdet till exempel är 1, och idag är den 7 mars, uppdateras befintliga data på fliken [!UICONTROL RAW] till den 6 mars (och börjar med det startdatum som anges av parametern [!UICONTROL Back Fill From]). Om värdet är 1 är parametern [!UICONTROL Back Fill Until] 7 och idag är den 7 mars uppdateras befintliga data på fliken [!UICONTROL RAW] från 1 mars till 6. I båda exemplen tas inte befintliga datarader för datum efter 6 mars bort, men de uppdateras inte. |
| [!UICONTROL Email Recipients] | E-postadresser som du använder för att skicka meddelanden varje gång rapporten uppdateras, eller varje gång rapporten körs när mallen innehåller ett schema. Som standard anges adressen för ditt användarkonto. Om du vill ange flera adresser avgränsar du dem med kommatecken, blanksteg eller nya rader. |
| [!UICONTROL Schedule Time] | Tidpunkt för uppdatering av kalkylbladsflöden: antingen 08:00 eller någon timme mellan 10:00 och 23:00 i annonsörens tidszon. Standardvärdet för nya kalkylbladsfeeds är 10:00.<br><br><b>Obs!</b> Av prestandaskäl kan du inte uppdatera kalkylbladsfeeds på 09:00 när andra rapporter genereras. |
| [!UICONTROL Email Notification] | (När e-postmottagare anges) Vad som ska inkluderas i e-postmeddelanden till angivna adresser:<ul><li><i>Bifoga feed</i> — Skicka en kopia av den färdiga rapporten i XLSX-format. Om filen är större än 10 MB innehåller meddelandet ingen bifogad fil.</li><li><i>Endast meddelande</i> (standard) - Om du bara vill skicka ett meddelande om att rapporten har slutförts eller misslyckats, med en länk till rapporten.</li></ul> |

>[!MORELIKETHIS]
>
>* [Om tabellrapportfeeds](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Skapa en [!DNL Excel] mall för ett kalkylbladsrapportflöde](spreadsheet-feed-create-excel-template.md)
>* [Redigera inställningar för kalkylbladsrapportfeed](spreadsheet-feed-edit.md)
>* [Visa eller spara en kalkylbladsrapportfeed-fil](spreadsheet-feed-view-or-save.md)
>* [Uppdatera kalkylbladsrapportfeeds manuellt](spreadsheet-feed-refresh.md)
>* [Ta bort tabellrapportfeeds](spreadsheet-feed-delete.md)
