---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---
# Fält för automatisk överföring i konto- och kampanjinställningar

**[!UICONTROL Auto Upload]:** (För synkroniserade kampanjer med [!UICONTROL EF Redirect] endast) Överför automatiskt följande till annonsnätverket nästa gång sökningen, sociala medier och handel synkroniseras med det: (a) Spårningsparametrar för sökning, sociala medier och handel för spårningsmallar och samma parametrar som har lagts till i de slutliga URL:erna eller (b) nya mål-URL:er som är inbäddade med koden för sökning, sociala medier och handel. För annonsörer med en [Integrering mellan Adobe Advertising och Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) och en s_kwcid-konfiguration på serversidan, innehåller överföringen också s_kwcid-parametrar för dina [!DNL Google Ads] och [!DNL Microsoft Advertising] konton. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar. Du kan åsidosätta inställningen på kontonivå på kampanjnivå.

**Obs!** Spårnings-URL:er uppdateras dagligen endast för entiteter som är osynkroniserade (det vill säga nya entiteter som lagts till och befintliga entiteter vars egenskaper har ändrats). Om du ändrar den här inställningen från inaktiverad till aktiverad för en befintlig annonserare/konto/kampanj uppdateras därför inte spårnings-URL:er för befintliga enheter som redan är synkroniserade. Om du vill lägga till spårning i URL:er för befintliga, synkroniserade enheter kontaktar du kontoteamet på Adobe och begär en manuell synkroniseringsprocess som utförs en gång. Den automatiska överföringsprocessen hanterar framtida ändringar.
