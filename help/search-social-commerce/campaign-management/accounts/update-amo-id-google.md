---
title: Uppdatera spårningskod för AMO ID (s_kwcid) för en [!DNL Google Ads] konto
description: Lär dig hur du byter till den senaste spårningskoden för AMO ID för en [!DNL Google Ads] konto.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Uppdatera spårningskod för AMO ID (s_kwcid) för en [!DNL Google Ads] konto

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*[!DNL Google Ads]endast konton*

Det äldre formatet (före oktober 2019) för [Spårningskod för AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) för befintlig [!DNL Google Ads] konton har inte stöd för vissa funktioner i Analytics, till exempel rapportering på kampanjnivå och annonsgruppsnivå för [!DNL Google Ads] max-prestandakampanjer, utkast och experimentera och andra användningsfall där samma kombination av ad+keyword+match finns i flera kampanjer.

Det aktuella formatet innehåller parametrar för kampanj-ID och annonsgrupps-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Du kan ändra det aktuella formatet för ett eller alla befintliga konton, enskilt. Om ni inte har max antal resultatkampanjer eller utkast och experimentkampanjer är migrering till det nya formatet valfritt.

Alla nya [!DNL Google Ads] konton använder automatiskt det aktuella AMO ID-formatet.

>[!NOTE]
>
>När du har migrerat ett konto rapporteras alla klicknings-, kostnads- och visningsdata korrekt efter ändringen, men alla klickningar som inträffade före migreringen tillskrivs fortfarande konverteringsdata baserat på det gamla AMO-ID-formatet.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Håll markören över kontonamnet och klicka ![pil-listruteikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png)och sedan markera **[!UICONTROL Edit]**.

1. Klicka på **[!UICONTROL Set Account Tracking]**.

1. Starta migreringen:

   1. Nästa till **[!UICONTROL S_KWCID FORMAT]** , klicka **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klicka på **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Markera kryssrutan i bekräftelsemeddelandet och klicka på **[!UICONTROL Continue]**.

   1. Klicka på **[!UICONTROL Post]**.

   Metadata för kampanjerna uppdateras i [!DNL Analytics] inom några dagar. Spårningen fortsätter utan avbrott, så inga data går förlorade, men rapporteringen kanske inte speglar de nya spårningskoderna förrän [!DNL Analytics] tar emot alla metadata.

   >[!NOTE]
   >
   >Alla klickningar som inträffade före migreringen rapporterar fortfarande konverteringsdata baserat på det gamla formatet.

1. När du har påbörjat migreringen uppdaterar du inställningarna för landningssidans suffix (kallat &quot;slutligt URL-suffix&quot; i vissa annonsnätverk) efter behov:

   * När [!UICONTROL Auto Upload]&quot; är aktiverat i spårningsinställningarna så uppdaterar Search, Social och Commerce automatiskt spårningskoden i Landing Page Suffix för det här kontot och dess kampanjer. Ni behöver inte göra någonting.

   * När [!UICONTROL Auto Upload]&quot; är inte aktiverad och du använder inte [AMO ID-funktion på serversidan](/help/integrations/analytics/ids.md#amo-id-formats)måste du manuellt uppdatera parametern AMO ID i inställningarna för delningssidans suffix. Du kan ändra konto- och kampanjnivåsuffix manuellt i konto- och kampanjinställningarna eller genom att överföra ändringar i ett kalkylblad. Om du vill konfigurera ett suffix på annonsgruppnivå eller lägre använder du [!DNL Google Ads] redigerare.

   * Om du inkluderar AMO-ID:t i inställningen Bas-URL för någon kampanjkomponent, flyttar du det till relevant inställning för Landing Page Suffix.

1. (Rekommenderas) Verifiera data för kontot i [!DNL Analytics] innan du migrerar ytterligare konton.

>[!MORELIKETHIS]
>
>* [Hantera och nätverkskonton](ad-network-account-manage.md)
>* [Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Översikt [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
