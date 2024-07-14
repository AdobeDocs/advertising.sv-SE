---
title: Varumärkessäkerhet och mediakvalitet
description: Läs mer om varumärkessäkerhet och funktioner för mediekvalitet.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: a927c073fd27e0b2c84bd1929eb4d6d233a29cb5
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Varumärkessäkerhet och mediakvalitet

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP har en uppsättning funktioner för varumärkesskydd som säkerställer att alla era kampanjer når verkliga användare i en varumärkessäker miljö.

Vårt team för bedrägeriövervakning samarbetar nära med branschledande partner, som [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] och [!DNL WhiteOps], för att noggrant strukturera inventeringen på vår plattform. Genom en proaktiv hantering av vårt utbud säkerställer DSP att alla annonsörer på plattformen skyddas från icke-mänsklig trafik (botar, crawler, datacentralstrafik och bedrägeri) och endast levererar i varumärkessäkra sammanhang.

Förutom att tillhandahålla central kvalitetsstyrning anser vi att annonsörerna ska kunna utforma de kontroller som är anpassade till deras varumärke. DSP erbjuder integreringar med [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] och [!DNL Peer39], vilket säkerställer att varje annonsör kan välja önskad nivå på bedrägeriskydd, kontextfiltrering och målgruppsanpassning för nyckelord.

## Kvalitetsinitiativ

### Lagerverifiering med stöd för [!DNL Ads.txt]

[[!DNL Ads.txt], som står för  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) är ett initiativ som startades av [!DNL Interactive Advertising Bureau] ([!DNL IAB]) i juni 2017 för att underlätta korrekt återgivning av lager på den öppna marknaden och därmed motverkas olagliga källor till trafik och domänförfalskning. Deltagande utgivare och distributörer deklarerar offentligt företagen som auktoriserade att sälja sitt digitala lager, och vilken typ av relationer det gäller, genom att ha en `ads.txt`-sida på domänens högsta nivå (till exempel `example.com/ads.txt`).

DSP stöder [!DNL ads.txt] genom att läsa varje utgivares `ads.txt`-fil och ger dig möjlighet att endast köpa från verifierade [!DNL ads.txt]-försäljare. Genom att matcha de säljare vi ser med åtkomst av `nytimes.com` till New York Times `ads.txt`-filen kan vi identifiera vilka som är berättigade och vilka som inte är det. Vi blockerar de som gör intrång om placeringen är konfigurerad att endast köpa från verifierade säljare. <!-- can we actually mention NY Times? -->

Du kan ange [!DNL ads.txt]-standardkontroller för varje annonsörer<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) till:

* köpa lager endast från en domäns auktoriserade direktförsäljare

* köpa lager endast från en domäns auktoriserade direktförsäljare och återförsäljare

* prioritera att köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare

* köpa lager från alla säljare

### Övervakning av plattformsbedrägerier

DSP har byggt kraftfulla interna verktyg och system för att hantera bedrägerier på hela vår plattform, och samarbetar med ledande branschleverantörer som [!DNL Whiteops] och [!DNL Integral Ad Science].

Dessutom samarbetar Adobe nära med [!DNL IAB] och [!DNL TAG] för att säkerställa en stabil, branschstandard blockering av bedrägerier för att skydda våra annonsörer, med hjälp av verktyg som [!DNL ads.txt] (se föregående avsnitt), listan [!DNL IAB] Bots and Spiders samt IP-listan för [!DNL TAG] Datacenter.

Genom vår flerdimensionella strategi för kvalitet övervakar vårt team avvikelser och ogiltiga trafikmönster, vilket säkerställer mindre än 3 % ogiltig trafik på skyddat lager. Alla lager som är misstänkta - inklusive lager på specifika domäner eller från specifika utgivare eller säljare - blockeras omedelbart på hela plattformen.

### Lagermappning, nivåindelning och kategorisering

Inventariemappning är den detaljerade process för granskning och introduktion som krävs för allt nytt lager innan det läggs till på vår plattform. Denna process är utformad för att säkerställa säkerheten och kvaliteten för alla DSP.

* **Mappning:** Inventeringsteamet granskar varje domän noggrant och utvärderar till exempel:

   * Varumärkessäkerhet

   * Annonstypverifiering

   * Allmänt innehåll, dubblettdomäner och fejkad annonsvisning

