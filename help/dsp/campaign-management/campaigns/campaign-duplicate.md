---
title: Duplicera en kampanj
description: Lär dig hur du duplicerar en kampanj.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Duplicera en kampanj

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicera en kampanj för att skapa en ny kampanj med liknande inställningar. Du kan:

* Duplicera kampanjen för den ursprungliga annonsören eller för en annan

* Duplicera originalpaketen och -placeringarna om du vill

* Ändra flygdatum för den nya kampanjen

Se [Vad som inte är duplicerat](#campaign-not-duplicated) för en lista över placeringsinställningar som inte är duplicerade.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** bredvid kampanjnamnet.

1. Ange de nya kampanjinställningarna:

   1. Ange det nya kampanjnamnet och slutflygdatumet.

   1. (Valfritt) Ändra standardinställningarna.

      Som standard tilldelas den nya kampanjen till den ursprungliga annonsören, har ett flygschema som börjar den aktuella dagen och innehåller originalpaketen och -placeringarna.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#campaign-not-duplicated}

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

## Bästa metoder för att konfigurera den nya kampanjen

>[!TIP]
>
>* Använd kalkylblad för att [göra ändringar i flera kampanjkomponenter samtidigt](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Använd märkordsblad för att [överföra flera tredjepartsannonser](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausa den nya kampanjen tills du är redo att aktivera den.

* Tänk på följande och redigera de nya kampanjinställningarna efter behov:

   * Har kontot tillräcklig finansiering för att passa den nya kampanjbudgeten?

   * Behöver den nya kampanjen en annan budget än den föregående?

   * Ladda upp kreatörer, inklusive eventuell nödvändig anpassad annonsvåg och schemaläggning, och bifoga dem till placeringarna.

   * Koppla händelsepixlar efter behov till placeringar och annonser.

   * Inkludera geografiska mål och [!DNL DoubleVerify Authentic Brand Safety]-segment på placeringsnivå efter behov för placeringar.

   * För programmatiska garanterade erbjudanden använder du nya avtal-ID:n och skapar standardplaceringar.

   * Skapa nya ersättningar för [!UICONTROL Simple Ad Serving] erbjudanden efter behov.

* För prestandakampanjer (det vill säga kampanjer med paket som använder anpassade optimeringsmål) använder du [[!UICONTROL Linked Package for Optimization Learnings Carryover]-inställningen ](/help/dsp/campaign-management/packages/package-settings.md) för varje paket för att använda den föregående kampanjens historiska data som indata för optimering av paketet.

>[!MORELIKETHIS]
>
>* [Om kampanjhantering](campaign-about.md)
>* [Skapa en kampanj](campaign-create.md)
>* [Redigera en kampanj](campaign-edit.md)
>* [Visa ändringsloggen för en kampanj](campaign-change-log.md)
>* [Kampanjinställningar](campaign-settings.md)
