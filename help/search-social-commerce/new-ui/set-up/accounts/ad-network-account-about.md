---
title: (Nytt användargränssnitt) Om annonsnätverkskonton
description: Läs mer om annonsnätverkskonton i det nya gränssnittet Sök, Social och Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Nytt användargränssnitt) Om annonsnätverkskonton

Search, Social och Commerce kan spåra alla annonsörer i annonsnätverk som stöds. Om du vill aktivera spårning av ett konto måste du skapa en motsvarande kontopost. Du måste konfigurera kontoinformation för alla typer av konton, oavsett om Sök, Sociala och Commerce synkroniserar med det eller optimerar bud och budgetar för annonserna.

## Konton som har synkroniserats via API:er

*[!DNL Google Ads], [!DNL Microsoft Advertising] (tidigare [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] och befintliga [!DNL Baidu]-konton*

Sökning, socialt arbete och Commerce synkroniserar (*synkroniserar*) med annonsnätverkskonton som stöds så att du kan spåra, rapportera om och visualisera prestanda för annonserna. För alla annonsnätverk utom [!DNL Yahoo! Display Network] kan du hantera kampanjer för ditt konto i Sök, Socialt och Commerce. [!DNL Yahoo! Display Network], kampanjer är skrivskyddade. För alla annonsnätverk kan ni tillåta optimeringsmöjligheterna att optimera anbud, kampanjbudgetar och kampanjanbudsstrategier för kampanjer i hanterade konton genom att lägga till kampanjer i portföljer.

Om du vill aktivera synkronisering av ett konto måste kontoposten innehålla autentiseringsuppgifter för kontoåtkomst och vara aktiverad (aktiv).

Under synkroniseringen hämtar Search, Social och Commerce annonsörens kampanjstrukturer och kampanjentiteter som stöds, inklusive de flesta attribut som hanteras eller rapporteras i Search, Social och Commerce. Det omfattar inte klickdata, och inte heller bud och budmodifierare som anges utanför Search, Social och Commerce, som samlas in separat. Search, Social och Commerce synkroniserar automatiskt med annonsnätverkskonton en gång om dagen, och även när det upptäcker en ny kampanj i något av dina annonsnätverk. Dessutom skickas omedelbart alla ändringar av kampanjdata från Search, Social och Commerce till annonsnätverket. Du kan begära manuell synkronisering när det behövs.

Mer information om hur du skapar och redigerar synkroniserade kampanjer finns i kapitlet&quot;Kampanjhantering&quot;.

## Konton för vilka du överför data manuellt

För onlineannonsnätverk där Search, Social och Commerce inte tillhandahåller API-stöd kan du ladda upp kampanjinnehåll och offlinekostnader, klicka och konverteringsdata för ett konto för rapportering och prestandamuleringar. Search, Social och Commerce synkroniserar inte data med annonsnätverket, erbjuder automatiserad budgivning eller erbjuder någon typ av optimering, men ni kan effektivisera insikterna i olika kanaler och identifiera möjligheter till manuell optimering.

## Mallbaserade uppföljningskonton

*Endast tillgängligt för befintliga [!DNL Naver]-konton*

Med spårningskampanjer kan ni spåra, rapportera om och visualisera resultatet för annonser som ni köper direkt från annonsnätverket. Search, Social, &amp; Commerce synkroniserar inte data med annonsnätverket, erbjuder automatiserad budgivning eller erbjuder någon typ av optimering eller simuleringar.

Om du vill att konverteringar ska kunna attributeras till klickningar i Search, Social och Commerce anger du spårningsalternativ i kontoposten och aktiverar kontoposten. Du kan sedan använda kalkylblad för att generera spårnings-URL:er för dina annonser och nyckelord, och manuellt lägga till spårnings-URL:er i annonshanteraren [!DNL Naver].

Du kan inte konfigurera nya [!DNL Naver]-konton i Sök, Sociala och Commerce. Mer information om [!DNL Naver] kampanjer med endast spårning finns i [Implementera [!DNL Naver] konton med endast spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Hantera annonskonton via API-anslutning](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Hantera och nätverkskonton för dataöverföringar](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Hantera [!DNL Naver] konton för enbart spårning](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implementera [!DNL Naver] konton med endast spårning](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Hantera handlarcenterkonton](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