* **Nivåer:** Vi undersöker helhetsintrycket av varumärket i det övergripande ekosystemet för att klassificera lagret i olika nivåer. Du kan [ange dina placeringar](/help/dsp/campaign-management/placements/placement-settings.md) som mål för dessa nivåer för önskad nivå av räckvidd:

   * **[!UICONTROL T1]** - Varumärkesnamn, internationellt identifierbara webbplatser

   * **[!UICONTROL T2]** - snygga webbplatser som är aktuella, aktuella, utan användargenererat innehåll och som vanligtvis saknas i den globala igenkänningen

   * **[!UICONTROL T3]** - Användargenererat innehåll och nischinnehåll

* **Webbplatskategorisering:** För att säkerställa enkel målinriktning och blockering av innehåll taggar vi varje egenskap med en DSP definierad webbplatskategori baserat på egenskapens innehåll. Du kan [ange som mål eller exkludera dessa webbplatskategorier för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) baserat på placeringsmålen.

### Omfattande stöd för webbplatsblockering

DSP innehåller både en global lista över blockerade webbplatser och alternativet att skapa anpassade listor över blockerade webbplatser för annonsörer och konton.

#### DSP Globalt blockerade webbplatser {#global-blocked-sites}

DSP har en global lista över webbplatser som blockerats och som anses osäkra att köra annonser på. Den här listan innehåller webbplatser med stötande innehåll (till exempel hat eller terror) och webbplatser som infekterats med botar, falska förrullningsdomäner, felmatchade domäner och annan bedräglig aktivitet.

Som en del av vårt varumärkessäkerhetsinitiativ för att rota bort aktiviteter som lockar annonsörer, skärs alla webbplatser med hjälp av åtgärderna i listan över blockerade webbplatser. Alla webbplatser som inte godkänns i varumärkessäkerhetskontrollerna läggs till i listan över globalt blockerade platser. Eftersom DSP hanterar den här listan dynamiskt kan sajterna när som helst gå vidare på eller bort från listan baserat på den senaste varumärkessäkerhetsanalysen.

När du tar med en plats i den globalt blockerade platslistan som placeringsmål flaggas platsen med ett rött utropstecken (!). Detta indikerar att annonser inte körs på den flaggade webbplatsen.

>[!NOTE]
>
>Du kan också kringgå den globala listan över blockerade webbplatser för standarddisplayannonser som är kopplade till en betrodd privat affär genom att aktivera alternativet [!UICONTROL Allow unscreened sites] i [placeringsinställningarna](/help/dsp/campaign-management/placements/placement-settings.md). Om det behövs kan kontoteamet på Adobe också avaktivera webbplatsblockering för ett offentligt (auktionsnivå) avtal i utgivarinställningarna för avtalet.

#### Blockerade webbplatslistor på kontonivå och annonsnivå

Användare kan också underhålla listor över blockerade webbplatser på kontonivå och annonsörnivå <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, som används automatiskt för alla placeringar. Listan Blockerade webbplatser på den lägre nivån används utöver listan Blockerade platser globalt.

## Tredjepartsintegreringar

### Sammanhangsbaserad filtrering

Med kontextuell filtrering kan du rikta eller blockera annonsmöjligheter baserat på kontexten på den sida som annonsen ska användas på. Adobe tillhandahåller kontextuell filtrering via integreringar med ledande leverantörer i branschen: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39]. Exempel på aktuella filter är [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] och [!UICONTROL G-rated Sites].

Du kan ange standardinställningar för kontextuella filter för varje annonsörer<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) om du vill. Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![Comscore logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png) ![Peer39 logo](/help/dsp/assets/peer39-logo.png)

### Blockering av bedrägeri före köp

Utnyttja våra tredjepartsintegreringar med [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39] för att blockera icke-mänsklig trafik från era kampanjer. Dessa integreringar ger branschledande funktioner för att blockera före bud för att minimera både allmän och avancerad ogiltig trafik (GIVT och SIVT) i era kampanjer.

Du kan ange standardinställningar för spärrkontroll före köp för varje annonsörer<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) om du vill. Ytterligare avgifter kan tillkomma när du använder den här funktionen.

