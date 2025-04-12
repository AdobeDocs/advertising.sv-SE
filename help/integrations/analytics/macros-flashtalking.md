---
title: Lägg till  [!DNL Analytics for Advertising] makron i  [!DNL Flashtalking] Lägg till taggar
description: Lär dig varför och hur du lägger till  [!DNL Analytics for Advertising] makron i dina  [!DNL Flashtalking] ad-taggar
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 181a22c83b77dabbd949d9e47d0a7cadf1e68c18
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising] makron i [!DNL Flashtalking]-märkord

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

*Organisationer utan direktkoppling med [!DNL Flashtalking] endast*

*Gäller endast Advertising DSP*

Om du använder annonstaggar från [!DNL Flashtalking] för dina Advertising DSP-annonser måste du lägga till spårningsparametrar i URL:er för landningssidan. Om du vill använda Advertising DSP-partnerskapet med [!DNL Flashtalking] lägger du till parametrar för Advertising i dina URL:er för landningssidan. Parametrarna registrerar AMO ID (`s_kwcid`) och `ef_id` frågesträngsparametrar i landningssidans URL, vilket gör att Adobe Advertising kan skicka klickdata för annonserna till Adobe Analytics.

>[!NOTE]
>
>Om din organisation har ett direktsamarbete med [!DNL Flashtalking] är den här proceduren inte nödvändig för dig. Logga i stället in på ditt [!DNL Flashtalking]-konto och följ [!DNL Flashtalking]-supportdokumentationen för att samla in klickdata med hjälp av datappassmakron på `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Använd makron för [!DNL Flashtalking]-visning och videoannonser för följande typer av [!DNL Analytics for Advertising]-implementeringar:

* **Annonsörer med JavaScript-koden [!DNL Adobe] [!DNL Analytics for Advertising] implementerad på deras webbplatser**: JavaScript-koden registrerar redan parametrarna för AMO-ID (`s_kwcid`) och `ef_id` frågesträngar. Om du använder makron utökas dock spårningen så att den omfattar klickbaserade konverteringar när cookies från tredje part inte stöds. Det bästa sättet är att lägga till makron i följande avsnitt i dina annonstaggar för att hämta ytterligare klickdata som inte fångas in via JavaScript-koden.

  >[!NOTE]
  >
  >JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När cookies har upphört måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder JavaScript-koden [!DNL Analytics for Advertising] och i stället förlitar sig på vidarebefordran på [!DNL Analytics] endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickningsaktiviteter på webbplatsen som styrs av annonser som du köper via Adobe Advertising.

## Visa annonstaggar

Lägg till följande makro i slutet av klicknings-URL:en i fältet `Clicktag` i inställningarna för annonstaggen [!DNL Flashtalking]:

```
[ftqs:[AdobeAMO]]
```

Om det är den första eller enda frågesträngen efter bas-URL:en separerar du den från bas-URL:en med `?`. Om bas-URL:en innehåller flera frågesträngar börjar du den första strängen med en `?` och varje efterföljande sträng med en `&`.

Exempel:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video Ad-taggar

Lägg till följande makro i slutet av klicknings-URL:en i fältet `Clicktag` i inställningarna för annonstaggen [!DNL Flashtalking]:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Om det är den första eller enda frågesträngen efter bas-URL:en separerar du den från bas-URL:en med `?`. Om bas-URL:en innehåller flera frågesträngar börjar du den första strängen med en `?` och varje efterföljande sträng med en `&`.

Exempel:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Lägg till [!DNL Analytics for Advertising] makron i [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md)

