---
title: Stöd för aktivering av universella ID
description: Lär dig mer om stöd för import av era universella ID-segment, skapa anpassade segment för att spåra universella ID:n och konvertera andra användaridentifierare i era förstapartssegment till universella ID:n för cookiefri anpassning.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Stöd för aktivering av universella ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Funktionen Beta*

DSP har stöd för personbaserade, universella ID:n för cookiefri anpassning till olika digitala format som stöds av DSP.

* Du kan skicka din autentiserade [[!DNL LiveRamp] [!DNL RampIDs]] direkt till DSP med [!DNL LiveRamp] [!DNL Connect] kontrollpanel. Se &quot;[Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP kan importera era egna segment som består av hash-kodade e-post-ID:n som är byggda i kunddataplattformen (CDP) och konvertera dem till [!DNL LiveRamp] [!DNL RampIDs] och [!DNL Unified ID 2.0 (UID2.0)] ID. Mer information om vilka kunddataplattformar som stöds, vilka funktioner som är tillgängliga för alla universella ID-typer som stöds samt relaterade arbetsflöden finns i &quot;[Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md).&quot;

* Du kan skapa anpassade segment som spårar användare som är kopplade till universella ID:n för ID5 som exponeras för annonser från datorer och mobila enheter och som besöker specifika webbsidor. ID5 använder en sannolikhetsmodell för att tilldela ett ID som härleds från olika användarsignaler och webbläsarsignaler. Instruktioner finns i &quot;[Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md).&quot;

* Tredjepartssegment från vissa leverantörer kan automatiskt inkludera universella ID:n utöver användare som spåras med cookies eller enhets-ID:n. Till exempel segment från [!DNL Eyeota] kan automatiskt inkludera ID5-ID:n och segment från [!DNL Lotame] kan innehålla UID2.0-ID. Segmentinformationen innehåller storleken för varje typ. Den vanliga användaravgiften för varje segment, som anges bredvid segmentnamnet, gäller. Inga ytterligare avgifter tas ut för ID5-ID:n.

## Rapportering efter typ av universellt ID

* **Anpassade rapporter:** Kostnads-, intrycks-, klicknings-, konverterings- och frekvensdata per universell ID-typ är tillgängliga i anpassade rapporter.

* **[!DNL Analytics]rapporter:** Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) som har implementerat alla nödvändiga steg kan se genomskinlighetskonverteringar med universaltyp i [!DNL Analytics].

  >[!IMPORTANT]
  >
  >För korrekt konverteringsattribuering bör du se till att klicknings-URL:erna för dina annonser innehåller båda [EF-ID och AMO-ID](/help/integrations/analytics/ids.md).

* **Segmentinformation:** För alla segmenttyper omfattar segmentinformationen målgruppens storlek efter typ av universellt ID och efter den enhetstyp som spåras av cookies eller enhets-ID.

## Använda ett universellt ID som målgrupp i dina praktikanter

>[!NOTE]
>
>Du kan inte ändra måltypen för ID i en direktplacering. Om det behövs kan du duplicera en aktiv placering och ändra typerna av mål-ID på den nya placeringen.

Gör följande i en ny, schemalagd eller pausad placering:

1. I [!UICONTROL Geo-Targeting] Ange de geografiska områden som ska vara mål. Varje partner för universella ID tillåter endast målgruppsanpassning i specifika geografiska områden, och endast giltiga ID-typer är tillgängliga i [!UICONTROL Targeting] inställningar.

