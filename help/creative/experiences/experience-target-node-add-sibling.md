---
title: Lägga till en målnod på samma nivå mellan noder i en upplevelse
description: Lär dig hur du lägger till en nod på samma nivå i en nod som har ett mål eller som finns på samma nivå som en nod med ett mål.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: f71747a4973ec3f3e2c3a8a5913d27311849883c
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Lägga till en målnod på samma nivå mellan noder i en upplevelse

*Upplevelser med endast mål för beslutsträd*
*Stängd beta*

Du kan lägga till en nod på samma nivå i alla noder som har ett mål eller som är på samma nivå som en nod med ett mål.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Ovanför noden där du vill lägga till noden på samma nivå klickar du på ![Lägg till](/help/creative/assets/add.png "Lägg till") och väljer sedan **[!UICONTROL Insert Sibling Target]**.

1. Ange mål:

   * Gör följande för målgrupper:

      1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Audience Targeting]-alternativ och gör sedan följande:

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

   * För geografiska mål gör du följande:

      1. Klicka på **[!UICONTROL Click to Browse]** för att öppna dina [!UICONTROL Geo Targeting]-alternativ, ange ett eller flera av de geografiska målen och klicka sedan på **[!UICONTROL Save]**.

         Postkodsmål har gruppredigeringsalternativ. Om du vill klistra in flera postnummer klickar du på fliken **[!UICONTROL Paste postal codes]**, markerar landet, klistrar in eller anger postnummer avgränsade med kommatecken eller på separata rader och klickar sedan på **[!UICONTROL Include All]**. Om du vill ta bort ett inkluderat postkodsmål håller du markören över målet och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Remove]**.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

      1. Klicka på **[!UICONTROL Apply]**.

   * Om du vill anpassa nyckeln för dataöverföring anger du ett värde för dataöverföring och klickar sedan på **[!UICONTROL Apply]**.

     Ett standardvärde för nyckeln i nyckelvärdepar har redan angetts i fältet **[!UICONTROL Data Pass]** i avsnittet [!UICONTROL Advanced] i [upplevelseinställningarna](experience-settings-targeting.md). Du kan också anpassa tangenten.

   * Om du vill återanvända pixelmål markerar du den återmarknadsföringspixel som ska användas och de värden som krävs för något av pixelattributen som måste finnas för att visa de kreativa. Klicka sedan på **[!UICONTROL Apply]**.

     Attributen för återmarknadsföringspixeln konfigureras i [inställningarna för återmarknadsföring av pixlar](/help/creative/pixels/retargeting-pixel-manage.md).

   * Gör följande för enhetsmål:

      1. Välj mål.

      1. (Valfritt) Om du vill skapa flera målnoder när flera geografiska mål har angetts väljer du **[!UICONTROL Split targets to create nodes]**.

         Den här funktionen skapar en separat målnod (med separata kreativa paket) för varje angivet geografiskt mål. Om du inte delar upp målen måste användaren tillhöra alla angivna platser (en [!DNL Boolean] `AND` -sats).

      1. Klicka på **[!UICONTROL Apply]**.

1. (Valfritt) Ange ett eget grennamn för en användardefinierad gren.

   Som standard är användardefinierade grenar märkta med de angivna målen.

   Du kan inte skapa ett anpassat grennamn för en Alla eller Alla andra grenar.

   1. Håll markören över målnoden och klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Ange **[!UICONTROL Node Name]** och klicka sedan på **[!UICONTROL Save]**.

1. Gör något av följande:

   * (Valfritt) [Tilldela kreatörer](experience-assign-creative-bundles.md) till den nya målnoden.

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
>* [Infoga en målnod mellan noder](experience-target-node-add-inner.md)
>* [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md)
>* [Tilldela kreatörer till en slutlig nod](experience-assign-creative-bundles.md)
>* [Ta bort en målnod eller en kreativ lövnod](/help/creative/experiences/experience-target-node-delete.md)
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
>* [Inställningar för anpassad upplevelse](experience-settings-targeting.md)
