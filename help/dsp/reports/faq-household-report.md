---
title: Frågor och svar om hushållsrapporter
description: Läs mer om hushållens räckvidd, frekvens och konverteringsdata, inklusive hur hushållsrapporterna skiljer sig från andra rapporter och felsökning.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: ae6028d7dc9b35906e4abcd727b84b169e5594b1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Frågor och svar om hushållsrapporter

## The [!UICONTROL Household Reach & Frequency] Rapport

### Hur [!UICONTROL Household Reach & Frequency] rapporter som skiljer sig från andra anpassade rapporter?

The [!UICONTROL Household Reach & Frequency] Rapportera mått som omfattar räckvidd, intryck och frekvens i olika dimensioner på hushållsnivå baserat på IP-adressen. De andra anpassade rapporterna genereras på enhets- eller cookie-nivå.

Till exempel, även om ett intryck ges till tre enheter i ett hushåll, är det unika hushållets mätvärde ett.

#### Dimensioner som stöds

The [!UICONTROL Household Reach & Frequency] rapporten har stöd för [följande dimensioner](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (som inte ger tillgång till överlappningsstatistik), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length]och placeringen &quot;[!UICONTROL Tags].&quot; |

#### Mätvärden som stöds

The [tillgängliga mått](/help/dsp/reports/report-columns.md) inkludera:

* Överlappningsmått: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]och [!UICONTROL Unique Household (Overlap)].

  Överlappningsmått är de värden som bara förekommer för den rapporterade dimensionen eller kombinationen av dimensioner, och inte för andra dimensioner. <!-- For example, it might show the ?? -->

* Mätvärden som inte överlappar: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]och [!UICONTROL Unique Household Reached]

Konverteringsstatistik och anpassade mål stöds inte.

### Vad är skillnaden mellan överlappnings- och icke-överlappningsstatistik?

Följande bild visar tre mätvärden (Unique Household Reached, Incremental Household Reached, and Incremental Household (Overlap)) för tre kampanjer (A, B och C).

![Illustration av överlappningsstatistik för hushåll](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration av överlappningsstatistik för hushåll")

* Unikt hushåll uppnått (totalt) är det unika hushåll som nås av var och en av kampanjerna eller det totala området för var och en av cirklarna. I figuren uppnåddes ett unikt hushåll som nås av A = inkrementellt hushåll som nås av A + (A+B) + (A+C) +(A+B+C)

* Inkrementellt hushållet är det unika hushållet som bara har uppnåtts genom en kampanj. I denna siffra är det inkrementella hushåll som nås av A, B, C det inkrementella hushåll som nås av A, B respektive C.

* Inkrementellt hushåll (överlappning) är det unika hushåll som nås av kampanjen eller kombinationen av kampanjer. I figuren är det inkrementella hushållet som A, C, når A+C.

### Arbetsflöde

Följ de normala stegen för att [skapa en anpassad rapport](report-create.md).

The [!UICONTROL Household Reach & Frequency] -rapporten kan bara innehålla en dimension. Den kan även innehålla antingen a) överlappningsmått av alla dimensioner förutom för Site/Apps eller b) icke-överlappningsmått, men inte båda.

### Vilka begränsningar finns för [!UICONTROL Household Reach & Frequency] rapportera?

Rapporter med överlappande mätvärden som ger utdataöverlappningar på upp till tre värden. Om du till exempel använder måttet [!UICONTROL Unique Household (Overlap)] för 10 praktik kan du se de unika hushåll som nås av enskilda placeringar, vanliga hushåll nås genom en kombination av två praktikanter och vanliga hushåll nås genom kombinationer av tre praktikanter. Du kan inte se vanliga hushåll nås med fyra eller fler placeringar.

För andra dimensioner än kampanj, paket eller placering stöder rapporten upp till 10 värden i varje dimension. Om du till exempel vill skapa en [!UICONTROL Unique Household Reached] rapport för [!UICONTROL Audience] måste antalet unika målgrupper vara mindre än eller lika med 10. Om ni inkluderar fler än 10 unika målgrupper genereras en tom rapport.

### Varför skiljer sig frekvensen och de unika värdena för räckvidd mellan [!UICONTROL Custom] rapporter och [!UICONTROL Household Reach & Frequency] rapportera?

