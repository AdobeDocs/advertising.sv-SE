---
title: Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och proppar
description: Konfigurera anpassade händelsemätningar med [!DNL eVar]- och [!DNL prop]data på -nivå.
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: a0d5bc1791f5d05e2cbdeab58e1943f4d494b53f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och [!DNL props]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Ni kan använda framgångsstatistik för att optimera DSP och sök-, sociala och handelskampanjer baserade på Adobe Analytics webbplatsdata som bäst passar ert varumärkes mål. Du kan konfigurera anpassade händelsemätningar för framgångshändelser baserat på dina befintliga [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) och [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) med kanttning [!DNL eVar]- och [!DNL prop]data på -nivå till en händelse. Övriga [!DNL Analytics] Mätvärden, inklusive standardvärden, anpassade och reserverade konverteringsvärden och trafikvärden, är automatiskt tillgängliga i DSP och sökningar, sociala medier och handel.

![Exempel på användning](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exempel på användning")

De flesta av följande åtgärder måste utföras av en [!DNL Analytics] administratör eller annan användare. Om du behöver hjälp kan du kontakta (DSP användare) den DSP tekniska supportteamet på `adcloud_support@adobe.com` eller (sök-, sociala och handelsmässiga användare) ditt kontoteam för Adobe.

1. I [!DNL Analytics], [skapa en platshållarhändelse](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Använd följande ytterligare parametrar:

   **Typ:** `Counter`

   **Polaritet:**  antingen `Up is Good` eller `Up is Bad`

   **Synlighet:** `Visible Everywhere`

   **Unik händelseinspelning:** `Always Record Event`

   **Deltagande:** `Enabled`

   Ni behöver inte implementera det nya evenemanget på ert varumärkes webbplats eftersom det använder befintliga data som redan har samlats in.

1. Skapa och validera en bearbetningsregel i [!DNL Analytics]:

   >[!NOTE]
   >
   >Endast [!DNL Analytics] kontoadministratörer kan skapa bearbetningsregler såvida de inte har gett tillstånd till icke-administratörer.

   1. [Skapa en bearbetningsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), med följande konfiguration:

      * För villkoret som måste uppfyllas anger du det som krävs [!DNL eVars] eller [!DNL props].

        Du kan konfigurera ytterligare granularitetsnivåer efter behov för att säkerställa att de mest korrekta händelserna skapas.

        >[!TIP]
        >
        >Det bästa sättet är att bara använda en [!DNL eVar] eller [!DNL prop].

      * För åtgärden väljer du **Ange händelse** och välj platshållarhändelsen.

   1. I [!DNL Analytics] [!DNL Analysis Workspace], [skapa ett projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) och dra in den nya händelsen i en frihandstabell för att säkerställa att data fylls i för [!DNL eVar] eller [!DNL prop] mätvärden.

1. Kontakta kontoteamet på Adobe för att synkronisera det nya mätvärdet med Adobe Advertising.

När mätvärdena är tillgängliga kan du använda dem för att skapa ett mål som du sedan kan tilldela till en portfölj för sökning, sociala medier och handel eller använda som en [anpassat mål](/help/dsp/optimization/custom-goal.md) för ett DSP.

Mer information om hur du skapar mål finns i kapitlet om optimeringsguiden,&quot;Mål&quot;, som du når via Sök, Socialt och Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
