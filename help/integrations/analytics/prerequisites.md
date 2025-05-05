---
title: Krav och nyckelinformation för implementering av  [!DNL Analytics for Advertising]
description: Krav och nyckelinformation för implementering av  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Krav och nyckelinformation för implementering av [!DNL Analytics for Advertising]

*Annonsörer med Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Granska följande information innan du integrerar Adobe Advertising med Adobe Analytics.

## Krav för rapportering av Adobe Advertising-data i [!DNL Analytics]

* Något av följande:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.0 eller senare
* Alla versioner av Adobe Analytics (inklusive [!DNL Prime], [!DNL Premium] eller [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` version 2.1 eller senare
* (Advertising DSP-kunder) Ett [Advertising DSP JavaScript-utdrag](javascript.md) som distribueras på dina webbsidor för att spåra visningar.

>[!TIP]
>
>Använd den senaste versionen av varje bibliotek för att förbättra datakvaliteten.

## Krav för delning av analyssegment med Adobe Advertising

* Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.1 eller senare
* Adobe Analytics: `appMeasurement.js` version 1.8 eller senare

## Krav för rapportering av [!DNL Analytics]-data i Adobe Advertising

Ge Adobe Advertising implementeringsteamet följande:

* [!DNL Analytics]-rapportsvitens-ID som ska användas för rapportering av betalmediaaktivitet och för matning av webbplatsaktivitet för optimering och rapportering i Adobe Advertising
* Företagets organisations-ID (Org-ID) för Experience Cloud.

Du hittar båda dessa ID:n på fliken [Sammanfattning i Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=sv-SE).

![Sammanfattningsskärm för Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] data i Adobe Advertising {#lookback-a4adc}

Eftersom [!DNL Analytics]-data skickas till Adobe Advertising för rapportering och optimering omfattas data av attribueringsreglerna, inklusive utseendet och klickningsfönster, som är konfigurerade för annonsören i Adobe Advertising.

![inställningar för visningsfönster på annonsnivå i Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-attribueringsklickningsfönster: Det antal dagar efter att den första klickningen inträffar där klickningen kan kopplas till en konvertering. Som standard är det här värdet 60 dagar. Det högsta värdet är 90 dagar.
* Adobe Advertising-fönster för visningssökning efter attribuering: Det antal dagar efter ett annonsintryck som kan tilldelas en konvertering. Som standard är det här värdet 14 dagar. Det högsta värdet är 30 dagar

  >[!NOTE]
  >
  > Fönstret för visningssökning är specifikt för Adobe Advertising, inte för [!DNL Analytics for Advertising], och rapporterar.

JavaScript [!DNL Analytics for Advertising] använder de här inställningarna för att avgöra hur långt tillbaka en genomskinlig eller klickbar post till webbplatsen ska vara giltig. Mer information om hur du kan se genomgångar och klickningar finns i &quot;[Adobe Advertising ID:n som används av Analytics](ids.md)&quot;.

## Adobe Advertising data i [!DNL Analytics]

[!DNL Analytics] ställer in Adobe Advertising ID:n (AMO ID:n) i Analytics-träffen, enligt annonsörens [!DNL eVar]-beständighetsinställning, som gäller både klickningar och genomvisningar. Inställningen för beständighet konfigureras på baksidan av Adobe Advertising och din kontogrupp på Adobe kan ändra den.

* [!DNL Analytics for Advertising] [!DNL eVar] förfaller: 60 dagar som standard för AMO-ID:n

>[!NOTE]
>
>Om du vill segmentera data för en annan tidsram kan du [konfigurera anpassade segment](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=sv-SE) med olika uppslagsfönster i Analysis Workspace.

## Annonsmiljöer som stöds

* Sök
* Visa
* Video
* Online-video
* Ansluten TV
* Inbyggt

Kontakta kontoteamet på Adobe för att få de senaste annonsmiljöerna som stöds i varje kanal.

## Saker att känna till innan du implementerar

* Implementeringsteamet på Adobe Advertising ställer upp integreringen.

* Inga ytterligare kostnader debiteras för den här integreringen och serveranrop leder inte heller till ytterligare [!DNL Analytics]- eller Adobe Advertising-avgifter.

* [!DNL Analytics for Advertising] är en annonsserveragnostikversion: en genomgång eller klickning kan inträffa från vilken annonsserver som helst, och rätt ID:n genereras vid webbplatsposten.

* Integreringen skickar bara [!DNL Analytics] standard- och anpassade händelser till Adobe Advertising för att optimera antalet köpta medier och annonsaktiviteter. Det skickar inte [!DNL Analytics] segment, beräknade värden och [!DNL eVars] till Adobe Advertising för anbudsoptimering.

* Adobe Advertising skapar beständiga ID:n inom [!DNL Analytics] baserat på den senaste annonsen som klickades eller visades innan användaren kom in på webbplatsen, baserat på de [klicknings- och vysökningsfönster](#lookback-a4adc) som konfigurerats i Adobe Advertising. Om en besökare har båda typerna av webbplatsposteringsinteraktioner i sin profil, och klickningen är inom uppslagsperioden, åsidosätter besökarens klicknings-ID visnings-ID:t för platsrapportering.

* Konverteringsspårning för [!DNL Analytics for Advertising] i Adobe Analytics använder ett konfigurerbart uppföljningsfönster (60 dagar som standard). Adobe Advertising-rapporter återspeglar webbplatskonverteringar och engagemang i slutet av detta uppföljningsfönster.

* Alla annonstyper stöds. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] konverteringar spåras för närvarande och tilldelas bara till en besökare på samma enhet.

* [!DNL Analytics for Advertising] stöder inte konverteringar i appvyn.

* Vyspårning stöds inte för annonsörer som använder en vidarebefordringsimplementering på serversidan av [!DNL Analytics].

### Kompletterande ID

När identitetstjänsten Experience Cloud har implementerats för en webbplats innehåller träffar som innehåller data från [!DNL Analytics] eller Adobe Advertising ett extra ID.

Exempel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

För korrekt dataintegrering måste alla Adobe Advertising-anrop som används av en [!DNL Analytics for Advertising]-aktivitet för att leverera innehåll eller registrera målmåttet ha en motsvarande [!DNL Analytics]-träff som delar samma extra ID.

När du felsöker i [!DNL Analytics] måste du kontrollera att det extra ID:t finns för [!DNL Analytics] träffar. I [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=sv-SE) kan du se detta ID på fliken Adobe Advertising som `sdid` -parameter.

>[!NOTE]
>
> Den här implementeringen fungerar på liknande sätt som [!DNL Analytics for Target]-integreringen.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
