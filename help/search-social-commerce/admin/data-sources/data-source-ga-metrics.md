---
title: Tillgänglig [!DNL Google Analytics] mått
description: Referera till [!DNL Google Analytics] Tillgängliga mätvärden för datakällor.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Bilaga - tillgänglig [!DNL Google Analytics] mått

Följande mått, förutom de undantag som anges, är tillgängliga när de aktiveras i kundens implementering i [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Kategori | Exkluderad | Kommentar |
| ---- | ---- | ---- |
| \[Alla\] | Mätvärden med datatypen PERCENT | Mätvärden som presenteras som en procentandel exkluderas alltid. |
| Användare | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Session | ga:uniqueDimensionKombinations | — |
| Målkonverteringar | — | — |
| Sidspårning | ga:entrances, ga:timeOnPage, ga:exits | — |
| Intern sökning | — | De egna namnen på alla mätvärden från den interna sökningen anges med värdet &quot;InternalSearch:&quot; |
| Händelsespårning | — | — |
| E-handel | — | — |
| Social interaktion | — | — |
| Undantag | — | — |
| Anpassade variabler eller kolumner | ga:calcMetric_* | Beräknade värden exkluderas alltid. |

>[!MORELIKETHIS]
>
>* [Synkronisering [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] visa som en datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
