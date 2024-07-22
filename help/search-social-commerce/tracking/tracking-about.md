---
title: Om spårning för sökningar, sociala medier och Commerce
description: Läs om spårningsalternativ för Sök, Socialt och Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Om spårning för sökningar, sociala medier och Commerce

Om du vill spåra hur annonserna fungerar behöver du bara klicka på, koda och konvertera (transaktion) data för dina annonser i sökningen, sociala medier och Commerce. Search, Social och Commerce använder dessa data för att bygga de dataprognosmodeller som behövs för att optimera era era annonsportföljer.

## Kostnads-, klicknings- och visningsdata

Search, Social och Commerce hämtar bild-, klicknings- och kostnadsdata direkt från [stödda annonsnätverk](/help/search-social-commerce/introduction/supported-inventory.md) varje dag. Dessutom kan Search, Social och Commerce lägga till en unik klickspårningskod (inklusive en omdirigering till en spårningsserver) i spårningsmallarna och mål-URL:er för att spåra visningar, klickningar och kostnader och senare knyta händelserna till konverteringar.

Om du vill spåra kampanjer i annonsnätverk som inte synkroniseras med data från Search, Social och Commerce måste du tillhandahålla data för dessa kampanjer genom att skicka en daglig feed-fil med intryck, klick och kostnadsdata.

### Klickspårningstaggar

Ert implementeringsteam i Search, Social och Commerce ställer in klickspårning genom att uppdatera spårningsmallarna och mål-URL:erna för annonser, nyckelord, placeringar, produktgrupper och sitelink-tillägg i era synkade annonskampanjer så att de innehåller en unik spårnings-ID-sträng och en omdirigering av Adobe Advertising. De lägger även till spårning till landsidessuffix (slutliga URL-suffix) för dina [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton och kampanjer.

Spårningsparametrarna gör det möjligt för Adobe Advertising att spåra klick på en enskild nyckelordsnivå (sökkampanjer) eller annonsvariationsnivå (sökkampanjer med innehåll eller webbplatsanpassning, webbkampanjer och sociala kampanjer). Varje gång en användare tittar på en skärm/ett innehåll och klickar på någon av dina annonser, skickar annonsnätverket händelsen till Adobe Advertising-pixelservrarna med en klickspårningstagg som är kopplad till nyckelordet eller annonsen. För klickningar:

* För [!DNL Google Ads]- och [!DNL Microsoft Advertising]-annonser i webbläsare som stöder parallell spårning skickar annonsnätverket klickningen till webbplatsen först och sedan till Adobe Advertising-pixelservrarna, som sedan placerar en cookie på användarens dator, om det inte redan finns en.

* I alla andra fall skickar annonsnätverket klickljudet direkt till Adobe Advertising-pixelservrarna. Pixelservern placerar en cookie på användarens dator (om det inte finns någon) och dirigerar sedan om användaren till den relevanta URL:en på webbplatsen. Den övergripande upplevelsen för slutanvändaren är densamma som den skulle vara utan en omdirigering.

Cookien anges i domänen [!DNL Adobe] (`everesttech.net`) som en cookie från första part. Efter en omdirigering finns användaren i annonsörens domän, och cookien behandlas sedan som en cookie från tredje part. Mer information om Adobe Advertising-cookies finns i &quot;[Adobe Advertising cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html)&quot;.

## Konverteringsdata

När en kund klickar på en annons eller visar en displayannonsering eller en social annons måste sökningen, sociala medier och Commerce mappa varje konvertering tillbaka till det ursprungliga klicket eller displayen/det sociala intrycket.

Annonsören spelar en roll när det gäller att tillhandahålla konverteringsdata för alla klick och visningar/sociala visningar. Konverteringsdata kan innehålla information om alla typer av händelser på en webbplats som kan användas för anbudsoptimering. Du kan tillhandahålla konverteringsdata genom att implementera konverteringsspårningskoden på annonsörens konverteringssidor (till exempel den framgångssida som visas när en kund har slutfört en transaktion) eller genom att skicka en daglig feed-fil med konverteringsdata som hämtats med en annan metod.

### Taggar för konverteringsspårning

Du kan använda [konverteringstaggar från olika leverantörer](/help/search-social-commerce/tracking/conversion-tracking-about.md).

När du använder en konverteringstagg i Adobe Advertising och en användare slutför en lyckad transaktion och går till en sida där det lyckades, söker pixelservern i Adobe Advertising efter cookie-filen på användarens dator, som angavs när klickomdirigeringen gjordes. När en cookie hittas skickas information om transaktionshändelsen med parametern ef_transid, och transaktionen identifieras som en konvertering och krediteras med föregående annons-klick eller visningsintryck.

Om användaren klickade på mer än en av dina annonser, krediterar Adobe Advertising transaktionen till den sista annonsklickningen eller (för webbkampanjer eller videokampanjer) det sista annonsintrycket om du inte anger något annat. Fönstret för [klicksökning](/help/search-social-commerce/glossary.md#c-d) och [visningssökning](/help/search-social-commerce/glossary.md#i-j) avgör hur många dagar efter ett betalt klick eller ett visnings-/videouppslag (respektive) som händelsen kan tilldelas till en konvertering.

Adobe Advertising-implementeringsteamet arbetar tillsammans med annonsören för att fastställa formatet för de konverteringstaggar annonsören behöver implementera, identifiera de webbsidor där varje konverteringstagg ska infogas och ange sedan de konverteringstaggar som ska implementeras.
