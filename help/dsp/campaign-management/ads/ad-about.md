---
title: Om annonshantering i DSP
description: Läs mer om annonshantering.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# Om annonshantering i DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP har stöd för annonsleverans via tredjepartstaggar för annonsvisning (som Google, Flashtalk eller Sizmek) för olika annonstyper och direkt medieöverföring för inbyggda displayannonser. Du kan överföra tredjepartstaggar individuellt eller gruppvis. Överföringar gruppvis använder partnertaggmallar eller en mall för grupptaggar.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

När era annonser väl är klara måste ni bifoga varje annons till en placering, som inkluderar målinriktningsparametrar (som geo, målgrupp, enhet och målinriktning mot lager) som styr hur kampanjen kommer att leverera. Du kan bifoga en annons till en eller flera placeringar.

## Tillgängliga annonstyper {#ad-types}

Alla följande annonstyper är tillgängliga i DSP. Fullständiga specifikationer för varje annonstyp finns i [Annonsspecifikationer](ad-specs.md).

* **Ljudannonser (endast från tredje part)**: Ljudannonser spelas upp mellan innehåll på digitala utgivarwebbplatser och kan köras fristående som ljudfiler eller tillsammans med andra banners. Ljud används bäst för att öka varumärkeskännedomen och engagera en publik på språng. Viktiga prestandaindikatorer för ljud är bland annat [!UICONTROL Completion Rate] och [!UICONTROL Cost per Completion].

* **Visa annonser (endast från tredje part)**: Visningsannonser är animerade eller statiska bilder som visas i webbläsare eller i appar. När du klickar på annonsenheten tar det användaren till en varumärkesprofilerad plats eller mikroplats. Skärmen är bäst att använda för att driva effektiva CPM-annonser, öka e-postkopplingen, lägga till fler varumärkes- eller produktkontaktytor och få användarna att stanna längre. Viktiga resultatindikatorer för visning är bland annat [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]och [!UICONTROL Cost per Conversion]. DSP har stöd för en mängd olika annonsstorlekar för visningsbanderoller.

* **Mobilannonser (endast från tredje part)**: Mobilannonser kan vara i förrullningsvideo (VAST, MRAID) eller standardvisningsformat. Mobil pre-roll-video kan spelas upp automatiskt eller spelas upp klick för uppspelning och är bäst för att nå tittare på olika skärmar. Visning av mobilstandard är en statisk bild som visas i webbläsare eller i appar för mobila enheter och är bäst att använda för att komplettera köp av digital video, skapa en meddelandeassociation och lägga till ytterligare varumärke eller produktkontaktytor. Mobilannonser kan också fungera som helskärmsannonser eller som mobilinterstitialer, som är högeffektiva mobilannonser i helskärmsläge som är bäst för att utveckla varumärkeskännedom för mobiler och driva konverteringar.

* **Inbyggda visningsannonser (endast för första part)**: Inbyggda annonser stöds i standardvisningsformat. Interna annonser innehåller en rubrik och/eller titel, beskrivning, logotyp och bild. Annonselementen kombineras och återges så att de matchar utgivarens sidstil, så att annonsen blandas in med utgivarens organiska innehåll och skapar större engagemang. Det inbyggda formatet används bäst för att öka varumärkeskännedomen och öka läsarnas exponering och engagemang med visningsvänlig reklam. Viktiga resultatindikatorer omfattar [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]och [!UICONTROL Cost Per Conversion].

* **Pre-roll Ads (endast från tredje part)**: Pre-roll-annonser (VAST och VPAID) visas före premiumvideomaterial och ger en engagerande, engagerande tittarupplevelse. Videor före filmningen kan vara interaktiva, innehålla multimediefunktioner och innehålla övertäckningar, överrullningar och actionanrop. Viktiga resultatindikatorer för videoannonser före rullning är bland annat [!UICONTROL Video Completion Rate] och [!UICONTROL Viewability Rate].

* **Anslutna TV-annonser (endast från tredje part)**: Anslutna TV-annonser visas före och under Premium TV-videomaterial. Alla anslutna TV-inventeringar körs på tv-enheter, vilket innebär att videon spelas upp automatiskt i en återgivningsmiljö i helskärmsläge som tittarna inte kan hoppa över. Uppkopplad TV är det närmaste digitala videoformatet för TV-reklamen. Viktiga resultatindikatorer för uppkopplad TV är bland annat [!UICONTROL Completion Rate].

* **Universal Video Ads (endast från tredje part)**: Universella videoannonser kombinerar alla funktioner i uppkopplad TV, Pre-roll och Mobile Pre-roll Ads (VAST och VPAID) till en och visas före och under videoinnehåll. Universal Video-annonser kan användas för videolager från skrivbordsmiljöer, mobiler och anslutna tv-miljöer, vilket gör att man slipper skapa flera videoannonser. Viktiga prestandaindikatorer för Universal Video är [!UICONTROL Completion Rate] och [!UICONTROL Viewability Rate].

## DSP annonsgodkännanden

När du skapar en annons läser DSP om den innehåller känsliga kategorier, klickar på URL-funktionalitet och förhandsgranskar återgivning.

Till att börja med visas en röd punkt i [!UICONTROL Status] kolumn. Granskningsprocessen tar normalt 24-48 timmar. En trasig annons kan dock ha en väntande status i mer än 48 timmar, så du har tid att åtgärda fel innan annonsen refuseras. Avvisade annonser innehåller en orsak till refuseringen.

När DSP godkänner en annons visas en grön punkt i statuskolumnen.

![godkännandeindikator i [!UICONTROL Status] kolumn](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Din annons kan endast användas om både DSP och SSP har godkänt den kreativa processen. Varje enskild SSP har sina egna krav och processer för godkännande.

>[!MORELIKETHIS]
>
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Annonsspecifikationer](ad-specs.md)

