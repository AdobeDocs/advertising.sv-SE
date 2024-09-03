---
title: Ladda upp offlinekonverteringsdata för förbättrad konvertering
description: Lär dig hur du överför konverteringsdata från första part, offline för att mappa till  [!DNL Google Ads] förbättrade konverteringar för leads.
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Ladda upp offlinekonverteringsdata för förbättrad konvertering

Endast *[!DNL Google Ads]konton*

<!-- Tweak metadata title/description and heading -->

Du kan överföra dina egna offlinekonverteringsdata, inklusive hashade e-postadresser och telefonnummer, för att mappa till dina befintliga [[!DNL Google Ads] förbättrade konverteringar för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md). Alla överförda data synkroniseras i realtid till [!DNL Google Ads].

## Överför data för [!DNL Google Ads] förbättrade konverteringar för leads

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** på huvudmenyn och klicka sedan på fliken **[!UICONTROL Upload]**.

1. Välj annonsnätverket och sedan kontot.

1. (Valfritt) Om du vill hämta en mall med alla [obligatoriska datafält](#enhanced-conversions-leads-data) i [!DNL Microsoft Excel]-format klickar du på **[!UICONTROL View Template]** och hämtar sedan filen enligt webbläsarens normala procedur.

   Du kan redigera filen så att den innehåller dina data och spara ändringarna, och sedan överföra filen i nästa steg.

1. Klicka på **[!UICONTROL Choose File]** och välj sedan en fil som ska överföras från enheten eller nätverket.

## Nödvändiga data för överförda filer {#enhanced-conversions-leads-data}

### Data ovanför tabellen

`Parameters:TimeZone=insert_timezone`

Ange kontots tidszon antingen på den här platsen eller i kolumnen [!UICONTROL Conversion Time] för varje rad. Använd antingen a) det [tidszon-ID som stöds](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) eller b) GMT-förskjutningen, vilket anges med + eller - och den 4-siffriga tidsskillnaden (till exempel -0500 för New York).

### Tabellkolumner och -värden

| Kolumn | Beskrivning |
| ------ | ----------- |
| E-post | Användarens e-postadress, som måste hashas med hjälp av SHA-256-algoritmen. Varje rad måste innehålla antingen ett e-postvärde eller ett telefonnummer. |
| Telefonnummer | Användarens telefonnummer, som måste hashas med hjälp av SHA-256-algoritmen. Den måste innehålla en landskod och kan innehålla bindestreck och andra symboler. Varje rad måste innehålla antingen ett e-postvärde eller ett telefonnummer. |
| Konverteringsnamn | (Obligatoriskt) Namnet på konverteringsåtgärden. |
| Konverteringstid | (Obligatoriskt) Den tidpunkt då konverteringshändelsen inträffade i ett [tidsformat som stöds](https://support.google.com/google-ads/answer/7014069#prepare_data). Om du inte inkluderar kontots tidszon-ID på raden `Parameters:TimeZone=insert_timezone` ovanför datatabellen, inkluderar du tidszonen för varje rad antingen med a) det [tidszon-ID som stöds](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) eller b) GMT-förskjutningen, vilket anges med + eller - och den 4-siffriga tidsskillnaden (till exempel -0500 för New York). |
| Konverteringsvärde | (Obligatoriskt) Det numeriska konverteringsvärdet. |
| Konverteringsvaluta | Valutakoden för konverteringshändelsen. |
| Annonsanvändardata | (Gäller för data som gäller användare i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK)) Anger om användargodkännande har lämnats för att skicka användardata till [!DNL Google] för annonspersonalisering. Värdena kan vara `Granted`, `Denied` eller \[null\] (som skickas till [!DNL Google Ads] som `Unspecified`). **Obs!** [!DNL Google Ads] kräver för närvarande inte samtycke för utökade konverteringar för leads, men det kan göra det i framtiden. |
| Lägg till Personalization | (Gäller för data som gäller användare i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK)) Anger om användartillstånd har lämnats för att skicka användardata till [!DNL Google] i reklamsyfte. Värdena kan vara `Granted`, `Denied` eller \[null\] (som skickas till [!DNL Google Ads] som `Unspecified`). **Obs!** [!DNL Google Ads] kräver för närvarande inte samtycke för utökade konverteringar för leads, men det kan göra det i framtiden. |

>[!MORELIKETHIS]
>
>* [Skapa en konverteringsåtgärd för en [!DNL Google Ads] förbättrad konvertering för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Implementera [!DNL Google Ads] förbättrade konverteringar för leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Överför konverteringsstatistik för sökning, sociala medier och Commerce till  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
