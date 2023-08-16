---
title: Spårningsparametern för AMO-ID (s_kwcid)
description: Läs mer om spårningsparametern som används för att dela data från Adobe Advertising med Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Spårningsparametern för AMO-ID (s_kwcid)

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising delar data om era kampanjer med Adobe Analytics med hjälp av tilläggsparametern AMO ID, som också kallas `s_kwcid` -parameter, som består av annonskanaler och annonsspecifika element.

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) Funktionen för infogning på serversidan implementeras.

   * DSP: Pixelservern lägger automatiskt till parametern s_kwcid i landningssidans suffix när en användare tittar på en displayannons med pixeln Adobe Advertising.

   * Kunder inom sökning, sociala medier och handel:

      * För [!DNL Google Ads] och [!DNL Microsoft® Advertising] konton med [!UICONTROL Auto Upload] om inställningen är aktiverad för kontot eller kampanjen lägger pixelservern automatiskt till parametern s_kwcid i landningssidans suffix när en slutanvändare klickar på en annons med Adobe Advertising.

      * för andra annonsnätverk, eller [!DNL Google Ads] och [!DNL Microsoft® Advertising] konton med [!UICONTROL Auto Upload] om inställningen är inaktiverad lägger du till parametern manuellt i tilläggsparametrarna på kontonivån, som läggs till i bas-URL:erna.

* Infoga-funktionen på serversidan är inte implementerad:

   * DSP kunder:

      * För [!DNL Flashtalking] annonstaggar, infoga ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * För [!DNL Google Campaign Manager 360] annonstaggar, infoga ytterligare makron manuellt per &quot;[Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Kunder inom sökning, sociala medier och handel:

      * För ([!DNL Google Ads] och [!DNL Microsoft® Advertising]), lägger du till AMO ID-parametern manuellt i landningssidans suffix.

      * För annonser i alla andra annonsnätverk lägger du manuellt till parametern AMO ID i dina tilläggsparametrar på kontonivå, som lägger till den i dina bas-URL:er.

Om du vill implementera infogningsfunktionen på serversidan eller fastställa det bästa alternativet för din verksamhet kan du tala med ditt Adobe-kontoteam.

AMO ID-formaten för DSP och sökning, sociala medier och handel finns i &quot;[Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Sökning, sociala medier och handel) [Hantera och nätverkskonton](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Sökning, sociala medier och handel) [Inställningar för Baidu-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Sökning, sociala medier och handel) [Kampanjinställningar för Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Sökning, sociala medier och handel) [Inställningar för Microsoft® Advertising-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Sökning, sociala medier och handel) [Yahoo! Inställningar för japanska annonskampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Sökning, sociala medier och handel) [Inställningar för Yandex-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
