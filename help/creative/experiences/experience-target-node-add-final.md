---
title: Lägg till en målnod till den sista nivån i en upplevelse
description: Lär dig hur du lägger till en målnod på den slutliga målnivån i en annonsupplevelse.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Lägg till en målnod till den sista nivån i en upplevelse

*Upplevelser med endast mål för beslutsträd*

När du lägger till en målnod på den understa nivån i upplevelsen, oavsett om det är rotnoden&quot;Alla&quot;, en målspecifik nod eller en&quot;Allt annat&quot;-nod, definierar du målet direkt och behöver inte skapa en jämställd nod. Om du lägger till en nod på den nedersta nivån skapas målnoden och en annan&quot;Allt annat&quot;-nod på samma nivå.

>[!NOTE]
>
>Om du vill infoga en målnod mellan befintliga nivåer i ett beslutsträd ska du läsa &quot;[Infoga en målnod mellan noder i en upplevelse](experience-target-node-add-inner.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Klicka på ![Lägg till](/help/creative/assets/add.png "Lägg till") under den nod där du vill infoga målet och välj sedan **[!UICONTROL Insert New Target]**.

1. Ange mål:

   * För målgrupper väljer du **[!UICONTROL Audience]**, klickar på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Audience Targeting]-alternativ och gör sedan följande:

      * Om du vill lägga till det första segmentet letar du reda på segmentet i den vänstra panelen och markerar kryssrutan bredvid segmentnamnet.

      * Lägga till ett segment i en befintlig segmentgrupp:

         1. Klicka på segmentgruppen på den högra panelen.

         1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* eller *[!UICONTROL Exclude All]* efter behov.

            *[!UICONTROL Exclude All]* är inte tillgänglig för den första segmentgruppen. För en målgrupp som endast innehåller undantag kan du skapa den här målgruppen som *[!UICONTROL Include Any]* och sedan exkludera den målgruppen när du lägger till den på en plats i din DSP.

         1. Leta reda på det nya segmentet i den vänstra panelen och markera kryssrutan bredvid segmentnamnet.

            Segmentgruppen uppdateras automatiskt med det nya segmentet.

      * Så här lägger du till en ny segmentgrupp:

         1. Klicka på **[!UICONTROL + New Group]** i den högra panelen.

         1. (Valfritt) Ändra logiken mellan den föregående gruppen och den nya gruppen till *[!UICONTROL And]* eller *[!UICONTROL Or]* efter behov.

         1. Leta reda på segmenten för den nya gruppen i den vänstra panelen och markera kryssrutorna bredvid segmentnamnen.

         1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* eller *[!UICONTROL Exclude All]* efter behov.

      1. Klicka på **[!UICONTROL Create]**.

      1. Klicka på **[!UICONTROL Apply]**.

   * För geografiska mål väljer du en enda geografisk kategori (till exempel [!UICONTROL Geo: Country]) och gör sedan följande:

      1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Geo Targeting]-alternativ, ange ett eller flera av de geografiska målen och klicka sedan på **[!UICONTROL Save]**.

         Postkodsmål har gruppredigeringsalternativ. Om du vill klistra in flera postnummer klickar du på fliken **[!UICONTROL Paste postal codes]**, markerar landet, klistrar in eller anger postnummer avgränsade med kommatecken eller på separata rader och klickar sedan på **[!UICONTROL Include All]**. Om du vill ta bort ett inkluderat postkodsmål håller du markören över målet och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Remove]**.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

      1. Klicka på **[!UICONTROL Apply]**.

   * För ett datapassmål väljer du **[!UICONTROL Data Pass]**, alternativt anpassar du datapassnyckeln, anger ett enda datapassvärde och klickar sedan på **[!UICONTROL Apply]**.

   Ett standardvärde för nyckeln i nyckelvärdepar har redan angetts i fältet **[!UICONTROL Data Pass]** i avsnittet [!UICONTROL Advanced] i [upplevelseinställningarna](experience-settings-targeting.md). Du kan också anpassa tangenten.

   * Om du vill återanvända ett pixelmål väljer du **[!UICONTROL RT Pixel]**, markerar en enda återmarknadsföringspixel och värdena för någon av pixelattributen som krävs för att visa de kreativa och klickar sedan på **[!UICONTROL Apply]**.

     Attributen för återmarknadsföringspixeln konfigureras i [inställningarna för återmarknadsföring av pixlar](/help/creative/pixels/retargeting-pixel-manage.md).

   * Gör följande för enhetsmål:

      1. Välj en enda målkategori (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** eller **[!UICONTROL Device: Browser]**) och välj sedan målen.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

      1. Klicka på **[!UICONTROL Apply]**.

1. (Valfritt) Ange ett eget grennamn för en användardefinierad gren.

   Som standard är användardefinierade grenar märkta med de angivna målen.

   Du kan inte skapa ett anpassat grennamn för en Alla eller Alla andra grenar.

   1. Håll markören över målnoden och klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Ange **[!UICONTROL Node Name]** och klicka sedan på **[!UICONTROL Save]**.

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
