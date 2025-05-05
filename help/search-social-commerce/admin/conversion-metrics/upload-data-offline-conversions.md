---
title: Ladda upp offlinekonverteringsdata för förbättrad konvertering
description: Lär dig hur du överför konverteringsdata från första part, offline för att mappa till  [!DNL Google Ads] förbättrade konverteringar för leads och [!DNL Microsoft Advertising] förbättrade konverteringar.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Ladda upp offlinekonverteringsdata för förbättrad konvertering

Endast *[!DNL Google Ads]och [!DNL Microsoft Advertising] konton*

Du kan överföra dina egna offlinekonverteringsdata, inklusive hash-kodade e-postadresser och telefonnummer, för att mappa till dina befintliga [[!DNL Google Ads] förbättrade konverteringar för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) och [[!DNL Microsoft Advertising] förbättrade konverteringar](https://help.ads.microsoft.com/#apex/ads/en/60178). Alla överförda data synkroniseras i realtid till annonsnätverket.

## Ladda upp data för förbättrad konvertering

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** på huvudmenyn och klicka sedan på fliken **[!UICONTROL Upload]**.

1. Välj annonsnätverket och sedan kontot.

1. (Valfritt) Om du vill hämta en mall med alla [obligatoriska datafält](#enhanced-conversions-leads-data) i [!DNL Microsoft Excel]-format klickar du på **[!UICONTROL View Template]** och hämtar sedan filen enligt webbläsarens normala procedur.

   Du kan redigera filen så att den innehåller dina data och spara ändringarna, och sedan överföra filen i nästa steg.

1. Klicka på **[!UICONTROL Choose File]** och välj sedan en fil som ska överföras från enheten eller nätverket.

## Nödvändiga data för överförda filer {#enhanced-conversions-leads-data}

### Data ovanför tabellen

`Parameters:TimeZone=insert_timezone`

Ange kontots tidszon antingen på den här platsen eller i kolumnen [!UICONTROL Conversion Time] för varje rad. Använd antingen a\) ([!DNL Google Ads only]) det [tidszon-ID som stöds](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) eller b\) GMT-förskjutningen, vilket anges med + eller - och den 4-siffriga tidsskillnaden (till exempel -0500 för New York, +0100 för Berlin eller +0000 för Greenwich Mean Time).

### Tabellkolumner och värden för [!DNL Google Ads]

| Kolumn | Beskrivning |
| ------ | ----------- |
| E-post | Användarens e-postadress, som måste hashas med hjälp av SHA-256-algoritmen. Varje rad måste innehålla antingen ett e-postvärde eller ett telefonnummer. |
| Telefonnummer | Användarens telefonnummer, som måste hashas med hjälp av SHA-256-algoritmen. Den måste innehålla en landskod och kan innehålla bindestreck och andra symboler. Varje rad måste innehålla antingen ett e-postvärde eller ett telefonnummer. |
| Konverteringsnamn | (Obligatoriskt) Namnet på konverteringsåtgärden. |
| Konverteringstid | (Obligatoriskt) Den tidpunkt då konverteringshändelsen inträffade i ett [tidsformat som stöds](https://support.google.com/google-ads/answer/7014069#prepare_data). Om du inte inkluderar kontots tidszon-ID i raden `Parameters:TimeZone=insert_timezone` ovanför datatabellen, inkluderar du tidszonen för varje rad med antingen a\) [ID-formatet för den tidszon som stöds](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) eller b\) GMT-förskjutningen, vilket anges med + eller - och den 4-siffriga tidsskillnaden (till exempel -0500 för New York, +0100 för Berlin eller +0 (000 för Greenwich Mean Time). |
| Konverteringsvärde | (Obligatoriskt) Det numeriska konverteringsvärdet. |
| Konverteringsvaluta | Valutakoden för konverteringshändelsen. |
| Annonsanvändardata | (Gäller för data som gäller användare i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK)) Anger om användargodkännande har lämnats för att skicka användardata till [!DNL Google] för annonspersonalisering. Värdena kan vara `Granted`, `Denied` eller \[null\] (som skickas till [!DNL Google Ads] som `Unspecified`). **Obs!** [!DNL Google Ads] kräver för närvarande inte samtycke för utökade konverteringar för leads, men det kan göra det i framtiden. |
| Lägg till Personalization | (Gäller för data som gäller användare i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK)) Anger om användartillstånd har lämnats för att skicka användardata till [!DNL Google] i reklamsyfte. Värdena kan vara `Granted`, `Denied` eller \[null\] (som skickas till [!DNL Google Ads] som `Unspecified`). **Obs!** [!DNL Google Ads] kräver för närvarande inte samtycke för utökade konverteringar för leads, men det kan göra det i framtiden. |

### Tabellkolumner och värden för [!DNL Microsoft Advertising]

Mer information om hur du använder mallen finns i [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Kolumn | Beskrivning |
| ------ | ----------- |
| Konverteringsnamn | (Obligatoriskt) Namnet på konverteringsmålet. |
| Konverteringstid | (Obligatoriskt) Den tidpunkt då konverteringshändelsen inträffade. Om du inte inkluderar kontots tidszon-ID i raden `Parameters:TimeZone=insert_timezone` ovanför datatabellen, inkluderar du tidszonen för varje rad med GMT-förskjutningen, vilket anges med + eller -, och den 4-siffriga tidsskillnaden (till exempel -0500 för New York, +0100 för Berlin eller +0000 för Greenwich Mean Time). En lista över tidszoner för olika städer finns i [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), men se till att du använder det format som anges här i stället för formatet i tidszonslistan. |
| Konverteringsvärde | (Obligatoriskt) Det numeriska konverteringsvärdet. |
| Konverteringsvaluta | Valutakoden för konverteringshändelsen. |
| Microsoft Click ID | Den associerade unika klickidentifieraren [!DNL Microsoft] (MSCLKID). Det här fältet kan vara tomt för utökade offlinekonverteringar. |
| Hash-kodad e-postadress | Användarens e-postadress, som måste hashas med hjälp av SHA-256-algoritmen. För förbättrade offlinekonverteringar måste varje rad innehålla antingen ett värde för Hash-kodad e-postadress eller ett Hashed-telefonnummer. |
| Hash-kodat telefonnummer | Användarens telefonnummer, som måste hashas med hjälp av SHA-256-algoritmen. Den måste innehålla en landskod och kan innehålla bindestreck och andra symboler. För förbättrade offlinekonverteringar måste varje rad innehålla antingen ett värde för Hash-kodad e-postadress eller ett Hashed-telefonnummer. |

>[!MORELIKETHIS]
>
>* [Implementera [!DNL Google Ads] förbättrade konverteringar för leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementera [!DNL Microsoft Advertising] förbättrade offlinekonverteringar](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only]) [Skapa en konverteringsåtgärd för en [!DNL Google Ads] förbättrad konvertering för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Överför konverteringsstatistik för sökning, sociala medier och Commerce till  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
