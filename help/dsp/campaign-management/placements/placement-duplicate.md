---
title: Duplicera placeringar
description: Lär dig duplicera en eller flera placeringar.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 1fe0d3c026cac52104d54b571fd9c2202cc2384b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Duplicera placeringar

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicera en eller flera placeringar för att skapa placeringar med liknande inställningar. Du kan:

* Skapa flera dubbletter av placeringar
* Duplicera placeringar inom de ursprungliga annonsörerna och kampanjerna eller inom olika
* (För duplicerade placeringar inom de ursprungliga kampanjerna) Duplicera de ursprungliga annonserna om du vill
* Ändra status och flygdatum för de nya placeringarna

Se [Vad som inte är duplicerat](#placement-not-duplicated) för en lista över placeringsinställningar som inte är duplicerade.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]** på undermenyn.

1. Gör något av följande:

   * Om du vill duplicera en placering klickar du på **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** bredvid paketnamnet.

   * Så här duplicerar du flera placeringar:

      1. Markera kryssrutan bredvid varje placering som ska dupliceras.

      1. Klicka på **[!UICONTROL Duplicate]** i verktygsfältet för gruppåtgärder.

1. Ange de nya placeringsinställningarna:

   1. (Enstaka placeringar) Ange det nya placeringsnamnet.

   1. Välj antingen det överordnade paketet eller **[!UICONTROL No package]* på menyn **[!UICONTROL Choose Package (Required)]**.

   1. (Valfritt) Ändra standardinställningarna.

   Inställningarna gäller för alla markerade placeringar.

   Som standard är de nya platserna för den ursprungliga annonstypen, tilldelade till de ursprungliga annonsörer och kampanjer, har flygscheman som börjar den aktuella dagen, pausas och inte innehåller de ursprungliga annonserna.

   När du skapar flera placeringar läggs de nya placeringsnamnen till med en siffra, i sekvens, med konventionen &lt;*original_placement_name #N*>, till exempel &quot;Min placering nr 2&quot;.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#placement-not-duplicated}

Alla inställningar från den ursprungliga placeringen dupliceras förutom:

* Experimentera
* (Om du ändrar flygdatum) Anpassad annonsplanering
* (Om du inte bifogar annonser) Anpassad annonseringskoefficient och schemaläggning
* Standardersättningar för köp med programgaranti (PG) för [!UICONTROL Simple Ad Serving]-erbjudanden
* (Om du kopierar praktik till en annan kampanj):
   * Geografiska mål
   * Händelsepixlar
   * Annonser
   * Segment på placeringsnivå [!DNL DoubleVerify Authentic Brand Safety] (som åsidosätter segmenten på annonsörnivå)

## Bästa metoder för att konfigurera nya placeringar

>[!TIP]
>
>* Använd kalkylblad för att [göra ändringar i flera kampanjkomponenter samtidigt](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Använd märkordsblad för att [överföra flera tredjepartsannonser](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausa de nya placeringarna tills du är redo att aktivera dem.

* Tänk på följande och redigera de nya placeringarna efter behov:

   * Har kontot tillräcklig finansiering för att passa de nya placeringsbudgetarna?

   * Behöver de nya placeringarna andra budgetar än de tidigare?

   * Ladda upp kreatörer, inklusive eventuell nödvändig anpassad annonsvåg och schemaläggning, och bifoga dem till placeringarna.

   * Koppla händelsepixlar efter behov till placeringar och annonser.

   * Inkludera geografiska mål och [!DNL DoubleVerify Authentic Brand Safety]-segment på placeringsnivå efter behov för placeringarna.

   * För programmatiska garanterade erbjudanden använder du nya avtal-ID:n och skapar standardplaceringar.

   * Skapa nya ersättningar för [!UICONTROL Simple Ad Serving] erbjudanden efter behov.

>[!MORELIKETHIS]
>
>* [Om placeringshantering](placement-about.md)
>* [Skapa en placering](placement-create.md)
>* [Redigera placeringar](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
