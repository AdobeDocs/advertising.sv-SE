---
title: Bästa metoder för att skapa ett anpassat mål
description: Lär dig de bästa sätten att skapa anpassade mål för att definiera framgångsrika händelser.
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Bästa metoder för att skapa ett anpassat mål

## Anpassade mål med en enda egenskap

I följande exempel visas hur du kan konfigurera mål som har ett enda konverteringsmått som mål.

### Exempel på en kampanj med &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Optimeringsmål

Om kampanjmålet är intäkter ([!UICONTROL Highest Return on Ad Spend (ROAS)]), kommer ditt anpassade mål (mål) att innehålla[!UICONTROL Revenue]&quot; med en vikt på 1 (1).

![exempel på ett anpassat ROAS-mål med ett enda konverteringsmått](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] av en är lika med ett värde på en för varje $1 av intäkt som spåras.
>
> En konvertering på 250 USD med vikten 1 rapporteras till exempel som 250 USD. Om konverteringsmåttet har tilldelats vikten 0,5, rapporteras konverteringen på $250 som $125 i Adobe Advertising ($250 Conversion * 0,5) [!UICONTROL Property Weight] = $125).

### Exempel på en kampanj med &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Optimeringsmål

Om kampanjmålet är den lägsta kostnaden per förvärv (CPA) och endast kräver en lyckad händelse, inkluderar du det måttet (i följande exempel&quot;Application Submit&quot;). Det bästa sättet är att ange vikten som ett (1).

![exempel på ett anpassat CPA-mål med ett enda konverteringsmått](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] av ett är lika med värdet ett för varje konvertering som spåras.
>
> Om till exempel 10 programsändningskonverteringar spåras rapporteras 10 programsändningskonverteringar.  Om konverteringsmåttet har tilldelats vikten 0,5, rapporteras 10 konverteringar som fem (5) i Adobe Advertising (10 konverteringar * 0,5) [!UICONTROL Property Weight] = 5).

## Anpassade mål med flera egenskaper

Det finns två scenarier där du kan använda flera egenskaper i ett anpassat mål:

* Kampanjmålet har flera lyckade händelser. Du kanske till exempel gör reklam för mer än en åtgärd på plats, och alla är kopplade till ditt mål för CPA. Följande exempelmål innehåller tre separata egenskaper (PDF Download, Contact Us och Email Sign up), var och en med vikten 1 (1), som anger [!DNL Adobe Sensei] att var och en av egenskaperna har samma betydelse. Om du inkluderar egenskaper med varierande kostnader eller prioritet kan du justera deras relativa vikt därefter.

  ![exempel på ett anpassat mål med flera egenskaper](/help/dsp/assets/custom-goal-multiple-properties.png)

* Det anpassade målets konverteringsmått för en enda konvertering är inte att uppnå det minimum på 10 konverteringar per dag som krävs för optimerade prestanda. Detta kan bero på minimal daglig paketkostnad eller ett begränsat antal naturliga konverteringar. Genom att lägga till ytterligare stödegenskaper till det anpassade målet kan du uppnå tröskelvärdet på 10 konverteringar per dag. Tio stödhändelser kan hjälpa ett paket att uppnå tröskelvärdet 10/dag, även när varje vikt är under 1 (1). Men du kanske inte behöver lägga till så många händelser.

  När du lägger till stödegenskaper till ett anpassat mål ska du väga dem efter deras relativa betydelse för händelsen om det ska lyckas och tänka på mängden datapunkter. På så sätt kan Adobe Sensei-algoritmen balansera flera egenskaper och optimera mot ditt mål.

  Följande exempelmål innehåller tre egenskaper, var och en med olika vikt: Application Submit = 1, Application Start = 0.1 och Advertiser Landing Page = 0.01. Det innebär att varje konvertering av Application Submit har samma värde som i genomsnitt 10 konverteringar av Application Start och 100 konverteringar av Advertiser Landing Page.

  ![exempel på ett anpassat mål med flera egenskaper](/help/dsp/assets/custom-goal-multiple-properties2.png)

  Om du i stället vägde besök för landningssidor lika mycket som i ansökningsformulär, kan det naturligt högre antalet besök på landningssidor överbelasta ditt mål och skevhet för besöken på landningssidor.<!--reword-->

>[!MORELIKETHIS]
>
>* [Om anpassade mål](custom-goal-about.md)
>* [Skapa ett anpassat mål](custom-goal-create.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
