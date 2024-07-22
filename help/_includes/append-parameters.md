---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Lägg till parameterfält i konto- och kampanjinställningar

**[!UICONTROL Append Parameters]:** (Valfritt) Eventuella ytterligare spårningsparametrar som ska läggas till i bas-URL:erna.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Parametrar för annonseringstillägg inkluderas som standard på kontonivå och kampanjnivå, men du kan åsidosätta båda.

Du kan använda valfri statisk textsträng, inklusive spårningsparametrar från tredje part, eller någon av de [spårningsparametrar](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md) som stöds, som infogar ett lämpligt datavärde i bas-URL:en.

Avgränsa flera parametrar med kommatecken eller et-tecken (&amp;). Kapslade hakparenteser stöds inte.

**Anteckningar:**

* Ändringar av tilläggsparametrar styrs inte av alternativet [!UICONTROL Auto Upload]. Om du ändrar tilläggsparametrarna för befintliga bas-URL:er genereras inte nya URL:er automatiskt. Lägg till de nya parametrarna genom att hämta en kalkylbladsfil för kontot eller kampanjen, uppdatera fälten [!UICONTROL Base URL/Final URL] och sedan överföra och publicera kalkylbladet.

* (Annonsnätverk med parallell spårning) Undvik att använda makron, som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.

* (Annonsörer med integrering mellan Adobe Advertising och Adobe Analytics) Om du vill inkludera en AMO ID-parameter för att skicka data från Search, Social och Commerce till [!DNL Analytics] läser du [annons nätverksspecifika format](/help/integrations/analytics/ids.md#amo-id-formats). Det är inte nödvändigt att manuellt lägga till parametern för [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton med en AMO ID-implementering på serversidan.