1. I [!UICONTROL Audience Targeting] gör du följande:

   1. I [!UICONTROL Included Audiences] väljer du det segment för vilket användardata konverterades till universella ID.

      Du kan inkludera ytterligare segment om du vill.

   1. I [!UICONTROL Targeting] inställningar:

      1. Välj den universella ID-typ som du vill använda som mål.

         Inställningen innehåller alternativen &quot;[!UICONTROL Legacy IDs]och &quot;[!UICONTROL Universal ID],&quot; som kan innehålla underalternativen &quot;[!UICONTROL ID5],&quot;[!UICONTROL RampID],&quot; och &quot;[!UICONTROL Unified ID2.0].&quot; De valda geografiska målen avgör vilka delalternativ som är tillgängliga.

         Du kan välja båda[!UICONTROL Legacy IDs]och &quot;[!UICONTROL Universal ID],&quot; men du kan bara välja en typ av universellt ID per placering. När du väljer både äldre ID:n och universella ID:n ges budgivningsinställningar till universella ID:n.

      1. (Om det behövs) Acceptera villkoren i serviceavtalet för användning av universella ID:n.

         Innan du kan konvertera data till en ny ID-typ måste en användare på DSP acceptera villkoren i serviceavtalet. Villkoren får bara godkännas en gång per ID-typ, per konto.

