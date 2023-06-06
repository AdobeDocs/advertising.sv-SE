---
title: "[!UICONTROL Label Classification Report]"
description: Läs mer om [!UICONTROL Label Classification Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

The [!UICONTROL Label Classification Report] innehåller kostnads-, klick- och (valfritt) konverteringsdata per nyckelordsnivå eller etikettklassificering på annonsnivå som aggregerats över annonsnätverk, konton, kampanjer eller annonsgrupper. Som standard innehåller data en rad för varje tillämplig nyckelordsetikettklassificering för nyckelord, annonser och placeringar som tagit emot visningar för varje tidsenhet i det angivna datumintervallet. Raderna är i stigande ordning först efter startdatumet för tidsenheten, sedan efter etikettklassificering och sedan efter etikettvärde som standard.

Du kan visa data för de senaste 36 månaderna.

>[!NOTE]
>
>* Det går inte att rapportera per etikettklassificeringar på ad-nivå för [!DNL Microsoft® Advertising] annonskampanjer för dynamisk sökning (DSA).
>* Mer än en etikettklassificering kan gälla för samma enhet, så summan för varje mätvärde kan vara högre än den faktiska summan för enheten. Exempel: ett nyckelord &quot;suede skor&quot; har två etikettvärden, &quot;suede&quot; och &quot;skodon&quot;, och nyckelordet fick 100 klick. Kolumnen Click skulle visa &quot;100&quot; för vart och ett av dessa etikettvärden, så summan för båda raderna blir &quot;200&quot;.

* Alla ändringar du gör av etiketteringsindelningar och underordnade etikettvärden för en enhet visas på ungefär en timme.

## Standardkolumner

Beskrivningar av alla standardkolumner och anpassade kolumner finns i &quot;[Rapportkolumner för grundläggande och avancerade rapporter](basic-advanced-report-columns.md).&quot;

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [Grundläggande och avancerade rapporter](basic-advanced-report-about.md)
>* [Generera en grundläggande eller avancerad rapport](basic-advanced-report-generate.md)
>* [Grundläggande och avancerade rapportinställningar](basic-advanced-report-settings.md)

