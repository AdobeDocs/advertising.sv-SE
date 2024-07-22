---
title: "Konvertera användar-ID:n från [!DNL ActionIQ] till universella ID:n"
description: "Lär dig hur du aktiverar DSP att importera dina [!DNL ActionIQ] förstapartssegment."
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Konvertera användar-ID från [!DNL ActionIQ] till universella ID

*Beta-funktion*

Använd den DSP integreringen med kunddataplattformen [!DNL ActionIQ] för att konvertera dina hashade e-postadresser till universella ID:n för riktad annonsering.

Det finns <!-- NN --> steg för att dela data från [!DNL ActionIQ] med DSP:

1. [Skapa en publikkälla i DSP](#source-create).

1. ?

## Steg 1: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en målgruppskälla](source-manage.md) om du vill importera målgrupper till ditt DSP eller ett annonserarkonto och ange de [universella ID-format](source-about.md) som du vill konvertera dina användaridentifierare till.

1. När du har skapat målgruppskällan delar du källkodnyckeln med användaren [!DNL ActionIQ].

## Steg 2:

## Steg 3:

1. Kontrollera i målgruppsbiblioteket (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet fylls i och jämför antalet universella ID:n med antalet ursprungliga hashade e-postadresser.

   Segmenten ska vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata ska antalet deltagare vara synligt inom nio (9) timmar. Mer information om godkända ID-översättningsfrekvenser och varför antalet segment kan variera finns i [Datavarianser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).

Segmenten uppdateras var 24:e timme.

## Felsökning

Om du vill felsöka problem med översättningsfrekvens och antal användare läser du i &quot;[Stöd för aktivering av universella ID:n](/help/dsp/audiences/universal-ids.md)&quot;.

Om du vill felsöka problem med konverteringsproceduren kontaktar du kontogruppen på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID:n](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID:n](/help/dsp/audiences/sources/source-tealium.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
