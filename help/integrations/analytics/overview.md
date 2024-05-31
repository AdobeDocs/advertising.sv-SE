---
title: Översikt [!DNL Analytics for Advertising]
description: Översikt [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: a0a3bb1e74ffc687118d0336a03dcc6164b67226
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Översikt [!DNL Analytics for Advertising]

*Annonsörer med DSP och[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integrerar Adobe Analytics och Adobe Advertising för att utöka och förbättra funktionerna i respektive produkt.

Tack vare integreringen kan annonsörer spåra klicknings- och genomskinlighetsinteraktioner på webbplatser i sina [!DNL Analytics] instanser, som gör det möjligt för varumärken att se hur deras annonskostnader leder till webbplatsengagemang och viktiga affärsmål.

Dessutom kan Adobe Advertising komma åt de omfattande förstahandsdata som [!DNL Analytics] samlingar med [!DNL Analytics] -taggar finns redan på platsen. Detta ger en mer robust hantering av resor, återmarknadsföring från första part och rapportering av betalda webbplatser. Adobe Advertising kan använda [!DNL Analytics] data för optimering av utgifter och bud.

När de är korrekt anställda, [!DNL Analytics for Advertising] Skapar oskärpa mellan två traditionella roller: hantering av annonseringsresor (den åtgärd som innebär att användare skickas till webbplatsen via annonser) och förståelse för webbplatsengagemanget via webbanalys.

Fördelar:

* Skicka [!DNL Analytics] segment direkt till Adobe Advertising för återmarknadsföring av förstahandswebbplatser.
* Använd [!DNL Analytics] anpassade händelser och standardhändelser som konverteringssignaler för optimering av betalmediereklam.
* Utnyttja [!DNL Analytics] Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden.
* Bättre samarbete mellan webbanalytiker och betalteam.
* Använd beständiga Adobe Advertising-vy- och klicknings-ID:n i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Förbättra traditionella betalda medierapporter i Analysis Workspace med anpassade mätvärden, anpassade dimensioner och webbplatsaktivitet som inte är möjliga när data eller pixlar exporteras till annonsservrar eller andra DSP.
* Utnyttja [!DNL Analytics] finns redan på webbplatsen för att spåra och optimera Adobe Advertising.

>[!TIP]
>
> Se en [videopresentation till [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Använda analyser för betald medierapportering

[!DNL Analytics for Advertising] ger bättre rapporter och insikt i hur annonserna påverkar webbplatsens beteende genom att göra det möjligt för er att:

* Använd beständiga Adobe Advertising-vy- och klicknings-ID:n i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Utnyttja Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden. Ni har tillgång till dimensionella data och händelsedata för betalda media, som innehåller kampanjenhetsnamn i Adobe Advertising (inte bara för utplaceringar och annonser) och tillhörande mått, t.ex. klick, visningar och kostnader.

Används [!DNL Analytics] som ert betalda medierapporteringsverktyg behöver din organisation logga in på Experience Cloud med tillgång till Analysis Workspace. Adobe Advertising-teamet kommer att hjälpa er att mappa data från Adobe Advertising till enskilda rapporteringsprogram i Analysis Workspace. Du kan skicka data från Adobe Advertising till alla rapportsviter, men du bör vara medveten om de rapportsviter som har mappats till Adobe Advertising och de som inte har det. Beroende på rapportsviten kan detta ändra rapporterade data.

[Adobe Advertising-ID:n i [!DNL Analytics]](ids.md) arbeta som andra [!DNL eVars], med en anpassad, permanent förfallotid. Som standard är attributsökningsfönstret inställt på 60 dagar under Adobe Advertising-implementeringen. Om du vill ändra den här inställningen arbetar du med ditt kontoteam på Adobe.

Adobe Advertising-dimensioner läggs till med suffixet&quot;(AMO ID)&quot; (t.ex.&quot;Ad Type (AMO ID)&quot;). Se &quot;[Adobe Advertising Metrics in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; för en lista över tillgängliga dimensioner.

>[!NOTE]
>
> När du visar data från Adobe Advertising (eller en datauppsättning) i [!DNL Analytics]ska du vara medveten om att mätvärden och rapporter baseras på de regler som anges i [!DNL Analytics]. Informationen kan skilja sig från vad du ser i andra rapporteringssystem, som annonsserverrapporter, [!DNL DSP] rapporter eller sökmotorrapporter. För att förstå datamatchningsskillnaderna i [!DNL Analytics]behöver du veta när [!DNL eVar] data förfaller, vilket definierar ett besök, vad som betraktas som sista beröringsattribuering jämfört med total bestående attribuering och andra faktorer. Mer information finns i [Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising](data-variances.md).

## Använda analyser för att driva Adobe Advertising-kampanjer och Portfolio

Utan behov av ytterligare pixlar, [!DNL Analytics for Advertising] ger bättre optimering och enklare målgruppssegmentering genom att skicka två huvudsignaler till Adobe Advertising:

* Konverteringsmått som ska användas som anbudssignaler:
   * standardvärden, som [!UICONTROL Revenue] och [!UICONTROL Cart Views].
   * mått för webbplatsengagemang, t.ex. sidvisning och besök.
   * anpassade intäktsmått.
   * reserverade intäktsmått.
* Segment skapade i [!DNL Analytics] och publiceras i Experience Cloud.

  Du kan använda [!DNL Analytics] segment för återmarknadsföring av förstahandswebbplatser i [!DNL DSP] och betalda sökannonser.

  ([!DNL Search, Social, & Commerce] endast) Annonsörer med [!DNL Analytics] men inte Audience Manager kan också skapa taggbaserade målgrupper (ommarknadsföringslistor) för Google webbplatser och kundmatchande målgrupper (kundlistor) från [!DNL Analytics] segment som delas med Experience Cloud.

### Webbplatskonverteringsmått som budsignaler

Du kan använda standardhändelser och anpassade händelser från [!DNL Analytics] bygga viktade mål i Adobe Advertising. Målen ligger till grund för era anbudsbeslut [!DNL DSP] paket och sökportfolior.

>[!NOTE]
>
> Du kan inte mappa beräknade värden från [!DNL Analytics] till Adobe Advertising.

Adobe Advertising-teamet hjälper dig att identifiera och kartlägga de händelser som gäller för betalmedieprestanda i Adobe Advertising, där de listas i [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Se &quot;[Analytics-statistik i Adobe Advertising](analytics-data-in-advertising.md)&quot; om du vill se en lista över tillgängliga mätvärden.

### Analyssegment för återmarknadsföring av webbplatser

Adobe Advertising kan äta [!DNL Analytics] segment för återmarknadsföring för DSP och [!DNL Search, Social, & Commerce] annonser som använder Experience Cloud-målgruppsintegreringen mellan [!DNL Analytics] och Experience Cloud.

Så här öppnar du [!DNL Analytics] segment, ett annonserarkonto måste aktivera [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html). När ID-tjänsten är aktiverad, alla segment i Experience Cloud (inklusive segment skapade i [!DNL Analytics] och publiceras i Experience Cloud, segment som skapats i Adobe Audience Manager, segment som skapats i Experience Cloud med [!DNL People core service]och segment som skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager) blir tillgängliga i Adobe Advertising så snart de bearbetas.

[!DNL Analytics] segmenten är tillgängliga inom 24 timmar och uppdateras dagligen.

Mer information om Publiktjänsten i Experience Cloud finns i [Experience Cloud målgrupper](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exempel på hur du använder integreringen {#integration-examples}

### Använda data från Adobe Advertising i Analysis Workspace

Om du vill veta hur du kan använda dina Adobe Advertising-data för att skapa visuella rapporter i Analysis Workspace kan du titta på videon &quot;[Introduktion till arbetsyta och rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Använda Conversions i rapporter för direktansluten TV-visning

*Annonsera endast DSP användare*

Ni kan mäta fullkanalseffekten för era uppkopplade TV-kampanjer genom att länka annonsexponering på CTV-enheter till konverteringar på plats. Den nya [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; delar upp konverteringar till separata rader för [!UICONTROL Click Through], [!UICONTROL View Through]och [!UICONTROL View Through (CTV)] värden.

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

Om du vill veta hur du kan spåra dina Adobe Advertising-data mot dina mål i Analysis Workspace kan du titta på videon &quot;[Skapa instrumentpaneler för Adobe Advertising med Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Använda Adobe Advertising-ID för analys av webbplatspost

Se videon &quot; om du vill se hur du kan skapa en rapport på Adobe Advertising för att övervaka veckodag, tidpunkt, webbläsare och geografiska förhållanden.[Skapa rapporter för webbplatsposter i Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

## Initiera en [!DNL Analytics for Advertising] Implementering

Kontakta kontoteamet på Adobe som kommer att slutföra den initiala konfiguration som krävs för att börja och hjälpa dig att planera implementeringen och dataanvändningen baserat på organisationens behov.

>[!MORELIKETHIS]
>
>* [Video: Introduktion till [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising ID som används av Analytics](ids.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Förväntade datavariationer mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
