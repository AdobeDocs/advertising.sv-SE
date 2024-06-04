---
title: Skapa och implementera ett anpassat segment
description: Lär dig hur du skapar och implementerar ett anpassat segment för att spåra användare som exponeras för annonser eller användare som besöker dina webbsidor.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 2fe54fbcd9711e714246f074ede086910b538b80
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Skapa och implementera ett anpassat segment

Ni kan samla in era egna data från förstapartsmålgrupper genom att skapa och implementera ett anpassat DSP. Du kan använda segmentet för att spåra a) användare som exponeras för annonser från datorer och mobila enheter och b) användare som besöker specifika webbsidor. Du kan senare rikta om användare i segmentet med ytterligare annonser eller hindra användare i segmentet från att få ytterligare annonser.

>[!NOTE]
>
>Om du vill spåra användar-ID:n från förfrågningar om avanmälan till försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA), skapar du en [CCPA Avanmäl segmentet](ccpa-opt-out-segment-create.md).

## Krav för segment för att spåra ID5

*Betafunktion*

* Innan du genererar ett segment för att spåra användare som är kopplade till ID5-ID:n måste du signera ett avtal med [!DNL ID5] och skaffa din organisations partner-ID. Kontakta kontoteamet på Adobe för instruktioner.

* För mätning i Adobe Analytics måste du:

   1. Slutför alla [krav för implementering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)och se till att [AMO ID och EF ID](/help/integrations/analytics/ids.md) fylls i i dina spårnings-URL:er.

   1. Lägg till följande parameter på dina webbsidor före eller i dialogrutan [JavaScript-kod krävs för [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) - var som helst innan den sista händelsetjänsten initieras.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Exempel:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

   1. Använd valfritt felsökningsverktyg för webbläsare för att verifiera att varje anrop initieras till domänen `lasteventf-tm.everesttech.net` och innehåller parametern `_les_id5` med ett krypterat ID5-ID som värde.

## Skapa och implementera ett anpassat segment

1. Skapa segmentet:

   1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Ovanför datatabellen klickar du **[!UICONTROL Create]**.

   1. Ange ett unikt **[!UICONTROL Segment Name]**.

   1. För **[!UICONTROL Segment Type]**, markera *[!UICONTROL Custom]*.

   1. Ange **[!UICONTROL Lookback Window]**, vilket är antalet dagar som en användares cookie stannar kvar i segmentet.

      Standardfönstret är 45 dagar. Ange ett värde mellan 1 och 365.

   1. Klicka **[!UICONTROL Advanced]** för att utöka de avancerade inställningarna och sedan välja de typer av användaridentifierare som segmenttaggen spårar:

      * *[!UICONTROL Cookies]:* (Standardvärdet) Segmenttaggen spårar cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Segmenttaggspår [!DNL ID5] ID. Inga avgifter tas ut för visningar som skickas till universella ID:n.

        **[!UICONTROL Terms of Service]:** Villkor för serviceavtal för användning av universella ID:n. Du eller en annan användare på DSP måste acceptera villkoren en gång innan du kan använda universella ID:n för en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren å din organisations vägnar. Om du vill läsa villkoren klickar du **>**. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera taggar för att spåra segmentet efter behov:

   1. Återgå till **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Håll markören över segmentraden och klicka **[!UICONTROL Get Pixel]**.

      * Så här spårar du besökare på en webbsida:

         1. Kopiera spårningstaggen för sidvyn, som har etiketten[!UICONTROL Desktop or mobile websites].&quot;

         1. (Taggar för segment som spårar [!DNL ID5] ID) Ersätt i den kopierade taggen `ID5_PARTNER_ID` med partner-ID som [!DNL ID5] som tilldelats din organisation.

            Om ditt ID5-partner-ID till exempel är `abcde` och den genererade segmenttaggen är

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            och ersätt `ID5_PARTNER_ID` med `abcde` i -taggen för att få följande:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Organisationen fick sitt partner-ID när den signerade ett avtal med [!DNL ID5]. Om du inte känner till ditt partner-ID kontaktar du ditt Adobe-kontoteam.

            Det här steget behövs inte för att taggar ska kunna spåra [!DNL ID5] ID för användare som exponeras för en annonsenhet på datorer eller mobila enheter.

         1. Ange taggen till annonsören eller webbplatskontakten för distribution.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      * Så här spårar du användare som exponeras för en annonsenhet på datorer eller mobila enheter:

         1. Kopiera taggen för visningsspårning, som har etiketten &quot;[!UICONTROL Desktop or mobile ads].&quot;

         1. Lägg till taggen i antingen [!UICONTROL Pixel] för varje relevant annons eller för [!UICONTROL Event Pixels] i [[!UICONTROL Tracking] inställningar för varje relevant placering](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!TIP]
>
>Håll reda på segmentstorleken när användarna spåras.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Redigera segmentinformation](segment-edit.md)
>* [Ta bort ett segment](segment-delete.md)
>* [Visa spårningspixlar för ett segment](segment-view-pixels.md)
>* [Dela eller Sluta dela ett segment](segment-share.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
