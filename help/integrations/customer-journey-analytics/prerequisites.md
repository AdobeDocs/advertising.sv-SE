---
title: Krav för att integrera Adobe Advertising med Customer Journey Analytics
description: Krav för att integrera Adobe Advertising med Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: ba23ab97c916f829cf9d640669423dd8e72949c0
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Krav för att integrera Adobe Advertising med Customer Journey Analytics

*Annonsörer med Advertising DSP och[!DNL Advertising Search, Social, & Commerce]*

Läs följande information innan du integrerar Adobe Advertising med Adobe Customer Journey Analytics.

## Krav för rapportering av Adobe Advertising-data i Customer Journey Analytics

* Annonsörer med både [!DNL Analytics for Advertising] och Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [Alla andra krav för  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Annonsörer med Customer Journey Analytics men inte [!DNL Analytics for Advertising]:

   * Adobe Experience Platform Web SDK-bibliotek: `alloy.js`

     [!DNL Org ID] som används för Web SDK och för Adobe Advertising annonserarkonto måste vara samma. Du hittar detta ID på fliken [Sammanfattning i Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

     ![Sammanfattningsskärm för Experience Cloud-felsökning](/help/integrations/assets/a4adc-debugger-summary.png)

     Du behöver support från din webbplatsadministratör för Experience Platform för att skapa ett Experience Platform datastream- och XDM-schema.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     Du behöver stöd från din interna webbanalytiker för att konfigurera en anslutning till datauppsättningen och konfigurera rapportering.

>[!TIP]
>
>Använd den senaste versionen av varje bibliotek för att förbättra datakvaliteten.

>[!MORELIKETHIS]
>
>* [Översikt](overview.md)
>* (Adobe Analytics-användare) [Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
