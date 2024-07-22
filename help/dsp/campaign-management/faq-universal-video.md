---
title: Frågor och svar om universell video
description: Läs mer om universella videoannonser.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Frågor och svar om universell video

Med [universella videoannonser](/help/dsp/campaign-management/ads/ad-about.md#ad-types) kan du målinrikta videolagret från skrivbordsmiljöer, mobilmiljöer och anslutna TV-miljöer för VPAID- och VAST-inventering med en enda videoplacering.

## Hur skapar man universella videomaterial och annonser?

Universella videomaterial kan bara innehålla universella videoannonser och universella videoannonser kan bara bifogas till universella videomaterial.

Skapa universella videomaterial och annonser på ungefär samma sätt som du skapar andra typer av videomaterial:

1. I den önskade kampanjen [skapar du en universell videoutplacering](/help/dsp/campaign-management/placements/placement-create.md) och väljer [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Du måste ange minst en miljö (Skrivbord, Mobil, Ansluten TV) som mål.

1. I samma kampanj som den universella videoplaceringen [skapar du en universell videoannons](/help/dsp/campaign-management/ads/ad-create.md) eller [skapar flera universella videoannonser](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Om du skapar flera annonser måste du ange [!UICONTROL Universal Video] som [!UICONTROL Ad Type]:

   * För [!DNL Google] eller [!DNL Flashtalking] annonser: Klicka på fältet **[!UICONTROL Ad Type]** i steget [!UICONTROL Review ad types] efter att du har överfört filen och välj **[!UICONTROL Universal Video]**.

   * För andra typer av annonstaggar: I kalkylbladsfilen som du överför anger du fältet Annonstyp för varje annons som **[!UICONTROL Universal Video]**.

1. [Öppna annonsinställningarna](/help/dsp/campaign-management/ads/ad-edit.md) för varje ny annons och välj önskat videoformat:

   * **[!UICONTROL VPAID]:** Synlighet mäts alltid.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inkluderar lager som inte tillåter visningsbarhetsmätning.
   * **[!UICONTROL VAST]** - Passar för ansluten TV-inventering.

   Mer information finns i [Universella inställningar för videoannonsering](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

1. [Koppla de nya universella videoannonserna](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) till den universella videoplaceringen.

## Varför är vissa optimeringsmål och paket inte tillgängliga när miljön för uppkopplad TV väljs för en universell videoutplacering?

Mål som är inkompatibla med vanliga anslutna tv-utplaceringar, t.ex. lägsta kostnad per klick, stöds inte för den anslutna TV-miljön i universalvideomonsplaceringar. Paket med inkompatibla optimeringsmål kan inte heller väljas.

## När ska videoformatet **[!UICONTROL VAST]** användas för universella videoannonser?

Använd **[!UICONTROL VAST]** i något av följande scenarier:

* Placeringsmålen för ansluten TV-inventering.
* Placeringen avser videolager från Google Ad Manager, Appnexus, SpotX eller Freewheel. Dessa SSP:er stöder inte videoformatet VPAID och VAST.

## Går det att bifoga flera universella videoannonser till samma universella videomaterial?

Ja.
