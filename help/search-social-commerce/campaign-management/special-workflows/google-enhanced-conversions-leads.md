---
title: Implementera [!DNL Google Ads] utökade konverteringar för leads
description: Lär dig mer om arbetsflödet för att konfigurera  [!DNL Google Ads] förbättrade konverteringar för leads.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: e0b1a65e3eddc41bed73817dabb6e38b1ef881b5
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Implementera [!DNL Google Ads] utökade konverteringar för leads

Endast *[!DNL Google Ads]konton*

Med [[!DNL Google Ads] förbättrade konverteringar för leads](https://support.google.com/google-ads/answer/9888656) kan du mappa användare till offlinekonverteringar med hjälp av dina egna konverteringsdata. Använd förbättrade konverteringar för leads i miljöer där klicknings-ID inte är tillgängliga, till exempel för att spåra telefonförsäljning eller e-postförsäljning som är ett resultat av webbleads.

I Search, Social och Commerce kan du

* Visa dina befintliga förbättrade konverteringar för leads.

  Search, Social, &amp; Commerce synkroniserar dina befintliga förbättrade konverteringar för leads varje dag kl. 05:00 i annonsörens tidszon.

* Skapa bättre konverteringar för leads.

* Ladda upp konverteringsdata från första part, offline för att mappa till era förbättrade konverteringar för leads.

* Inkludera era förbättrade konverteringar för leads som mätvärden i rapporter och som viktade mätvärden inom mål för optimering.

Utför följande steg om du vill använda den här funktionen. Stegen för att skapa konverteringsspårningstaggar och för att skapa konverteringsåtgärder kan också ångras.

1. I [!DNL Google Ads] väljer du att få utökade konverteringar för leads:

   1. Öppna kontots konverteringsinställningar.

   1. Välj alternativet för utökade konverteringar för leads och acceptera användarvillkoren.

   1. Välj om du vill använda en [!DNL Google]-tagg eller [!DNL Google Tag Manager] för att skapa konverteringstaggen.

1. Konfigurera och implementera en tagg för att spåra konverteringsåtgärden.

   Instruktioner finns i hjälpen för [!DNL Google Ads] om hur du skapar taggar för förbättrad konvertering av leads [med en [!DNL Google] tagg](https://support.google.com/google-ads/answer/11021502) eller [med  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Skapa en konverteringsåtgärd för den förbättrade konverteringen av leads i antingen [Sök, Social och Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) eller [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Om du skapar konverteringsåtgärden i Sök, Socialt och Commerce anger du **typen av konvertering** som *Importera konvertering* eller *Importera.*

1. Ladda upp egna data, inklusive hash-kodade e-postadresser eller telefonnummer, och tilldela konverteringen för ett visst konto så ofta det behövs. Du kan slutföra det här steget från antingen [Sök, Socialt och Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) eller med [!DNL Google Data Manager].

   * I Search, Social och Commerce kan du hämta en mall i [!DNL Microsoft Excel]-format, ange konverteringsdata och spara filen lokalt och sedan överföra den redigerade filen. Mallen innehåller kolumner som anger om användargodkännande har getts för att överföra data till [!DNL Google] i annonssyfte och för annonspersonalisering.

     Alla överförda data synkroniseras i realtid till [!DNL Google Ads].

   * Mer information om hur du överför data med [!DNL Google Data Manager] finns i [Om Datahanteraren](https://support.google.com/google-ads/answer/14639041).

>[!MORELIKETHIS]
>
>* [Skapa en konverteringsåtgärd för en [!DNL Google Ads] förbättrad konvertering för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
