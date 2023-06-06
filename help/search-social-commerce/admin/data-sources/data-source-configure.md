---
title: Konfigurera en [!DNL Google Analytics] visa som en datakälla
description: Lär dig konfigurera en datakälla från en [!DNL Google Analytics] vy.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Konfigurera en [!DNL Google Analytics] visa som en datakälla

*Byråadministratörer, kontoansvariga för myndigheter, kontoansvariga för Adobe och administratörer*

Du kan skapa en datakälla per [!DNL Google Analytics] kombination av konto, egenskap och vy.

Om du vill integrera mätvärden för flera egenskaper eller för flera vyer för en enda egenskap skapar du en separat datakälla för varje.

1. [Utför alla förutsättningar för att integrera [!DNL Google Analytics] konto](data-source-prerequisites.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. I [!UICONTROL Deployment Prerequisites] markerar du kryssrutan för att bekräfta att den nödvändiga anpassade dimensionen &quot;ef_id&quot; implementeras i [!DNL Google Analytics] och klicka sedan på **[!UICONTROL Continue]**.

   Vissa förutsättningar kan ha uppfyllts av andra roller i organisationen. Om du har frågor om förutsättningarna kan du prata med ditt Adobe-kontoteam.

1. Ange [inställningar för datakälla](data-source-settings.md):

   1. I **[!UICONTROL Connect to [!DNL Google Analytics]]** gör du följande.

      1. Ange det numeriska ID:t för [!DNL Google Analytics] konto.

      1. Ange den e-postadress som ska användas för att komma åt data för den här datakällan. E-postadressen måste registreras hos en [!DNL Google] kontot och har behörigheten&quot;Läs och analysera&quot; för [!DNL Google Analytics] konto. Se [instruktioner för att tilldela användarbehörigheter i [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Se till att bara [!DNL Google Analytics] egenskaper och vyer är tillgängliga i Adobe Advertising, log in using an email address that has access only those properties and views.

         >[!NOTE]
         >
         >Om du senare ändrar lösenordet för det här e-postkontot stängs alla öppna anslutningar till e-postkontot. Om du vill återuppta synkroniseringen av data går du tillbaka till den här sidan och [reauthenticate](data-source-reauthenticate.md).

      1. Markera kryssrutan för att godkänna Adobe-annonsering för att få åtkomst till kontots statistik.

      1. Klicka på **[!UICONTROL Authenticate]**.
   1. I [!UICONTROL Account Details] anger du egenskapen och vyn för måtten som ska importeras. Ange dessutom den anpassade dimensionen som är ifylld med värdet för frågesträngsparametern&quot;ef_id&quot;.

   1. I [!UICONTROL Import Metrics] anger du de mätvärden som ska ingå i feeden/fotona.

      Du kan inte ta bort [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], eller [!UICONTROL Session Duration], som inkluderas automatiskt. Ni kan lägga till upp till 16 ytterligare giltiga mått eller mätvärden utan data.

      >[!WARNING]
      >
      >[!DNL Google Analytics] tillåter upp till 10 mätvärden i ett enda dataflöde. Search, Social, &amp; Commerce har stöd för upp till två feeds med totalt 20 mätvärden, men med en andra feed fördubblas API-anropen till [!DNL Google Analytics]. Om du har många mätvärden väljer du bara de mätvärden som du vill använda i optimeringsmål. Läs mer om [kvoter och anropsbegränsningar för API-begäranden till [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. I [!UICONTROL Metric Tag] anger du namnet på taggen som ska läggas till i varje mått för datakällan.


1. Klicka på uppe till höger **[!UICONTROL Post]**.

   Datakällan heter&quot;AccountName > PropertyName > ViewName&quot; och aktiveras automatiskt. Om du vill pausa datakällan läser du &quot;[Pausa en feed från en datakälla](data-source-pause.md).&quot;

   Mätvärdena är tillgängliga nästa dag efter att den dagliga datasynkroniseringen har slutförts, som börjar klockan 05:00 i annonsörens tidszon. När mätvärdena är tillgängliga visas de i [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Varje ny transaktionsegenskap heter`ga:backEndMetricName_propertyID_viewID`,&quot; där&quot;backEndMetricName&quot; är det metriska namn som används av API:t. Visningsnamnet för varje ny transaktionsegenskap är &quot;`friendlyMetricName_ga:MetricTag`,&quot; där&quot;friendlyMetricName&quot; är måttnamnet som visas i [!DNL Google Analytics] och &quot;MetricTag&quot; är [!UICONTROL Metric Tag] som definieras i inställningarna för datakällan.

   Ni kan lägga till mätvärden direkt till kampanjhanteringsaktiviteter och portföljhanteringsvyer, rapporter och optimeringsmål.

>[!MORELIKETHIS]
>
>* [Synkronisering [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [Återautentisera en [!DNL Google Analytics] datakälla](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgänglig [!DNL Google Analytics] mått](data-source-ga-metrics.md)

