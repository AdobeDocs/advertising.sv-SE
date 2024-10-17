---
title: Om och nätverkskonton
description: Läs om annonsnätverkskonton i Search, Social och Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Om och nätverkskonton

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Search, Social och Commerce kan spåra alla annonsörer i annonsnätverk som stöds. Om du vill aktivera spårning av ett konto måste du skapa en motsvarande kontopost. Du måste konfigurera kontoinformation för alla typer av konton, oavsett om Sök, Sociala och Commerce synkroniserar med det eller optimerar bud och budgetar för annonserna.

## Konton som har synkroniserats via API:er

*[!DNL Google Ads], [!DNL Microsoft Advertising] (tidigare [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] och befintliga [!DNL Baidu]-konton*

Sökning, socialt arbete och Commerce synkroniserar (*synkroniserar*) med annonsnätverkskonton som stöds så att du kan spåra, rapportera om och visualisera prestanda för annonserna. För alla annonsnätverk utom [!DNL Yahoo! Display Network] kan du hantera kampanjer för ditt konto i Sök, Socialt och Commerce. [!DNL Yahoo! Display Network], kampanjer är skrivskyddade. För alla annonsnätverk kan ni tillåta optimeringsmöjligheterna att optimera anbud, kampanjbudgetar och kampanjanbudsstrategier för kampanjer i hanterade konton genom att lägga till kampanjer i portföljer.

Om du vill aktivera synkronisering av ett konto måste kontoposten innehålla autentiseringsuppgifter för kontoåtkomst och vara aktiverad (aktiv).

Under synkroniseringen hämtar Search, Social och Commerce annonsörens kampanjstrukturer och kampanjentiteter som stöds, inklusive de flesta attribut som hanteras eller rapporteras i Search, Social och Commerce. Det omfattar inte klickdata, och inte heller bud och budmodifierare som anges utanför Search, Social och Commerce, som samlas in separat. Search, Social och Commerce synkroniserar automatiskt med annonsnätverkskonton en gång om dagen, och även när det upptäcker en ny kampanj i något av dina annonsnätverk. Dessutom skickas omedelbart alla ändringar av kampanjdata från Search, Social och Commerce till annonsnätverket. Du kan begära manuell synkronisering när det behövs.

Mer information om hur du skapar och redigerar synkroniserade kampanjer finns i kapitlet&quot;Campaign Management&quot;.

## Konton som bara är för uppföljning

*[!DNL Naver]konton*

Med spårningskampanjer kan ni spåra, rapportera om och visualisera resultatet för annonser som ni köper direkt från annonsnätverket. Search, Social, &amp; Commerce synkroniserar inte data med annonsnätverket, lägger bud för kontot eller tillhandahåller ingen typ av optimering eller simuleringar.

Om du vill att konverteringar ska kunna attributeras till klickningar i Search, Social och Commerce anger du spårningsalternativ i kontoposten och aktiverar kontoposten. Du kan sedan använda kalkylblad för att generera spårnings-URL:er för dina annonser och nyckelord, och manuellt lägga till spårnings-URL:er i annonshanteraren [!DNL Naver].

Mer information om [!DNL Naver] kampanjer med endast spårning finns i [Implementera [!DNL Naver] konton med endast spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Hantera annonskonton](ad-network-account-manage.md)
>* [Hantera handlarcenterkonton](merchant-account-manage.md)
>* [Uppdatera spårningskoden för AMO-ID för ett [!DNL Google Ads] konto](update-amo-id-google.md)
