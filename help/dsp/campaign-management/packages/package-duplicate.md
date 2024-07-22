---
title: Duplicera ett paket
description: Lär dig duplicera ett paket.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
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

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Paketinställningar](package-settings.md)
