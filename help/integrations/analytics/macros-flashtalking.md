---
title: Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar
description: Lär dig varför och hur du lägger till [!DNL Analytics for Advertising] makron till [!DNL Flashtalking] annonstaggar
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: c7821f112757f695a6ab9da1fffb014b822e1ff3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

*Gäller endast DSP*

Om du använder annonstaggar från [!DNL Flashtalking] för era annonser DSP annonser, lägga till parametrar för annonsering i era URL:er för landningssidor. Parameterposten för AMO-ID (`s_kwcid`) och `ef_id` frågesträngsparametrar i landningssidans URL, vilket gör att Adobe Advertising kan skicka klickdata för annonserna till Adobe Analytics.

Använd makron för [!DNL Flashtalking] webbannonser och videoannonser för följande typer av [!DNL Analytics for Advertising] implementeringar:

* **Annonsörer med [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript-kod som implementeras på deras webbplatser**: JavaScript-koden registrerar redan AMO-ID:t (`s_kwcid`) och `ef_id` frågesträngparametrar. Om du använder makron utökas dock spårningen så att den omfattar klickbaserade konverteringar när cookies från tredje part inte stöds. Det bästa sättet är att lägga till makron i följande avsnitt i dina annonstaggar för att hämta ytterligare klickdata som inte fångas in via JavaScript-koden.

>[!NOTE]
>
>JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När cookies har upphört måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder [!DNL Analytics for Advertising] JavaScript-kod och förlita dig istället på [!DNL Analytics] vidarebefordran på serversidan endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickningsaktiviteter på plats som är kopplade till annonser som du köper via Adobe Advertising.

## Visa annonstaggar

I [!DNL Flashtalking] lägg till följande makro i slutet av klicknings-URL:en i `Clicktag` fält:

```
[ftqs:[AdobeAMO]]
```

Om det är den första eller enda frågesträngen efter bas-URL:en separerar du den från bas-URL:en med en `?`. Om bas-URL:en innehåller flera frågesträngar börjar du den första strängen med en `?` och varje efterföljande sträng med en `&`.

Exempel:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video Ad-taggar

I [!DNL Flashtalking] lägg till följande makro i slutet av klicknings-URL:en i `Clicktag` fält:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Om det är den första eller enda frågesträngen efter bas-URL:en separerar du den från bas-URL:en med en `?`. Om bas-URL:en innehåller flera frågesträngar börjar du den första strängen med en `?` och varje efterföljande sträng med en `&`.

Exempel:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md)

