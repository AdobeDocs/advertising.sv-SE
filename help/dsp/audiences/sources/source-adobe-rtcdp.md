---
title: Använda DSP integrering med [!DNL Adobe] [!DNL Real-time CDP]
description: Lär dig hur du aktiverar DSP att importera [!DNL Adobe] [!DNL Real-time CDP] förstahandssegment.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID

*Betafunktion*

Använd DSP integrering med [den [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), som ingår i Adobe Experience Platform, för att konvertera dina hashade e-postadresser till universella ID:n för riktad reklam.

1. (Konvertera e-postadresser till [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonsörer med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Ställ in spårning för [!DNL Analytics] mått:

   1. (Om du inte redan har gjort det) Slutför alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och [AMO ID och EF ID i dina spårnings-URL:er](/help/integrations/analytics/ids.md).

   1. Registrera dig hos den universella ID-partnern och distribuera universell ID-specifik kod på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att visa genomgångar:

      * **För [!DNL RampIDs]:** Du måste distribuera ytterligare en JavaScript-tagg på dina webbsidor för att matcha konverteringar från ID:n i webbläsare för datorer och mobila enheter (men inte i mobilappar) för att kunna visa igenom dem. Kontakta kontoteamet på Adobe som ger dig anvisningar om hur du registrerar dig för en [!DNL LiveRamp] [!DNL LaunchPad] tagga från [!DNL LiveRamp] Lösningar för autentiseringstrafik. Registreringen är kostnadsfri, men du måste signera ett avtal. När du har registrerat dig genererar ditt Adobe-kontoteam en unik tagg som din organisation kan implementera på dina webbsidor.

1. [Skapa en publikkälla](source-manage.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto. Du kan välja att konvertera dina användaridentifierare till någon av [tillgängliga universella ID-format](source-about.md).

   Källinställningarna innehåller en automatiskt genererad källnyckel, som du kommer att använda i nästa steg.

1. I Adobe Experience Platform konfigurerar du en målanslutning DSP annonsering med [!UICONTROL Source Key] som genererades i DSP källinställningar.

   Instruktioner om hur du aktiverar DSP målanslutning, markerar segment och får åtkomst till kontrollbehörigheter finns i &quot;[Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   Källans e-postadresser måste hashas med hjälp av SHA-256-algoritmen.

1. När du är klar med alla steg kan du verifiera i ditt målgruppsbibliotek (som är tillgängligt när du skapar eller redigerar en målgrupp från [!UICONTROL Audiences] > [!UICONTROL All Audiences] eller inom placeringsinställningarna) som segmentet fylls i inom 24 timmar. Jämför antalet universella ID:n med antalet ursprungliga hash-adresser.

   Översättningsfrekvensen för hash-kodade e-postadresser till universella ID:n måste vara större än 90 %. Om du till exempel skickar 100 hashas-e-postadresser från din kunddataplattform bör de översättas till mer än 90 universella ID:n. En översättningsgrad på 90 % eller mindre är ett problem. Mer information om hur antalet segment kan variera finns i &quot;[Orsaker till dataavvikelser mellan e-post-ID och universella ID](#universal-ids-data-variances).&quot;

   Om du vill ha felsökningssupport kontaktar du kontoteamet på Adobe eller `adcloud-support@adobe.com`.

Segmenten uppdateras var 24:e timme. Inkluderingen i ett segment upphör dock efter 30 dagar för att säkerställa sekretessefterlevnad, så uppdatera målgrupperna genom att föra över dem från Real-Time CDP var 30:e dag eller mindre.

>[!MORELIKETHIS]
>
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Översikt över målkatalog](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Importera autentiserade segment manuellt från [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID](/help/dsp/audiences/sources/source-tealium.md)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
