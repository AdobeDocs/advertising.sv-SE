---
title: '''[!DNL Analytics] Data i Adobe Advertising'
description: '''[!DNL Analytics] Data i Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: b382184072af88273570fc045d0bcebe24ed81fb
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# [!DNL Analytics] Data i Adobe Advertising

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

## Analyssegment

Alla segment skapade i [!DNL Analytics] och publiceras i Experience Cloud.

Det tar 24-48 timmar för nya segment att visas i Adobe Advertising. Uppdateringar av befintliga segment synkroniseras inom cirka åtta timmar.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mätvärden för webbplatsengagemang

>[!NOTE]
>
>* [!DNL Analytics] skickar händelser för EF ID-eVar till Adobe Advertising.  Standardintegreringen stöder inte sändning av beräknade mått eller andra dimensioner (eVars) till Adobe Advertising. Om det beräknade måttet kan hämtas helt i en anpassad händelse kan Adobe Advertising däremot importera den anpassade händelsen.
>* [!DNL Analytics] skickar data till Adobe Advertising per timme.

* [!UICONTROL Timespent_secs_1stvisit]: Antalet sekunder som har ägnats åt webbplatsen under besökarens första besök.
* [!UICONTROL Timespent_secs_total]: Det totala antalet sekunder som har tillbringats på webbplatsen för alla besök i klickfönstret.
* [!UICONTROL Pageviews_1stvisit]: Antalet sidvisningar på webbplatsen under besökarens första besök.
* [!UICONTROL Pageviews_total]: Det totala antalet sidvisningar på webbplatsen för alla besök i klickningsfönstret.
* [[!UICONTROL Bounces] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Antal gånger som [!DNL Analytics] insamlat [!UICONTROL EF ID].

## Konverteringsmått

[!DNL Analytics] skickar konverteringsstatistik till Adobe Advertising dagligen.

### Standardkonverteringsmått

* [[!UICONTROL Revenue] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] mått](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Anpassade konverteringsmått

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

### Anpassade konverteringsmått skapade från eVars och Props

Tillgängliga mätvärden varierar för varje kund. Se &quot;[Skapa konverteringsstatistik från Adobe Analytics eVars och props](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Reserverade konverteringsmått

Dessa mätvärden är specifika för rapportsviten, så de tillgängliga mätvärdena varierar för varje kund och rapportserie.

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
