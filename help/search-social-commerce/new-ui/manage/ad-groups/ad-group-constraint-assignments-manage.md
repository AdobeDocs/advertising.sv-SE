---
title: Hantera begränsningstilldelningar för annonsgrupper
description: Lär dig hur du tilldelar begränsningar till annonsgrupper.
feature: Search Optimization, Search Campaign Management
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# (Nytt användargränssnitt) Hantera villkorstilldelningar för annonsgrupper

*Beta-funktion*

Du kan tilldela och ta bort anbudsbegränsningar för följande sökentiteter: kampanj, annonsgrupp, nyckelord, placering, produktgrupp på enhetsnivå och dynamiskt sökmål. Varje entitet kan bara ha en begränsning.

Begränsningar ärvs av underordnade entiteter, så du behöver inte tilldela begränsningar för underordnade entiteter om du inte vill åsidosätta de ärvda värdena.

När du frigör en begränsning tas kopplingen till kontokomponenterna och alla deras underordnade komponenter bort, och rapportdata för begränsningen är inte längre tillgängliga för dessa komponenter. När du frigör en begränsning tas varken begränsningen eller själva kontokomponenterna bort.

## Tilldela en begränsning till valda annonsgrupper från den nya vyn [!UICONTROL Ad Groups]

1. Klicka på **[!UICONTROL Manage]>[!UICONTROL Ad Groups]** på huvudmenyn.

1. Markera kryssrutan bredvid varje annonsgrupp som du ska tilldela en enskild begränsning till.

1. Klicka på ![Fler åtgärder](/help/search-social-commerce/assets/more-actions.png "Fler åtgärder") **[!UICONTROL More Actions]** > ![Tilldela](/help/search-social-commerce/assets/assign.png "Tilldela") **[!UICONTROL Assign]** > **[!UICONTROL Constraint]** i verktygsfältet.

1. Markera begränsningen.

1. Klicka på **[!UICONTROL Assign Now]**.

## Tilldela en begränsning till valda sökbudsenheter från de äldre [!UICONTROL Campaigns] vyerna

1. I **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** markerar du kontokomponentvyn.

1. Markera kryssrutan bredvid varje relevant rad.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på **[!UICONTROL More]** i verktygsfältet ovanför datatabellen och klicka sedan på **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Välj önskad begränsning.

1. (Valfritt) Ange ytterligare information:

   1. Klicka på [!UICONTROL Additional Details] bredvid **[!UICONTROL Open]** för att expandera informationen.

   1. Ange ett valfritt **[!UICONTROL Project Name]** och/eller valfritt **[!UICONTROL Description]**.

1. Klicka på **[!UICONTROL Save]**.

## Ta bort tilldelning från markerade annonsgrupper från den nya vyn [!UICONTROL Ad Groups]

1. Klicka på **[!UICONTROL Manage]>[!UICONTROL Ad Groups]** på huvudmenyn.

1. Markera kryssrutan bredvid varje annonsgrupp som du vill ta bort begränsningar från.

1. Klicka på ![Fler åtgärder](/help/search-social-commerce/assets/more-actions.png "Fler åtgärder") **[!UICONTROL More Actions]** > ![Tilldela](/help/search-social-commerce/assets/unassign.png "Ta bort tilldelning") **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]** i verktygsfältet.

1. Klicka på **[!UICONTROL Confirm]**.

## Ta bort begränsningar från sökbudsenheter från de gamla [!UICONTROL Campaigns] vyerna

>[!NOTE]
>
>Om du vill ta bort en begränsning och göra den otillgänglig för framtida bruk kan du läsa Ta bort begränsningar för sökbudsenheter i kapitlet i optimeringsguiden om &quot;Bid Constraints&quot;, som är tillgängligt i Search, Social och Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. I **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** markerar du kontokomponentvyn.

1. Markera kryssrutan bredvid varje komponent som du vill ta bort begränsningen från.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på **[!UICONTROL More]** i verktygsfältet ovanför datatabellen och klicka sedan på **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Välj **[!UICONTROL Yes, Unassign]** i bekräftelsedialogrutan.

>[!MORELIKETHIS]
>
>* [Hantera begränsningstilldelningar för kampanjer](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
