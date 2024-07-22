---
title: Överför konverteringsmått till  [!DNL Google Ads]
description: Lär dig hur du överför konverteringsstatistik för sökning, sociala medier och Commerce till  [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Överför konverteringsmått till [!DNL Google Ads]

*Annonsörer med [!DNL Google Ads] Endast konton*

Search, Social, &amp; Commerce kan överföra alla konverteringsmått som spåras till [!DNL Google Ads] för [!DNL Google Ads]-kampanjer som använder Adobe Advertising-konverteringstjänsten. Det här alternativet gör inte konverteringarna tillgängliga för hybridoptimering. Om du vill använda dina Adobe-konverteringar för hybridoptimering läser du i &quot;[Aktivera överföring av mål till annonsnätverk](objective-upload-to-networks.md)&quot;.

Dagliga överföringar inkluderar det spårade `gclid`-värdet, konverteringsvärdet som definierats med attribueringsmodellen på annonsörnivå och tidsstämpeln. Om attribueringsmodellen uppdateras kommer nästa överföring att använda den nya modellen, men tidigare data uppdateras inte för att använda den nya modellen.

>[!NOTE]
>
>Överföringarna inkluderar inte konverteringsmått som överförts till Adobe Advertising från feedsfiler.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]** på huvudmenyn.

1. Markera kryssrutan bredvid **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Annonsörer som bedriver verksamhet i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK); valfritt) Om du har inhämtat medgivande från användare i EES och Storbritannien att överföra sina data i annonssyfte markerar du kryssrutan bredvid **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicka på **[!UICONTROL Save]**.

1. (Om dina konverteringar spåras på en hanterarkontonivå) [Lägg till autentiseringsuppgifter för ditt hanterarkonto](/help/search-social-commerce/admin/manager-accounts.md) på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Aktivera överföring av mål till annonsnätverk](objective-upload-to-networks.md)
