---
title: Frågor och svar om universell video
description: Läs mer om universella videoannonser.
feature: DSP Placements, DSP Ads
source-git-commit: 8e0237355e834f4ae2b9ef1ed211e047b41cafe7
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# # FAQs About Universal Video

## Hur skapar man universella videomaterial och annonser?

Universella videomaterial kan bara innehålla universella videoannonser och universella videoannonser kan bara bifogas till universella videomaterial.

Skapa dem på samma sätt som när du skapar andra typer av placeringar och videoklipp:

1. Inom den önskade kampanjen [skapa en universell videoplacering](/help/dsp/campaign-management/placements/placement-create.md), markera [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Du måste ange minst en miljö (Skrivbord, Mobil, Ansluten TV) som mål.

1. I samma kampanj som den universella videoutplaceringen [skapa en enda universell videoannons](/help/dsp/campaign-management/ads/ad-create.md) eller [skapa flera universella videoannonser](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Om du skapar flera annonser måste du ange &quot;[!UICONTROL Universal Video]&quot; som [!UICONTROL Ad Type]. För [!DNL Google] eller [!DNL Flashtalking] annonser, när du har överfört filen klickar du på fältet annonstyp i &quot;[!UICONTROL Review ad types]&quot; och redigera det. För andra typer av annonstaggar anger du annonstypen i den kalkylbladsfil som du överför.

1. [Öppna annonsinställningarna](/help/dsp/campaign-management/ads/ad-edit.md) för varje ny annons och välj önskat videoformat:

   * **[!UICONTROL VPAID]:** Synligheten mäts alltid.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inkluderar lager som inte tillåter visning.
   * **[!UICONTROL VAST]** - Passar för ansluten TV-inventering.

   Se &quot;[Universella inställningar för videoreklam](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; för mer information.

1. [Bifoga de nya videoannonserna](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) till den universella videomappningen.

## Varför är vissa optimeringsmål och paket inte tillgängliga när miljön för uppkopplad TV väljs för en universell videoutplacering?

Mål som är inkompatibla med vanliga anslutna tv-utplaceringar, t.ex. lägsta kostnad per klick, stöds inte för den anslutna TV-miljön i universalvideomonsplaceringar. Paket med inkompatibla optimeringsmål kan inte heller väljas.

## När ska **[!UICONTROL VAST]** videoformat för universella videoannonser?

Använd **[!UICONTROL VAST]** i något av följande scenarier:

* Placeringen kommer att rikta in sig på ansluten TV-inventering.
* Placeringen kommer att rikta in videolagret från Google Ad Manager, Appnexus, SpotX eller Freewheel. Dessa SSP:er stöder inte videoformatet VPAID och VAST.

## Går det att bifoga flera universella videoannonser till samma universella videomaterial?

Ja.
