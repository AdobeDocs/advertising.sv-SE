---
title: Implementera [!DNL Google Ads] max-kampanjer för prestanda
description: Läs mer om arbetsflödet för konfiguration [!DNL Google Ads] maximalt antal kampanjer.
source-git-commit: 333d32963b96d2add1d99b2e27d7725341b4cfdf
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementera [!DNL Google Ads] max-kampanjer för prestanda

I [!DNL Google Ads] max-kampanjer, ni inte skapar annonsgrupper, annonser eller nyckelord. I stället anger du en eller flera resursgrupper, som innehåller rubriker, beskrivningar och överförda bilder, logotyper och [!DNL YouTube videos]. [!DNL Google Ads] kombinerar automatiskt resurserna för att leverera annonser baserat på kanalen (som [!DNL YouTube], [!DNL Gmail], eller [!DNL Search]).

Du kan visa dina befintliga maximala prestandakampanjer, med prestandadata i tabell- och trenddiagramformat, i [!DNL Campaigns] vy, data är inte tillgängliga på lägre nivåer. Prestandadata på kampanjnivå finns även i rapporter och i Adobe Analytics (för annonsörer med en [Integrering med Analytics](/help/integrations/analytics/overview.md). För att visa prestandadata för maximala prestandakampanjer i [!DNL Analytics]måste kampanjen använda [uppgraderad s_kwcid spårningskod](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) (som spårar kampanj-ID och annonsgrupps-ID).

>[!NOTE]
>
>* Du måste överföra alla bildfiler manuellt. Länkar till [!DNL Google Merchant Center] produktflöden stöds inte.
>* Endast nödvändiga inställningar är tillgängliga. Logga in på [!DNL Google Ads] redigerare.
>* Stöd för listgrupper är inte tillgängligt. Om du vill hantera och visa data för listgrupper loggar du in på [!DNL Google Ads] redigerare.


## Steg som ska konfigureras [!DNL Google Ads] max-kampanjer för prestanda

Du kan ställa in maximala prestandakampanjer individuellt från [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vy.

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) med kampanjtyp **[!UICONTROL Performance Max]**.

   Ange [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting]och [!UICONTROL URL Options]. Ange eventuellt [!UICONTROL Negative Keywords], ange [!UICONTROL Negative Websites]och/eller åsidosätt [!UICONTROL Campaign Tracking] alternativ.

1. Skapa resursgrupper och överför resurser för kampanjen:

   1. Klicka på längst ned i kampanjinställningarna **[!UICONTROL Manage Asset Groups]**.

   1. Ange inställningarna för den första resursgruppen och överför bilderna, logotyperna och valfria videor för resursgruppen.

      Se [beskrivningar av tillgångsgruppsinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) för att förstå kraven och specifikationerna.

   1. Lägg till ytterligare resursgrupper efter behov.

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Lägg till kampanjen i en hybridportfölj för optimering.
