---
title: Om annonshantering i DSP
description: Läs mer om annonshantering.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Om annonshantering i DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP har stöd för annonsleverans via tredjepartstaggar för annonsvisning (som Google, Flashtalk eller Sizmek) för olika annonstyper och direkt medieöverföring för inbyggda displayannonser. Du kan överföra tredjepartstaggar individuellt eller gruppvis. Överföringar gruppvis använder partnertaggmallar eller en mall för grupptaggar.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

När era annonser har konfigurerats kan ni bifoga varje annons till en placering, som innehåller målgruppsparametrar (som geo, målgrupp, enhet och målinriktning mot lager) som styr hur kampanjen levererar. Du kan bifoga en annons till en eller flera placeringar.

## Tillgängliga annonstyper {#ad-types}

Alla följande annonstyper är tillgängliga i DSP. Fullständiga specifikationer för varje annonstyp finns i [Annonsspecifikationer](ad-specs.md).

* **Ljudannonser (endast från tredje part)**: Ljudannonser spelas upp mellan innehåll på digitala utgivarwebbplatser och kan köras fristående som ljudfiler eller tillsammans med andra banners. Ljud används bäst för att öka varumärkeskännedomen och engagera en publik på språng. Viktiga prestandaindikatorer för ljud är bland annat [!UICONTROL Completion Rate] och [!UICONTROL Cost per Completion].

* **Visa annonser (endast från tredje part)**: Visningsannonser är animerade eller statiska bilder som visas i webbläsare eller i appar. När du klickar på annonsenheten tar det användaren till en varumärkesanpassad plats eller mikroplats. Skärmen är bäst att använda för att driva effektiva CPM-annonser, öka e-postkopplingen, lägga till fler varumärkes- eller produktkontaktytor och få användarna att stanna längre. Viktiga resultatindikatorer för visning är bland annat [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]och [!UICONTROL Cost per Conversion]. DSP har stöd för en mängd olika annonsstorlekar för visningsbanderoller.

* **Mobilannonser (endast från tredje part)**: Mobilannonser kan vara i förrullningsvideo (VAST, MRAID) eller standardvisningsformat. Mobil pre-roll-video kan spelas upp automatiskt eller spelas upp klick för uppspelning och är bäst för att nå tittare på olika skärmar. Visning av mobilstandard är en statisk bild som visas i webbläsare eller i appar för mobila enheter och är bäst att använda för att komplettera köp av digital video, skapa en meddelandeassociation och lägga till ytterligare varumärke eller produktkontaktytor. Mobilannonser kan också fungera som helskärmsannonser eller som mobilinterstitialer, som är högeffektiva mobilannonser i helskärmsläge som är bäst för att utveckla varumärkeskännedom för mobiler och driva konverteringar.

* **Inbyggda visningsannonser (endast för första part)**: Inbyggda annonser stöds i standardvisningsformat. Interna annonser innehåller en rubrik och/eller titel, beskrivning, logotyp och bild. Annonselementen kombineras och återges så att de matchar utgivarens sidstil, så att annonsen blandas in med utgivarens organiska innehåll och skapar ett större engagemang. Det inbyggda formatet används bäst för att öka varumärkeskännedomen och öka läsarnas exponering och engagemang med visningsvänlig reklam. Viktiga resultatindikatorer omfattar [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]och [!UICONTROL Cost Per Conversion].

* **Pre-roll Ads (endast från tredje part)**: Pre-roll-annonser (VAST och VPAID) visas före premiumvideomaterial och ger en engagerande, engagerande tittarupplevelse. Videor före filmningen kan vara interaktiva, innehålla multimediefunktioner och innehålla övertäckningar, överrullningar och actionanrop. Viktiga resultatindikatorer för videoannonser före rullning är bland annat [!UICONTROL Video Completion Rate] och [!UICONTROL Viewability Rate].

* **Anslutna TV-annonser (endast från tredje part)**: Annonser på uppkopplade TV-apparater visas före och under videoinnehåll på premium-TV. Alla anslutna TV-inventeringar körs på tv-enheter, vilket innebär att videon spelas upp automatiskt i en återgivningsmiljö i helskärmsläge som tittarna inte kan hoppa över. Uppkopplad TV är det närmaste digitala videoformatet för TV-reklamen. Viktiga resultatindikatorer för uppkopplad TV omfattar [!UICONTROL Completion Rate].

* **Universal Video Ads (endast från tredje part)**: Med universella videoannonser kan ni rikta in er på videolagret från datorer, mobiler och anslutna TV-miljöer för VPAID- och VAST-inventering med en enda videoplacering. De kombinerar alla funktioner som finns i uppkopplad TV, pre-roll och mobil pre-roll-reklam och visas före och under videoinnehåll. Viktiga prestandaindikatorer för universell video [!UICONTROL Completion Rate] och [!UICONTROL Viewability Rate].

  Universella videoannonser kan bara bifogas till universella videomaterial.

  Se &quot;[Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)&quot; för mer information om universella videoannonser.

## DSP annonsgodkännanden

När du skapar en annons DSP igenom den för att se om det finns känsliga kategorier, klickar på URL-funktionen och förhandsgranskar återgivningen.

Till att börja med är annonserna [!UICONTROL Status] kolumn visar en röd punkt. Granskningsprocessen tar normalt 24-48 timmar. En trasig annons kan dock ha en väntande status i mer än 48 timmar, så du har tid att åtgärda fel innan annonsen refuseras. Avvisade annonser innehåller en orsak till refuseringen.

När DSP godkänner en annons visas en grön punkt i annonsens statuskolumn.

![godkännandeindikator i [!UICONTROL Status] kolumn](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Din annons kan bara visas om både DSP och SSP har godkänt den kreativa processen. Varje enskild SSP har sina egna krav och processer för godkännande.

>[!MORELIKETHIS]
>
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Annonsspecifikationer](ad-specs.md)
