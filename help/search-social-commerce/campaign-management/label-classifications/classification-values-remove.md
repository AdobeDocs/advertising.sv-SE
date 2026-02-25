---
title: Ta bort etikettklassificeringsvärden från kontokomponenter
description: Lär dig hur du tar bort associationer mellan etikettklassificeringsvärden och kontokomponenter.
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Ta bort etikettklassificeringsvärden från kontokomponenter

Om du tar bort ett klassificeringsvärde tas associationen med kontokomponenten och alla dess underordnade komponenter bort. Rapportdata för klassificeringsvärdet är inte längre tillgängliga för dessa komponenter. Om du tar bort ett klassificeringsvärde tas varken värdet eller kontokomponenterna bort.

>[!NOTE]
>
>Mer information om hur du tar bort ett värde från en etikettklassificering finns i [Ta bort etikettklassificeringsvärden](classification-values-delete.md).

## (Nytt användargränssnitt) Ta bort etikettklassificeringsvärden från kontokomponenter

Du kan ta bort klassificeringsvärden från alla tillämpliga kontokomponenter som är tillgängliga i det nya användargränssnittet.

1. Öppna entitetsvyn från menyn **[!UICONTROL Manage]** eller **[!UICONTROL Target]**.

1. Markera kryssrutan bredvid varje relevant rad.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på **-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]** i verktygsfältet för gruppåtgärder.

1. Markera kryssrutan bredvid varje klassificeringsvärde som ska tas bort från de markerade entiteterna.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Om du vill välja alla tilldelade värden klickar du på **[!UICONTROL Select All]**. Om du vill avmarkera alla tilldelade värden klickar du på **[!UICONTROL Deselect All]**.

1. Klicka på **[!UICONTROL Unassign Selected]**.

## (Äldre användargränssnitt) Ta bort etikettklassificeringsvärden från kontokomponenter

1. Välj entitetsvyn i **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**.

1. Gör något av följande:

   * (Om du vill ta bort värden från en enskild enhet) Håll markören över enhetsnamnet, klicka på ![Menyknappen](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyknapp") och välj sedan **[!UICONTROL Classification]**.

   * (Så här tar du bort värden från en eller flera enheter:)

      * Markera kryssrutan bredvid varje rad.

        Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * Klicka på ![Mer](/help/search-social-commerce/assets/more.png "Mer") i verktygsfältet ovanför datatabellen och klicka sedan på **[!UICONTROL Classification]**.

1. I [!UICONTROL Assignment Details] väljer du **[!UICONTROL Remove]**.

1. Gör följande för varje klassificeringsvärde som ska tas bort:

   * Klicka på klassificeringsnamnet i kolumnen **[!UICONTROL Classification]** för att expandera det.

   * Klicka på namnet på värdet i kolumnen **[!UICONTROL Value Name]** för att markera det.

1. (Valfritt) Ange ytterligare information:

   * Klicka på **[!UICONTROL Additional Details]**&#x200B;Öppna![Öppna](/help/search-social-commerce/assets/chevron-up.png " bredvid ") för att utöka informationen.

   * Ange ett valfritt **[!UICONTROL Project Name]** och/eller valfritt **[!UICONTROL Description]**.

   * Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Om etikettklassificeringar](classification-about.md)
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer](classification-values-assign-campaign-management.md)
>* [Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad](classification-values-assign-bulksheets.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)
