---
title: JavaScript-kod för  [!DNL Analytics for Advertising]
description: JavaScript-kod för  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# JavaScript-kod för [!DNL Analytics for Advertising]

*Annonsörer med endast Advertising DSP*

För Advertising DSP spårar integreringen av [!DNL Analytics for Advertising] genom-vy- och klickfrekvens-interaktioner. Klickningsbesök spåras av Adobe Analytics-standardkoden på dina webbsidor. Koden [!DNL Analytics] hämtar parametrarna för AMO-ID och EF-ID i landningssidans URL och spårar dem i deras respektive reserverade [!DNL eVars] . Du kan spåra besök genom att distribuera ett JavaScript-fragment på dina webbsidor.

På den första sidan av besöket på webbplatsen kontrollerar Adobe Advertising JavaScript-koden om besökaren tidigare har sett eller klickat på en annons. Om användaren tidigare har kommit in på webbplatsen via en klickning eller inte har sett någon annons, ignoreras besökaren. Om besökaren har sett en annons och inte har öppnat webbplatsen via ett klick i [klickningsfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc) i Adobe Advertising, använder Adobe Advertising JavaScript-koden antingen a) [Experience Cloud ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/home.html) för att generera ett extra ID (`SDID`) eller b) Adobe Experience Platform [!DNL Web SDK] `generateRandomID` -metoden för att generera `[!DNL StitchID]`. Båda ID:n används för att knyta data från Adobe Advertising till besökarens Adobe Analytics-träff. Adobe Analytics frågar sedan Adobe Advertising efter det AMO-ID och EF-ID som är kopplat till annonsexponeringen. AMO-ID:t och EF-ID:n fylls sedan i i deras respektive [!DNL eVars]. Dessa värden gäller under en angiven period (som standard 60 dagar).

[!DNL Analytics] skickar statistik om webbplatstrafiken (t.ex. sidvisningar, besök och hur lång tid som har ägnats åt den) och eventuella anpassade [!DNL Analytics]-händelser eller standardhändelser till Adobe Advertising per timme, med EF-ID som nyckel. Dessa [!DNL Analytics]-mått körs sedan genom Adobe Advertising-attribueringssystemet för att ansluta konverteringarna till klicknings- och exponeringshistoriken.

>[!NOTE]
>
>Spårningslogiken i Adobe Advertising JavaScript finns på Adobe och påverkar därmed inte sidans inläsningstid.
>
>Logiken för dataanslutningen [!DNL DCM] till [!DNL Analytics] (med [!DNL Google Campaign Manager 360]) för Advertising DSP finns däremot på klientsidan. Klientsidans sammanslagning saktar ned sidbelastningen och ökar risken för dataförlust. Detta inträffar eftersom [!DNL Analytics] JavaScript måste pinga [!DNL DoubleClick] och vänta på att [!DNL DoubleClick] ska skicka tillbaka de senaste klicknings-/visningsdata till [!DNL Analytics]. När ditt [!DNL DSP]-team konfigurerar dataanslutningen [!DNL DCM] måste du ange hur länge du vill fördröja sidan.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Distribuera JavaScript Code

JavaScript-biblioteket består av två rader som gör att [!DNL Analytics] och Adobe Advertising kan kommunicera med varandra. Om integreringen av [!DNL Analytics for Advertising] slutfördes under implementeringen av Adobe Advertising bör du redan ha fått den här koden med instruktioner om hur den ska distribueras.

### Koden

