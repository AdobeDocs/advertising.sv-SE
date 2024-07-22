---
title: Om [!UICONTROL Simple Ad Serving]
description: Läs mer om [!UICONTROL Simple Ad Serving] erbjudanden med hjälp av pixlar för händelsespårning.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Om [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] tillhandahåller garanterad, icke-beslutad annonsleverans och rapportering för en angiven utgivare och en enda annonstyp med en enda dedikerad placering. Använd [!DNL Simple Ad Serving] när din utgivare inte kan genomföra ditt avtal via avtal-ID. All målgruppsanpassning, budgetering och begränsning samt frekvensbegränsning hanteras av utgivaren. Utför dessa erbjudanden via pixlar för händelsespårning.

Med [!UICONTROL Simple Ad Serving] hanteras varje annons direkt av utgivaren (webbplatsservern) och DSP tillhandahåller en pixel för händelsespårning som skickas till utgivaren, som måste implementera pixeln och hantera DSP annonser. Beroende på lagertypen mäter händelsepixlarna intryckta händelser, klickfrekvens och videouppspelningshändelser.

Följande annonstyper är tillgängliga:

* förrullning av datorstandard
* surfplatta och mobilstandard för pre-roll
* ansluten TV-standard för förrullning
* visa
* ljud

Du kan skapa ett [!UICONTROL Simple Ad Serving]-avtal i vyn [!UICONTROL Inventory] > [!UICONTROL Deals]. DSP genererar automatiskt en placering med undertypen [!DNL Simple ad serving] för annonsen. Placeringen har som mål avtalet men tillåter inte ytterligare målgruppsanpassning, budget eller frekvensbegränsning. Du kan bara redigera vissa av avtalsinställningarna, till exempel avtalsnamn, CPM, avtryck och flygdatum.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] placeringar uppfyller inte kontots användbara medel eller kampanjens och paketets budgetar. Utgifterna spåras dock och räknas in i dessa budgetar. Även när CPM:en är $0 spåras alltid händelsedata.

>[!MORELIKETHIS]
>
>* [Skapa ett [!UICONTROL Simple Ad Serving] avtal](simple-deal-create.md)
>* [Redigera [!UICONTROL Simple Ad Serving] avtalsinställningar](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Inställningar](simple-deal-settings.md)
>* [Visa en detaljerad rapport för ett avtal](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
