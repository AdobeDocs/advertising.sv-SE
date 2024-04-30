---
title: Aktivera överföring av mål till annonsnätverk
description: Lär dig hur du överför mål för dina hybridportfolior till [!DNL Google Ads] och [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 1f2ffd65f9341db4492a2796bc82ed0bb42f13ed
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Aktivera överföring av mål till annonsnätverk

*Annonsörer med [!DNL Google Ads] och [!DNL Microsoft® Advertising] endast konton*

*Annonsörer endast aktiverade för hybridoptimering*

Search, Social, &amp; Commerce kan överföra målen för ett annonskontos portföljer till [!DNL Google Ads] och [!DNL Microsoft® Advertising] så att du kan använda dem för hybridoptimering. De uppladdade målen är tillgängliga som konverteringsåtgärder för anpassade konverteringsmål på kontonivå och kampanjnivå.

Om du aktiverar det här alternativet aktiveras automatiskt en överföring för mål i portföljer som innehåller kampanjer med smarta budgivningsstrategier. Search, Social, &amp; Commerce skapar en konvertering i annonsnätverket för varje relevant mål. Konverteringen representerar alla viktade konverteringsvärden i målet. Varje konvertering har ett av följande namn:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  där `<network_ID>` är det numeriska ID som används för annonsnätverket i Search, Social och Commerce, `<objective_id>` är det numeriska mål-ID:t, och `<network_account_ID>` är det numeriska ID:t för annonsnätverkskontot eller hanterarkontot.

* (Gammalt format som kommer att bli inaktuellt i framtiden) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  där `<portfolio_id>` är det numeriska portfölj-ID:t och `<se_acctid/conversion_manager_se_acctid>` är det numeriska ID:t för annonsnätverkskontot eller hanterarkontot.

  Kontoteamet på Adobe kommer att arbeta med dig för att migrera befintliga namn på konverteringsåtgärder i annonsnätverket innan det gamla formatet har tagits bort. Under migreringsperioden kommer både den gamla och den nya formatöverföringen att köras parallellt. Modellering och optimering påverkas inte eftersom de nya konverteringsåtgärderna visas först med sekundär (inte optimerad) status och med 90 dagars data för bakåtfyllnad.

Överför till [!DNL Google Ads] inträffar dagligen klockan 06:00 i annonsörens tidszon. Överför till [!DNL Microsoft® Advertising] inträffar dagligen klockan 09:00 i annonsörens tidszon.

>[!IMPORTANT]
>
>Konverteringar som spåras av Google Ads och Microsoft Advertising Universal Event tracking (UET)-taggen överförs inte till annonsnätverken igen. Om ni inkluderar dem i ett mål lägger ni till dem i kampanjmålen i annonsnätverkets redaktör.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Markera kryssrutan intill **[!UICONTROL Enable Objective Upload]**.

1. (Annonsörer med [!DNL Google Ads] konton som bedriver verksamhet i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK); valfritt) Om du har inhämtat samtycke från användare i EES och Storbritannien att överföra sina uppgifter i annonssyfte markerar du kryssrutan bredvid **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicka på **[!UICONTROL Save]**.

1. (Om dina konverteringar spåras på en chefskontonivå) [Lägg till autentiseringsuppgifter för ditt chefskonto](/help/search-social-commerce/admin/manager-accounts.md) på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

När den dagliga överföringen är klar kan du verifiera att konverteringsåtgärderna visas i annonsnätverket.

>[!MORELIKETHIS]
>
>* [Om att hantera en annonsörs konverteringsstatistik](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Överför konverteringsmått till [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
