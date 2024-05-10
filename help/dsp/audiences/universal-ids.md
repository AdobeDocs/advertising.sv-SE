---
title: Stöd för aktivering av universella ID
description: Lär dig mer om stöd för import av era universella ID-segment, skapa anpassade segment för att spåra universella ID:n och konvertera andra användaridentifierare i era förstapartssegment till universella ID:n för cookiefri anpassning.
feature: DSP Audiences
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Stöd för aktivering av universella ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Betafunktion*

DSP har stöd för personbaserade, universella ID:n för cookiefri anpassning till olika digitala format som stöds av DSP.

* Du kan skicka din autentiserade [[!DNL LiveRamp] [!DNL RampIDs]] direkt till DSP med [!DNL LiveRamp] [!DNL Connect] kontrollpanel. Se &quot;[Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP kan importera era egna segment som består av hash-kodade e-post-ID:n som är byggda i kunddataplattformen (CDP) och konvertera dem till [!DNL LiveRamp] [!DNL RampIDs] och [!DNL Unified ID 2.0 (UID2.0)] ID. Mer information om vilka kunddataplattformar som stöds, vilka funktioner som är tillgängliga för alla universella ID-typer som stöds samt relaterade arbetsflöden finns i &quot;[Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md).&quot;

* Du kan skapa anpassade segment som spårar användare som är kopplade till universella ID:n för ID5 som exponeras för annonser från datorer och mobila enheter och som besöker specifika webbsidor. ID5 använder en sannolikhetsmodell för att tilldela ett ID som härleds från olika användarsignaler och webbläsarsignaler. Instruktioner finns i &quot;[Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md).&quot;

* Tredjepartssegment från [!DNL Eyeota] och vissa andra leverantörer kan automatiskt inkludera ID5-ID:n, förutom användare som spåras med cookies eller enhets-ID:n. Segmentinformationen innehåller storleken för varje typ. Den vanliga användaravgiften för varje segment, som anges bredvid segmentnamnet, gäller. Inga ytterligare avgifter tas ut för ID5-ID:n.

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## Rapportering efter typ av universellt ID

* **Anpassade rapporter:** Kostnads-, intrycks-, klicknings-, konverterings- och frekvensdata per universell ID-typ är tillgängliga i anpassade rapporter.

* **[!DNL Analytics]rapporter:** Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) som har implementerat alla nödvändiga steg kan se genomskinlighetskonverteringar med universaltyp i [!DNL Analytics].

* **Segmentinformation:** För alla segmenttyper omfattar segmentinformationen målgruppens storlek efter typ av universellt ID och efter den enhetstyp som spåras av cookies eller enhets-ID.

## Använda ett universellt ID som målgrupp i dina praktikanter

>[!NOTE]
>
>Du kan inte ändra måltypen för ID i en direktplacering. Om det behövs kan du duplicera en aktiv placering och ändra typerna av mål-ID på den nya placeringen.

Gör följande i en ny, schemalagd eller pausad placering:

* I [!UICONTROL Geo-Targeting] Ange de geografiska områden som ska vara mål. Varje partner för universella ID tillåter endast målgruppsanpassning i specifika geografiska områden, och endast giltiga ID-typer är tillgängliga i [!UICONTROL Targeting] inställningar.

* I [!UICONTROL Audience Targeting] gör du följande:

   * I [!UICONTROL Included Audiences] väljer du det segment för vilket användardata konverterades till universella ID.

     Du kan inkludera ytterligare segment om du vill.

   * I [!UICONTROL Targeting] anger du vilken universell ID-typ som ska användas som mål.

     Inställningen innehåller alternativen &quot;[!UICONTROL Legacy IDs]och &quot;[!UICONTROL Universal ID],&quot; som kan innehålla underalternativen &quot;[!UICONTROL ID5],&quot;[!UICONTROL RampID],&quot; och &quot;[!UICONTROL Unified ID2.0].&quot; De faktiska delalternativen bestäms av de valda geografiska målen.

     Du kan välja båda[!UICONTROL Legacy IDs]och &quot;[!UICONTROL Universal ID],&quot; men du kan bara välja en typ av universellt ID per placering. När du väljer både äldre ID:n och universella ID:n ges budgivningsinställningar till universella ID:n.

