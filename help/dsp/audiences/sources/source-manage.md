---
title: Skapa och hantera målgruppskällor för att aktivera universella ID-målgrupper
description: Lär dig hur du skapar och hanterar en källa för att importera målgrupper från din kunddataplattform och konvertera dem till segment som innehåller universella ID:n.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Skapa en målgruppskälla för att aktivera universella ID-målgrupper

*Betafunktion*

Skapa en källa i DSP för varje enskild målgrupp på kunddataplattformen som du vill konvertera till segment som innehåller angivna universella ID-typer. Du kan importera segmenten till din organisations DSP eller till ett annonsörskonto. Dataavgifter tillämpas baserat på de valda universella ID-typerna.

Ytterligare steg krävs för att importera målgrupperna från varje kunddataplattform. Se anmärkningen i slutet av proceduren.

## Skapa en publikkälla

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicka på **[!UICONTROL Add Source]**.

1. I [!UICONTROL Select a Type] väljer du din kunddataplattform:

   * *[!UICONTROL RT-CDP]*: [The [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: [[!DNL ActionIQ] plattform för kunddata](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Endast konfigurerade användare) [[!DNL Tealium] plattform för kunddata](source-about.md).

1. Ange [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* eller *[!UICONTROL Account]*.

1. Ange återstående [källinställningar](source-settings.md).

   Behåll en kopia av [!UICONTROL Source Key] som genereras. Du behöver värdet senare.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>När du har skapat en källa för din kunddataplattform måste du slutföra ytterligare steg. Se [arbetsflöde för att importera målgrupper från [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> och [arbetsflöde för att importera målgrupper från [!DNL Tealium]](source-tealium.md).

## Ändra ID-typer för en målkälla

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Edit]**.

1. Ändra [ID som valts för källan](source-settings.md).

1. Klicka på **[!UICONTROL Save]**.

## Ta bort en publikkälla

När du tar bort en källa tas de segment som översatts genom källan bort.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]**.

## Visa ändringsloggen för en publikkälla

Du kan visa information om ändringar i en målgruppskällpost och eventuellt bifoga anteckningar till loggen.

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Håll markören över källraden och klicka **[!UICONTROL Change log]**.

1. (Valfritt) Så här bifogar du en anteckning till ändringsloggen:

   1. Håll markören över källraden och klicka **[!UICONTROL Add Notes]**.

   1. Skriv anteckningen och klicka sedan på **[!UICONTROL Save]**.

      Maximala längden är 256 tecken.

1. (Valfritt) Om du vill öppna loggen på en större detaljskärm håller du markören över källraden och klickar på **[!UICONTROL View Details]**.

>[!MORELIKETHIS]
>
>* [Inställningar för målkälla](source-settings.md)
>* [Om källor för förstagångspubliker](source-about.md)
>* [Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
