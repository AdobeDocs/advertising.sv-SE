---
title: Om simuleringar
description: Lär dig mer om portföljsimuleringar.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Om simuleringar

*Beta-funktion*

Simuleringsrapporter visar det uppskattade marginalvärdet för kostnad-till-mål, kostnaden, antalet klick och det objektiva värde som du kan förvänta dig för en portfölj på olika utgiftsnivåer (kostnad) och motsvarande dagliga budgetar eller andra mål. Du kan anpassa vyn <!-- add link --> om du vill visa ytterligare trafikvärden, simuleringsinställningar och endast en viss simuleringstyp ([!UICONTROL Weekly] eller [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Simuleringstyper

* **Automatiserade veckosimuleringar:** Simuleringsrapporter körs automatiskt varje vecka med de aktuella portföljinställningarna. Automatiserade veckosimuleringar är bara tillgängliga för perioder där portföljen är [optimerad eller aktiv](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Varje veckovis simulering består av en arbetsbok. Varje arbetsbok innehåller målet för var och en av de 20 stegnivåerna samt prognostiserade kostnader, klick, viktade intäkter (objektivt värde) och konverteringsvärden som ingår i målet, baserat på motsvarande mål. Begränsningarna tillämpades inte för de första 20 dataraderna. Begränsningarna tillämpades för de återstående dataraderna.

* **Anpassade, användargenererade simuleringar:** Du kan skapa en anpassad simuleringsrapport för en enskild [optimerad eller aktiv](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)-portfölj med de aktuella portföljinställningarna eller använda anpassade portföljinställningar för att se resultatet som dessa inställningar skulle ge utan att ändra dem. Du kan till exempel skapa en anpassad simulering för att se effekten av att använda en annan utgiftsstrategi eller utbildningsbudget <!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. Du kan visa beräknade prestanda på portfölj-, kampanj-, offertenhets- och enhetsnivå. Anpassade simuleringar ärver begränsningsinställningen från portföljen.

  >[!NOTE]
  >
  > Det nya anpassade simuleringsformuläret använder samma inställningar som det äldre formuläret, förutom att det ärver begränsningsinformationen för budenheten från portföljinställningarna. Du har inte möjlighet att ignorera begränsningar för budenheter, som du gjorde på den gamla sidan med anpassade simuleringsinställningar.

  Varje hämtad anpassad simulering består av en arbetsbok. Varje arbetsbok innehåller ett kalkylblad för varje angiven entitetsnivå för simulering (portföljer, kampanjer, annonsgrupper, budenheter) när data finns tillgängliga för den nivån. När du anger data på enhetsnivå innehåller varje kalkylblad en [!UICONTROL Device]-kolumn. Varje kalkylblad innehåller en rad med data för varje tillämplig enhet och (när det anges för rapporten) och enhetstyp för varje 20 steg (till exempel en rad per kampanj). Data på varje rad innehåller beräknade marginalkostnader, kostnad, klick, viktade intäkter (objektivt värde), enhetstyp och konverteringsmått som ingår i målet, baserat på motsvarande mål. I kalkylbladet på portföljnivå ingår även målet för stegnivåerna, och i kalkylbladet på entitetsnivå ingår annonsnätverket, kontot, kampanjen och (när det är tillämpligt) annonskoncern.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## Vyn [!UICONTROL Simulations]

Vyn [!UICONTROL Simulations] visar veckosimuleringar och anpassade simuleringar. Administratören och vissa andra användartyper <!-- Verify which --> kan se anpassade simuleringar som skapats av andra användare. Alla andra användare kan bara se de anpassade simuleringar de skapar.

Datatabellen innehåller förloppet för varje simulering, en [!UICONTROL Target Midpoint]-kolumn som fylls i för varje rad och kolumner för kostnads-/intrycks-/klicknings-/objektiva värdeprognoser, faktiska värden och noggrannhet. Du kan också lägga till ytterligare anpassade kolumner (inklusive höjdvärden, till exempel faktiskt målvärde delat med kostnad).

### Tillgängliga åtgärder {#simulations-actions}

* [Anpassa vyn](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) så att den innehåller ytterligare mått, inklusive de uppskattade intrycken, den faktiska kostnaden, klick, exponeringar och det objektiva värdet, värdet för kostnad-till-mål, kostnadseffektiviteten, klicknoggrannheten och det objektiva värdet samt skillnaden (delta) mellan det förväntade och faktiska objektiva värdet och värdet för kostnad-till-mål. Du kan även inkludera kolumner för de flesta simuleringsinställningarna och simuleringstypen ([!UICONTROL Custom] eller [!UICONTROL Weekly]).

* [Generera eller kör om en anpassad simulering](simulation-create.md) för en enskild portfölj. Du kan antingen skapa en ny simulering eller återskapa en befintlig simulering i listan.

* [Hämta veckovisa och anpassade simuleringar](simulation-download.md) som [!DNL Microsoft Excel] arbetsböcker i ZIP-filer.

* Använd knappen [!UICONTROL Spend Planner] för att öppna det gamla verktyget för utgiftsrekommendation, som hjälper dig att identifiera den optimala utgiftsfördelningen mellan portföljer.

## God praxis

Övervaka simuleringsrapporter i följande situationer:

* Innan du startar en portfölj för att uppskatta den prestanda du kan förvänta dig med motsvarande portföljinställningar bör du använda minst två veckors data. Om simuleringsresultaten visar på lägre prestanda än du förväntade dig baserat på historiska data för de inkluderade kampanjerna bör du undersöka och lösa problemen innan du startar portföljen.

* Efter en större förändring av en portfölj, som att lägga till en kampanj eller ändra målet. Om du ändrar portföljens modellstartdatum, vikten för ett konverteringsmått eller klickvärdet för ett mål, väntar du tills efter 17:00 PST nästa dag för att köra simuleringen, när det finns uppdaterade kostnads- och intäktsmodeller tillgängliga.

* Övervaka med jämna mellanrum resultattrender på konverteringsmätnivå.

>[!MORELIKETHIS]
>
>* [Kör eller kör en simulering igen](simulation-create.md)
>* [Hämta simuleringar](simulation-download.md)
