---
title: Använda Adobe Advertising ID:n för att skapa  [!DNL Marketing Channels] regler
description: Lär dig hur du använder Adobe Advertising ID:n för att skapa bearbetningsregler för  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] bearbetningsregler

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

Du kan använda Adobe Advertising-ID:n ([AMO-ID och EF-ID](../ids.md)) för att konfigurera [!DNL Marketing Channels] bearbetningsregler i Adobe Analytics. Använd Adobe Advertising ID:n för regler som är specifika för era Adobe Advertising-kampanjer. Den ordning som du bearbetar reglerna i avgör om alla möjliga data hämtas korrekt.

## AMO-ID:t i bearbetningsregler

AMO-ID är den primära spårningskod som används för att rapportera Adobe Advertising-data inom [!DNL Analytics]. AMO-ID är en sammanfogning av dynamiska värden som hanteras av Adobe för att ge detaljerad rapportering i [!DNL Analytics]. Den lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) - eller rVar-dimension (AMO-ID). AMO-ID kan anges i [!DNL Analytics] på två sätt:

* Klickningsspårning: Adobe Advertising anger frågesträngsparametern `s_kwcid` i en länk och [!DNL Analytics] hämtar parametern från landningssidans URL när en klickning inträffar.

* Direktspårning ([!DNL DSP] endast): [!DNL Last Event Service] identifierar en genomsiktsvy på serversidan och skickar AMO-ID:t till [!DNL Analytics]. I det här fallet innehåller URL-adressen inte någon `s_kwcid`-parameter.

De dynamiska värdena i AMO-ID:n anger marknadsföringskanalen som spårades:

* Prefixet i AMO-ID kan användas för att identifiera kanalen på den översta nivån i [!DNL Marketing Channels].

* Teckenfraser i texten för AMO-ID anger en mer specifik kampanjtyp.

* Suffixet&quot;vt&quot; finns för [!DNL DSP]-genomsiktstrafik och kan användas för att skapa separata genomklicknings- och visningskanaler i [!DNL DSP].

Resten av AMO-ID kan ignoreras.

| [!UICONTROL AMO ID] | Kanal | Regellogik |
|--------|---------|--------------------|
| !ctv (suffix) | [!UICONTROL DSP Connected TV ViewThrough] | Slutar med |
| !d! (brödtext) | [!UICONTROL Display Network] | Innehåller |
| !g! (brödtext) | [!UICONTROL Google Search] | Innehåller |
| !s! (brödtext) | [!UICONTROL Search Partner] | Innehåller |
| !u! (brödtext) | [!UICONTROL Smart Shopping Campaign] | Innehåller |
| !ytv! (brödtext) | [!UICONTROL YouTube Video Ad] | Innehåller |
| !yts! (brödtext) | [!UICONTROL YouTube Search Ad] | Innehåller |
| !vp! (brödtext) | [!UICONTROL Google Video Partners] | Innehåller |
| !vt (suffix) | [!UICONTROL DSP ViewThrough] | Slutar med |
| AL! (prefix) | [!UICONTROL Paid Search] | Börjar med |
| AC! (prefix) | [!UICONTROL DSP Display] | Börjar med |

## EF-ID:t i bearbetningsreglerna

AMO EF ID (EF ID) är den andra spårningskoden som används i integreringen [!DNL Analytics for Advertising]. Dess främsta syfte är att spåra och skicka [!DNL Analytics] händelsedata till Adobe Advertising. Varje gång en klickning eller genomgång sker genereras ett unikt EF-ID, även om det är exakt samma annons för samma besökare. EF-ID används inte i [!DNL Analytics]-rapportanvändargränssnittet eftersom det vanligtvis överstiger gränsen på 500 kB för unika värden per variabel i [!DNL Analytics], vilket gör det oanvändbart för rapportering. Adobe Advertising-mått och metadata tillämpas inte på EF-id:t. De tillämpas bara på AMO-ID:t. Spårning krävs för kampanjoptimering i Adobe Advertising, så båda ID:n krävs.

