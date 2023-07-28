---
title: Ändra transaktionsegenskaperna som är tillgängliga i hanteringsvyer och rapporter
description: Lär dig hur du gör transaktionsegenskaper tillgängliga i hanteringsvyer och rapporter.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: Search Admin, Search Transaction Properties
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Ändra transaktionsegenskaperna som är tillgängliga i hanteringsvyer och rapporter

När Adobe Advertising spårar en [transaktionsegenskap](/help/search-social-commerce/glossary.md#s-t) För en annonsörer har annonsören från början uteslutits från portföljmål, rapporter och vyer över ledningen. Om du vill göra en egenskap synlig måste du uttryckligen göra den tillgänglig och sedan eventuellt ändra standardvisningsnamnet, som är det namn som visas. Det enda undantaget är att konverteringar spåras av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] universella händelsespårningstaggar är automatiskt tillgängliga och synliga.

På samma sätt kan du dölja en egenskap för portföljmål, rapporter och hanteringsvyer. När du döljer en egenskap som tidigare var synlig tas den bort från alla härledda mått som innehåller egenskapen.

I listan med tillgängliga egenskaper kan varje användare som har tillgång till annonsörens data anpassa de egenskaper som de ser för hanteringsvyer och rapporter, inklusive eller utelämna specifika egenskaper när de väljer.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Alla transaktionsegenskaper som har samlats in för annonsören och alla andra namn som har angetts för visning visas.

1. (Valfritt) Filtrera listan:

   * Om du vill söka efter ett specifikt egenskapsnamn eller visningsnamn klickar du på ![Sök](/help/search-social-commerce/assets/search.png "Sök")anger du ordet eller strängen i indatafältet och trycker sedan på **[!DNL Enter]** -tangenten.

     Du kan söka efter strängar som visas var som helst i frasen (till exempel den första bokstaven eller de sista tre bokstäverna) och söktermerna är inte [skiftlägeskänslig](/help/search-social-commerce/glossary.md#c-d).

   * Om du vill söka efter egenskaper utifrån deras tillgänglighet i hanteringsvyer och rapporter klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter")och markera filtret **[!UICONTROL Show in UI and Reports]**. Välj sedan antingen **[!UICONTROL Show]** (för att visa de egenskaper som är tillgängliga för rapporter och hanteringsvyer) eller **[!UICONTROL Hide]** (för att visa egenskaper som inte är tillgängliga i rapporter och hanteringsvyer).

1. Ändra de egenskaper som är tillgängliga för hanteringsvyer och rapporter:

   * Om du vill visa eller dölja en enskild egenskap klickar du på knappen i **[!UICONTROL Show in UI and Reports]** -kolumn för att ändra inställningen.

   * Så här visar eller döljer du flera egenskaper:

      1. Markera kryssrutan bredvid varje egenskap.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Visa](/help/search-social-commerce/assets/show.png "Visa") för att visa egenskaperna eller ![Dölj](/help/search-social-commerce/assets/hide.png "Dölj") om du vill dölja egenskaperna.

      1. (Om du vill dölja egenskaper) Klicka på **[!UICONTROL Yes]** om du vill dölja egenskaperna, inklusive ta bort dem från alla härledda mått som innehåller egenskaperna.

1. (Valfritt) [Ändra namnet som visas i kolumnrubriker](transaction-property-edit-display-name.md) för någon av egenskaperna.

   Standardvisningsnamnet för varje synlig egenskap är egenskapsnamnet som det är stavat i hämtade data.

>[!NOTE]
>
>Om Adobe Advertising samlar in data för nya egenskaper, kommer de nya egenskaperna att gälla - med undantag för konverteringar som spåras av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] taggar för universell händelsespårning - exkluderas automatiskt från hanteringsvyer och rapporter tills du inkluderar dem. Nya konverteringar spårade av [!DNL Google Ads], [!DNL Google Analytics]och [!DNL Microsoft® Advertising] universella händelsespårningstaggar är alltid automatiskt tillgängliga.

>[!MORELIKETHIS]
>
* [Hantera en annonsörs transaktionsegenskaper](transaction-property-about.md)
* [Visa transaktionsegenskaper som spårats för en annonsörer](transaction-property-view-tracked.md)
* [Ändra visningsnamnet för en transaktionsegenskap](transaction-property-edit-display-name.md)
