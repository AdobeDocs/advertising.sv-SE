---
title: Om insikter
description: Läs om prestandainsikter med visualiseringar.
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: a098e99f26a4e7d472d4a391d2cd465fc8d4255b
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---

# Om insikter

*Beta-funktion*

Prestandainsikter på hög nivå med visualiseringar ger er den information ni behöver för att optimera era era kampanjer och upptäcka nya möjligheter att skala upp resultatet. Ni kan visa data för olika kampanjer för en viss annonser eller gå ned på en lägre nivå.

Använd resultatinsikter för att

* Spåra långsiktiga trender för strategisk planering och välgrundat beslutsfattande.

* Identifiera möjligheter för att uppnå bättre resultat.

* Förbättra effektiviteten genom att minska tiden mellan att hämta rådata och få åtgärdbara insikter.

Du kan exportera alla visualiseringar för en flik till en PDF-fil eller hämta data för en viss insikt utan visualiseringar i Microsoft Excel-kalkylbladsformat (XLSX).

Du kan också [ändra datumintervallet, konfigurera vyn och spara en anpassad vy](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} på samma sätt som du kan för kampanjhanteringsvyer.

## Typer av insikter

### Fliken [!UICONTROL Home]

Fliken [!UICONTROL Home] innehåller viktiga värden för standard, prestanda och visningsbarhet för alla annonserarens kampanjer. Som standard visas information om korsvis placering för en viss annonsörer och anpassade mål. Du kan också konfigurera filter så att de visar data för en annan annonsörer, ett annat anpassat mål eller en viss placering. <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. --> Insikterna är:

* **[!UICONTROL Trends]:** Ett trenddiagram för tre kundspecificerade mätvärden (som standard, [!UICONTROL Net Spend], [!UICONTROL Impressions] och [!UICONTROL Net CPM]).

* **[!UICONTROL Delivery Breakdown]:** En uppdelning av data för specifika mått efter tre kundspecificerade dimensioner, t.ex. efter kampanj, utgivare och medietyp. För varje flerdimensionell uppdelning kan du välja ett annat mått.

### Fliken [!UICONTROL Household Reach]

Fliken [!UICONTROL Household Reach] tillhandahåller hushållens räckvidd för alla annonserarens kampanjer. Som standard visas data för olika kampanjer. Du kan också konfigurera filter så att de visar data för en annan annonsörer, för en viss kampanj, för flera paket eller placeringar eller för ett visst paket eller en viss placering. Några av insikterna:

* **[!UICONTROL Trends]:** Ett trenddiagram per dag eller vecka för tre kundspecificerade mått (som standard, [!UICONTROL Net Spend], [!UICONTROL Unique Reach] och [!UICONTROL Net CPM]).

* **[!UICONTROL Incremental Household Reach]:** Ett donutdiagram som visar den inkrementella hushållsräckvidden av [!UICONTROL Media Type], [!UICONTROL Device Type] eller [!UICONTROL Inventory Type]. *Inkrementell hushållsräckvidd* definieras som ett hushåll som nås exklusivt via en enda medie-, enhets- eller lagertyp.

* **[!UICONTROL Reach Breakdown]:** Den inkrementella unika hushållsräckvidden jämfört med överlappande hushållsräckvidd av [!UICONTROL Media Type], [!UICONTROL Device Type] eller [!UICONTROL Inventory Type].

  *Inkrementell hushållsräckvidd* definieras som ett hushåll som nås exklusivt via en enda medie-, enhets- eller lagertyp. *Överlappande hushållsräckvidd* definieras som ett hushåll som nås av flera medie-, enhets- eller lagertyper.

* **[!UICONTROL Top Performers]:** Kampanjer, placeringar, paket, utgivare, webbplatser/appar, medietyper, inventeringstyper eller enhetstyper som utförts av [!UICONTROL Unique Reach], [!UICONTROL Net Spend] och [!UICONTROL Cost per Reach].

* **[!UICONTROL Performance Analysis]:** [!UICONTROL Cost per Reach] och [!UICONTROL Net Spend] efter paket, utgivare eller webbplats/app. Använd den här insikten för att se vilka paket, utgivare eller webbplatser/appar som visar på potentialen för ökad räckvidd.

  Storleken på varje bubbla indikerar det inkrementella nålspåret, med större bubblor som indikerar en högre inkrementell räckvidd i genomsnitt. Håll markören över bubblan om du vill se det fullständiga enhetsnamnet och nyckelmåtten för en bubbla.

  Effektnivåerna är följande:

   * **Hög effekt:** Överväg att öka budgeten.
   * **Måttlig effekt**
   * **Begränsad påverkan:** Behöver åtgärdas

