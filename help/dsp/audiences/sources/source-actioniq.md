---
title: "Konvertera användar-ID från [!DNL ActionIQ] till universella ID"
description: "Lär dig hur DSP kan importera [!DNL ActionIQ] förstapartssegment."
feature: DSP Audiences
source-git-commit: 4292083dac92860854dca30f7897e1b0279f68ec
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL ActionIQ] till universella ID

*Funktionen Beta*

Använd DSP integrering med [!DNL ActionIQ] kunddataplattform för att konvertera era hashade e-postadresser till universella ID:n för riktad reklam.

Det finns <!-- NN --> steg för att dela data från [!DNL ActionIQ] med DSP:

1. [Skapa en publikkälla i DSP](#source-create).

1. ?

## Steg 1: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto och ange [universella ID-format](source-about.md) som du vill konvertera dina användaridentifierare till.

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL ActionIQ] användare.

1. 
   <!-- ActionIQ-specific step(s) -->

1. Verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) som segmentet fyller i och jämför antalet universella ID med antalet ursprungliga hashade e-postadresser.

   Segmenten ska vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata ska antalet deltagare vara synligt inom nio (9) timmar.

   Översättningsfrekvensen för hash-kodade e-postadresser till universella ID måste vara högre än 90 %. Översättningsfrekvensen för [!DNL RampIDs] ska i synnerhet vara 95 % om alla hash-kodade e-postadresser är unika. Om du t.ex. skickar 100 hash-kodade e-postadresser från din kunddataplattform bör de översättas till minst 95 [!DNL RampIDs] eller mer än 90 andra typer av universella ID:n. En lägre översättningsgrad är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

   Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

Segmenten uppdateras var 24:e timme.

## Steg 2:

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID](/help/dsp/audiences/sources/source-tealium.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
