---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# Fält för automatisk överföring i konto- och kampanjinställningar

**[!UICONTROL Auto Upload]:** (Endast för synkroniserade kampanjer med [!UICONTROL EF Redirect]) Överför automatiskt följande till annonsnätverket nästa gång Search, Social och Commerce synkroniseras med det: (a) Parametrar för sökning, social och Commerce-spårning för spårningsmallar och samma parametrar läggs till i de slutliga URL:erna eller (b) nya mål-URL:er som är inbäddade med kod för sökning, social och Commerce-spårning. För annonsörer med en [Adobe Advertising-Adobe Analytics-integrering](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=sv-SE) och en AMO ID (s_kwcid)-konfiguration på serversidan, innehåller överföringen även [AMO ID-parametrar](/help/integrations/analytics/ids.md#amo-id) för dina [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar. Du kan åsidosätta inställningen på kontonivå på kampanjnivå.

**Obs!** URL:er för spårning uppdateras dagligen endast för entiteter som inte är synkroniserade (det vill säga nya entiteter som lagts till och befintliga entiteter vars egenskaper har ändrats). Om du ändrar den här inställningen från inaktiverad till aktiverad för en befintlig annonserare/konto/kampanj uppdateras därför inte spårnings-URL:er för befintliga enheter som redan är synkroniserade. Om du vill lägga till spårning i URL:er för befintliga, synkroniserade enheter kontaktar du kontoteamet på Adobe och begär en manuell synkroniseringsprocess som utförs en gång. Den automatiska överföringsprocessen hanterar framtida ändringar.
