---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Fältet Enheter i inställningarna för GL- och MS-kampanj och annonsgrupp

**[!UICONTROL Devices]:** (Valfritt, inte tillgängligt för [!DNL Google Ads] prestandamängdskampanjer eller [!DNL Microsoft Advertising] video- eller CTV-videoannonser) Konfigurera anbudsjusteringar för olika enhetstyper, som procentandelar av nyckelordsnivåanbudet. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för smarttelefoner är 50 %, är smarttelefonanbudet 1,50 USD. Som standard anges inga värden (budjustering=0) och alla enheter bjuds vid nyckelordsnivån bud.

För [!DNL Google Ads] kan giltiga procentsatser innehålla -100 för smarttelefoner och surfplattor (men inte för att lämna anbud för enhetstypen) och från -90 till 900 för alla enhetstyper.

Giltiga procentsatser för [!DNL Microsoft Advertising] kan vara:

* Smarttelefoner och surfplattor: -100 (köp inte för enhetstypen) och från -90 till 900
* Stationär dator: från 0 till 900

>[!NOTE]
>* Inställningarna på annonsgruppnivå åsidosätter inställningarna på kampanjnivå. Om du däremot utesluter en enhet på kampanjnivå kan du inte åsidosätta undantaget på annonsgruppsnivå.
>* Om du tilldelar den här kampanjen till en standardoptimerad portfölj avgör Search, Social och Commerce automatiskt vilket nyckelordserbjudande som ska hjälpa portföljen att uppnå sitt mål. Annonsnätverket justerar sedan budet enligt inställningarna för olika enhetstyper.
>* (För alla kampanjer/annonsgrupper utom för [!DNL Microsoft Advertising] annonsgrupper i målgruppsnätverket) Om du tilldelar den här kampanjen till en optimerad standardportfölj som är konfigurerad till [!UICONTROL Auto-optimize Bid Adjustment Values] ändras de angivna enhetsprisjusteringarna på annonsgruppsnivå, så länge det ideala värde som beräknas ligger inom de lägsta och högsta värden som anges i portföljinställningarna och annonsgruppen inte utesluter budgivning för enhetstypen.
