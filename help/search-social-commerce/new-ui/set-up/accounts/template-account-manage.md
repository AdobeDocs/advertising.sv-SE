---
title: (Nytt användargränssnitt) Hantera [!DNL Naver] konton endast för spårning
description: Lär dig hur du konfigurerar och hanterar kontoinformation i det nya användargränssnittet för ett [!DNL Naver] konto.
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nytt användargränssnitt) Hantera [!DNL Naver]-konton endast för spårning

*Beta-funktion*

Nedan följer instruktioner om hur du hanterar [[!DNL Naver] konton](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) för att spåra, rapportera om och visualisera prestanda för annonser som du köper direkt från annonsnätverket. Search, Social, &amp; Commerce synkroniserar inte data med annonsnätverket, erbjuder automatiserad budgivning eller erbjuder någon typ av optimering eller simuleringar.

Mer information om tillgängliga funktioner finns i &quot;[Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Skapa information om annonsnätverkskonton {#create-account}

Om du vill aktivera spårning av ett konto måste du skapa en motsvarande kontopost som innehåller kontoinloggningsuppgifterna och med statusen *aktiverad*.

>[!NOTE]
>
>Om du vill skapa ett verkligt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Account]**.

1. Klicka på annonsnätverkets namn och sedan på **[!UICONTROL Next]**.

1. Ange [kontoinställningarna](#account-settings-naver):

   1. På fliken **[!UICONTROL Enter Account Details]** anger du de allmänna kontoinställningarna.

   1. (Annonsörer med en [[!DNL Adobe Analytics for Advertising] integrering](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och välj alla [!DNL Analytics] rapporteringsprogram som ska användas för att spåra och rapportera kampanjaktiviteter.

1. Klicka på **[!UICONTROL Save]**.

## Redigera information om nätverkskonton {#edit-account}

Om du vill ändra kontonamnet, ändra kontostatusen eller ändra rapportsviterna [!DNL Analytics] som ska användas för spårning och rapportering redigerar du kontoinformationen.

>[!NOTE]
>
>Om du vill redigera ett faktiskt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Välj konto på något av följande sätt:

   * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

   * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

1. Redigera [kontoinställningarna](#account-settings-api):

   1. (Valfritt) Redigera kontoinformationen på fliken **[!UICONTROL Account Details]**.

   1. (Valfritt, annonsörer med en [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och redigera [!DNL Analytics]-rapporteringssviterna som ska användas för att spåra och rapportera kampanjaktiviteter.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicka på **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Inställningar för annonsnätverkskonto {#account-settings-api}

### Fliken [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Namnet som ska visas för kontot i Sök, Socialt och Commerce.

>[!NOTE]
>
>Om du har en integrering med Search, Social och Commerce-Adobe Analytics och ändrar namnet på sökkontot ber du ditt Adobe-kontoteam att uppdatera mappningen.

**[!UICONTROL Network Account ID]:** Konto-ID som tilldelats av annonsnätverket.

**[!UICONTROL Currency]:** Förkortningen för valutan som används för kontot.

**[!UICONTROL Time Zone]:** Annonsörens tidszon.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Sökning, socialt och Commerce synkroniserar kampanjdata med kontot (när det stöds) och pushar automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer.

## Fliken [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, &amp; Commerce send data you upload for the ad network, including entity classifications and click data for the account.

För att data ska visas i rapportsviterna måste antingen (a) funktionen för AMO ID på serversidan konfigureras för kontot eller (b) inställningen [!UICONTROL Enable Advertising reporting in Analytics] på annonsörnivå måste aktiveras. Dessutom måste annonserarens [!DNL Analytics]-konto vara konfigurerat för att ta emot data från Search, Social och Commerce. Kontakta Adobe Account Team om du vill ha mer information.

>[!MORELIKETHIS]
>
>* [Implementera [!DNL Naver] konton med endast spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Om annonskonton](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
