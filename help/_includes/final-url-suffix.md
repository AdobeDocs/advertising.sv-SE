---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definition av slutlig URL-suffix

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] och [!DNL Microsoft Advertising] konton endast; valfritt) Alla parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. Inkludera alla parametrar som företaget måste spåra. Exempel:`param1=value1&param2=value2`

I konton som använder Adobe Advertising-konverteringsspårning måste suffixet innehålla annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]; `gclid` för [!DNL Google Ads]).

Konton med en Adobe Analytics-integrering måste använda parametern [AMO ID](/help/integrations/analytics/ids.md) . Om kontot har en AMO ID-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. I annat fall måste du lägga till den manuellt här. Se de [suffixformat som krävs för  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Det här fältet uppdateras inte av spårningsinställningen [!UICONTROL Auto Upload].
>* Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.
