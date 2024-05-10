---
title: Anpassade mål
description: Läs mer om anpassade mål för att definiera framgångshändelser i paket som är optimerade för det lägsta CPA eller högsta ROAS.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# Anpassade mål

Anpassade mål definierar vilka framgångshändelser en annonsörer behöver för att uppfylla sina affärsmål. Varje paket som använder optimeringsmålet[!UICONTROL Highest Return on Ad Spend (ROAS)"] eller &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; måste innehålla ett anpassat mål för att uppnå det övergripande optimeringsmålet. Du kan skapa anpassade mål som *mål* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Varje anpassat mål består av en eller flera konverteringsvärden och de relativa vikterna för dessa värden. De tillgängliga konverteringsmåtten inkluderar alla mätvärden som spåras med konverteringspixeln Adobe Advertising och via Adobe Analytics.

Anta till exempel att tre konverteringsvärden är relevanta för ett specifikt paket i en av era kampanjer:&quot;Hämta PDF&quot;, som värderas till 20 USD,&quot;Registrera via e-post&quot; som värderas till 30 USD och&quot;Bekräfta beställning&quot; som värderas till 40 USD. Om ni vill lägga vikt efter det engångs-monetära värdet av kundens åtgärd blir de relativa vikterna för måtten 1, 1,5 och 2.

En gång [skapa ett anpassat mål](#custom-goal-create)kan du [tilldela det till ett paket](/help/dsp/campaign-management/packages/package-settings.md) för rapportering och algoritmisk optimering med Adobe Sensei.

## Skapa ett anpassat mål {#custom-goal-create}

Om du vill skapa ett anpassat mål måste DSP vara länkat till ett [!DNL Search, Social, & Commerce] med samma Adobe Experience Cloud-organisations-ID, inifrån [!DNL Search, Social, & Commerce] klientinställningar. Om ditt DSP inte är länkat till en [!DNL Search, Social, & Commerce] och sedan kontakta ditt kontoteam på Adobe.

1. Logga in på [!DNL Advertising Search, Social, & Commerce] at (användare i Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) eller (alla andra användare) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Kontrollera att mätvärdena du vill inkludera i ditt mål har spårats, att de är tillgängliga i produkten och att de innehåller ett visningsnamn:

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Leta reda på måtten och se till att **[!UICONTROL Show in UI and Reports]** är aktiverat för måttet.

      >[!NOTE]
      >
      >* [!DNL Analytics] anpassade händelser följer den här namnkonventionen: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exempel: `custom_event_16_examplersid`

   1. Om måttet inte har något värde i **[!UICONTROL Display Name]** kolumn, klicka i cellen, ange visningsnamnet och klicka på **[!UICONTROL Apply].**

1. Skapa det anpassade målet som ett *mål*:

   1. Klicka på **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Klicka på i verktygsfältet ![Skapa](/help/dsp/assets/create-search-ui.png "Skapa").

   1. Ange de objektiva inställningarna, inklusive tillhörande mått och deras relativa numeriska vikter för icke-mobila enheter och mobila enheter, och spara sedan målet.

      Minst ett mått måste ha måtttypen *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] anpassade händelser följer den här namnkonventionen: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exempel: `custom_event_16_examplersid`
      >* [!DNL Analytics] dimensioner och segment är inte tillgängliga för optimering av Adobe Advertising.

      >[!TIP]
      >
      >För optimala prestanda måste de kombinerade mätvärdena i det anpassade målet (mål) innehålla minst tio konverteringar per dag. Om de inte gör det är det bästa sättet att lägga till ytterligare konverteringsmått, som produktsidor eller programstart, i målet. Se [Bästa metoder för att skapa ett anpassat mål](#custom-goal-best-practices) för riktlinjer.

I DSP för paket som använder optimeringsmålet[!UICONTROL Highest Return on Ad Spend (ROAS)"] eller &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot; finns nu målnamnet med i [!UICONTROL Custom Goals] lista. När du väljer målet som anpassat mål för ett paket visas [!UICONTROL Conversion Metric] listan innehåller alla målvärden för målet.

## Bästa metoder för att skapa ett anpassat mål {#custom-goal-best-practices}

### Anpassade mål med ett enda mått

I följande exempel visas hur du kan konfigurera mål som har ett enda konverteringsmått som mål.

#### Exempel på en kampanj med &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Optimeringsmål

Om kampanjmålet är intäkter ([!UICONTROL Highest Return on Ad Spend (ROAS)]), och intäkter från alla typer av enheter är lika viktiga för dig, och inkluderar sedan[!UICONTROL Revenue]&quot; med en icke-mobil vikt (för konverteringar från en icke-mobil enhet) på ett (1) och en mobilvikt (för konverteringar från en mobil enhet) på ett (1). Välj måtttyp *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> En mobilvikt eller en icke-mobil vikt på 1 (1) motsvarar värdet 1 (1) för varje $1 av intäkt som spåras.
>
> En konvertering på 250 USD med en icke-mobil vikt på 1 (1) rapporteras som 250 USD för konverteringar. Om konverteringsmåttet har tilldelats en icke-mobil vikt på 0,5, rapporteras konverteringen på $250 från en icke-mobil enhet som $125 i Adobe Advertising ($250 Conversion * 0,5) [!UICONTROL Non-mobile Weight] = $125).

#### Exempel på en kampanj med &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Optimeringsmål

Om kampanjmålet är den lägsta kostnaden per förvärv (CPA) och endast kräver en lyckad händelse (t.ex. &quot;Application Submit&quot;) inkluderar du det måttet och anger måtttypen som *[!UICONTROL Goal]*. Det bästa sättet är att ange både icke-mobil vikt och den mobila vikten som en (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> En mobilvikt eller icke-mobil vikt på 1 (1) motsvarar värdet 1 (1) för varje konvertering som spåras. Om till exempel 10 programsändningskonverteringar spåras rapporteras 10 programsändningskonverteringar. Om konverteringsmåttet tilldelas en icke-mobil vikt på 0,5 rapporteras däremot de 10 icke-mobila konverteringarna som fem (5) i Adobe Advertising (10 konverteringar * 0,5) [!UICONTROL Non-mobile Weight] = 5).

### Anpassade mål med flera mätvärden

Det finns två scenarier där du kan använda flera mätvärden i ett anpassat mål:

* Kampanjmålet har flera lyckade händelser. Du kanske till exempel annonserar för mer än en åtgärd på plats (PDF Download, Contact Us och Email Sign up), och alla åtgärder bidrar till ditt mål med CPA. Om målet innehåller tre separata mätvärden, där varje mätvärde har en (1) icke-mobil- och mobilvikt, ska [!DNL Adobe Sensei] algoritmen behandlar alla mätvärden och användarenhetstyper lika viktigt. Om de olika måtten och enhetstyperna har olika kostnader eller betydelse justerar du deras relativa vikt därefter.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Det anpassade målets konverteringsmått för en enda konvertering är inte att uppnå det minimum på 10 konverteringar per dag som krävs för optimerade prestanda. Detta kan bero på minimal daglig paketkostnad eller ett begränsat antal naturliga konverteringar. Genom att lägga till ytterligare stödmått till det anpassade målet kan du uppnå tröskelvärdet på 10 konverteringar per dag. Tio stödhändelser kan hjälpa ett paket att uppnå tröskelvärdet 10/dag, även när varje vikt är under 1 (1). Men du kanske inte behöver lägga till så många händelser.

  När du lägger till stödmått till ett anpassat mål ska du väga dem efter deras relativa betydelse för händelsen om det ska lyckas och tänka på mängden datapunkter. På så sätt kan Adobe Sensei-algoritmen balansera flera mätvärden och optimera mot ditt mål.

  Följande exempelmål innehåller tre mätvärden, var och en med olika icke-mobilvikt: Application Submit = 1, Application Start = 0.1 och Advertiser Landing Page = 0.01. Det innebär att varje konvertering av Application Submit från icke-mobila enheter har samma värde för ditt företag som i genomsnitt 10 konverteringar av Application Start från icke-mobila enheter och 100 konverteringar av Advertiser Landing Page från icke-mobila enheter.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Om du i stället vägde besök för landningssidor lika mycket som i Ansökningsomgångar, kan det naturligt högre antalet besök på landningssidor överbelasta ditt mål och skevhet för besöken på landningssidor.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
