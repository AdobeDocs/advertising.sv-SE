---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Fält för automatisk överföring i konto- och kampanjinställningar

**[!UICONTROL Auto Upload]:** (För synkroniserade kampanjer med [!UICONTROL EF Redirect] endast) Överför automatiskt följande till annonsnätverket nästa gång sökningen, sociala medier och handel synkroniseras med det: (a) parametrar för sökning, sociala medier och handelsuppföljning för spårningsmallar och samma parametrar som läggs till i de slutliga URL:erna eller (b) nya mål-URL:er som är inbäddade med kod för sökning, sociala nätverk och handel. För annonsörer med en [Integration mellan Adobe Advertising och Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) och en konfiguration av AMO ID (s_kwcid) på serversidan, innehåller överföringen även AMO ID-parametrar för dina [!DNL Google Ads] och [!DNL Microsoft Advertising] konton. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar. Du kan åsidosätta inställningen på kontonivå på kampanjnivå.

**Obs!** Spårnings-URL:er uppdateras dagligen endast för entiteter som är osynkroniserade (det vill säga nya entiteter som lagts till och befintliga entiteter vars egenskaper har ändrats). Om du ändrar den här inställningen från inaktiverad till aktiverad för en befintlig annonserare/konto/kampanj uppdateras därför inte spårnings-URL:er för befintliga enheter som redan är synkroniserade. Om du vill lägga till spårning i URL:er för befintliga, synkroniserade enheter kontaktar du kontoteamet på Adobe och begär en manuell synkroniseringsprocess som utförs en gång. Den automatiska överföringsprocessen hanterar framtida ändringar.
