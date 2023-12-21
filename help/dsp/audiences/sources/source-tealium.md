---
title: "Arbetsflöde för att använda DSP integrering med [!DNL Tealium]"
description: "Lär dig hur DSP kan importera [!DNL Tealium] förstapartssegment."
feature: DSP Audiences
source-git-commit: e7c967d66be9c8ca78a64d644c7e3a691f1e216a
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Arbetsflöde för att använda DSP integrering med [!DNL Tealium]

Du kan dela organisationens egna data från [!DNL Tealium] plattform för kunddata med [!DNL Amazon Web Services] (AWS) firehose-anslutning. Det finns fyra steg för att dela data från Tealium med DSP:

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbered och dela segmentmappningsdata](#map-data).

1. [Skapa kopplingar i [!DNL Tealium] dela segmentdata](#tealium-connector).

1. [Duplicera den befintliga kopplingen i [!DNL Tealium] för att fortsätta dela segment](#duplicate-connector).

## Steg 1: Skapa en publikkälla i DSP {#source-create}

* [Skapa en publikkälla](source-create.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto och dela källkodnyckeln med [!DNL Tealium] användare.

## Steg 2: Förbered och dela segmentmappningsdata {#map-data}

1. Annonsören måste förbereda och dela segmentmappningsdata:

   1. Annonsören måste förbereda uppgifterna i [!DNL Tealium]:

      1. E-post-ID:n för annonsörens målgrupp måste hashas med algoritmen SHA-256.

      1. Kolumnen som innehåller hash-kodade e-post-ID:n måste mappas till attributet för typen av besökar-ID.

      1. Publiken måste skapas med `Tealium_visitor_id` -attribut. Rätt berikning måste tillämpas för att få publiken att lyfta. Se [[!DNL Tealium] dokumentation om attribut för besökar-ID](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. Annonsören måste ge segmentmappningsdata till kontoteamet på Adobe för att skapa segmenten i DSP. Använd följande kolumnnamn och värden i en kommaavgränsad värdefil:

      * **Extern segmentnyckel:** Den externa segmentnyckeln som du senare anger i åtgärdsinställningarna för kopplingen i [!DNL Tealium]. Den rekommenderade namnkonventionen är &quot;`<DSP source key>_<Tealium segment name>`, till exempel &quot;57bf424dc10_kaffedryckers.&quot;

      * **Segmentnamn:** Segmentnamnet.

      * **Segmentbeskrivning:** Segmentets syfte eller regel, eller både och.

      * **Överordnat ID:** Behåll tomt

      * **Video CPM:** 0

      * **CPM för bildskärm:** 0

      * **Segmentfönster:** Segmentets time-to-live.

## Steg 3: Skapa anslutningar i [!DNL Tealium] dela segmentdata {#tealium-connector}

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

            1. I alternativet att skapa ett anpassat fält, i [!DNL Source Key] fält, ange [!UICONTROL External Segment Key] som ingick i segmentmappningsdata i [Steg 2](#map-data).

               DSP använder den här nyckeln för att fylla i ditt segment.

            1. (Rekommenderas) Skapa en uppdateringsåtgärd för att hålla segmentet aktuellt.

## Steg 4: Duplicera den befintliga kopplingen i [!DNL Tealium] för att fortsätta dela segment {#duplicate-connector}

Du kan bara ha en koppling per segment och ett segment per koppling.

1. I [!DNL Tealium], duplicera det segment som du vill skapa ett annat segment för och byt namn på det nya segmentet.

1. I [!DNL Tealium], duplicera den koppling du skapade i [Steg 3](#tealium-connector)och byta namn på den nya kopplingen från`<original name>-copy`till det nya segmentnamnet.

>[!MORELIKETHIS]
>
>* [Aktivera autentiserade segment från målgruppskällor](/help/dsp/audiences/sources/source-about.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målkälla](source-settings.md)
>* [Arbetsflöde för att använda DSP integrering med [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
