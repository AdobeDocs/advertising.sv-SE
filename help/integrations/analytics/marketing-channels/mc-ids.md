---
title: Använda Adobe Advertising-ID:n för att skapa [!DNL Marketing Channels] regler
description: Lär dig hur du använder Adobe Advertising-ID:n för att skapa bearbetningsregler för  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] bearbetningsregler

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Du kan använda Adobe Advertising ID:n ([AMO ID och EF ID](../ids.md)) för att konfigurera [!DNL Marketing Channels] bearbetningsregler i Adobe Analytics. Använd Adobe Advertising-ID:n för regler som är specifika för era Adobe Advertising-kampanjer.

## AMO-ID:t i bearbetningsreglerna

AMO-ID är den primära spårningskod som används för att rapportera Adobe Advertising-data inom [!DNL Analytics]. AMO-ID är en sammanfogning av dynamiska värden som hanteras av Adobe för att ge detaljerad rapportering i [!DNL Analytics]. Den lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- eller rVar-dimension (AMO-ID). AMO-ID kan anges i [!DNL Analytics] på två sätt:

* Klickningsspårning: Adobe Advertising ställer in frågesträngsparametern `s_kwcid` i en länk och [!DNL Analytics] hämtar parametern från landningssidans URL när en klickning inträffar.
* Direktspårning ([!DNL DSP] endast): Den senaste händelsetjänsten identifierar en genomsiktsvy på serversidan och skickar AMO-ID:t till [!DNL Analytics]. I det här fallet innehåller URL-adressen inte någon `s_kwcid`-parameter.

De dynamiska värdena i AMO-ID:n anger marknadsföringskanalen som spårades:

* Prefixet i AMO-ID kan användas för att identifiera kanalen på den översta nivån i [!DNL Marketing Channels].

* Teckenfraser i texten för AMO-ID anger en mer specifik kampanjtyp.

* Suffixet&quot;vt&quot; finns för [!DNL DSP]-genomsiktstrafik och kan användas för att skapa separata genomklicknings- och visningskanaler i [!DNL DSP].

Resten av AMO-ID kan ignoreras.

| [!UICONTROL AMO ID] | Kanal | Regellogik |
|--------|---------|--------------------|
| !ctv (suffix) | [!UICONTROL DSP Connected TV View-through] | Slutar med |
| !d! (brödtext) | [!UICONTROL Display Network] | Innehåller |
| !g! (brödtext) | [!UICONTROL Google Search] | Innehåller |
| !s! (brödtext) | [!UICONTROL Search Partner] | Innehåller |
| !u! (brödtext) | [!UICONTROL Smart Shopping Campaign] | Innehåller |
| !ytv! (brödtext) | [!UICONTROL YouTube Video Ad] | Innehåller |
| !yts! (brödtext) | [!UICONTROL YouTube Search Ad] | Innehåller |
| !vp! (brödtext) | [!UICONTROL Google Video Partners] | Innehåller |
| !vt (suffix) | [!UICONTROL DSP View-through] | Slutar med |
| AL! (prefix) | [!UICONTROL Paid Search] | Börjar med |
| AC! (prefix) | [!UICONTROL DSP] | Börjar med |

### Exempel på bearbetningsregler som använder AMO-ID

Bearbetningsregeln [!DNL Marketing Channels] för kanalen [!UICONTROL Paid Search] kan se ut så här:

![Exempel på en [!UICONTROL Paid Search] regel ](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Bearbetningsregeln [!DNL Marketing Channels] för kanalen [!UICONTROL YouTube Video Ads] kan se ut så här:

![Exempel på en [!UICONTROL YouTube Video Ads] regel ](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Var noga med att köra reglerna i den ordning de är specifika. Om de två ovanstående reglerna var ordnade faller videobandstrafiken [!DNL YouTube] under [!UICONTROL Paid Search]-kanalen eftersom både AMO-ID:t skulle börja med&quot;AL!&quot; och innehåller %ytv!.

## EF ID in Processing Rules

AMO EF ID (EF ID) är den andra spårningskoden som används i integreringen [!DNL Analytics for Advertising]. Dess främsta syfte är att spåra och skicka [!DNL Analytics] händelsedata till Adobe Advertising. Varje gång en klickning eller genomgång sker genereras ett unikt EF-ID, även om det är exakt samma annons för samma besökare. EF-ID används inte i [!DNL Analytics]-rapportanvändargränssnittet eftersom det vanligtvis överstiger gränsen på 500 kB för unika värden per variabel i [!DNL Analytics], vilket gör det oanvändbart för rapportering. Mätvärden och metadata för Adobe Advertising tillämpas inte på EF-id:t, utan endast på AMO-ID:t. Spårning krävs för kampanjoptimering i Adobe Advertising, så båda ID:n krävs.

Trots att EF ID-dimensionen inte används direkt i [!DNL Analytics]-rapportering kan EF ID vara användbart när du skapar marknadsföringskanaler. EF ID-suffixet anger kanalen (visning eller sökning) och om besöket drivs av en klickfrekvens eller en genomgång. Avgränsaren i EF-ID är ett kolon i stället för utropstecknet i AMO-ID.

| EF ID-suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exempel på bearbetningsregler som använder EF-ID

#### Visa genomklickningsregel

Skapa en klickbar marknadsföringskanal för webbannonsering genom att endast klickningar görs. Eftersom AMO-ID:t är samma för både klickningar och genomvisningar används variabeln EF ID och frågesträngsparametern `ef_id` i den här regeln.

Ibland spåras klickningar via webbadressen (standardvärdet). I andra fall spåras klickningar via den senaste händelsetjänsten på serversidan, och därför innehåller URL-adressen inte parametern `ef_id`. Regeln kontrollerar därför om det finns villkor där variabeln EF ID eller frågesträngsparametern `ef_id` slutar med &quot;:d&quot;. Använd operatorn `Any` eftersom du vill att den här regeln ska aktiveras för båda villkoren.

![Exempel på en genomklickningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visa genomskinlighetsregel

Om du vill skapa en visningskanal skapar du en regel där EF-ID:t avslutas med &quot;:i&quot;. Eftersom besökaren inte klickade på annonsen inkluderas inte `ef_id` eller `s_kwcid` i URL:en, så regeln kräver bara ett villkor.

![Exempel på en genomskärningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundprinciper för [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Använda [!DNL Analytics Marketing Channels] med Adobe Advertising-data](mc-ac-data.md)
>* [Video: Använder  [!DNL Marketing Channels] för Adobe Advertising-rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising-ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
