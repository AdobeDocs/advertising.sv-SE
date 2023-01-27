---
title: Förväntade datavariationer mellan [!DNL Analytics] och Adobe
description: Förväntade datavariationer mellan [!DNL Analytics] och Adobe
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '3276'
ht-degree: 0%

---

# Förväntade datavariationer mellan [!DNL Analytics] och Adobe

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

Annonsörer med [!DNL Analytics for Advertising] <!-- (A4AdC) --> integreringsspår för betald annonsering via Adobe Advertising och Adobe Analytics. När ni spårar media, kampanjer och kanaler via flera system matchar sällan samma datauppsättningar från olika system helt. I det här dokumentet beskrivs hur ni kan förvänta er att data för media som har sålts via Adobe-reklam ska jämföras med data i de olika system där mediet spåras i [!DNL Analytics].

>[!NOTE]
>
>Det här dokumentet fokuserar på Adobe-reklam och -analys, men många av de viktigaste punkterna kan också överföras till andra spårningslösningar.

## Attributionsskillnader i liknande rapporter

### Olika Lookback-fönster och attribueringsmodeller

The [!DNL Analytics for Advertising] integreringen använder två variabler (eVars eller rVars \[reserverade eVars]\) för att fånga upp [EF-ID och AMO-ID](ids.md). Variablerna konfigureras med ett enda uppslagsfönster (den tid som klickningar och genomgångar tilldelas) och en attribueringsmodell. Om inget annat anges konfigureras variablerna så att de matchar standardfönstret för klickning på annonsnivå och attribueringsmodellen i Adobe Advertising.

Uppslagsfönster och attribueringsmodeller kan dock konfigureras i både Analytics (via eVars) och Adobe Advertising. I Adobe Advertising är attribueringsmodellen konfigurerbar inte bara på annonsörsnivå (för budoptimering) utan också inom enskilda datavyer och rapporter (endast för rapportering). En organisation kan till exempel föredra att använda modellen för jämn fördelning för optimering, men använda den senaste beröringsattribueringen för rapporter i DSP eller [!DNL Advertising Search]. Om du ändrar attribueringsmodeller ändras antalet konverteringar.

Om ett rapportsökningsfönster eller en attribueringsmodell ändras i en produkt och inte i en annan, kommer samma rapporter från varje system att visa distinkta data:

