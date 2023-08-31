---
title: Adobe Advertising Metrics in Analysis Workspace
description: Adobe Advertising Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Adobe Advertising Metrics in Analysis Workspace

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

>[!NOTE]
>
>* Adobe Advertising överför trafikstatistik och mått till [!DNL Analytics] varje dag.
>* [!DNL Analytics] tar klickningar och genomgångar i realtid för Adobe Advertising.
>* För [!DNL Search, Social, & Commerce], stöds den här funktionen för de flesta annonsnätverk och kampanjtyper. Se &quot;[Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md)&quot; i [!DNL Search, Social, & Commerce] Guide för mer information.

## Trafikstatistik från Adobe Advertising

Adobe Advertising trafikstatistik på [!DNL Analytics] börjar oftast med &quot;Adobe Advertising&quot;, förutom &quot;[!UICONTROL AMO ID Instances].&quot; Men för långtidskunder som använde en anpassad händelse (i stället för en reserverad händelse) för att ursprungligen skapa mätvärden för klick, kostnader och visningar börjar mätvärdena fortfarande med&quot;AMO&quot;.

| Trafikmått | Beskrivning |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] eller (vissa gamla kunder) [!UICONTROL AMO Clicks] | Antal Adobe Advertising-klick totalt. |
| [!UICONTROL Adobe Advertising Cost] eller (vissa gamla kunder) [!UICONTROL AMO Cost] | Adobe Advertising i rapporteringsprogrammets valuta. |
| [!UICONTROL Adobe Advertising Impressions] eller (vissa gamla kunder) [!UICONTROL AMO Impressions] | Antalet Adobe Advertising-visningar. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Antalet visningar som har opererats och för vilka visningspotentieringen har initierats. Detta värde beräknas som (instrumenterade avtryck - antalet omätbara avtryck). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Hur många minuter en Adobe Advertising-video visades. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Antalet visningar som inte kunde visas. Detta värde beräknas som ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Antalet avtryck som har mätts så att de kan visas enligt placeringskonfigurationen. |
| [!UICONTROL Adobe Advertising Views] | Antalet vyer på en annons. En vy räknas när visningsprogrammet startar Adobe Advertising-videon. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Antalet vyer för vilka minst 25 % av en Adobe Advertising-video bevakades. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Antalet vyer för vilka minst 50 % av en Adobe Advertising-video bevakades. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Antalet vyer för vilka minst 75 % av en Adobe Advertising-video bevakades. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Antalet vyer som 100 % av en Adobe Advertising-video bevakades för. |
| [!UICONTROL AMO ID Instances] | Antalet gånger [!UICONTROL AMO ID] är inställt. |

## Adobe Advertising Dimensioner

>[!NOTE]
>
>Alla Adobe Advertising-dimensioner i [!DNL Analytics] följs av &quot;[!DNL (AMO ID)].&quot;

| Dimension | Tillämpliga Adobe Advertising-data | Beskrivning |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | DSP eller sökmotorns namn |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Kontonamnet. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) eller annonsnätverksnamnet ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Kampanjnamnet. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Paketet ([!DNL DSP]) eller portfölj ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Placeringsnamnet. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | Annonsgruppens namn. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | Nyckelordet. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Sökmatchningstypen. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Nyckelordet och matchningstypen. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Annonstypen, till exempel `text`, `video`, `display`, eller `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Annonstypen ([!DNL DSP]) eller annonsrubrik ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Annonsbeskrivningen ([!DNL DSP]) eller reklamtext ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Den URL som visas i annonsen. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Annonsens mål-URL. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] och [!DNL Search, Social, & Commerce] data | Anger om landningssidan var en genomsiktlig eller klickbar. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Produktmålet för en produktlistad annons. |

## Användbara anpassade beräknade värden för Adobe Advertising

Överväg att skapa följande mått för dina Adobe Advertising-data.

* Klicka på instansen av landningssidan ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Detta är den procentuella andelen personer som klickade på annonsen och tog den till landningssidan.
* Mätbar hastighet ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Synlig tryckhastighet ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kostnad per vy ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kostnad per klick ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
