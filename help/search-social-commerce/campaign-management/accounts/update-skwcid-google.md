---
title: "Uppdatera s\_kwcid-spårningskod för en [!DNL Google Ads] konto"
description: Lär dig hur du byter till den senaste s\_kwcid-spårningskoden för en [!DNL Google Ads] konto.
source-git-commit: a9e23de134274d8f5004a908853c4132300b84e8
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Uppdatera s\_kwcid-spårningskoden för en [!DNL Google Ads] konto

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*[!DNL Google Ads]endast konton*

Det gamla formatet för s\_kwcid-spårningskoden för befintlig [!DNL Google Ads] konton har inte stöd för vissa funktioner i Analytics, till exempel rapportering på kampanjnivå och annonsgruppsnivå för [!DNL Google Ads] max-prestandakampanjer, utkast och experimentera och andra användningsfall där samma kombination av ad+keyword+match finns i flera kampanjer.

Det senaste formatet innehåller parametrar för kampanj-ID och annonsgrupps-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Du kan ändra till det nya formatet för något eller alla befintliga konton, enskilt. Om ni inte har max antal resultatkampanjer eller utkast och experimentkampanjer är migrering till det nya formatet valfritt.

Alla nya [!DNL Google Ads] kontona använder automatiskt det nya s\_kwcid-formatet.

>[!NOTE]
>
>När du har migrerat ett konto rapporteras alla klicknings-, kostnads- och visningsdata korrekt efter ändringen, men alla klickningar som inträffade före migreringen tillskrivs fortfarande konverteringsdata baserat på det gamla s\_kwcid-formatet.

1. På huvudmenyn klickar du på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Håll markören över kontonamnet och klicka ![pil-listruteikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png)och sedan markera **[!UICONTROL Edit]**.
1. Klicka på **[!UICONTROL Set Account Tracking]**.
1. Starta migreringen:

   1. Nästa till **[!UICONTROL S_KWCID FORMAT]** , klicka **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Klicka på **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Markera kryssrutan i bekräftelsemeddelandet och klicka sedan på **[!UICONTROL Continue]**.
   1. Klicka på **[!UICONTROL Post]**.

   Metadata för kampanjerna uppdateras i Analytics inom några dagar. Spårningen fortsätter utan avbrott, så inga data går förlorade, men rapporteringen kanske inte speglar de nya spårningskoderna förrän Analytics tar emot alla metadata.

   >[!NOTE]
   >
   >Alla klickningar som inträffade före migreringen rapporterar fortfarande konverteringsdata baserat på det gamla formatet.

1. När du har påbörjat migreringen uppdaterar du inställningarna för landningssidans suffix (kallat &quot;slutligt URL-suffix&quot; i vissa annonsnätverk) efter behov:

   * När funktionen &quot;Automatisk överföring&quot; är aktiverad i spårningsinställningarna uppdaterar Search, Social och Commerce automatiskt spårningskoden i Landing Page Suffix för det här kontot och dess kampanjer. Ni behöver inte göra någonting.
   * När funktionen &quot;Automatisk överföring&quot; inte är aktiverad och du inte använder serversidans s-kwcid, måste du uppdatera parametern s\_kwcid manuellt i inställningarna för landningssidans suffix. Du kan ändra konto- och kampanjnivåsuffix manuellt i konto- och kampanjinställningarna eller genom att överföra ändringar i ett kalkylblad. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du [!DNL Google Ads] redigerare.
   * Om du tar med s\_kwcid i inställningen för bas-URL för någon kampanjkomponent flyttar du den till relevant inställning för Landing Page Suffix.

1. (Rekommenderas) Verifiera data för det här kontot i Analytics innan du migrerar ytterligare konton.

>[!MORELIKETHIS]
>
>* [Hantera och nätverkskonton](ad-network-account-manage.md)
>* [s_kwcid tracking-parametern](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Översikt över [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
