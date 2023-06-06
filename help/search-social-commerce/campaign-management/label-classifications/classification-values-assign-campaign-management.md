---
title: Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer
description: Lär dig hur du tilldelar klassificeringsvärden till kontokomponenter.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Tilldela klassificeringsvärden till kontokomponenter från kampanjhanteringsvyer

Du kan tilldela och ta bort klassificeringsvärden för följande sökentiteter från kampanjhanteringsvyerna: kampanj, annonsgrupp, nyckelord, annons, placering, produktgrupp på enhetsnivå och dynamiskt sökmål. Om det behövs kan du skapa klassificeringar och klassificeringsvärden under tilldelningsprocessen. Varje etikettklassificering kan ha upp till 2 000 värden.

Varje entitet kan ha ett etikettvärde per klassificering. Exempel: Shoes_Campaign kan ha färgvärdet &quot;red&quot; och det geografiska värdet &quot;Los Angeles&quot;, men det kan inte ha flera värden för Color eller Geo.

Etikettvärden ärvs av underordnade entiteter, så ange inte värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena.

>[!NOTE]
>
>Dina nyckelord och din annonskopia för vissa annonsnätverk och kampanjtyper är [ej ändringsbar](/help/search-social-commerce/campaign-management/faqs-campaigns.md), vilket innebär att om du redigerar dem tas den befintliga enheten bort och en ny skapas. När en befintlig entitet tas bort på det här sättet tilldelas inte etikettklassificeringen till den nya entiteten.

1. Klicka **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** och välj sedan kontokomponentvyn.

1. Gör något av följande:

   * (Om du vill tilldela värden till en enskild enhet) Håll markören över enhetsnamnet klickar du på ![Menyknapp](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyknapp")och sedan markera **[!UICONTROL Classification]**.

   * (Så här tilldelar du värden till en eller flera enheter):

      * Markera kryssrutan bredvid varje relevant rad.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Klicka på i verktygsfältet ovanför datatabellen ![Mer](/help/search-social-commerce/assets/more.png "Mer")och klicka sedan på **[!UICONTROL Classification]**.

1. I [!UICONTROL Assignment Details]gör du något av följande:

   * Om du vill ändra befintliga klassificeringsvärden till nya värden väljer du **[!UICONTROL Set To]**.

      Värdet får innehålla högst 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

   * Om du vill tilldela angivna klassificeringsvärden utan att ta bort befintliga värden väljer du **[!UICONTROL Assign]**.

   * Om du vill ta bort specifika, för närvarande tilldelade klassificeringsvärden väljer du **[!UICONTROL Remove]**.

      När du tar bort ett klassificeringsvärde är rapportdata för värdet inte längre tillgängliga för de angivna kontokomponenterna.

   * Om du vill ta bort angivna klassificeringsvärden väljer du **[!UICONTROL Delete]**.

      Om du tar bort ett klassificeringsvärde blir det inte tillgängligt för framtida bruk och rapportdata är inte längre tillgängliga för värdet. Alla tilldelningar mellan värden och specifika kontokomponenter tas bort, men kontokomponenterna tas inte bort.

1. Gör följande för varje tillämpligt klassificeringsvärde:

   1. I **[!UICONTROL Classification]** kolumn, ange klassificeringsnamnet:

      * Om du vill använda en befintlig klassificering klickar du på klassificeringsnamnet för att expandera den.

      * Om du vill skapa en klassificering klickar du på [!UICONTROL +]. Ange klassificeringsnamnet i indatafältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/select.png "Spara") för att omedelbart spara klassificeringen.

         Namnet måste bestå av [ASCII-tecken 32-126](https://www.asciitable.com/)och den maximala längden är 27 enkelbyte-tecken.
   1. I **[!UICONTROL Value Name]** -kolumn anger du namnet på värdet:

      * Om du vill använda ett befintligt värde klickar du på värdenamnet för att markera det.

      * Om du vill skapa ett värde klickar du på [!UICONTROL +]. Ange värdet i inmatningsfältet och klicka sedan på ![Spara](/help/search-social-commerce/assets/select.png "Spara") för att omedelbart spara värdet.

         Maxlängden är 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.


1. (Valfritt) Ange ytterligare information:

   1. Nästa till **[!UICONTROL Additional Details]**, klicka ![Öppna](/help/search-social-commerce/assets/chevron-up.png "Öppna") för att utöka detaljerna.

   1. Ange ett valfritt **[!UICONTROL Project Name]** och/eller valfritt **[!UICONTROL Description]**.

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Etikettklassificeringar](classification-about.md)
>* [Skapa en etikettklassificering](classification-create.md)
>* [Tilldela klassificeringsvärden till kontokomponenter med hjälp av kalkylblad](classification-values-assign-bulksheets.md)
>* [Ta bort etikettklassificeringsvärden från kontokomponenter](classification-values-remove.md)
>* [Ta bort etikettklassificeringsvärden](classification-values-delete.md)
>* [Ta bort etikettklassificeringar](classification-delete.md)

