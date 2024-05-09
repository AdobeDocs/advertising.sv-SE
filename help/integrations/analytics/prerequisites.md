---
title: Krav och viktig information för implementering [!DNL Analytics for Advertising]
description: Krav och viktig information för implementering [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Krav och viktig information för implementering [!DNL Analytics for Advertising]

*Annonsörer med DSP och[!DNL Advertising Search, Social, & Commerce]*

Granska följande information innan du integrerar Adobe Advertising med Adobe Analytics.

## Krav för rapportering av data från Adobe Advertising i [!DNL Analytics]

* Något av följande:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.0 eller senare
* Alla versioner av Adobe Analytics (inklusive [!DNL Prime], [!DNL Premium], eller [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` version 2.1 eller senare
* (DSP kunder) och [Advertising DSP JavaScript snippet](javascript.md) på webbsidorna för att spåra besök.

>[!TIP]
>
>Använd den senaste versionen av varje bibliotek för att förbättra datakvaliteten.

## Krav för delning av analyssegment med Adobe Advertising

* Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.1 eller senare
* Adobe Analytics: `appMeasurement.js` version 1.8 eller senare

## Rapporteringskrav [!DNL Analytics] Data i Adobe Advertising

Ge Adobe Advertising implementeringsteamet följande:

* The [!DNL Analytics] Rapportera programsvit-ID som ska användas för rapportering av betalmedieaktivitet och för matning av webbplatsaktivitet för optimering och rapportering i Adobe Advertising
* Företagets organisations-ID (Org-ID) för Experience Cloud.

Du hittar båda dessa ID:n på [Fliken Sammanfattning i Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Sammanfattningsskärmen för Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Data i Adobe Advertising {#lookback-a4adc}

För [!DNL Analytics] data skickas till Adobe Advertising för rapportering och optimering. Dessa data omfattas av attribueringsreglerna, inklusive vilka fönster som är konfigurerade för annonsören i Adobe Advertising, där man kan läsa och klicka.

![inställningar för visningsfönster på annonsnivå i Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-attribueringsklickningsfönster: Det antal dagar efter att den första klickningen inträffar där klickningen kan kopplas till en konvertering. Som standard är det här värdet 60 dagar. Det högsta värdet är 90 dagar.
* Adobe Advertising-fönster för visningssökning efter attribuering: Det antal dagar efter ett annonsintryck som kan tilldelas en konvertering. Som standard är det här värdet 14 dagar. Det högsta värdet är 30 dagar

  >[!NOTE]
  >
  > Fönstret för visningssökning är specifikt för Adobe Advertising, inte [!DNL Analytics for Advertising], rapporter.

The [!DNL Analytics for Advertising] JavaScript använder dessa inställningar för att avgöra hur långt tillbaka en genomskinlig post eller klickbar post till webbplatsen ska vara giltig. Mer information om hur du ser genom- och genomklickningar finns i &quot;[Adobe Advertising ID som används av Analytics](ids.md).&quot;

## Adobe Advertising data i [!DNL Analytics]

[!DNL Analytics] ställer in Adobe Advertising ID:n (AMO ID:n) i Analytics-träffen, enligt annonsörens [!DNL eVar] beständighetsinställning, som gäller både klickningar och genomskinlighet. Inställningen för beständighet konfigureras på baksidan av Adobe Advertising och din kontogrupp på Adobe kan ändra den.

* [!DNL Analytics for Advertising] [!DNL eVar] förfallodatum: 60 dagar som standard för AMO-ID:n

>[!NOTE]
>
>Om du vill segmentera data för en annan tidsram kan du [skapa anpassade segment](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) med olika fönster för uppslag i Analysis Workspace.

## Annonsmiljöer som stöds

* Sök
* Visa
* Video
* Online-video
* Inbyggt

Kontakta kontoteamet på Adobe för att få de senaste annonsmiljöerna som stöds i varje kanal.

## Saker att känna till innan du implementerar

* Implementeringsteamet på Adobe Advertising kommer att konfigurera integreringen.

* Inga extra kostnader debiteras för den här integreringen och serveranrop leder inte heller till ytterligare [!DNL Analytics] eller avgifter från Adobe Advertising.

* [!DNL Analytics for Advertising] är annonsserveragnostiker: en genomskinlig eller klickbar-igenom-funktion kan komma från vilken annonsserver som helst, och rätt ID:n genereras vid webbplatsinmatning.

* Integreringen godkänns endast [!DNL Analytics] standardhändelser och anpassade händelser till Adobe Advertising för att optimera antalet köpta medier och annonssatsningar. Det går inte [!DNL Analytics] segment, beräknade värden, och [!DNL eVars] till Adobe Advertising för anbudsoptimering.

* Adobe Advertising skapar beständiga ID:n i [!DNL Analytics] baserat på den senaste annonsen som klickades eller visades innan användaren kom in på webbplatsen, baserat på [klicka och visa sökningsfönster](#lookback-a4adc) konfigurerat i Adobe Advertising. Om en besökare har båda typerna av webbplatsposteringsinteraktioner i sin profil, och klickningen är inom uppslagsperioden, åsidosätter besökarens klicknings-ID visnings-ID:t för platsrapportering.

* [!DNL Analytics for Advertising] Vid konverteringsspårning i Adobe Analytics används ett konfigurerbart uppföljningsfönster (60 dagar som standard). Adobe Advertising-rapporter återspeglar webbplatskonverteringar och engagemang i slutet av detta uppföljningsfönster.

* Alla annonstyper stöds. Alla annonsmiljöer stöds dock inte.

  Annonser för uppkopplad TV (CTV) spåras till exempel inte eftersom det inte finns några klick i CTV och inga konverteringar kan ske på samma enhet. Men om annonsen visas i en skrivbordsmiljö kan vissa data för genomskinlig webbplatspost spåras.

* [!DNL Analytics] konverteringar spåras för närvarande och tilldelas endast en besökare på samma enhet.

* [!DNL Analytics for Advertising] saknar stöd för konverteringar i appvyn.

* Direktspårning stöds inte för annonsörer som använder en serversidesimplementering av [!DNL Analytics].

### Kompletterande ID

När identitetstjänsten Experience Cloud har implementerats för en webbplats träffar som innehåller data från [!DNL Analytics] eller Adobe Advertising innehåller ett extra ID.

Exempel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

För korrekt dataintegrering används alla Adobe Advertising-anrop av en [!DNL Analytics for Advertising] aktivitet för att leverera innehåll eller registrera målmåttet måste ha en motsvarande [!DNL Analytics] en träff som delar samma extra ID.

När du felsöker i [!DNL Analytics]måste du bekräfta att det kompletterande ID:t finns för [!DNL Analytics] träffar. I [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)kan du se det här ID:t på fliken Adobe Advertising som `sdid` parameter.

>[!NOTE]
>
> Den här implementeringen fungerar ungefär som [!DNL Analytics for Target] integrering.

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
