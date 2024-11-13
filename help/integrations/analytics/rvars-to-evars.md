---
title: Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics
description: Lär dig hur du samlar in historiska data för dina reserverade variabler i Adobe Analytics för framtida bruk i Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Samla in historiska data för AMO ID:n och EF ID:n för användning i Adobe Customer Journey Analytics

*Annonsörer med endast [!DNL Analytics for Advertising] och Adobe Customer Journey Analytics*

Om du använder reserverade variabler för att hämta [AMO ID och EF ID](ids.md) för din [!DNL Analytics for Advertising]-integrering, kan du förbereda dig för en framtida integrering mellan Adobe Advertising och [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), som är Adobe:s nästa generations [!DNL analytics]-lösning, genom att kopiera dina reserverade variabler för AMO ID och EF ID till [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) så snart som möjligt. Detta gör det möjligt att samla in historiska data för AMO-ID:n och EF-ID:n så snart du har slutfört uppgiften. Kontoteamet på Adobe meddelar dig om du använder reserverade variabler och behöver slutföra den här uppgiften.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Varför måste jag samla in historiska data för Customer Journey Analytics?

Med Customer Journey Analytics kan du synkronisera data från Adobe Experience Platform till Adobe Analytics Analysis Workspace. För närvarande skickar inte [!DNL Analytics Data Connector] till Experience Platform data för reserverade variabler från [!DNL Analytics] till Experience Platform. Därför är data för AMO ID:n och EF ID:n som hämtas av reserverade variabler för närvarande inte tillgängliga i Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising planerar en framtida implementering med Customer Journey Analytics. När implementeringen har släppts kommer din [!DNL Analytics for Advertising]-integrering fortfarande att kräva att du samlar in klickbara data och (DSP användare) genomsiktsdata med [!DNL Analytics] tracking, men du kan visa dina data i både 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> och 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> om din organisation har båda produkterna. När funktionen släpps kommer Experience Platform att börja samla in data för ditt AMO ID och EF ID för användning i Customer Journey Analytics, men det kommer inte att finnas några historiska data före releasedatumet.

Du kan dock börja samla in data för dina AMO ID:n och EF ID:n <!-- [!DNL rVars] --> tidigare genom att skapa en enkel [[!DNL Analytics] bearbetningsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) som kopierar dina AMO ID:n och EF ID:n <!-- [!DNL rVars] --> till [!DNL eVars] nu. När du har skapat bearbetningsregeln börjar du samla in data för dina AMO-ID:n och EF-ID:n <!-- [!DNL rVars] --> så snart de spårar nya händelser. Historikdata kommer sedan att finnas tillgängliga i Customer Journey Analytics när implementeringen är tillgänglig.

>[!NOTE]
>
>Bearbetningsreglerna tillämpas bara på nya data som tas emot. De arbetar inte retroaktivt för att samla in tidigare data.

## Kopiera dina reserverade variabler för AMO ID:n och EF ID:n till [!DNL eVars]

Det här steget är manuellt och måste slutföras för varje rapportserie som spårar AMO-ID:n och EF-ID:n <!-- [!DNL rVars] --> som du förväntar dig ska integreras med Adobe Advertising i framtiden.

1. [Skapa en bearbetningsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) med följande inställningar:

   * Välj den rapportsvit som du vill migrera AMO ID- och EF ID <!-- [!DNL rVar] -->-data för till Experience Platform för användning av Customer Journey Analytics.

   * Använd ett beskrivande namn för [!UICONTROL Rule Title], till exempel&quot;Kopiera AMO ID och EF ID till eVars&quot;.

   * I avsnittet [!UICONTROL Always Execute] lägger du till två åtgärder för att skapa nya eVars:

      * För `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * För `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Använd en beskrivande anteckning för [!UICONTROL Reason for rule], till exempel&quot;AMO ID och EF ID kommer att transporteras till AEP via Adobe Analytics Connector.&quot;

1. Validera den sparade bearbetningsregeln.

   När du har sparat bearbetningsregeln ska data för `AMO ID` och `AMO EF ID` <!-- the existing reserved variables --> vara identiska med data för de två nya eVars som de kopieras till.

   Om till exempel den nya eVarna `eVar142` mappas till `amo.s_kwcid(Context Data)`, ska data för `eVar142` och `AMO ID` vara identiska.

Mer information om hur bearbetningsregler tillämpas finns i [Hur bearbetningsregler fungerar](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about).

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
