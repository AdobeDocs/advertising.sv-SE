---
title: Konvertera användar-ID:n från [!DNL Amperity] till universella ID
description: Lär dig hur du aktiverar DSP att importera [!DNL Amperity] förstahandssegment.
feature: DSP Audiences
source-git-commit: 25bcc2eefa4dc7873ab8189122d43da336e3e046
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Amperity] till universella ID

*Betafunktion*

Använd DSP integrering med [!DNL Amperity] plattform för kunddata för att konvertera organisationens egna hashade e-postadresser till universella ID:n för riktad reklam.

1. (Konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Aktivera spårning [!DNL Analytics] mått](#analytics-tracking).

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbered och dela segmentmappningsdata](#map-data).

1. [Begär en datapush från [!DNL Amperity] till DSP](#push-data).

1. [Jämför antalet universella ID:n med antalet hashade e-postadresser](#compare-id-count).

## Steg 1: Ställ in spårning för [!DNL Analytics] mått {#analytics-tracking}

*Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Konvertera e-postadresser till [!DNL RampIDs] eller [!DNL ID5] ID måste du göra följande:

1. (Om du inte redan har gjort det) Slutför alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och se till att [AMO ID och EF ID](/help/integrations/analytics/ids.md) fylls i i dina spårnings-URL:er.

1. Registrera dig hos den universella ID-partnern och distribuera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att visa genomgångar:

   * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att kunna visa igenom dem. Kontakta kontoteamet på Adobe som ger dig anvisningar om hur du registrerar dig för en [!DNL LiveRamp] [!DNL LaunchPad] tagga från [!DNL LiveRamp] Lösningar för autentiseringstrafik. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

## Steg 2: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto. Du kan välja att konvertera dina användaridentifierare till någon av [tillgängliga universella ID-format](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel som du använder för att överföra segmentdata.

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL Amperity] användare.

## Steg 3: Förbered och dela segmentmappningsdata {#map-data}

Annonsören måste ta fram och dela segmentmappningsdata.

1. Inom [!DNL Amperity], hash the email IDs for the målgrupp using the SHA-256 algorithm.

1. Annonsören måste ge segmentmappningsdata till kontoteamet på Adobe för att skapa segmenten i DSP. Använd följande kolumnnamn och värden i en kommaavgränsad värdefil:

   * **Extern segmentnyckel:** The [!DNL Amperity] segmentnyckel som är associerad med segmentet.

   * **Segmentnamn:** Segmentnamnet.

   * **Segmentbeskrivning:** Segmentets syfte eller regel, eller både och.

   * **Överordnat ID:** Behåll tomt

   * **Video CPM:** 0

   * **CPM för bildskärm:** 0

   * **Segmentfönster:** Segmentets time-to-live.

## Steg 4: Begär en datapush från [!DNL Amperity] till DSP {#push-data}

1. När segmentet har mappats inom DSP måste annonsören arbeta med sina [!DNL Amperity] för att distribuera segmentdata till DSP.

1. Annonsören måste sedan bekräfta med Adobe Account Team att segmentuppgifterna har tagits emot.

Segmenten ska vara tillgängliga i DSP inom 24 timmar och uppdateras enligt annonsörens konfiguration inom [!DNL Amperity]. Oberoende av hur ofta segmentet uppdateras, upphör inkludering i ett segment efter 30 dagar som standard eller efter en av kunden angiven förfalloperiod. Uppdatera era segment genom att trycka på dem igen [!DNL Amperity] före utgångsdatumet. Kontakta ditt Adobe-kontoteam om du vill begära att ett anpassat segment ska upphöra att gälla.

## Steg 5: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

När du är klar med alla steg kan du verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet är tillgängligt och fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hash-adresser.

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Om du till exempel skickar 100 hashas-e-postadresser från din kunddataplattform bör de översättas till mer än 90 universella ID:n. En översättningsgrad på 90 % eller mindre är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