De här mätvärdena [!UICONTROL Household] rapporter beräknas med det faktiska antalet IP-adresser, medan mätvärdena i [!UICONTROL Custom] rapporten använder uppskattade tal beräknade med modeller. Skillnaden bör dock vara mindre än 10 procent.

### Hur konfigurerar jag rapporten för [!UICONTROL Placement Tags] dimension?

Om du vill skapa taggar för placeringen [öppna placeringsinställningarna](/help/dsp/campaign-management/placements/placement-edit.md) och ange värden i [Fältet Placeringstaggar](/help/dsp/campaign-management/placements/placement-settings.md).

När en placering innehåller flera taggar betraktas hela strängen som en tagg. Rapporten innehåller en rad för varje unik sträng.

## The [!UICONTROL Household Conversions] Rapport

### Vilka typer av attribueringsmetoder stöds i [!UICONTROL Household Conversions] rapportera?

Två typer av attribueringsmetoder stöds:

* Unik: Räknar antalet gånger som ett dimensionsvärde (till exempel en enhet eller placering) var på vägen till konverteringen.

* MTA (Multi-Touch Attribution): Fördelar krediten för varje konvertering baserat på frekvensen för förekomsten av dimensionsvärdet (till exempel en enhet eller placering) på sökvägen till konverteringen. Om det till exempel fanns totalt 10 visningar före konverteringen, med 8 på CTV och 2 på Mobile, ges 80 % av krediten (0,8) till CTV-skärmar och 0,2 till Mobile.

### Hur skiljer sig rapporteringen om hushållskonvertering från rapporter om CTV-visning i Adobe Analytics?

CTV-tittardata i [!DNL Analytics] är strömförsörjd [!DNL Analytics] spårning och data för hushållskonvertering använder data som samlats in med hjälp av spårning av konvertering till Adobe Advertising. Dessutom DSP attribueringslogiken i [!DNL Analytics] använder bara den sista händelsen, men hushållskonverteringsrapportering stöder två olika attribueringsmetoder: Unikt och MTA.

### Kan jag visa CTV-vydata i båda [!DNL Analytics for Advertising] och i anpassade rapporter?

Annonsörer utan [!DNL Analytics for Advertising] kan endast använda rapporten för hushållskonvertering för rapportering av hushållskonvertering.

Om din organisation har [!DNL Analytics for Advertising], använder båda typerna av rapportering tillsammans. Visningsrapportering för CTV passar bra för breda kanalanalyser, webbplatsbeteenden och så vidare, men anpassade rapporter ger en detaljerad bild (med data uppdelade efter medietyp, utgivare och så vidare) för att ange de faktorer som driver konverteringsgraden.

## [!UICONTROL Household Reach & Frequency] och [!UICONTROL Household Conversions] Rapporter jämfört med data från [!DNL Advanced Measurement Services]

För avancerade rapporter om hushållsbaserad räckvidd och frekvens eller konverteringar finns [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) kan tillhandahålla anpassningsbara rapporter tillsammans med övergripande strategiska rekommendationer. Mer information om [!DNL Advanced Measurement Services]kontaktar du kontoteamet på Adobe.

### Om jag redan använder [!DNL Advanced Measurement Services], varför ska jag använda [!UICONTROL Household Reach & Frequency] och [!UICONTROL Household Conversions] rapporter?

The [!UICONTROL Household Reach & Frequency] och [!UICONTROL Household Conversions] rapporter ger kunderna möjlighet att i realtid utnyttja sin räckvidd, frekvens och konverteringsgrad på egen hand.

### Kan jag använda båda [!UICONTROL Household Reach & Frequency] och [!UICONTROL Household Conversions] rapporter och [!DNL Advanced Measurement Services]?

Det bästa användningssättet är att använda båda [!UICONTROL Household] rapporten och [!DNL Advanced Measurement Services] Rapporterings- och konsulttjänster tillsammans. Tänk på [!UICONTROL Household] rapportera som transaktioner, som ska vara till hjälp vid dagliga optimeringar, och [!DNL Advanced Measurement Services] som mer strategiskt, avsett att fungera som grund för helhetslärande och arbetssätt knutna till övergripande affärsmål.

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
