---
title: Översikt över  [!DNL Analytics for Advertising]
description: Översikt över  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 8911f6ea16878bede96151f004e6de2717484140
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Översikt över [!DNL Analytics for Advertising]

*Annonsörer med Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integrerar Adobe Analytics och Adobe Advertising för att utöka och förbättra funktionerna i varje produkt.

Integrationen gör att annonsörer kan spåra klicknings- och genomskinlighetsinteraktioner på webbplatser i sina [!DNL Analytics]-instanser, vilket gör att varumärken kan se hur deras annonsutgifter leder till webbplatsengagemang och viktiga affärsmål.

Dessutom kan Adobe Advertising komma åt de omfattande förstahandsdata som [!DNL Analytics] samlar in med hjälp av [!DNL Analytics] -taggar som redan finns på webbplatsen. Detta ger en mer robust hantering av resor, återmarknadsföring från första part och rapportering av betalda webbplatser. Adobe Advertising kan använda [!DNL Analytics]-data ytterligare för optimering av utgifter och bud.

När [!DNL Analytics for Advertising] används på rätt sätt blir gränserna mellan två traditionella roller suddiga: hantering av annonseringsresor (den åtgärd som innebär att användare skickas till webbplatsen via annonser) och förståelse för webbplatsengagemanget via webbanalys.

Fördelar:

* Skicka [!DNL Analytics] segment direkt till Adobe Advertising för återmarknadsföring av förstahandswebbplatser.
* Använd anpassade [!DNL Analytics]- och standardhändelser som konverteringssignaler för optimering av betalmediereklam.
* Dra nytta av [!DNL Analytics] Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden.
* Bättre samarbete mellan webbanalytiker och betalteam.
* Använd beständig Adobe Advertising-vy och klicknings-ID:n i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Förbättra traditionella betalda medierapporter i Analysis Workspace med anpassade mätvärden, anpassade dimensioner och webbplatsaktivitet som inte är möjliga när data eller pixlar exporteras till annonsservrar eller andra DSP.
* Dra nytta av den [!DNL Analytics]-kod som redan finns på webbplatsen för att spåra och optimera den i Adobe Advertising.

