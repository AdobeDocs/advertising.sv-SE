---
title: Duplicera placeringar
description: Lär dig duplicera en eller flera placeringar.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Duplicera placeringar

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicera en eller flera placeringar för att skapa placeringar med liknande inställningar. Du kan:

* Skapa flera dubbletter av placeringar
* Duplicera placeringar inom de ursprungliga annonsörerna och kampanjerna eller inom olika
* (För duplicerade placeringar inom de ursprungliga kampanjerna) Duplicera de ursprungliga annonserna om du vill
* Ändra status och flygdatum för de nya placeringarna

Se &quot;[Vad som inte är duplicerat](#placement-not-duplicated)&quot; för en lista med placeringsinställningar som inte är duplicerade.

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Gör något av följande:

   * Om du vill duplicera en placering klickar du  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** bredvid paketnamnet.

   * Så här duplicerar du flera placeringar:

      1. Markera kryssrutan bredvid varje placering som ska dupliceras.

      1. Klicka på i verktygsfältet för gruppåtgärder **[!UICONTROL Duplicate]**.

1. Ange de nya placeringsinställningarna:

   1. (Enstaka placeringar) Ange det nya placeringsnamnet.

   1. I **[!UICONTROL Choose Package (Required)]** väljer du antingen det överordnade paketet eller **[!UICONTROL No package]*.

   1. (Valfritt) Ändra standardinställningarna.

   Inställningarna gäller för alla markerade placeringar.

   Som standard är de nya platserna för den ursprungliga annonstypen, tilldelade till de ursprungliga annonsörer och kampanjer, har flygscheman som börjar den aktuella dagen, pausas och inte innehåller de ursprungliga annonserna.

   När du skapar flera placeringar läggs de nya placeringsnamnen till med en siffra, i sekvens, enligt konventionen &lt;*original_placement_name #N*>, till exempel&quot;Min placering nr 2&quot;.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#placement-not-duplicated}

Alla inställningar från den ursprungliga placeringen dupliceras förutom:

* Experimentera
* (Om du ändrar flygdatum) Anpassad annonsplanering
* (Om du inte bifogar annonser) Anpassad annonseringskoefficient och schemaläggning
* Standardplaceringar för köp av programmatiska annonsköp (PG) för [!UICONTROL Simple Ad Serving] erbjudanden
* (Om du kopierar praktik till en annan kampanj):
   * Geografiska mål
   * Händelsepixlar
   * Annonser
   * Placeringsnivå [!DNL DoubleVerify Authentic Brand Safety] segment (som åsidosätter segmenten på annonsörnivå)

>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Skapa en placering](placement-create.md)
>* [Redigera placeringar](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
