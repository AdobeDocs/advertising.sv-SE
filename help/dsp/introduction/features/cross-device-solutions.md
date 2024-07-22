---
title: Enhetsoberoende lösningar
description: Läs mer om funktioner för olika enheter.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Enhetsoberoende lösningar

Tack vare Advertising DSP-integreringen med [!DNL LiveRamp] kan du utöka din publik till alla kända enheter, inte bara de enheter som varumärket har spårat. Integreringen ger även frekvensbegränsning och attribueringsmätning på alla enheter.

När du använder ett personbaserat enhetsdiagram som stöds kan du:

* Matcha målgrupper över alla kanaler och enheter för att leverera annonser till människor och hushåll, i stället för till enheter.
* Balansera annonsexponering genom förståelse och frekvens mellan olika individer.
* Testa strategier som exponerar kontra konverterar målgrupper över olika kanaler eller enheter.

## Fördelar med enhetsdiagrammet [!DNL LiveRamp]

* Tillhandahåller en deterministisk datapool, inklusive kunddata offline

* Gäller även cookie-ID:n och mobila enhets-ID:n

* Inkluderar data främst från USA

* Är kostnadsfritt för frekvensbegränsning och attribueringsmätning

* Prissatt till $0,35 CPM för utökade visningar (visningar som levereras enbart med enhetsdiagrammet [!DNL LiveRamp] i stället för på enheter som hittas inom målgruppssegmenten)

  Kursen visas på ditt kontokort.

## Personbaserad frekvenshantering

Med personbaserad frekvenshantering kan du ange frekvensgränser på personnivå, i stället för på enhetsnivå, för kontroll av medieexponering.

### Aktivera personbaserad frekvenshantering

* **Kampanjer:** När du skapar en ny kampanj kan du ange en [!UICONTROL Cross-Device Level]-inställning. Aktivera [!UICONTROL Same Device] -> [!UICONTROL People] och välj ett enhetsdiagram. Det angivna enhetsdiagrammet används både för målinriktning mellan olika enheter på placeringsnivå och för personbaserad frekvenshantering på kampanj-, paket- och placeringsnivå. Frekvensintervallen gäller för alla en persons kända enheter.

Mer information finns i [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md).

När du har sparat en kampanj kan du inte ändra dess [!UICONTROL Cross Device Level]-inställning.

* **Paket:** Du kan välja att ange ytterligare frekvensgränser på paketnivå. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

* **Placeringar:** Du kan ange ytterligare frekvensomslag på placeringsnivån om du vill. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

## Målgruppsbaserad anpassning

Med personbaserad målinriktning kan ni hitta kunder på både dator och mobil.

### Aktivera personbaserad anpassning

* **Kampanjer:** När du skapar en ny kampanj kan du ange en [!UICONTROL Cross-Device Level]-inställning. Aktivera [!UICONTROL Same Device] -> [!UICONTROL People] och välj ett enhetsdiagram. Det angivna enhetsdiagrammet används både för målinriktning mellan olika enheter på placeringsnivå och för personbaserad frekvenshantering.

