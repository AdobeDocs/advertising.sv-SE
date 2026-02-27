---
title: Tillgängliga rapportkolumner
description: Se beskrivningar av tillgängliga kolumner i anpassade rapporter.
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: c318c29e78f33c665380e5e5ac0b58a653f8987a
workflow-type: tm+mt
source-wordcount: '2933'
ht-degree: 0%

---

# Tillgängliga rapportkolumner

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| Mätningstyp | Undertyp | Kolumnnamn | Beskrivning |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | Det annons-ID som tilldelats av den externa annonsservern. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | Unik identifierare för annonsen i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | Namnet på annonsen som tilldelats av användaren. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | Annonsens format. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | Klassificeringen av annonsen har ändrats av användaren eller markerats med datumindata: *[!UICONTROL live]*, *[!UICONTROL scheduled]*, *[!UICONTROL completed]* eller *[!UICONTROL archived]*. |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | Annonsörens namn. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | Den totala budget som tilldelats av användaren för kampanjen. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | Slutdatumet för kampanjen. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | Unik identifierare för kampanjen i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | Namnet på kampanjen som tilldelats av användaren. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | Det första datumet för kampanjen. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | Innehåll/filmtitel. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | Innehållsserien. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | Innehållsgenren. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | Produktionskvaliteten, enligt definition i [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Värdena kan vara `Unknown`, `Professionally Produced`, `Prosumer` eller `User Generated`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | Innehållstypen som definieras av [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Värdena kan vara `Video,` `Game`, `Music`, `Application`, `Text`, `Other` eller `Unknown`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | Innehållsklassificering, till exempel PG eller R. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | Anger om annonsen fanns i en djurbesättning: `Not Live` eller `Live`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | Innehållets längd i sekunder, som vanligtvis används för video eller ljud. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | Innehållets språk med ISO-639-1-alpha-2. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | År, månad och dag. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | Dag [!UICONTROL of Week] | Den angivna dagen, till exempel [!UICONTROL Monday] eller [!UICONTROL Tuesday]. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | År, månad, dag och timme. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | Månad och år. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | Tiden till timmen, från 0 till 23. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | Datumintervallet för den aktuella veckan, från söndag till lördag. Exempel: 2021-02-18 till 2021-03-07. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | Leverantören av webbläsaren där annonsen visades (till exempel Google eller Mozilla). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | Den version av webbläsaren där annonsen visades (till exempel [!UICONTROL Safari 4.3] eller [!UICONTROL Chrome 7.0]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | Webbläsaren som annonsen visades i (till exempel [!UICONTROL Chrome] eller [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Environment] | Enhetsmiljöerna som placeringen har som mål: (*[!UICONTROL Desktop]*, *[!UICONTROL Mobile]* och/eller *[!UICONTROL Connected TV])*. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | Den typ av enhet som annonsen visades på (till exempel [!UICONTROL Set Top Box] eller [!UICONTROL Mobile Phone]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | Tillverkaren av den enhet som annonsen visades på (till exempel [!UICONTROL Samsung], [!UICONTROL Lenovo] eller [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | Modellen för den enhet på vilken annonsen visades (till exempel [!UICONTROL iPhone XS] eller [!UICONTROL Galaxy Note 7]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | Leverantören av det operativsystem där annonsen visades (till exempel [!UICONTROL Microsoft] eller [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | Den version av operativsystemet som annonsen visades på (till exempel [!UICONTROL Windows 10] eller [!UICONTROL iOS Mojave]) |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | Det operativsystem som annonsen visades på (till exempel [!UICONTROL Apple iOS] eller [!UICONTROL Android]). |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | Det användartilldelade namnet för erbjudandet, som anges i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | Om erbjudandet är *[!UICONTROL Guaranteed]* eller *[!UICONTROL Non-Guaranteed]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | Klassificeringen av lagret: *[!UICONTROL Private],* *[!UICONTROL On Demand],* eller *[!UICONTROL Public]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | Den unika identifierare som tilldelats en privat affär via den externa leveranspartnern. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | Leverantörspartnern som tillhandahåller lagret. Detta är vanligtvis en utgivare, men kan också vara en SSP. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | Den SSP-partner som mediet är hänförligt till. |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | Antalet gånger en enhet har fått en annons, baserat på den unika cookien eller enhets-ID:t. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | Den stad som de rapporterade uppgifterna härrör från. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | Det land som de rapporterade uppgifterna härrör från. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | Det utsedda marknadsområde (DMA) som de rapporterade uppgifterna tillskrivs. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | Den PIN-kod (Postal Index Number) som de rapporterade uppgifterna tilldelas. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | Tillståndet som de rapporterade uppgifterna tilldelas till. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | Publiken. Rapporten stöder upp till 10 unika målgrupper. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | Kampanjen. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | Den kreativa personens längd. Rapporten har stöd för upp till 10 unika kreativa längder. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | Enheten. Rapporten stöder upp till 10 unika enheter. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | Typen av feed. Rapporten har stöd för upp till 10 unika feeds-typer. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | Medietypen. Rapporten har stöd för upp till 10 unika medietyper. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | Utgivaren. Rapporten stöder upp till 10 unika utgivare. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | Paketet. <!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | Placeringen.<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | Webbplatsen eller appen där annonsintrycket tjänades. Rapporten har stöd för upp till 10 unika webbplatser eller appar. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | Placeringstaggen som används som en anpassad identifierare för placeringen. Rapporten stöder upp till 10 unika placeringstaggar. <!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | Publiken. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | Kampanjen. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | Den kreativa personens längd. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | Enheten. (som CTV, Desktop etc.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | Medietypen. (som Bildskärm, Ljud osv.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | Utgivaren. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | Placeringen. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | Budgeten för paketresan. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | Slutdatumet för paketflygningen. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | Eventuell överrullningsbudget för paketflygningen. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | Startdatumet för paketflygningen. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | Paketets slutdatum. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | Paketets målbelopp för paketet. Detta belopp utgörs antingen av utgifter eller exponeringar. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | Unik identifierare för paketet i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | Paketets namn |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | Paketets startdatum. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | Placeringens slutdatum. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | (Borttaget) Konverterings-ID som tilldelats av DSP till äldre [!DNL TubeMogul] konverteringshändelser. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | (Föråldrat) Konverteringsnamnet som har tilldelats äldre [!DNL TubeMogul] konverteringshändelser. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | Unik identifierare för placeringen i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | Namnet på placeringen som tilldelats av användaren. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | Placeringsbudgeten. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | Det högsta anbudet för placeringen. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | Placeringens slutdatum. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | Placeringens startdatum. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | Placeringstaggen som används som en anpassad identifierare för placeringen. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | Beskrivningen som är associerad med ett fakturerbart segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | Den unika nyckeln som är associerad med ett fakturerbart segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | Namnet på ett fakturerbart segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | Beskrivningen som är associerad med ett segment, som tillhandahålls av DataProvider. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | Den unika nyckel som är associerad med ett segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | Namnet på ett segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | Namnet på den DataProvider som är associerad med ett segment. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | Unik identifierare för webbplatsen eller appen i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | Platsens namn. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Traffic Type] | Anger om annonsen visades på *[!UICONTROL sites]* eller *[!UICONTROL Apps]*. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | Videolängden, som bearbetas efter överföringen. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | Den unika identifieraren för videokreativiteten i DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | Namnet på den kreativa som tilldelats av användaren. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | [!UICONTROL App/Site Distinct Uniques] delat med [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | Det totala antalet enheter som nåtts endast på den här appen. Ett visningsprogram som visas för en annons över flera utgivare ingår inte i det här värdet. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | [!UICONTROL Total Spend] delat med [!UICONTROL App/Site Distinct Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | [!UICONTROL Total Spend] delat med [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | Den uppskattade procentandel av målgruppen för hushållsuniversum som fick en exponering. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | Genomsnittligt antal visningar som visas för unika. För en del lager skickas ingen enhets-ID och dessa visningar inkluderas inte i det här värdet. Det finns ett liknande mått i rapporten [!UICONTROL Frequency (by App/Site)], men det måttet har inte beräknats. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | (Ingår i rapporten [!UICONTROL Frequency (by Impression)]) De uppskattade intrycken för en viss frekvensbrytning. DSP skattningar bygger på ett urval av visningar. För en del lager skickas ingen enhets-ID och dessa visningar inkluderas inte i det här värdet. Det finns ett liknande mått i rapporten [!UICONTROL Frequency (by App/Site)], men det måttet har inte beräknats. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | (Ingår i rapporten [!UICONTROL Frequency (by Impression)]) Antalet unika webbläsare eller enheter som registrerats för en viss frekvens. DSP skattningar bygger på ett urval av visningar. För en del lager ska du inte skicka med en enhetsidentifierare, och dessa visningar inkluderas inte i det här värdet. Det finns ett liknande mått i rapporten [!UICONTROL Frequency (by App/Site)], men det måttet har inte beräknats. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | Summan av unika hushåll som DSP (auktioner) har sett inom datumintervallet. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | Det totala antalet visningar som fungerade som ett resultat av att ett enhetsdiagram används för personbaserad målinriktning på olika enheter. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | Hur ofta visningar ska göras per hushåll. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | Frekvensen för att nå hushåll med endast den rapporterade dimensionen, inklusive skärningar på upp till tre värden för dimensionen. Om du till exempel använder dimensionen [!UICONTROL Placement] kan du se den frekvens som uppnås av enskilda placeringar, frekvenser som nås av en kombination av två placeringar och frekvenser som nås av kombinationer av tre placeringar. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | Antalet hushåll som bara uppnåddes av den rapporterade dimensionen, beräknat som <code>[IP-adresser som bara uppnåddes av den rapporterade dimensionen] - [IP-adresser som nåtts av någon annan dimension]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | Procentandelen hushåll som bara uppnåddes av den rapporterade dimensionen, beräknad som <code>[procentandelen av IP-adresser som uppnåddes av dimensionen] - [den procentandel IP-adresser som nåddes av någon annan dimension]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | Det totala antalet annonsvisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | Det totala antalet visningar som kunde mätas med avseende på visningsbarhet. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | Det totala antalet mätbara avtryck som endast betjänas av den rapporterade dimensionen, inklusive skärningar på upp till tre värden för dimensionen. Om du till exempel använder dimensionen [!UICONTROL Placement] kan du se de mätbara intrycken som enskilda placeringar uppnår, mätbara exponeringar som uppnås med en kombination av två placeringar och mätbara exponeringar som uppnås med kombinationer av tre placeringar. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | De totala utgifterna. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | Det totala antalet unika hushåll (distinkta IP-adresser) har uppnåtts. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | Det totala antalet unika hushåll (distinkta IP-adresser) som bara uppnås genom den rapporterade dimensionen, inklusive skärningar på upp till tre värden för dimensionen. Om du till exempel använder dimensionen [!UICONTROL Placement] kan du se de unika hushåll som nås av enskilda placeringar, vanliga hushåll nås av en kombination av två placeringar och vanliga hushåll nås av kombinationer av tre placeringar. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | Total utgift dividerad med inkrementell hushålleräna uppnådd. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | Den totala kostnaden dividerad med det unika hushållet har uppnåtts. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | Hur ofta visningar ska göras per hushåll. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | Antalet hushåll som bara uppnåddes av den rapporterade dimensionen, beräknat som [IP-adresser som bara uppnåddes av den rapporterade dimensionen] - [IP-adresser som nåtts av någon annan dimension]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | Procentandelen hushåll som bara uppnåddes av den rapporterade dimensionen, beräknad som [procentandelen av IP-adresser som uppnåddes av dimensionen] - [den procentandel IP-adresser som nåddes av någon annan dimension]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | Det totala antalet annonsvisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | Det totala antalet visningar som kunde mätas med avseende på visningsbarhet. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | De totala utgifterna. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | Det totala antalet unika hushåll (distinkta IP-adresser) har uppnåtts. |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | Måltypen för ID. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | Procentandel av det totala anbudet på Max CPM. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | Genomsnittlig bruttokostnad per förvärv, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | Genomsnittlig bruttokostnad per annonsklickning, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | Genomsnittskostnaden per slutförd videovy, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | Genomsnittlig bruttokostnad per annonsåtagande, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Engagements]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | Genomsnittlig bruttopris per annonsintryck, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | Genomsnittskostnaden per 1 000 visningar, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | Genomsnittskostnaden per videovy, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>, där [!UICONTROL Custom Goal] är den objektiva vikten för alla konverteringar som är kopplade till det anpassade målet. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | Genomsnittskostnaden per 1 000 visningar som kan visas, beräknad med <code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | Genomsnittlig nettokostnad per annonstillfälle, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | Genomsnittlig nettokostnad per slutförd videovy, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | Genomsnittlig nettokostnad per annonsintryck, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | Genomsnittlig nettokostnad per 1 000 visningar, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | Genomsnittlig nettokostnad per videovy, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | Genomsnittlig nettokostnad per 1 000 visningar som kan visas, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | Antalet distinkta användare som DSP erbjuder för placeringen. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | Byråns serviceavgift. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | De totala utgifterna för annonser från Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | Den totala nettokostnaden för informationsavgifter för målgruppssegment som faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | Den totala nettokostnaden för fakturerbara medier, inklusive teknikavgiften, som faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | Den totala kostnaden för andra serviceavgifter (verifieringspartners, annonsvisning och så vidare) som faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | Uppskattad skatt på annonser från Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | Beräknad skatt på kundsegment och datatjänster från tredje part. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | Uppskattad moms på media inklusive moms på återfakturering av mediekostnader och teknisk avgiftsservice i DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | Uppskattad moms på andra serviceavgifter (inklusive verifieringspartners från tredje part, målgruppsanpassning o.s.v.) som faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | Bruttoutgifterna. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | (När marginalhantering är aktiverad) Marginalprocenten, som beräknas av <code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | Summan av icke-fakturerbara och fakturerbara mediekostnader utan några tekniska avgifter. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | Genomsnittlig nettokostnad per 1 000 visningar som kan visas, beräknad med <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | De totala utgifterna för annonser som inte faktureras via Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | Den totala nettokostnaden för informationsavgifter för målgruppssegment som inte faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | Den totala nettokostnaden för icke-fakturerbara medier, inklusive teknikavgiften, som inte faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | Den totala kostnaden för andra serviceavgifter (verifieringspartners, annonsvisning och så vidare) som inte faktureras via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | Summan av [!UICONTROL Billable Spend (Media)], [!UICONTROL Billable Spend (Data)] och [!UICONTROL Billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | Genomsnittlig nettomediekostnad per 1 000 visningar för annonser från Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | De totala fakturerbara och icke fakturerbara utgifterna för annonser från Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | Den genomsnittliga nettodatakostnaden per 1 000 visningar, beräknad med <code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | Den totala nettokostnaden för avgifter för data för målgruppssegment. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | Genomsnittlig nettomediekostnad per 1 000 visningar, beräknad med <code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | Den totala nettokostnaden för media, inklusive teknikavgifter. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | Summan av [!UICONTROL Net Spend (Media)], [!UICONTROL Net Spend (Data)] och [!UICONTROL Net Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | Summan av [!UICONTROL Non-billable Spend (Media)], [!UICONTROL Non-billable Spend (Data)] och [!UICONTROL Non-billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | Genomsnittlig nettokostnad per 1 000 visningar för andra avgifter, beräknad med <code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | Den totala nettokostnaden för andra serviceavgifter (verifieringspartners, annonsvisning och så vidare). |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Clicks] | De totala klickningarna. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL CTR] | Procentandelen klick dividerat med avtryck. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Engagements] | Antalet interaktioner för en serverad annons. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Engagement Rate] | Andelen interaktioner för en serverad annons dividerad med visningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Impressions] | Det totala intrycket. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Media Match Rate] | Den andel av visningar (eller händelser) för vilka den kreativa processen matchades med avsedda medier/inventarier eller målgrupper. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Clicks] | Det totala antalet klick för en viss produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Conversions] | De totala omräkningarna för en viss produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Conversion Rate] | [!UICONTROL Product Conversions] dividerat med [!UICONTROL Product Impressions] som tilldelats en specifik produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product CTR] | [!UICONTROL Product Clicks] dividerat med [!UICONTROL Product Impressions] som tilldelats en specifik produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Impressions] | Det totala intrycket av en viss produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Revenue] | De totala intäkterna för en viss produkt. Använd när dina kreatörer visar flera produkter (till exempel i en karusellannons) och du rapporterar per produkt. |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Revenue] | De totala intäkterna. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | Procentandel av vyerna som tittade på annonsen i dess helhet. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | Antalet vyer som tittade på annonsen i dess helhet. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | Procentandel av visningar som tittade på hela annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | Procentandel av visningar som tittade på minst en fjärdedel av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | Antalet vyer som tittade på minst en fjärdedel av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | Procentandel av visningar som tittade på minst två fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | Antalet vyer som tittade på minst två fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | Procentandelen visningsbara visningar som tittade på minst två kvartilter av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | Procentandel av visningar som tittade på minst tre fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | Antalet visningar som tittade på minst tre fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | Den genomsnittliga procentandel en annons bevakades tills den slutfördes, vilket motsvarar alla vyer. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | Antalet klick på annonsövertäckningen och banners. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | Andelen klick dividerat med annonsvisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | Procentandel av klickningarna delat med videovyer. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | Antalet banderollklickningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | Procentandel klick delat med motsvarande banneravtryck. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | Antalet banneravtryck. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | Den typ av internetanslutning som användes för att visa annonsen (till exempel Wifi eller 4g LTE). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Antalet interaktioner för en serverad annons. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Totalt antal annonsvisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | Den procentandel av visningar som användes som resulterade i videovisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | Den genomsnittliga längden för en videovy, mätt i sekunder. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | Summan av alla klick på en annons. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | Det totala antalet minuter som en videoannons visades. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | Det totala antalet videoannonsvyer. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completion Rate] | (Anpassad Creative-rapport) Procentandel av visningar som tittade på annonsen i dess helhet. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completions] | (Anpassad Creative-rapport) Antalet visningar som tittade på annonsen i dess helhet. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completion Rate] | (Anpassad Creative-rapport) Procentandel av visningar som tittade på minst en fjärdedel av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completions] | (Anpassad Creative-rapport) Antalet visningar som tittade på minst en fjärdedel av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completion Rate] | (Anpassad Creative-rapport) Procentandel av visningar som tittade på minst två fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completions] | (Anpassad Creative-rapport) Antalet visningar som tittade på minst två fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completion Rate] | (Anpassad Creative-rapport) Procentandel av visningar som tittade på minst tre fjärdedelar av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completions] | (Anpassad Creative-rapport) Antalet visningar som tittade på minst tre kvartilter av annonsen. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Avg Percent Viewed] | (Anpassad Creative-rapport) Den genomsnittliga procentandel en annons har bevakats tills den är klar, och alla vyer redovisas. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Play Rate] | (Anpassad Creative-rapport) Procentandel av visningar som resulterade i videovisningar. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Playtime per View] | (Anpassad Creative-rapport) Den genomsnittliga längden för en videovy, mätt i sekunder. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Mute] | (Anpassad Creative-rapport) Det totala antalet gånger som videon stängdes av. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Pause] | (Anpassad Creative-rapport) Det totala antalet gånger som videon pausades. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Resume] | (Anpassad Creative-rapport) Det totala antalet gånger som videon återupptogs efter pausning. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Rewind] | (Anpassad Creative-rapport) Det totala antalet gånger som videon spolades tillbaka. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Start] | (Anpassad Creative-rapport) Det totala antalet gånger som videon startades. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Unmute] | (Anpassad Creative-rapport) Det totala antalet gånger som videon togs bort. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Viewed Minutes] | (Anpassad Creative-rapport) Det totala antalet minuter en videoannons visades. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Views] | (Anpassad Creative-rapport) Det totala antalet videoannonsvyer. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | Genomsnittlig spelarbredd och -höjd. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | Det totala antalet visningar som kunde mätas med avseende på visningsbarhet. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | Procentandel av visningar som kunde mätas för visningsbarhet, beräknat som <code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | Procentandel av visningar som inte kan mätas för visning på grund av inkompatibla iFrames. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | Antalet visningar som inte kan mätas för att de ska visas på grund av att annonsens visningsspårning inte stöds. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | Procentandel av visningar som inte kan mätas för att se dem på grund av andra orsaker. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | Antalet annonsvisningar som inte kan mätas för att se dem. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | Andelen annonsvisningar som inte kan mätas för att se dem. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | Procentandel av visningar som inte kan mätas för visning på grund av att visningsspårning inte stöds för annonsenheten. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | Procentandel av visningar som kan visas av alla mätbara visningar, beräknat som <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | Det antal annonsvisningar som kan visas. |
| [!UICONTROL Conversion Metrics] | [Grupperad av annonsören i rapportinställningarna] | [Annonsspecifik konvertering] | Summan för en angiven annonsörspecifik konverteringsmetod eller Adobe Analytics-händelse. |
| [!UICONTROL Custom Goals] | [Grupperad av annonsören i rapportinställningarna] | [Advertiser-specifikt anpassat mål] | Den viktade summan av alla konverteringar som ingår i det angivna [anpassade målet](/help/dsp/optimization/custom-goal.md). |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Duplicera en anpassad rapport](/help/dsp/reports/report-copy.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
