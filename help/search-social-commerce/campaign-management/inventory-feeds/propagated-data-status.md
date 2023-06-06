---
title: Status för data som genererats från feeds
description: Lär dig mer om statusvärdena för data som genereras från lagerdataflöden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status för data som genererats från feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

Varje komponent kan ha en av följande statusvärden:

* *[!UICONTROL New]:* Komponenten finns inte i annonsnätverket och har inte publicerats i annonsnätverket, och du kan fortfarande redigera dess inställningar om det behövs genom att klicka på komponentnamnet. När du är redo att publicera data klickar du på **[!UICONTROL Post to SE]** och ange vilka data som ska skickas.

* *[!UICONTROL Posted]:* (Endast kampanjer och annonsgrupper) Kampanjen eller annonsgruppen publicerades delvis i annonsnätverket, men vissa komponenter bokfördes inte på grund av fel. Valideringsstatusen för varje nyckelord och annons visar vilken information som behöver korrigeras. Om det behövs kan du redigera komponentens inställningar genom att klicka på komponentnamnet.

* *[!UICONTROL Active]:* Komponenten är redan aktiv i annonsnätverket och du kan inte redigera dess inställningar här. Aktiva komponenter kan innehålla underkomponenter som [!UICONTROL New], som kan bokföras om uppgifterna är giltiga.

* *[!UICONTROL Paused]:* Komponenten är redan pausad i annonsnätverket och du kan inte redigera dess inställningar här. Pausade komponenter kan innehålla underkomponenter som [!UICONTROL New], som kan bokföras om uppgifterna är giltiga.

* *[!UICONTROL Deleted]:* Komponenten har redan tagits bort i annonsnätverket och du kan inte redigera dess inställningar här. Borttagna komponenter kan innehålla underkomponenter som [!UICONTROL New], som kan bokföras om uppgifterna är giltiga.

>[!MORELIKETHIS]
>
>* [Om lagerflöden](inventory-feeds-about.md)
>* [Visa data som genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Posta kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)

