---
title: Konfigurera en [!DNL Google Analytics] vy som datakälla
description: Lär dig hur du konfigurerar en datakälla från en [!DNL Google Analytics] vy.
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Konfigurera en [!DNL Google Analytics]-vy som datakälla

*Endast kontoansvariga, kontoansvariga för kontoansvariga, kontoansvariga för Adobe och administratörer*

Du kan skapa en datakälla per kombination av konto, egenskap och vy för [!DNL Google Analytics].

Om du vill integrera mätvärden för flera egenskaper eller för flera vyer för en enda egenskap skapar du en separat datakälla för varje.

1. [Utför alla nödvändiga komponenter för att integrera  [!DNL Google Analytics] kontot](data-source-prerequisites.md).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]** på huvudmenyn.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. I dialogrutan [!UICONTROL Deployment Prerequisites] markerar du kryssrutan för att bekräfta att den nödvändiga anpassade dimensionen &quot;ef_id&quot; har implementerats i [!DNL Google Analytics]-kontot och klickar sedan på **[!UICONTROL Continue]**.

   Vissa förutsättningar kan ha uppfyllts av andra roller i organisationen. Om du har frågor om förutsättningarna kan du kontakta ditt Adobe-kontoteam.

1. Ange inställningarna för [datakälla](data-source-settings.md):

   1. Gör följande i avsnittet **[!UICONTROL Connect to [!DNL Google Analytics]]**.

      1. Ange det numeriska ID:t för kontot [!DNL Google Analytics].

      1. Ange den e-postadress som ska användas för att komma åt data för den här datakällan. E-postadressen måste vara registrerad för ett [!DNL Google]-konto och ha behörigheten Läs och analysera för [!DNL Google Analytics]-kontot. Se [instruktionerna om hur du tilldelar användarbehörigheter i  [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Om du vill vara säker på att endast vissa [!DNL Google Analytics] egenskaper och vyer är tillgängliga i Adobe Advertising loggar du in med en e-postadress som bara har åtkomst till dessa egenskaper och vyer.

         >[!NOTE]
         >
         >Om du senare ändrar lösenordet för det här e-postkontot stängs alla öppna anslutningar till e-postkontot. Om du vill återuppta synkroniseringen av data går du tillbaka till den här sidan och [återautentiserar](data-source-reauthenticate.md).

      1. Markera kryssrutan för att godkänna att Adobe Advertising får åtkomst till kontots statistik.

      1. Klicka på **[!UICONTROL Authenticate]**.

   1. I avsnittet [!UICONTROL Account Details] anger du egenskapen och vyn för måtten som ska importeras. Ange dessutom den anpassade dimensionen som är ifylld med värdet för frågesträngsparametern&quot;ef_id&quot;.

   1. I avsnittet [!UICONTROL Import Metrics] anger du de mått som ska inkluderas i feeden/flödena.

      Du kan inte ta bort [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] eller [!UICONTROL Session Duration] som inkluderas automatiskt. Ni kan lägga till upp till 16 ytterligare giltiga mått eller mätvärden utan data.

      >[!WARNING]
      >
      >[!DNL Google Analytics] tillåter upp till 10 mätvärden i en enda datafeed. Search, Social och Commerce har stöd för upp till två feeds med totalt 20 mätvärden, men om du använder en andra feed dubbleras dina API-anrop till [!DNL Google Analytics]. Om du har många mätvärden väljer du bara de mätvärden som du vill använda i optimeringsmål. Se mer om [kvoter och anropsgränser för API-begäranden till [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. I avsnittet [!UICONTROL Metric Tag] anger du namnet på taggen som ska läggas till i varje mått för datakällan.

1. Klicka på **[!UICONTROL Post]** i det övre högra hörnet.

   Datakällan heter&quot;AccountName > PropertyName > ViewName&quot; och aktiveras automatiskt. Information om hur du pausar datakällan finns i [Pausa en feed från en Data Source](data-source-pause.md).

   Mätvärdena är tillgängliga nästa dag efter att den dagliga datasynkroniseringen har slutförts, som börjar klockan 05:00 i annonsörens tidszon. När mätvärdena är tillgängliga visas de i [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Varje nytt konverteringsmått har namnet `ga:backEndMetricName_propertyID_viewID`, där backEndMetricName är det metriska namn som används av API:t. Visningsnamnet för varje nytt konverteringsmått är `friendlyMetricName_ga:MetricTag`, där&quot;friendlyMetricName&quot; är måttnamnet som visas i [!DNL Google Analytics] och&quot;MetricTag&quot; är [!UICONTROL Metric Tag] som definieras i inställningarna för datakällan.

   Ni kan lägga till mätvärden direkt till kampanjhanteringsaktiviteter och portföljhanteringsvyer, rapporter och optimeringsmål.

>[!MORELIKETHIS]
>
>* [Synkronisering av  [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgängliga [!DNL Google Analytics] mått](data-source-ga-metrics.md)
