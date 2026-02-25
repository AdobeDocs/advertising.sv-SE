---
title: Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer
description: Lär dig hur du tilldelar klassificeringsvärden till kontokomponenter.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer

Du kan tilldela och ta bort klassificeringsvärden för följande sökentiteter från kampanjhanteringsvyerna: kampanj, annonsgrupp, nyckelord, annons, placering, produktgrupp på enhetsnivå och dynamiskt sökmål. Om det behövs kan du skapa klassificeringar och klassificeringsvärden under tilldelningsprocessen. Varje etikettklassificering kan ha upp till 2 000 värden.

Varje entitet kan ha ett etikettvärde per klassificering. Exempel: Shoes_Campaign kan ha färgvärdet &quot;red&quot; och det geografiska värdet &quot;Los Angeles&quot;, men det kan inte ha flera värden för Color eller Geo.

Etikettvärden ärvs av underordnade entiteter, så ange inte värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena.

>[!NOTE]
>
>Dina nyckelord och din annonskopia för vissa annonsnätverk och kampanjtyper är [inte ändringsbara](/help/search-social-commerce/campaign-management/faqs-campaigns.md), vilket innebär att om du redigerar dem tas den befintliga entiteten bort och en ny skapas. När en befintlig enhet tas bort på det här sättet tilldelas inte etikettklassificeringen till den nya enheten.

## (Nytt användargränssnitt) Tilldela klassificeringsvärden till kontokomponenter

Du kan tilldela klassificeringsvärden till alla tillämpliga kontokomponenter som är tillgängliga i det nya användargränssnittet.

1. Öppna entitetsvyn från menyn **[!UICONTROL Manage]** eller **[!UICONTROL Target]**.

1. Markera kryssrutan bredvid varje relevant rad.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]** i verktygsfältet för gruppåtgärder.

1. Gör följande för varje tillämpligt klassificeringsvärde:

   1. Ange klassificeringen i kolumnen **[!UICONTROL Classifications]**:

      * Om du vill använda en befintlig klassificering klickar du på klassificeringsnamnet för att expandera den.

      * Om du vill skapa en klassificering klickar du på [!UICONTROL +] i kolumnrubriken. Ange klassificeringsnamnet i indatafältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/save-checkmark.png "Spara") för att spara klassificeringen omedelbart. Om du vill använda den nya klassificeringen klickar du på klassificeringsnamnet för att expandera den.

        Namnet måste bestå av [ASCII-tecken 32-126](https://www.asciitable.com/) och får innehålla högst 27 enkelbyte-tecken.

   1. I kolumnen **[!UICONTROL Value Name]** anger du värdet för den valda klassificeringen:

      * Om du vill använda ett befintligt värde markerar du värdet.

      * Om du vill skapa ett värde klickar du på [!UICONTROL +] i kolumnrubriken. Ange värdet i inmatningsfältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/save-checkmark.png "Spara") för att spara värdet omedelbart och markera det som standard.

        Maxlängden är 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

1. Klicka på **+[!UICONTROL Assign Now]**.

## (Äldre användargränssnitt) Tilldela klassificeringsvärden till kontokomponenter

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** och välj sedan kontokomponentvyn.

1. Gör något av följande:

   * (Om du vill tilldela värden till en enskild enhet) Håll markören över enhetsnamnet, klicka på ![Menyknappen](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyknapp") och välj sedan **[!UICONTROL Classification]**.

   * (Så här tilldelar du värden till en eller flera enheter):

      * Markera kryssrutan bredvid varje relevant rad.

        Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * Klicka på ![Mer](/help/search-social-commerce/assets/more.png "Mer") i verktygsfältet ovanför datatabellen och klicka sedan på **[!UICONTROL Classification]**.

1. Gör något av följande i [!UICONTROL Assignment Details]:

   * Om du vill ändra befintliga klassificeringsvärden till nya värden väljer du **[!UICONTROL Set To]**.

     Värdet får innehålla högst 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

   * Om du vill tilldela angivna klassificeringsvärden utan att ta bort befintliga värden väljer du **[!UICONTROL Assign]**.

   * Om du vill ta bort specifika, för närvarande tilldelade klassificeringsvärden väljer du **[!UICONTROL Remove]**.

     När du tar bort ett klassificeringsvärde är rapportdata för värdet inte längre tillgängliga för de angivna kontokomponenterna.

   * Om du vill ta bort angivna klassificeringsvärden väljer du **[!UICONTROL Delete]**.

     Om du tar bort ett klassificeringsvärde blir det inte tillgängligt för framtida bruk och rapportdata är inte längre tillgängliga för värdet. Alla tilldelningar mellan värden och specifika kontokomponenter tas bort, men kontokomponenterna tas inte bort.

1. Gör följande för varje tillämpligt klassificeringsvärde:

   1. I kolumnen **[!UICONTROL Classification]** anger du klassificeringsnamnet:

      * Om du vill använda en befintlig klassificering klickar du på klassificeringsnamnet för att expandera den.

      * Om du vill skapa en klassificering klickar du på [!UICONTROL +]. Ange klassificeringsnamnet i indatafältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/select.png "Spara") för att spara klassificeringen omedelbart.

        Namnet måste bestå av [ASCII-tecken 32-126](https://www.asciitable.com/) och får innehålla högst 27 enkelbyte-tecken.

   1. Ange värdets namn i kolumnen **[!UICONTROL Value Name]**:

      * Om du vill använda ett befintligt värde klickar du på värdenamnet för att markera det.

      * Klicka på [!UICONTROL +] om du vill skapa ett värde. Ange värdet i indatafältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/select.png "Spara") för att spara värdet direkt.

        Maxlängden är 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

1. (Valfritt) Ange ytterligare information:

   1. Klicka på **[!UICONTROL Additional Details]**&#x200B;Öppna![Öppna](/help/search-social-commerce/assets/chevron-up.png " bredvid ") för att utöka informationen.

   1. Ange ett valfritt **[!UICONTROL Project Name]** och/eller valfritt **[!UICONTROL Description]**.

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Om etikettklassificeringar](classification-about.md)
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad](classification-values-assign-bulksheets.md)
>* [Ta bort etikettklassificeringsvärden från kontokomponenter](classification-values-remove.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)