Trots att EF ID-dimensionen inte används direkt i [!DNL Analytics]-rapportering kan EF ID vara användbart när du skapar marknadsföringskanaler. EF ID-suffixet anger kanalen (visning eller sökning) och om besöket drivs av en klickfrekvens eller en genomgång. Avgränsaren i EF-ID är ett kolon i stället för utropstecknet i AMO-ID.

| EF ID-suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Exempel på bearbetningsregler för Adobe Advertising

Följande exempelregeluppsättning fokuserar på reglerna för annonskanalerna (Betald sökning, Display ClickThrough och Display ViewThrough). Den rekommenderade regeln för identifiering av betald sökning (inklusive hur den regeln interagerar med logiken för naturligt sökmarknadsföringskanal) och en valfri uppdatering av regeln för naturligt refererande domäner visas också.

**Obs!** Visning kan separeras som två kanaler eller slås samman till en kanal baserat på annonsörens inställning.

Andra kanaler ingår i exempelbilden för att illustrera den rekommenderade ordningen för reklamkanalernas verksamhet jämfört med andra kanaler i en vanlig implementering.

>[!IMPORTANT]
>
>Mer information om i vilken ordning reglerna ska bearbetas finns i [Åtgärdsordning för [!DNL Marketing Channels] regler](#rule-order).

![Exempel på en uppsättning bearbetningsregler](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Betalsökregel

Det bästa sättet är att inkludera två villkor med operatorn &quot;Any&quot; för en [!UICONTROL Paid Search]-regel:

* Kostnads-/klicknings-/visningsdata innehåller AMO-ID:t, så inkludera AMO-ID:t. AMO-ID:t ska börja med &quot;AL!&quot; för att korrekt allokera klicknings-/kostnads-/visningsdata till [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* URL:erna för [!UICONTROL Paid Search] klickningar inkluderar alltid frågesträngsparametern `s_kwcid`, så inkludera den för att säkerställa att dubbletter tas bort korrekt om besökaren går tillbaka till landningssidan. Inkludera &quot;AL!&quot; före `s_kwcid` för att korrekt allokera klicknings-/kostnads-/visningsdata till [!UICONTROL Paid Search].

Ange inte kanalens värde som AMO-ID. I stället anger du det till något som till exempel Referensdomän, Sökmotor + nyckelord eller Sida. (Detta gäller för alla [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Exempel på en betald sökregel](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Exempel på en betald sökregel")

### Naturlig sökregel

Kontrollera att [!UICONTROL Natural Search]-identifieringsreglerna [[!UICONTROL Paid Search] för &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) innehåller frågesträngsparametrarna `ef_id` och `s_kwcid`. (Vanligtvis konfigureras detta automatiskt när Advertising Search, Social och Commerce integreras i [!DNL Analytics], men om en [!DNL Analytics]-administratör har ändrat logiken efter att integreringen konfigurerats bör du kontrollera detta.)

Ställ in regeln på&quot;Matchar reglerna för identifiering av naturlig sökning&quot; (vilket vanligtvis är standardinställningen för den här kanalen).

![Exempel på en regel för naturlig sökning](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Exempel på en regel för naturlig sökning")

### Visa klickningsregel 1

Skapa en Display ClickThrough-marknadsföringskanal genom att endast samla in klickningar. Eftersom AMO-ID:t är samma för både klickningar och genomvisningar används variabeln EF ID och frågesträngsparametern `ef_id` i den här regeln.

Ibland spåras klickningar via webbadressen (standardvärdet). I andra fall spåras klickningar via den senaste händelsetjänsten på serversidan, och därför innehåller URL-adressen inte parametern `ef_id`. Regeln kontrollerar därför om det finns villkor där EF-ID-variabeln eller frågesträngsparametern `ef_id` slutar med :d. Använd operatorn `Any` eftersom du vill att den här regeln ska aktiveras för båda villkoren.

![Exempel på en första Display ClickThrough-regel](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Exempel på en första Display ClickThrough-regel")

### Regel för naturligt refererande domäner

(Valfritt) Det bästa sättet är att lägga till villkoret&quot;Är första sidan av besök&quot; med operatorn&quot;Valfri&quot; i standardregeln [!UICONTROL Natural Referring Domains]. Den här regeln är valfri, men den kan förhindra att versaler för naturliga referenser ställs in när användaren klickar på bakåtknappen för att gå tillbaka till landningssidan.

![Exempel på en regel för naturligt refererande domäner](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Exempel på en regel för naturligt refererande domäner")

### Visa CTV-vyigenom-regel

Om du vill spåra [!DNL DSP]-anslutna TV-vyer (CTV) skapar du en regel där AMO-ID:t slutar med `"!ctv"`. Eftersom besökaren inte klickade på annonsen inkluderas inte `ef_id` eller `s_kwcid` i URL:en, och regeln kräver bara ett villkor.

![Exempel på en Visa CTV-vy](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "Exempel på en Visa CTV-vy")

### Visa genomskinlighetsregel

Om du vill skapa en DisplayThrough-kanal skapar du en regel där EF-ID:t slutar med :i. Eftersom besökaren inte klickade på annonsen inkluderas inte `ef_id` eller `s_kwcid` i URL:en, och regeln kräver bara ett villkor.

![Exempel på en visningsvyVia-regel](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Exempel på en visningsvy")

### Visa klickningsregel 2

Ange **AMO ID börjar med &quot;AC!&quot; för den andra Display ClickThrough-regeln**. Den andra regeln finns för att hämta klicknings-/kostnads-/visningsdata för visningskanalen som kommer in direkt från Adobe Advertising till [!DNL Analytics]. Dessa data tilldelas ett AMO-ID men innehåller inte någon URL med frågesträngen `ef_id`, så de här träffarna är inte kopplade till ett AMO EF-ID, vilket är den första Display ClickThrough-regeln fångar.

![Exempel på en andra Display ClickThrough-regel](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Exempel på en andra Display ClickThrough-regel")

## Åtgärdsordning för [!DNL Marketing Channels]-regler {#rule-order}

![Idealisk ordning för åtgärder för Adobe Advertising-relaterade regler](/help/integrations/assets/a4adc-mc-rule-order.png "Idealisk ordning för åtgärder för Adobe Advertising-relaterade regler")

* Placera [!UICONTROL Paid Search] *före* [!UICONTROL Natural Search]. I annat fall kan betalda sökdata tilldelas till naturlig sökning.

* Placera **först** [!UICONTROL Display ClickThrough] *före* [!UICONTROL Natural Referring Domains] och [!UICONTROL Natural Social].

* När du använder [!UICONTROL CTV view-throughs] ska du placera den *före* [!UICONTROL Display ViewThroughs]. I annat fall hämtas CTV-visningar som Display ViewThgros.

* Placera [!UICONTROL Display ViewThroughs] *efter* andra kanaler, men före [!UICONTROL Internal] och [!UICONTROL Direct] eftersom det är möjligt att en genomskinlig och en icke-[!DNL Advertising] genomklickning kan inträffa i samma landningshändelse. En besökare kan till exempel se en Adobe Advertising-annons, få ett intryck och sedan gå till webbplatsen via [!UICONTROL Natural Search].

  Det bästa sättet är att prioritera de andra kanalerna (utom [!UICONTROL Internal] och [!UICONTROL Direct]) framför genomsiktningarna.

* Vissa annonsörer kan välja att prioritera [!UICONTROL Display ViewThroughs] framför [!UICONTROL Natural Referring Domains]. Det gör du genom att byta bearbetningsordning för de två reglerna.

* Regeln **second** [!UICONTROL Display ClickThrough] finns där för att fånga upp de klicknings-/kostnads-/inställningsdata som kommer in direkt från Adobe Advertising till [!DNL Analytics]. Eftersom dessa data endast tilldelas ett AMO-ID är dessa träffar inte kopplade till ett AMO EF-ID. Om du inte anger den här regeln hamnar alla klicknings-/kostnads-/inställningsdata under [!UICONTROL Direct]-kanalen, som är standardkanalen för alla data som inte matchar en [!DNL Marketing Channel]. Den här regeln måste komma *efter* genomskinlighetsregeln, annars hämtas alla genomvisningar.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Grundprinciper för [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Använda [!DNL Analytics Marketing Channels] med Adobe Advertising-data](mc-ac-data.md)
>* [Video: Använder [!DNL Marketing Channels] för Adobe Advertising-rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising-id:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)