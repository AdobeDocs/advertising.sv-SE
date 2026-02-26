---
title: Anpassa den kreativa optimeringen och planeringen för en upplevelse
description: Lär dig hur du konfigurerar optimering och annonsplanering för riktade upplevelser.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# Anpassa den kreativa optimeringen och planeringen för en upplevelse med målgruppsanpassning i beslutsträd

*Endast målnoder med befintliga kreatörer*

Som standard bestäms den kreativa rotationen för en upplevelse algoritmiskt för att optimera den övergripande klickfrekvensen, och inställningarna för den kreativa optimeringen gäller för alla tilldelade paket. Du kan alternativt algoritmiskt optimera för ett visst anpassat Advertising DSP-mål, rotera paket enligt en angiven paketsekvens, med ett visst antal visningar för varje paketsekvens eller enligt relativa vikter. Du kan också schemalägga att specifika kreativa programpaket ska köras under angivna, sekventiella tidsperioder och tillämpa anpassade inställningar för kreativ rotation för varje schema.

>[!NOTE]
>
>De här funktionerna är inte tillgängliga för noder som använder standardkreatörerna i stället för tilldelade kreatörer.

## Konfigurera kreativ optimering utan schemaläggning

När den kreativa planeringen är inaktiverad gäller inställningarna för den kreativa optimeringen för alla tilldelade kreatörer.

1. Öppna inställningarna för kreativ optimering när du [skapar](experience-create-targeting.md) eller [redigerar](experience-edit-targeting.md) upplevelsen:

   1. Håll markören över den kreativa bladnoden under målnoden och gör följande:

      * Klicka **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** för befintliga paket.

      * Klicka på **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** och [tilldela paketen](experience-assign-creative-bundles.md) för nya paket.

1. Klicka på fliken **[!UICONTROL Creative Optimization]**.

1. Inaktivera **[!UICONTROL Schedule]**.

1. Välj den kreativa rotationstypen för annonsvarianter i de associerade paketen:

   * *[!UICONTROL Weighted]:* Visar annonsvarianter i associerade kreativa paket enligt relativa vikter. Ange vikten för varje paket som en procentandel. Om du vill tillämpa samma vikt på alla associerade paket klickar du på (![Använd samma vikt](/help/creative/assets/apply-equal-weight.png "Använd samma vikt")). Vikten för alla valda paket måste vara upp till 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* Visar de mest effektiva annonsvarianterna oftare, baserat på ett angivet mål.

      * För **[!UICONTROL Optimization Goal]** väljer du *[!UICONTROL Click Through Rate]*, (standardvideoreklam) *[!UICONTROL Completion Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* Visar de associerade kreativa paketen i en angiven ordning (med paket 1 aktiverat först, paket 2 levererat sekund och så vidare), med ett angivet totalt antal visningar för varje paketsekvens. Annonsstorlekarna som hanteras bestäms av det tillgängliga lagret. Du kan konfigurera det slutliga paketet i sekvensen till en\) som ska visas oändligt (standard) eller b\) som en slinga tillbaka till det första paketet. Du kan till exempel visa alla annonsvarianter i programpaket 1 för tre (3) visningar, sedan visa valfri annonsvariant i programpaket 2 för ett (1) intryck, sedan visa någon av annonsvarianterna i programpaket 3 för två (2) visningar och sedan börja om från början. När annonsvarianterna i Bundle 3 visas kan du fortsätta att visa annonsvarianterna i Bundle 3 i oändlighet, i stället för att skapa en slinga. När du aktiverar sekvensering:

      1. Dra och släpp de tilldelade paketen i önskad ordning.

     Som standard ordnas de tilldelade paketen i den ordning som de lades till i upplevelsen.

      1. Ange antalet visningar för varje sekvens.

      1. För den sista sekvensen ändrar du om du vill visa det slutliga paketet i sekvensen i oändlig (*[!UICONTROL Infinite]* (standard) eller b\)-slinga tillbaka till det första paketet efter att det sista paketet visas (*[!UICONTROL Keep in Loop]*).

1. Klicka på **[!UICONTROL Save]**.

## Konfigurera kreativ optimering med kreativ planering

Du kan också schemalägga att specifika kreativa programpaket ska köras under angivna, sekventiella tidsperioder mellan start- och slutdatumet för upplevelsen och använda anpassade kreativa rotationsinställningar för varje schema. Du kan till exempel schemalägga att paket 1 ska köras under de första två veckorna för att optimera klickfrekvensen och paket 2 ska köras under de följande två veckorna för att optimera för ett visst anpassat mål.

