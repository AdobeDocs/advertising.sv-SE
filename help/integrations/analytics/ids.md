---
title: Adobe Advertising ID som används av  [!DNL Analytics]
description: Adobe Advertising ID som används av  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Adobe Advertising ID som används av [!DNL Analytics]

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

*Gäller för Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising använder två ID:n för prestandaspårning på plats: *EF ID* och *AMO ID*.

När ett annonsintryck inträffar skapar Adobe Advertising värdena för AMO-ID och EF-ID och lagrar dem. När en besökare som har sett en annons komma in på webbplatsen utan att klicka på en annons, anropar [!DNL Analytics] dessa värden från Adobe Advertising via JavaScript-koden [!DNL Analytics for Advertising]. För genomsynstrafik genererar [!DNL Analytics] ett extra ID (`SDID`) som används för att sammanfoga EF-ID och AMO-ID till [!DNL Analytics]. För genomklickningstrafik inkluderas dessa ID:n i landningssidans URL med hjälp av frågesträngsparametrarna `ef_id` och `s_kwcid` (för AMO ID).

Adobe Advertising skiljer mellan klickbara eller genomskinliga poster på webbplatsen enligt följande kriterier:

* En genomsiktspost hämtas när en användare besöker webbplatsen efter att ha visat en annons, men inte klickat på den. [!DNL Analytics] spelar in en genomgång om två villkor uppfylls:

   * Besökaren har inga klickningar för en [!DNL DSP] eller [!DNL Search, Social, & Commerce] annons under [klickningsfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * Besökaren har sett minst en [!DNL DSP] annons under [visningsfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc). Det sista intrycket skickas som en genomgång.

* En klickbar post hämtas när en besökare klickar på en annons innan han/hon kommer in på webbplatsen. [!DNL Analytics] hämtar en klickfrekvens när något av följande inträffar:

   * URL:en innehåller ett EF-ID och AMO-ID som har lagts till i Adobe Advertising-URL:en för landningssidan.

   * URL:en innehåller inga spårningskoder, men Adobe Advertising JavaScript-koden hittar ett klick under de senaste två minuterna.

![Adobe Advertising vybaserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figur 1: Adobe Advertising vybaserad [!DNL Analytics] integrering*

![Adobe Advertising klickar på URL-baserad [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figur 2: Adobe Advertising klickar på URL-baserad [!DNL Analytics] integrering*

## Adobe Advertising EF ID:n

{{$include /help/_includes/ef-id.md}}

### EF ID-format {#ef-id-formats}

{{$include /help/_includes/ef-id-formats.md}}

### EF ID Dimension i [!DNL Analytics]

I [!DNL Analytics]-rapporter kan du hitta EF ID-data genom att söka efter dimensionen [!UICONTROL EF ID] och använda måttet [!UICONTROL EF ID Instance].

EF ID:n omfattas av den unika identifierargränsen på 500 kB i Analysis Workspace. När 500 kB-värdet har nåtts rapporteras alla nya spårningskoder under rubriken [!UICONTROL Low Traffic] för radartikel. Eftersom det är möjligt att rapportens följsamhet saknas klassificeras inte dessa ID:n, och du bör inte använda dem för segment eller rapportering i [!DNL Analytics].

## ADOBE ADVERTISING AMO ID {#amo-id}

{{$include /help/_includes/amo-id.md}}

## AMO ID-format {#amo-id-formats}

{{$include /help/_includes/amo-id.md}}

### Sätt att implementera AMO-ID {#amo-id-implement}

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) När infogningsfunktionen på serversidan implementeras.

   * DSP-kunder: Pixelservern lägger automatiskt till parametern s_kwcid i landningssidans suffix när en användare tittar på en displayannons med Adobe Advertising pixel.

   * Sök-, sociala och Commerce-kunder:

      * För [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton med inställningen [!UICONTROL Auto Upload] aktiverad för kontot eller kampanjen, lägger pixelservern automatiskt till parametern s_kwcid i landningssidans suffix när en slutanvändare klickar på en annons med Adobe Advertising pixel.

      * För andra annonsnätverk, eller för [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton med inställningen [!UICONTROL Auto Upload] inaktiverad, lägger du manuellt till parametern i [på kontonivå-tilläggsparametrarna](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den till dina bas-URL:er.

* När infogningsfunktionen på serversidan inte är implementerad:

   * DSP-kunder: I [JavaScript-koden](javascript.md) registreras klickningar och genomgångar automatiskt. När en webbläsare inte stöder cookies från tredje part kan du fortfarande spåra klickbaserade konverteringar för följande annonstyper:

      * För [!DNL Flashtalking]-annonstaggar infogar du ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] makron till [!DNL Flashtalking] Lägg till taggar](/help/integrations/analytics/macros-flashtalking.md)&quot;. **Obs!** Den här proceduren är inte nödvändig om din organisation har ett direkt samarbete med [!DNL Flashtalking] och du använder datappassmakron för att spåra parametrarna `s_kwcid` och `ef_id` enligt [!DNL Flashtalking] supportdokumentationen på [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) .

      * För [!DNL Google Campaign Manager 360]-annonstaggar infogar du ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] makron till [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;.

   * Sök-, sociala och Commerce-kunder:

      * För annonser ([!DNL Google Ads] och [!DNL Microsoft Advertising]) lägger du manuellt till parametern AMO ID i landningssidans suffix, helst på [kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, såvida inte olika spårning för enskilda kontokomponenter krävs.

      * För annonser i alla andra annonsnätverk lägger du till AMO ID-parametern manuellt i [tilläggsparametrarna på kontonivå](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, som lägger till den i dina bas-URL:er.

Om du vill implementera infogningsfunktionen på serversidan, eller fastställa det bästa alternativet för ditt företag, pratar du med ditt Adobe-kontoteam.

### AMO ID Dimension i [!DNL Analytics]

I analysrapporter kan du hitta AMO ID-data genom att söka efter dimensionen [!UICONTROL AMO ID] och använda måttet [!UICONTROL AMO ID Instances]. Dimensionen [!UICONTROL AMO ID] lagrar alla infångade AMO ID-värden, medan måttet [!UICONTROL AMO ID Instances] anger hur ofta ett AMO ID-värde hämtades av webbplatsen. Om till exempel samma sökannons klickades fyra gånger men Analytics spårade sju webbplatsposter, skulle [!UICONTROL AMO ID Instances] vara sju (7) och [!UICONTROL Clicks] skulle vara fyra (4).

För alla rapporter och granskningar inom [!DNL Analytics] är det bästa sättet att använda AMO-ID tillsammans med motsvarande instans. Mer information finns i &quot;[Genomklickningsdataverifiering för [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; i &quot;Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising&quot;.

## Om analysklassificeringar

I [!DNL Analytics] är en [klassificering](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=sv-SE) en del metadata för en viss spårningskod, till exempel Konto, Kampanj eller Annons. Adobe Advertising kategoriserar Adobe Advertising-rådata med hjälp av klassificeringar så att du kan visa data på olika sätt (t.ex. efter annonstyp eller Campaign) när du genererar rapporter. Klassificeringar utgör grunden för Adobe Advertising-rapportering i [!DNL Analytics] och kan användas med AMO-mått, som [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] och [!UICONTROL AMO Clicks], samt med anpassade och standardbaserade händelser på plats som [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] och [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising](data-variances.md)
