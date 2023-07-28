---
title: Hantera [!DNL Microsoft Advertising] dynamisk återmarknadsföring
description: Lär dig hur du skapar och hanterar [!DNL Microsoft Advertising] dynamisk återmarknadsföring.
exl-id: 6f0cb6a0-36cc-4a07-82a8-247191b6c4f5
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Hantera [!DNL Microsoft Advertising] dynamisk återmarknadsföring

*[!DNL Microsoft Advertising]endast konton*

Du kan skapa [!DNL Microsoft Advertising] dynamisk återmarknadsföring av publiken när du använder sökmotorns JavaScript-konvertering och målgruppsspårningstagg på dina webbsidor. Varje publik skapas med en angiven tagg som finns med på de webbsidor vars användare ska utgöra målgruppen. Du kan skapa flera målgrupper med samma spårningstagg. Du kan också ändra namn och datakälla för befintliga målgrupper eller ta bort befintliga målgrupper.

Målgrupper för dynamisk återmarknadsföring har typen Målgrupp[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; (t.ex.&quot;Dynamic Remarketing Past Buyers&quot;).

Mer information om dynamisk återmarknadsföring och hur du implementerar den JavaScript-tagg som krävs finns i [[!DNL Microsoft Advertising] dokumentation om dynamisk återmarknadsföring](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Skapa en dynamisk publik för återmarknadsföring

>[!NOTE]
>
>För [!DNL Microsoft Advertising] -konton måste JavaScript-taggen innehålla [produkt-ID och sidtypsparametrar](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifiera namnet på [!DNL Microsoft Advertising] UET-tagg (Universal Event tracking) som ingår i de webbsidor som målgruppen ska skapas från.

   Du behöver taggens namn i ett senare steg.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. I **[!UICONTROL Data Source]** meny, välja **[!UICONTROL Dynamic Remarketing List]**.

   1. Ange **[!UICONTROL Audience Name]**.

   1. Välj namnet på sökmotorkontot i en lista över alla tillgängliga taggar för sökmotorkontot [!DNL Microsoft Advertising] UET-tagg som ingår i de webbsidor vars användare ska omfatta publiken.

   1. Välj besökartyp för målgruppen, som baseras på besökaråtgärder på relevanta webbsidor: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, eller *[!UICONTROL Shopping Cart Abandoners]*.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar kvar hos publiken. Värdena kan ligga mellan ett (1) och 180.

      Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>Dina [!DNL Microsoft Advertising] dynamiska listor för återmarknadsföring är berättigade till stöd när de innehåller minst 300 användare.

## Redigera en dynamisk publik för återmarknadsföring

Du kan ändra namn och datakälla för en [!DNL Microsoft Advertising] dynamisk publik för återmarknadsföring. Du kan inte redigera värdet för [!UICONTROL Membership Days] inställning.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Markera kryssrutan bredvid målgruppen som ska redigeras.

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera målgruppsinformationen:

   1. I **[!UICONTROL Data Source]** avsnitt, klicka ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

   1. (Valfritt) Ändra **[!UICONTROL Audience Name]**.

   1. (Valfritt) Ändra namnet på annonsnätverkskontot i en lista över alla tillgängliga taggar för annonsnätverkskontot [!DNL Microsoft Advertising] UET-tagg som ingår i de webbsidor vars användare ska omfatta publiken.

   1. (Valfritt) Ändra besökartypen för målgruppen, som baseras på besökaråtgärder på relevanta webbsidor: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, eller *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klicka på **[!UICONTROL Post]**.

## Ta bort en dynamisk publik för återmarknadsföring

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika målgrupper.

1. Markera kryssrutan bredvid varje målgrupp som ska tas bort.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera kundmatchande målgrupper med hjälp av kunddatalistor](audience-from-customer-data-list.md)
