---
title: Implementera  [!DNL Google Ads] maximala prestandakampanjer
description: Lär dig mer om arbetsflödet för att konfigurera  [!DNL Google Ads] maximala prestandakampanjer.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementera max-kampanjer för [!DNL Google Ads] prestanda

I [!DNL Google Ads] prestandamängdskampanjer konfigurerar du inte annonsgrupper, annonser eller nyckelord. I stället anger du en eller flera resursgrupper, som innehåller rubriker, beskrivningar och överförda bilder, logotyper och [!DNL YouTube videos], i kampanjinställningarna. [!DNL Google Ads] kombinerar automatiskt resurserna för att hantera annonser baserat på kanalen (till exempel [!DNL YouTube], [!DNL Gmail] eller [!DNL Search]).

Du kan visa dina befintliga maximala prestandakampanjer, med prestandadata i tabell- och trenddiagramformat, i vyn [!DNL Campaigns]. Data är inte tillgängliga på lägre nivåer. Prestandadata på kampanjnivå är också tillgängliga i rapporter och i Adobe Analytics (för annonsörer med en [Analytics-integrering](/help/integrations/analytics/overview.md)). Om du vill visa prestandadata för maximala prestandakampanjer i [!DNL Analytics] måste kampanjen använda den [uppgraderade spårningskoden för AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) (som spårar kampanj-ID och annonsgrupps-ID).

>[!NOTE]
>
>* Du måste överföra alla bildfiler manuellt. Länkar till [!DNL Google Merchant Center] produktfeeds stöds inte.
>* Endast nödvändiga inställningar är tillgängliga. Logga in på [!DNL Google Ads]-redigeraren om du vill ha valfria inställningar.
>* Stöd för listgrupper är inte tillgängligt. Om du vill hantera och visa data för listgrupper loggar du in på [!DNL Google Ads]-redigeraren.

## Steg för att konfigurera [!DNL Google Ads] maximala prestandakampanjer

Du kan ställa in maximala prestandakampanjer individuellt från vyn [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) med kampanjtypen **[!UICONTROL Performance Max]**.

   Ange [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] och [!UICONTROL URL Options]. Du kan även ange [!UICONTROL Negative Keywords], ange [!UICONTROL Negative Websites] och/eller åsidosätta alternativen för [!UICONTROL Campaign Tracking].

1. Skapa resursgrupper och överför resurser för kampanjen:

   1. Klicka på **[!UICONTROL Manage Asset Groups]** längst ned i kampanjinställningarna.

   1. Ange inställningarna för den första resursgruppen och överför bilderna, logotyperna och valfria videor för resursgruppen.

      Mer information om krav och specifikationer finns i [beskrivningar av resursgruppsinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

   1. Lägg till ytterligare resursgrupper efter behov.

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Lägg till kampanjen i en hybridportfölj för optimering.
