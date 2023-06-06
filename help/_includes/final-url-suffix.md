---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definition av slutlig URL-suffix

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] och [!DNL Microsoft Advertising] Endast konton. Valfria) Eventuella parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information. innehåller alla parametrar som företaget måste spåra. Exempel:`param1=value1&param2=value2`

I konton där konverteringsspårning för annonsering i Adobe används måste suffixet innehålla annonsnätverkets klickidentifierare (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]).

Konton med en Adobe Analytics-integrering måste använda parametern s_kwcid. Om kontot har en s_kwcid-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. annars måste du lägga till den manuellt här. Se [obligatoriska suffixformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Det här fältet uppdateras inte av [!UICONTROL Auto Upload] spårningsinställning.
>* Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter behövs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

