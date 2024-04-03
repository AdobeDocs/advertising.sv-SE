---
title: Om anpassade mål
description: Läs mer om anpassade mål för att definiera framgångshändelser i paket som är optimerade för det lägsta CPA eller högsta ROAS.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Om anpassade mål

Anpassade mål definierar vilka framgångshändelser en annonsörer behöver för att uppfylla sina affärsmål. Varje paket som använder optimeringsmålet[!UICONTROL Highest Return on Ad Spend (ROAS)"] eller &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; måste innehålla ett anpassat mål som hjälper till att uppnå det övergripande optimeringsmålet. Du kan skapa anpassade mål som *mål* in [!DNL Advertising Search, Social, & Commerce].

![anpassade mål](/help/dsp/assets/objective-goals.png)

Varje anpassat mål består av en eller flera konverteringsvärden och de relativa vikterna för dessa värden. De tillgängliga konverteringsmåtten inkluderar alla mätvärden som spåras med konverteringspixeln Adobe Advertising och via Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensioner och segment är inte tillgängliga för optimering av Adobe Advertising.
>* Om du vill använda Analytics-händelser i DSP samarbetar du med ditt kontoteam på Adobe för att konfigurera en integrering på annonsörnivå.
>* [!DNL Analytics] anpassade händelser följer den här namnkonventionen: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exempel: `custom_event_16_examplersid`

Anta till exempel att tre konverteringsvärden är relevanta för ett specifikt paket i en av era kampanjer:&quot;Hämta PDF&quot;, som värderas till 20 USD,&quot;Registrera via e-post&quot; som värderas till 30 USD och&quot;Bekräfta beställning&quot; som värderas till 40 USD. Om du vill ge tyngd i enlighet med det engångs-monetära värdet av kundåtgärden, blir egenskapernas relativa vikter 1, 2 och 1,5.

Se [bästa sättet att skapa anpassade mål](custom-goal-best-practices.md) för tips om hur du konfigurerar dina anpassade mål.

En gång [skapa ett anpassat mål](custom-goal-create.md)kan du [tilldela det till ett paket](/help/dsp/campaign-management/packages/package-settings.md) för rapportering och algoritmisk optimering med Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Skapa ett anpassat mål](custom-goal-create.md)
>* [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
