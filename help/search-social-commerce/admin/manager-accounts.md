---
title: Hantera autentiseringsuppgifter för annonsnätverkshanterarkonton
description: Lär dig hur du anger autentiseringsuppgifter för dina  [!DNL Google Ads] hanterarkonton.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Hantera autentiseringsuppgifter för annonsnätverkshanterarkonton

Endast *[!DNL Google Ads]konton*

Ange autentiseringsuppgifterna för dina [!DNL Google Ads]-hanterarkonton som du vill att konversationer ska överföras till via Search, Social och Commerce. Använd den här funktionen om du vill a) överföra [!DNL Adobe]-spårade konverteringsvärden mellan konton till ett [!DNL Google Ads]-hanterarkonto eller b) överföra portföljmål som inkluderar kontokonverteringar till [!DNL Google Ads] för hybridoptimering.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Du kan lägga till autentiseringsuppgifter för nya poster för chefskonton eller autentisera om ett befintligt hanterarkonto.

När du lägger till autentiseringsuppgifter för ett hanterarkonto visas det associerade hanterarkontots ID som skrivskyddat i kontoinställningarna. Dessutom visar den valfria kolumnen [!UICONTROL Manager Account for Cross-Account Conversions] i vyn [!UICONTROL Campaigns] > [!UICONTROL Accounts] hanterarkonto-ID:t för varje underordnat konto och anger ett fel när hanterarkontot inte är autentiserat. [!UICONTROL Notification Center] innehåller meddelanden om när autentiseringsuppgifter för ett hanterarkonto saknas ([the [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) eller när en autentiseringstoken för ett hanterarkonto upphör ([the [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Så här lägger du till autentiseringsuppgifter för ett nytt chefskonto

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** på huvudmenyn.

1. Välj **[!UICONTROL Create new manager account]**.

1. Ange inloggningsuppgifter för hanterarkontot.

   **[!UICONTROL Manager Account ID]** och **[!UICONTROL Login Email]** krävs. Search, Social och Commerce hämtar och lagrar automatiskt den kontotoken som ska användas för autentisering.

   Du kan även inkludera en **[!UICONTROL MCC Account Name]** för identifiering i Search, Social och Commerce samt kontot **[!UICONTROL Password]**. Ange lösenordet när du vill kryptera och spara det så att kontohanteraren kan uppdatera tokens efter behov.

1. Klicka på **[!UICONTROL Authenticate]**.

1. Klicka på **[!UICONTROL Save]**.

## Återautentisera ett befintligt chefskonto

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** på huvudmenyn.

1. Välj **[!UICONTROL Reauthenticate existing manager account]**.

1. Välj chefskontot.

1. Ange inloggningsuppgifter för hanterarkontot.

   E-postadressen **[!UICONTROL Manager Account ID]** och **inloggningen** krävs. Search, Social och Commerce hämtar och lagrar automatiskt den kontotoken som ska användas för autentisering.

   Du kan även inkludera en **[!UICONTROL MCC Account Name]** för identifiering i Search, Social och Commerce samt kontot **[!UICONTROL Password]**. Ange lösenordet när du vill kryptera och spara det så att kontohanteraren kan uppdatera tokens efter behov.

1. Klicka på **[!UICONTROL Authenticate]**.

1. Klicka på **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Aktivera överföring av mål till annonsnätverk](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Överför konverteringsstatistik för sökning, sociala medier och Commerce till  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Redigera aviseringsinställningarna](/help/search-social-commerce/notifications/notification-edit.md)
