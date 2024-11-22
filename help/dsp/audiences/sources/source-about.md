---
title: Om källor för förstagångspubliker
description: Lär dig hur du konverterar andra användaridentifierare i dina förstapartssegment till universella ID:n för cookiefri målinriktning.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Om källor för förstagångspubliker

*Beta-funktion*

DSP kan importera förstahandssegment som består av hash-kodade e-post-ID:n som är byggda i kunddataplattformen (CDP) och konvertera dem till segment som består av universella ID:n. Varje resulterande ID är personbaserat och annonsfrekvenser används på ID-nivå <!-- Move that info. to somewhere else? -->.

Segmentinformationen omfattar storleken på varje universell ID-typ samt storleken för varje enhetstyp som spåras av cookies eller enhets-ID.

## Universella ID-typer {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Du kan översätta dina egna segment till segment med autentiserade (deterministiska) ID:n från följande universella ID-partners.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * För återmarknadsföring av inloggade användare.

     [!DNL RampIDs] är tillgängligt för användare i Nordamerika, Australien och Nya Zeeland.

     Avgifterna är 0,15 USD per visningar och 0,25 USD per videoredigering.

   * För mätning med [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID:n](https://unifiedid.com):

   * För återmarknadsföring av inloggade användare.

     [!DNL UID2 IDs] är inte tillgängligt för användare i EES och vissa andra länder. Se [listan över förbjudna länder](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Avgifterna är 0,15 USD per visningar och 0,25 USD per videoredigering.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Kunddataplattformar som stöds för segment från första part

DSP har upprättat kopplingar till följande CDP:er för att snabbt importera era egna segment.

DSP kan även ansluta till ytterligare CDP:er med batchvis, direktuppspelad eller API-baserad datadelning. Om du vill integrera med en ny CDP kontaktar du kontoteamet på Adobe.

### [!DNL Adobe Real-Time CDP]

DSP är ett integrerat *mål* för [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), som är en del av Adobe Experience Platform.

I [!DNL Real-Time CDP] är mål anslutningar till externa dataplattformar som tillåter smidig dataaktivering. Du kan använda destinationer för att aktivera dina hash-kodade e-postadresser för riktad annonsering i DSP. Mer information om destinationer finns i [Destinationshandboken](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) för Experience Platform, inklusive en översikt över produkten, instruktioner om hur du [skapar målarbetsytor](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) och [skapar målanslutningar](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) samt [aktiverar data till destinationer](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Se &quot;[Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md) om du vill att DSP ska kunna importera dina [!DNL Adobe] [!DNL Real-time CDP]-segment och konvertera dina hashade e-postadresser till universella ID:n.&quot;

### [!DNL ActionIQ]

Du kan dela din organisations egna data från [!DNL ActionIQ]-kunddataplattformen med DSP för att konvertera dina hashade e-postadresser till universella ID:n för riktad annonsering i DSP. Den här integreringen kräver anpassning. Kontakta kontoteamet på Adobe för mer information.

### [!DNL Amperity]

Du kan dela din organisations egna data från [!DNL Amperity]-kunddataplattformen med DSP för att konvertera dina hashade e-postadresser till universella ID:n för riktad annonsering i DSP. Mer information finns i [Konvertera användar-ID:n från [!DNL Amperity] till universella ID:n](/help/dsp/audiences/sources/source-amperity.md).

### [!DNL Optimizely]

Du kan dela din organisations egna data från [!DNL Optimizely]-kunddataplattformen med DSP för att konvertera dina hashade e-postadresser till universella ID:n för riktad annonsering i DSP. Mer information finns i [Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n](/help/dsp/audiences/sources/source-optimizely.md).

### [!DNL Tealium]

Du kan dela din organisations egna data från [!DNL Tealium]-kunddataplattformen med hjälp av [!DNL Amazon Web Services]. Mer information om hur du konverterar dina streckade e-postadresser till universella ID:n för riktad annonsering i DSP finns i &quot;[Konvertera användar-ID:n från [!DNL Tealium] till universella ID:n](/help/dsp/audiences/sources/source-tealium.md)&quot;.

>[!MORELIKETHIS]
>
>* [Hantera målgruppskällor för att aktivera universella ID-målgrupper](source-manage.md)
>* [Stöd för aktivering av universella ID](/help/dsp/audiences/universal-ids.md)
>* [Konvertera användar-ID:n från [!DNL Adobe Real-Time CDP] till universella ID:n](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertera användar-ID:n från [!DNL Amperity] till universella ID:n](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertera användar-ID:n från [!DNL Optimizely] till universella ID:n](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertera användar-ID:n från [!DNL Tealium] till universella ID:n](/help/dsp/audiences/sources/source-tealium.md)
>* [Om målgruppshantering](/help/dsp/audiences/audience-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
