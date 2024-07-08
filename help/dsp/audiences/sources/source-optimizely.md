---
title: Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n
description: Lär dig hur du aktiverar DSP för att importera dina [!DNL Optimizely] förstapartssegment.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n

*Beta-funktion*

Använd DSP-integreringen [!DNL Optimizely] med kunddataplattformen för att konvertera organisationens hash-kodade e-postadresser från första part till universella ID:n för riktad annonsering.

1. (För att konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Ställ in spårning för att aktivera [!DNL Analytics] mätning](#analytics-tracking).

1. [Skapa en målgruppskälla i DSP](#source-create).

1. [Förbered och skicka segmentdata](#push-data).

1. [Jämför antalet universella ID:n med antalet hashade e-postadresser](#compare-id-count).

## Steg 1: Ställ in spårning för [!DNL Analytics] mätning {#analytics-tracking}

*Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Om du vill konvertera e-postadresser till [!DNL RampIDs] eller [!DNL ID5] ID:n måste du göra följande:

1. (Om du inte redan har gjort det) Slutför alla [krav för att implementera [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och se till att AMO-ID:t och EF-ID](/help/integrations/analytics/ids.md):t fylls [i i dina spårnings-URL:er.

1. Registrera dig hos den universella ID-partnern och implementera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare på datorer och mobila enheter (men inte i mobilappar) till visningar:

   * **För [!DNL RampIDs]:** Du måste implementera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från id:n i webbläsare på datorer och mobila enheter (men inte i mobilappar) med genomgångar. Kontakta kontoteamet på Adobe, som ger dig instruktioner om hur du registrerar dig för en [!DNL LiveRamp] [!DNL LaunchPad] tagg från [!DNL LiveRamp] Authentication Traffic Solutions. Registreringen är gratis, men du måste skriva under ett avtal. När du har registrerat dig kommer ditt kontoteam på Adobe att generera och tillhandahålla en unik tagg som din organisation kan implementera på dina webbsidor.

## Steg 2: Skapa en målgruppskälla i DSP {#source-create}

1. [Skapa en målgruppskälla](source-manage.md) för att importera målgrupper till ditt DSP-konto eller ett annonsörskonto. Du kan välja att konvertera dina användaridentifierare till något av de tillgängliga universella ID-formaten[](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel som du använder för att skicka segmentdata.

1. När du har skapat målgruppskällan delar du källkodsnyckeln med användaren [!DNL Optimizely] .

## Steg 3: Förbered och skicka segmentdata {#push-data}

Annonsören måste förbereda och skicka data med hjälp av sin [!DNL Optimizely] representant.

1. Inom [!DNL Optimizely Data Platform]hash e-post-ID:n för annonsörens målgrupp med hjälp av SHA-256-algoritmen.

1. Följ [[!DNL Optimizely's] instruktionerna för att skicka segmentet till DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inkludera följande information för att aktivera integreringen:

   * **Källnyckel:** Det här är källnyckeln som skapades i [steg 2](#source-create).

   * **Kontokod:** Detta är den alfanumeriska DSP-kontokoden, som du hittar i DSP på [!UICONTROL Settings] > [!UICONTROL Account].

Segmenten ska vara tillgängliga i DSP inom 24 timmar och uppdateras enligt konfigurationen för annonsören. Oavsett hur ofta segmentet uppdateras upphör inkluderingen i ett segment att gälla efter 30 dagar som standard eller efter en kundspecificerad förfalloperiod. Uppdatera dina segment genom att skicka om dem från [!DNL Optimizely] före förfallodatumet. Om du vill begära att ett anpassat segment upphör att gälla kontaktar du kontoteamet på Adobe.

## Steg 4: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

När du har slutfört alla steg verifierar du i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller i placeringsinställningarna) att segmentet är tillgängligt och fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hashade e-postadresser.

Översättningshastigheten för hash-kodade e-postadresser till universella ID:n bör vara större än 90 %. Om du till exempel skickar 100 hashade e-postadresser från din kunddataplattform bör de översättas till fler än 90 universella ID:n. En översättningshastighet på 90 % eller mindre är ett problem. Mer information om hur segmentantalet kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).&quot;

Om du behöver hjälp med felsökning kan du kontakta kontoteamet på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om källor för förstapartsmålgrupper](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID:n](/help/dsp/audiences/universal-ids.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)
