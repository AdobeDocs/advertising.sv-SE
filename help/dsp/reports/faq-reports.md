---
title: Vanliga frågor om anpassade rapporter
description: Läs mer om anpassade rapporter, inklusive hushållsrapporter och rapporter om konverteringsmetoder.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# Vanliga frågor om anpassade rapporter

## Hushållsrapporter

### Rapporten [!UICONTROL Household Reach & Frequency]

#### Hur skiljer sig [!UICONTROL Household Reach & Frequency]-rapporter från andra anpassade rapporter?

[!UICONTROL Household Reach & Frequency]-rapportmåtten når, gör intryck och frekvens i olika dimensioner på hushållsnivå baserat på IP-adressen. De andra anpassade rapporterna genereras på enhets- eller cookie-nivå.

Till exempel, även om ett intryck ges till tre enheter i ett hushåll, är det unika hushållets mätvärde ett.

##### Dimensioner som stöds

Rapporten [!UICONTROL Household Reach & Frequency] har stöd för [följande dimensioner](/help/dsp/reports/report-columns.md): [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Site/Apps] (som inte ger åtkomst till överlappningsmått), [!UICONTROL Media Type], [!UICONTROL Feed Type], [!UICONTROL Device], [!UICONTROL Publisher], [!UICONTROL Audience], [!UICONTROL Creative Length] och placering som skapats av användare &quot;[!UICONTROL Tags].&quot; |

##### Mätvärden som stöds

[Tillgängliga värden](/help/dsp/reports/report-columns.md) inkluderar:

* Överlappa mått: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] och [!UICONTROL Unique Household (Overlap)].

  Överlappningsmått är de värden som bara förekommer för den rapporterade dimensionen eller kombinationen av dimensioner, och inte för andra dimensioner. <!-- For example, it might show the ?? -->

* Mätvärden som inte överlappar: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] och [!UICONTROL Unique Household Reached]

Konverteringsstatistik och anpassade mål stöds inte.

#### Vad är skillnaden mellan överlappnings- och icke-överlappningsstatistik?

Följande bild visar tre mätvärden (Unique Household Reached, Incremental Household Reached, and Incremental Household (Overlap)) för tre kampanjer (A, B och C).

![Illustration av överlappningsstatistik för hushåll](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration av överlappningsstatistik för hushåll")

* Unikt hushåll uppnått (totalt) är det unika hushåll som nås av var och en av kampanjerna eller det totala området för var och en av cirklarna. I figuren uppnåddes ett unikt hushåll med A = inkrementellt hushåll som nås av A + (A+B) + (A+C) +(A+B+C)

* Inkrementellt hushållet är det unika hushållet som bara har uppnåtts genom en kampanj. I denna siffra är det inkrementella hushåll som nås av A, B, C det inkrementella hushåll som nås av A, B respektive C.

* Inkrementellt hushåll (överlappning) är det unika hushåll som nås av kampanjen eller kombinationen av kampanjer. I figuren är det inkrementella hushållet som A, C, når A+C.

#### Arbetsflöde

Följ de normala stegen för att [skapa en anpassad rapport](report-create.md).

Rapporten [!UICONTROL Household Reach & Frequency] kan bara innehålla en dimension. Den kan även innehålla antingen a) överlappningsmått av alla dimensioner förutom för Site/Apps eller b) icke-överlappningsmått, men inte båda.

#### Vilka begränsningar finns för rapporten [!UICONTROL Household Reach & Frequency]?

Rapporter med överlappande mätvärden som ger utdataöverlappningar på upp till tre värden. Om du till exempel använder måttet [!UICONTROL Unique Household (Overlap)] för 10 praktik kan du se de unika hushåll som nås av enskilda placeringar, vanliga hushåll nås genom en kombination av två placeringar och vanliga hushåll nås genom kombinationer av tre placeringar. Du kan inte se vanliga hushåll nås med fyra eller fler placeringar.

För andra dimensioner än kampanj, paket eller placering stöder rapporten upp till 10 värden i varje dimension. Om du till exempel vill generera en [!UICONTROL Unique Household Reached]-rapport för dimensionen [!UICONTROL Audience] måste antalet unika målgrupper vara mindre än eller lika med 10. Om ni inkluderar fler än 10 unika målgrupper genereras en tom rapport.

#### Varför skiljer sig frekvensen och unika värden för räckvidd mellan mina [!UICONTROL Custom]-rapporter och [!UICONTROL Household Reach & Frequency]-rapporten?

Dessa mått i [!UICONTROL Household]-rapporter beräknas med det faktiska antalet IP-adresser, medan måtten i [!UICONTROL Custom]-rapporten använder beräknade tal som beräknas med modeller. Skillnaden bör dock vara mindre än 10 procent.

#### Hur konfigurerar jag rapporten för dimensionen [!UICONTROL Placement Tags]?

Om du vill skapa taggar för placeringen [öppnar du placeringsinställningarna](/help/dsp/campaign-management/placements/placement-edit.md) och anger värden i fältet [Placeringstaggar](/help/dsp/campaign-management/placements/placement-settings.md).

När en placering innehåller flera taggar betraktas hela strängen som en tagg. Rapporten innehåller en rad för varje unik sträng.

### Rapporten [!UICONTROL Household Conversions]

#### Vilka attribueringsmetoder stöds i [!UICONTROL Household Conversions]-rapporten?

Två typer av attribueringsmetoder stöds:

* [!UICONTROL Unique]: Räknar antalet gånger som ett dimensionsvärde (till exempel en enhet eller placering) fanns på sökvägen till konverteringen.

