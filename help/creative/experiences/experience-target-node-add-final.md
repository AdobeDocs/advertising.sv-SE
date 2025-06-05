---
title: Lägg till en målnod till den sista nivån i en upplevelse
description: Lär dig hur du lägger till en målnod på den slutliga målnivån i en annonsupplevelse.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 9f93990bcd6b3c8f7d6fb29186da620ac6d4ecf5
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Lägg till en målnod till den sista nivån i en upplevelse

*Upplevelser med endast mål för beslutsträd*
*Stängd beta*

När du lägger till en målnod på den understa nivån i upplevelsen, oavsett om det är rotnoden&quot;Alla&quot;, en målspecifik nod eller en&quot;Allt annat&quot;-nod, definierar du målet direkt och behöver inte skapa en jämställd nod. Om du lägger till en nod på den nedersta nivån skapas målnoden och en annan&quot;Allt annat&quot;-nod på samma nivå.

>[!NOTE]
>
>Om du vill infoga en målnod mellan befintliga nivåer i ett beslutsträd ska du läsa &quot;[Infoga en målnod mellan noder i en upplevelse](experience-target-node-add-inner.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Klicka på ![Lägg till](/help/creative/assets/add.png "Lägg till") under den nod där du vill infoga målet och välj sedan **[!UICONTROL Insert New Target]**.

1. Ange mål:

   * För Adobe Audience-mål väljer du **[!UICONTROL Adobe Audience]** och gör sedan följande:

      1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Audience Targeting]-alternativ, öppna fliken **[!UICONTROL Adobe Segments]**, ange en eller flera av annonsörens [!DNL Adobe] målgrupper och klicka sedan på **[!UICONTROL Create]**.

      1. (Valfritt) Om du vill skapa flera målnoder när flera målgrupper har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angiven målgrupp. Om du inte delar upp målen måste användaren tillhöra alla angivna målgrupper.

      1. Klicka på **[!UICONTROL Apply]**.

   * För geografiska mål väljer du en enda geografisk kategori (till exempel [!UICONTROL Geo: Country]) och gör sedan följande:

      1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Geo Targeting]-alternativ, ange ett eller flera av de geografiska målen och klicka sedan på **[!UICONTROL Save]**.

         Postkodsmål har gruppredigeringsalternativ. Om du vill klistra in flera postnummer klickar du på fliken **[!UICONTROL Paste postal codes]**, markerar landet, klistrar in eller anger postnummer avgränsade med kommatecken eller på separata rader och klickar sedan på **[!UICONTROL Include All]**. Om du vill ta bort ett inkluderat postkodsmål håller du markören över målet och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Remove]**.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser.

      1. Klicka på **[!UICONTROL Apply]**.

   * För ett datapassmål väljer du **[!UICONTROL Data Pass]**, alternativt anpassar du datapassnyckeln, anger ett enda datapassvärde och klickar sedan på **[!UICONTROL Apply]**.

   Ett standardvärde för nyckeln i nyckelvärdepar har redan angetts i fältet **[!UICONTROL Data Pass]** i avsnittet [!UICONTROL Advanced] i [upplevelseinställningarna](experience-settings-targeting.md). Du kan också anpassa tangenten.

   * Om du vill återanvända ett pixelmål väljer du **[!UICONTROL RT Pixel]**, markerar en enda återmarknadsföringspixel och värdena för någon av pixelattributen som krävs för att visa de kreativa och klickar sedan på **[!UICONTROL Apply]**.

     Attributen för återmarknadsföringspixeln konfigureras i [inställningarna för återmarknadsföring av pixlar](/help/creative/pixels/retargeting-pixel-manage.md).

   * Gör följande för enhetsmål:

      1. Välj en enda målkategori (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** eller **[!UICONTROL Device: Browser]**) och välj sedan målen.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser.

      1. Klicka på **[!UICONTROL Apply]**.

1. Gör något av följande:

   * (Valfritt) [Tilldela kreatörer](experience-assign-creative-bundles.md) till den nya målnoden och till noden&quot;Allt annat&quot;.

   * (Valfritt) Så här sparar du upplevelsen:

      1. Klicka på **[!UICONTROL Save]** och sedan på **[!UICONTROL OK]**.

      1. (Om varje nod längst ned inte innehåller minst en kreativ nod): Gör något av följande:

         * Om du vill spara upplevelsen utan alla nödvändiga kreativa paket klickar du på **[!UICONTROL Save as Draft]**.

           Du kan inte skapa en annonstagg för en utkastupplevelse.

         * Om du vill tilldela standardkreativiteten till varje mål som inte redan har tilldelats ett kreativt paket klickar du på **[!UICONTROL Assign Default Creatives]**. När du har granskat det uppdaterade trädet med tilldelade standardkreatörer klickar du på **[!UICONTROL Save]** och **[!UICONTROL OK]**.

         * Klicka på **[!UICONTROL Continue Edit]** om du vill fortsätta redigera beslutsträdet.

>[!MORELIKETHIS]
>
>* [Infoga en målnod mellan noder](experience-target-node-add-inner.md)
>* [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md)
>* [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md)
>* [Tilldela kreatörer till en slutlig nod](experience-assign-creative-bundles.md)
>* [Ta bort en målnod eller en kreativ lövnod](/help/creative/experiences/experience-target-node-delete.md)
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
>* [Inställningar för anpassad upplevelse](experience-settings-targeting.md)
