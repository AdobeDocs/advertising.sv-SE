---
title: Om och nätverkskonton
description: Läs mer om annonsnätverkskonton i Sök, Socialt och Handel.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Om och nätverkskonton

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Sökning, sociala medier och handel kan spåra ett annonsörs konton i annonsnätverk som stöds. Om du vill aktivera spårning av ett konto måste du skapa en motsvarande kontopost. Du måste konfigurera kontoinformation för alla typer av konton, oavsett om Sök, Sociala och Commerce synkroniserar med det eller optimerar bud och budgetar för annonserna.

## Konton som har synkroniserats via API:er

*[!DNL Google Ads], [!DNL Microsoft Advertising] (tidigare [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex]och befintlig [!DNL Baidu] konton*

Synkronisering av sökning, sociala medier och handel (*synk*) med annonsnätverkskonton som stöds så att ni kan spåra, rapportera om och visualisera resultatet för annonserna. För alla annonsnätverk utom [!DNL Yahoo! Display Network]kan du hantera kampanjer för ditt konto i Sök, Socialt och Commerce, om du vill. [!DNL Yahoo! Display Network], är kampanjer skrivskyddade. För alla annonsnätverk kan ni tillåta optimeringsmöjligheterna att optimera annonser i hanterade konton genom att lägga till dem i portföljer.

Om du vill aktivera synkronisering av ett konto måste kontoposten innehålla autentiseringsuppgifter för kontoåtkomst och vara aktiverad (aktiv).

Under synkroniseringen hämtar Search, Social och Commerce annonsörens kampanjstrukturer och kampanjentiteter som stöds, inklusive de flesta av deras attribut som hanteras eller rapporteras i Sök, Socialt och Commerce. Det omfattar inte klickdata, och inte heller bud och budmodifierare som anges utanför Sök, Social och Commerce, som samlas in separat. Search, Social, &amp; Commerce synkroniserar automatiskt med annonsnätverkskonton en gång om dagen, och även när det upptäcker en ny kampanj i något av dina annonsnätverk. Dessutom skickas omedelbart alla ändringar av kampanjdata som gjorts i Search, Social och Commerce till annonsnätverket. Du kan begära manuell synkronisering när det behövs.

Mer information om hur du skapar och redigerar synkroniserade kampanjer finns i kapitlet&quot;Campaign Management&quot;.

## Konton som bara är för uppföljning

*[!DNL Naver]Konton*

Med spårningskampanjer kan ni spåra, rapportera om och visualisera resultatet för annonser som ni köper direkt från annonsnätverket. Sökning, sociala medier och handel synkroniserar inte data med annonsnätverket, lägger bud för kontot eller tillhandahåller ingen typ av optimering eller simuleringar.

Om du vill att konverteringar ska kunna attributeras till klickningar i Sök, Socialt och Commerce ställer du in spårningsalternativ i kontoposten och aktiverar kontoposten. Du kan sedan använda kalkylblad för att generera spårnings-URL:er för dina annonser och nyckelord, och manuellt lägga till spårnings-URL:er i dialogrutan [!DNL Naver] annonsansvarig.

Mer information om [!DNL Naver] spåra kampanjer endast, se&quot;[Implementera [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Hantera och nätverkskonton](ad-network-account-manage.md)
>* [Hantera säljcenterkonton](merchant-account-manage.md)
>* [Uppdatera spårningskoden för AMO ID för en [!DNL Google Ads] konto](update-amo-id-google.md)
