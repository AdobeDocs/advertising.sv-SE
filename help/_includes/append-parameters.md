---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Lägg till parameterfält i konto- och kampanjinställningar

**[!UICONTROL Append Parameters]:** (Valfritt) Eventuella ytterligare spårningsparametrar som ska läggas till i bas-URL:erna.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Parametrar för annonseringstillägg inkluderas som standard på kontonivå och kampanjnivå, men du kan åsidosätta båda.

Du kan använda vilken statisk textsträng som helst, inklusive spårningsparametrar från tredje part, eller någon av [spårningsparametrar](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), som infogar ett lämpligt datavärde i bas-URL:en.

Avgränsa flera parametrar med kommatecken eller et-tecken (&amp;). Kapslade hakparenteser stöds inte.

**Anteckningar:**

* Ändringar i tilläggsparametrar styrs inte av [!UICONTROL Auto Upload] alternativ. Om du ändrar tilläggsparametrarna för befintliga bas-URL:er genereras inte nya URL:er automatiskt. Lägg till de nya parametrarna genom att hämta en kalkylbladsfil för kontot eller kampanjen, uppdatera [!UICONTROL Base URL/Final URL] och sedan överföra och bokföra kalkylbladet.

* (Annonsnätverk med parallell spårning) Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

* (Annonsörer med integrering mellan Adobe Advertising och Adobe Analytics) Att inkludera en AMO ID-parameter för att skicka data från sök, sociala och kommersiella aktiviteter till [!DNL Analytics], se [och nätverksspecifika format](/help/integrations/analytics/ids.md#amo-id-formats). Du behöver inte lägga till parametern manuellt för [!DNL Google Ads] och [!DNL Microsoft Advertising] konton med en AMO ID-implementering på serversidan.
