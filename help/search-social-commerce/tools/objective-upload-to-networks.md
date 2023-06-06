---
title: Aktivera överföring av mål till annonsnätverk
description: Lär dig hur du överför mål för dina hybridportfolior till [!DNL Google Ads] och [!DNL Microsoft® Advertising].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Aktivera överföring av mål till annonsnätverk

*Annonsörer med [!DNL Google Ads] och [!DNL Microsoft® Advertising] endast konton*

*Annonsörer endast aktiverade för hybridoptimering*

Om annonserarkontot är konfigurerat att använda hybridoptimering kan Adobe Advertising överföra målen för kontots portföljer till [!DNL Google Ads] och [!DNL Microsoft® Advertising] som konverteringar så att du kan använda dem för hybridoptimering.

Om du aktiverar det här alternativet aktiveras automatiskt en överföring för portföljer som innehåller kampanjer med smarta anbudsstrategier. Search, Social, &amp; Commerce skapar en konvertering i annonsnätverket för varje tillämplig kombination av portfölj och mål. Varje konvertering har namnet `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, där `<portfolio_id>` är det numeriska portfölj-ID och `<se_acctid/conversion_manager_se_acctid>` är det numeriska ID:t för annonsnätverkskontot eller hanterarkontot. Konverteringen representerar alla viktade transaktionsegenskaper i målet.

Överför till [!DNL Google Ads] inträffar dagligen klockan 06:00 i annonsörens tidszon. Överför till [!DNL Microsoft® Advertising] inträffar dagligen klockan 09:00 i annonsörens tidszon.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Markera kryssrutan bredvid **[!UICONTROL Enable Objective Upload]**.

   Det här alternativet är bara tillgängligt om annonserarkontot är konfigurerat att använda hybridoptimering. Om du vill aktivera hybridoptimering kontaktar du kontoteamet på Adobe.

1. Klicka på **[!UICONTROL Save]**.

1. (Om dina konverteringar spåras på en chefskontonivå) [Lägg till autentiseringsuppgifter för ditt chefskonto](/help/search-social-commerce/admin/manager-accounts.md) på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Hantera en annonsörs transaktionsegenskaper](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [Överför konverteringsmått till [!DNL Google Ads]](conversion-metrics-upload-to-google.md)

