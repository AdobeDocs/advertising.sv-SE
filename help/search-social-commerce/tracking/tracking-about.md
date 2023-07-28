---
title: Om spårning för sökning, sociala medier och handel
description: Läs om spårningsalternativ för sökning, sociala medier och handel.
exl-id: 0a26f67c-8b3b-4fa1-ac24-a8461624cfc5
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Om spårning för sökning, sociala medier och handel

För att spåra hur era annonser fungerar behöver du bara klicka, klicka, koda och konvertera (transaktion) data för dina annonser. Search, Social, &amp; Commerce använder dessa data för att skapa de dataprognosmodeller som behövs för att optimera era era annonsportföljer.

## Kostnads-, klicknings- och visningsdata

Sökning, sociala medier och handel hämtar bild-, klicknings- och kostnadsdata direkt från [stödda annonsnätverk](/help/search-social-commerce/introduction/supported-inventory.md) varje dag. Dessutom kan du lägga till en unik klickspårningskod (inklusive en omdirigering till en spårningsserver) i spårningsmallar och mål-URL:er för att spåra visningar, klickningar och kostnader för displayen/innehållet och senare knyta händelserna till konverteringar.

Om du vill spåra kampanjer i annonsnätverk som inte synkroniserar data med Search, Social och Commerce måste du tillhandahålla data för dessa kampanjer genom att skicka en daglig feed-fil med intryck, klickning och kostnadsdata.

### Klickspårningstaggar

Ert implementeringsteam för sökning, sociala medier och handel ställer in klickspårning genom att uppdatera spårningsmallarna och mål-URL:erna för annonser, nyckelord, placeringar, produktgrupper och sitelink-tillägg i era synkroniserade annonskampanjer, så att de innehåller en unik spårnings-ID-sträng och en omdirigering från Adobe Advertising. De lägger även till spårning i landsidessuffixen (sista URL-suffix) för dina [!DNL Google Ads] och [!DNL Microsoft Advertising] konton och kampanjer.

Spårningsparametrarna gör det möjligt för Adobe Advertising att spåra klick på en enskild nyckelordsnivå (sökkampanjer) eller annonsvariationsnivå (sökkampanjer med innehåll eller webbplatsanpassning, webbkampanjer och sociala kampanjer). Varje gång en användare tittar på en skärm/ett innehåll och klickar på någon av dina annonser, skickar annonsnätverket händelsen till Adobe Advertising-pixelservrarna med en klickspårningstagg som är kopplad till nyckelordet eller annonsen. För klickningar:

* För annonser i Google Ads och Microsoft Advertising i webbläsare som stöder parallell spårning skickar annonsnätverket klicket först till din webbplats och sedan till pixelservrarna i Adobe Advertising, som sedan placerar en cookie på användarens dator, om det inte redan finns en.

* I alla andra fall skickar annonsnätverket klickljudet direkt till Adobe Advertising-pixelservrarna. Pixelservern placerar en cookie på användarens dator (om det inte finns någon) och dirigerar sedan om användaren till den relevanta URL:en på webbplatsen. Den övergripande upplevelsen för slutanvändaren är densamma som den skulle vara utan en omdirigering.

Kakan anges i [!DNL Adobe] domän (`everesttech.net`) som en cookie från första part. Efter en omdirigering finns användaren i annonsörens domän, och cookien behandlas sedan som en cookie från tredje part. Mer information om Adobe Advertising-cookies finns i &quot;[Adobe Advertising cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Konverteringsdata

När en kund klickar på en annons eller visar en displayannonsering eller social annonsering måste sökningen, sociala medier och handel mappa varje konvertering tillbaka till det ursprungliga klicket eller den inledande displayen/det sociala intrycket.

Annonsören spelar en roll när det gäller att tillhandahålla konverteringsdata för alla klick och visningar/sociala visningar. Konverteringsdata kan innehålla information om alla typer av händelser på en webbplats som kan användas för anbudsoptimering. Du kan tillhandahålla konverteringsdata genom att implementera konverteringsspårningskoden på annonsörens konverteringssidor (till exempel den framgångssida som visas när en kund har slutfört en transaktion) eller genom att skicka en daglig feed-fil med konverteringsdata som hämtats med en annan metod.

### Taggar för konverteringsspårning

Du kan använda [konverteringstaggar från olika leverantörer](/help/search-social-commerce/tracking/conversion-tracking-about.md).

När du använder en konverteringstagg i Adobe Advertising och en användare slutför en lyckad transaktion och går till en sida där det lyckades, söker pixelservern i Adobe Advertising efter cookie-filen på användarens dator, som angavs när klickomdirigeringen gjordes. När en cookie hittas skickas information om transaktionshändelsen med parametern ef_transid, och transaktionen identifieras som en konvertering och krediteras med föregående annons-klick eller visningsintryck.

Om användaren klickade på mer än en av dina annonser, krediterar Adobe Advertising transaktionen till den sista annonsklickningen eller (för webbkampanjer eller videokampanjer) det sista annonsintrycket om du inte anger något annat. Dina [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j) bestämmer hur många dagar efter en betald klickning eller ett visnings-/videointryck (respektive) som händelsen kan tilldelas till en konvertering.

Adobe Advertising-implementeringsteamet arbetar tillsammans med annonsören för att fastställa formatet för de konverteringstaggar annonsören behöver implementera, identifiera de webbsidor där varje konverteringstagg ska infogas och ange sedan de konverteringstaggar som ska implementeras.
