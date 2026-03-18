---
title: '[!DNL Analytics] data i Adobe Advertising'
description: '[!DNL Analytics] data i Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] data i Adobe Advertising

*Annonsörer med endast Adobe Advertising-Adobe Analytics-integrering*

## Analyssegment

Alla segment som skapats i [!DNL Analytics] och publicerats till Experience Cloud.

Det tar 24-48 timmar innan nya segment visas i Adobe Advertising. Uppdateringar av befintliga segment synkroniseras inom cirka åtta timmar.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mått för webbplatsengagemang

>[!NOTE]
>
>* [!DNL Analytics] skickar händelser för EF-ID [!DNL eVar] till Adobe Advertising.  Standardintegreringen stöder inte sändning av beräknade mått eller andra dimensioner ([!DNL eVars]) till Adobe Advertising. Om det beräknade måttet kan hämtas helt i en anpassad händelse kan Adobe Advertising däremot importera den anpassade händelsen.
>* [!DNL Analytics] skickar data till Adobe Advertising varje timme.

* [!UICONTROL Timespent_secs_1stvisit]: Antalet sekunder som har ägnats åt webbplatsen under besökarens första besök.
* [!UICONTROL Timespent_secs_total]: Det totala antalet sekunder som har tillbringats på webbplatsen för alla besök i fönstret för klicksökning.
* [!UICONTROL Pageviews_1stvisit]: Antalet sidvisningar på webbplatsen under besökarens första besök.
* [!UICONTROL Pageviews_total]: Det totala antalet sidvisningar på webbplatsen för alla besök i klickningsfönstret.
* [[!UICONTROL Bounces]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Antalet gånger som [!DNL Analytics] samlade in en [!UICONTROL EF ID].

## Konverteringsmått

[!DNL Analytics] skickar konverteringsvärden till Adobe Advertising dagligen.

### Standardkonverteringsmått

* [[!UICONTROL Revenue]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals]-mått &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Anpassade konverteringsvärden

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

### Anpassade konverteringsmått skapade från [!DNL eVars] och [!DNL Props]

Tillgängliga mätvärden varierar för varje kund. Se [Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).

### Reserverade konverteringsvärden

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
