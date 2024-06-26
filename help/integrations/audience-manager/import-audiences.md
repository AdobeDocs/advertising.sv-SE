---
title: Importera Adobe Audience Manager-segment för annonsinriktning
description: Så här importerar du [!DNL Adobe] målgrupper i Advertising DSP och Search med Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importera Adobe Audience Manager-segment för annonsinriktning

Annonserar DSP och [!DNL Advertising Search, Social, & Commerce] kan alla hämta in metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers [!DNL Adobe] målgrupper<!-- segments or audiences? Standardize terms per AAM's docs -->, inklusive:

* Adobe Audience Manager segment

* Adobe Analytics-segment som publiceras till Adobe Experience Cloud

* Segment som har skapats med Adobe Experience Cloud [!DNL Audience Library]

* Segment som har skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager

För åtkomst [!DNL Adobe] målgrupper i DSP eller [!DNL Creative]måste ni importera målgrupperna till DSP. För åtkomst [!DNL Adobe] målgrupper i [!DNL Search, Social, & Commerce]måste du importera målgrupperna till [!DNL Search, Social, & Commerce].

## Förutsättningar

* Annonsören måste implementera [den [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) version 2.0 eller senare. The [!DNL Identity Service] ger ett universellt, beständigt ID som identifierar besökarna i alla lösningar i Experience Cloud.

  Implementeringen innefattar att lägga till [!DNL Identity service] koda till varje webbsida på annonsörens webbplatser.

* Organisationen måste vara [aktiverat för Experience Cloud-tjänster](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) och ha Experience Cloud [!DNL Organization ID] (kallades tidigare [!DNL IMS org ID]).

  The [!UICONTROL Organization ID] kan företag med flera Adobe Experience Cloud-produkter dela data mellan vissa av dessa produkter.

* (Annonsörer med [!DNL Analytics]) Annonsören måste [implementera [!DNL Analytics] använda `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) version 1.6.4 eller senare.

* Annonsörens webbplatsbesökare har inte så många [!DNL Apple Safari] -användare.

* (Rekommenderas när annonsören använder både Audience Manager och [!DNL Analytics]) Om du vill minska antalet anrop till varje webbsida tar du bort Audience Manager [!DNL Data Integration Library] kod för datainsamling och aktivera vidarebefordran på serversidan för varje [!DNL Analytics] istället. Mer information finns i &quot;[Översikt över vidarebefordran på serversidan](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Rekommenderas) Om du vill ha högre matchningsfrekvenser skickar du endast data från förstahandswebbplatser till Adobe Advertising. Om annonsören paketerar data från tredje part eller offlinedata från ett kundrelationshanteringssystem kan dataläckage minska matchningsfrekvensen.

## Importera målgrupper från Audience Manager till DSP

### Steg för att importera målgrupper till DSP

The [!DNL Adobe] Konto- och datahanteringsteamen utför följande steg.

1. Kontoteamet på Adobe bör konfigurera inställningen på annonsörnivå[!UICONTROL Adobe Analytics Cloud].&quot;

1. Kontoteamet på Adobe bör skicka en begäran till datahanteringsteamet om att importera organisationens Audience Manager-segment med hjälp av ADvertising DSP:s inbyggda API-integrering.

### Vilka förändringar ger Audience Manager?

API automatiskt:

* Skapar två DSP mål i Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mappar de två destinationerna till alla Audience Manager-segment, så att Audience Manager kan dela segmenten med det DSP annonskonto som är associerat med samma Experience Cloud [!DNL Organization ID] används för Audience Manager.

  Organisationen kan även ta bort onödiga segment från destinationerna i Audience Manager.

* Lägger till följande cookie-synkpixel för utbyte i Audience Manager-behållaren för att öka kundkampanjernas räckvidd:

   * Adobe AdCloud: 411 (Den här pixeln kommer som standard och automatiskt som en del av [!DNL Identity Service] version 2.0. Organisationer med [!DNL Identity Service] i versioner under 2.0 bör den här pixeln läggas till i Audience Manager-behållaren.

## Importera målgrupper från Audience Manager till [!DNL Search, Social, & Commerce]

### Steg för att importera målgrupper till [!DNL Search, Social, & Commerce]

[!DNL Adobe] personalen utför de flesta eller alla av följande steg.

1. Kontoteamet på Adobe bör skicka en begäran till datahanteringsteamet om att skapa en integrering mellan [!DNL Search, Social, & Commerce] och Audience Manager. Inkludera namnen på de Audience Manager-segment som du vill exportera till [!DNL Search, Social, & Commerce].

1. Konfigurera mål för Audience Manager [!DNL Search, Social, & Commerce]:

   1. Skapa två nya mål: `[!UICONTROL Adobe Media Optimizer (HTTP)]` och `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] är ett tidigare namn för [!DNL Search, Social, & Commerce].

   1. Ange segmenten för var och en av destinationerna.

      Med [!UICONTROL Automatically map all current and future segments] kan alla segment mappas och synkroniseras dagligen.

      The [!UICONTROL Manually map segments] gör att du kan mappa segmenten manuellt för att synkronisera med gruppmålet (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Inga segment behöver mappas manuellt till HTTP-målet.

1. Inom [!DNL Search, Social, & Commerce], antingen [!DNL Search, Social, & Commerce] implementeringsteamet eller en användare med klienthanterarrollen för direkt åtkomst bör initiera importen från [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Organisationens Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) krävs. ID:t måste vara samma som det som används för organisationens Audience Manager-konto.

### Vilka förändringar ger Audience Manager?

Två [!DNL Search, Social, & Commerce] destinationer blir tillgängliga för organisationen i Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Datasynkronisering

Den inledande importen tar ca 24 timmar. Efter den första importen synkroniseras data i realtid med en fördröjning på en till två sekunder.

Data för segmentmedlemskap skickas endast när någon av följande händelser inträffar:

* (Annonsörer med DSP):

   * Segmentet är riktat mot en annons på Adobe Advertising.

   * Segmentet läggs till i [!DNL Adobe AdCloud Cross-Channel] och mål i realtid i användargränssnittet i Audience Manager.

* (Annonsörer med [!DNL Search, Social, & Commerce]):

   * Segmentet är riktat mot en sökannons från Adobe Advertising.

   * Segmentet läggs till i [!DNL Adobe Media Optimizer] batch- och HTTP-mål i användargränssnittet i Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Hur DSP synkroniserar data

DSP synkroniserar data automatiskt med [!DNL Adobe Experience Cloud Identity (ECID) Service]. Under synkroniseringen [!DNL ECID Service] anropar Adobe Advertising at [!DNL cm.everesttech.net]. Eftersom Adobe Advertising är en betrodd domän synkroniseras ID från överordnade sidor i stället för i målpubliceringens iframes, som de flesta andra aktiveringspartners gör. Audience Manager identifierar unika användare efter enhets-ID med hjälp av [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), som även kallas [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Hur sökningar, sociala medier och Commerce synkroniserar data

Sökning, socialt arbete och Commerce synkroniserar data automatiskt med [!DNL Adobe Experience Cloud Identity (ECID) Service]. Under synkroniseringen [!DNL ECID Service] anropar Adobe Advertising at [!DNL cm.everesttech.net], som är en betrodd domän som tillhör Adobe Advertising. Audience Manager identifierar unika användare efter enhets-ID med hjälp av [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), som även kallas [!DNL Device ID].

## Var hittar du dina synkroniserade segment?

### I DSP

DSP sorterar segmentnamnen efter Audience Manager-taxonomin och inkluderar motsvarande antal segmentmedlemmar i:

* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): På [!UICONTROL Adobe Segments] -fliken i [!UICONTROL Audience Targeting] -avsnitt.

* I [målgruppsinställningar](/help/dsp/audiences/audience-settings.md): På [!UICONTROL Adobe Segments] -fliken.

### I ADVERTISING CREATIVE

I [!DNL Creative], är segmenten tillgängliga i upplevelseinställningarna för målnoder.

### I [!DNL Advertising Search, Social, & Commerce]

I [!DNL Search, Social, & Commerce]är segmenten tillgängliga när du skapar en [!DNL Google] målgrupp med [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; från [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

För varje [!DNL Google] målgrupper som du skapar, [!DNL Google] används för att anpassa målgruppens storlek.

>[!MORELIKETHIS]
>
>* [Integrering av Adobe Advertising med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
