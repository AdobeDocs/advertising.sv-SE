---
title: Status för data som genererats från feeds
description: Lär dig mer om statusvärdena för data som genereras från lagerdataflöden.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status för data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Varje komponent kan ha en av följande statusvärden:

* *[!UICONTROL New]:* Komponenten finns inte i annonsnätverket och har inte publicerats i annonsnätverket, och du kan fortfarande redigera dess inställningar om det behövs genom att klicka på komponentnamnet. När du är redo att publicera data klickar du på **[!UICONTROL Post to SE]** och anger de data som ska skickas.

* *[!UICONTROL Posted]:* (Endast kampanjer och annonsgrupper) Kampanjen eller annonsgruppen publicerades delvis i annonsnätverket, men vissa komponenter bokfördes inte på grund av fel. Valideringsstatusen för varje nyckelord och annons visar vilken information som behöver korrigeras. Om det behövs kan du redigera komponentens inställningar genom att klicka på komponentens namn.

* *[!UICONTROL Active]:* Komponenten är redan aktiv i annonsnätverket och du kan inte redigera dess inställningar här. Aktiva komponenter kan innehålla underkomponenter som är [!UICONTROL New], som kan bokföras om data är giltiga.

* *[!UICONTROL Paused]:* Komponenten är redan pausad i annonsnätverket och du kan inte redigera dess inställningar här. Pausade komponenter kan innehålla underkomponenter som är [!UICONTROL New], som kan bokföras om data är giltiga.

* *[!UICONTROL Deleted]:* Komponenten har redan tagits bort i annonsnätverket, och du kan inte redigera dess inställningar här. Borttagna komponenter kan innehålla underkomponenter som är [!UICONTROL New], som kan bokföras om data är giltiga.

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](inventory-feeds-about.md)
>* [Visa data som har genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
