---
title: Ange placeringar och annonser för ett privat avtal
description: Lär dig hur du använder ett privat avtal med ytterligare praktik och annonser.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: d6d295119bc974a87840e757877c1507237a6fa2
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Ange placeringar och annonser för ett privat avtal

För erbjudanden utan garanti kan du ange att erbjudandet ska vara ett lagermål för nya placeringar från [!UICONTROL Placements] vy.

För programmatiska annonserbjudanden (PG) kan du skapa praktik med angivna annonser från [!UICONTROL Deals] vy.

Du kan också [bifoga annonser till placeringar](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) som hör ihop med PG och erbjudanden utan garanti när som helst.

## Ange ett icke-garanterat avtal som ett lagermål för en placering

* [Skapa en placering från [!UICONTROL Placements] visa](/help/dsp/campaign-management/placements/placement-create.md). I [!UICONTROL Inventory Targeting] väljer du det privata erbjudandet.

## Bifoga placeringar och annonser i en PG-affär

1. Klicka på **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicka på  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. I [!UICONTROL Ad & Campaign Selection] väljer du de annonser som ska användas för placeringen:

       1. Välj annonsören, kampanjen och annonstypen. Du kan också välja en annonsstatus att filtrera annonserna med.
       
       1. Markera kryssrutan bredvid varje annons som ska användas för erbjudandet i listan över tillgängliga annonser.
       
       1. Klicka **[!UICONTROL Apply]**.
   
   1. På skärmen för placeringsinställningar:

      1. Ange placeringsnamnet.

      1. (Valfritt) Redigera [placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md), inklusive att skriva över standarderbjudandet, som automatiskt fylls i med CPM-värdet från avtalet, ändra datumintervallet eller bifoga fler annonser.

      Avtalen anges automatiskt i avsnittet Inventeringsmål. Alla andra målinriktningsalternativ är inte tillämpliga.

      1. Klicka på **[!UICONTROL Create placement]**.

Placeringen börjar gälla när utgivaren har aktiverat ditt PG-erbjudande-ID.

>[!NOTE]
>
> Du behöver inte skicka avtalstaggen till utgivaren för verifiering.

>[!MORELIKETHIS]
>
>* [Om privat lager](private-inventory-about.md)
>* [Lista placeringar och annonser för ett privat avtal](/help/dsp/inventory/private-deal-view-placements.md)
>* [Skapa information om avtal-ID manuellt](deal-id-create.md)
>* [Manuella inställningar för avtal-ID](deal-id-settings.md)
>* [Ställ in en programgaranterad affär](programmatic-guaranteed-set-up.md)
