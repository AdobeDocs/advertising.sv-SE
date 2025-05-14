---
title: Duplicera ett paket
description: Lär dig duplicera ett paket.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Duplicera ett paket

Duplicera ett paket om du vill skapa ett paket med liknande inställningar. Du kan:

* Duplicera paketet inom den ursprungliga annonseraren och kampanjen eller inom olika

* Du kan även duplicera placeringarna i paketet

* (För duplicerade paket inom de ursprungliga kampanjerna) Duplicera alternativt de ursprungliga annonserna och händelsepixlarna på placeringsnivå

* Ändra flygdatum för det nya paketet

Se [Vad som inte är duplicerat](#package-not-duplicated) för en lista över placeringsinställningar som inte är duplicerade.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på namnet på kampanjen för att öppna vyn [!UICONTROL Packages].

1. Klicka **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** bredvid paketnamnet.

1. Ange de nya paketinställningarna:

   1. Ange det nya paketnamnet.

   1. (Valfritt) Ändra standardinställningarna.

      Som standard:

      * Det nya paketet tilldelas den ursprungliga annonsören och kampanjen.

      * Det nya paketet blir aktivt den aktuella dagen.<!-- and the flight continues for NN  days. -->

      * Placeringar i originalpaketet kopieras till det nya paketet.

      * Annonserna och händelsepixlarna på placeringsnivå kopieras inte till det nya paketet.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#package-not-duplicated}

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

## Bästa metoder för att konfigurera det nya paketet

>[!TIP]
>
>* Använd kalkylblad för att [göra ändringar i flera kampanjkomponenter samtidigt](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Använd märkordsblad för att [överföra flera tredjepartsannonser](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausa det nya paketet tills du är redo att aktivera det.

* Tänk på följande och redigera de nya paketinställningarna efter behov:

   * Har kontot tillräcklig finansiering för att passa den nya paketbudgeten?

   * Behöver det nya paketet en annan budget än det tidigare paketet?

   * Ladda upp kreatörer, inklusive eventuell nödvändig anpassad annonsvåg och schemaläggning, och bifoga dem till placeringarna.

   * Koppla händelsepixlar efter behov till placeringar och annonser.

   * Inkludera geografiska mål och [!DNL DoubleVerify Authentic Brand Safety]-segment på placeringsnivå efter behov för placeringar.

   * För programmatiska garanterade erbjudanden använder du nya avtal-ID:n och skapar standardplaceringar.

   * Skapa nya ersättningar för [!UICONTROL Simple Ad Serving] erbjudanden efter behov.

* För paket där anpassade optimeringsmål används [[!UICONTROL Linked Package for Optimization Learnings Carryover]-inställningen ](/help/dsp/campaign-management/packages/package-settings.md) för varje paket för att använda den tidigare kampanjens historiska data som indata för optimering av paketet.

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Paketinställningar](package-settings.md)
