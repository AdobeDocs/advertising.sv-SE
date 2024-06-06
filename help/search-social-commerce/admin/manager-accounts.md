---
title: Hantera autentiseringsuppgifter för annonsnätverkshanterarkonton
description: Lär dig hur du anger autentiseringsuppgifter för [!DNL Google Ads] chefskonton.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---

# Hantera autentiseringsuppgifter för annonsnätverkshanterarkonton

*[!DNL Google Ads]endast konton*

Ange autentiseringsuppgifter för [!DNL Google Ads] hanterarkonton som du vill att Search, Social och Commerce ska överföra kontonakonverteringar till. Använd den här funktionen om du vill a) överföra [!DNL Adobe]-spårade, kontoövergripande konverteringsvärden till en [!DNL Google Ads] chefskonto eller b) överföra portföljmål som omfattar kontoövergripande konverteringar till [!DNL Google Ads] för hybridoptimering.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Du kan lägga till autentiseringsuppgifter för nya poster för chefskonton eller autentisera om ett befintligt hanterarkonto.

När du lägger till autentiseringsuppgifter för ett hanterarkonto visas det associerade hanterarkontots ID som skrivskyddat i kontoinställningarna. Dessutom kan du välja &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; i [!UICONTROL Campaigns] > [!UICONTROL Accounts] visar hanterarkonto-ID för varje underordnat konto och visar ett fel när hanterarkontot inte är autentiserat. [!UICONTROL Notification Center] innehåller meddelanden om när autentiseringsuppgifter för ett hanterarkonto saknas ([den [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) eller när en token för autentisering av ett hanterarkonto upphör ([den [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Så här lägger du till autentiseringsuppgifter för ett nytt chefskonto

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Välj **[!UICONTROL Create new manager account]**.

1. Ange inloggningsuppgifter för hanterarkontot.

   The **[!UICONTROL Manager Account ID]** och **[!UICONTROL Login Email]** krävs. Search, Social och Commerce hämtar och lagrar automatiskt den kontotoken som ska användas för autentisering.

   Du kan även inkludera en **[!UICONTROL MCC Account Name]** för identifiering i Search, Social och Commerce samt kontot **[!UICONTROL Password]**. Ange lösenordet när du vill kryptera och spara det så att kontohanteraren kan uppdatera tokens efter behov.

1. Klicka på **[!UICONTROL Authenticate]**.

1. Klicka på **[!UICONTROL Save]**.

## Återautentisera ett befintligt chefskonto

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Välj **[!UICONTROL Reauthenticate existing manager account]**.

1. Välj chefskontot.

1. Ange inloggningsuppgifter för hanterarkontot.

   The **[!UICONTROL Manager Account ID]** och **E-postadress för inloggning** krävs. Search, Social och Commerce hämtar och lagrar automatiskt den kontotoken som ska användas för autentisering.

   Du kan även inkludera en **[!UICONTROL MCC Account Name]** för identifiering i Search, Social och Commerce samt kontot **[!UICONTROL Password]**. Ange lösenordet när du vill kryptera och spara det så att kontohanteraren kan uppdatera tokens efter behov.

1. Klicka på **[!UICONTROL Authenticate]**.

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Aktivera överföring av mål till annonsnätverk](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Överför konverteringsmått till [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Redigera meddelandeinställningarna](/help/search-social-commerce/notifications/notification-edit.md)
