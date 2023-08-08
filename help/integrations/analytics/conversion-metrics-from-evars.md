---
title: Skapa konverteringsstatistik från Adobe Analytics eVars och props
description: Konfigurera anpassade händelsemätningar för framgångar med hjälp av data på eVar- och prop-nivå.
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Skapa konverteringsstatistik från Adobe Analytics eVars och props

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Ni kan använda framgångsstatistik för att optimera DSP och sök-, sociala och handelskampanjer baserade på Adobe Analytics webbplatsdata som bäst passar ert varumärkes mål. Du kan konfigurera anpassade händelsemätningar för framgångshändelser baserat på dina befintliga [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) och [proppar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) genom att samla data på eVar- och prop-nivå i en händelse. Övriga [!DNL Analytics] Mätvärden, inklusive standardvärden, anpassade och reserverade konverteringsvärden och trafikvärden, är automatiskt tillgängliga i DSP och sökningar, sociala medier och handel.

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

1. Skapa en bearbetningsregel i [!DNL Analytics]:

   >[!NOTE]
   >
   >Endast [!DNL Analytics] kontoadministratörer kan skapa bearbetningsregler såvida de inte har gett tillstånd till icke-administratörer.

   1. [Skapa en bearbetningsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), med följande konfiguration:

      * Ange de eVars eller props som krävs för villkoret som måste uppfyllas.

        Du kan konfigurera ytterligare granularitetsnivåer efter behov för att säkerställa att de mest korrekta händelserna skapas.

        >[!TIP]
        >
        >Det bästa sättet är att bara använda en eVar eller ett produktstöd.

      * För åtgärden väljer du **Ange händelse** och välj platshållarhändelsen.

   1. I [!DNL Analytics] [!DNL Analysis Workspace], [skapa ett projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) och dra in den nya händelsen i en frihandstabell för att säkerställa att data fylls i för eVar- eller propmåttet.

1. Kontakta kontoteamet på Adobe för att synkronisera det nya mätvärdet med Adobe Advertising.

När mätvärdena är tillgängliga kan du använda dem för att skapa ett mål som du sedan kan tilldela till en portfölj för sökning, sociala medier och handel eller använda som en [anpassat mål](/help/dsp/optimization/custom-goal-about.md) för ett DSP.

Mer information om hur du skapar mål finns i kapitlet om optimeringsguiden,&quot;Mål&quot;, som du når via Sök, Socialt och Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Data i Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->