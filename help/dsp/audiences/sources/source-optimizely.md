---
title: Konvertera användar-ID:n från [!DNL Optimizely] till universella ID
description: Lär dig hur du aktiverar DSP att importera [!DNL Optimizely] förstahandssegment.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Optimizely] till universella ID

*Funktionen Beta*

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

   * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att kunna se dem. Kontakta kontoteamet på Adobe som ger dig anvisningar om hur du registrerar dig för en [!DNL LiveRamp] [!DNL LaunchPad] tagga från [!DNL LiveRamp] Lösningar för autentiseringstrafik. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

## Steg 2: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto. Du kan välja att konvertera dina användaridentifierare till någon av [tillgängliga universella ID-format](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel som du använder för att överföra segmentdata.

1. När du har skapat målgruppskällan kan du dela källkodnyckeln med [!DNL Optimizely] användare.

## Steg 3: Förbered och push-överföra segmentdata {#push-data}

Annonsören måste förbereda och skicka data med [!DNL Optimizely Data Platform]. Kontakta [!DNL Optimizely] -representant.

1. Inom [!DNL Optimizely Data Platform], hash the email IDs for the målgrupp using the SHA-256 algorithm.

1. Följ [[!DNL Optimizely's] instruktioner för att skjuta upp segmentet till DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inkludera följande information för att aktivera integreringen:

   * **Source Key:** Detta är den källnyckel som skapas i [Steg 2](#source-create).

   * **Kontokod:** Det här är den alfanumeriska DSP kontokoden som du hittar DSP på [!UICONTROL Settings] > [!UICONTROL Account].

Segmenten kommer att uppdateras enligt annonsörens konfiguration. Oberoende av hur ofta segmentet uppdateras, upphör inkludering i ett segment efter 30 dagar som standard eller efter en av kunden angiven förfalloperiod. Uppdatera era segment genom att trycka på dem igen [!DNL Optimizely] före utgångsdatumet. Kontakta ditt Adobe-kontoteam om du vill begära att ett anpassat segment ska upphöra att gälla.

## Steg 4: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

Segmenten ska vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata ska antalet deltagare vara synligt inom nio (9) timmar.

Verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet är tillgängligt och fylls i, och jämför antalet universella ID med antalet ursprungliga hashade e-postadresser.

Information om godtagbara ID-översättningsfrekvenser och varför antalet segment kan variera finns i &quot;[Datavariationer mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstagångspubliker](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
