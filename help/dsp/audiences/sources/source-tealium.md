---
title: Konvertera användar-ID:n från [!DNL Tealium] till universella ID
description: Lär dig hur du aktiverar DSP att importera [!DNL Tealium] förstahandssegment.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 44c2fcad42be2d25524a49cdc9cb4184297cd3a1
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Tealium] till universella ID

*Funktionen Beta*

Använd DSP integrering med [!DNL Tealium] plattform för kunddata för att konvertera organisationens egna hashade e-postadresser till universella ID:n för riktad reklam. Processen använder [!DNL Amazon Web Services] (AWS) firehose-anslutning. Så här delar du data från Tealium med DSP:

1. (Konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Aktivera spårning [!DNL Analytics] mått](#analytics-tracking).

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbered och dela segmentmappningsdata](#map-data).

1. [Skapa kopplingar i [!DNL Tealium] dela segmentdata](#tealium-connector).

1. [Duplicera den befintliga kopplingen i [!DNL Tealium] för att fortsätta dela segment](#duplicate-connector).

1. [Jämför antalet universella ID:n med antalet hashade e-postadresser](#compare-id-count).

## Steg 1: Ställ in spårning för [!DNL Analytics] mått {#analytics-tracking}

*Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Konvertera e-postadresser till [!DNL RampIDs] eller [!DNL ID5] ID måste du göra följande:

1. (Om du inte redan har gjort det) Slutför alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och se till att [AMO ID och EF ID](/help/integrations/analytics/ids.md) fylls i i dina spårnings-URL:er.

1. Registrera dig hos den universella ID-partnern och distribuera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att visa genomgångar:

   * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att kunna se dem. Kontakta kontoteamet på Adobe som ger dig anvisningar om hur du registrerar dig för en [!DNL LiveRamp] [!DNL LaunchPad] tagga från [!DNL LiveRamp] Lösningar för autentiseringstrafik. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

## Steg 2: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto. Du kan välja att konvertera dina användaridentifierare till någon av [tillgängliga universella ID-format](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel som du använder för att förbereda segmentmappningsdata.

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL Tealium] användare.

## Steg 3: Förbered och dela segmentmappningsdata {#map-data}

Annonsören måste ta fram och dela segmentmappningsdata.

1. Annonsören måste förbereda uppgifterna i [!DNL Tealium]:

   1. Hash-koda e-post-ID:n för annonsörens målgrupp med hjälp av SHA-256-algoritmen.

   1. Mappa kolumnen som innehåller hash-kodade e-post-ID:n till attributet för typen av besökar-ID.

   1. Skapa målgrupper med `Tealium_visitor_id` -attribut. Använd rätt berikning för att få publiken att häpna. Se [[!DNL Tealium] dokumentation om attribut för besökar-ID](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. Annonsören måste ge segmentmappningsdata till kontoteamet på Adobe för att skapa segmenten i DSP. Använd följande kolumnnamn och värden i en kommaavgränsad värdefil:

   * **Extern segmentnyckel:** Den externa segmentnyckeln som du senare anger i åtgärdsinställningarna för kopplingen i [!DNL Tealium]. Den rekommenderade namnkonventionen är &quot;`<DSP source key>_<Tealium segment name>`, till exempel &quot;57bf424dc10_kaffedryckers.&quot; Använd DSP [!UICONTROL Source Key] från DSP inställningar för målgruppskälla.

   * **Segmentnamn:** Segmentnamnet.

   * **Segmentbeskrivning:** Segmentets syfte eller regel, eller både och.

   * **Överordnat ID:** Behåll tomt

   * **Video CPM:** 0

   * **CPM för bildskärm:** 0

   * **Segmentfönster:** Segmentets time-to-live.

## Steg 4: Skapa anslutningar i [!DNL Tealium] dela segmentdata {#tealium-connector}

För varje segment som du vill dela skapar du en separat koppling för varje åtgärd som utlöser dataändringar. Om du till exempel vill dela två segment som var och en har två utlösare, skapar du fyra kopplingar.

1. Adobe Account Team förser annonsören med AWS-autentiseringsuppgifter för brandslänksanslutning.

1. I [!DNL Tealium], [lägg till en koppling](https://docs.tealium.com/server-side/connectors/add/), med följande alternativ:

   1. Välj [!DNL AWS Firehose] koppling.

   1. I källinställningarna:

      1. Välj det målgruppssegment som ska delas.

      1. Konfigurera en utlösare:

         * För segmentets första koppling väljer du utlösaren `Joined Audience`. Detta garanterar att data delas med DSP när en användare går med i ett segment.

         * För segmentets andra koppling väljer du utlösaren `Left Audience`. Den här kopplingen används för att hantera alla avanmälningar och användare som lämnar segmentet i DSP.

   1. Ange AWS-brandslingkopplingen i konfigurationsinställningarna. Om du ännu inte har lagt till brandslingkopplingen för DSP lägger du till en brandslingkoppling med följande information:

      * **Namn:** Namnet på kopplingen.

      * **Åtkomstnyckel:** Åtkomstnyckeln som tillhandahålls av kontoteamet på Adobe.

      * **Hemlig nyckel:** Den hemliga nyckeln som tillhandahålls av kontogruppen i Adobe.

      * **Region:** US East North Virginia (us-east-1)

   1. Gör följande i åtgärdsinställningarna:

      1. Skapa en&quot;Skicka kunddata till leveransström (avancerat)&quot;-åtgärd för att lägga till data i segmentet med hjälp av följande information:

         * **Åtgärdsnamn:** Namnet på åtgärden.

         * **Åtgärdstyp:** Skicka kunddata till leveransström (avancerat)

         * **Leveransström:** Tealium_CDP_Connector

         * **Meddelandedata:**  Gör följande:

            1. Välj ett attribut för segmentet:

               * Ge det anpassade meddelandet för attributet Hashed_Email `hashed_email`.

               * Namnge det anpassade meddelandet för Cookies-attributet `cookies`.

            1. I alternativet att skapa ett anpassat fält, i [!DNL Source Key] fält, ange [!UICONTROL External Segment Key] som ingick i [segmentmappningsdata](#map-data) i föregående procedur.

               DSP använder den här nyckeln för att fylla i ditt segment.

            1. (Rekommenderas) Skapa en uppdateringsåtgärd för att hålla segmentet aktuellt.

## Steg 5: Duplicera den befintliga kopplingen i [!DNL Tealium] för att fortsätta dela segment {#duplicate-connector}

Du kan bara ha en koppling per segment och ett segment per koppling.

1. I [!DNL Tealium], duplicera det segment som du vill skapa ett annat segment för och byt namn på det nya segmentet.

1. I [!DNL Tealium], duplicera [den koppling du skapade](#tealium-connector) i föregående procedur och ändra namnet på den nya kopplingen från`<original name>-copy`till det nya segmentnamnet.

## Steg 6: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

Segmenten ska vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata ska antalet deltagare vara synligt inom nio (9) timmar.

Verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) som segmentet fyller i och jämför antalet universella ID med antalet ursprungliga hashade e-postadresser.

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID måste vara högre än 90 %. Översättningsfrekvensen för [!DNL RampIDs] ska i synnerhet vara 95 % om alla hash-kodade e-postadresser är unika. Om du t.ex. skickar 100 hash-kodade e-postadresser från din kunddataplattform bör de översättas till minst 95 [!DNL RampIDs] eller mer än 90 andra typer av universella ID:n. En lägre översättningsgrad är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

Segmenten uppdateras var 24:e timme. Inkluderingen i ett segment upphör dock efter 30 dagar som standard eller efter en av kunden specificerad förfalloperiod. Uppdatera era segment genom att trycka på dem igen [!DNL Tealium] före utgångsdatumet. Kontakta ditt Adobe-kontoteam om du vill begära att ett anpassat segment ska upphöra att gälla.

Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
