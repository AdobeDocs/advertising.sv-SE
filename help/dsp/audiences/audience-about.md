---
title: Om Audience Management i DSP
description: Läs om funktioner för målgruppshantering.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 94c41ec311ed79897e1e26a650605c0213450071
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---

# Om Audience Management i DSP

I DSP kan ni skapa och hantera målgruppssegment och målgruppsuppsättningar, som ni kan använda som mål för era ersättningar:

* Samla in egna data från förstahandsmålgrupper genom att skapa och implementera DSP. Du kan senare rikta om användare i segmentet med annonser eller hindra användare i segmentet från att ta emot annonser. Du kan skapa följande typer av segment:

   * [Egna segment](/help/dsp/audiences/custom-segment-create.md) spåra a) användare som exponeras för annonser från datorer och mobila enheter och b) användare som besöker specifika webbsidor. Spårningstaggen kan spåra antingen cookie-baserade användare eller användare som är kopplade till universella ID:n för ID5.

   * [CCPA-segment för avstående från försäljning](/help/dsp/audiences/ccpa-opt-out-segment-create.md) för att spåra användar-ID:n från förfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA). Du kan hämta månadsrapporter om användar-ID:n från begäranden om att avanmäla dig.

     Mer information om stöd för CCPA-begäran om avanmälan finns i Adobe Advertising [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Betafunktion) [Hämta och använda universella ID:n för cookiefri målinriktning](/help/dsp/audiences/universal-ids.md):

   * Skicka autentiserade dokument manuellt [!DNL LiveRamp] [!DNL RampID] segment direkt till DSP.

   * Tillåt DSP att importera förstahandssegment från kunddataplattformen och översätta dem till universella ID-typer som stöds.

   * Inkludera tredjepartssegment som innehåller universella ID:n i dina placeringsmål utan några extra steg.

* Skapa ett målgruppsbibliotek med [återanvändbara målgrupper](/help/dsp/audiences/reusable-audience-create.md). Sparade målgrupper består av alla era tillgängliga målgruppssegment och alla era andra sparade målgrupper. Alla ändringar du gör för en sparad målgrupp tillämpas automatiskt på alla placeringar som riktar sig till eller utesluter målgruppen och på alla andra målgrupper som inkluderar den sparade målgruppen.

  Med sparade målgrupper kan mediemanners gruppera målgrupper efter behov genom att inkludera och exkludera flera segment med komplex boolesk logik. Storleken på varje enskilt segment och den totala målgruppsstorleken anges när du skapar en målgrupp. Kampanjcheferna kan sedan välja en eller flera sparade målgrupper som placeringsmål i stället för att manuellt konfigurera målgrupper för varje placering.

Det finns även andra typer av målgrupper att tillgå för riktad marknadsföring.

## Importera datasegment från första och tredje part

Det finns många alternativ för att importera data från första part och tredje part till DSP, via det DSP användargränssnittet och/eller via anpassade importtjänster.

* DSP kan dra in din Adobe Audience Manager och andra [!DNL Adobe] målgrupper för målinriktning. Information om krav och instruktioner finns i &quot;[Importera Adobe Audience Manager-segment för annonsinriktning](/help/integrations/audience-manager/import-audiences.md).

* DSP kan översätta datasegment från första part från de kunddataplattformar som stöds till segment med universella ID:n med [Funktionen Källor](/help/dsp/audiences/sources/source-about.md). Du kan också [skicka dina autentiserade [!DNL LiveRamp] [!DNL RampID] segment direkt till DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kan importera dina andra datasegment från första part direkt från datahanteringsplattformen (DMP) och tillhandahålla dem till alla typer av annonsörer efter behov.

* DSP kan importera egna tredjepartssegment, inklusive komplexa kombinationer av tredjepartssegment. Ni kan vid behov tillhandahålla segmenten till valfri uppsättning annonsörer.

Kontakta kontoteamet på Adobe för mer information.

## Målgrupper som är tillgängliga som placeringsmål

Du kan rikta dina placeringar till alla följande typer av målgrupper.

* Alla användarskapade målgruppsuppsättningar som sparades i DSP.

* Alla användarskapade målgruppssegment som skapades i DSP:

   * Anpassade segment för användare som besökte specifika webbsidor och användare som exponerats för visningar av specifika annonser.

     Inga avgifter tas ut för visningar som skickas till universella ID:n.

   * CCPA-målgruppssegment för avanmälan av försäljning för användare som lämnat in begäran om avanmälan av försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA).

* Alla importerade datasegment från första part, inklusive segment som har översatts till universella ID:n.

  Ytterligare avgifter tas ut för visningar som skickas till universella ID:n. Se &quot;[Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)&quot; för priser.

* Alla importerade anpassade datasegment från tredje part.