* [!UICONTROL Multi-Touch Attribution (MTA)]: Distribuerar krediten för varje konvertering baserat på frekvensen för förekomsten av dimensionsvärdet (till exempel en enhet eller placering) på sökvägen till konverteringen. Om det till exempel fanns totalt 10 visningar före konverteringen, med 8 på CTV och 2 på Mobile, ges 80 % av krediten (0,8) till CTV-skärmar och 0,2 till Mobile.

#### Hur skiljer sig rapporteringen om hushållskonvertering från rapporter om CTV-visning i Adobe Analytics?

* I [!DNL Analytics] visar [!DNL CTV View-Through Conversion]-rapporten antalet konverteringar för vilka ett CTV-intryck var den sista kontaktytan före konverteringen. DSP [!UICONTROL Household Conversions]-rapporten visar däremot antalet unika hushåll som exponerats för en CTV-bild vid någon tidpunkt inom det definierade uppslagsfönstret före konverteringen.

* I [!DNL Analytics] tilldelar attribueringslogiken konverteringar exklusivt till den sista kontaktytan från Adobe Advertising. DSP [!UICONTROL Household Conversions]-rapporten har däremot stöd för ytterligare attribueringsmodeller, *[!UICONTROL Unique]* och *[!UICONTROL Multi-Touch Attribution (MTA)]*.

* [!DNL Analytics]-rapportdata är särskilt värdefulla för att analysera via marknadsföringskanaler, interaktionsstatistik för webbplatser och så vidare. DSP [!UICONTROL Household Conversions]-rapporten ger mer detaljerade insikter genom att tillåta att konverteringsdata delas upp efter olika dimensioner, till exempel medietyp och utgivare.

### [!UICONTROL Household Reach & Frequency] och [!UICONTROL Household Conversions] Rapporter jämfört med data från [!DNL Advanced Measurement Services]

För avancerade rapporter om hushållsbaserad räckvidd och frekvens eller konverteringar kan [[!DNL Strategic Advertising Consulting] teamet](/help/dsp/introduction/advanced-measurement-services.md) tillhandahålla anpassningsbara rapporter tillsammans med övergripande strategiska rekommendationer. Mer information om [!DNL Advanced Measurement Services] får du av ditt Adobe-kontoteam.

#### Om jag redan använder [!DNL Advanced Measurement Services], varför ska jag använda [!UICONTROL Household Reach & Frequency]- och [!UICONTROL Household Conversions]-rapporterna?

[!UICONTROL Household Reach & Frequency]- och [!UICONTROL Household Conversions]-rapporterna ger klienter möjlighet att hämta värden för räckvidd, frekvens och konvertering på hushållsnivå oberoende i realtid.

#### Kan jag använda både [!UICONTROL Household Reach & Frequency]- och [!UICONTROL Household Conversions]-rapporterna och [!DNL Advanced Measurement Services]?

Det bästa användningsexemplet är att använda både [!UICONTROL Household]-rapporten och [!DNL Advanced Measurement Services]-rapporterings- och konsulttjänsterna tillsammans. Se rapporten [!UICONTROL Household] som en transaktion, som är avsedd att informera om dagliga optimeringar och [!DNL Advanced Measurement Services] som mer strategiska, som är avsedda att informera helhetsintryck och aktiviteter kopplade till övergripande affärsmål.

## Analysrapporter för konverteringssökväg

### Hur fungerar rapporten Sökväg till konvertering jämfört med rapporter som skapats av [!DNL Advanced Measurement Services] och Adobe Analytics Analysis Workspace?

| | Sökväg till konverteringsrapport | Haloeffekt för Advanced Measurement Services i sökrapporter | Rapporter i Analysis Workspace |
| --- | --- | --- |---|
| Kundvärde | Generera en självbetjäningsrapport för att förstå vilka vägar i annonsen som ledde till fler konverteringar för att öka optimeringen | Förstå hur uppkopplad TV-taktik påverkar sökklickningar | Förstå effekten av er helhetsbaserade investering i Adobe Advertising, tillsammans med andra marknadsföringskanaler, på sökklick |
| Hushållsnivå | Ja | Ja | Nej |
| Stöds CTV? | Ja | Ja | Ja |
| Attributionsmetod | Den sista pekhändelsen (intrycket eller klickningen) måste finnas i sökboksfönstret. | Uniques | Senaste beröring |
| | Interaktionspunkter mer än 30 dagar innan senaste beröringshändelsen beaktas för konverteringsbanan. | (CTV får kredit, oavsett var CTV-exponeringen sker i användarens väg-till-klick) | (CTV får kredit om intrycket är den sista händelsen i uppslagsfönstret OCH det inte finns någon betald klickning från andra format, varken före eller efter CTV-exponering) |
| Rapporteringsnivå | Granulat | Granulat | Bred |
| | (Kanaltyp, Creative/Ad, Nyckelord, Banor, Längd, Tid för konvertering) | (CTV Tactic, CTV App/Publisher) | (Adobe Advertising och andra marknadsföringskanaler) |
| Marknadsföringskanaler | DSP + Search (från Search, Social och Commerce) | DSP + Search (från Search, Social och Commerce) | Marknadsföringskanaler som inte spåras av Adobe Advertising klickbara EF-ID (som Organic Search, Organic Social, Email och Affiliate) |
| Konverteringsmått som stöds | Mätvärden som spåras med hjälp av Adobe Advertising händelsepixel (AMO ID) och Adobe Analytics tracking | Klicka (inga konverteringar) | Mätvärden som spåras med hjälp av Adobe Analytics tracking |

Mer information om haloeffekten för Advanced Measurement Services i sökrapporter finns i [Advanced Measurement Services](/help/dsp/introduction/advanced-measurement-services.md).

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