>[!TIP]
>
> Se en [videopresentation till  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Använda analyser för betald medierapportering

[!DNL Analytics for Advertising] förbättrar rapporteringen och inblicken om hur annonseringen påverkar webbplatsens beteende genom att du kan:

* Använd beständig Adobe Advertising-vy och klicknings-ID:n i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Utnyttja Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden. Ni har tillgång till dimensionella data och händelsedata för betalda media, som innehåller kampanjenhetsnamn i Adobe Advertising (inte bara för utplaceringar och annonser) och tillhörande mått, t.ex. klick, visningar och kostnader.

Om du vill använda [!DNL Analytics] som ditt betalda medierapporteringsverktyg behöver din organisation en Experience Cloud-inloggning med åtkomst till Analysis Workspace. Adobe Advertising-teamet kommer att hjälpa er att mappa data från Adobe Advertising till enskilda rapporteringsprogram i Analysis Workspace. Du kan skicka data från Adobe Advertising till alla rapportsviter, men du bör vara medveten om de rapportsviter som har mappats till Adobe Advertising och de som inte har det. Beroende på rapportsviten kan detta ändra rapporterade data.

[Adobe Advertising-ID:n i [!DNL Analytics]](ids.md) fungerar som andra [!DNL eVars], med en anpassad, beständig förfallotid. Som standard är attributsökningsfönstret inställt på 60 dagar under Adobe Advertising-implementeringen. Om du vill ändra den här inställningen arbetar du med ditt kontoteam på Adobe.

Adobe Advertising-dimensioner läggs till med suffixet&quot;(AMO ID)&quot; (t.ex.&quot;Ad Type (AMO ID)&quot;). En lista med tillgängliga dimensioner finns i [Adobe Advertising-mått i Analysis Workspace](advertising-metrics-in-analytics.md).

>[!NOTE]
>
> När du visar Adobe Advertising-data (eller en datauppsättning) inom [!DNL Analytics], ska du vara medveten om att mått och rapporter baseras på reglerna som anges i [!DNL Analytics]. Data kan skilja sig från vad du ser i andra rapporteringssystem, till exempel annonsserverrapporter, [!DNL DSP]-rapporter eller sökmotorrapporter. För att förstå dataskillnaderna i [!DNL Analytics] måste du veta när [!DNL eVar]-data förfaller, vad som definierar ett besök, vad som betraktas som senaste beröringsattribuering jämfört med total bestående attribuering och andra faktorer. Mer information finns i [Förväntade datavariationer mellan  [!DNL Analytics]  och Adobe Advertising](data-variances.md).

## Använda analyser för att driva Adobe Advertising-kampanjer och Portfolio

Utan att ytterligare pixlar behövs kan [!DNL Analytics for Advertising] optimera och segmentera målgrupper bättre genom att skicka två huvudsignaler till Adobe Advertising:

* Konverteringsmått som ska användas som anbudssignaler:
   * standardmått, som [!UICONTROL Revenue] och [!UICONTROL Cart Views].
   * mått för webbplatsengagemang, t.ex. sidvisning och besök.
   * anpassade intäktsmått.
   * reserverade intäktsmått.
* Segment som har skapats i [!DNL Analytics] och publicerats i Experience Cloud.

  Du kan använda [!DNL Analytics] segment för återmarknadsföring av förstahandswebbplatser i [!DNL DSP] och betalda sökannonser.

  ([!DNL Search, Social, & Commerce] endast) Annonsörer med [!DNL Analytics], men inte Audience Manager, kan också skapa taggremsbaserade målgrupper (ommarknadsföringslistor) för Google webbplats och kundmatchande målgrupper (kundlistor) från [!DNL Analytics] segment som delas med Experience Cloud.

### Webbplatskonverteringsmått som budsignaler

Du kan använda standardhändelser och anpassade händelser från [!DNL Analytics] för att skapa viktade mål i Adobe Advertising. Mål är grunden för beslut om anbudsgivning för dina [!DNL DSP]-paket samt för Search-, Social- och Commerce-portföljer.

För [!DNL Google Ads]- och [!DNL Google Microsoft Advertising]-kampanjer i hybridportföljerna Search, Social och Commerce kan du överföra målen - inklusive eventuella [!DNL Analytics] -händelser i målen - direkt till annonsnätverken, där de blir tillgängliga som konverteringsåtgärder för anpassade konverteringsmål på kontonivå och kampanjnivå.

>[!NOTE]
>
> Du kan inte mappa beräknade värden från [!DNL Analytics] till Adobe Advertising.

Ditt Adobe Advertising-team hjälper dig att identifiera och mappa händelser som gäller för betalmedieprestanda till Adobe Advertising, där de listas i [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

I [Analysstatistik i Adobe Advertising](analytics-data-in-advertising.md) finns en lista med tillgängliga mätvärden.

### Analyssegment för återmarknadsföring av webbplatser

Adobe Advertising kan importera [!DNL Analytics] segment för återmarknadsföring för Advertising DSP och [!DNL Search, Social, & Commerce] annonser med hjälp av integreringen mellan [!DNL Analytics] och Experience Cloud.

Om du vill komma åt [!DNL Analytics]-segmenten måste ett annonserarkonto aktivera [Experience Cloud ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/home.html). När ID-tjänsten är aktiverad blir alla segment i Experience Cloud (inklusive segment som skapats i [!DNL Analytics] och publicerats i Experience Cloud, segment som skapats i Adobe Audience Manager, segment som skapats i Experience Cloud med [!DNL People core service] samt segment som skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager) tillgängliga i Adobe Advertising så snart de bearbetas.

[!DNL Analytics] segment är tillgängliga inom 24 timmar och uppdateras dagligen.

Mer information om tjänsten Experience Cloud Publiker finns i [Experience Cloud Publiker](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exempel på hur du använder integreringen {#integration-examples}

### Använda data från Adobe Advertising i Analysis Workspace

Om du vill veta hur du kan använda dina Adobe Advertising-data för att skapa visuella rapporter i Analysis Workspace ska du titta på videon &quot;[Introduktion till Workspace och rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

#### Använda Conversions i rapporter för direktansluten TV-visning

*Endast Advertising DSP-användare*

Ni kan mäta fullkanalseffekten för era uppkopplade TV-kampanjer genom att länka annonsexponering på CTV-enheter till konverteringar på plats. Det nya [!UICONTROL Landing Type]-filtret [!UICONTROL View-through (CTV)] delar upp konverteringar i separata rader för värdena [!UICONTROL Click Through], [!UICONTROL View Through] och [!UICONTROL View Through (CTV)].

Använd antingen placeringsvyn eller marknadsföringskanalvyn i Analysis Workspace för att visa dina CTV-konverteringsvärden.

Använda placeringsvyn:

1. Inkludera utgifter för CTV i rapportvyn.

1. Inkludera önskade mätvärden, t.ex. &quot;Impressions&quot;, &quot;Clicks&quot; osv.

1. Använd följande filter:

   Annonsplattform: `Advertising Cloud DSP`

   Landningssida: `View-Through (CTV)`

Använda vyn Marknadsföringskanal:

1. Inkludera dimensionen `Marketing Channel`.

1. Inkludera önskade mätvärden, t.ex. &quot;Impressions&quot;, &quot;Clicks&quot; osv.

1. Använd följande filter:

   Annonsplattform: `Advertising Cloud DSP`

   Landningssida: `View-Through (CTV)`

### Skapa instrumentpaneler för Adobe Advertising

Om du vill veta hur du kan spåra dina Adobe Advertising-data mot dina mål i Analysis Workspace kan du titta på videon &quot;[Skapa instrumentpaneler för Adobe Advertising med Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Använda Adobe Advertising-ID för analys av webbplatspost

Se videon [Skapa rapporter om webbplatsposter för Adobe Advertising ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html) om du vill se hur du kan skapa en Adobe Advertising-platspost för att övervaka veckodag, veckotid, webbläsare och geografisk påverkan.

## Initiera en [!DNL Analytics for Advertising]-implementering

Kontakta kontoteamet på Adobe som kommer att slutföra den initiala konfiguration som krävs för att börja och hjälpa dig att planera implementeringen och dataanvändningen baserat på organisationens behov.

>[!MORELIKETHIS]
>
>* [Video: Introduktion till  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Krav och nyckelinformation för implementering [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising-ID:n som används av analyser](ids.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
>* [Adobe Advertising-mått i Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
