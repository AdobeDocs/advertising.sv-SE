---
title: Spårningsparametern för AMO-ID (s_kwcid)
description: Läs mer om spårningsparametern som används för att dela data från Adobe Advertising med Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Spårningsparametern för AMO-ID (s_kwcid)

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising delar data om era kampanjer med Adobe Analytics med hjälp av tilläggsparametern AMO ID, som också kallas `s_kwcid` -parameter, som består av annonskanaler och annonsspecifika element.

<!-- add everything below to IDs page -->

Parametern läggs till i dina spårnings-URL:er på något av följande sätt:

* (Rekommenderas) Funktionen för infogning på serversidan implementeras.

  För [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] inställning aktiverad för kontot eller kampanjen lägger pixelservern automatiskt till AMO ID-parametern i landningssidans suffix när en slutanvändare klickar på en annons <!-- click a search ad or views a display ad --> med Adobe Advertising-pixeln.

  för andra annonsnätverk, eller [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med [!UICONTROL Auto Upload] om inställningen är inaktiverad lägger du manuellt till parametern AMO ID i dina tilläggsparametrar på kontonivå, som lägger till den i dina bas-URL:er.

* <!-- (Search, Social, & Commerce only) -->Serversidesinfogningsfunktionen är inte implementerad och du måste lägga till AMO ID-parametern manuellt i ([!DNL Google Ads] och [!DNL Microsoft Advertising]) landningssidessuffix eller (andra annonsnätverk) tilläggsparametrar på kontonivå.

Om du vill implementera infogningsfunktionen på serversidan eller fastställa det bästa alternativet för din verksamhet kan du tala med ditt Adobe-kontoteam.

AMO ID-formaten för DSP och sökning, sociala medier och handel finns i &quot;[Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Översikt [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe Advertising-ID som används av [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Hantera och nätverkskonton](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Inställningar för Baidu-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampanjinställningar för Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Inställningar för Microsoft Advertising-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Inställningar för japanska annonskampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Inställningar för Yandex-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
