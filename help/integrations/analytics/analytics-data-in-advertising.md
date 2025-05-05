---
title: '[!DNL Analytics] data i Adobe Advertising'
description: '[!DNL Analytics] data i Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] data i Adobe Advertising

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

## Analyssegment

Alla segment som skapats i [!DNL Analytics] och publicerats i Experience Cloud.

Det tar 24-48 timmar för nya segment att visas i Adobe Advertising. Uppdateringar av befintliga segment synkroniseras inom cirka åtta timmar.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mätvärden för webbplatsengagemang

>[!NOTE]
>
>* [!DNL Analytics] skickar händelser för EF-ID:t [!DNL eVar] till Adobe Advertising.  Standardintegreringen stöder inte sändning av beräknade mått eller andra dimensioner ([!DNL eVars]) till Adobe Advertising. Om det beräknade måttet kan hämtas helt i en anpassad händelse kan Adobe Advertising däremot importera den anpassade händelsen.
>* [!DNL Analytics] skickar data till Adobe Advertising per timme.

* [!UICONTROL Timespent_secs_1stvisit]: Antalet sekunder som har ägnats åt webbplatsen under besökarens första besök.
* [!UICONTROL Timespent_secs_total]: Det totala antalet sekunder som har tillbringats på webbplatsen för alla besök i fönstret för klicksökning.
* [!UICONTROL Pageviews_1stvisit]: Antalet sidvisningar på webbplatsen under besökarens första besök.
* [!UICONTROL Pageviews_total]: Det totala antalet sidvisningar på webbplatsen för alla besök i klickningsfönstret.
* [[!UICONTROL Bounces]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=sv-SE)
* [[!UICONTROL Visits]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=sv-SE)
* [!UICONTROL ef_id_instances]: Antalet gånger som [!DNL Analytics] samlade in en [!UICONTROL EF ID].

## Konverteringsmått

[!DNL Analytics] skickar konverteringsvärden till Adobe Advertising dagligen.

### Standardkonverteringsmått

* [[!UICONTROL Revenue]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=sv-SE)
* [[!UICONTROL Orders]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=sv-SE)
* [[!UICONTROL Units]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=sv-SE)
* [[!UICONTROL Carts]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=sv-SE)
* [[!UICONTROL Cart Views]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=sv-SE)
* [[!UICONTROL Checkouts]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=sv-SE)
* [[!UICONTROL Cart Additions]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=sv-SE)
* [[!UICONTROL Cart Removals]-mått ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=sv-SE)

### Anpassade konverteringsmått

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

### Anpassade konverteringsmått skapade från [!DNL eVars] och [!DNL Props]

Tillgängliga mätvärden varierar för varje kund. Se [Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).

### Reserverade konverteringsmått

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-mått i Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
