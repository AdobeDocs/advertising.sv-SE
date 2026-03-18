---
title: Konvertera användar-ID:n från [!DNL ActionIQ] till universella ID:n
description: Lär dig hur du gör det möjligt för DSP att importera dina [!DNL ActionIQ] egna segment.
feature: DSP Audiences
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Konvertera användar-ID från [!DNL ActionIQ] till universella ID

*Beta-funktion*

Använd DSP-integreringen med kunddataplattformen [!DNL ActionIQ] för att konvertera dina hashade e-postadresser till universella ID:n för riktad annonsering.

Det finns <!-- NN --> steg för att dela data från [!DNL ActionIQ] med DSP:

1. [Skapa en publikkälla i DSP](#source-create).

1. ?

## Steg 1: Skapa en målgruppskälla i DSP {#source-create}

1. [Skapa en målgruppskälla](source-manage.md) om du vill importera målgrupper till ditt DSP-konto eller till ett annonsörskonto och ange de [universella ID-format](source-about.md) som du vill konvertera dina användaridentifierare till.

1. När du har skapat målgruppskällan delar du källkodnyckeln med användaren [!DNL ActionIQ].

## Steg 2:

## Steg 3:

1. Kontrollera i målgruppsbiblioteket (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet fylls i och jämför antalet universella ID:n med antalet ursprungliga hashade e-postadresser.

   Segmenten bör vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata bör antalet deltagare vara synligt inom nio (9) timmar. Mer information om godkända ID-översättningsfrekvenser och varför antalet segment kan variera finns i [Datavarianser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).

Segmenten uppdateras var 24:e timme.

## Felsökning

Om du vill felsöka problem med översättningsfrekvens och antal användare läser du i &quot;[Stöd för aktivering av universella ID:n](/help/dsp/audiences/universal-ids.md)&quot;.

Om du vill felsöka problem med konverteringsproceduren kontaktar du Adobe Account Team eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID:n](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID:n](/help/dsp/audiences/sources/source-tealium.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
