---
title: Uppdatera spårningskoden för AMO-ID (s_kwcid) för ett [!DNL Google Ads] konto
description: Lär dig hur du byter till den senaste spårningskoden för AMO ID för ett [!DNL Google Ads] konto.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Uppdatera spårningskoden för AMO-ID (s_kwcid) för ett [!DNL Google Ads]-konto

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Endast *[!DNL Google Ads]konton*

Det äldre formatet (före oktober 2019) för spårningskoden för [AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) för befintliga [!DNL Google Ads]-konton stöder inte vissa funktioner i Analytics, till exempel rapportering på kampanjnivå och annonsgruppsnivå för [!DNL Google Ads] prestandamängdskampanjer, utkast och experimentkampanjer, och andra användningsfall där samma kombination av typen ad+keyword+match finns i flera kampanjer.

Det aktuella formatet innehåller parametrar för kampanj-ID och annonsgrupps-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

För ett befintligt konto som använder det äldre formatet kan du ändra till det aktuella formatet. Om ni inte har max antal resultatkampanjer eller utkast och experimentkampanjer är migrering till det nya formatet valfritt.

Alla nya [!DNL Google Ads]-konton använder automatiskt det aktuella AMO ID-formatet.

>[!NOTE]
>
>Det här alternativet är bara tillgängligt för konton som inte använder det aktuella formatet.
>
>När du har migrerat ett konto rapporteras alla klicknings-, kostnads- och visningsdata korrekt efter ändringen, men alla klickningar som inträffade före migreringen tillskrivs fortfarande konverteringsdata baserat på det gamla AMO-ID-formatet.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** på undermenyn.

1. Håll markören över kontonamnet, klicka på ![pil-listruteikonen](/help/search-social-commerce/assets/arrow-dropdown-menu.png) och välj sedan **[!UICONTROL Edit]**.

1. Klicka på **[!UICONTROL Set Account Tracking]**.

1. Starta migreringen:

   1. Klicka på **[!UICONTROL S_KWCID FORMAT]** bredvid [!UICONTROL Account Tracking] i inställningarna för **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klicka på **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Markera kryssrutan i bekräftelsemeddelandet och klicka sedan på **[!UICONTROL Continue]**.

   1. Klicka på **[!UICONTROL Post]** i kontoinställningarna.

   Metadata för kampanjerna uppdateras om [!DNL Analytics] inom några dagar. Spårningen fortsätter utan avbrott, så inga data går förlorade, men rapporteringen kanske inte speglar de nya spårningskoderna förrän [!DNL Analytics] tar emot alla metadata.

   >[!NOTE]
   >
   >Alla klickningar som inträffade före migreringen rapporterar fortfarande konverteringsdata baserat på det gamla formatet.

1. När du har påbörjat migreringen uppdaterar du inställningarna för landningssidans suffix (kallat &quot;slutligt URL-suffix&quot; i vissa annonsnätverk) efter behov:

   * När funktionen [!UICONTROL Auto Upload] är aktiverad i spårningsinställningarna uppdaterar Search, Social och Commerce automatiskt spårningskoden i Landing Page Suffix för det här kontot och dess kampanjer. Ni behöver inte göra någonting.

   * När funktionen [!UICONTROL Auto Upload] inte är aktiverad och du inte använder funktionen [AMO ID på serversidan](/help/integrations/analytics/ids.md#amo-id-formats) måste du uppdatera parametern AMO ID manuellt i inställningarna för landningssidans suffix. Du kan ändra konto- och kampanjnivåsuffix manuellt i [kontoinställningarna](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) och [kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) eller genom att [överföra ändringar i ett kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Google Ads]-redigeraren.

   * Om du inkluderar AMO-ID:t i inställningen Bas-URL för någon kampanjkomponent, flyttar du det till relevant inställning för Landing Page Suffix.

1. (Rekommenderas) Verifiera data för det här kontot i [!DNL Analytics] innan du migrerar ytterligare konton.

>[!MORELIKETHIS]
>
>* [Hantera annonskonton](ad-network-account-manage.md)
>* [Adobe Advertising ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Översikt över [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=sv-SE){target="_blank"}
