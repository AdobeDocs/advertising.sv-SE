---
title: Frågor och svar om spårning
description: Lär dig svar på vanliga frågor om spårning, inklusive felsökning.
exl-id: f559b977-dd44-4d29-b49e-c41c6fb783d1
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Frågor och svar om spårning

## Spårningsfunktioner

+++Kan jag spåra kampanjer som Adobe Advertising inte klarar?

Ja. Om Search, Social, &amp; Commerce synkroniserar ett av dina annonsnätverkskonton spåras annonsnätverkets klickdata för alla [kampanjtyper](/help/search-social-commerce/introduction/supported-inventory.md) på det kontot. Konverteringsdata spåras även om du har lagt till omdirigeringen Sök, Socialt och Commerce till dina annons- och/eller nyckelordsmål-URL:er eller spårningsmallar och implementerat konverteringsspårning på konverteringssidorna. Förtydliga med ert Adobe Account Team vilka kampanjer ni vill att Search, Social och Commerce ska spåra och vilka ni vill att de ska hantera.
+++

+++Hur får jag attribuering vid flera händelser?

För annonsörer som använder taggarna Sök, Socialt, &amp; Commerce eller Adobe Analytics konverteringsspårning finns det flera alternativ i Adobe Advertising för att tilldela konverteringsdata för en serie händelser som leder till konvertering. En inställning på annonsörnivå avgör hur konverteringsdata ska tilldelas i olika händelser, även när de inträffar i flera annonskanaler, så länge som kanalerna tillåter uppföljning på händelsenivå. Som standard tilldelas konverteringar till den senaste (senaste) händelsen, men inställningen kan konfigureras på ett annat sätt, t.ex. för att attribuera konverteringar till den första händelsen eller för att väga alla händelser jämnt. Om du ändrar attribueringsregeln påverkas hur framtida bud beräknas.

Annonsörer som tillhandahåller alla konverteringsdata i en feed-fil måste själva attribuera konverteringen till de relaterade transaktionshändelserna.

>[!NOTE]
>
>I vyer för kampanjhantering och portföljhantering, rapporter och (tillgängliga för vissa användare) anpassade simuleringar kan du ändra regeln som används för att attributera konverteringsdata i vyerna och rapportresultaten, utan att det påverkar hur framtida offerter beräknas.

+++

+++Hur identifierar Adobe Advertising dubbletttransaktioner?

Dubblerade transaktioner kan inträffa när en användare uppdaterar bekräftelsesidan efter att ha slutfört en transaktion. Adobe Advertising använder `ev_transid` för att ta bort dubbletttransaktioner med samma transaktions-ID och egenskapsvärde.

Följande är Adobe Advertising-dupliceringslogik:

* **När en kund skickar ett värde för `ev_transid` attribute:** Efterföljande pixelbegäranden betraktas som dubbletter av det föregående om följande är desamma: `ev_transid`; spårnings-ID för samma nyckelord, annons eller placering samt värdet för en viss transaktionsegenskap.

  Om flera låneansökningar till exempel har samma program-ID och lånebelopp för samma nyckelord i ett visst annonsnätverk betraktas de som dubbletter och endast den första låneansökan räknas.

* **När en klient inte skickar något värde för `ev_transid` attribute:** Efterföljande transaktioner betraktas som dubbletter av det föregående om de delar ett spårnings-ID för samma nyckelord, annons eller placering, och samma värde för en viss transaktionsegenskap.

  Om flera låneansökningar till exempel har samma nyckelord-ID och lånebelopp betraktas de som dubbletter och endast den första låneansökan räknas.
+++

## Typer av spårningsimplementering

+++Jag vill sluta använda tjänsten för spårning av konvertering i Adobe Advertising för en eller flera kampanjer eller konton. Hur tar jag snabbt bort spårningskoden från spårnings-URL:erna?

Ta först kontakt med ditt Adobe-kontoteam för att ta reda på vad det innebär att ta bort spårnings-URL:er.

I kontot eller kampanjen ändrar du spårningsmetoden till[!UICONTROL No EF Redirect].&quot; Skapa sedan ett kalkylblad med[!UICONTROL Generate Tracking URLs]och lägga in det i annonsnätverket. Alla befintliga spårnings-URL:er eller mål-URL:er ersätts.
+++

## Datafrågor

+++Hur vet jag vilken transaktionsegenskap som kommer från en datafeed eller spåras av taggen för spårning av konvertering i Adobe Advertising?

