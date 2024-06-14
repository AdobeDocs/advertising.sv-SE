---
title: Konvertera användar-ID:n från [!DNL Optimizely] till universella ID
description: Lär dig hur du aktiverar DSP att importera [!DNL Optimizely] förstahandssegment.
feature: DSP Audiences
source-git-commit: f51f07c1e057eb09c2cad292b2c8062f7d993166
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Optimizely] till universella ID

*Betafunktion*

Använd DSP integrering med [!DNL Optimizely] plattform för kunddata för att konvertera organisationens egna hashade e-postadresser till universella ID:n för riktad reklam.

1. (Konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Aktivera spårning [!DNL Analytics] mått](#analytics-tracking).

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbereda och flytta segmentdata](#push-data).

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

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL Optimizely] användare.

## Steg 3: Förbered och push-överföra segmentdata {#push-data}

Annonsören måste ta fram och publicera data med hjälp av sina [!DNL Optimizely] -representant.

1. Inom [!DNL Optimizely Data Platform], hash the email IDs for the publish&#39;s publiser using the SHA-256 algorithm.

1. Kontakta annonsörens [!DNL Optimizely] -representant för instruktioner om hur du flyttar segmentet till DSP. Inkludera följande information när du flyttar segmentet:

   * **Källnyckel:** Detta är den källnyckel som skapas i [Steg 2](#source-create).

   * **Kontokod:** Det här är den alfanumeriska DSP kontokoden som du hittar DSP på [!UICONTROL Settings] > [!UICONTROL Account].

Segmenten ska vara tillgängliga i DSP inom 24 timmar och uppdateras enligt annonsörens konfiguration. Oberoende av hur ofta segmentet uppdateras, upphör inkludering i ett segment efter 30 dagar som standard eller efter en av kunden angiven förfalloperiod. Uppdatera era segment genom att trycka på dem igen [!DNL Optimizely] före utgångsdatumet. Kontakta ditt Adobe-kontoteam om du vill begära att ett anpassat segment ska upphöra att gälla.

<!--
Are they using the Data Platform web services, another type of API, or a UI? Add a link to instructions, including how to designate DSP as the destination. And where will they input the DSP-specific fields?]
-->

## Steg 4: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

När du är klar med alla steg kan du verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet är tillgängligt och fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hash-adresser.

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Om du till exempel skickar 100 hashas-e-postadresser från din kunddataplattform bör de översättas till mer än 90 universella ID:n. En översättningsgrad på 90 % eller mindre är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
