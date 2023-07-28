---
title: Produktfilter för köpkampanjer
description: Referera till de produktfilter som finns för att handla produktgrupper.
exl-id: 9c4f3c64-5a51-49de-aeba-bcda8a379609
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Produktfilter för köpkampanjer

Se även [!DNL Google Ads] help &quot;[Hantera en shoppingkampanj med produktgrupper](https://support.google.com/google-ads/answer/6275317)&quot; och [!DNL Microsoft Advertising] help &quot;[Förstå och använda produktgrupper](https://help.ads.microsoft.com/#apex/bae/en/56782).&quot;

| Shoppingnätverk | Dimension | Attribut | Anteckningar |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] till [!UICONTROL Category 5=] | \[Kategori-ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[varumärke\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[objekt-ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] till [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[Produkttyp\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] till [!UICONTROL Custom Label 4=] | \[The attribute for the custom label\] | — |
| [!DNL Google Ads] | Kanal= | [!UICONTROL Local], [!UICONTROL Online] | Visa endast annonser för lokala produkter eller onlineprodukter.<br><br><b>Obs!</b> Om du vill skapa annonser för lokala produkter måste alternativet &quot;Lokala lagerannonser&quot; vara aktiverat och du måste vara med i det lokala shoppingprogrammet med [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Om annonser ska visas för produkter som bara är tillgängliga för en kanal (antingen endast lokalt eller endast online) eller som är tillgängliga för flera kanaler (både lokalt och online). |

>[!MORELIKETHIS]
>
>* [Implementera [!DNL Google Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [Implementera [!DNL Microsoft Advertising Ads] shoppingkampanjer](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
>* [Om att handla produktgrupper](product-group-about.md)
>* [Hantera produktgrupper för butik](product-group-manage.md)
>* [[!DNL Google Ads] produktgruppsinställningar](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-google.md)
>* [[!DNL Microsoft® Advertising] produktgruppsinställningar](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md)
>* [[!DNL Google Ads] inställningar för butiks- och mallinställningar för lagerflöden](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)
>* [[!DNL Microsoft Advertising] inställningar för butiks- och mallinställningar för lagerflöden](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md)
>* [Obligatoriska data för [!DNL Google Ads] glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
>* [Obligatoriska data för [!DNL Microsoft Advertising] glödlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
