---
title: Om meddelanden
description: Lär dig mer om meddelanden, inklusive olika typer och kategorier.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Om meddelanden

*Betafunktion*

Du kan konfigurera dina meddelandeinställningar så att du kan prenumerera på eller avbryta prenumerationen på olika typer av aviseringar. Du kan visa dina meddelanden på något av följande sätt:

* Från [!UICONTROL Notifications] som finns på huvudmenyn på ![Meddelanden](/help/search-social-commerce/assets/notifications-panel.png "Meddelanden").

* Från [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Från en [!UICONTROL Notification Center] webbprogram, som öppnas [!UICONTROL Notification Center] i ett separat fönster utanför Search, Social och Commerce.

  Programmet läses in snabbare än den vanliga webbläsarversionen och uppdateras automatiskt. Du kan installera programmet och hantera det med webbläsarens apphanterare.

* Från push-meddelanden till webbläsaren.

  När du aktiverar push-meddelanden visas de i enlighet med webbläsarens meddelandekonventioner.

Du kan visa dina meddelanden, markera meddelanden som lästa eller olästa samt ta bort meddelanden.

## Meddelandetyper

* **[!UICONTROL Notices]**: Versionsinformation, information om driftstopp och annan ändringshantering.

* **[!UICONTROL Recommendations]**: Möjligheter som identifierats för att förbättra prestanda, implementera bästa praxis osv.

* **[!UICONTROL Warnings]**: Problem som kräver åtgärd men som inte är viktiga för optimering eller hantering.

* **[!UICONTROL Issues]**: Kritiska problem som kräver omedelbar åtgärd. Felmeddelanden för kontoauktorisering ingår.

## Meddelandekategorier

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: Meddelanden om att [operation](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) har slutförts eller misslyckats.

   * **[!UICONTROL Manager Account Missing]**: Meddelanden om att autentiseringsuppgifterna för en sökning, sociala medier och handel saknas [annonsera konto för nätverkshanterare](/help/search-social-commerce/admin/manager-accounts.md), som krävs för korrekt konfiguration av kritiska funktioner.

   * **[!UICONTROL UI Actions]**: Meddelanden om att de jobb som utförs i bakgrunden har slutförts eller misslyckats. Jobbtyperna omfattar [bladarbeten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), massredigera jobb i datatabellen eller med verktygsfältet, enhetstilldelningsjobb eller andra åtgärder i användargränssnittet (t.ex. synkronisering med annonsnätverk, inklistring av rader eller namnbyte av enheter). Enhetstilldelningar omfattar tilldelning eller frigörande av en [etikettklassificeringsvärde](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) till alla enheter, tilldela en kampanj till en portfölj och tilldela eller ta bort en begränsning till en portfölj.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: Används för en sluten betaversion

      * **[!UICONTROL File Upload to Cloud Storage]**: Används för en sluten betaversion

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: Meddelanden om att det inte gick att komma åt en [annonsnätverkskonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) på grund av ogiltiga autentiseringsuppgifter eller en ogiltig eller utgången autentiseringstoken.

      * **[!UICONTROL Account Missing]**: Meddelanden om att autentiseringsuppgifterna för en sökning, sociala medier och handel saknas [annonsnätverkskonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**: Meddelanden om att det inte gick att synkronisera med en [annonsera konto för nätverkshanterare](/help/search-social-commerce/admin/manager-accounts.md) på grund av ogiltiga autentiseringsuppgifter eller en ogiltig eller utgången autentiseringstoken.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Meddelanden om att [en [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) har slutförts eller misslyckats.

   * **[!UICONTROL Custom Alerts]**: Meddelanden om att [varningsinstanser](/help/search-social-commerce/alerts/alert-about.md) har utlösts för en aviseringsmall.

   * **[!UICONTROL Reports]**: Meddelanden om att [anpassad eller schemalagd rapport](/help/search-social-commerce/reports/report-about.md) har slutförts eller misslyckats.

   * **[!UICONTROL Spreadsheet Feeds]**: Meddelanden om att [kalkylbladsmatning](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) har slutförts eller misslyckats.

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [Visa dina meddelanden](notification-view.md)
>* [Markera ett meddelande som läst eller oläst](notification-mark-read-unread.md)
>* [Ta bort ett meddelande](notification-delete.md)
>* [Redigera meddelandeinställningarna](notification-edit.md)
>* [Aktivera och inaktivera push-meddelanden från [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installera och avinstallera [!UICONTROL Notification Center] webbprogram](notification-app-install-uninstall.md)
