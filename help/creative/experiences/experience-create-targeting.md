---
title: Skapa en upplevelse med målgruppsanpassning i beslutsträd
description: Lär dig skapa en riktad annonsupplevelse med hjälp av ett beslutsträd.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 7031347edb4491a91d622c0357ea2d3fb63f0a8a
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Skapa en upplevelse med målgruppsanpassning i beslutsträd

Skapa en riktad annonsupplevelse med hjälp av ett beslutsträd. För varje upplevelse används annonser från ett enda kreativt bibliotek.

>[!NOTE]
>
>* När du väl har skapat en målinriktad upplevelse kan du inte ändra den senare till en upplevelse som inte är målinriktad och som använder ett annat arbetsflöde.
>* Se till att era annonsupplevelser innehåller målgruppsanpassning som är kompatibel med de kampanjer ni ska implementera den i. Hierarkisk målinriktning kan variera beroende på DSP. När du överför en annonsupplevelsetagg till Advertising DSP och bifogar den till en placering läggs annonsupplevelseanpassning till (inte i stället för) på placeringsnivå. Om en placering till exempel riktar sig till användare i Australien och en annons riktar sig till användare i Japan, kommer annonsen att rikta sig till grenen&quot;Alla andra&quot;.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create New Experience]**.

1. Ange de [allmänna upplevelseinställningarna](experience-settings-targeting.md).

1. Klicka på **[!UICONTROL Create]**.

1. Gör följande i beslutsträdet:

   1. (Valfritt) Ändra vyinställningarna för beslutsträdet.

      Dina inställningar sparas tills du loggar ut.

      * Zooma in eller ut genom att flytta skjutreglaget.

      * Växla mellan att visa en lodrät lista och en vågrät lista genom att klicka på ![Visa som lodrätt träd](/help/creative/assets/tree-vertical.png "Visa som lodrätt träd") respektive ![Visa som vågrätt träd](/help/creative/assets/tree-horizontal.png "Visa som vågrätt träd").

   1. (Valfritt) Ställ in annonsmålen och motsvarande kreativa alternativ på något av följande sätt:

      * Målgrupper:

         * [Lägg till en målnod på den sista nivån](experience-target-node-add-final.md).

         * [Infoga en målnod mellan noder](experience-target-node-add-inner.md).

         * [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md).

         * [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md).

      * Creative-paket:

         * [Tilldela och ta bort tilldelning av kreatörer till en slutlig nod](experience-assign-creative-bundles.md).

           Om du inte tilldelar minst ett paket till varje slutnod kan du välja att använda standardalternativen för varje otilldelad nod när du sparar upplevelsen. Om du vill publicera en upplevelse måste du antingen tilldela paket eller använda standardkreatörerna för varje slutlig nod.

         * [Anpassa URL:er för spårning för kreatörer i de tilldelade paketen](experience-tracking-urls-targeting.md).

         * [Anpassa den kreativa optimeringen och schemaläggningen](experience-optimization-scheduling-targeting.md) för de tilldelade paketen.

1. (Valfritt) Växla mellan beslutsträdet och de allmänna inställningarna:

   * Klicka **[!UICONTROL Experience Form]** i det övre högra hörnet för att öppna de allmänna inställningarna från beslutsträdet.

   * Om du vill öppna beslutsträdet från de allmänna inställningarna klickar du på **[!UICONTROL Decision Tree]** i det övre högra hörnet.

1. Klicka på **[!UICONTROL Save]** och gör sedan följande.

   * (Om varje nod längst ned innehåller minst ett kreativt paket) klickar du på **[!UICONTROL OK]**.

   * (Om varje nod längst ned inte innehåller minst ett kreativt paket) Gör något av följande:

      * Om du vill spara upplevelsen utan alla nödvändiga kreativa paket klickar du på **[!UICONTROL Save as Draft]**.

        Du kan inte skapa en annonstagg för en [utkastupplevelse](experience-about.md#experience-statuses).

      * Om du vill tilldela standardkreativiteten till varje mål som inte redan har tilldelats ett kreativt paket klickar du på **[!UICONTROL Assign Default Creatives]**. När du har granskat det uppdaterade trädet med tilldelade standardkreatörer klickar du på **[!UICONTROL Save]** och **[!UICONTROL OK]**.

      * Klicka på **[!UICONTROL Continue Edit]** om du vill fortsätta redigera beslutsträdet.

När upplevelsen är aktiv skapar [!DNL Creative] automatiskt en annonstagg för varje tillämplig kreativ storlek eller videons längd. Du kan sedan [exportera en annonstagg och implementera den i en DSP](/help/creative/experiences/experience-tag-export.md).

För videoreklamupplevelser omkodas videokreatörer automatiskt av Adobe Advertising DSP som VAST 2.0-taggar så att du kan förhandsgranska dem. Du kan [använda omkodning för en annan DSP](experience-tag-video-transcoding.md) för alla taggar för videoannonser.

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
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
