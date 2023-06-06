---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Fält för landningssidessuffix i GGL- och MS-kontoinställningar, kampanjinställningar och vissa annonsinställningar

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] och [!DNL Microsoft Advertising] Endast konton. Valfria) Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. innehåller alla parametrar som företaget måste spåra. Exempel: `param1=value1&param2=value2`

Konton som använder konverteringsspårning för annonsering i Adobe måste innehålla annonsnätverkets klickidentifierare (`gclid` for [!DNL Google Ads] eller `msclkid` for [!DNL Microsoft Advertising]) i suffixet.

Konton med en Adobe Analytics-integrering måste använda parametern s_kwcid. Om kontot har en s_kwcid-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. annars måste du lägga till den manuellt här. Se [obligatoriska suffixformat för Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Anteckningar:**

* Det här fältet uppdateras inte av [!UICONTROL Auto Upload] spårningsinställning.

* Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.
