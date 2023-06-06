---
title: Hantera produktgrupper för butik
description: Lär dig hur du skapar och hanterar kundproduktgrupper i shoppingkampanjer.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Hantera produktgrupper för butik

*[!DNL Google Ads]och [!DNL Microsoft Advertising] endast köpkampanjer*

Du kan skapa och redigera produktgrupper och ta bort produktgrupper och deras underordnade produktgrupper i [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] vy.

## Skapa en[!UICONTROL All Products]&quot; produktgrupp

Innan du kan skapa produktgrupper med specifika attribut måste du först skapa en produktgrupp som innehåller alla funktioner och som heter[!UICONTROL All Products].&quot; Varje annonsgrupp kan bara ha en[!UICONTROL All Products]&quot; grupp.

>[!TIP]
>
>Om du vill skapa flera kontokomponenter samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket, kontot, kampanjen och annonsgruppen och klicka sedan på **[!UICONTROL Continue]**.

1. Ange [[!DNL Google Ads] produktgruppsinställningar](product-group-settings-google.md) eller [[!DNL Microsoft Advertising] produktgruppsinställningar](product-group-settings-microsoft.md).

1. Klicka på **[!UICONTROL Post]**.

## Skapa en underordnad produktgruppnod i en befintlig produktgrupp

När du har skapat minst en fullständig[!UICONTROL All Products]&quot; grupp för en annonsgrupp, kan du skapa underordnade produktgruppnoder för delmängder av produkter som ska inkluderas i eller exkluderas från bud, där en eller flera produktgrupper har samma attribut på varje nivå (till exempel [!UICONTROL Brand]=Köp för en produktgrupp och [!UICONTROL Brand]=AcmePlus för en annan på samma nivå. Du kan skapa upp till sju nivåer med underordnade produktgruppnoder, förutom &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Du kan inte skapa en underordnad produktgrupp för en[!UICONTROL Everything Else]&quot; produktgrupp.

>[!TIP]
>
>Om du vill skapa flera kontokomponenter samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Valfritt) Om du vill visa en produktgrupp och dess underordnade produktgruppnoder i trädvyn håller du markören över produktgruppens namn och klickar på ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL Tree View]**.

1. Håll markören över produktgruppens namn och klicka ![Listruta med pilar](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Listruta med pilar")och sedan markera **[!UICONTROL + Add Node]**.

1. Ange [[!DNL Google Ads] produktgruppsinställningar](product-group-settings-google.md) eller [[!DNL Microsoft Advertising] produktgruppsinställningar](product-group-settings-microsoft.md), inklusive produktdimension och attribut.

1. Klicka på **[!UICONTROL Post]**.

## Redigera inställningar för produktgruppnod

Du kan redigera köp- och spårningsmallen för enhetsproduktgruppsnoder (produktgrupper utan underordnade produktgruppnoder) som ingår för en annonsgrupp. Du kan inte redigera någon information för uteslutna enhetsproduktgrupper eller för inkluderade eller exkluderade delavdelningsnoder, som är produktgrupper med underordnade produktgruppnoder.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Valfritt) Om du vill visa en produktgrupp och dess underordnade produktgruppnoder i trädvyn håller du markören över produktgruppens namn och klickar på ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL Tree View]**.

1. Gör något av följande:

   1. (Om du vill redigera inställningar för en enskild produktgruppsnod håller du pekaren över produktgruppsnamnet genom att klicka på ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL + Edit Node]**.

   1. (Så här redigerar du inställningar för en eller flera annonsgrupper):

      1. Markera kryssrutan bredvid varje nod.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [[!DNL Google Ads] produktgruppsinställningar](product-group-settings-google.md) eller [[!DNL Microsoft Advertising] produktgruppsinställningar](product-group-settings-microsoft.md).

   För flera noder tillämpas ändringarna på alla markerade noder. För [!UICONTROL Bid] har du möjlighet att ändra befintliga värden till ett angivet värde eller att antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns. För [!UICONTROL Tracking Template] kan du ändra befintliga värden till ett angivet värde, ersätta en befintlig sträng med en angiven sträng, lägga till ett angivet prefix i början av varje värde eller lägga till ett suffix i slutet av varje värde.

1. (Valfritt) Klicka på **[!UICONTROL Additional Details]** och kan även ange ett projektnamn och en beskrivning.

1. Klicka på **[!UICONTROL Post]**.

## Ta bort produktgruppsnoder

Du kan ta bort vilken produktgrupp som helst, förutom en&quot;Allt annat&quot;-grupp när det finns andra produktgrupper på samma nivå, som används för att avgöra vilka produkter i ert handlarcenterkonto som ingår i annonsgruppens shoppingannonser. Om du tar bort en produktgrupp tas alla underordnade produktgrupper bort.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika produktgrupper.

1. Gör något av följande:

   * Om du vill ta bort en produktgrupp klickar du på **[!UICONTROL Status]** kolumn och markera **[!UICONTROL Delete]**.

   * Så här tar du bort en eller flera produktgrupper:

      1. Markera kryssrutan bredvid varje produktgrupp som du vill ta bort.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ![Mer](/help/search-social-commerce/assets/more.png "Mer") och markera **[!UICONTROL Delete]**.

      1. Klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Om att handla produktgrupper](product-group-about.md)
>* [[!DNL Google Ads] produktgruppsinställningar](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] produktgruppsinställningar](product-group-settings-microsoft.md)

