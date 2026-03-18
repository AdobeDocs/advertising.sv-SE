---
title: Använda DSP-integrering med  [!DNL Adobe] [!DNL Real-time CDP]
description: Lär dig hur du gör det möjligt för DSP att importera dina  [!DNL Adobe] [!DNL Real-time CDP] förstapartssegment.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 5110e9b4c966f5d719743d09b5a3aebbb37e0a05
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Konvertera användar-ID från [!DNL Adobe Real-Time CDP] till universella ID

*Beta-funktion*

Använd DSP-integreringen med [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=sv-SE), som är en del av Adobe Experience Platform, för att konvertera dina streckade e-postadresser till universella ID:n för riktad reklam.

1. (Så här konverterar du e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Ställ in spårning för [!DNL Analytics]-mätning:

   1. (Om du inte redan har gjort det) Fyll i alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och [AMO ID och EF ID i dina spårnings-URL:er](/help/integrations/analytics/ids.md).

   1. Registrera dig hos den universella ID-partnern och distribuera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att visa genomgångar:

      * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n på datorwebbläsare och mobila webbläsare (men inte mobilappar) för att visa igenom dem. Kontakta ditt Adobe-kontoteam som ger dig anvisningar om att registrera dig för en [!DNL LiveRamp] [!DNL LaunchPad] -tagg från [!DNL LiveRamp] Authentication Traffic Solutions. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

1. [Skapa en målgruppskälla](source-manage.md) om du vill importera målgrupper till ditt DSP-konto eller till ett annonsörskonto. Du kan välja att konvertera dina användaridentifierare till något av de [tillgängliga universella ID-formaten](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel, som du kommer att använda i nästa steg.

1. Konfigurera en Advertising DSP-målanslutning i Adobe Experience Platform med hjälp av [!UICONTROL Source Key] som genererades i DSP källinställningar.

   Instruktioner om hur du aktiverar DSP-målanslutningen, markerar segment och får åtkomst till kontrollbehörigheter finns i &quot;[Adobe Advertising Cloud DSP-anslutning](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=sv-SE)&quot;.

   Källans e-postadresser måste hashas med hjälp av SHA-256-algoritmen.

1. Kontrollera i målgruppsbiblioteket (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) att segmentet fylls i och jämför antalet universella ID:n med antalet ursprungliga hashade e-postadresser.

   Segmenten bör vara tillgängliga i DSP inom 24 timmar. När DSP har tagit emot segmentdata bör antalet deltagare vara synligt inom nio (9) timmar. Mer information om godkända ID-översättningsfrekvenser och varför antalet segment kan variera finns i [Datavarianser mellan e-post-ID:n och universella ID:n](#universal-ids-data-variances).

Segmenten uppdateras var 24:e timme. Inkluderingen i ett segment upphör dock efter 30 dagar som standard eller efter en av kunden specificerad förfalloperiod. Uppdatera era segment genom att trycka dem igen från Real-Time CDP innan de upphör att gälla. Kontakta Adobe Account Team om du vill begära att ett anpassat segment ska upphöra att gälla.

## Felsökning

Om du vill felsöka problem med översättningsfrekvens och antal användare läser du i &quot;[Stöd för aktivering av universella ID:n](/help/dsp/audiences/universal-ids.md)&quot;.

Om du vill felsöka problem med konverteringsproceduren kontaktar du Adobe Account Team eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om förstapartsmålskällor](/help/dsp/audiences/sources/source-about.md)
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=sv-SE)
>* Adobe Experience Platform [Översikt över destinationskatalogen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=sv-SE)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
