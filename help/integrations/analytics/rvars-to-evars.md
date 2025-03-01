---
title: Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics
description: Lär dig hur du samlar in historiska data för dina reserverade variabler i Adobe Analytics för framtida bruk i Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: 5b78ec0fc4c5ea4742cbb080b992bdb323fc9af3
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics

*Annonsörer med endast [!DNL Analytics for Advertising] och Adobe Customer Journey Analytics*

Om du använder reserverade variabler för att hämta [AMO ID och EF ID](ids.md) för din [!DNL Analytics for Advertising]-integrering, kan du förbereda dig för en framtida integrering mellan Adobe Advertising och [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), som är Adobe nästa generations [!DNL analytics]-lösning, genom att kopiera dina reserverade variabler för AMO ID och EF ID till [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) så snart som möjligt. Detta gör det möjligt att samla in historiska data för AMO-ID:n och EF-ID:n så snart du har slutfört uppgiften. Kontoteamet på Adobe meddelar dig om du använder reserverade variabler och behöver slutföra den här uppgiften.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Varför behöver jag samla in historiska data för Customer Journey Analytics?

Med Customer Journey Analytics kan du synkronisera data från Adobe Experience Platform till Adobe Analytics Analysis Workspace. För närvarande skickar inte [!DNL Analytics Data Connector] till Experience Platform data för reserverade variabler från [!DNL Analytics] till Experience Platform. Därför är data för AMO ID:n och EF ID:n som hämtas av reserverade variabler inte tillgängliga i Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising planerar en framtida implementering med Customer Journey Analytics. När implementeringen har släppts kommer din [!DNL Analytics for Advertising]-integrering fortfarande att kräva att du samlar in klickbara data <!-- Add back if we implement this:  and (DSP users) view-through data --> med hjälp av [!DNL Analytics]-spårning, men du kan visa dina data i både 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> och 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> om din organisation har båda produkterna. När funktionen släpps börjar Experience Platform samla in data för ditt AMO ID och EF ID för användning i Customer Journey Analytics, men det finns inga historiska data före releasedatumet.

Du kan dock börja samla in data för dina AMO ID:n och EF ID:n <!-- [!DNL rVars] --> tidigare genom att skapa en enkel [[!DNL Analytics] bearbetningsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) som kopierar dina AMO ID:n och EF ID:n <!-- [!DNL rVars] --> till [!DNL eVars] nu. När du har skapat bearbetningsregeln börjar du samla in data för dina AMO-ID:n och EF-ID:n <!-- [!DNL rVars] --> så snart de spårar nya händelser. Historikdata kommer sedan att vara tillgängliga i Customer Journey Analytics när implementeringen är tillgänglig.

>[!NOTE]
>
>* Från och med den 28 februari 2025 spårar den här processen klickdata men inte genomskinliga data.
>* Bearbetningsreglerna tillämpas bara på nya data som tas emot. De arbetar inte retroaktivt för att samla in tidigare data.

## Kopiera dina reserverade variabler för AMO ID:n och EF ID:n till [!DNL eVars]

Det här steget är manuellt och måste slutföras för varje rapportserie som spårar AMO-ID:n och EF-ID:n <!-- [!DNL rVars] --> som du förväntar dig ska integreras med Adobe Advertising i framtiden.

1. [Skapa en bearbetningsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) med följande inställningar:

   * Välj den rapportsvit för vilken du vill migrera AMO ID- och EF ID <!-- [!DNL rVar] -->-data till Experience Platform för användning av Customer Journey Analytics.

   * Använd ett beskrivande namn för [!UICONTROL Rule Title], till exempel&quot;Kopiera AMO ID och EF ID till eVars&quot;.

   * I avsnittet [!UICONTROL Always Execute] lägger du till två åtgärder för att skapa nya eVars:

      * För `AMO ID`:

         1. Välj **Skriv över värdet för**.
         1. Välj *\&lt;den nya/oanvända eVar\>*.
         1. Välj **Fråga efter strängparameter**.
         1. Ange `s_kwcid`.

        Exempel: ```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * För `EF ID`:

         1. Välj **Skriv över värdet för**.
         1. Välj *\&lt;den nya/oanvända eVar\>*.
         1. Välj **Fråga efter strängparameter**.
         1. Ange `ef_id`.

        Exempel: `Overwrite the value of rVar11 with Query String Parameter ef_id`

   * Använd en beskrivande anteckning för [!UICONTROL Reason for rule], till exempel&quot;AMO ID och EF ID kommer att transporteras till AEP via Adobe Analytics Connector.&quot;

1. Validera den sparade bearbetningsregeln.

   När du har sparat bearbetningsregeln ska data för `AMO ID` och `AMO EF ID` <!-- the existing reserved variables --> vara identiska med data för de två nya eVars som de kopieras till.

   Om till exempel den nya eVar `eVar142` mappas till `amo.s_kwcid(Context Data)`, ska data för `eVar142` och `AMO ID` vara identiska.

Mer information om hur bearbetningsregler tillämpas finns i [Hur bearbetningsregler fungerar](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about).

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
