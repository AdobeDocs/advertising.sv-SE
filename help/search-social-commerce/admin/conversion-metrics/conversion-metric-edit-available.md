---
title: Ändra konverteringsstatistik som är tillgänglig i ledningslägen och rapporter
description: Lär dig hur du gör konverteringsstatistik tillgänglig i dina ledningslägen och rapporter.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Ändra konverteringsstatistik som är tillgänglig i ledningslägen och rapporter

När Adobe Advertising spårar ett [konverteringsmått](/help/search-social-commerce/glossary.md#c-d) för en annonsörer exkluderas det från portföljmål, rapporter och hanteringsvyer. Om du vill att ett konverteringsmått ska vara synligt måste du göra det tillgängligt explicit och sedan eventuellt ändra standardvisningsnamnet, som är det namn som visas. Det enda undantaget är att konverteringar som spåras av [!DNL Google Ads], [!DNL Google Analytics] och [!DNL Microsoft Advertising] universella händelsespårningstaggar är automatiskt tillgängliga och synliga.

På samma sätt kan du dölja ett konverteringsmått för portföljmål, rapporter och vyer över hanteringen. När du döljer ett konverteringsmått som tidigare var synligt tas det bort från alla härledda mått som innehåller konverteringsmåttet.

I den lista över konverteringsmått som är tillgängliga kan varje användare med tillgång till annonsörens data anpassa de mätvärden de ser för vyer och rapporter, inklusive eller utelämna specifika mätvärden när de väljer.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** på huvudmenyn.

   Alla konverteringsvärden som har samlats in för annonsören och alla andra namn som har angetts för visning visas.

1. (Valfritt) Filtrera listan:

   * Om du vill söka efter ett specifikt måttnamn eller visningsnamn klickar du på ![Sök](/help/search-social-commerce/assets/search.png "Sök"), anger ordet eller strängen i inmatningsfältet och trycker sedan på **[!DNL Enter]**.

     Du kan söka efter strängar som visas var som helst inom frasen (till exempel den första bokstaven eller de sista tre bokstäverna) och söktermerna är inte [skiftlägeskänsliga](/help/search-social-commerce/glossary.md#c-d).

   * Om du vill söka efter konverteringsmått efter deras tillgänglighet i hanteringsvyer och rapporter klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") och väljer filtret **[!UICONTROL Show in UI and Reports]**. Välj sedan antingen **[!UICONTROL Show]** (för att visa konverteringsstatistik som är tillgänglig för rapporter och hanteringsvyer) eller **[!UICONTROL Hide]** (för att visa konverteringsstatistik som inte är tillgänglig i rapporter och hanteringsvyer).

1. Ändra konverteringsmåtten som är tillgängliga för hanteringsvyer och rapporter:

   * Om du vill visa eller dölja ett enskilt mått klickar du på växeln i kolumnen **[!UICONTROL Show in UI and Reports]** för att ändra inställningen.

   * Så här visar eller döljer du flera mätvärden:

      1. Markera kryssrutan bredvid varje konverteringsmått.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicka på ![Visa](/help/search-social-commerce/assets/show.png "Visa") i verktygsfältet ovanför datatabellen om du vill visa måtten eller ![Dölj](/help/search-social-commerce/assets/hide.png "Dölj") om du vill dölja måtten.

      1. (Om du vill dölja mätvärden) Klicka på **[!UICONTROL Yes]** i bekräftelsemeddelandet för att dölja mätvärdena, inklusive att ta bort dem från härledda mätvärden som innehåller mätvärdena.

1. (Valfritt) [Ändra namnet som visas i kolumnrubriker](conversion-metric-edit-display-name.md) för något av konverteringsmåtten.

   Standardvisningsnamnet för varje synligt konverteringsmått är måttets namn så som det är stavat i hämtade data.

>[!NOTE]
>
>Om Adobe Advertising samlar in data för nya konverteringsmått, kommer de nya mätvärdena - förutom konverteringar som spåras av [!DNL Google Ads], [!DNL Google Analytics] och [!DNL Microsoft Advertising] universella händelsespårningstaggar - automatiskt att exkluderas från hanteringsvyer och rapporter tills du inkluderar dem. Nya konverteringar som spåras av [!DNL Google Ads], [!DNL Google Analytics] och [!DNL Microsoft Advertising] universella händelsespårningstaggar är alltid automatiskt tillgängliga.

>[!MORELIKETHIS]
>
>* [Om att hantera en annonsörs konverteringsmått](conversion-metric-about.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](conversion-metric-view-tracked.md)
>* [Ändra visningsnamnet för ett konverteringsmått](conversion-metric-edit-display-name.md)
