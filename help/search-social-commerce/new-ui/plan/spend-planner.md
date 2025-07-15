---
title: Använda [!UICONTROL Spend Planner]
description: Lär dig hur du använder [!UICONTROL Spend Planner] för att identifiera den optimala utgiftsfördelningen mellan portföljer.
feature: Search Optimization, Search Portfolios, Search Simulations
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Använda [!UICONTROL Spend Planner]

<!-- When this becomes a menu item, move file and TOC entry accordingly -->

[!UICONTROL Spend Planner] (som kallas&quot;verktyget för utgiftsrekommendation&quot; i det äldre användargränssnittet) identifierar den optimala utgiftsfördelningen för optimerade och aktiva portföljer med samma mål och valuta så att du kan maximera intäkterna eller målmålen för portföljuppsättningen.

När du visar en utgiftsrekommendationsrapport för portföljer med daglig budget kan du ändra budgeten för vilken som helst av portföljerna till den rekommenderade budgeten.

## Data i rapporten [!UICONTROL Spend Planner]

För portföljer med målet [!UICONTROL Maximize Clicks] innehåller rapporten utgiftsrekommendationer och klickprognoser. För alla andra mål innehåller rapporten utgiftsrekommendationer och intäktsprognoser.

Rapporten om utgiftsrekommendationer innehåller följande data:

* Ett punktdiagram visar de förväntade maximala intäkterna eller klick som kan uppnås med en given totalkostnad för portföljuppsättningen när de enskilda utgiftsmålen ställs in optimalt. Den förväntade kostnaden för varje intäktspunkt eller klickpunkt inkluderas.

* Två donndiagram som visar utgiften och den förväntade intäkten eller klicka på distributionen per portfölj för 1\) de aktuella utgiftsmålen och 2\) de föreslagna utgiftsmålen.

* Ett stapeldiagram för var och en av portföljerna som visar den rekommenderade dagliga utgiftsfördelningen (kostnad) och den förväntade intäktsfördelningen eller klickfördelningen när du behåller det aktuella totala dagliga utgiftsmålet för alla valda portföljer, eller för ett föreslaget totalt utgiftsmål. Du kan också använda de rekommenderade utgiftsmålen för de valda portföljerna, vilket påverkar budgivning under nästa budkörningscykel.

## (Nytt användargränssnitt) Generera en [!UICONTROL Spend Planner]-rapport från vyn [!UICONTROL Manage] > [!UICONTROL Simulations]

<!-- The path will probably change, so then update the heading and instructions -->

1. Klicka på **[!UICONTROL Plan]>[!UICONTROL Simulations]** på huvudmenyn.

1. I verktygsfältet ovanför datatabellen klickar du på ![Spend Planner](/help/search-social-commerce/assets/spend-planner-icon.png "Spend Planner").

   Verktyget [!UICONTROL Spend Recommendation] öppnas i det äldre användargränssnittet.

1. Visa data med aktuella, kombinerade budgetar för de valda portföljerna:

   1. Välj portföljmålet.

   1. Välj valuta.

   1. (Valfritt) Välj en strategi för portföljutgifter för att ytterligare filtrera portföljlistan.

   1. Markera kryssrutan bredvid varje portfölj som ska inkluderas. Om du vill välja alla portföljer markerar du kryssrutan bredvid [!UICONTROL Portfolios].

      Endast optimerade och aktiva portföljer med de valda parametrarna visas.

   1. Klicka på **[!UICONTROL Update]**.

   1. (Valfritt) Håll markören över punkten om du vill se kostnad och intäkt för en punkt i diagrammet.

1. (Valfritt) Om du vill visa rekommenderad daglig utgift och förväntade intäkter för var och en av portföljerna med ett nytt totalt utgiftsmål anger du ett föreslaget totalt dagligt utgiftsmål för alla portföljer i fältet [!UICONTROL Total Spend Target]. Tryck sedan på tangenten **Enter**.

   Verktyget för utgiftsrekommendation använder data från veckosimuleringar, så den totala rekommenderade utgiften är den närmaste matchningen till det föreslagna utgiftsmålet med den idealiska utgiftsmixen.

## (Äldre användargränssnitt) Generera en [!UICONTROL Spend Recommendation]-rapport från vyn [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation]

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]** på huvudmenyn.

1. Visa data med aktuella, kombinerade budgetar för de valda portföljerna:

   1. Välj portföljmålet.

   1. Välj valuta.

   1. (Valfritt) Välj en strategi för portföljutgifter för att ytterligare filtrera portföljlistan.

   1. Markera kryssrutan bredvid varje portfölj som ska inkluderas. Om du vill välja alla portföljer markerar du kryssrutan bredvid [!UICONTROL Portfolios].

      Endast optimerade och aktiva portföljer med de valda parametrarna visas.

   1. Klicka på **[!UICONTROL Update]**.

   1. (Valfritt) Håll markören över punkten om du vill se kostnad och intäkt för en punkt i diagrammet.

1. (Valfritt) Om du vill visa rekommenderad daglig utgift och förväntade intäkter för var och en av portföljerna med ett nytt totalt utgiftsmål anger du ett föreslaget totalt dagligt utgiftsmål för alla portföljer i fältet [!UICONTROL Total Spend Target]. Tryck sedan på tangenten **Enter**.

   Verktyget för utgiftsrekommendation använder data från veckosimuleringar, så den totala rekommenderade utgiften är den närmaste matchningen till det föreslagna utgiftsmålet med den idealiska utgiftsmixen.

## Använd utgiftsrekommendationer

*Portföljer med endast daglig budget*

>[!NOTE]
>
>* Om de tillämpade ändringarna ökar eller minskar utgiftsmålet för en portfölj med mer än 20 % får du ett meddelande och måste godkänna ändringen.
>* När utgiftsmålet för en portfölj ändras med över 20 % tar det upp till 3-4 dagar för Search, Social och Commerce att justera sina modeller och uppnå det nya målet.

1. Visa utgiftsrekommendationsrapporten för en eller flera portföljer med daglig budget.

1. Markera kryssrutan bredvid varje portfölj som du vill använda det rekommenderade utgiftsmålet för. Om du vill välja alla portföljer markerar du kryssrutan bredvid [!UICONTROL Select All Recommendations].

1. Klicka på **[!UICONTROL Apply Selected Recommendations]**.

1. (Om någon av budgetarna ändras med mer än 20 %) Klicka på **[!UICONTROL Yes]** i bekräftelsemeddelandet för att godkänna ändringarna.

## Öppna eller spara data i en fil

Du kan exportera rapportdata från alla avsnitt i rapporten [!UICONTROL Spend Recommendation]. Du kan antingen öppna eller spara data som en [!DNL Microsoft Excel]-arbetsboksfil.

1. Generera en utgiftsrekommendationsrapport för valda portföljer.

1. Ovanför rapporten klickar du på ![Hämta](/help/search-social-commerce/assets/download-spend-recommendation.png "Hämta").

   Öppna eller spara filen enligt webbläsarens normala procedur.  Mer information finns i webbläsarens onlinehjälp.