Om du vill ha mer information om funktionalitet kontaktar du din föredragna leverantör direkt eller kontaktar ditt Adobe-kontoteam.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science-logotyp](/help/dsp/assets/ias-logo.png) ![Peer39-logotyp](/help/dsp/assets/peer39-logo.png)

### Visning före köp {#pre-bid-viewability}

Visningsfilter före bud som drivs av våra branschledande partners [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) och [!DNL Integral Ad Science] gör att annonsörer kan se till att deras kampanjer uppfyller de önskade visningsprestandamålen för video och displayannonser.

>[!NOTE]
>
>[!DNL Oracle] kommer att upphöra med sin annonsverksamhet senast den 30 september 2024, inklusive alla tjänster från [!DNL MOAT].

Du kan ange standardfilter för visning för varje annonsörer<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) om du vill. Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising-logotyp](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science-logotyp](/help/dsp/assets/ias-logo.png)

### Målinriktning och mätning

Partnerskapet [!DNL Adobe's] med [!DNL Adelaide] ger annonsörer stöd för Adelaide-måttet [!DNL Attention Units], som mäter mediekvaliteten baserat på ögonspårnings-, exponerings- och resultatdata.

[Med riktad uppmärksamhet före bud på placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md) kan annonsörer rikta in specifika uppmärksamhetsnivåer för att förbättra kundengagemanget.

Dessutom kan annonsörer aktivera [spårning för [!UICONTROL Attention Score]-mätvärdet ](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) på placeringsnivå (det viktade genomsnittliga antalet [!DNL Attention Units] över visningar) för alla kampanjer för att förstå vilka placeringsmetoder som ger bäst affärsresultat.

Ytterligare avgifter tillkommer för varje separat funktion.

### Ämnesanpassning

DSP kan du rikta in dig på eller blockera nyckelordslistor genom att utnyttja våra branschledande sammanhangsberoende partner [!DNL Comscore] och [!DNL Oracle Data Cloud] (tidigare [!DNL Grapeshot]). Ämnesinriktningen hjälper er att se till att era annonser alltid får plats i en miljö som är anpassad efter ert varumärke, oavsett om det handlar om att blockera skadligt innehåll eller säkerställa utgifter i ett sammanhang som garanterar ett bättre resultat.

>[!NOTE]
>
>[!DNL Oracle] kommer att upphöra med sin annonsverksamhet senast den 30 september 2024, inklusive alla tjänster från [!DNL Oracle Data Cloud] (tidigare [!DNL Grapeshot]).

För målinriktning efter ämne måste du skapa anpassade ämnessegment direkt med partnerplattformen. När segmenten har skapats kan du [ange ett mål eller utesluta ett segment-ID i avsnittet [!UICONTROL Audience Targeting] för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma för den här funktionen.

Om du vill skapa ett [!DNL Comscore]-konto och skapa anpassade ämnessegment kan du begära inloggning för [!DNL Activation Segment Manager] på [https://agents.comscore.com](https://agents.comscore.com). Mer information om hur du konfigurerar anpassade segment finns i [[!DNL Comscore] hjälpcentret](https://comscoreactivation.zendesk.com/hc/). Avgifter för anpassade segment visas i [!DNL Segment Manager] när du skapar dem.

![Comscore-logotyp](/help/dsp/assets/comscore-logo.png) ![Grapeshot-logotyp](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP har samarbetat med [!DNL DoubleVerify] för att kunna erbjuda sin [!DNL Authentic Brand Safety] målinriktningslösning, som gör att du kan skapa en centraliserad uppsättning varumärkessäkerhetskrav för att nå en enhetlig nivå på alla inköpsplattformar.

När du har byggt ett [!DNL DoubleVerify]-varumärkessäkerhetssegment med den nödvändiga målgruppsanpassningen kan du använda det i DSP för att replikera era era postanbudsblockregler med förhandsbud i olika webbmiljöer.

Du kan ange ett [!DNL DoubleVerify]-segment-ID för varje annonsör<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan [aktivera eller inaktivera [!UICONTROL Authentic Brand Safety] för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). DSP fakturerar ditt konto för användning av segment-ID.

Om du vill ha mer information om funktioner kontaktar du [!DNL DoubleVerify] direkt eller kontaktar ditt Adobe-kontoteam.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
