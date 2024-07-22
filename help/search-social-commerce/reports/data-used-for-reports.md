---
title: Data som används för rapporter
description: Lär dig mer om olika typer av data som finns i datavyer och anpassade rapporter.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: 840c7f6295b73a784725c301a78ae89c827fd45e
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Data som används för rapporter

Search, Social och Commerce innehåller en omfattande uppsättning resultatrapporter baserade på klicknings- och konverteringsdata. Du kan visa grundläggande prestandadata för de olika komponenterna i en portfölj eller ett annonskonto från vyerna [!UICONTROL Portfolios] och [!UICONTROL Campaigns] samt genom att generera olika grundläggande och avancerade rapporter.

Annonsörer som använder tjänsten för spårning av konvertering i Adobe Advertising kan också identifiera antalet klick för en geografisk plats eller ett domännamn för en refererande webbplats, hur annonser i varje kanal och de olika händelser som leder till konvertering bidrar till den övergripande konverteringsgraden och distributionen av konverteringar för ett enskilt [konverteringsmått](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) per marknadsföringskanal. Vilka rapporter som är tillgängliga varierar beroende på typ av användarkonto. Kontogruppen Adobe har tillgång till alla rapporter.

De flesta rapporter kan anpassas så att endast den information som du vill se visas. Följande standardvärden är tillgängliga i de flesta rapporter och beräknas på annonsnivå:

* **Standardprestandamått:**

   * **[!UICONTROL Impressions]:** Det totala antalet gånger som annonsen placerades ut.

   * **[!UICONTROL Clicks]:** Det totala antalet gånger som en länk i annonsen klickades.

   * **[!UICONTROL Cost]:** Den totala kostnaden för annonsen. Kostnaden för PPC-annonsering (betala per klick) är alltid antalet klick multiplicerat med kostnaden per klick.

   * **[!UICONTROL Cost per Click]:** Den genomsnittliga kostnaden för en annons med ett klick, vilket är kostnaden för annonsen dividerat med det totala antalet klick för annonsen. Om du till exempel spenderar 100 USD för ett annonsintryck och annonsen genererar 10 klick blir kostnaden per klick 100 USD/10=10 USD per klick.

   * **[!UICONTROL Average Position]:** (i tillämpliga fall) Den genomsnittliga positionen för en annons som har placerats, viktad med antalet visningar.

   * **[!UICONTROL Estimated Clicks]:** (Ingår i avancerade rapporter för annonsörer med endast tjänsten för spårning av konvertering i Adobe Advertising) Det totala antalet beräknade klick för en ort eller domän för en refererande webbplats. Detta kan omfatta data för annonsnätverk som en annonsörer inte har något annonskonto för.

* **Konverteringsmått:** Det totala antalet konverteringar för varje annonsörs konverteringsmått, eller transaktionsdata som spårats mot ett konverteringsmått. Detta kan inkludera konverterings- och webbplatsengagemangsmått, men inte beräknade mätvärden och avancerade beräknade mätvärden, som synkroniseras från Adobe Analytics.

  Detta kan även omfatta [[!DNL Google Ads] spårade konverteringar ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) och [[!DNL Google Analytics] spårade konverteringar ](/help/search-social-commerce/admin/data-sources/data-source-about.md) som synkroniseras för annonserarkontot.

* **Anpassade mått:** Dina egna mått, som du härleder genom att skapa formler baserade på befintliga mått (till exempel kostnaden per order).

## Tillgänglighet

När du genererar rapporter kan du välja hur konverteringsdata ska tilldelas i en serie händelser som leder till en konvertering. Du kan till exempel välja att tilldela hela konverteringen till den sista händelsen eller att väga den sista händelsen mer än de andra. Som standard tilldelas konverteringar till den sista händelsen.

Beroende på vilken attribueringsregel du anger för rapporten är data för varje rapporttyp tillgängliga för följande datum.

| Rapportgrupp | Rapport | Datum för vilka data är tillgängliga |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Från och med den 15 maj 2021.<br><br><b>Undantag:</b> Prominence metrics data is available from 8 September 2022. |
| | Alla andra [!UICONTROL Basic Reports] | De senaste 36 månaderna.<br><br><b>Undantag:</b> Prominence metrics data is available from 8 September 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | De senaste 45 dagarna. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | De föregående två (2) månaderna plus den aktuella månaden. |
| [!UICONTROL Assist Reports] | Alla | De senaste 18 månaderna. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Föregående år. |
| | [!UICONTROL RSA Assets Report] | Från och med den 10 augusti 2022. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | De senaste 180 dagarna. |
| | Alla andra [!UICONTROL Specialty Reports] | De föregående två (2) månaderna. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | De senaste 18 månaderna. |
| [!UICONTROL Change History Report] | — | De senaste 31 dagarna. |

>[!MORELIKETHIS]
>
>* [Om rapporter](report-about.md)
>* [Inledande inställningsaktiviteter för rapporter](initial-setup.md)
