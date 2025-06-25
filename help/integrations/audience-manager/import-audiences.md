---
title: Importera Adobe Audience Manager-segment för annonsinriktning
description: Lär dig hur du importerar dina [!DNL Adobe] målgrupper till Advertising DSP och Sök med Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importera Adobe Audience Manager-segment för annonsinriktning

Advertising DSP och [!DNL Advertising Search, Social, & Commerce] kan samla in metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers [!DNL Adobe] målgrupper <!-- segments or audiences? Standardize terms per AAM's docs -->, inklusive:

* Adobe Audience Manager segment

* Adobe Analytics-segment som publiceras till Adobe Experience Cloud

* Segment som har skapats med Adobe Experience Cloud [!DNL Audience Library]

* Segment som har skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager

Om du vill få åtkomst till [!DNL Adobe] målgrupper i DSP eller [!DNL Creative] måste du importera målgrupperna till DSP. Om du vill få åtkomst till [!DNL Adobe] målgrupper i [!DNL Search, Social, & Commerce] måste du importera målgrupperna till [!DNL Search, Social, & Commerce].

## Förutsättningar

* Annonsören måste implementera [versionen  [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) 2.0 eller senare. [!DNL Identity Service] innehåller ett universellt, beständigt ID som identifierar dina besökare för alla lösningar i Experience Cloud.

  I implementeringen ingår att lägga till [!DNL Identity service]-koden på varje webbsida på annonsörens webbplatser.

* Organisationen måste vara [aktiverad för Experience Cloud-tjänster](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) och ha en Experience Cloud [!DNL Organization ID] (kallades tidigare [!DNL IMS org ID]).

  Med [!UICONTROL Organization ID] kan organisationer med flera Adobe Experience Cloud-produkter dela data mellan vissa produkter.

* (Annonsörer med [!DNL Analytics]) Annonsören måste [implementera [!DNL Analytics] med `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) version 1.6.4 eller senare.

* Annonsörens webbplatsbesökare har inte ett stort antal [!DNL Apple Safari] användare.

* (Rekommenderas när annonsören använder både Audience Manager och [!DNL Analytics]) Om du vill minska antalet anrop till varje webbsida tar du bort befintlig Audience Manager [!DNL Data Integration Library]-kod för datainsamling och aktiverar servervidarebefordran för varje [!DNL Analytics] -rapportserie i stället. Mer information finns i [Översikt över vidarebefordran på serversidan](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Rekommenderas) Om du vill ha högre matchningsfrekvenser skickar du endast data från förstahandswebbplatser till Adobe Advertising. Om annonsören paketerar data från tredje part eller offlinedata från ett kundrelationshanteringssystem kan dataläckage minska matchningsfrekvensen.

## Importera Audience Manager-målgrupper till DSP

### Steg för att importera målgrupper till DSP

Konto- och dataåtgärdsteamen för [!DNL Adobe] utför följande steg.

1. Adobe Kontoteam bör konfigurera inställningen [!UICONTROL Adobe Analytics Cloud] på annonsörnivå.

1. Adobe Account Team ska skicka en begäran till datateam om att importera organisationens Audience Manager-segment med hjälp av Advertising DSP inbyggda API-integrering.

### Vilka förändringar resulterar i Audience Manager?

API automatiskt:

* Skapar två DSP-mål i Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Kopplar de två destinationerna till alla Audience Manager-segment, så att Audience Manager kan dela segmenten med DSP-annonskontot som är associerat med samma Experience Cloud [!DNL Organization ID] som används för Audience Manager.

  Organisationen kan även ta bort onödiga segment från Audience Manager destinationer.

* Lägger till följande cookie-synkpixel för utbyte i organisationens Audience Manager-behållare för att öka kundkampanjernas räckvidd:

   * Adobe AdCloud: 411 (Denna pixel kommer som standard och automatiskt som en del av [!DNL Identity Service] version 2.0. Organisationer med [!DNL Identity Service] versioner under 2.0 bör lägga till den här pixeln i sin Audience Manager-behållare.

## Importera Audience Manager-målgrupper till [!DNL Search, Social, & Commerce]

### Steg för att importera målgrupper till [!DNL Search, Social, & Commerce]

[!DNL Adobe]-personal utför de flesta eller alla av följande steg.

1. Adobe Account Team ska skicka en begäran till datahanteringsteamet om att skapa en integrering mellan [!DNL Search, Social, & Commerce] och Audience Manager. Inkludera namnen på de Audience Manager-segment som du vill exportera till [!DNL Search, Social, & Commerce].

1. Konfigurera mål för [!DNL Search, Social, & Commerce] i Audience Manager:

   1. Skapa två nya mål: `[!UICONTROL Adobe Media Optimizer (HTTP)]` och `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] är ett tidigare namn för [!DNL Search, Social, & Commerce].

   1. Ange segmenten för var och en av destinationerna.

      Med alternativet [!UICONTROL Automatically map all current and future segments] mappas och synkroniseras alla segment dagligen.

      Med alternativet [!UICONTROL Manually map segments] kan du mappa segmenten manuellt för att synkronisera med gruppmålet (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Inga segment behöver mappas manuellt till HTTP-målet.

1. Inom [!DNL Search, Social, & Commerce] bör antingen implementeringsteamet [!DNL Search, Social, & Commerce] eller en användare med klienthanterarrollen för direkt åtkomst initiera importen från [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Organisationens Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) krävs. ID:t måste vara samma som det som används för organisationens Audience Manager-konto.

### Vilka förändringar resulterar i Audience Manager?

Två [!DNL Search, Social, & Commerce] mål blir tillgängliga för organisationen i Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Datasynkronisering

Den inledande importen tar ca 24 timmar. Efter den första importen synkroniseras data i realtid med en fördröjning på en till två sekunder.

Data för segmentmedlemskap skickas endast när någon av följande händelser inträffar:

* (Annonsörer med DSP):

   * Segmentet är avsett för en Adobe Advertising-webbannons.

   * Segmentet läggs till i gruppen [!DNL Adobe AdCloud Cross-Channel] och målplatserna i realtid i Audience Manager användargränssnitt.

* (Annonsörer med [!DNL Search, Social, & Commerce]):

   * Segmentet är avsett för en sökannons från Adobe Advertising.

   * Segmentet läggs till i gruppen [!DNL Adobe Media Optimizer] och HTTP-målen i Audience Manager användargränssnitt.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Så här synkroniserar DSP data

DSP synkroniserar data automatiskt med [!DNL Adobe Experience Cloud Identity (ECID) Service]. Under synkroniseringen anropar [!DNL ECID Service] Adobe Advertising på [!DNL cm.everesttech.net]. Eftersom Adobe Advertising är en betrodd domän synkroniseras ID från överordnade sidor i stället för i målpubliceringens iframes, som de flesta andra aktiveringspartners gör. Audience Manager identifierar unika användare utifrån enhets-ID:n med hjälp av [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), som även kallas [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Hur sökningar, sociala medier och Commerce synkroniserar data

Sök, Socialt och Commerce synkroniserar data automatiskt med [!DNL Adobe Experience Cloud Identity (ECID) Service]. Under synkroniseringen anropar [!DNL ECID Service] Adobe Advertising på [!DNL cm.everesttech.net], som är en betrodd domän som tillhör Adobe Advertising. Audience Manager identifierar unika användare utifrån enhets-ID:n med hjälp av [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), som även kallas [!DNL Device ID].

## Var hittar du dina synkroniserade segment?

### I DSP

DSP organiserar segmentnamnen efter Audience Manager taxonomi och inkluderar motsvarande antal medlemskap i:

* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): På fliken [!UICONTROL Adobe Segments] i avsnittet [!UICONTROL Audience Targeting].

* I [målgruppsinställningar](/help/dsp/audiences/audience-settings.md): På fliken [!UICONTROL Adobe Segments].

### I ADVERTISING CREATIVE

I [!DNL Creative] är segmenten tillgängliga i upplevelseinställningarna för målnoder.

### I [!DNL Advertising Search, Social, & Commerce]

I [!DNL Search, Social, & Commerce] är segmenten tillgängliga när du skapar en [!DNL Google]-målgrupp med [!UICONTROL Data Source] [!UICONTROL Adobe Audience] från [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

För varje [!DNL Google]-målgrupp som du skapar anger [!DNL Google] målgruppens storlek.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-integreringar med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