När du använder schemaläggning måste du schemalägga paket under hela upplevelsen.

1. Öppna inställningarna för kreativ optimering när du [skapar](experience-create-targeting.md) eller [redigerar](experience-edit-targeting.md) upplevelsen:

   1. Håll markören över den kreativa bladnoden under målnoden och gör följande:

      * Klicka **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** för befintliga paket.

      * Klicka på **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** och [tilldela paketen](experience-assign-creative-bundles.md) för nya paket.

1. Klicka på fliken **[!UICONTROL Creative Optimization]**.

1. Aktivera **[!UICONTROL Schedule]**.

1. För det första schemat:

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreativt paket som ska läggas till i det första schemat.

   1. Ange startdatum och starttid samt slutdatum och sluttid för schemat.

   1. Välj den kreativa rotationstypen:

      * *[!UICONTROL Weighted]:* Roterar kreatörerna i varje paket manuellt enligt relativa vikter. Ange vikten för varje paket som en procentandel. Om du vill tillämpa samma vikt på alla paket i schemat klickar du på (![Använd samma vikt](/help/creative/assets/apply-equal-weight.png "Använd samma vikt")). Vikten för alla valda paket måste vara 100.

      * *[!UICONTROL Algorithmic]:* Roterar kreatörerna i varje paket algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du *[!UICONTROL Click Through Rate]*, (standardvideoreklam) *[!UICONTROL Completion Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Roterar de associerade kreativa paketen i en angiven ordning (där Paket 1 har opererats först, Paket 2 har sedermera), med ett angivet totalt antal visningar för varje paketsekvens. Annonsstorlekarna som hanteras bestäms av det tillgängliga lagret. Du kan konfigurera det slutliga paketet i sekvensen till en\) som ska visas oändligt (standard) eller b\) som en slinga tillbaka till det första paketet. Du kan t.ex. visa någon av de kreativa i paket 1 för tre (3) visningar, sedan visa valfri kreativ i paket 2 för ett (1) intryck, sedan visa någon av de kreativa i paket 3 för två (2) visningar och sedan börja om från början. När de som skapat paketet 3 visas kan du i stället fortsätta att visa de som skapat paketet i oändlighet 3 i stället för att skapa en slinga. När du aktiverar sekvensering:

         1. Dra och släpp de tilldelade paketen i önskad ordning.

            Som standard ordnas de tilldelade paketen i den ordning som de lades till i upplevelsen.

         1. Ange antalet visningar för varje sekvens.

         1. För den sista sekvensen ändrar du om du vill visa det slutliga paketet i sekvensen i oändlig (*[!UICONTROL Infinite]* (standard) eller b\)-slinga tillbaka till det första paketet efter att det sista paketet visas (*[!UICONTROL Keep in Loop]*).

1. För varje ytterligare schema:

   1. Klicka på **[!UICONTROL + Add Schedule]**.

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreativt paket som ska läggas till i det första schemat.

   1. Ange start- och slutdatum för schemat.

   1. Välj den kreativa rotationstypen:

      * *[!UICONTROL Weighted]:* Roterar kreatörerna i varje paket manuellt enligt relativa vikter. Ange vikten för varje paket som en procentandel. Vikten för alla valda paket måste vara 100.

      * *[!UICONTROL Algorithmic]:* Roterar kreatörerna i varje paket algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Roterar de associerade kreativa paketen i en angiven ordning, med ett angivet totalt antal visningar för varje paketsekvens. När du aktiverar sekvensering:

         1. Dra och släpp de tilldelade paketen i önskad ordning.

            Som standard ordnas de tilldelade paketen i den ordning som de lades till i upplevelsen.

         1. Ange antalet visningar för varje sekvens.

         1. För den sista sekvensen ändrar du om du vill visa det slutliga paketet i sekvensen i oändlig (*[!UICONTROL Infinite]* (standard) eller b\)-slinga tillbaka till det första paketet efter att det sista paketet visas (*[!UICONTROL Keep in Loop]*).

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Tilldela och ta bort tilldelning av kreativa paket till en slutlig nod i en upplevelse](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Anpassa URL:er för spårning för kreatörer](/help/creative/experiences/experience-tracking-urls-targeting.md)
