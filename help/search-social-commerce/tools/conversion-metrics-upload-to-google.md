---
title: Överför konverteringsmått till [!DNL Google Ads]
description: Lär dig hur du överför konverteringsstatistik för sökning, sociala medier och handel till [!DNL Google Ads].
exl-id: 88db66c2-12db-41cf-b6c4-ed821cb3b8ea
source-git-commit: 00f9e5e3892be305f5d7c69161bdb7609f13f1bf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Överför konverteringsmått till [!DNL Google Ads]

*Annonsörer med [!DNL Google Ads] Endast konton*

Sök, Socialt, &amp; Commerce kan överföra till [!DNL Google Ads] alla konverteringsmått som identifieras [!DNL Google Ads] kampanjer som använder Adobe Advertising konverteringsspårningstjänsten och konverteringsstatistik som synkroniseras från Adobe Analytics. Det här alternativet gör inte konverteringarna tillgängliga för hybridoptimering. Om du vill använda dina Adobe-konverteringar för hybridoptimering, se&quot;[Aktivera överföring av mål till annonsnätverk](objective-upload-to-networks.md).&quot;

Dagliga överföringar inkluderar spårade `gclid` värdet, det konverteringsvärde som definieras med hjälp av attribueringsmodellen på annonsörnivå och tidsstämpeln. Om attribueringsmodellen uppdateras kommer nästa överföring att använda den nya modellen, men tidigare data uppdateras inte för att använda den nya modellen.

>[!NOTE]
>
>Överföringarna inkluderar inte konverteringsmått som överförts till Adobe Advertising från feed-filer.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Markera kryssrutan bredvid **[!UICONTROL Upload Conversions to Google Ads]**.

1. Klicka på **[!UICONTROL Save]**.

1. (Om dina konverteringar spåras på en chefskontonivå) [Lägg till autentiseringsuppgifter för ditt chefskonto](/help/search-social-commerce/admin/manager-accounts.md) på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Aktivera överföring av mål till annonsnätverk](objective-upload-to-networks.md)
