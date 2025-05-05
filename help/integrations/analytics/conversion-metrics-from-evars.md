---
title: Skapa konverteringsvärden från Adobe Analytics [!DNL eVars] och proffs
description: Konfigurera anpassade händelsemått för lyckade åtgärder med data på  [!DNL eVar]- och [!DNL prop]-nivå.
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 91e8435ff00feca804dfa2f4c323f88ee31813ab
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Skapa konverteringsmått från Adobe Analytics [!DNL eVars] och [!DNL props]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Ni kan använda framgångsstatistik för att optimera DSP och sök-, sociala och Commerce-kampanjer baserat på Adobe Analytics webbplatsdata som bäst passar ert varumärkes mål. Du kan konfigurera anpassade händelsemått baserat på dina befintliga [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=sv-SE) och [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=sv-SE) genom att samla data på [!DNL eVar]- och [!DNL prop]-nivå i en händelse. Andra [!DNL Analytics]-mått, inklusive standardvärden, anpassade värden och reserverade konverteringsvärden och trafikvärden, är automatiskt tillgängliga i DSP och sökningar, sociala medier och Commerce.

![Exempel på användning](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exempel på användning")

De flesta av följande åtgärder måste utföras av en [!DNL Analytics]-administratör eller annan användare. Om du behöver hjälp kan du kontakta (DSP användare) det DSP tekniska supportteamet på `adcloud_support@adobe.com` eller (användare av Search, Social och Commerce) ditt kontoteam på Adobe.

1. I [!DNL Analytics] [skapar du en platshållarhändelse ](https://experienceleague.adobe.com/sv/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Använd följande ytterligare parametrar:

   **Typ:** `Counter`

   **Polaritet:** antingen `Up is Good` eller `Up is Bad`

   **Synlighet:** `Visible Everywhere`

   **Unik händelseinspelning:** `Always Record Event`

   **Deltagande:** `Enabled`

   Ni behöver inte implementera det nya evenemanget på ert varumärkes webbplats eftersom det använder befintliga data som redan har samlats in.

1. Skapa och validera en bearbetningsregel i [!DNL Analytics]:

   >[!NOTE]
   >
   >Endast kontoadministratörer för [!DNL Analytics] kan skapa bearbetningsregler om de inte har gett behörighet till icke-administratörer.

   1. [Skapa en bearbetningsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=sv-SE) med följande konfiguration:

      * Ange [!DNL eVars] eller [!DNL props] som krävs för villkoret som måste uppfyllas.

        Du kan konfigurera ytterligare granularitetsnivåer efter behov för att säkerställa att de mest korrekta händelserna skapas.

        >[!TIP]
        >
        >Det bästa sättet är att bara använda en [!DNL eVar] eller [!DNL prop].

      * För åtgärden väljer du **Ange händelse** och markerar platshållarhändelsen.

   1. I [!DNL Analytics] [!DNL Analysis Workspace] [skapar du ett projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=sv-SE) och drar den nya händelsen till en friformstabell för att se till att data fylls i för måttet [!DNL eVar] eller [!DNL prop].

1. Kontakta kontoteamet på Adobe för att synkronisera det nya mätvärdet med Adobe Advertising.

När mätvärdena är tillgängliga kan du använda dem för att skapa ett mål, som du sedan kan tilldela till en Search-, Social- och Commerce-portfölj eller använda som ett [anpassat mål](/help/dsp/optimization/custom-goal.md) för ett DSP.

Mer information om hur du skapar mål finns i kapitlet om optimeringsguiden, &quot;Mål&quot;, som du når från Search, Social och Commerce

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
