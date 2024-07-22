---
title: Inställningar för uppkopplade TV-program
description: Se beskrivningar av inställningarna för räckviddsplaner för anslutna tv-apparater.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 8574d76fd322cb1cbc6aaaf316e7ad2f961a9f6c
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Inställningar för uppkopplade TV-program

| Parameter | Beskrivning | Obligatoriskt? |
| --- | --- | --- |
| Namn | Namnet som identifierar din plan. | Ja |
| Annonsör | Den specifika annonsören i kontot som planen skapas för. | Ja |
| Medietyp | Den typ av media som ska ingå i planen.<br><br>För närvarande är bara [!UICONTROL Connected TV] tillgängligt. | Ja |
| Datumintervall | Start- och slutdatum för planen.<br><br>Startdatumet kan inte infalla före det aktuella datumet. Datumintervallet får inte vara längre än 90 dagar. | Ja |
| Måltyp | Den typ av mål (till exempel [!UICONTROL Budget]) som ska beaktas för planen.<br><br>För närvarande är bara [!UICONTROL Budget] tillgängligt. | Ja |
| Målvärde | Målvärdet för prognosen. Använd ett värde > 5000 USD om du vill ha mer exakta prognosresultat. | Ja |
| Max. bud | Det högsta belopp som får betalas för 1 000 visningar. Om medietypen [!UICONTROL Connected TV] är markerad anger du ett värde på minst 10 USD. | Ja |
| Frekvensgräns | Antal gånger ett unikt hushåll ska betjänas annonser.<br><br>När du implementerar en plan och måste skapa flera placeringar använder du inställningen för frekvensbegränsning på paketnivå, inte placeringsnivå, för att säkerställa korrekt leverans. | Ja |
| Geografisk inriktning | Platser som ska inkluderas eller exkluderas som mål. | Ja |
| Målinriktning för lager | Lagerkällor som ska inkluderas eller exkluderas som mål. Välj minst en feed eller källa. | Ja |
| Målgruppsanpassning | Målgrupper som ska inkluderas eller exkluderas som mål. | Nej |
| Annonsens varaktighet | Tidslängden för annonser som ska beaktas för planen. | Nej |

>[!MORELIKETHIS]
>
>* [Om DSP ](planner-about.md)
>* [Skapa en plan för ansluten TV-räckvidd](planner-create.md)
>* [Duplicera en ansluten TV-sändningsplan](planner-duplicate.md)
>* [Redigera en plan för ansluten TV-räckvidd](planner-edit.md)
>* [Exportera en plan för ansluten TV-räckvidd](planner-export.md)
>* [Generera om prognosen för en plan för en ansluten TV-räckvidd](planner-forecast.md)
>* [Arkivera en plan för ansluten TV-räckvidd](planner-archive.md)
