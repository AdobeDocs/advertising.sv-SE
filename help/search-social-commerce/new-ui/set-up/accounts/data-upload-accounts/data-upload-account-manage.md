---
title: Konfigurera och nätverkskonton för dataöverföring
description: Lär dig hur du konfigurerar och hanterar kontoinformation för ett annonsnätverkskonto.
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Hantera och nätverkskonton för dataöverföringar

<!-- Edit all, including title and metadata -->

Här följer instruktioner för hur du hanterar kontoinformation för annonsnätverkskonton som du överför kontodata för.

Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).

>[!NOTE]
>
>Instruktioner om hur du hanterar kontoinformation för ett annonsnätverkskonto som synkroniseras med API:t för Search, Social och Commerce finns i [Hantera annonsnätverkskonton via API-anslutning](../api-accounts/api-account-manage.md) i stället.

## Skapa kontoinformation {#create-account}

1. Klicka på **[!UICONTROL Create Account]**.

1. Klicka på annonsnätverkets namn och sedan på **[!UICONTROL Next]**.

1. Ange [kontoinställningarna](#account-settings):

   1. Redigera kontoinformationen på fliken **[!UICONTROL Account Details]**.

   1. (Annonsörer med en [[!DNL Adobe Analytics for Advertising] integrering](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och redigera [!DNL Analytics]-rapporteringssviterna som ska användas för att spåra och rapportera kampanjaktiviteter.

   1. (Valfritt) På fliken **[!UICONTROL Upload File]** överför du datafiler för kontot.

1. Klicka på **[!UICONTROL Save]**.

## Redigera kontoinformation {#edit-account}

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Välj konto på något av följande sätt:

   * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

   * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

1. Redigera [kontoinställningarna](#account-settings-upload):

   1. (Valfritt) Redigera kontoinformationen på fliken **[!UICONTROL Account Details]**.

   1. (Valfritt, annonsörer med en [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och redigera [!DNL Analytics]-rapporteringssviterna som ska användas för att spåra och rapportera kampanjaktiviteter.

   1. (Valfritt) På fliken **[!UICONTROL Upload File]** överför du datafiler för kontot.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicka på **[!UICONTROL Save]**.

## Aktivera eller inaktivera annonskonton {#enable-disable-account}

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Gör något av följande:

   * (Från vyn [!UICONTROL Accounts]):

      * (Om du vill aktivera kontot) Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Activate]** i verktygsfältet för gruppåtgärder.

      * (Om du vill inaktivera kontot) Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Pause]** i verktygsfältet för gruppåtgärder.

   * (Från kontoinställningarna):

      1. Välj konto på något av följande sätt:

         * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

         * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

      1. Stäng av **[!UICONTROL Account Details]** på fliken **[!UICONTROL Account enabled]**.

      1. Klicka på **[!UICONTROL Save]**.

## Kontoinställningar {#account-settings-upload}

### Fliken [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Namnet som ska visas för kontot i Sök, Socialt och Commerce.

>[!NOTE]
>
>Om du har en integrering med Search, Social och Commerce-Adobe Analytics och ändrar namnet på sökkontot kontaktar du Adobe Account Team så att de kan uppdatera mappningen.

**[!UICONTROL Network Account ID]:** Konto-ID som tilldelats av annonsnätverket. Detta ID används endast för rapportering. Search, Social, &amp; Commerce kommer inte att ansluta direkt till annonsnätverkskontot.

**[!UICONTROL Currency]:** (Skrivskyddad för befintliga konton) Förkortningen för valutan som används för kontot.

**[!UICONTROL Time Zone]:** (Skrivskyddad för befintliga konton) Annonsörens tidszon.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Med Search, Social och Commerce kan du hämta data automatiskt för en angiven S3-bucket.

## Fliken [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, &amp; Commerce send data you upload for the ad network, including entity classifications and click data for the account.

För att data ska visas i rapportsviterna måste antingen (a) funktionen för AMO ID på serversidan konfigureras för kontot eller (b) inställningen [!UICONTROL Enable Advertising reporting in Analytics] på annonsörnivå måste aktiveras. Dessutom måste annonserarens [!DNL Analytics]-konto vara konfigurerat för att ta emot data från Search, Social och Commerce. Kontakta Adobe Account Team om du vill ha mer information.

### Fliken [!UICONTROL Upload File]

(Valfritt) Överför datafiler för kontot.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