I en [!UICONTROL Transaction Report]kan du se om en inkluderad transaktionsegenskap spårades av Adobe Advertising-konverteringsspårningspunkten om du inkluderar den anpassade kolumnen &quot;[!UICONTROL Tracking URL].&quot; Spårnings-URL:er med spårningspixeln Adobe Advertising börjar med `http://pixel.everesttech.net`.
+++

+++Vad är överblivna transaktioner?

Enstaka transaktioner är transaktionshändelser som inte kan kopplas till ett specifikt nyckelord eller en viss annons. Adobe Advertising lägger in transaktioner/intäkter i ett nyckelord eller en annons genom att matcha de spårnings-ID som tagits emot med intäktshändelsen med det unika spårnings-ID som finns i nyckelordets eller annonsens spårnings-URL.

När en kontogrupp på Adobe misstänker att det är obehöriga som kan få skulden för en intäktsminskning, söker kundtjänstteamet efter horungar och undersöker, om sådana finns, problemet.

Orphans förekommer i följande situationer.

**Pixelimplementeringar**

Enstaka transaktioner inträffar nästan aldrig för pixelimplementeringar. Pixelhorungar har dock inträffat när:

* Klickdata är inte tillgängliga för konverteringens klickdatum. I det här fallet mappas data tillbaka när sökdata, sociala data och e-handel hämtar klickdata från annonsnätverket.

* Klickloggarna bearbetas inte före konverteringsloggarna.

**Implementeringar av flöden**

* Spårnings-ID:t som skickas i feeden kommer från ett konto som inte är känt i Search, Social och Commerce.

* Kontot är inte synkroniserat eller så uppstod fel under synkroniseringsprocessen.

* Spårnings-ID lades till och togs bort från annonsnätverket medan Sök, Socialt och Commerce var osynkroniserat med annonsnätverket, så Search, Social och Commerce har ingen information om ID:t. Detta problem fortsätter att förorsaka ägarlösa intäkter om det uppstår en fördröjning i intäkten.

* Klienten skickade ett spårnings-ID som är felaktigt formaterat i feeden och som inte matchar spårnings-ID:t i URL:en. Detta inträffar vanligtvis på grund av ett formateringsproblem eller när spårnings-ID:n förkortas i feeden.

* I konfigurationsfilen är det reguljära uttryck som används för att extrahera spårnings-ID:t från URL:erna felaktigt eller inaktuellt. Ibland ändrar annonsören spårnings-ID i URL:en eller antar ett helt nytt spårningssystem, vilket kräver att implementeringsteamet för sökning, sociala medier och handel uppdaterar det reguljära uttrycket. I sådana fall är en stor del av intäkterna överblivna.

**Flödesimplementeringar med ett transaktions-ID**

Det finns inga onlinetransaktioner tillgängliga före de datum för vilka data är tillgängliga i offlineflödet.

**Feed-implementeringar med en token (ef_id)**

Det går inte att hitta en motsvarande klickning på servern eller i annonsnätverket. Detta kan bero på att klickdata inte är tillgängliga för konverteringens klickdatum eller (sällan) på att klickloggarna inte bearbetades före konverteringsloggarna. När klickdata tas emot från annonsnätverket eller klickloggarna bearbetas, mappas data till konverteringen.
+++

## Problem med intäktsspårning

+++Hur korrigerar jag gamla/felaktiga data från en feed-fil?

Kontakta kundtjänst med den korrigerade datafilen.
+++

+++Flera nyckelord har samma spårnings-URL.

**Konsekvenser**

För flödesimplementeringar med flera spårnings-ID rapporteras data mot flera nyckelord. För andra implementeringar kan konverteringar tillskrivas fel nyckelord eftersom systemet tilldelar en konvertering godtyckligt till ett av nyckelorden.

**Möjlig orsak**

URL:en för ett nytt nyckelord eller en ny annons kopierades från ett annat nyckelord eller en annons.

Detta bör inte ske med displayannonsering eller social annonsering.

**Möjlig lösning eller tillfällig lösning**

* Om du hanterar dina egna nyckelord och annonser skapar du en kalkylbladsfil med rätt URL:er för de duplicerade URL:erna och publicerar den till rätt konto med hjälp av **[!UICONTROL Generate Tracking URLs]** som återskapar URL:er för alla nyckelord och annonser.

* Om ett Adobe-kontoteam hanterar dina nyckelord ber du dem skapa nya URL:er för de duplicerade URL:erna.
+++
