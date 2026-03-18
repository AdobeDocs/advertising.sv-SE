---
title: Samla in klicknings- och visningsdata från Advertising DSP-kampanjer
description: Lär dig hur du fångar in cookie-baserat intryck och klickar på händelser från Advertising DSP-annonser med Audience Manager-pixlar
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Samla in data om medieexponering från Advertising DSP kampanjer

*Annonsörer med endast Advertising DSP*

*Annonsörer med endast Adobe Advertising-Adobe Audience Manager-integrering*

I det här dokumentet beskrivs hur du taggar Advertising DSP-annonser för att fånga in cookie-baserat intryck och klickningshändelser med Audience Manager-pixlar, och ytterligare åtgärder som krävs för att använda data.

Händelsepixlarna fångar inte in händelser som inträffar i cookie-fria miljöer, som mobilappar och ansluten TV (CTV).

## Steg 1: Konfigurera en datakälla i Audience Manager {#set-up-data-source}

I Audience Manager skapar du en [datakälla](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=sv-SE) för DSP-intrycket och klickar på data. Inkludera datakällans ID [&#x200B; i varje händelsetagg &#x200B;](#implement-dsp-pixels) så att alla spårade händelser tilldelas datakällan.

>[!NOTE]
> Det är möjligt att samla in alla intryckta data och klickdata för annonskampanjer som körs på flera DSP:er inom en enda datakälla.

## Steg 2: Implementera intrycket och klicka på händelsepixlar på webbsidor {#implement-dsp-pixels}

Annonsörer kan skapa och implementera händelsetaggar för sina egna varumärken. Kontakta vid behov din Adobe Audience Manager-konsult eller ditt kontoteam på Adobe för att få hjälp.

>[!NOTE]
>
>Om din organisation använder [!DNL Analytics]-spårning kanske du inte behöver Audience Manager-klickspårning. Adobe Analytics fångar upp klicksignaler och kan skicka dem till Audience Manager via [vidarebefordran på serversidan](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=sv-SE).

### Pixelsyntax

Händelsepixlar måste innehålla följande parametrar.

**Impression-tracking-pixlar:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

med [valfria ytterligare parametrar](#parameters) som prefix med `&`

**Klickspårning av pixlar:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

med [valfria ytterligare parametrar](#parameters) som prefix med `&`

Var:

* `[Audience Manager customer domain]` är det domännamn som ska skicka intrycket eller klickningshändelser till [!DNL Adobe].

* `[source id]` är ID:t för den [datakälla](#set-up-data-source) där du spårar DSP-indrag och klickar på data.

* `[redirect URL]` är den dubbelkodade omdirigerings-URL:en. Om du använder ett kodningsverktyg online, t.ex. www.urlencoder.org, kör du strängen genom kodaren och kodar om resultatet.

* `${TM_CAMPAIGN_ID_NUM}` är det numeriska kampanj-ID:t i DSP. Om du vill hårdkoda ett enskilt kampanj-ID i stället för att använda DSP-makrot letar du reda på ID:t i kampanjinställningarna.

* Varje [parameter](#key-value-pairs) har prefixet `&` och formatet `d_parameter=parameter_id`, där `parameter` ersätts av nyckelvärdepar för det nya fältet. Exempel: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parametrar som nyckelvärdepar {#parameters}

**Format:** `d_parameter=parameter_id`

    där:
    
    * parametern har prefixet `&amp;`
    
    * `parameter` ersätts med nyckelvärdepar för det nya fältet
    
    Exempel: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Båda pixeltyperna kan innehålla ytterligare parametrar som *nyckelvärdepar* för att samla in egenskaper eller för att tillhandahålla kampanjmetadata (till exempel ett placeringsnamn eller ett kampanjnamn) för andra rapporter. Ett nyckelvärdepar består av två relaterade element: *key*, som är en konstant som definierar datauppsättningen, och *value*, som är en variabel som tillhör uppsättningen.

I nyckelvärdepar kan värdevariabeln vara antingen ett hårdkodat ID eller ett *makro*, som är en liten enhet av självständig kod som dynamiskt ersätts med motsvarande värden när annonstaggen läses in för kampanj- och användarspårning. För kampanjrelaterade parametrar kan du använda [DSP-makron](/help/dsp/campaign-management/macros.md) i stället för Audience Manager-makron för att skicka kampanjattribut tillsammans med motsvarande inställningsdata eller klicka på data till Audience Manager, med en enda pixel för alla annonser. De DSP-makron som du infogar i händelsepixlarna måste vara lämpliga värden för de nyckel/värde-par som du inkluderar i pixlarna. För tangenten `d_placement` använder du till exempel DSP-makrot `${TM_PLACEMENT_ID_NUM}` som värde för att hämta placerings-ID:n som genereras av Adobe Advertising-makrot.

En lista över makron som Audience Manager stöder för att visa händelsepixlar finns i &quot;[Hämta kampanjkomprimeringsdata via pixelanrop](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=sv-SE#supported-key-value-pairs)&quot;.

En lista över makron som Audience Manager stöder för klickhändelsepixlar finns i &quot;[Hämta klickdata via pixelanrop](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=sv-SE)&quot;.

>[!TIP]
>
>* Det bästa sättet är att inkludera kampanj-, placerings-, kreativa (annons) och webbplats-ID:n så att du kan använda kampanjattributen för att skapa Audience Manager-egenskaper.
>* Ytterligare parametrar krävs för att skapa Audience Optimization-rapporter.
>* Ersätt värdena i nyckelvärdepar med relevanta [DSP-makron](/help/dsp/campaign-management/macros.md) så att du kan använda en enda pixel för alla annonser i alla kampanjer. Ändra till exempel `d_campaign=[%campaignID%]` till `d_campaign=${TM_CAMPAIGN_ID_NUM}` för att hämta kampanj-ID:n som genereras av Adobe Advertising-makrot.
>* Om det behövs kan du skapa egna parametrar med hårdkodade värden. Exempel: `d_DSP=AdCloud`

Exempel på en visningshändelsepixel:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Var ska pixlarna läggas till?

#### Pixel för Impression-tracking

Koppla en pixel för händelsespårning för ett intryck till alla annonser i dina [!DNL DSP]-kampanjer. Du kan göra det på följande platser:

* På placeringsnivån, som tillämpar pixeln som standard på alla annonser i placeringen. Lägg till pixeln i fältet [[!UICONTROL Event pixels] &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md) i avsnittet Spårning i placeringsinställningarna.

* På annonsnivån, som åsidosätter händelsepixlar på placeringsnivå. I annonsinställningarna [skapar du en händelsepixel på fliken [!UICONTROL Pixel] &#x200B;](/help/dsp/campaign-management/ads/ad-edit.md).

* (För annonser på en annonsserver från tredje part) På annonsnivån i annonsservern.

#### Klickspårningspixel

På annonsservern infogar du klickhändelsepixeln (med den kodade URL:en tillagd) på det ställe där du normalt infogar annonsens klicknings-URL.

## Steg 3: Åtgärder efter implementeringen

När händelsetaggar har implementerats flödar data in på Audience Manager datainsamlingsservrar. Utför följande åtgärder innan du kan använda data i rapporter.

### Skapa en [!DNL Amazon S3]-bucket och en datakälla

När dina data finns på Audience Manager-servrarna måste du skapa en [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])-bucket och sedan en datakälla som alla pixeldata skickas till. Kontakta din Audience Manager-konsult eller [kundtjänst](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=sv-SE) om du behöver hjälp.

### Skapa Audience Manager-egenskaper och -segment

Dina händelsedata flödar till Audience Manager som [oanvända signaler](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=sv-SE). Skapa [regelbaserade &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=sv-SE) manuellt från inkapslade data och skapa sedan [segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=sv-SE) med dessa egenskaper innan du kan använda data i rapporter.

Exempeldiagram som fyller i användarnivådata för användare som exponeras för en viss kreativ i DSP:

1. Identifiera händelsen som `d_event = imp`.
1. Identifiera det kreativa ID:t i DSP-kampanjen och mappa det sedan till egenskapen som `d_creative=[Creative ID]`.

![Skärm för att skapa egenskaper](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP-makron](/help/dsp/campaign-management/macros.md)
>* [Översikt över att skicka exponeringsdata för DSP-medier till Adobe Audience Manager](overview.md)
>* [Användningsexempel](use-cases.md)