* **Exempel på avvikelser orsakade av olika uppslagsfönster:**

   Anta att Adobe Advertising har ett 60-dagars klickfönster och [!DNL Analytics] har ett 30-dagars uppslagsfönster. Anta att en användare kommer till webbplatsen via en annonsering som spåras i Adobe, lämnar och sedan återgår på dag 45 och konverterar. Adobe Advertising kommer att attribuera konverteringen till det ursprungliga besöket eftersom konverteringen inträffade inom 60-dagars uppslagsfönstret. [!DNL Analytics]Men det går inte att attribuera konverteringen till det ursprungliga besöket eftersom konverteringen inträffade efter att 30-dagars uppslagsfönstret hade gått ut. I det här exemplet skulle Adobe Advertising rapportera ett högre antal konverteringar än [!DNL Analytics] skulle.

   ![Exempel på konvertering i Adobe-annonsering men inte [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exempel på avvikelser orsakade av olika attribueringsmodeller:**

   Anta att en användare interagerar med tre olika annonser från Adobe innan de konverterar, med intäkt som konverteringstyp. Om en Adobe Advertising-rapport använder en jämn distributionsmodell för attribuering, fördelas intäkterna jämnt över alla annonser. If [!DNL Analytics] använder den sista pekattribueringsmodellen, men då attribueras intäkterna till den sista annonsen. I följande exempel tillskriver Adobe Advertising ett värde på 10 USD av de 30 USD av intäkterna som tagits emot till var och en av de tre annonserna, medan [!DNL Analytics] tilldelar alla 30 USD av intäkter till den sista annansen som användaren ser. När du jämför rapporter från Adobe Advertising och [!DNL Analytics]kan du förvänta dig att se effekten av skillnaden i attribuering.

   ![Olika intäkter från Adobe-reklam och [!DNL Analytics] baserat på olika attribueringsmodeller](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Det bästa sättet är att använda samma uppslagsfönster och attribueringsmodell i både Adobe-annonsering och [!DNL Analytics]. Arbeta med dina [!DNL Adobe] kontogruppen efter behov för att identifiera de aktuella inställningarna och för att hålla konfigurationerna synkroniserade.

Samma koncept gäller alla andra kanaler som använder olika uppslagsfönster eller attribueringsmodeller.

#### Olika Lookback-fönster för vystyrningsspårning {#impression-lookback}

I Adobe Advertising baseras attribueringen på klick och visningar, och du kan konfigurera olika uppslagsfönster för klick och för visningar. I [!DNL Analytics]attribueringen bygger dock på klickfrekvens och genomskinlighet, och du har inte möjlighet att ange olika attribueringsfönster för klickningar och genomvisningar. spårning för varje start vid det första webbplatsbesöket. Ett intryck kan göras samma dag eller flera dagar innan en genomgång sker, vilket kan påverka var attribueringsfönstret börjar i varje system.

Vanligtvis sker de flesta genomskinliga konverteringar tillräckligt snabbt för att båda systemen ska kunna attribuera krediter. Vissa konverteringar kan dock inträffa utanför visningsfönstret för Adobe Advertising, men inom [!DNL Analytics] fönster; sådana konverteringar beror på genomgången [!DNL Analytics] men inte på intryck i Adobe Advertising.

Anta att en besökare fick en annons dag 1 i följande exempel, utförde ett besök (dvs. besökte annonsens landningssida utan att tidigare klicka på annonsen) dag 2 och konverterades dag 45. I det här fallet skulle Adobe Advertising spåra användaren från dag 1-14 (med 14-dagars uppslag), [!DNL Analytics] skulle spåra användaren från dag 2-61 (med 60 dagars uppslag) och konverteringen dag 45 skulle tillskrivas annonsen i [!DNL Analytics] men inte inom Adobe Advertising.

![Exempel på en konvertering av genomskinlig bild i [!DNL Analytics] men inte Adobe](/help/integrations/assets/a4adc-viewthrough-example.png)

En annan orsak till diskrepanser är att du i Adobe Advertising kan tilldela visningskonverteringar till anpassade *genomskinlig vikt* som är relativ till den vikt som tillskrivs en klickbaserad konvertering. Standardbredden för genomvyn är 40 %, vilket innebär att en genomsiktskonvertering räknas som 40 % av värdet för en klickbaserad konvertering. [!DNL Analytics] innehåller ingen sådan viktning av genomskinliga konverteringar. En 100 US-dollar-intäktsorder som hämtats in i [!DNL Analytics] kommer att diskonteras till 40 USD i Adobe-annonsering om du använder standardvyns genomvikt - en skillnad på 60 USD.

Ta hänsyn till dessa skillnader när du jämför vykonverteringar mellan Adobe-annonsering och [!DNL Analytics] rapporter.

#### Tillgängliga attribueringsmodeller

| Adobe Advertising Attribution | [!DNL Analytics] Attribut | eVar/rVar-allokering |
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
>För linjär tilldelning [!DNL Analytics] attribuerar framgångshändelser lika i alla eVar inom ett enda besök, så använd linjär allokering med en eVar som förfaller&quot;Besök&quot;. För annonsering leder emellertid användningen av linjär attribuering till en allokering som inte är helt linjär och till mindre än-idealisk rapportering. Om en besökare till exempel interagerar med tre annonser innan de konverterar till tre separata besök, tillskrivs bara den annons som sågs vid det senaste besöket konverteringen, inte alla tre annonserna.
>
>Dessutom förhindrar en växling av konverteringsallokering till eller från &quot;Linjär&quot; att historiska data visas, vilket kan leda till felaktiga data i rapporter. Linjärt allokering kan till exempel dela intäkten över ett antal olika eVar. Om du ändrar allokeringen till&quot;Senaste&quot; kopplas 100 % av denna intäkt till det senaste enskilda värdet. Den här föreningen kan leda till felaktiga slutsatser.
>
>För att undvika förvirring [!DNL Analytics] gör historiska data otillgängliga i rapporteringsgränssnittet. Du kan visa historiska data om du ändrar tillbaka eVar till den ursprungliga allokeringsinställningen, men du bör inte ändra eVar allokeringsinställningar bara för att få tillgång till historiska data. Adobe rekommenderar att du använder en ny eVar när du vill använda en ny allokeringsinställning för data som redan spelas in, i stället för att ändra allokeringsinställningarna för en eVar som redan har en stor mängd historiska data.

Se en lista med [!DNL Analytics] attribueringsmodeller och deras definitioner på [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Om du är inloggad [!DNL Search]hittar du en lista över attribueringsmodeller på
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Attribut för händelsedatum i Adobe-annonsering

I Adobe Advertising kan du rapportera konverteringsdata antingen efter det associerade klickdatumet/händelsedatumet (datumet för klickhändelsen eller tryckhändelsen) eller efter transaktionsdatumet (konverteringsdatumet). Konceptet för klicknings-/händelsedatumrapportering finns inte i [!DNL Analytics]; alla konverteringar spårade i [!DNL Analytics] rapporteras per transaktionsdatum. Därför kan samma konvertering rapporteras med olika datum i Adobe-annonsering och [!DNL Analytics]. Tänk dig en användare som klickar på en annons den 1 januari och konverterar den 5 januari. Om du visar konverteringsdata per händelsedatum i Adobe Advertising, kommer konverteringen att rapporteras den 1 januari, när klickningen inträffade. I [!DNL Analytics], skulle samma konvertering rapporteras den 5 januari.

![Exempel på en konvertering som tilldelats olika datum](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribut i [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] rapportering](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) låter er konfigurera regler för att identifiera olika marknadsföringskanaler baserat på distinkta aspekter av träffinformation. Du kan spåra kanaler som spåras i Adobe-annonsering ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]och [!UICONTROL Paid Search]) as [!DNL Marketing Channels] genom att använda `ef_id` frågesträngsparameter för att identifiera kanalen. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Även om [!DNL Marketing Channels] -rapporter kan spåra annonskanaler i Adobe. Det kan hända att data inte matchar Adobe-annonsrapporterna av flera anledningar. Mer information finns i följande avsnitt.

>[!NOTE]
>
> Följande centrala begrepp gäller också för flerkanalsspårning som omfattar kampanjer som inte spåras i Adobe-annonsering, som [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) -variabel (kallas även&quot;Tracking code&quot;-Dimension eller&quot;eVar 0&quot;) och anpassad spårning av eVar.

### Potentiellt olika attribueringsmodeller i [!DNL Marketing Channels]

Mest [!DNL Marketing Channels] rapporter har konfigurerats med [!UICONTROL Last Touch] attribuering, för vilken den senaste marknadsföringskanalen har tilldelats 100 % av konverteringsvärdet. Använda olika attribueringsmodeller för [!DNL Marketing Channels] Rapporter och Adobe Advertising-rapporter kommer att leda till skillnader i de konverteringar som tilldelats.

### Ett potentiellt annorlunda fönster för att söka efter [!DNL Marketing Channels]

Uppslagsfönstret för [!DNL Marketing Channels] kan anpassas. I Adobe Advertising är fönstret för klicksökning konfigurerbart, även om ett fast 60-dagarsfönster är vanligt. Om de två produkterna använder olika fönster för sökning kan du förvänta dig avvikelser i data.

### Olika kanalattribut i [!DNL Marketing Channels]

Adobe Advertising-rapporter fångar endast betalmedier som har handlagts via Adobe Advertising (betald sökning efter [!DNL Advertising Search] annonser och displayannonser för annonser DSP annonser), medan [!DNL Marketing Channels] kan spåra alla digitala kanaler. Detta kan leda till en diskrepans i den kanal för vilken en konvertering görs.

Till exempel har betalsökningar och naturliga sökkanaler ofta en symbiotisk relation, där varje kanal hjälper den andra. The [!DNL Marketing Channels] rapporten attribuerar vissa konverteringar till naturlig sökning som Adobe Advertising inte kommer att göra eftersom den inte spårar naturlig sökning.

Överväg också en kund som visar en displayannons, klickar på en betald sökannons, klickar i ett e-postmeddelande och lägger sedan en 30 USD-order. Även om Adobe Advertising och [!DNL Marketing Channels] båda använder den sista pekattribueringsmodellen, men konverteringen skulle ändå tilldelas olika till var och en. Adobe Advertising har inte tillgång till [!UICONTROL Email] kanal, vilket innebär att betalsökningen för konverteringen får poäng. [!DNL Marketing Channels]har dock tillgång till alla tre kanalerna, så det skulle kreditera [!UICONTROL Email] för konverteringen.

![Exempel på olika konverteringsattribuering i Adobe Advertising jämfört med [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Mer information om varför mätvärdena kan variera finns i &quot;[Varför kanaldata kan variera mellan Adobe och [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Skillnader i data i Adobe Analytics [!DNL Paid Search Detection]

The [äldre [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) funktion i [!DNL Analytics] tillåter företag att [Definiera regler för att spåra betald och organisk söktrafik](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) för angivna sökmotorer. The [!DNL Paid Search Detection] regler använder både en frågesträng och den refererande domänen för att identifiera betald och naturlig söktrafik. The [!DNL Paid Search Detection] rapporter ingår i den större gruppen av [Sökmetoder](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) som förfaller antingen när en viss händelse (till exempel en kundvagnsutcheckning) inträffar eller besöket avslutas.

Följande gränssnitt används för att skapa en [!DNL Paid Search Detection] regeluppsättning:

![Exempel på en regel för identifiering av betald sökning i [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Resultatet [!DNL Paid Search Detection] rapporterna innehåller [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]och [!UICONTROL Natural Search Keywords] rapporter.

Observera följande två begränsningar med data i [!DNL Paid Search Detection] rapporter:

* The [!UICONTROL Paid Search Keywords] och [!UICONTROL Natural Search Keywords] -rapporter visar sökfrågorna så som de identifieras av de refererande URL:erna, inte nyckelorden som användarna lägger bud på. Adobe [!DNL Analytics] rapporter visar de faktiska nyckelorden, så vänta dig inte att de ska överensstämma med [!DNL Paid Search Detection] nyckelordsrapporter.

* När [!DNL Paid Search Detection] den ursprungliga sökfrågan (teckensträngen som användaren angav i sökfältet i sökmotorn) var mer lättillgänglig för annonsörer via den refererande URL:en. Idag är sökmotorer i stort sett otydliga med sökfrågan och [!DNL Paid Search Detection] nyckelordsrapporter har begränsat värde eftersom de flesta frågedata tillhör &quot;unspecified&quot;.

   Med [!DNL Analytics for Advertising], kan annonsörer fortfarande spåra betalda nyckelord i [!DNL Analytics]. Den refererande domänen informerar motorn om vilken sökmotor som körde trafiken. Eftersom den annonserarspecifika kontoinformationen inte är kopplad till den refererande domänen, listas all trafik under sökmotorn. Annonsörer med flera konton i samma sökmotor bör hänvisa till Adobe-annonsering eller [!DNL Analytics] rapportering för kontospecifik rapportering.

### Varför konfigurera [!DNL Paid Search Detection]?

The [!DNL Paid Search Detection] kan du identifiera naturlig söktrafik i [[!DNL Analytics Marketing Channels] rapporter](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Att separera betald söktrafik och naturlig söktrafik är ett bra sätt att förstå det värde som naturlig sökning tillför hela marknadsföringsekosystemet.

## Klicka igenom dataverifiering för [!DNL Analytics for Advertising] {#data-validation}

För integreringen bör du validera klickinformationen för att säkerställa att alla sidor på webbplatsen följer klickfrekvensen.

I [!DNL Analytics], ett av de enklaste sätten att validera [!DNL Analytics for Advertising] tracking är att jämföra klickningar med instanser med hjälp av det beräknade måttet&quot;Click to AMO ID Instances&quot;, som beräknas så här:

```
Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)
```

[!UICONTROL AMO ID Instances] representerar antalet gånger som AMO-ID:n (`s_kwcid` parametrar) spåras på platsen. Varje gång någon klickar på en annons visas en `s_kwcid` parametern läggs till i landningssidans URL. Antalet [!UICONTROL AMO ID Instances]motsvarar därför antalet klick och kan valideras mot faktiska annonsklickningar. Vi ser vanligtvis en matchningsfrekvens på 80 % för [!DNL Search] och en matchningsfrekvens på 30 % för [!DNL DSP] trafik (när den filtreras så att den endast innehåller klickfrekvens [!UICONTROL AMO ID Instances]). Skillnaden i förväntningarna mellan sökning och visning kan förklaras av det förväntade trafikbeteendet. Sökfunktionen hämtar avsikten, och som sådan har användarna vanligtvis för avsikt att klicka på sökresultaten från sin fråga. Användare som ser en webbannons eller en videoannons är mer benägna att klicka på annonsen oavsiktligt och sedan antingen hoppa från webbplatsen eller avbryta det nya fönster som läses in innan sidaktiviteten spåras.

I Adobe Advertising-rapporter kan du jämföra klickningar med instanser med hjälp av &quot;[!UICONTROL ef_id_instances]&quot; i stället för [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Du bör förvänta dig en hög matchningsfrekvens mellan AMO ID och EF ID, men vänta inte med 100 % paritet eftersom AMO ID och EF ID i grunden spårar olika data, och den här skillnaden kan leda till små skillnader i den totala [!UICONTROL AMO ID Instances] och [!UICONTROL EF ID Instances]. Om summan [!UICONTROL AMO ID Instances] in [!DNL Analytics] skiljer sig från [!UICONTROL EF ID Instances] i Adobe-annonsering med mer än 1 %, kontakta dock [!DNL Adobe] kontoteam för att få hjälp.

Mer information om AMO ID och EF ID finns i [Adobe Advertising IDs Used by Analytics](ids.md).

Följande är ett exempel på en arbetsyta som du kan använda för att spåra klickningar på instanser.

![Exempel på en arbetsyta som spårar klickningar till instanser](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Jämföra datauppsättningar i [!DNL Analytics for Advertising] Jämfört i Adobe

The [AMO-ID](ids.md) (s_kwcid query string parameter) används för rapportering i [!DNL Analytics]och [EF ID](ids.md) används för rapportering i Adobe-reklam. Eftersom de är distinkta värden kan ett värde vara skadat eller inte läggas till på landningssidan.

Anta att vi har följande landningssida:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

där EF-ID är`test_ef_id`&quot; och AMO-ID:t är &quot;`test_amo_id`.&quot;

Om en omdirigering sker på en webbplats kan URL:en sluta på följande sätt:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

där EF-ID är`test_ef_id`&quot; och AMO-ID:t är &quot;`test_amo_id#redirectAnchorTag`.&quot;

I det här exemplet lägger tillägget av ankartaggen till oväntade tecken i AMO-ID:t, vilket resulterar i ett värde som inte känns igen i Analytics. Detta AMO-ID skulle inte klassificeras, och konverteringar som är kopplade till det skulle omfattas av[!UICONTROL unspecified]&quot; eller &quot;[!UICONTROL none]&quot; in [!DNL Analytics] rapporter.

Men även om sådana här problem är vanliga så brukar de vanligtvis inte resultera i en hög procent skillnader. Om du däremot upptäcker en stor skillnad mellan AMO-ID:n i [!DNL Analytics] och EF ID:n i Adobe Advertising, kontakta [!DNL Adobe] kontoteam för att få hjälp.

## Andra mätvärden

### Skillnaden mellan klick och besök {#clicks-vs-visits}

De verkar analoga, men klick och besök representerar olika data:

* **Klicka:** [!DNL DSP] eller sökmotorn registrerar ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Besök:** [!DNL Analytics] definierar en [besök](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) som en serie sidvyer av en användare, som avslutas enligt ett av flera kriterier, t.ex. 30 minuters inaktivitet.

En klickning kan per definition leda till flera besök.

Titta på följande exempel: Användare 1 och Användare 2 har båda åtkomst till en webbplats genom att klicka på en annons från Adobe. Användare 1 visar fyra sidor och går sedan ut för dagen, så det första klicket ger ett besök. Användare 2 visar två sidor, löv för en 45-minuters lunch, återvänder, visar ytterligare två sidor och sedan löv, I det här fallet resulterar den första klickningen i två besök.

![Exempel på skillnaden mellan klick och besök](/help/integrations/assets/a4adc-visits-example.png)

### Skillnaden mellan klick och genomklickningar

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klick och klickningar är två olika mätvärden:

* **Klicka:** [!DNL DSP] eller sökmotorn registrerar ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Klickfunktioner:** [!DNL Analytics] registrerar en klickfrekvens när besökaren kommer in på målwebbplatsen, landningssidan läses in och [!DNL Analytics] begäran längst ned på sidan skickar data till [!DNL Analytics].

Klickningar och klickningar kan skilja sig avsevärt på grund av oavsiktliga annonsklick. Vi har observerat att de flesta klick på displayannonser är oavsiktliga klick, och dessa oavsiktliga besökare trycker på knappen Tillbaka innan landningssidan läses in, så [!DNL Analytics] det går inte att spela in en klickfrekvens. Detta gäller särskilt annonser där en oavsiktlig klickning är mer sannolik, som mobilannonser, videoannonser och annonser som fyller skärmen och måste stängas innan användaren kan visa sidan.

Webbplatser som är inlästa på mobila enheter är också mindre benägna att resultera i klickningar på grund av lägre bandbredder eller tillgänglig processorkraft, vilket gör att landningssidor tar längre tid att läsa in. Det är inte ovanligt att 50-70 % av klickningarna inte leder till klickningar. I mobilmiljöer kan skillnaden vara så hög som 90 % på grund av kombinationen av en långsammare webbläsare och den större sannolikheten att användaren av misstag klickar på annonsen när han eller hon bläddrar igenom sidan eller försöker stänga annonsen.

Klickdata kan också spelas in i miljöer där klickningar inte kan spelas in med de aktuella spårningsmekanismerna (t.ex. klick som går in i eller från en mobilapp) eller där annonsören endast har använt en spårningsmetod (t.ex. med den genomskinliga JavaScript-metoden, webbläsare som blockerar cookies från tredje part spårar klickningar, men inte klickningar). En viktig orsak till att Adobe rekommenderar att man använder sig av både klicknings-URL:er och JavaScript-spårningsmetoder är att maximera täckningen av spårbara klickningar.

### Använda Adobe-reklamstatistik för icke-Adobe-reklamDimensioner

Adobe Advertising ger Analytics [reklamspecifik trafikstatistik och relaterade dimensioner från [!DNL DSP] och [!DNL Search]](advertising-metrics-in-analytics.md). Måtten för annonsering i Adobe gäller endast för de angivna måtten för annonsering i Adobe, och data är inte tillgängliga för andra dimensioner i [!DNL Analytics].

Om du till exempel visar [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] mått per konto, som är en Adobe-annonsdimension, så ser ni det totala [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] efter konto.

![Exempel på marknadsföringsstatistik för Adobe i en rapport som använder en Adobe Advertising-dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Om du däremot visar [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] mått per siddimension (t.ex. sida), för vilken Adobe Advertising inte tillhandahåller data, [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] för varje sida är noll (0).

![Exempel på marknadsföringsstatistik för Adobe i en rapport som använder en dimension som inte stöds](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Använda [!UICONTROL AMO ID Instances] som ersättning för clicks med icke-Adobe-reklamannonserande Dimensioner

Eftersom du inte kan använda [!UICONTROL AMO Clicks] med webbplatsdimensioner kan du behöva hitta en som motsvarar klickningar. Det kan vara frestande att använda besök som ersättning, men det är inte det bästa alternativet eftersom varje besökare kan ha flera besök. (Se &quot;[Skillnaden mellan klick och besök](#clicks-vs-visits).&quot; Vi rekommenderar istället att du använder [!UICONTROL AMO ID Instances], vilket är antalet gånger som AMO-ID:t hämtas. while [!UICONTROL AMO ID Instances] kommer inte att matcha [!UICONTROL AMO Clicks] exakt är de det bästa alternativet för att mäta klicktrafiken på webbplatsen. Mer information finns i &quot;[Dataverifiering för [!DNL Analytics for Advertising]](#data-validation).&quot;

![Exempel på [!UICONTROL AMO ID Instances] i stället för [!UICONTROL AMO Clicks] för en dimension som inte stöds](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Adobe-reklam](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Varför data kan variera mellan Adobe och [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