#### Implementeringar som använder Experience Cloud-identitetstjänstens `visitorAPI.js`-kod

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`-koden

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Placera koden där

JavaScript-funktionen [!DNL Analytics for Advertising] måste komma efter Experience Cloud ID-tjänsten men före Analytics App Measurement-koden. Detta garanterar att det extra ID:t (`SDID`) eller `[!DNL StitchID]` inkluderas i ditt Analytics-anrop.

![Kodplacering](/help/integrations/assets/a4adc-code-placement.png)

### Verifierar koddistribution

Du kan utföra valideringen med valfri typ av verktyg för paketkodsnuttar (till exempel [!DNL Charles], [!DNL Fiddler] eller [!DNL Chrome Developer Tools]) genom att jämföra värdena för de fyra ID:n mellan begäran som går till Adobe Advertising och begäran som går till [!DNL Analytics] enligt instruktionerna nedan.

#### Bekräfta koden med [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öppna [!DNL Chrome Developer Tools] och klicka på fliken **Nätverk**.

1. Läs in en webbsida som innehåller JavaScript:n [!DNL Analytics for Advertising].

1. Filtrera fliken [!UICONTROL Network] efter `last` och granska två rader:

   ![Filtrerar senast](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Den första raden är anropet till JavaScript-biblioteket och kallas `last-event-tag-latest.min.js`.
   * Den andra raden är det samtal som skickar begäran till Adobe Advertising. Det börjar så här: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Om du inte ser samtalet till Adobe Advertising kanske det inte är den första sidvyn av ditt besök. I testsyfte kan du ta bort cookien så att nästa anrop blir den första sidvyn för motsvarande besök:

   1. På fliken Program letar du reda på cookien `adcloud` och kontrollerar att cookien innehåller `_les_v` (senaste besök) med värdet `y` och en UTC-epok som förfaller om 30 minuter.
      1. Ta bort cookien `adcloud` och uppdatera sidan.

1. (Implementeringar som använder Experience Cloud-identitetstjänstens `visitorAPI.js`-kod) filter på `/b/ss` för att se Analytics-träffen.

   ![Filtrerar på `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`code) Filter på `/interact` för att verifiera att nyttolasten för begäran till Edge Network innehåller `advertisingStitchID`.

   ![Filtrerar på `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Jämför ID-värdena mellan de två träffarna. Alla värden ska finnas i frågesträngsparametrar förutom för rapportsvitens-ID i Analytics-träffen, som är URL-sökvägen omedelbart efter `/b/ss/`.

   | ID | Analysparameter | Edge Network | Adobe Advertising-parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS-organisation | `mcorgid` |  | `_les_imsOrgid` |
   | Kompletterande data-ID | sdid |  | `_les_sdid` |
   | Häftnings-ID | stitchId | `advertisingStitchID` under egenskapen `_adcloud` |  |
   | Analytics Report Suite | Värdet efter `/b/ss/` | | `_les_rsid` |
   | Experience Cloud Visitor-ID | mitten |  | `_les_mid` |

   Om ID-värdena matchar varandra bekräftas JavaScript-implementeringen. Adobe Advertising skickar eventuella klicknings- eller vyspårningsdetaljer till [!DNL Analytics]-servern, om sådana finns.

#### Bekräfta koden med [!DNL Adobe Experience Cloud Debugger]

1. Öppna [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) på din hemsida.
1. Gå till fliken [!UICONTROL Network].
1. Klicka på [!UICONTROL Adobe Advertising] och [!UICONTROL Analytics] i verktygsfältet [!UICONTROL Solutions Filter].
1. Gå till `lasteventf-tm.everesttech.net` i parameterraden [!UICONTROL Request URL - Hostname].
1. Granska genererade signaler på raden [!UICONTROL Request - Parameters], liknande steg 3 i &quot;[Bekräfta koden med  [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implementeringar som använder koden för Experience Cloud-identitetstjänsten `visitorAPI.js`) Kontrollera att parametern `Sdid` matchar parametern `Supplemental Data ID` i Adobe Analytics-filtret.
   * (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js` -koden) Kontrollera att värdet för `advertisingStitchID` -parametern matchar det `Sdid` som skickas till Experience Platform Edge Network.
   * Om koden inte genereras kontrollerar du att cookien Adobe Advertising har tagits bort på fliken [!UICONTROL Application]. Uppdatera sidan och upprepa processen när den har tagits bort.

   ![Granskar [!DNL Analytics for Advertising] JavaScript-kod i [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Krav och nyckelinformation för implementering [!DNL Analytics for Advertising]](prerequisites.md)