Se &quot;[Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Bästa metoder för testning och dataverifiering

Använd följande metodtips för [!DNL RampID]-baserade segment och ID5-baserade segment, för vilka Adobe Analytics-mätningar är tillgängliga.

* Ungefär 24 timmar efter att du har aktiverat ett segment ska du kontrollera antalet konverterade ID:n för segmentet inom [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Kontakta ditt kontoteam på Adobe om ID-antalet är oväntat.

  Se &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances)&quot; för mer information om hur antalet segment kan variera.

* Ändra inte befintliga paket och placeringar. Om du inte har en stegvis budget för att testa universella ID:n ska du minska den ursprungliga budgeten för att finansiera testerna.

* Kopiera dina originalpaket och -placeringar, justera budgeten baserat på testets storlek, ändra målgrupperna till att använda [!DNL RampID]-baserade segment (för autentiserade användare) eller ID5-baserade segment (för oautentiserade användare) och verifiera att de nya paketen och placeringarna spenderar sin fulla budget.

   * Om du vill jämföra prestanda för universella ID-baserade segment med prestanda för placeringar som riktar sig till andra målgruppsidentifierare, som cookies eller mobilannonser, skapar du en kampanj med en separat universell ID-baserad placering och en äldre ID-baserad placering.

     Att få bästa prestanda bör inte vara den primära jämförelsen. Bestäm i stället vilka ID:n som ska skalas bra, vilket kan informera optimeringen och budgetallokeringarna senare. Det långsiktiga målet är att kompensera för förlorade intryck och webbplatstrafik när cookies används.

   * Om du vill jämföra den totala webbläsarräckvidden ska du inrikta dig på universella ID-baserade segment och äldre ID-baserade segment på samma plats. Använd samma kampanjinställningar som i det föregående användningsexemplet, förutom att du inte behöver dela upp kampanjbudgeten.

     Inställningen för budgivning ges till universella ID:n, men äldre ID:n får bud när universella ID:n inte är tillgängliga. Se till att jämföra räckvidd i olika webbläsare (inklusive Chrome, Safari och Mozilla).

     >[!NOTE]
     >
     >Frekvensbegränsningen gäller för ett enskilt ID. När en användare har flera ID-typer kanske du når den användaren mer än du hade förväntat dig.

* Tänk på att räckvidden för autentiserade målgruppssegment är naturligt mindre än räckvidden för cookie-baserade segment, och att ytterligare målgruppsalternativ minskar er räckvidd ytterligare. Var klok på att använda detaljerad målinriktning, särskilt genom att koppla ihop flera mål med AND-satser.

## Orsaker till dataavvikelser mellan e-post-ID och universella ID {#universal-ids-data-variances}

Det finns två orsaker till avvikelser för hashad e-post-ID:n som har översatts till [!DNL RampIDs]:

* När flera profiler använder samma e-post-ID kan antalet DSP vara lägre än antalet profiler på er kunddataplattform. I Adobe Photoshop kan du till exempel skapa ett företagskonto och ett personligt konto med ett enda e-post-ID. Men om båda profilerna tillhör samma segment mappas profilerna till ett e-post-ID och därefter till ett [!DNL RampID].

* A [!DNL RampID] kan uppgraderas till ett nytt värde. If [!DNL LiveRamp] känner inte igen ett e-post-ID eller kan inte mappa det till ett befintligt [!DNL RampID] i sin databas tilldelar den en ny [!DNL RampID] till e-post-ID:t. När de kan mappa e-post-ID:t till ett annat [!DNL RampID] eller kan samla in mer information om samma e-post-ID, uppgradera [!DNL RampID] till ett nytt värde. [!DNL LiveRamp] avser denna åtgärd uppgradering från en&quot;härledd&quot; [!DNL RampID] till en&quot;bibehållen&quot; [!DNL RampID]. DSP får dock inte mappningar mellan härledda och bevarade [!DNL RampIDs] och kan därför inte ta bort den tidigare versionen av rampID från DSP. I det här fallet kan segmentantalet vara större än profidräkningen.

  Exempel: En användare loggar in på [!DNL Adobe] och besöker Photoshop sida. If [!DNL LiveRamp] saknar befintlig information om e-post-ID, så tilldelar de det till en härledd [!DNL RampID], säger D123. Femton dagar senare besöker användaren samma sida, men [!DNL LiveRamp] har uppgraderat [!DNL RampID] under dessa 15 dagar och har omfördelat [!DNL RampID] till M123. Även om kunddataplattformens segment&quot;Photoshop Enthusiast&quot; bara har ett e-post-ID för användaren har DSP-segmentet två ramp-ID: D123 och M123.

>[!MORELIKETHIS]
>
>* [Skapa en målgruppskälla för att aktivera universella ID-målgrupper](/help/dsp/audiences/sources/source-create.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID](/help/dsp/audiences/sources/source-tealium.md)
>* [Skapa och implementera ett anpassat segment](/help/dsp/audiences/custom-segment-create.md)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
