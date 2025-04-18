---
title: Om annonshantering i Advertising DSP
description: Läs mer om annonshantering.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Om annonshantering i Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP har stöd för annonsleverans via tredjepartstaggar för annonsvisning (som Google, Flashtalk eller Sizmek) för olika annonstyper och direkt medieöverföring för inbyggda displayannonser. Du kan överföra tredjepartstaggar individuellt eller gruppvis. Överföringar gruppvis använder partnertaggmallar eller en mall för grupptaggar.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

När era annonser har konfigurerats kan ni bifoga varje annons till en eller flera annonser, som innehåller målinriktningsparametrar (som geo, målgrupp, enhet och målinriktning mot lager) som styr hur kampanjen levererar. Du måste bifoga en annons till en plats för att kunna börja köra annonsen.

## Tillgängliga annonstyper {#ad-types}

Alla följande annonstyper är tillgängliga i DSP. Fullständiga specifikationer för varje annonstyp finns i [annonsspecifikationerna](ad-specs.md).

* **Ljudannonser (endast från tredje part)**: Ljudannonser spelas upp mellan innehåll på digitala utgivarwebbplatser och kan köras fristående som ljudfiler eller tillsammans med pekskärmsannonser. Ljud används bäst för att öka varumärkeskännedomen och engagera en publik på språng. Viktiga prestandaindikatorer för ljud är [!UICONTROL Completion Rate] och [!UICONTROL Cost per Completion].

* **Visningsannonser (endast från tredje part)**: Visningsannonser är animerade eller statiska bilder som visas i webbläsare eller i appar. När du klickar på annonsenheten tar det användaren till en varumärkesanpassad plats eller mikroplats. Skärmen är bäst att använda för att driva effektiva CPM-annonser, öka e-postkopplingen, lägga till fler varumärkes- eller produktkontaktytor och få användarna att stanna längre. Viktiga prestandaindikatorer för visning är [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] och [!UICONTROL Cost per Conversion]. DSP har stöd för en mängd olika annonsstorlekar för visningsbanderoller.

* **Mobilannonser (endast från tredje part)**: Mobilannonser kan finnas i förrullningsvideo (VAST, MRAID) eller standardvisningsformat. Mobil pre-roll-video kan spelas upp automatiskt eller spelas upp klick för uppspelning och är bäst för att nå tittare på olika skärmar. Visning av mobilstandard är en statisk bild som visas i webbläsare eller i appar för mobila enheter och är bäst att använda för att komplettera köp av digital video, skapa en meddelandeassociation och lägga till ytterligare varumärke eller produktkontaktytor. Mobilannonser kan också fungera som helskärmsannonser eller som mobilinterstitialer, som är högeffektiva mobilannonser i helskärmsläge som är bäst för att utveckla varumärkeskännedom för mobiler och driva konverteringar.

* **Inbyggda visningsannonser (endast för första part)**: Inbyggda annonser stöds i standardvisningsformat. Interna annonser innehåller en rubrik och/eller titel, beskrivning, logotyp och bild. Annonselementen kombineras och återges så att de matchar utgivarens sidstil, så att annonsen blandas in med utgivarens organiska innehåll och skapar ett större engagemang. Det inbyggda formatet används bäst för att öka varumärkeskännedomen och öka läsarnas exponering och engagemang med visningsvänlig reklam. Nyckeltal för prestandaindikatorer är [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] och [!UICONTROL Cost Per Conversion].

* **Pre-roll Ads (endast från tredje part)**: Pre-roll-ads (VAST och VPAID) visas före Premium-videomaterial och ger en engagerande tittarupplevelse. Videor före filmningen kan vara interaktiva, innehålla multimediefunktioner och innehålla övertäckningar, överrullningar och actionanrop. Viktiga prestandaindikatorer för videoannonser före rullning är [!UICONTROL Video Completion Rate] och [!UICONTROL Viewability Rate].

* **Anslutna TV-annonser (endast från tredje part)**: Anslutna TV-annonser visas före och under premium-TV-videomaterial. Alla anslutna TV-inventeringar körs på tv-enheter, vilket innebär att videon spelas upp automatiskt i en återgivningsmiljö i helskärmsläge som tittarna inte kan hoppa över. Uppkopplad TV är det närmaste digitala videoformatet för TV-reklamen. Nyckeltal för prestandaindikatorer för ansluten TV är [!UICONTROL Completion Rate].

* **Universal Video Ads (endast från tredje part)**: Med Universal Video Adds kan du rikta in videolagret från stationära, mobila och anslutna TV-miljöer för VPAID- och VAST-inventering med en enda videoplacering. De kombinerar alla funktioner som finns i uppkopplad TV, pre-roll och mobil pre-roll-reklam och visas före och under videoinnehåll. Viktiga prestandaindikatorer för universell video är [!UICONTROL Completion Rate] och [!UICONTROL Viewability Rate].

  Universella videoannonser kan bara bifogas till universella videomaterial.

  Mer information om universella videoannonser finns i [Vanliga frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md).

## DSP annonsgodkännanden

När du skapar en annons DSP igenom den för att se om det finns känsliga kategorier, klickar på URL-funktionen och förhandsgranskar återgivningen.

Till att börja med visas en röd punkt i annonsens [!UICONTROL Status]-kolumn. Granskningsprocessen tar normalt 24-48 timmar. En trasig annons kan dock ha en väntande status i mer än 48 timmar, så du har tid att åtgärda fel innan annonsen refuseras. Avvisade annonser innehåller en orsak till refuseringen.

När DSP godkänner en annons visas en grön punkt i annonsens statuskolumn.

![godkännandeindikator i [!UICONTROL Status] kolumn ](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Din annons kan bara visas om både DSP och SSP har godkänt den kreativa processen. Varje enskild SSP har sina egna krav och processer för godkännande.

>[!MORELIKETHIS]
>
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Annonsspecifikationer](ad-specs.md)
