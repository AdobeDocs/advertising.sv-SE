---
title: Anpassa den kreativa optimeringen och planeringen för en upplevelse
description: Lär dig hur
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 4d0f4b2a46a65c7fa1afec0a4ef419e58b8f8f59
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Anpassa den kreativa optimeringen och planeringen för en upplevelse utan målgruppsanpassning för beslutsträd

*Endast upplevelser med befintliga kreatörer*
*Stängd beta*

Som standard bestäms den kreativa rotationen för en annonsupplevelsetagg algoritmiskt för att optimera den övergripande klickfrekvensen, och inställningarna för den kreativa optimeringen gäller för alla tilldelade kreatörer. Du kan anpassa den kreativa rotationen för att manuellt köra de kreativa objekten enligt relativa vikter eller för att algoritmiskt optimera för ett specifikt Advertising DSP-mål. <!-- verify --> Du kan också schemalägga att specifika kreatörer ska köras under angivna, sekventiella tidsperioder och tillämpa anpassade inställningar för kreativ rotation för varje schema.

## Konfigurera kreativ optimering utan schemaläggning

När den kreativa planeringen är inaktiverad gäller inställningarna för den kreativa optimeringen för alla tilldelade kreatörer.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. Gör något av följande:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Tag Manager]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Tag Manager]**

1. Håll markören över raden för den tillämpliga annonstaggen och klicka på ![Lägg till schema](/help/creative/assets/edit-gray.png "Redigera spårnings-URL:er") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tagghanteraren har bara en listvy, men ingen kortvy, från och med 2/2. >

1. Inaktivera **[!UICONTROL Schedule]**.

1. Välj den kreativa rotationstypen:

   * &amp;ast;&amp;ast; *Viktad* &amp;ast;&amp;ast; - Roterar kreatörerna manuellt enligt relativa vikter. Ange vikten för varje kreatör som en procentandel. Vikten för alla utvalda kreatörer måste vara upp till 100.

   * &amp;ast;&amp;ast; *Algoritmisk* &amp;ast;&amp;ast; - roterar kreatörerna algoritmiskt enligt ett angivet optimeringsmål.

      * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Klicka på **[!UICONTROL Save]**.

## Konfigurera kreativ optimering med kreativ planering

Du kan också schemalägga specifika kreatörer som används för en annonsupplevelsetagg att köras under angivna, sekventiella tidsperioder mellan upplevelsens start- och slutdatum, och använda anpassade kreativa rotationsinställningar för varje schema. Du kan till exempel schemalägga att Creative 1 ska köras under de första två veckorna för att optimera klickfrekvensen och att Creative 2 ska köras under de följande två veckorna för att optimera för ett visst anpassat mål.

När du använder schemaläggning måste du schemalägga kreatörerna under hela upplevelsen.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. Gör något av följande:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Tag Manager]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Tag Manager]**

1. Håll markören över raden för den tillämpliga annonstaggen och klicka på ![Lägg till schema](/help/creative/assets/edit-gray.png "Redigera spårnings-URL:er") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tagghanteraren har bara en listvy, men ingen kortvy, från och med 2/2. >

1. Aktivera **[!UICONTROL Schedule]**.

1. För det första schemat:

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreatör som ska läggas till i det första schemat.

   1. Ange start- och slutdatum för schemat.

   1. Välj den kreativa rotationstypen:

      * &amp;ast;&amp;ast; *Viktad* &amp;ast;&amp;ast; - Roterar kreatörerna manuellt enligt relativa vikter. Ange vikten för varje kreatör som en procentandel. Vikten för alla utvalda kreatörer måste vara upp till 100.

      * &amp;ast;&amp;ast; *Algoritmisk* &amp;ast;&amp;ast; - roterar kreatörerna algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. För varje ytterligare schema:

   1. Klicka på **[!UICONTROL + Add Schedule]**.

   1. I den vänstra kolumnen markerar du kryssrutan bredvid varje kreatör som ska läggas till i det första schemat.

   1. Ange start- och slutdatum för schemat.

   1. Välj den kreativa rotationstypen:

      * &amp;ast;&amp;ast; *Viktad* &amp;ast;&amp;ast; - Roterar kreatörerna manuellt enligt relativa vikter. Ange vikten för varje kreatör som en procentandel. Vikten för alla utvalda kreatörer måste vara upp till 100.

      * &amp;ast;&amp;ast; *Algoritmisk* &amp;ast;&amp;ast; - roterar kreatörerna algoritmiskt enligt ett angivet optimeringsmål.

         * För **[!UICONTROL Optimization Goal]** väljer du antingen *[!UICONTROL Click Through Rate]* eller *[!UICONTROL Custom Objective]*.  Om du väljer *[!UICONTROL Custom Objective]* väljer du ett befintligt anpassat [Advertising DSP-mål](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Skapa en annonstagg manuellt för en tillämplig kreativ storlek](/help/creative/experiences/experience-tag-create-manually.md)
>* [Tilldela kreatörer till en annonstagg för upplevelser utan målinriktning](experience-tag-assign-creatives.md)
>* [Anpassa spårnings-URL:er för en upplevelse utan mål för beslutsträd](experience-tracking-urls-no-targeting.md)
