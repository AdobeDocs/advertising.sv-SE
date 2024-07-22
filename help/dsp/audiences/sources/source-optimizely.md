---
title: Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n
description: Lär dig hur du aktiverar DSP att importera dina [!DNL Optimizely] förstapartssegment.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Konvertera användar-ID från [!DNL Optimizely] till universella ID

*Beta-funktion*

Använd den DSP integreringen med [!DNL Optimizely]-kunddataplattformen för att konvertera din organisations e-postadresser från första part till universella ID:n för riktad annonsering.

1. (Att konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Ställ in spårning för att aktivera [!DNL Analytics] mätning](#analytics-tracking).

1. [Skapa en publikkälla i DSP](#source-create).

1. [Förbered och skicka segmentdata](#push-data).

1. [Jämför antalet universella ID:n med antalet hashade e-postadresser](#compare-id-count).

## Steg 1: Ställ in spårning för [!DNL Analytics]-mätning {#analytics-tracking}

*Annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Om du vill konvertera e-postadresser till [!DNL RampIDs] eller [!DNL ID5] ID:n måste du göra följande:

1. (Om du inte redan har gjort det) Fyll i alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och se till att [AMO-ID:t och EF-ID](/help/integrations/analytics/ids.md) fylls i i dina spårnings-URL:er.

1. Registrera dig hos den universella ID-partnern och distribuera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att visa genomgångar:

   * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n på datorwebbläsare och mobila webbläsare (men inte mobilappar) för att visa igenom dem. Kontakta kontoteamet på Adobe som ger dig anvisningar om att registrera dig för en [!DNL LiveRamp] [!DNL LaunchPad]-tagg från [!DNL LiveRamp] Authentication Traffic Solutions. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

## Steg 2: Skapa en publikkälla i DSP {#source-create}

1. [Skapa en målgruppskälla](source-manage.md) om du vill importera målgrupper till ditt DSP eller ett annonserarkonto. Du kan välja att konvertera dina användaridentifierare till något av de [tillgängliga universella ID-formaten](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel som du använder för att överföra segmentdata.

1. När du har skapat målgruppskällan delar du källkodnyckeln med användaren [!DNL Optimizely].

## Steg 3: Förbered och push-överföra segmentdata {#push-data}

Annonsören måste förbereda och skicka data med [!DNL Optimizely Data Platform]. Kontakta din [!DNL Optimizely]-representant om du har frågor om processen.

1. Hash-koda e-post-ID:n för målgruppen med SHA-256-algoritmen i [!DNL Optimizely Data Platform].

1. Följ [[!DNL Optimizely's] instruktionerna för att överföra segmentet till DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inkludera följande information för att aktivera integreringen:

   * **Source-nyckel:** Detta är den källnyckel som skapades i [steg 2](#source-create).

   * **Kontokod:** Detta är den alfanumeriska DSP kontokoden, som du hittar i DSP på [!UICONTROL Settings] > [!UICONTROL Account].

Segmenten kommer att uppdateras enligt annonsörens konfiguration. Oberoende av hur ofta segmentet uppdateras, upphör inkludering i ett segment efter 30 dagar som standard eller efter en av kunden angiven förfalloperiod. Uppdatera dina segment genom att trycka på dem igen från [!DNL Optimizely] före förfallodatumet. Kontakta ditt Adobe-kontoteam om du vill begära att ett anpassat segment ska upphöra att gälla.

## Steg 4: Jämför antalet universella ID:n med antalet hashade e-postadresser {#compare-id-count}

Segmenten ska vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata ska antalet deltagare vara synligt inom nio (9) timmar.

Verifiera i målgruppsbiblioteket (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet är tillgängligt och fylls i, och jämför antalet universella ID:n med antalet ursprungliga hashade e-postadresser. Mer information om godkända ID-översättningsfrekvenser och varför antalet segment kan variera finns i [Datavarianser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).

## Felsökning

Om du vill felsöka problem med översättningsfrekvens och antal användare läser du i &quot;[Stöd för aktivering av universella ID:n](/help/dsp/audiences/universal-ids.md)&quot;.

Om du vill felsöka problem med konverteringsproceduren kontaktar du kontogruppen på Adobe eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
