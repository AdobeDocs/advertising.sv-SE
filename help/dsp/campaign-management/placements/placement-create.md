---
title: Skapa en placering
description: Lär dig hur du skapar en placering.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Skapa en placering

>[!TIP]
>
>Skapa praktik baserat på specifika kampanjmål eller rapporteringsbehov.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på namnet på kampanjen där placeringen ska inkluderas.

1. Klicka på **[!UICONTROL Create]** ovanför datatabellen. Klicka på placeringstypen i avsnittet [!UICONTROL Placement Types] på menyn.

   Placeringstypen bestämmer annonstypen som placeringen kan inkludera.

1. Ange [placeringsinställningarna](placement-settings.md):

   1. Ange inställningarna för [!UICONTROL Placement Basics].

   1. I avsnittet [!UICONTROL Goals] anger du [!UICONTROL Gross Budget] och eventuellt anger ytterligare placeringsmål.

      Vissa fält har standardvärden som du kan åsidosätta.

      Om paketet som placeringen är tilldelad till har paketnivåpaketering, återspeglar mål- och paketinställningarna paketinställningarna.

   1. (Valfritt) I avsnittet [!UICONTROL Geo-Targeting] kan du begränsa de platser som är inkluderade eller exkluderade.

      Om du inte identifierar specifika platser anges alla platser som mål.

      >[!NOTE]
      >
      >Ort och DMA-platser är inte tillgängliga för Roku-ersättningar.

   1. I avsnittet [!UICONTROL Inventory Targeting] kan du begränsa vilka lagerkällor som ska inkluderas eller exkluderas.

      För de flesta placeringstyper inkluderas alla lagertyper och alla källor för varje typ som standard. För [!DNL Roku] placeringar måste du ange lagertyp och källor.

   1. (Valfritt) I avsnittet [!UICONTROL Site Targeting] kan du begränsa vilka webbplatser du vill använda som mål och ange vilka webbplatser du vill utesluta.

   1. (Valfritt) I avsnittet [!UICONTROL Audience Targeting]:

      1. Begränsa publiken. Detta inkluderar att välja målgruppssegment att inrikta sig på inom placeringen.

         För [!DNL Roku]-placeringar kan du utnyttja [DSP unika målgruppsmatchning med  [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) genom att ta med ett eller flera målgruppssegment som kan matchas mot den [!DNL Roku] (valfria) deterministiska datamängden.

      1. (För kampanjer med enhetsövergripande målgruppsanpassning på personnivå, valfritt) När placeringen riktar sig till en eller flera specifika målgrupper kan du aktivera personbaserad målinriktning på olika enheter för placeringen.

         Personbaserad målinriktning mellan olika enheter tillhandahålls av [!DNL LiveRamp] endast med data från USA. Tjänsten är tillgänglig för alla annonsörer på $0,35 CPM för visningar som levereras med enhetsdiagrammet [!DNL LiveRamp] (det vill säga för enheter som inte hittas i målgruppssegmenten).

   1. (Valfritt) Använd varumärkessäkerhetsbegränsningar för dina placeringar i avsnittet [!DNL Brand Safety and Media Targeting].

   1. (Valfritt) Ange händelsepixlar från tredje part eller konverteringspixlar för annonser i placeringen i avsnittet [!DNL Tracking].

      >[!NOTE]
      >
      >([!DNL Roku] placeringar) Tredjepartsleverantörer av pixlar som godkänts av [!DNL Roku] omfattar [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] och [!DNL Research Now].

1. Klicka på **[!UICONTROL Create Placement]**.

1. (Valfritt) Lägg till annonser på placeringen:

   1. Klicka på **[!UICONTROL Attach an ad]**.

   1. Gör något av följande:

      * Så här skapar du en ny annons:

         1. Klicka på **[!UICONTROL Create a New Ad].**

         1. Ange annonsinställningarna för [ljudannonser](/help/dsp/campaign-management/ads/ad-settings-audio.md), [anslutna TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [visningsannonser](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobilannonser](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [inbyggda annonser](/help/dsp/campaign-management/ads/ad-settings-native.md), [pre-roll-ads](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) eller [universella videoannonser](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Universella videomaterial kan bara innehålla universella videoannonser.

         1. Klicka på **[!UICONTROL Save & Submit for Review]**.

         1. (Valfritt) För varje ytterligare annons som du vill skapa för placeringen klickar du på **[!UICONTROL Attach Another Ad]** och upprepar sedan steg 1-3.

         1. Om du inte vill bifoga några befintliga annonser klickar du på **[!UICONTROL I'm done for now]**.

      * Så här bifogar du befintliga annonser i kampanjen:

      1. Klicka på **[!UICONTROL Select an Ad]**.

      1. Gör något av följande:

         * Så här lägger du till en annons i taget:

            1. Klicka på **[!UICONTROL Select]bredvid annonsnamnet.**

            1. (Valfritt) För varje ytterligare annons som du vill bifoga klickar du på **[!UICONTROL Attach Another Ad]** och upprepar sedan processen.

         * Så här lägger du till upp till 20 annonser i taget:

            1. Markera kryssrutan ovanför annonslistan.

            1. Markera kryssrutan bredvid varje annons som ska läggas till.

            1. Klicka på **[!UICONTROL Attach]**.

            1. Klicka på **[!UICONTROL Select]** bredvid annonsnamnet.

      1. (Valfritt) Om du vill åsidosätta standardflygperioden och annonsrotationen för specifika annonser i placeringen:

         1. Klicka på **[!UICONTROL Custom Schedule Ads]**.

         1. Gör något av följande:

            * Om du vill lägga till en flygning klickar du på **[!UICONTROL Add Flight]** och anger sedan startdatum och slutdatum.

            * Om du vill lägga till en befintlig flygning i en annons klickar du på **[!UICONTROL +]** i annonsraden för flygkolumnen.

            * Om du vill ta bort en befintlig flygning från en annons klickar du på **[!UICONTROL x]** i annonsraden för flygkolumnen.

            * (När flera annonser har samma flygning) Om du vill rotera annonserna ojämnt klickar du på **[!UICONTROL Even Rotation]** i flyginformationen och anger sedan den relativa vikt som varje annons ska roteras med, i procent.

              Den totala vikten måste vara lika med 100.

         1. Klicka på **[!UICONTROL Continue]** i det övre högra hörnet.

         1. Granska flyginformationen och klicka sedan på **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Om placeringshantering](placement-about.md)
>* [Redigera placeringar](placement-edit.md)
>* [Hantera aktivitetsmultiplikatorer för placeringar](placement-manage-bid-multipliers.md)
>* [Redigera annonsplanerna för placeringar](placement-edit-ad-schedule.md)
>* [Pausa eller aktivera en placering](placement-pause-activate.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
>* [Visa prognosrapport för placering](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Kortkommandon](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Felsökningsprestanda](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: Så här skapar du en standardbildskärmsplacering](https://video.tv.adobe.com/v/340454)
