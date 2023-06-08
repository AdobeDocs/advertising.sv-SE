---
title: Hantera [!DNL Google Ads] placeringar
description: Lär dig hur du skapar och hanterar prisvärda ersättningar för [!DNL Google Ads] annonsgrupper.
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] placeringar

*[!DNL Google Ads]endast konton*

Du kan skapa och redigera placeringar för annonsgrupper i [kampanjtyper som stöds](/help/search-social-commerce/introduction/supported-inventory.md) som har ett visningsnätverk som mål inom en [synkroniserat annonsnätverkskonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Skapa [!DNL Google Ads] placeringar

>[!TIP]
>
>Om du vill skapa flera placeringar samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket, kontot, kampanjen och annonsgruppen och klicka sedan på **[!UICONTROL Continue]**.

1. Konfigurera [placeringsinställningar](#placement-settings).

1. Klicka på **[!UICONTROL Post]**.

## Redigera [!DNL Google Ads] placeringar

>[!TIP]
>
>Om du vill redigera flera placeringar samtidigt använder du [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Markera kryssrutan bredvid varje rad som ska redigeras.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") .

1. Redigera [placeringsinställningar](#placement-settings).

   För flera placeringar tillämpas ändringarna på alla markerade placeringar. För vissa alfanumeriska fält kan du ändra befintliga värden till ett angivet värde, ersätta en befintlig sträng med en angiven sträng, lägga till ett angivet prefix i början av varje värde eller lägga till ett suffix i slutet av varje värde. För vissa monetära fält kan du ändra befintliga värden till ett angivet värde eller antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

1. Spara data:

   * (Enstaka placeringar) Klicka **[!UICONTROL Post]**.

   * (Flera placeringar) Klicka **[!UICONTROL Post Now]**.

## Placeringsinställningar {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Webbplatser i det innehållsnätverk där annonsen kan visas. Ange en giltig URL, till exempel www.example.com, example.com eller www.example.com/shoes/kids. Om du vill ange flera strängar avgränsar du dem med kommatecken eller anger dem på separata rader. URL:en får inte innehålla ett frågetecken (`?`). **Obs!** Du kan [utelämna webbplatsplaceringar](placement-negative-create.md) från [!UICONTROL Placements] > [!UICONTROL Negatives] i annonsgruppen och kampanjinställningarna.

**[!UICONTROL Status]:** Placeringens visningsstatus: *Aktiv* (för att möjliggöra budgivning, standard), *Pausad* (för att inaktivera budgivning), eller *Borttagen* (ta bort placeringen, (endast befintliga placeringar).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Valfritt) Den maximala kostnaden per klick (CPC) eller kostnaden per tusen visningar (vCPM) för den placeringsbaserade annonsen, beroende på kampanjanbudsstrategin. Det här värdet åsidosätter annonsköpet på gruppnivå.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Om placeringar](placement-about.md)
>* [Skapa negativa placeringar](placement-negative-create.md)
>* [Ändra status för placeringar och negativa placeringar](placement-status-edit.md)
