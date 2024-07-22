---
title: Hantera [!DNL Microsoft Advertising] dynamiska ommarknadsföringsmålgrupper
description: Lär dig hur du skapar och hanterar  [!DNL Microsoft Advertising] dynamiska marknadsföringsmålgrupper.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Hantera [!DNL Microsoft Advertising] dynamiska ommarknadsföringsmålgrupper

Endast *[!DNL Microsoft Advertising]konton*

Du kan skapa en [!DNL Microsoft Advertising] dynamisk publik för återmarknadsföring när du använder sökmotorns tagg för JavaScript-konvertering och målgruppsspårning på dina webbsidor. Varje publik skapas med en angiven tagg som finns på de webbsidor vars användare omfattar publiken. Du kan skapa flera målgrupper med samma spårningstagg. Du kan också ändra namn och datakälla för befintliga målgrupper eller ta bort befintliga målgrupper.

Målgrupper för dynamisk återmarknadsföring har målgruppstypen [!UICONTROL Dynamic Remarketing] \&lt;besökartyp\> (t.ex. &quot;Dynamic Remarketing Past Buyers&quot;).

Mer information om dynamisk återmarknadsföring och hur du implementerar den nödvändiga JavaScript-taggen finns i [[!DNL Microsoft Advertising] dokumentationen om dynamisk återmarknadsföring](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Skapa en dynamisk publik för återmarknadsföring

>[!NOTE]
>
>För [!DNL Microsoft Advertising]-konton måste JavaScript-taggen innehålla parametrarna [product ID och page type](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifiera namnet på UET-taggen (Universal Event tracking) [!DNL Microsoft Advertising] som finns på de webbsidor som målgruppen ska skapas från.

   Du behöver taggens namn i ett senare steg.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Markera annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. Välj **[!UICONTROL Dynamic Remarketing List]** på menyn **[!UICONTROL Data Source]**.

   1. Ange **[!UICONTROL Audience Name]**.

   1. I en lista över alla tillgängliga taggar för sökmotorkontot markerar du namnet på UET-taggen [!DNL Microsoft Advertising] som finns på de webbsidor vars användare omfattar målgruppen.

   1. Välj besökartyp för målgruppen, som baseras på besökaråtgärder på de relevanta webbsidorna: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* eller *[!UICONTROL Shopping Cart Abandoners]*.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar i målgruppen. Värdena kan ligga mellan ett (1) och 180.

      Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>Dina [!DNL Microsoft Advertising] dynamiska ommarknadsföringslistor är berättigade till mål när de innehåller minst 300 användare.

## Redigera en dynamisk publik för återmarknadsföring

Du kan ändra namnet och datakällan för en [!DNL Microsoft Advertising] dynamisk publik för återmarknadsföring. Du kan inte redigera värdet för inställningen [!UICONTROL Membership Days].

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. Markera kryssrutan bredvid målgruppen som ska redigeras.

1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet ovanför datatabellen.

1. Redigera målgruppsinformationen:

   1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i avsnittet **[!UICONTROL Data Source]**.

   1. (Valfritt) Ändra **[!UICONTROL Audience Name]**.

   1. (Valfritt) I en lista över alla tillgängliga taggar för annonsnätverkskontot ändrar du namnet på UET-taggen [!DNL Microsoft Advertising] som finns på de webbsidor vars användare omfattar målgruppen.

   1. (Valfritt) Ändra besökartypen för målgruppen, som baseras på besökaråtgärder på de relevanta webbsidorna: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* eller *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klicka på **[!UICONTROL Post]**.

## Ta bort en dynamisk publik för återmarknadsföring

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. (Valfritt) Filtrera listan så att den innehåller specifika målgrupper.

1. Markera kryssrutan bredvid varje målgrupp som ska tas bort.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera kundmatchande målgrupper med kunddatalistor](audience-from-customer-data-list.md)
