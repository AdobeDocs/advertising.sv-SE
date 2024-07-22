---
title: Förväntade datavarianser mellan  [!DNL Analytics]  och Adobe Advertising
description: Förväntade datavarianser mellan  [!DNL Analytics]  och Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: e1c1d43c7fe5f44e34ada7dee09afd77f1b3f305
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Annonsörer med integreringsspåret [!DNL Analytics for Advertising] <!-- (A4AdC) --> har betalat annonser via Adobe Advertising och Adobe Analytics. När ni spårar media, kampanjer och kanaler via flera system matchar sällan samma datauppsättningar från olika system helt. I det här dokumentet beskrivs hur du bör förvänta dig att data för media som har sålts via Adobe Advertising ska jämföras med data i de olika system där mediet spåras i [!DNL Analytics].

>[!NOTE]
>
>Det här dokumentet fokuserar på Adobe Advertising och Analytics, men många av de viktigaste punkterna kan också överföras till andra spårningslösningar.

## Attributionsskillnader i liknande rapporter

### Olika Lookback-fönster och attribueringsmodeller

Integreringen av [!DNL Analytics for Advertising] använder två variabler ([!DNL eVars] eller [!DNL rVars] \[reserverad [!DNL eVars]]\) för att hämta [EF-ID och AMO-ID](ids.md). Variablerna konfigureras med ett enda uppslagsfönster (den tid som klickningar och genomgångar tilldelas) och en attribueringsmodell. Om inget annat anges konfigureras variablerna så att de matchar standardfönstret för klickning på annonsnivå och attribueringsmodellen i Adobe Advertising.

Uppslagsfönster och attribueringsmodeller kan dock konfigureras i både Analytics (via [!DNL eVars]) och Adobe Advertising. I Adobe Advertising är attribueringsmodellen dessutom konfigurerbar inte bara på annonsörsnivå (för anbudsoptimering) utan också inom enskilda datavyer och rapporter (endast för rapportering). En organisation kanske föredrar att använda den jämna distributionsattribueringsmodellen för optimering, men använder den senaste touchattribueringen för rapporter i Advertising DSP eller [!DNL Advertising Search, Social, & Commerce]. Om du ändrar attribueringsmodeller ändras antalet konverteringar.

Om ett rapportsökningsfönster eller en attribueringsmodell ändras i en produkt och inte i en annan, visar samma rapporter från varje system distinkta data:

* **Exempel på avvikelser orsakade av olika uppslagsfönster:**

  Anta att Adobe Advertising har ett 60-dagars klickfönster och att [!DNL Analytics] har ett 30-dagars uppslagsfönster. Anta också att en användare kommer till webbplatsen via en Adobe Advertising-spårad annons, lämnar och sedan återgår till dag 45 och konverterar. Adobe Advertising attribuerar konverteringen till det ursprungliga besöket eftersom konverteringen inträffade inom 60-dagars uppslagsfönstret. [!DNL Analytics] kan dock inte attribuera konverteringen till det ursprungliga besöket eftersom konverteringen inträffade efter att 30-dagars uppslagsfönstret har gått ut. I det här exemplet rapporterar Adobe Advertising fler konverteringar än vad [!DNL Analytics] gör.

  ![Exempel på konverteringsattribut i Adobe Advertising, men inte [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exempel på avvikelser orsakade av olika attribueringsmodeller:**

  Anta att en användare interagerar med tre olika Adobe Advertising-annonser innan de konverterar, med intäkt som konverteringstyp. Om en Adobe Advertising-rapport använder en jämn distributionsmodell för attribuering, fördelas intäkterna jämnt över alla annonser. Om [!DNL Analytics] däremot använder den sista pekattribueringsmodellen, så attribueras intäkterna till den sista annonsen. I följande exempel tilldelar Adobe Advertising till sig 10 USD av de 30 USD som har tagits med i intäkter till var och en av de tre annonserna, medan [!DNL Analytics] tilldelar alla 30 USD i intäkter till den sista annonsen som visas av användaren. När du jämför rapporter från Adobe Advertising och [!DNL Analytics] kan du förvänta dig att se effekten av skillnaden i attribuering.

  ![Olika intäkter som har tilldelats Adobe Advertising och [!DNL Analytics] baserat på olika attribueringsmodeller](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Det bästa sättet är att använda samma uppslagsfönster och attribueringsmodell i både Adobe Advertising och [!DNL Analytics]. Samarbeta med kontoteamet på Adobe om det behövs för att identifiera de aktuella inställningarna och hålla konfigurationerna synkroniserade.

Samma koncept gäller alla andra kanaler som använder olika uppslagsfönster eller attribueringsmodeller.

#### Olika Lookback-fönster för vystyrningsspårning {#impression-lookback}

I Adobe Advertising baseras attribueringen på klick och visningar, och du kan konfigurera olika uppslagsfönster för klick och visningar. I [!DNL Analytics] baseras dock attribueringen på klickfrekvens och genomskinlighet, och du har inte möjlighet att ange olika attribueringsfönster för klickningar och genomvisningar. Spåra varje start vid det första webbplatsbesöket. Ett intryck kan göras samma dag eller flera dagar innan en genomgång sker, och tidpunkten kan påverka var attribueringsfönstret börjar i varje system.

Vanligtvis sker de flesta genomskinliga konverteringar tillräckligt snabbt för att båda systemen ska kunna attribuera krediter. Vissa konverteringar kan dock inträffa utanför uppslagsfönstret för Adobe Advertising men i uppslagsfönstret [!DNL Analytics]. Sådana konverteringar beror på genomgången i [!DNL Analytics] men inte på intrycket i Adobe Advertising.

Anta i följande exempel att en besökare fick en annons Dag 1, genomförde ett besök (dvs. besökte annonsens landningssida utan att tidigare klicka på annonsen) Dag 2 och konverterades Dag 45. I det här fallet skulle Adobe Advertising spåra användaren från dag 1-14 (med 14 dagars uppslag), [!DNL Analytics] skulle spåra användaren från dag 2-61 (med 60 dagars uppslag) och konverteringen dag 45 skulle tillskrivas annonsen inom [!DNL Analytics] men inte inom Adobe Advertising.

![Exempel på en konverteringsgrad för genomvisning i [!DNL Analytics] men inte Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

En annan orsak till diskrepanser är att du i Adobe Advertising kan tilldela visningskonverteringar en anpassad *genomsynlig vikt* som är relativ till den vikt som tilldelats en klickbaserad konvertering. Standardbredden för genomvyn är 40 %, vilket innebär att en genomsiktskonvertering räknas som 40 % av värdet för en klickbaserad konvertering. [!DNL Analytics] innehåller ingen sådan viktning av visningskonverteringar. En 100 USD-intäktsorder som hämtats in i [!DNL Analytics] diskonteras till exempel till 40 USD i Adobe Advertising om du använder standardgenomsynvikten - en skillnad på 60 USD.

Ta hänsyn till de här skillnaderna när du jämför vykonverteringar mellan Adobe Advertising och [!DNL Analytics] rapporter.

#### Tillgängliga attribueringsmodeller

| Adobe Advertising Attribution | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] allokering |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Använd inte* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>För linjär allokering attribuerar [!DNL Analytics] lyckade händelser jämnt över alla [!DNL eVar] -värden inom ett enda besök, så använd linjär allokering med ett [!DNL eVar]-förfallodatum på&quot;Besök&quot;. För annonsering leder emellertid användningen av linjär attribuering till en allokering som inte är helt linjär och till mindre än-idealisk rapportering. Om en besökare till exempel interagerar med tre annonser innan de konverterar till tre separata besök, tillskrivs bara den annons som sågs vid det senaste besöket konverteringen, inte alla tre annonserna.
>
>Dessutom förhindrar en växling av konverteringsallokering till eller från &quot;Linjär&quot; att historiska data visas, vilket kan leda till felaktiga data i rapporter. Linjärt allokering kan till exempel dela intäkten över ett antal olika [!DNL eVar]-värden. Om du ändrar allokeringen till&quot;Senaste&quot; kopplas 100 % av denna intäkt till det senaste enskilda värdet. Den här föreningen kan leda till felaktiga slutsatser.
>
>För att undvika missförstånd gör [!DNL Analytics] historiska data otillgängliga i rapporteringsgränssnittet. Du kan visa historiska data om du ändrar [!DNL eVar] tillbaka till den ursprungliga allokeringsinställningen, men du bör inte ändra [!DNL eVar] allokeringsinställningarna bara för att få tillgång till historiska data. Adobe rekommenderar att du använder en ny [!DNL eVar] när du vill använda en ny allokeringsinställning för data som redan spelas in, i stället för att ändra allokeringsinställningarna för en [!DNL eVar] som redan har en stor mängd historiska data.

En lista med [!DNL Analytics]-attribueringsmodeller och deras definitioner finns på [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Om du är inloggad på [!DNL Search, Social, & Commerce] kan du hitta en lista

* (Användare i Nordamerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alla andra användare) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attribut för händelsedatum i Adobe Advertising

I Adobe Advertising kan du rapportera konverteringsdata antingen efter det associerade klickdatumet/händelsedatumet (datumet för klickhändelsen eller tryckhändelsen) eller efter transaktionsdatumet (konverteringsdatumet). Konceptet för klicknings-/händelsedatumrapportering finns inte i [!DNL Analytics]. Alla konverteringar som spåras i [!DNL Analytics] rapporteras per transaktionsdatum. Därför kan samma konvertering rapporteras med olika datum i Adobe Advertising och [!DNL Analytics]. Tänk dig en användare som klickar på en annons den 1 januari och konverterar den 5 januari. Om du visar konverteringsdata per händelsemedatum i Adobe Advertising rapporteras konverteringen den 1 januari, när klickningen inträffade. I [!DNL Analytics] rapporteras samma konvertering den 5 januari.

![Exempel på en konvertering som har tilldelats olika datum](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

Med [[!DNL Analytics Marketing Channels] rapportering](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) kan du konfigurera regler för att identifiera olika marknadsföringskanaler baserat på distinkta aspekter av träffinformation. Du kan spåra kanaler som spåras i Adobe Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] och [!UICONTROL Paid Search]) som [!DNL Marketing Channels] genom att använda frågesträngsparametern `ef_id` för att identifiera kanalen. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Men även om [!DNL Marketing Channels]-rapporterna kan spåra Adobe Advertising-kanaler kanske data inte matchar Adobe Advertising-rapporterna av flera anledningar. Mer information finns i följande avsnitt.

>[!NOTE]
>
> Följande huvudbegrepp gäller också för flerkanalsspårning som omfattar kampanjer som inte spåras i Adobe Advertising, till exempel variabeln [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (kallas även spårningskod eller [!DNL eVar] 0) och anpassad [!DNL eVar]-spårning.

### Potentiellt annorlunda attributmodeller i [!DNL Marketing Channels]

De flesta [!DNL Marketing Channels]-rapporter har konfigurerats med [!UICONTROL Last Touch]-attribuering, som den senaste marknadsföringskanalen som identifieras tilldelas 100 % av konverteringsvärdet. Om du använder olika attribueringsmodeller för [!DNL Marketing Channels]-rapporterna och Adobe Advertising-rapporterna leder det till skillnader i de tilldelade konverteringarna.

### Ett potentiellt annorlunda fönster för återsökning i [!DNL Marketing Channels]

Uppslagsfönstret för [!DNL Marketing Channels] kan anpassas. I Adobe Advertising går det att konfigurera fönstret för klicksökning, men ett fast 60-dagarsfönster är vanligt. Om de två produkterna använder olika fönster för sökning kan du förvänta dig avvikelser i data.

### Annat kanalattribut i [!DNL Marketing Channels]

Adobe Advertising-rapporter fångar endast betalda medier som har handlats via Adobe Advertising (betald sökning för [!DNL Advertising Search, Social, & Commerce] annonser och visning för Advertising DSP-annonser), medan [!DNL Marketing Channels]-rapporter kan spåra alla digitala kanaler. Detta kan leda till en diskrepans i den kanal för vilken en konvertering görs.

Till exempel har betalsökningar och naturliga sökkanaler ofta en symbiotisk relation, där varje kanal hjälper den andra. Rapporten [!DNL Marketing Channels] attribuerar vissa konverteringar till naturlig sökning som Adobe Advertising inte gör eftersom den inte spårar naturlig sökning.

Överväg också en kund som visar en displayannons, klickar på en betald sökannons, klickar i ett e-postmeddelande och lägger sedan en 30 USD-order. Även om både Adobe Advertising och [!DNL Marketing Channels] använder den senaste pekattribueringsmodellen skulle konverteringen fortfarande tilldelas olika till var och en. Adobe Advertising har inte åtkomst till [!UICONTROL Email]-kanalen, så den skulle kreditera betald sökning för konverteringen. [!DNL Marketing Channels] har dock åtkomst till alla tre kanaler, så det skulle kreditera [!UICONTROL Email] för konverteringen.

![Exempel på olika konverteringsattribuering i Adobe Advertising jämfört med [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Mer information om varför mätvärdena kan variera finns i [Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).

## Skillnader i data i Adobe Analytics [!DNL Paid Search Detection]

Med funktionen [äldre [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) i [!DNL Analytics] kan företag [definiera regler för att spåra betald och organisk söktrafik](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) för angivna sökmotorer. Regler i [!DNL Paid Search Detection] använder både en frågesträng och den refererande domänen för att identifiera betald och naturlig söktrafik. [!DNL Paid Search Detection]-rapporterna ingår i den större gruppen med [Hitta metoder](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html)-rapporter, som förfaller antingen när en angiven händelse (till exempel en kundvagnsutcheckning) inträffar eller besöket avslutas.

Följande gränssnitt används för att skapa en [!DNL Paid Search Detection]-regeluppsättning:

![Exempel på en regel för identifiering av betald sökning i [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

De resulterande [!DNL Paid Search Detection]-rapporterna innehåller [!UICONTROL Paid Search Engine]-, [!UICONTROL Paid Search Keywords]-, [!UICONTROL Natural Search Engine]- och [!UICONTROL Natural Search Keywords]-rapporterna.

Observera följande två begränsningar med data i [!DNL Paid Search Detection]-rapporter:

* Rapporterna [!UICONTROL Paid Search Keywords] och [!UICONTROL Natural Search Keywords] visar sökfrågorna som identifieras av de refererande URL:erna, inte nyckelorden som användarna lägger bud på. Adobe Advertising- och [!DNL Analytics]-rapporter visar de faktiska nyckelorden, så vänta dig inte att de ska överensstämma med nyckelordsrapporterna för [!DNL Paid Search Detection].

* När funktionen [!DNL Paid Search Detection] ursprungligen skapades var den ursprungliga sökfrågan (teckensträngen som användaren angav i sökfältet i sökmotorn) mer lättillgänglig för annonsörer via den refererande URL:en. Idag är sökmotorer i stort sett otydliga med sökfrågan och nyckelordsrapporterna [!DNL Paid Search Detection] har ett begränsat värde eftersom de flesta frågedata är &quot;ospecificerade&quot;.

  Med [!DNL Analytics for Advertising] kan annonsörer fortfarande spåra betalda nyckelord i [!DNL Analytics]. Den refererande domänen informerar motorn om vilken sökmotor som körde trafiken. Eftersom den annonserarspecifika kontoinformationen inte är kopplad till den refererande domänen, listas all trafik under sökmotorn. Annonsörer med flera konton i samma sökmotor bör referera till Adobe Advertising eller [!DNL Analytics]-rapportering för kontospecifik rapportering.

### Varför konfigurera [!DNL Paid Search Detection]?

Med [!DNL Paid Search Detection]-rapporterna kan du identifiera naturlig söktrafik i [[!DNL Analytics Marketing Channels] rapporter](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Att separera betald söktrafik och naturlig söktrafik är ett bra sätt att förstå det värde som naturlig sökning tillför hela marknadsföringsekosystemet.

## Genomklickningsdataverifiering för [!DNL Analytics for Advertising] {#data-validation}

För integreringen bör du validera klickinformationen för att säkerställa att alla sidor på webbplatsen följer klickfrekvensen.

I [!DNL Analytics] är ett av de enklaste sätten att validera [!DNL Analytics for Advertising]-spårning att jämföra instanser med klickningar med hjälp av ett beräkningsmått för&quot;AMO ID Instances to Clicks&quot;, som beräknas enligt följande:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] representerar det antal gånger som [AMO-ID:n](ids.md) spåras på webbplatsen. Varje gång en annons klickas läggs en AMO-ID (`s_kwcid`)-parameter till på landningssidans URL. Antalet [!UICONTROL AMO ID Instances] motsvarar därför antalet klick och kan valideras mot faktiska annonsklickningar. Vi ser vanligtvis en matchningsfrekvens på 85 % för [!DNL Search, Social, & Commerce] och en matchningsfrekvens på 30 % för [!DNL DSP]-trafik (vid filtrering så att endast klickfrekvens [!UICONTROL AMO ID Instances] inkluderas). Skillnaden i förväntningarna mellan sökning och visning kan förklaras av det förväntade trafikbeteendet. Sökfunktionen hämtar avsikten, och som sådan har användarna vanligtvis för avsikt att klicka på sökresultaten från sin fråga. Användare som ser en webbannons eller en videoannons är mer benägna att klicka på annonsen oavsiktligt och sedan antingen hoppa från webbplatsen eller avbryta det nya fönster som läses in innan sidaktiviteten spåras.

I Adobe Advertising-rapporter kan du jämföra instanser med klickningar med hjälp av måttet [!UICONTROL EF ID Instances] i stället för [!UICONTROL AMO ID Instances]:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Du bör förvänta dig en hög matchningsfrekvens mellan AMO-ID och EF-ID, men vänta inte med 100 % paritet eftersom AMO-ID och EF-ID i grunden spårar olika data, och den här skillnaden kan leda till små skillnader i det totala antalet [!UICONTROL AMO ID Instances] och [!UICONTROL EF ID Instances]. Om det totala antalet [!UICONTROL AMO ID Instances] i [!DNL Analytics] skiljer sig från [!UICONTROL EF ID Instances] i Adobe Advertising med mer än 1 % kontaktar du Adobe Account Team för att få hjälp.

Mer information om AMO ID och EF ID finns i [Adobe Advertising ID:n som används av Analytics](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Felsöka skillnader mellan klick och instanser

Om [!UICONTROL EF ID Instances]-till-klickförhållandet är under 85 % ska du kontrollera följande:

* Saknar du klickspårning för kontot eller på någon undernivå, eller har du klickspårning (till exempel på både konto- och kampanjnivå)?

  I Sök, Socialt och Commerce [hämtar du ett kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) för kontot för att kontrollera spårnings-URL:er.

  I [!DNL Analytics] kan du även se om AMO-ID och EF IF har lagts till konsekvent med hjälp av ett [!DNL AMO ID] till [!DNL EF ID]-beräknat mått, vilket beräknas enligt följande:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Ett större värde än 100 % anger att fler EF-ID:n saknas än AMO-ID:n.

* Har landningssidan ett inläsningsproblem så att AMO-ID och EF-ID inte hämtas?

* Omdirigeras landningssidans URL så att AMO-ID och EF-ID går förlorade?

* Använder alla landningssidor den konfigurerade rapportsviten?

>[!NOTE]
>
>Teoretiskt sett är det möjligt att en instans har flera klick. Kontrollera om det finns några klick på olika enheter (till exempel datorer, mobiler och surfplattor).

## Jämför datauppsättningar i [!DNL Analytics for Advertising] med i Adobe Advertising

[AMO ID](ids.md) (frågesträngsparametern s_kwcid) används för rapportering i [!DNL Analytics] och [EF ID](ids.md) (frågesträngsparametern ef_id) används för rapportering i Adobe Advertising. Eftersom de är distinkta värden kan ett värde vara skadat eller inte läggas till på landningssidan.

Anta att vi har följande landningssida:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

där EF-ID är `test_ef_id` och AMO-ID är `test_amo_id`.

Om en omdirigering sker på en webbplats kan URL:en sluta på följande sätt:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

där EF-ID är `test_ef_id` och AMO-ID är `test_amo_id#redirectAnchorTag`.

I det här exemplet lägger tillägget av ankartaggen till oväntade tecken i AMO-ID:t, vilket resulterar i ett värde som inte känns igen i Analytics. Detta AMO-ID skulle inte klassificeras och konverteringar som är kopplade till det skulle hamna under [!UICONTROL unspecified] eller [!UICONTROL none] i [!DNL Analytics]-rapporter.

Men även om sådana här problem är vanliga så brukar de vanligtvis inte resultera i en hög procent skillnader. Men om du upptäcker en stor skillnad mellan AMO ID i [!DNL Analytics] och EF ID i Adobe Advertising kontaktar du Adobe Account Team för att få hjälp.

## Andra mätvärden

### Skillnaden mellan klick och besök {#clicks-vs-visits}

De verkar analoga, men klick och besök representerar olika data:

* **Klicka:** [!DNL DSP] eller så spelar sökmotorn in ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Besök:** [!DNL Analytics] definierar ett [besök](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) som en serie sidvisningar av en användare, som avslutas enligt ett av flera kriterier, t.ex. 30 minuters inaktivitet.

En klickning kan per definition leda till flera besök.

Tänk på följande exempel: Användare 1 och Användare 2 har båda åtkomst till en webbplats genom att klicka på en Adobe Advertising-annons. Användare 1 visar fyra sidor och går sedan ut för dagen, så det första klicket ger ett besök. Användare 2 tittar på två sidor, går till en 45-minuters lunch, återvänder, visar ytterligare två sidor och sedan går. I det här fallet resulterar den första klickningen i två besök.

![Exempel på skillnaden mellan klick och besök](/help/integrations/assets/a4adc-visits-example.png)

### Skillnaden mellan klick och genomklickningar

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klick och klickningar är två olika mätvärden:

* **Klicka:** [!DNL DSP] eller så spelar sökmotorn in ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Klickningar:** [!DNL Analytics] spelar in en klickfrekvens när besökaren kommer till målwebbplatsen, landningssidan läses in och [!DNL Analytics]-begäran längst ned på sidan skickar data till [!DNL Analytics].

Klickningar och klickningar kan skilja sig avsevärt på grund av oavsiktliga annonsklickningar. Vi har observerat att de flesta klick på displayannonser är oavsiktliga klick, och dessa oavsiktliga besökare trycker på knappen Bakåt innan landningssidan läses in, så [!DNL Analytics] kan inte spela in en klickning. Detta gäller särskilt annonser där en oavsiktlig klickning är mer sannolik, som mobilannonser, videoannonser och annonser som fyller skärmen och måste stängas innan användaren kan visa sidan.

Webbplatser som är inlästa på mobila enheter är också mindre benägna att resultera i klickningar på grund av lägre bandbredder eller tillgänglig processorkraft, vilket gör att landningssidor tar längre tid att läsa in. Det är inte ovanligt att 50-70 % av klickningarna inte leder till klickningar. I mobilmiljöer kan skillnaden vara så hög som 90 % på grund av kombinationen av en långsammare webbläsare och den större sannolikheten att användaren av misstag klickar på annonsen när han eller hon bläddrar igenom sidan eller försöker stänga annonsen.

Klickdata kan också spelas in i miljöer där klickningar inte kan spelas in med de nuvarande spårningsmekanismerna (t.ex. klick som kommer in i eller från en mobilapp) eller där annonsören bara använde en spårningsmetod (t.ex. med den genomskinliga JavaScript-metoden, webbläsare som blockerar cookies från tredje part spårar klickningar, men inte klickningar). En viktig orsak till att Adobe rekommenderar att man använder sig av både klicknings-URL:er och JavaScript-spårningsmetoder är att maximera täckningen av spårbara klickningar.

### Använda Adobe Advertising-trafikstatistik för Dimensioner utanför Adobe Advertising

Adobe Advertising förser Analytics med [reklamspecifika trafikdata och relaterade dimensioner från  [!DNL DSP]  och [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Mätvärdena som tillhandahålls av Adobe Advertising gäller endast de angivna Adobe Advertising-dimensionerna och data är inte tillgängliga för andra dimensioner i [!DNL Analytics].

Om du till exempel visar [!UICONTROL Adobe Advertising Clicks]- och [!UICONTROL Adobe Advertising Cost]-måtten per konto, som är en Adobe Advertising-dimension, visas summan [!UICONTROL Adobe Advertising Clicks] och [!UICONTROL Adobe Advertising Cost] per konto.

![Exempel på Adobe Advertising-mått i en rapport med en Adobe Advertising-dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Om du däremot visar måtten [!UICONTROL Adobe Advertising Clicks] och [!UICONTROL Adobe Advertising Cost] med en siddimension (till exempel Sida), som Adobe Advertising inte tillhandahåller data för, är [!UICONTROL Adobe Advertising Clicks] och [!UICONTROL Adobe Advertising Cost] för varje sida noll (0).

![Exempel på Adobe Advertising-mått i en rapport som använder en dimension som inte stöds](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Använder [!UICONTROL AMO ID Instances] som ersättning för klick med Dimensioner som inte är Adobe Advertising

Eftersom du inte kan använda [!UICONTROL AMO Clicks] med webbplatsdimensioner kan det vara bra att hitta en motsvarighet till klickningar. Det kan vara frestande att använda besök som ersättning, men det är inte det bästa alternativet eftersom varje besökare kan ha flera besök. (Se &quot;[Skillnaden mellan klick och besök](#clicks-vs-visits).&quot; Vi rekommenderar i stället att du använder [!UICONTROL AMO ID Instances], vilket är det antal gånger som AMO-ID:t hämtas. Även om [!UICONTROL AMO ID Instances] inte matchar [!UICONTROL AMO Clicks] exakt är de det bästa alternativet för att mäta klicktrafik på webbplatsen. Mer information finns i &quot;[Genomklickningsdataverifiering för [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Exempel på [!UICONTROL AMO ID Instances] i stället för [!UICONTROL Adobe Advertising Clicks] för en dimension som inte stöds](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising-mått i Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Varför data kan variera mellan Adobe Advertising och [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
