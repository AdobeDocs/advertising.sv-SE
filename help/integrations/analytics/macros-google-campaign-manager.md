---
title: Lägg till  [!DNL Analytics for Advertising] makron i  [!DNL Google Campaign Manager 360] Lägg till taggar
description: Lär dig varför och hur du lägger till  [!DNL Analytics for Advertising] makron i dina  [!DNL Google Campaign Manager 360] ad-taggar
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising] makron i [!DNL Google Campaign Manager 360]-märkord

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*Gäller endast Advertising DSP*

Om du använder annonstaggar från [!DNL Google Campaign Manager 360] för dina Advertising DSP-annonser lägger du till [!DNL Analytics for Advertising]-parametrar till dina startsidans URL:er med hjälp av [`%p`-makrot &#x200B;](https://support.google.com/campaignmanager/table/6096962). Parametrarna innehåller parametrarna AMO ID (`s_kwcid`) och `ef_id` frågesträngsparametrar i landningssidans URL, vilket gör att Adobe Advertising kan skicka klickdata för annonserna till Adobe Analytics.

Använd makron för [!DNL Campaign Manager 360]-visning och videoannonser för följande typer av [!DNL Analytics for Advertising]-implementeringar:

* **Annonsörer med JavaScript-koden [!DNL Adobe] [!DNL Analytics for Advertising] implementerad på deras webbplatser**: JavaScript-koden registrerar redan parametrarna för AMO-ID (`s_kwcid`) och `ef_id` frågesträngar. Om du använder makron utökas dock spårningen så att den omfattar klickbaserade konverteringar när cookies från tredje part inte stöds. Det bästa sättet är att lägga till makron i följande avsnitt i dina annonstaggar för att hämta ytterligare klickdata som inte fångas in via JavaScript-koden.

>[!NOTE]
>
>JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När cookies har upphört måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder JavaScript-koden [!DNL Analytics for Advertising] och i stället förlitar sig på vidarebefordran på [!DNL Analytics] endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickaktivitet på webbplatsen från annonser som du köper via Adobe Advertising.

## Lägg till makron i dina [!DNL Google Campaign Manager 360]-annonser

Inom [!DNL Google Campaign Manager 360] lägger du till följande parameter till landningssidans URL för var och en av dina annonser för visning och video: `%pamo=!;`

Du kan ange landningssidans URL på flera sätt. Instruktioner för varje alternativ finns i följande underavsnitt.

Följande är ett exempel på landningssidans URL-adress formaterad med suffixet.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Om landningssidans URL innehåller en hash-symbol (#), som inte är vanlig, placerar du parametern `amo` före hash-symbolen.
>* Om inga andra parametrar inkluderas efter parametern `amo` lägger du till en parameter (till exempel &amp;a=b) efter den. Exempel: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Konfigurera URL-suffixet för marknadsföringsnivålandningssida

1. Se [instruktionerna för att öppna annonsörsegenskaperna](https://support.google.com/campaignmanager/answer/2829344).
1. Inkludera `%pamo!;` i fältet [!UICONTROL URL suffix] i inställningarna för [!UICONTROL Landing page URL suffix].

### Konfigurera URL-suffixet för landningssida på kampanjnivå

1. Se [instruktionerna för att öppna kampanjegenskaperna](https://support.google.com/campaignmanager/answer/2838056#set).
1. Inkludera `%pamo!;` i fältet [!UICONTROL URL suffix] i inställningarna för [!UICONTROL Landing page URL suffix].

### Konfigurera URL-suffixet för landningssida på Creative-nivå

1. Öppna de kreativa egenskaperna.
1. Inkludera `%pamo!;` i kolumnen [!UICONTROL Landing page] för click-taggen i inställningen [!UICONTROL Click tags].

## Hur [!DNL Analytics for Advertising] makron utökas i DSP

När du skapar en annons som innehåller parametern [!DNL Analytics for Advertising] (`amo`) i DSP läggs makrona `ef_id` och `s_kwcid` automatiskt till i klicknings-URL:en. Det bästa sättet är att checka in DSP för att se till att makrona `ef_id` och `s_kwcid` finns.

Följande är ett exempel på en [!DNL Google Campaign Manager 360] [ins-tagg](https://support.google.com/campaignmanager/answer/6080468) så som den visas i DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

När en användare klickar på annonsen ser [!DNL Google Campaign Manager 360] `%pamo` i URL-suffixet och infogar dynamiskt värdet för parametern `amo` i URL:en.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Lägg till [!DNL Analytics for Advertising] makron i [!DNL Flashtalking] Lägg till taggar](macros-flashtalking.md)
