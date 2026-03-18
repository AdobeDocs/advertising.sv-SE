---
title: Adobe Advertising-statistik i Analysis Workspace
description: Adobe Advertising-statistik i Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Adobe Advertising-statistik i Analysis Workspace

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

>[!NOTE]
>
>* Adobe Advertising skickar trafikstatistik och dimensioner till [!DNL Analytics] dagligen.
>* [!DNL Analytics] fångar Adobe Advertising klickningar och genomgångar i realtid.
>* För [!DNL Search, Social, & Commerce] stöds den här funktionen för de flesta annonsnätverk och kampanjtyper. Mer information finns i [Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md) i [!DNL Search, Social, & Commerce]-handboken.

## Trafikstatistik från Adobe Advertising

Adobe Advertising trafikstatistik i [!DNL Analytics] börjar oftast med&quot;Adobe Advertising&quot;, förutom [!UICONTROL AMO ID Instances]. Men för långtidskunder som använde en anpassad händelse (i stället för en reserverad händelse) för att ursprungligen skapa mätvärden för klick, kostnader och visningar börjar mätvärdena fortfarande med&quot;AMO&quot;.

| Trafikmått | Beskrivning |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] eller (vissa gamla kunder) [!UICONTROL AMO Clicks] | Antal Adobe Advertising-klick. |
| [!UICONTROL Adobe Advertising Cost] eller (vissa gamla kunder) [!UICONTROL AMO Cost] | Adobe Advertising spenderar pengar i rapporteringsprogrammets valuta. |
| [!UICONTROL Adobe Advertising Impressions] eller (vissa gamla kunder) [!UICONTROL AMO Impressions] | Antalet Adobe Advertising-visningar. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Antalet visningar som har opererats och för vilka visningspotentieringen har initierats. Detta värde beräknas som (instrumenterade avtryck - antalet omätbara avtryck). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Hur många minuter en Adobe Advertising-video visades. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Antalet visningar som inte kunde visas. Värdet beräknas som ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Antalet avtryck som har mätts så att de kan visas enligt placeringskonfigurationen. |
| [!UICONTROL Adobe Advertising Views] | Antalet vyer på en annons. En vy räknas när visningsprogrammet startar Adobe Advertising-videon. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Antalet vyer som minst 25 % av en Adobe Advertising-video har tittat på. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Antalet vyer som minst 50 % av en Adobe Advertising-video har tittat på. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Antalet visningar som minst 75 % av en Adobe Advertising-video har tittat på. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Antalet vyer som 100 % av en Adobe Advertising-video bevakades för. |
| [!UICONTROL AMO ID Instances] | Antalet gånger som [!UICONTROL AMO ID] har angetts. |

## Adobe Advertising dimensioner

>[!NOTE]
>
>Alla Adobe Advertising-dimensioner i [!DNL Analytics] följs av [!DNL (AMO ID)].

| Dimension | Tillämpliga Adobe Advertising-data | Beskrivning |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Advertising DSP eller sökmotorns namn |
| [!UICONTROL Account (AMO ID] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Kontonamnet. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | RTB ([!DNL DSP]) eller annonsnätverksnamnet ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Kampanjnamnet. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Paketets ([!DNL DSP]) eller portföljens ([!DNL Search, Social, & Commerce]) namn. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Placeringsnamnet. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | Annonsgruppens namn. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | Nyckelordet. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Sökmatchningstypen. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Nyckelordet och matchningstypen. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Annonstypen, till exempel `text`, `video`, `display` eller `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Annonstypen ([!DNL DSP]) eller annonsrubriken ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Annonsbeskrivningen ([!DNL DSP]) eller annonstexten ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Den URL som visas i annonsen. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Annonsens mål-URL. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP]- och [!DNL Search, Social, & Commerce]-data | Anger om landningssidan var en genomsiktlig eller klickbar. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Produktmålet för en produktlistad annons. |

## Användbara anpassade beräknade värden för Adobe Advertising

Överväg att skapa följande mätvärden för dina Adobe Advertising-data.

* Klicka på instansen av landningssidan ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Detta är den procentandel av personerna som klickade på annonsen och gjorde den till landningssidan.
* Mätbar hastighet ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Synlig impressionshastighet ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kostnad per vy ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kostnad per klick ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
