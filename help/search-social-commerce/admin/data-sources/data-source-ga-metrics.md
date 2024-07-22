---
title: Tillgängliga [!DNL Google Analytics] mått
description: Referera till  [!DNL Google Analytics] mätvärden som är tillgängliga för datakällor.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Bilaga - tillgängliga [!DNL Google Analytics]-mått

Följande mått, förutom de undantag som anges, är tillgängliga när de är aktiverade i kundens implementering i [!DNL Google Analytics].

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
>* [Synkronisering av  [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] vy som datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
