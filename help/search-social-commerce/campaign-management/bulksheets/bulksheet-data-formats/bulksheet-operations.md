---
title: Åtgärder som du kan utföra i kalkylblad
description: Referera till allmän information om hur du lägger till, redigerar och tar bort kampanjdata med hjälp av kalkylblad.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Åtgärder som du kan utföra i kalkylblad

Du kan lägga till, redigera och ta bort kampanjdata via kalkylblad för [annonsnätverk som stöds](../bulksheet-about.md#bulksheet-functionality-by-network).

Inkludera en separat datarad för varje kampanjkomponent (kampanj, annonsgrupp, nyckelord eller textannons) som du vill lägga till, redigera eller ta bort, eller vars egenskaper du vill lägga till, redigera eller ta bort. Om du till exempel vill skapa en kampanj med en annonsgrupp, ett nyckelord och en annons - totalt fyra komponenter - behöver du fyra separata datarader. Om du vill redigera [!UICONTROL Ad Group Name] för en annonsgrupp (en komponent) behöver du bara en rad. Om du vill redigera fyra olika egenskaper för en annonsgrupp (en komponent) behöver du bara en rad.

Följande regler gäller för arbete med kampanjkomponenter och deras egenskaper.

* Lägger till:

   * Om du vill lägga till en komponent inkluderar du alla fält som krävs för att lägga till komponenten, plus eventuellt fält för någon av komponentens egenskaper.

   * Om du vill lägga till en egenskap för en befintlig komponent, till exempel [!UICONTROL Ad Group End Date] för en annonsgrupp, inkluderar du alla fält som krävs för att redigera den komponenten (annonsgruppen) plus fältet för egenskapen ([!UICONTROL Ad Group End Date]).

* Om du vill redigera en egenskap för en befintlig komponent inkluderar du alla fält som behövs för att redigera den komponenten plus fältet för egenskapen.

  Om du lämnar egenskapsfältet tomt behålls det befintliga värdet.

* Tar bort:

   * Om du vill ta bort en befintlig komponent inkluderar du alla fält som krävs för att redigera den komponenten och ändra dess status till [!UICONTROL Deleted]. Om du till exempel vill ta bort en [!DNL Google Ads]-annonsgrupp måste du inkludera [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] med värdet <i>[!UICONTROL Deleted]</i> och [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2] och [!UICONTROL Param3] värden) Om du vill ta bort ett befintligt [!DNL paramN]-värde för ett nyckelord tar du med alla fält som krävs för att redigera nyckelordet och tar även bort det befintliga [!DNL paramN]-värdet genom att ange värdet `[delete]` (inklusive parenteserna) i motsvarande fält.

   * (Tillåtna egenskapsfält) Om du vill ta bort ett befintligt egenskapsvärde för en komponent tar du med alla fält som krävs för att redigera den komponenten och även ta bort egenskapsvärdet genom att ange värdet `[delete]` (inklusive hakparenteserna). Tillåtna fält är:

      * ([!UICONTROL Google Ads] endast) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] och endast [!DNL Microsoft Advertising]) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>När du inkluderar ett värde i ett fält som inte är tillämpligt på åtgärden, ignoreras alla värden som anges i fältet.

>[!MORELIKETHIS]
>
>* [Om att hantera kampanjdata med hjälp av kalkylblad](../bulksheet-about.md)
>* [Mallfilformat som stöds](bulksheet-file-formats.md)
>* [Bilaga - fel i bulkark](../bulksheet-errors.md)
>* [Hämta/skapa en kalkylbladsfil](../bulksheet-download.md)
