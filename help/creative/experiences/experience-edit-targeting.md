---
title: Redigera en upplevelse med målgruppsanpassning i beslutsträd
description: Lär dig hur du redigerar inställningarna för en riktad annonsupplevelse med hjälp av ett beslutsträd.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: 47a230347059a26c6c1c2db7c73306a376062478
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Redigera en upplevelse med målgruppsanpassning i beslutsträd

*Stängd beta*

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika upplevelser.

1. Gör något av följande:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Edit]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Edit]**.

   Beslutsträdet öppnas som standard.

1. (Valfritt) Växla mellan beslutsträdet och de allmänna inställningarna efter behov:

   * Klicka **[!UICONTROL Experience Form]** i det övre högra hörnet för att öppna de allmänna inställningarna från beslutsträdet.

   * Om du vill öppna beslutsträdet från de allmänna inställningarna klickar du på **[!UICONTROL Decision Tree]** i det övre högra hörnet.

1. (Valfritt) Gör något av följande om du vill redigera beslutsträdet:

   * ([Bearbetar](experience-about.md#experience-statuses)-upplevelser) Gör något av följande:

      * Klicka på **[!UICONTROL Discard and start again]** om du vill ignorera de befintliga, ej bokförda ändringarna i direktuppspelningen.

      * Om du vill behålla de befintliga, ej bokförda ändringarna klickar du på **[!UICONTROL Continue editing draft]**.

      * Om du vill redigera upplevelseinformationen klickar du på **[!UICONTROL Edit Experience Details]**.

   * (Valfritt) Ändra vyinställningarna för beslutsträdet.

     Dina inställningar sparas tills du loggar ut.

   * Zooma in eller ut genom att flytta skjutreglaget.

   * Växla mellan att visa en lodrät lista och en vågrät lista genom att klicka på ![Visa som lodrätt träd](/help/creative/assets/tree-vertical.png "Visa som lodrätt träd") respektive ![Visa som vågrätt träd](/help/creative/assets/tree-horizontal.png "Visa som vågrätt träd").

   * (Valfritt) Ändra annonsmålen och motsvarande alternativ på något av följande sätt:

      * Målgrupper:

        *[Lägg till en målnod på den sista nivån](experience-target-node-add-final.md) i en upplevelse.

         * [Infoga en målnod mellan noder](experience-target-node-add-inner.md).

         * [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md).

         * [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md).

      * Creative-paket:

         * [Tilldela och ta bort tilldelning av kreatörer till en slutlig nod](experience-assign-creative-bundles.md).

           Om du inte tilldelar minst ett paket till varje slutnod kan du välja att använda standardalternativen för varje otilldelad nod när du sparar upplevelsen. Om du vill publicera en upplevelse måste du antingen tilldela paket eller använda standardkreatörerna för varje slutlig nod.

         * [Anpassa URL:er för spårning för kreatörer i de tilldelade paketen](experience-tracking-urls-targeting.md).

         * [Anpassa den kreativa optimeringen och schemaläggningen](experience-optimization-scheduling-targeting.md) för de tilldelade paketen.

1. (Valfritt) Redigera de [allmänna upplevelseinställningarna](experience-settings-targeting.md).

1. Klicka på **[!UICONTROL Save]** och gör sedan följande.

   * (Om varje nod längst ned innehåller minst ett kreativt paket) klickar du på **[!UICONTROL OK]**.

   * (Om varje nod längst ned inte innehåller minst ett kreativt paket) Gör något av följande:

      * Om du vill spara upplevelsen utan alla nödvändiga kreativa paket klickar du på **[!UICONTROL Save as Draft]**.

        Du kan inte skapa en annonstagg för en [utkastupplevelse](experience-about.md#experience-statuses).

      * Om du vill tilldela standardkreativiteten till varje mål som inte redan har tilldelats ett kreativt paket klickar du på **[!UICONTROL Assign Default Creatives]**. När du har granskat det uppdaterade trädet med tilldelade standardkreatörer klickar du på **[!UICONTROL Save]** och **[!UICONTROL OK]**.

      * Klicka på **[!UICONTROL Continue Edit]** om du vill fortsätta redigera beslutsträdet.

>[!MORELIKETHIS]
>
>* [Inställningar för anpassad upplevelse](experience-settings-targeting.md)
>* [Lägg till en målnod på den sista nivån](experience-target-node-add-final.md)
>* [Infoga en målnod mellan noder](experience-target-node-add-inner.md)
>* [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md)
>* [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md)
>* [Tilldela kreatörer till en slutlig nod](experience-assign-creative-bundles.md)
>* [Anpassa URL:er för spårning för kreatörer i de tilldelade paketen](experience-tracking-urls-targeting.md)
>* [Anpassa kreativ optimering och schemaläggning](experience-optimization-scheduling-targeting.md)
>* [Exportera och implementera en annonsupplevelsetagg för en liveupplevelse](/help/creative/experiences/experience-tag-export.md)
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
