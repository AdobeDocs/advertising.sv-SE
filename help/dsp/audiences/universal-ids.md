---
title: Stöd för aktivering av universella ID
description: Lär dig mer om stöd för import av era universella ID-segment, skapa anpassade segment för att spåra universella ID:n och konvertera andra användaridentifierare i era förstapartssegment till universella ID:n för cookiefri anpassning.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Stöd för aktivering av universella ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta-funktion*

DSP har stöd för personbaserade, universella ID:n för cookiefri anpassning till olika digitala format som stöds av DSP.

* Du kan skicka din autentiserade [[!DNL LiveRamp] [!DNL RampIDs]] manuellt direkt till DSP med kontrollpanelen [!DNL LiveRamp] [!DNL Connect]. Se [Importera autentiserade segment manuellt från  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kan importera dina egna segment som består av hashas-e-post-ID:n som är byggda i kunddataplattformen (CDP) och konvertera dem till [!DNL LiveRamp] [!DNL RampIDs] - och [!DNL Unified ID 2.0 (UID2.0)]-ID:n. Mer information om vilka kunddataplattformar som stöds, vilka funktioner som är tillgängliga för alla universella ID-typer som stöds samt relaterade arbetsflöden finns i [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md).

* Du kan skapa anpassade segment som spårar användare som är kopplade till universella ID:n för ID5 som exponeras för annonser från datorer och mobila enheter och som besöker specifika webbsidor. ID5 använder en sannolikhetsmodell för att tilldela ett ID som härleds från olika användarsignaler och webbläsarsignaler. Instruktioner finns i &quot;[Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md)&quot;.

* Tredjepartssegment från vissa leverantörer kan automatiskt inkludera universella ID:n utöver användare som spåras med cookies eller enhets-ID:n. Segment från [!DNL Eyeota] kan till exempel automatiskt inkludera ID5-ID:n, och segment från [!DNL Lotame] kan innehålla UID2.0-ID:n. Segmentinformationen innehåller storleken för varje typ. Den vanliga användaravgiften för varje segment, som anges bredvid segmentnamnet, gäller. Inga ytterligare avgifter tas ut för ID5-ID:n.

## Rapportering efter typ av universellt ID

* **Anpassade rapporter:** Kostnads-, intrycks-, klicknings-, konverterings- och frekvensdata per universell ID-typ finns i anpassade rapporter.

* **[!DNL Analytics]rapporter:** Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) som har implementerat alla nödvändiga steg kan se genomskinliga konverteringar efter universaltyp i [!DNL Analytics].

  >[!IMPORTANT]
  >
  >För korrekt konverteringsattribuering bör du se till att klicknings-URL:erna för annonserna innehåller både [EF-ID och AMO-ID](/help/integrations/analytics/ids.md).

* **Segmentinformation:** För alla segmenttyper omfattar segmentinformationen målgruppsstorleken efter universaltyp och efter den enhetstyp som spåras av cookies eller enhets-ID.

## Använda ett universellt ID som målgrupp i dina praktikanter

>[!NOTE]
>
>Du kan inte ändra måltypen för ID i en direktplacering. Om det behövs kan du duplicera en aktiv placering och ändra typerna av mål-ID på den nya placeringen.

Gör följande i en ny, schemalagd eller pausad placering:

1. I avsnittet [!UICONTROL Geo-Targeting] anger du de geografiska områden som du vill ha som mål. Varje universell ID-partner tillåter endast användaranpassning i specifika geografiska områden, och endast giltiga ID-typer är tillgängliga i inställningarna för [!UICONTROL Targeting].

1. Gör följande i avsnittet [!UICONTROL Audience Targeting]:

   1. I inställningen [!UICONTROL Included Audiences] väljer du det segment för vilket användardata konverterades till universella ID:n.

      Du kan inkludera ytterligare segment om du vill.

   1. I inställningarna för [!UICONTROL Targeting]:

      1. Välj den universella ID-typ som du vill använda som mål.

         Inställningen innehåller alternativen [!UICONTROL Legacy IDs] och [!UICONTROL Universal ID], som kan innehålla underalternativen [!UICONTROL ID5], [!UICONTROL RampID] och [!UICONTROL Unified ID2.0]. De valda geografiska målen avgör vilka delalternativ som är tillgängliga.

         Du kan välja både [!UICONTROL Legacy IDs] och [!UICONTROL Universal ID], men du kan bara välja en typ av universellt ID per placering. När du väljer både äldre ID:n och universella ID:n ges budgivningsinställningar till universella ID:n.

      1. (Om det behövs) Acceptera villkoren i serviceavtalet för användning av universella ID:n.

         Innan du kan konvertera data till en ny ID-typ måste en användare på DSP acceptera villkoren i serviceavtalet. Villkoren får bara godkännas en gång per ID-typ, per konto.

Se [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md).

## Bästa metoder för testning och dataverifiering

Använd följande metodtips för [!DNL RampID]-baserade segment och ID5-baserade segment för vilka Adobe Analytics-mått är tillgängliga.

