---
title: Feed-inställningar för kalkylbladsrapport
description: Lär dig mer om inställningarna för kalkylbladsfeeds.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Feed-inställningar för kalkylbladsrapport

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Feed Name] | Ett namn för kalkylarksfeeden. |
| [!UICONTROL Report Template] | Rapportmallen som anger de nödvändiga rapportuppgifterna. välj den som du använde för att skapa [!DNL Excel] mall. Alla grundläggande rapportmallar visas.<br><br><b>Obs!</b> Om du ändrar rapportmallen som används för rapporten, eller om du uppdaterar kolumnerna i mallen, måste du skapa och överföra en ny [!DNL Excel] mall. |
| [!UICONTROL Excel Template] | Specialformaterade [!DNL Excel] -mall som du har skapat i XLSX-format, som används för data som anges i rapportmallen. Ange vilken fil som ska överföras antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på <b>[!UICONTROL Browse]</b> för att hitta filen på enheten eller i nätverket. |
| [!UICONTROL Back Fill From] | Startdatum som befintliga data på [!UICONTROL RAW] har uppdaterats, vilket representeras av ett antal dagar tidigare. Ange ett värde på upp till 90 dagar. standardinställningen är sju (7) dagar.<br><br>Om värdet till exempel är 7 och idag är 7 mars, är befintliga data på [!UICONTROL RAW] fliken som börjar med mars 1 uppdateras (fram till det slutdatum som anges av [!UICONTROL Back Fill Until] parameter). Befintliga datarader för datum före 1 mars tas inte bort, men de uppdateras inte. |
| [!UICONTROL Back Fill Until] | Slutdatum som befintliga data på [!UICONTROL RAW] har uppdaterats, vilket representeras av ett antal dagar tidigare. Standardvärdet är en (1) dag.<br><br>Om det här värdet till exempel är 1 och idag är 7 mars, är befintliga data på [!UICONTROL RAW] har uppdaterats fram till 6 mars (och börjar med det startdatum som anges av [!UICONTROL Back Fill From] parameter). Om det här värdet är 1 visas [!UICONTROL Back Fill Until] är 7 och idag 7 mars är de befintliga uppgifterna på [!UICONTROL RAW] Fliken uppdateras från 1 mars till 6 mars. I båda exemplen tas inte befintliga datarader för datum efter 6 mars bort, men de uppdateras inte. |
| [!UICONTROL Email Recipients] | E-postadresser som du använder för att skicka meddelanden varje gång rapporten uppdateras, eller varje gång rapporten körs när mallen innehåller ett schema. Som standard anges adressen för ditt användarkonto. Om du vill ange flera adresser avgränsar du dem med kommatecken, blanksteg eller nya rader. |
| [!UICONTROL Schedule Time] | Tidpunkt när kalkylbladsfeeds uppdateras: antingen 08:00 eller någon timme mellan 10:00 och 23:00 i annonsörens tidszon. Standardvärdet för nya kalkylbladsfeeds är 10:00.<br><br><b>Obs!</b> Av prestandaskäl kan du inte uppdatera kalkylbladsfeeds på 09:00 när andra rapporter genereras. |
| [!UICONTROL Email Notification] | (När e-postmottagare anges) Vad som ska inkluderas i e-postmeddelanden till angivna adresser:<ul><li><i>Koppla feed</i> — Skicka en kopia av den färdiga rapporten i XLSX-format. Om filen är större än 10 MB innehåller meddelandet ingen bifogad fil.</li><li><i>Endast meddelande</i> (standard) - Om du bara vill skicka ett meddelande om att rapporten har slutförts eller misslyckats, med en länk till rapporten.</li></ul> |

>[!MORELIKETHIS]
>
>* [Om rapportflöden för kalkylblad](spreadsheet-feed-about.md)
>* [Skapa ett kalkylbladsrapportflöde](spreadsheet-feed-create.md)
>* [Skapa en [!DNL Excel] mall för kalkylbladsrapportflöde](spreadsheet-feed-create-excel-template.md)
>* [Redigera inställningar för matning av kalkylbladsrapporter](spreadsheet-feed-edit.md)
>* [Visa eller spara en matningsfil för kalkylbladsrapport](spreadsheet-feed-view-or-save.md)
>* [Uppdatera kalkylbladsrapportfeeds manuellt](spreadsheet-feed-refresh.md)
>* [Ta bort rapportflöden för kalkylblad](spreadsheet-feed-delete.md)

