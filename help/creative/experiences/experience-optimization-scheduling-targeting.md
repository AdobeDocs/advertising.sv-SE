---
title: Anpassa den kreativa optimeringen och planeringen för en upplevelse
description: Lär dig hur
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 4abb83d08a6633c36aa47b5acd67df3d4cc0923b
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Anpassa den kreativa optimeringen och planeringen för en upplevelse med målgruppsanpassning i beslutsträd

*Endast målnoder med befintliga kreatörer*
*Stängd beta*

Som standard bestäms den kreativa rotationen för en upplevelse algoritmiskt för att optimera den övergripande klickfrekvensen, och inställningarna för den kreativa optimeringen gäller för alla tilldelade paket. Du kan anpassa den kreativa rotationen för att manuellt köra kreatörerna i varje paket utifrån relativa vikter eller för att algoritmiskt optimera för ett specifikt Advertising DSP-mål. Du kan också schemalägga att specifika kreativa programpaket ska köras under angivna, sekventiella tidsperioder och tillämpa anpassade inställningar för kreativ rotation för varje schema.

>[!NOTE]
>
>De här funktionerna är inte tillgängliga för noder som använder standardbildkreatörerna i stället för tilldelade kreatörer.

## Konfigurera kreativ optimering utan schemaläggning

När den kreativa planeringen är inaktiverad gäller inställningarna för den kreativa optimeringen för alla tilldelade kreatörer.

1. Håll markören över den kreativa bladnoden under målnoden och klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Inaktivera **[!UICONTROL Schedule]**.

1. Välj den kreativa rotationstypen:

   * *[!UICONTROL Weighted]:* Roterar kreatörerna i varje paket manuellt enligt relativa vikter. Ange vikten för varje paket som en procentandel. Vikten för alla paket måste vara upp till 100.

   * *[!UICONTROL Algorithmic]:* Roterar kreatörerna i varje paket algoritmiskt enligt ett angivet optimeringsmål.

      * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

1. Klicka på **[!UICONTROL Save]**.

## Konfigurera kreativ optimering med kreativ planering

Du kan också schemalägga att specifika kreativa programpaket ska köras under angivna, sekventiella tidsperioder mellan start- och slutdatumet för upplevelsen och använda anpassade kreativa rotationsinställningar för varje schema. Du kan till exempel schemalägga att paket 1 ska köras under de första två veckorna för att optimera klickfrekvensen och paket 2 ska köras under de följande två veckorna för att optimera för ett visst anpassat mål.

När du använder schemaläggning måste du schemalägga paket under hela upplevelsen.

1. Håll markören över den kreativa bladnoden under målnoden och klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Aktivera **[!UICONTROL Schedule]**.

1. För det första schemat:

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreativt paket som ska läggas till i det första schemat.

   1. Ange start- och slutdatum för schemat.

   1. Välj den kreativa rotationstypen:

      * *[!UICONTROL Weighted]:* Roterar kreatörerna i varje paket manuellt enligt relativa vikter. Ange vikten för varje paket som en procentandel. Vikten för alla valda paket måste vara 100.

      * *[!UICONTROL Algorithmic]:* Roterar kreatörerna i varje paket algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

1. För varje ytterligare schema:

   1. Klicka på **[!UICONTROL + Add Schedule]**.

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreativt paket som ska läggas till i det första schemat.

   1. Ange start- och slutdatum för schemat.

   1. Välj den kreativa rotationstypen:

      * *[!UICONTROL Weighted]:* Roterar kreatörerna i varje paket manuellt enligt relativa vikter. Ange vikten för varje paket som en procentandel. Vikten för alla valda paket måste vara 100.

      * *[!UICONTROL Algorithmic]:* Roterar kreatörerna i varje paket algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Tilldela och ta bort tilldelning av kreativa paket till en slutlig nod i en upplevelse](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Anpassa URL:er för spårning för kreatörer](/help/creative/experiences/experience-tracking-urls-targeting.md)
