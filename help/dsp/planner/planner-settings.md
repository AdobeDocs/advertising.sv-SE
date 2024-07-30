---
title: Inställningar för uppkopplade TV-program
description: Se beskrivningar av inställningarna för räckviddsplaner för anslutna tv-apparater.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 5d8d981f08eaea2b0a0bc553ab06bd47f1e88ac9
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Inställningar för uppkopplade TV-program

<!-- Move out of table for consistency at some point. -->

| Parameter | Beskrivning | Obligatoriskt? |
| --- | --- | --- |
| [!UICONTROL Name] | Namnet som identifierar din plan. | Ja |
| [!UICONTROL Advertiser] | Den specifika annonsören i kontot som planen skapas för. | Ja |
| [!UICONTROL Media Type] | Den typ av media som ska ingå i planen.<br><br>För närvarande är bara [!UICONTROL Connected TV] tillgängligt. | Ja |
| [!UICONTROL Date Range] | Start- och slutdatum för planen.<br><br>Startdatumet kan inte infalla före det aktuella datumet. Datumintervallet får inte vara längre än 90 dagar. | Ja |
| [!UICONTROL Goal Type] | Den typ av mål (till exempel [!UICONTROL Budget]) som ska beaktas för planen.<br><br>För närvarande är bara [!UICONTROL Budget] tillgängligt. | Ja |
| [!UICONTROL Goal Value] | Målvärdet för prognosen. Använd ett värde > 5000 USD om du vill ha mer exakta prognosresultat. | Ja |
| [!UICONTROL Max Bid] | Det högsta belopp som får betalas för 1 000 visningar. Om medietypen [!UICONTROL Connected TV] är markerad anger du ett värde på minst 10 USD. | Ja |
| [!UICONTROL Frequency Cap] | Antal gånger ett unikt hushåll ska betjänas annonser.<br><br>När du implementerar en plan och måste skapa flera placeringar använder du inställningen för frekvensbegränsning på paketnivå, inte placeringsnivå, för att säkerställa korrekt leverans. | Ja |
| [!UICONTROL Geo-Targeting] | Platser som ska inkluderas eller exkluderas som mål. Alternativen är:<ul><li>Länder, städer, lägen: Klicka på fliken **[!UICONTROL Country/State/City]**, välj om området är ett *land*, *delstat* eller *stad*, eller expandera valfri plats för att visa dess underkomponenter och klicka sedan på **[!UICONTROL Include]** eller **[!UICONTROL Exclude]** bredvid platsen.</li><li>Utvalda marknadsområden (DMA:er) i USA: Klicka på fliken **[!UICONTROL DMA]**, eller expandera valfritt läge för att visa DMA:er och klicka sedan på **[!UICONTROL Include]** eller **[!UICONTROL Exclude]** bredvid platsen.</li><li>Postnummer: Du kan antingen:<ul><li>Klicka på fliken **[!UICONTROL Search postal code]**, markera landet, ange det fullständiga stadsnamnet eller bokstäverna i stadsnamnet och tryck sedan på **[Retur]**, klicka på rätt stadsnamn för att visa alla postnummer för staden, klicka på rätt postnummer och klicka sedan på **[!UICONTROL Include]** eller **[!UICONTROL Exclude]**.</li><li>Klicka på fliken **[!UICONTROL Paste postal code]**, markera landet, ange eller klistra in kommaseparerade värden och klicka sedan på **[!UICONTROL Include All]** eller **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Ja |
| [!UICONTROL Inventory Targeting] | Lagerkällor som ska inkluderas eller exkluderas som mål. Välj minst en feed eller källa. | Ja |
| [!UICONTROL Site/App Targeting] | Webbplatser och appar som ska inkluderas eller exkluderas som mål. Ange en URL per rad och klicka sedan på **[!UICONTROL Include All]** eller **[!UICONTROL Exclude All]**. | Nej |
| [!UICONTROL Audience Targeting] | Målgrupper som ska inkluderas eller exkluderas som mål. | Nej |
| [!UICONTROL Ad duration] | Tidslängden för annonser som ska beaktas för planen. | Nej |

>[!MORELIKETHIS]
>
>* [Om DSP ](planner-about.md)
>* [Skapa en plan för ansluten TV-räckvidd](planner-create.md)
>* [Duplicera en ansluten TV-sändningsplan](planner-duplicate.md)
>* [Redigera en plan för ansluten TV-räckvidd](planner-edit.md)
>* [Exportera en plan för ansluten TV-räckvidd](planner-export.md)
>* [Generera om prognosen för en plan för en ansluten TV-räckvidd](planner-forecast.md)
>* [Arkivera en plan för ansluten TV-räckvidd](planner-archive.md)