### Fliken [!UICONTROL Household Conversion]

Fliken [!UICONTROL Household Conversion] innehåller hushållskonverteringsvärden för alla annonserarens kampanjer <!-- active only? -->. Som standard visas data för olika kampanjer för en viss annonsörer och ett specifikt konverteringsmått. Du kan också konfigurera filter så att de visar data för en annan annonsörer eller konverteringsmått, för en viss kampanj, för olika paket eller placeringar, eller för ett visst paket eller en viss placering. Några av insikterna:

* **[!UICONTROL Trends]:** Ett trenddiagram per dag eller vecka för tre kundspecificerade mått (som standard, [!UICONTROL Net Spend], [!UICONTROL Conversions] och [!UICONTROL Net CPM]).

* **[!UICONTROL Conversion Participation Overview]:** Ett stapeldiagram som visar vilka medietyper, lagertyper och enhetstyper som resulterar i de flesta hushållskonverteringar.

  Impressioner som levereras inom uppslagsperioden (30 dagar) anses giltiga för konverteringsdeltagande.

* **[!UICONTROL Top Performers]:** En tabell över kampanjer, paket, placeringar, utgivare, webbplatser/appar, medietyper och lagertyper som ökar prestandan för tre kundspecificerade mätvärden (som standard, [!UICONTROL Net Spend], [!UICONTROL CPA] och [!UICONTROL Conversions]). Den översta utföraren visas först.

* **[!UICONTROL Performance Analysis]:** [!UICONTROL CPA] och [!UICONTROL Net Spend] efter paket, utgivare eller webbplats/app. Använd den här insikten för att se vilka paket, utgivare eller webbplatser/appar som visar på potentialen för ökad räckvidd.

  Storleken på varje bubbla indikerar det inkrementella nålspåret, med större bubblor som indikerar en högre inkrementell räckvidd i genomsnitt. Håll markören över bubblan om du vill se det fullständiga enhetsnamnet och nyckelmåtten för en bubbla.

  Effektnivåerna är följande:

   * **Hög effekt:** Överväg att öka budgeten.
   * **Måttlig effekt**
   * **Begränsad påverkan:** Behöver åtgärdas

## Open Performance Insights

* (Om du vill öppna insikter för alla kampanjer) Klicka på **[!UICONTROL Insights BETA]** på huvudmenyn.

* (Om du vill öppna insikter för en viss kampanj, ett visst paket eller en viss placering) Klicka [!UICONTROL Campaigns] > [!UICONTROL Packages] bredvid enhetsnamnet i vyn [!UICONTROL Placements], **[!UICONTROL ...]** eller **[!UICONTROL Insights]**.

## Använda filter på en tabb

1. Klicka på knappen ![Filter](/help/dsp/assets/filter.png) i verktygsfältet högst upp på fliken.

1. I den vänstra kolumnen väljer du en dimension och sedan ett eller flera värden i den högra kolumnen, beroende på vad som är tillämpligt.

   Du kan bara välja en annonsörer åt gången.

1. Klicka på **[!UICONTROL Apply]**.

1. (Valfritt) Om du vill begränsa data ytterligare väljer du enhetstypen i verktygsfältet och väljer sedan ett specifikt enhetsvärde (en kampanj, ett paket eller en placering).

## Ändra den rapporterade Dimension-versionen för en insight

* Välj dimension i listrutan till det övre vänstra hörnet av insikten.

## Ändra rapporterade värden för en insight

För konverteringsstatistik finns stöd för både Adobe Advertising-spårade och Adobe Analytics-spårade konverteringar.

1. Klicka på ![Målinställningar](/help/dsp/assets/metric-settings.png "Målinställningar") i det övre högra hörnet av insikten.

1. Markera mätvärdena och klicka sedan på **[!UICONTROL Apply]**.

## Exportera alla visualiseringar för en flik till en PDF-fil

* Ovanför fliken klickar du på **[!UICONTROL ...]** > **[!UICONTROL Export]**.

  Filen sparas i webbläsarens standardmapp för nedladdningar.

## Hämta en specifik insikt till en XLSX-fil

* Klicka på ![Hämta](/help/creative/assets/download.png "Hämta") i det övre högra hörnet av insikten.

  Filen sparas i webbläsarens standardmapp för nedladdningar.

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Typer av prestandarapporter i kampanjhanteringsvyer](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
>* [Hantera dina kampanjdatavyer](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
