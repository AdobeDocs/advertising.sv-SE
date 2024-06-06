---
title: Konvertera användar-ID:n från [!DNL Optimizely] till universella ID
description: Lär dig hur du aktiverar DSP att importera [!DNL Optimizely] förstahandssegment.
feature: DSP Audiences
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Optimizely] till universella ID

Använd DSP integrering med [!DNL Optimizely] plattform för kunddata för att konvertera organisationens egna hashade e-postadresser till universella ID:n för riktad reklam.

1. (Konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Aktivera spårning [!DNL Analytics] mått](#analytics-tracking).

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbered och flytta segmentdata i [!DNL Optimizely Data Platform]](#push-data).

1. [Jämför antalet universella ID:n med antalet hashade e-postadresser](#compare-id-count).

Segmenten bör vara tillgängliga i DSP inom 24 timmar och uppdateras var 24:e timme. **[Sant, eller annorlunda förväntningar för Optimizely?]**

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

Annonsören måste förbereda och föra över data inom [!DNL Optimizely Data Platform].  **[Använder de den optimala dataplattformen?]**  <!-- Data Platform? -->

1. Hash-koda e-post-ID:n för annonsörens målgrupp med hjälp av SHA-256-algoritmen.

1. Flytta segmentet till DSP, inklusive följande fält:

   **[Använder de Data Platform-webbtjänsterna, en annan typ av API eller ett gränssnitt? Lägg till en länk till instruktionerna. Och var kommer de att mata in dessa fält?]**  <!-- Are they using the Data Platform web services or what? Add a link to instructions. And where will they input these fields?  -->

   * **Källnyckel:** Detta är den källnyckel som skapas i [Steg 2](#source-create).

   * **Kontokod:** Det här är den alfanumeriska DSP kontokoden som du hittar DSP på [!UICONTROL Settings] > [!UICONTROL Account].

## Steg 4: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

När du är klar med alla steg kan du verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet är tillgängligt och fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hash-adresser.

Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Om du till exempel skickar 100 hashas-e-postadresser från din kunddataplattform bör de översättas till mer än 90 universella ID:n. En översättningsgrad på 90 % eller mindre är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

Segmenten uppdateras var 24:e timme. Inkluderingen i ett segment upphör dock efter 30 dagar för att säkerställa sekretessefterlevnad, så uppdatera målgrupperna genom att trycka på dem igen [!DNL Optimizely] var 30:e dag eller mindre.

Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID](/help/dsp/audiences/sources/source-tealium.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
