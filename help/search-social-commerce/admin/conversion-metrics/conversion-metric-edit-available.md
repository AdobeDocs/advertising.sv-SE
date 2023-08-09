---
title: Ändra konverteringsstatistik som är tillgänglig i ledningslägen och rapporter
description: Lär dig hur du gör konverteringsstatistik tillgänglig i dina ledningslägen och rapporter.
feature: Conversions
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Ändra konverteringsstatistik som är tillgänglig i ledningslägen och rapporter

När Adobe Advertising spårar en [konvertering](/help/search-social-commerce/glossary.md#c-d) För en annonsörer ingår den inte i portföljens mål, rapporter och ledningens åsikter. Om du vill att ett konverteringsmått ska vara synligt måste du göra det tillgängligt explicit och sedan eventuellt ändra standardvisningsnamnet, som är det namn som visas. Det enda undantaget är att konverteringar spåras av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] universella händelsespårningstaggar är automatiskt tillgängliga och synliga.

På samma sätt kan du dölja ett konverteringsmått för portföljmål, rapporter och vyer över hanteringen. När du döljer ett konverteringsmått som tidigare var synligt tas det bort från alla härledda mått som innehåller konverteringsmåttet.

I den lista över konverteringsmått som är tillgängliga kan varje användare med tillgång till annonsörens data anpassa de mätvärden de ser för vyer och rapporter, inklusive eller utelämna specifika mätvärden när de väljer.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Alla konverteringsvärden som har samlats in för annonsören och alla andra namn som har angetts för visning visas.

1. (Valfritt) Filtrera listan:

   * Om du vill söka efter ett specifikt måttnamn eller visningsnamn klickar du på ![Sök](/help/search-social-commerce/assets/search.png "Sök")anger du ordet eller strängen i indatafältet och trycker sedan på **[!DNL Enter]** -tangenten.

     Du kan söka efter strängar som visas var som helst i frasen (till exempel den första bokstaven eller de sista tre bokstäverna) och söktermerna är inte [skiftlägeskänslig](/help/search-social-commerce/glossary.md#c-d).

   * Om du vill söka efter konverteringsmått utifrån deras tillgänglighet i hanteringsvyer och rapporter klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter")och markera filtret **[!UICONTROL Show in UI and Reports]**. Välj sedan antingen **[!UICONTROL Show]** (för att visa konverteringsstatistik som kan inkluderas i rapporter och hanteringsvyer) eller **[!UICONTROL Hide]** (för att visa konverteringsvärden som inte är tillgängliga i rapporter och hanteringsvyer).

1. Ändra konverteringsmåtten som är tillgängliga för hanteringsvyer och rapporter:

   * Om du vill visa eller dölja ett enskilt mått klickar du på knappen i dialogrutan **[!UICONTROL Show in UI and Reports]** -kolumn för att ändra inställningen.

   * Så här visar eller döljer du flera mätvärden:

      1. Markera kryssrutan bredvid varje konverteringsmått.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Visa](/help/search-social-commerce/assets/show.png "Visa") för att visa mätvärden eller ![Dölj](/help/search-social-commerce/assets/hide.png "Dölj") för att dölja mätvärden.

      1. (Om du vill dölja mätvärden) Klicka på **[!UICONTROL Yes]** för att dölja mätvärden, inklusive att ta bort dem från härledda mätvärden som innehåller mätvärdena.

1. (Valfritt) [Ändra namnet som visas i kolumnrubriker](conversion-metric-edit-display-name.md) för alla konverteringsvärden.

   Standardvisningsnamnet för varje synligt konverteringsmått är måttets namn så som det är stavat i hämtade data.

>[!NOTE]
>
>Om Adobe Advertising samlar in data för nya konverteringsvärden, kommer de nya mätvärdena - förutom konverteringar som spåras av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] taggar för universell händelsespårning - exkluderas automatiskt från hanteringsvyer och rapporter tills du inkluderar dem. Nya konverteringar spårade av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] universella händelsespårningstaggar är alltid automatiskt tillgängliga.

>[!MORELIKETHIS]
>
* [Om att hantera en annonsörs konverteringsstatistik](conversion-metric-about.md)
* [Visa konverteringsstatistik som spårats för en annonsörer](conversion-metric-view-tracked.md)
* [Ändra visningsnamnet för ett konverteringsmått](conversion-metric-edit-display-name.md)