Mer information finns i [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Placeringar:** När du väljer målgruppsmål för en placering i en kampanj med ett angivet enhetsdiagram kan du med ett [!UICONTROL Cross-Device Targeting]-alternativ utöka målgruppsanpassningen för alla en persons kända enheter (enligt enhetsdiagrammet som anges i kampanjinställningarna), även enheter som inte finns i de angivna segmenten.

### Konfigurera rapportering för personbaserad målgruppsanpassning

Du kan inkludera följande mått i anpassade rapporter:

* **Utökade avbildningar:** (I avsnittet [!UICONTROL Build Your Report] under [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Volymen inkrementella avbildningar som levereras genom att ett enhetsdiagram används (och som inte hittas i de ursprungliga målgruppssegmenten). Det här måttet används också för att beräkna tillämpliga avgifter som är kopplade till användning av ett enhetsdiagram från tredje part.

  Om du vill fastställa kostnaden för dina utökade avbildningar under en tidsperiod, kör du en anpassad rapport som innehåller kolumnen [!UICONTROL Extended Impressions] och multiplicerar sedan det totala antalet utökade avbildningar med 0,00035 USD ($0,35/1000 visningar).

  Den aggregerade kostnaden inkluderas också i kolumnen [!UICONTROL Billable Other Net Spend] (under [!UICONTROL Metrics] > [!UICONTROL Spend]), även om det måttet även inkluderar andra kampanjavgifter som du kan ha lagt till.

* **Enhetsdiagram:** (i avsnittet [!UICONTROL Build Your Report] under [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Det valda enhetsdiagrammet för en viss kampanj, ett visst paket eller en viss placering.

## Personbaserad attribueringsmätning

*Annonsörer med endast konverteringsspårning i Adobe Advertising*

Med personbaserad attribuering kan du attribuera konverteringar som ägde rum på en annan enhet än den enhet som medieexponeringen inträffade på. Personbaserad attribueringsmätning är tillgänglig i alla DSP, [!DNL Adobe Advertising Creative] och [!DNL Adobe Advertising Search, Social, & Commerce] för annonsörer som har implementerat Adobe Advertising-konverteringspixlar på sina webbplatser.

### Aktivera personbaserad attribueringsmätning

Om du vill aktivera attribueringsmätning mellan enheter kontaktar du kontoteamet på Adobe.

### Ställ in konverteringsrapporter för attribut för konvertering mellan enheter

#### Inställningar för konverteringsrapport

När ett enhetsdiagram har aktiverats för attribueringsmätning innehåller [!UICONTROL Conversion]-rapporten en [!UICONTROL Cross-Device Breakout]-inställning som gör att du kan ta med upp till tre separata kolumner för varje konverteringsmått, inklusive:

* &lt;*Konvertering*>[!UICONTROL (tp)]: Innehåller det totala antalet konverteringar (totalt antal personer), som omfattar både konverteringar för samma enhet och konverteringar för olika enheter (om tillämpligt). I rapporten bifogas [!UICONTROL (tp)] till konverteringsmåttets namn, regeltyp och konverteringstyper i konverteringssökvägen (till exempel&quot;Responses(le)(tl)(tp))).

* &lt;*Konvertering*>[!UICONTROL (sd)]: (Valfritt) Inkluderar endast konverteringar för vilka endast en enhet spårades i konverteringssökvägen. I rapporten bifogas [!UICONTROL (sd)] till konverteringsmåttets namn, regeltyp och konverteringstyper i konverteringssökvägen (till exempel&quot;Responses(le)(tl)(sd)).

* &lt;*Konvertering*>[!UICONTROL (xd)]: (Valfritt) Inkluderar endast konverteringar för vilka mer än en enhet spårades i konverteringssökvägen. I rapporten bifogas [!UICONTROL (xd)] till konverteringsmåttets namn, regeltyp och konverteringstyper i konverteringssökvägen (till exempel&quot;Responses(le)(tl)(xd)).

#### Tolka konverteringsrapporten

Sortera procentandelen av det totala antalet konverteringar mellan enheter ([!UICONTROL (xd)]/[!UICONTROL (tl)]) från hög till låg för att förstå vad som genererar över medelvärdet för konverteringar mellan olika enheter. Du kan använda detta för att informera om din kreativa strategi eller målinriktningsstrategi så att meddelanden och kanalinvesteringar matchar användarens beteende.

* Paket - Se vilka paket som genererar flest konverteringar och vilka som har en hög andel konverteringar mellan olika enheter. Detta kan hjälpa er att förstå var ni ska satsa.

* Placeringar - Jämför placeringsprestanda och attribuering (en mobil webbannons kan till exempel leda till konverteringar på datorn). Utan ett enhetsdiagram för attribuering kan du missa en mobil webbpositions effekt på skrivbordskonverteringar, eller så kan den bli nedgrävd om de flesta av dina användare konverterar på datorn och inte på mobilwebben.

* Annonser - Upptäck vilka annonser som genererar högre konverteringar och kvantifiera deras värde och effekt i både webbläsare och mobilappsmiljöer.

* Webbplatser - Optimera för olika sajter i stället för att helt utesluta sajter manuellt. Om en webbplats driver konverteringar mellan olika enheter kan du se på vilka enheter detta beteende gäller.

* Erbjudanden - Förbättra den manuella optimeringen genom att kontrollera vilka lagererbjudanden som ger konverteringar mellan olika enheter och sedan avgöra om ni bör utöka er målinriktning för att inkludera fler enheter och kanaler i dessa avtal.

>[!MORELIKETHIS]
>
>* [Rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