* Ungefär 24 timmar efter att du har aktiverat ett segment kontrollerar du antalet konverterade ID:n för segmentet inom [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Kontakta ditt kontoteam på Adobe om ID-antalet är oväntat.

  Mer information om hur antalet segment kan variera finns i [Datavarianser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).

* Ändra inte befintliga paket och placeringar. Om du inte har någon ytterligare budget för att testa universella ID:n ska du minska den ursprungliga budgeten för att finansiera testerna.

* Kopiera dina ursprungliga paket och placeringar, justera budgeten baserat på testets storlek, ändra målgrupperna så att de använder [!DNL RampID]-baserade segment (för autentiserade användare) eller ID5-baserade segment (för oautentiserade användare) och verifiera att de nya paketen och placeringarna spenderar hela budgeten.

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

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Översättningsfrekvensen för [!DNL RampIDs] bör vara 95 % om alla hash-kodade e-postadresser är unika. Om du till exempel skickar 100 hashade e-postadresser från din kunddataplattform bör de översättas till minst 95 [!DNL RampIDs] eller fler än 90 andra typer av universella ID. En lägre översättningsgrad kan tyda på ett problem. Se [Orsaker till avvikelse](#universal-ids-data-variances-reason) för möjliga förklaringar.

För [!DNL RampIDs] kan du kontakta ditt Adobe-kontoteam om du vill veta mer om översättningsnivån är lägre än 70 %.

### Orsaker till avvikelse {#universal-ids-data-variances-causes}

* Alla segment:

  Antalet segment-till-enhet använder en sannolikhetsmodell som har en felvarians på +/- 5 %. Det innebär att antalet målgrupper kan överskattas eller underskattas med 5 %.

* Hash-kodade e-post-ID:n som översatts till [!DNL RampIDs]:

   * När flera profiler använder samma e-post-ID kan antalet DSP vara lägre än antalet profiler på er kunddataplattform. I Adobe Photoshop kan du till exempel skapa ett företagskonto och ett personligt konto med ett enda e-post-ID. Men om båda profilerna tillhör samma person mappas profilerna till ett e-post-ID och därefter till ett [!DNL RampID].

   * En [!DNL RampID] kan uppgraderas till ett nytt värde. Om [!DNL LiveRamp] inte känner igen ett e-post-ID eller inte kan mappa det till en befintlig [!DNL RampID] i sin databas tilldelas ett nytt [!DNL RampID] till e-post-ID:t. När de i framtiden kan mappa e-post-ID till en annan [!DNL RampID] eller samla in mer information om samma e-post-ID uppgraderar de [!DNL RampID] till ett nytt värde. [!DNL LiveRamp] hänvisar till den här åtgärden som uppgradering från en härledd [!DNL RampID] till en underhållen [!DNL RampID]. DSP hämtar dock inte mappningar mellan härledda och underhållna [!DNL RampIDs] och kan därför inte ta bort den tidigare versionen av rampID från det DSP segmentet. I det här fallet kan segmentantalet vara större än profidräkningen.

     Exempel: En användare loggar in på webbplatsen [!DNL Adobe] och besöker Photoshop-sidan. Om [!DNL LiveRamp] inte har någon befintlig information om e-post-ID:t tilldelar de det en härledd [!DNL RampID], till exempel D123. Femton dagar senare besöker användaren samma sida, men [!DNL LiveRamp] har uppgraderat [!DNL RampID] under dessa 15 dagar och har tilldelat om [!DNL RampID] till M123. Även om kunddataplattformens segment&quot;Photoshop Enthusiast&quot; bara har ett e-post-ID för användaren har DSP-segmentet två ramp-ID: D123 och M123.

## Felsökning

Om du inte ser antalet användare, eller om målgruppens storlek är låg, ska du kontrollera följande:

* Om du använder [!DNL Flashtalking] eller [!DNL Google Campaign Manager 360] annonser måste du se till att dina annonsers klicknings-URL:er har lagts till med rätt makron. Se makrona för [[!DNL Flashtalking] annonser](/help/integrations/analytics/macros-flashtalking.md) och [[!DNL Google Campaign Manager 360] annonser](/help/integrations/analytics/macros-google-campaign-manager.md).

* Se till att rätt, universell ID-partnerspecifik kod implementeras på din webbplats för att matcha händelser på plats och annonsexponeringar. Arbeta med din [!DNL LiveRamp] eller [!DNL ID5]-representant efter behov.

* (För [!DNL RampIDs] och [!DNL UID 2.0] ID:n) Kontrollera att datakällan [DSP är korrekt konfigurerad](/help/dsp/audiences/sources/source-manage.md#source-settings) och att användarantalet fylls i för de genererade målgruppssegmenten.

* Om ni är mindre än förväntat bör ni kontrollera att målgruppssegmentets logik inte är för detaljerad.

* Kontrollera att inställningarna för kampanj, paket och placering är korrekta.<!-- wording-->

Om du inte kan lösa problemet kontaktar du ditt kontoteam på Adobe.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](/help/dsp/audiences/sources/source-manage.md)
>* [Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
