---
title: Visa Sites, Ads, Frequency och Inventory Details för en placering
description: Lär dig hur du visar målwebbplatser, annonser, frekvens och inventeringsdata för en placering.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Visa Sites, Ads, Frequency och Inventory Details för en placering

För varje placering kan du [öppna en (detaljvy [!UICONTROL Inspector])](placement-details-view.md) som visar alla målwebbplatser, annonser och erbjudanden på en plats. Den innehåller även frekvensdata för placeringen. Du kan också exportera data från valfri flik.

![placeringsinspektör](/help/dsp/assets/placement-inspector.png)

## Information i placeringen [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Alla platser där placeringen har haft avbildningar.

  Fliken [!UICONTROL Sites] innehåller sök- och filterfunktioner, samma standardvy och anpassade kolumnvisningsalternativ som är tillgängliga på huvudsidan samt en [!UICONTROL Exclude]-knapp i varje rad så att du snabbt kan utesluta en webbplats från placeringen.

* **[!UICONTROL Ads]:** Alla annonser i placeringen.

  Fliken [!UICONTROL Ads] innehåller sök- och filterfunktioner, samma standardalternativ och anpassade kolumnvisningsalternativ som finns på huvudsidan samt snabbåtgärdsknappar i varje rad, till exempel [!UICONTROL Pause] (så att du snabbt kan pausa en annons).

* **[!UICONTROL Frequency]:** Data för varje annonsfrekvensnivå för placeringen, inklusive:
   * annonsfrekvensen (t.ex. &quot;1&quot; för alla tillfällen då användaren såg en annons en gång)
   * det uppskattade unika antalet enheter/webbläsare eller personer (beroende på den angivna [!UICONTROL Cross Device Level] för kampanjen) som fick visningar på den angivna frekvensnivån
   * det uppskattade antalet avtryck på den angivna frekvensnivån
   * den uppskattade genomsnittliga frekvensen för den angivna frekvensnivån. Detta värde är lika med (Estimated Impressions)/(Estimated Uniques).

* **[!UICONTROL Inventory]:** Information om alla erbjudanden som är riktade till placeringen.

  Fliken [!UICONTROL Inventory] gör det möjligt att snabbt felsöka genom att visa prestandastatistik, som [!UICONTROL Auctions], [!UICONTROL Bids] och [!UICONTROL Win Rate]. Fliken innehåller sök- och filterfunktioner, samma standardalternativ och anpassade kolumnvisningsalternativ som finns på huvudsidan, och snabbåtgärdsknappar i varje rad, inklusive [!UICONTROL Edit], [!UICONTROL View Report] och [[!UICONTROL Auction Insights] för ytterligare felsökning](/help/dsp/inventory/private-deal-auction-insights.md).

## Öppna [!UICONTROL Placement Inspector]

1. Öppna placeringsvyn för den överordnade kampanjen eller det överordnade paketet:

   * Visa alla placeringar i den överordnade kampanjen:

      1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

      1. Klicka på kampanjens namn.

      1. Klicka på fliken **[!UICONTROL Placements]**.

   * Visa alla placeringar i det överordnade paketet:

      1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

      1. Klicka på kampanjens namn.

      1. Klicka på fliken **[!UICONTROL Packages]**.

      1. Klicka på det överordnade paketets namn.

1. Håll markören över placeringsraden, klicka på **[!UICONTROL More]** och klicka sedan på ett alternativ:

   * Klicka på **[!UICONTROL Sites]** om du vill visa alla platser som placeringsmålen gäller.

   * Om du vill visa alla annonser på platsen klickar du på **[!UICONTROL Ads]**.

   * Om du vill visa frekvensdata för placeringen klickar du på **[!UICONTROL Frequency]**.

   * Om du vill visa alla avtal som placeringsmålen gäller klickar du på **[!UICONTROL Inventory]**.

1. (Valfritt) [Ändra kolumnvyn](campaign-data-views-manage.md#column-view-change) om det behövs för att visa de mått som krävs.

1. (Valfritt) Om du vill exportera data på en flik klickar du på ![Mer](/help/search-social-commerce/assets/more.png "Mer") i det övre högra hörnet och sedan på **[!UICONTROL Export]**.

   Informationen sparas i webbläsarens standardmapp för hämtning som en rapport i XLSM-format.

## Felsökning av lager

| Problem | Möjlig orsak | Åtgärder att vidta |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Utgivaren har inte börjat skicka anbudsförfrågningar. | Kontakta utgivaren för att aktivera erbjudandet. |
| | Avtalet ställdes in felaktigt, till exempel genom att ett felaktigt externt avtal-ID angavs. | Bekräfta avtalsinformationen och redigera erbjudandet. |
| [!UICONTROL Auctions but no Bids] | Placeringsmålet matchar inte inkommande anbudsförfrågningar för erbjudandet. <br><br> En placering kan till exempel ha en geografisk inriktning som inte är berättigad till erbjudandet. | Redigera placeringsmålen efter behov för att undvika felaktiga målmatchningar. |
| | Placeringen har ingen aktiv annons med den medietyp som krävs för erbjudandet. | Skapa och bifoga en annons med rätt medietyp till placeringen. |
| | Placeringen har inte tillräcklig budget. | Öka placeringsbudgeten för att tillåta offerter på inkommande begäranden. |
| | Flightdatumen för placeringen överlappar inte leveransdatumen för erbjudandet. | Redigera placeringens flygdatum efter behov. |
| [!UICONTROL Low Win Rate] | Placeringens högsta bud (golv eller fast) ligger under det minimiantal som krävs för erbjudandet. | Öka placeringens [!UICONTROL Max Bid] efter behov. |
| | I placeringen används filter som begränsar budgivning före bud. | Sänk tröskelvärdena för föranbudsfiltren så att fler budgivningar tillåts. |
| | Målgruppsanpassningen för placeringen är för restriktiv. | Kontrollera om de angivna målgruppsmålen har tillräckligt många aktiva användare och utöka målgruppen om möjligt. |

>[!MORELIKETHIS]
>
>* [Typer av prestandarapporter i Campaign Management-vyer](campaign-reports-about.md)
>* [Hantera dina kampanjdatavyer](campaign-data-views-manage.md)