* (Endast praktik i USA) [Alla tredjepartsdatasegment som är tillgängliga för DSP kunder från över 30 leverantörer](/help/dsp/audiences/third-party-data-providers.md), inklusive [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]och många fler.

  Du kan rikta in dig på specifika segment, som riktar sig till användare baserat på målgruppsdata (t.ex. användare med specifika demografiska profiler, intressen eller avsikter samt/eller beteendeprofiler). Du kan bläddra efter dataleverantör och kategori, söka efter segment efter namn eller segment-ID eller filtrera resultaten efter dataleverantör, total segmentstorlek, webbläsarantal eller antal enheter.

  Extra avgifter tillkommer för segment från tredje part, vilket anges bredvid varje segmentnamn.

* (Annonsörer med Adobe Experience Platform och [!DNL Real-Time CDP], Adobe Audience Manager eller Adobe Analytics som endast använder JavaScript-konverteringstaggar i Adobe Advertising) Alla tillgängliga första-, andra- eller tredjepartssegment som skapats i [!DNL Real-Time CDP], skapat i Audience Manager eller publicerat till Adobe Experience Cloud från Audience Manager eller [!DNL Analytics].

  Priset för segmenten är förförhandlat och syns inte i DSP.

  Segment från [!DNL Analytics] är tillgängliga ungefär en timme efter att du har skapat eller publicerat dem som Experience Cloud-målgrupper. Segment som kommer direkt från Audience Manager eller [!DNL Real-Time CDP] är tillgängliga inom 24 timmar efter att du delat dem.

  >[!NOTE]
  >
  >Läs dokumentationen för [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analyser](https://experienceleague.adobe.com/docs/analytics.html)och [den [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) för information om hur du ställer in och samlar in data för segment i dessa lösningar.

## Målgruppsstorleksdata

I Publiker > Alla målgrupper och i avsnittet Målgruppsanpassning i placeringsinställningarna kan du filtrera varje segmentlista efter storleksintervall, inklusive det totala intervallet och separata intervall för specifika enhetstyper eller universella ID-typer.

![filtrera efter målgruppsstorlek](/help/dsp/assets/audience-size-filter.png)

Du kan även se detaljerade data om målgruppsstorlek:

* Den totala och aktiva borttagna dubblettstorleken för alla valda segment och sparade målgrupper visas, och du kan visa information per enhetstyp (webbläsare, mobil eller ansluten TV).

  ![den kombinerade publiken](/help/dsp/assets/audience-size.png)

* För enskilda segment visas den totala målgruppsstorleken och CPM (om tillämpligt) bredvid segmentnamnet.

  ![den enskilda segmentstorleken](/help/dsp/assets/audience-size-segment.png)

* Du kan visa mer information om ett enskilt segment eller en sparad publik, inklusive storleken per webbläsare, mobil, ansluten TV och partner för universella ID. För sparade målgrupper är den totala storleken den deduplicerade summan.

  ![information om enskilda segment eller sparade målgrupper](/help/dsp/assets/audience-size-segment-details.png)

## Målgruppsvyer

### Vyn Alla målgrupper

I [!UICONTROL All Audiences] för , eller Audience Library, kan ni spara och hantera återanvändbara målgrupper, som innefattar grupper av målgruppssegment och till och med andra sparade målgrupper. Du kan använda målgrupper som mål för flera placeringar. Antalet placeringar där varje målgrupp används anges bredvid placeringsnamnet.

Du kan redigera, klona, ta bort, exportera och dela vilken målgrupp som helst.

### Segmentvyn

I [!UICONTROL Segments] kan alla användare skapa ytterligare anpassade segment.

The [!UICONTROL Segments] I visas även följande segmenttyper:

* Alla användarskapade anpassade segment är tillgängliga för användaren.

  Du kan visa spårningstaggar för alla anpassade segment som du har skapat och dela dessa segment med andra användare. Du kan också redigera eller ta bort de anpassade segment som du har skapat.

  Du kan inte redigera eller dela anpassade segment som andra användare har delat med dig.

* Alla segment från första part som importeras i befintligt skick och som är tillgängliga för användaren.

  Du kan inte redigera eller dela egna segment som delats med dig. Kontakta Adobe Account Team om du behöver dela egna segment med andra användare.

* Alla anpassade tredjepartssegment som är tillgängliga för användaren.

  Du kan inte redigera eller dela tredjepartssegment som delats med dig. Kontakta kontoteamet på Adobe om du behöver dela segment från tredje part med andra användare.

### Vyn Källor

I [!UICONTROL Sources] kan du konfigurera källor för förstahandssegment på de kunddataplattformar som stöds och som du vill konvertera till segment som innehåller angivna universella ID-typer. Källinställningarna innehåller en automatiskt genererad källnyckel som du skickar till din kunddataplattform för att upprätta anslutningen.

Mer information om vilka kunddataplattformar som stöds, vilka universella ID-typer som stöds samt arbetsflödena för att konfigurera anslutningar till varje kunddataplattform finns i &quot;[Om källor](/help/dsp/audiences/sources/source-about.md).&quot;

De översatta segmenten är tillgängliga för att inkluderas i återanvändbara målgrupper och i placeringsinställningar för cookiefri målinriktning.

>[!MORELIKETHIS]
>
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
