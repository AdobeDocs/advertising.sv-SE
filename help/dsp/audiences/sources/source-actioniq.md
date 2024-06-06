---
title: "Konvertera användar-ID från [!DNL ActionIQ] till universella ID"
description: "Lär dig hur DSP kan importera [!DNL ActionIQ] förstapartssegment."
feature: DSP Audiences
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL ActionIQ] till universella ID

*Betafunktion*

Använd DSP integrering med [!DNL ActionIQ] kunddataplattform för att konvertera era hashade e-postadresser till universella ID:n för riktad reklam.

Det finns <!-- NN --> steg för att dela data från [!DNL ActionIQ] med DSP:

1. [Skapa en publikkälla i DSP](#source-create).

1. ?

## Steg 1: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto och ange [universella ID-format](source-about.md) som du vill konvertera dina användaridentifierare till.

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL ActionIQ] användare.

1. När du är klar med alla steg kan du verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) som segmentet fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hash-adresser.

   Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Om du till exempel skickar 100 hashas-e-postadresser från din kunddataplattform bör de översättas till mer än 90 universella ID:n. En översättningsgrad på 90 % eller mindre är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

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

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
