---
title: Lägga till en målnod mellan noder i en upplevelse
description: Lär dig hur du lägger till en målnod mellan målböcker i en annonsupplevelse.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: 05bcaa63779856cfea2f9cd3a0ab5d5e9d3d472a
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 0%

---

# Lägga till en målnod mellan noder i en upplevelse

*Upplevelser med endast mål för beslutsträd*
*Stängd beta*

När du infogar en målnod mellan befintliga nivåer, behåller den nya målnoden alla befintliga underordnade mål och kreatörer och den nya noden kallas inledningsvis&quot;Alla&quot;. Du kan också behålla den nya noden utan att lägga till mer specifika mål.

Om du vill definiera ett specifikt mål lägger du till ytterligare en målnod på samma nivå, anger det nya målet och tilldelar sedan kreatörer till just det målet. Om du lägger till en målnod på samma nivå skapas den nya målnoden och alla underordnade mål och kreatörer som tidigare tilldelats till All flyttas till en ny&quot;Allt annat&quot;-nod på samma nivå. På så sätt påverkar inte tillägget av det nya målet de befintliga underordnade grenarna eftersom det bara är den nya noden på samma nivå som inkluderar den nya målinformationen.

>[!NOTE]
>
>Om du vill lägga till en målnod på den nedersta nivån i ett beslutsträd ska du läsa &quot;[Lägg till en målnod på den sista nivån i en upplevelse](experience-target-node-add-final.md)&quot;.

<!-- 1. [ways to get to the decision tree] -->

1. Klicka på ![Lägg till](/help/creative/assets/add.png "Lägg till") under den nod där du vill infoga målet och välj sedan **[!UICONTROL Insert New Target]**.

1. Gör något av följande:

   * Om det inte redan finns några noder på samma nivå gör du följande:

      1. Markera måltypen och klicka sedan på **[!UICONTROL Apply]**:

         * För Adobe målgrupper väljer du **[!UICONTROL Adobe Audience]**.

         * För geografiska mål väljer du en enda geografisk kategori (till exempel [!UICONTROL Geo: Country]).

         * Välj **[!UICONTROL Data Pass]** för mål för dataöverföring.

         * Välj **[!UICONTROL RT Pixel] för återmarknadsföring av pixelmål.

         * Välj en målkategori (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** eller **[!UICONTROL Device: Browser]**) för enhetsmål.

   * Om det redan finns noder på samma nivå gör du följande:

      * Gör följande för Adobe Audience-mål:

         1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Audience Targeting]-alternativ, öppna fliken **[!UICONTROL Adobe Segments]**, ange en eller flera av annonsörens [!DNL Adobe] målgrupper och klicka sedan på **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.

         1. (Valfritt) Om du vill skapa flera målnoder när flera målgrupper har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

            Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angiven målgrupp. Om du inte delar upp målen måste användaren tillhöra alla angivna målgrupper (en [!DNL Boolean] `AND` -sats).

         1. Klicka på **[!UICONTROL Apply]**.

      * För geografiska mål gör du följande:

         1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Geo Targeting]-alternativ, ange ett eller flera av de geografiska målen och klicka sedan på **[!UICONTROL Save]**.

            Postkodsmål har gruppredigeringsalternativ. Om du vill klistra in flera postnummer klickar du på fliken **[!UICONTROL Paste postal codes]**, markerar landet, klistrar in eller anger postnummer avgränsade med kommatecken eller på separata rader och klickar sedan på **[!UICONTROL Include All]**. Om du vill ta bort ett inkluderat postkodsmål håller du markören över målet och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Remove]**.

         1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

            Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

         1. Klicka på **[!UICONTROL Apply]**.

      * Om du vill anpassa datapassnyckeln för ett datapassemål anger du ett enda datapassvärde och klickar sedan på **[!UICONTROL Apply]**.

        Ett standardvärde för nyckeln i nyckelvärdepar har redan angetts i fältet **[!UICONTROL Data Pass]** i avsnittet [!UICONTROL Advanced] i [upplevelseinställningarna](experience-settings-targeting.md). Du kan också anpassa tangenten.

      * Om du vill återanvända ett pixelmål väljer du en enda återmarknadsföringspixel och värdena för något av pixelattributen som krävs för att visa de kreativa. Klicka sedan på **[!UICONTROL Apply]**.

        Attributen för återmarknadsföringspixeln konfigureras i [inställningarna för återmarknadsföring av pixlar](/help/creative/pixels/retargeting-pixel-manage.md).

      * Gör följande för enhetsmål:

         1. Välj mål.

         1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

            Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

         1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         1. Klicka på **[!UICONTROL Apply]**.

1. Gör något av följande:

   * (Valfritt) [Tilldela kreatörer](experience-assign-creative-bundles.md) till den nya målnoden och till noden&quot;Allt annat&quot;.

   * (Valfritt) [Lägg till en målnod på samma nivå](experience-target-node-add-sibling.md) med den angivna måltypen.

   * (Valfritt) Så här sparar du upplevelsen:

      1. Klicka på **[!UICONTROL Save]** och sedan på **[!UICONTROL OK]**.

      1. (Om varje nod längst ned inte innehåller minst en kreativ nod): Gör något av följande:

         * Om du vill spara upplevelsen utan alla nödvändiga kreativa paket klickar du på **[!UICONTROL Save as Draft]**.

           Du kan inte skapa en annonstagg för en utkastupplevelse.

         * Om du vill tilldela standardkreativiteten till varje mål som inte redan har tilldelats ett kreativt paket klickar du på **[!UICONTROL Assign Default Creatives]**. När du har granskat det uppdaterade trädet med tilldelade standardkreatörer klickar du på **[!UICONTROL Save]** och **[!UICONTROL OK]**.

         * Klicka på **[!UICONTROL Continue Edit]** om du vill fortsätta redigera beslutsträdet.

>[!MORELIKETHIS]
>
>* [Lägg till en målnod på den sista nivån](experience-target-node-add-final.md)
>* [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md)
>* [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md)
>* [Tilldela kreatörer till en slutlig nod](experience-assign-creative-bundles.md)
>* [Ta bort en målnod eller en kreativ lövnod](/help/creative/experiences/experience-target-node-delete.md)
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
>* [Inställningar för anpassad upplevelse](experience-settings-targeting.md)
