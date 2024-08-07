---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# Fält för landningssidessuffix i GGL- och MS-kontoinställningar, kampanjinställningar och vissa annonsinställningar

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] och [!DNL Microsoft Advertising] konton endast; valfritt) Alla parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Inkludera alla parametrar som företaget måste spåra. Exempel: `param1=value1&param2=value2`

Konton som använder Adobe Advertising-konverteringsspårning måste inkludera annonsnätverkets klickidentifierare (`gclid` för [!DNL Google Ads] eller `msclkid` för [!DNL Microsoft Advertising]) i suffixet.

Konton med en Adobe Analytics-integrering måste använda parametern s_kwcid. Om kontot har en s_kwcid-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. I annat fall måste du lägga till den manuellt här. Se de [obligatoriska suffixformaten för Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformaten för Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Anteckningar:**

* Det här fältet uppdateras inte av spårningsinställningen [!UICONTROL Auto Upload].

* Landing page suffix at lower levels override the account-level suffix. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.