Se &quot;[Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Bästa metoder för testning och dataverifiering

Använd följande metodtips för [!DNL RampID]-baserade segment och ID5-baserade segment, för vilka Adobe Analytics-mätningar är tillgängliga.

* Ungefär 24 timmar efter att du har aktiverat ett segment ska du kontrollera antalet konverterade ID:n för segmentet inom [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Kontakta ditt kontoteam på Adobe om ID-antalet är oväntat.

  Se &quot;[Datavariationer mellan e-post-ID och universella ID](#universal-ids-data-variances)&quot; för mer information om hur antalet segment kan variera.

* Ändra inte befintliga paket och placeringar. Om du inte har någon ytterligare budget för att testa universella ID:n ska du minska den ursprungliga budgeten för att finansiera testerna.

* Kopiera dina originalpaket och -placeringar, justera budgeten baserat på testets storlek, ändra målgrupperna till att använda [!DNL RampID]-baserade segment (för autentiserade användare) eller ID5-baserade segment (för oautentiserade användare) och verifiera att de nya paketen och placeringarna spenderar sin fulla budget.

   * Om du vill jämföra prestanda för universella ID-baserade segment med prestanda för placeringar som riktar sig till andra målgruppsidentifierare, som cookies eller mobilannonser, skapar du en kampanj med en separat universell ID-baserad placering och en äldre ID-baserad placering.

     Om du vill ha ett fullständigt återmarknadsföringstest anger du både ramp-ID:n för autentiserade användare och ID5s för oautentiserade användare som mål.

     Att få bästa prestanda bör inte vara den primära jämförelsen. Bestäm i stället vilka ID:n som ska skalas bra, vilket kan informera optimeringen och budgetallokeringarna senare. Det långsiktiga målet är att kompensera för förlorade intryck och webbplatstrafik när cookies används.

   * Om du vill jämföra den totala webbläsarräckvidden ska du inrikta dig på universella ID-baserade segment och äldre ID-baserade segment på samma plats. Använd samma kampanjinställningar som i det föregående användningsexemplet, förutom att du inte behöver dela upp kampanjbudgeten.

     Inställningen för budgivning ges till universella ID:n, men äldre ID:n får bud när universella ID:n inte är tillgängliga. Se till att jämföra räckvidd i olika webbläsare (inklusive Chrome, Safari och Mozilla).

     >[!NOTE]
     >
     >Frekvensbegränsningen gäller för ett enskilt ID. När en användare har flera ID-typer kan du nå användaren mer än du förväntar dig.

* Tänk på att räckvidden för autentiserade målgruppssegment är naturligt mindre än räckvidden för cookie-baserade segment, och att ytterligare målgruppsalternativ minskar er räckvidd ytterligare. Var klok på att använda detaljerad målinriktning, särskilt genom att koppla ihop flera mål med AND-satser.

## Datavariationer mellan e-post-ID och universella ID {#universal-ids-data-variances}

### Godtagbara variationsnivåer

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID måste vara högre än 90 %. Översättningsfrekvensen för [!DNL RampIDs] ska i synnerhet vara 95 % om alla hash-kodade e-postadresser är unika. Om du t.ex. skickar 100 hash-kodade e-postadresser från din kunddataplattform bör de översättas till minst 95 [!DNL RampIDs] eller mer än 90 andra typer av universella ID:n. En lägre översättningsgrad kan tyda på ett problem. Se &quot;[Orsaker till avvikelse](#universal-ids-data-variances-reasons&quot;) för möjliga förklaringar.

För [!DNL RampIDs]kan du kontakta kontoteamet på Adobe för att få mer information om översättningsnivån är lägre än 70 %.

### Orsaker till avvikelse {#universal-ids-data-variances-causes}

* Hash-kodade e-post-ID:n som översatts till ID5-ID:n:

  Sannolikhetsmodellen har en felvarians på +/- 5 %. Det innebär att antalet målgrupper kan överskattas eller underskattas med 5 %.

* Hash-kodade e-post-ID:n översatta till [!DNL RampIDs]:

   * När flera profiler använder samma e-post-ID kan antalet DSP vara lägre än antalet profiler på er kunddataplattform. I Adobe Photoshop kan du till exempel skapa ett företagskonto och ett personligt konto med ett enda e-post-ID. Men om båda profilerna tillhör samma person mappas profilerna till ett e-post-ID och därefter till ett [!DNL RampID].

   * A [!DNL RampID] kan uppgraderas till ett nytt värde. If [!DNL LiveRamp] känner inte igen ett e-post-ID eller kan inte mappa det till ett befintligt [!DNL RampID] i sin databas tilldelar den en ny [!DNL RampID] till e-post-ID:t. När de kan mappa e-post-ID:t till ett annat [!DNL RampID] eller kan samla in mer information om samma e-post-ID, uppgradera [!DNL RampID] till ett nytt värde. [!DNL LiveRamp] avser denna åtgärd uppgradering från en&quot;härledd&quot; [!DNL RampID] till en&quot;bibehållen&quot; [!DNL RampID]. DSP får dock inte mappningar mellan härledda och bevarade [!DNL RampIDs] och kan därför inte ta bort den tidigare versionen av rampID från DSP. I det här fallet kan segmentantalet vara större än profidräkningen.

     Exempel: En användare loggar in på [!DNL Adobe] och besöker Photoshop webbplats. If [!DNL LiveRamp] saknar befintlig information om e-post-ID, så tilldelar de det till en härledd [!DNL RampID], säger D123. Femton dagar senare besöker användaren samma sida, men [!DNL LiveRamp] har uppgraderat [!DNL RampID] under dessa 15 dagar och har omfördelat [!DNL RampID] till M123. Även om kunddataplattformens segment&quot;Photoshop Enthusiast&quot; bara har ett e-post-ID för användaren har DSP-segmentet två ramp-ID: D123 och M123.

## Felsökning

Om du inte ser antalet användare, eller om målgruppens storlek är låg, ska du kontrollera följande:

* Om du [!DNL Flashtalking] eller [!DNL Google Campaign Manager 360] annonser, kontrollera sedan att dina annonsers klicknings-URL:er har rätt makron. Se makrona för [[!DNL Flashtalking] annonser](/help/integrations/analytics/macros-flashtalking.md) och [[!DNL Google Campaign Manager 360] annonser](/help/integrations/analytics/macros-google-campaign-manager.md).

* Se till att rätt, universell ID-partnerspecifik kod implementeras på din webbplats för att matcha händelser på plats och annonsexponeringar. Arbeta med dina [!DNL LiveRamp] eller [!DNL ID5] vid behov.

* (för [!DNL RampIDs] och [!DNL UID 2.0] ID) Se till att [DSP datakälla är korrekt konfigurerad](/help/dsp/audiences/sources/source-manage.md#source-settings)och att antalet användare fylls i för de genererade målgruppssegmenten.

* Om ni är mindre än förväntat bör ni kontrollera att målgruppssegmentets logik inte är för detaljerad.

* Kontrollera att inställningarna för kampanj, paket och placering är korrekta.<!-- wording-->

Om du inte kan lösa problemet kontaktar du ditt kontoteam på Adobe.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](/help/dsp/audiences/sources/source-manage.md)
>* [Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
