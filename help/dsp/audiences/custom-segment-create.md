---
title: Skapa och implementera ett anpassat segment
description: Lär dig hur du skapar och implementerar ett anpassat segment för att spåra användare som exponeras för annonser eller användare som besöker dina webbsidor.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Skapa och implementera ett anpassat segment

Ni kan samla in era egna data från förstapartsmålgrupper genom att skapa och implementera ett anpassat DSP. Du kan använda segmentet för att spåra a) användare som exponeras för annonser från datorer och mobila enheter och b) användare som besöker specifika webbsidor. Du kan senare rikta om användare i segmentet med ytterligare annonser eller hindra användare i segmentet från att få ytterligare annonser.

>[!NOTE]
>
>Om du vill spåra användar-ID:n från förfrågningar om att avanmäla sig från försäljning på din webbplats skapar du ett [CCPA-segment för avanmälan från försäljning](ccpa-opt-out-segment-create.md) enligt California Consumer Privacy Act (CCPA).

## Krav för segment för att spåra ID5

*Beta-funktion*

* Innan du genererar ett segment för att spåra användare som är kopplade till ID5-ID:n måste du signera ett avtal med [!DNL ID5] och få din organisations partner-ID. Kontakta kontoteamet på Adobe för instruktioner.

* För mätning i Adobe Analytics måste du:

   1. Slutför alla [krav för implementering av [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) och se till att [AMO-ID:t och EF-ID:t](/help/integrations/analytics/ids.md) fylls i i dina spårnings-URL:er.

   1. Lägg till följande parameter på dina webbsidor före eller inom den [JavaScript-kod som krävs för [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) - var som helst innan den sista händelsetjänsten initieras.

      ```window.id5PartnerId=ID5_PartnerID;```

      Exempel:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Mer information om det fullständiga taggformatet finns i [Format för JavaScript-konverteringsspårningstaggar, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md) och [Format för JavaScript-konverteringsspårningstaggar, version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md).

   1. Använd valfritt felsökningsverktyg för webbläsare för att verifiera att varje anrop initieras till domänen `lasteventf-tm.everesttech.net` och innehåller parametern `_les_id5` med ett krypterat ID5-ID som värde.

## Skapa och implementera ett anpassat segment

1. Skapa segmentet:

   1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** på huvudmenyn.

   1. Klicka på **[!UICONTROL Create]** ovanför datatabellen.

   1. Ange en unik **[!UICONTROL Segment Name]**.

   1. För **[!UICONTROL Segment Type]** väljer du *[!UICONTROL Custom]*.

   1. Ange **[!UICONTROL Lookback Window]**, vilket är antalet dagar som en användares cookie stannar i segmentet.

      Standardfönstret är 45 dagar. Ange ett värde mellan 1 och 365.

   1. Klicka på **[!UICONTROL Advanced]** för att utöka de avancerade inställningarna och välj sedan de typer av användaridentifierare som segmenttaggen spårar:

      * *[!UICONTROL Cookies]:* (Standard) Segmenttaggen spårar cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Segmenttaggen spårar [!DNL ID5] ID:n. Inga avgifter tas ut för visningar som skickas till universella ID:n.

        **[!UICONTROL Terms of Service]:** Villkoren i serviceavtalet för användning av universella ID:n. Du eller en annan användare på DSP måste acceptera villkoren en gång innan du kan använda universella ID:n för en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren å din organisations vägnar. Om du vill läsa villkoren klickar du på **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera taggar för att spåra segmentet efter behov:

   1. Gå tillbaka till **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Håll markören över segmentraden och klicka på **[!UICONTROL Get Pixel]**.

      * Så här spårar du besökare på en webbsida:

         1. Kopiera spårningstaggen för sidvyn, som har etiketten [!UICONTROL Desktop or mobile websites].

         1. (Taggar för segment som spårar [!DNL ID5] ID:n) Ersätt `ID5_PARTNER_ID` i den kopierade taggen med det partner-ID som [!DNL ID5] har tilldelats din organisation.

            Om ditt ID5-partner-ID till exempel är `abcde` och den genererade segmenttaggen är

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            ersätt sedan `ID5_PARTNER_ID` med `abcde` i taggen för att få följande:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Din organisation fick partner-ID när den signerade ett avtal med [!DNL ID5]. Om du inte känner till ditt partner-ID kontaktar du ditt Adobe-kontoteam.

            Det här steget är inte nödvändigt för att taggar ska kunna spåra [!DNL ID5] ID:n för användare som exponeras för en annonsenhet på datorer eller mobila enheter.

         1. Ange taggen till annonsören eller webbplatskontakten för distribution.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      * Så här spårar du användare som exponeras för en annonsenhet på datorer eller mobila enheter:

         1. Kopiera taggen för visningsspårning, som har etiketten [!UICONTROL Desktop or mobile ads].

         1. Lägg till taggen antingen på fliken [!UICONTROL Pixel] för varje relevant annons eller i avsnittet [!UICONTROL Event Pixels] i inställningarna för [[!UICONTROL Tracking] för varje relevant placering &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!TIP]
>
>Håll reda på segmentstorleken när användarna spåras.

>[!MORELIKETHIS]
>
>* [Om målgruppshantering](audience-about.md)
>* [Redigera segmentinformation](segment-edit.md)
>* [Ta bort ett segment](segment-delete.md)
>* [Visa spårningspixlar för ett segment](segment-view-pixels.md)
>* [Dela eller sluta dela ett segment](segment-share.md)
>* [Skapa och implementera ett [!UICONTROL CCPA Opt-Out-of-Sale] segment &#x200B;](ccpa-opt-out-segment-create.md)
>* [Skapa en återanvändbar målgrupp](reusable-audience-create.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
