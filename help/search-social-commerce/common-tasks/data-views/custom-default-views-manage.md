---
title: Hantera standardvyer och anpassade vyer
description: Lär dig hur du anpassar standardvyer och anpassade vyer.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 399974645b5083e735ff7aa94eba0a1115b4ddeb
workflow-type: tm+mt
source-wordcount: '4453'
ht-degree: 0%

---

# Hantera standardvyer och anpassade vyer

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Med standardvyer och anpassade vyer kan du anpassa prestandadata som visas i datavyer för sökkampanjer. Visningsinställningarna innehåller de kolumner som ska inkluderas, filter, datumintervall, konverteringsattribueringsinställningar och andra avancerade inställningar. Du kan antingen tillämpa inställningarna tillfälligt eller spara dem. (Undantag: Du kan inte spara filter för standardvyer.) Varje anpassad standardvy och standardvy gäller endast för en viss vy (till exempel [!UICONTROL Portfolios] eller [!UICONTROL Campaigns]) och ett specifikt annonserarkonto. I det äldre användargränssnittet kan varje universell anpassad vy användas för entitetsvy för en viss annonsörer och kan därför inte innehålla egenskapskolumner (som entitetsnamn eller status), som varierar beroende på entitetstyp.

Standardvyer visas som standard varje gång du loggar in. Du kan skapa ytterligare anpassade vyer och använda dem när du vill. Du kan också dela en anpassad vy som du skapar med alla andra användare som kan visa annonsörens data. Det är bara den person som skapar en anpassad vy som kan ta bort den.

I det äldre användargränssnittet är varje vy tillgänglig som en genväg i avsnittet [!UICONTROL Custom Views] i den vänstra panelen.

## Använda en standardvy eller anpassad vy

### (Nytt användargränssnitt) Använda en standardvy eller anpassad vy i en hanteringsvy

1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

1. Klicka på någon av flikarna ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] och [!UICONTROL From Others]) för att leta upp vyn.

1. Håll markören över vynamnet och klicka på **[!UICONTROL Apply]**.

### (Äldre användargränssnitt) Använd en standardvy eller anpassad vy för en kampanjhanteringsvy

* (Standardvyer) Klicka på **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **\[enhetstyp\]** på undermenyerna.

* (Anpassade vyer) Från den vänstra navigeringspanelen:

   1. Klicka på menyn **[!UICONTROL Custom Views]** i den vänstra panelen för att expandera den.

      Vyer sorteras efter lämplig enhet.

   1. Expandera de tillgängliga menyerna.

      [!UICONTROL Universal Views] innehåller anpassade vyer som kan användas i alla entitetsvyer. Alla andra anpassade vyer grupperas efter entitetstyp.

   1. Klicka på vynamnet.

      Om vyn är universell eller gäller för den aktuella enheten visas datatabellen på nytt enligt visningskonfigurationen. Om vyn gäller för en annan enhet visas data för den tillämpliga enheten enligt vykonfigurationen.

## Skapa en anpassad vy {#create-custom-view}

>[!NOTE]
>
>Förutom de visningsinställningar som du anger för den anpassade vyn sparas även den aktuella kolumnsorteringsordningen.

### (Nytt användargränssnitt) Skapa en anpassad vy från en hanteringsvy

*Tillgängligt i vyerna [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] och [!UICONTROL Ad Groups]*

Anpassade vyer är specifika för en enskild vy (till exempel vyn [!UICONTROL Portfolios]).

1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

1. Klicka på **[!UICONTROL Create View]**.

1. Ange [anpassade visningsinställningar](#view-settings-new-ui).

1. Spara vyn:

   * Klicka på **[!UICONTROL Save & Apply]** om du vill spara vyn och använda den.

   * Om du vill spara vyn utan att använda den klickar du på **[!UICONTROL Save]**.

### (Äldre användargränssnitt) Skapa en anpassad vy från en kampanjhanteringsvy

Anpassade vyer kan bara användas för kampanjhanteringsvyer.

1. Klicka på namnet på den aktuella vyn (som kan vara [!UICONTROL Default]) till höger om verktygsfältet ovanför datatabellen.

1. Ange [anpassade visningsinställningar](#view-settings).

1. Klicka på **[!UICONTROL Save as New]**.

1. Ange namnet på den nya vyn och klicka sedan på **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Använd ett namn som hjälper dig att identifiera fliken och den information som den gäller för (till exempel&quot;Pausade kampanjer&quot; eller&quot;Top 50 Ads&quot;).

## Redigera en standardvy eller anpassad vy {#view-edit}

### (Nytt användargränssnitt) Redigera en standardvy eller anpassad vy

*Tillgängligt i vyerna [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] och [!UICONTROL Ad Groups]*

1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

1. Klicka på någon av flikarna ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] och [!UICONTROL From Others]) för att leta upp vyn.

1. Håll markören över vynamnet och klicka på ![Redigera](/help/search-social-commerce/assets/edit-new.png).

1. Redigera [anpassade visningsinställningar](#view-settings-new-ui).

1. Spara vyn:

   * Om du vill spara ändringarna utan att tillämpa dem klickar du på **[!UICONTROL Save]**.

   * Om du vill spara ändringarna och använda dem klickar du på **[!UICONTROL Apply]**.<!-- Should be Save & Apply -->

### (Äldre användargränssnitt) Redigera en standardvy eller anpassad vy

1. Öppna visningsinställningarna:

   * (Om du redan har använt vyn) Klicka på den aktuella vyns namn till höger om verktygsfältet ovanför datatabellen (som kan vara [!UICONTROL Default]).

   * (Anpassade vyer som inte används) Klicka på ![Anpassade vyer](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Anpassade vyer") i den vänstra panelen för att utöka menyn [!UICONTROL Custom Views]. Klicka på den anpassade vyns namn.

1. Redigera [visningsinställningarna](#view-settings).

   >[!NOTE]
   >
   >Du kan tillämpa men inte spara ändringar på filter i standardinställningarna för vyn.

1. Använd eller spara inställningarna:

   * Om du vill använda inställningarna tillfälligt utan att spara dem i vyn klickar du på **[!UICONTROL Apply]**.

     Inställningarna används på fliken tills du flyttar bort från hanteringsvyn på den översta nivån eller (om tillämpligt) [visar data för en annan annonsör](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (För standardvyer och anpassade vyer som du har skapat) Om du vill spara inställningarna i den aktuella vyn klickar du på **[!UICONTROL Save]**.

   * Klicka på **[!UICONTROL Save As]** om du vill spara inställningarna i en ny anpassad vy. I fönstret [!UICONTROL Enter New Custom View Name] anger du namnet på den nya vyn och klickar sedan på **[!UICONTROL Save]**.

## (Nytt användargränssnitt) Klona en standardvy eller anpassad vy {#view-clone}

*Tillgängligt i vyerna [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] och [!UICONTROL Ad Groups]*

1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

1. Klicka på någon av flikarna ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] och [!UICONTROL From Others]) för att leta upp vyn.

1. Håll markören över vynamnet och klicka på ![Klona](/help/search-social-commerce/assets/clone-new.png).

1. Ange ett nytt vynamn och redigera de [anpassade vyinställningarna](#view-settings-new-ui) efter behov.

1. Spara vyn:

   * Klicka på **[!UICONTROL Save & Apply]** om du vill spara vyn och använda den.

   * Om du vill spara vyn utan att använda den klickar du på **[!UICONTROL Save]**.

## Återställa en standardvy till systemets standardinställningar

Om du återställer standardinställningarna för vyn tas alla inställningar som du har sparat bort och standardinställningarna för systemet används igen.

Systemets standardinställningar varierar beroende på hanteringsvy. För de flesta hanteringsvyer visar systemets standardvy data för föregående dag för objekt i aktiverade konton och som är aktiva (t.ex. endast aktiva annonsgrupper i aktiva kampanjer), med data sorterade efter kostnad och med konverteringsdata baserade på transaktionsdatum.

* Från det nya användargränssnittet:

   1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

   1. Klicka på någon av flikarna ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] och [!UICONTROL From Others]) för att leta upp vyn.

   1. Håll markören över vynamnet och klicka på ![Återställ](/help/search-social-commerce/assets/revert-new.png).

* Från de äldre vyerna för kampanjhantering:

   1. Klicka på ![Anpassade vyer](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "anpassade vyer") i den vänstra panelen för att utöka menyn [!UICONTROL Custom Views].

      Vyer sorteras efter lämplig enhet.

   1. Klicka på ![Återställ till standardinställningar](/help/search-social-commerce/assets/restore.png "Återställ till standardinställningar") bredvid visningsnamnet.

## Ta bort en anpassad vy

Du kan ta bort alla anpassade vyer som du har skapat.

Om du tar bort en anpassad vy som används på den aktuella fliken fortsätter fliken att visa den anpassade vyn tills du går utanför vyuppsättningen (t.ex. från vyer på menyn [!UICONTROL Search] till menyn [!UICONTROL Reports]) eller (när det är tillämpligt) när du [visar data för en annan annonsör](/help/search-social-commerce/common-tasks/change-advertiser.md).

* Från det nya användargränssnittet:

   1. Ovanför datatabellen klickar du på namnet på den vy som används för tillfället (![Visa](/help/search-social-commerce/assets/view.png "Visa")).

   1. Klicka på någon av flikarna ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] och [!UICONTROL From Others]) för att leta upp vyn.

   1. Håll markören över vynamnet och klicka på ![Ta bort](/help/search-social-commerce/assets/delete-new.png).

   1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

* Från de äldre vyerna för kampanjhantering:

   1. Klicka på ![Anpassade vyer](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "anpassade vyer") i den vänstra panelen för att utöka menyn [!UICONTROL Custom Views].

   1. Håll markören över det anpassade vynamnet och klicka sedan på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort").

   1. Klicka på **[!UICONTROL Continue]** i bekräftelsemeddelandet.

## Inställningar för standardvy och anpassad vy

<!-- Simplify attribution rule definitions here and elsewhere and include links to "How attribution rules are calculated -->

### (Nytt användargränssnitt) Standardinställningar och anpassade visningsinställningar {#view-settings-new-ui}

| **Tabb** | **Fält** | **Beskrivning** |
| --- | --- | --- |
| [Över alla flikar] | Namn | Ett unikt namn för vyn. Du kan inte redigera namnet på en standardvy.<p><b>Tips!</b> Använd ett namn som hjälper dig att identifiera fliken och den information som den gäller för (till exempel&quot;Pausade kampanjer&quot; eller&quot;Top 50 Ads&quot;). |
|   | Dela med andra användare | (Endast anpassade vyer, valfritt) Gör vyn tillgänglig för alla andra användare som kan visa annonsörens data. Andra användare kan inte redigera eller ta bort vyn, men de kan skapa en ny vy från inställningarna. |
| Kolumner | Markerade kolumner och ordning | Kolumner med data som visas och deras ordning:<ul><li> (Om du vill lägga till en kolumn) Klicka på ett kolumnnamn i listan Tillgängliga kolumner och dra det sedan till listan Valda kolumner och ordning eller klicka på ![högerpilen](/help/search-social-commerce/assets/chevron-right.png) för att flytta den dit.</li><li>(Om du vill ändra den vågräta placeringen för en kolumn) Klicka på kolumnnamnet i listan Markerade kolumner och ordning och dra sedan kolumnnamnet till önskad position eller klicka på ![uppilen](/help/search-social-commerce/assets/chevron-up.png) eller ![nedpilen](/help/search-social-commerce/assets/chevron-down.png) för att flytta den dit. Namnet på den övre kolumnen visas i den vänstra kolumnen.</li><li>(Om du vill ta bort en kolumn) Klicka på ett kolumnnamn i listan Valda kolumner och ordning och dra det sedan till listan Tillgängliga kolumner eller klicka på ![vänsterpil](/help/search-social-commerce/assets/chevron-left.png) för att flytta den dit.</li></ul><b>Filtrera data</b><p>Om du bara vill visa en viss typ av data klickar du på någon av ikonerna bredvid listan:<ul><li>![egenskapsikonen](/help/search-social-commerce/assets/properties-icon-new.png) för egenskapsnamn och ID:n, till exempel [!UICONTROL Portfolio Name] eller [!UICONTROL Status]</li><li>![trafikikon](/help/search-social-commerce/assets/traffic-metrics-icon-new.png) för standardtrafikstatistik, t.ex. visningar och klickningar</li><li>![intäktsikon](/help/search-social-commerce/assets/revenue-metrics-icon-new.png) (för konverteringsstatistik som spårats för annonseraren, inklusive konverterings- och webbplatsengagemangsstatistik som synkroniserats med Analytics)</li><li>![anpassad ikon](/help/search-social-commerce/assets/custom-metrics-icon-new.png) (för anpassade mått som skapats av annonseraren)</li><li>![klassificeringsikon](/help/search-social-commerce/assets/classifications-icon-new.png) (för etikettklassificeringar).</li></ul> <b>Ytterligare information:</b><ul><li>Mer information om hur du lägger till, skapar eller redigerar nya mått finns i [Skapa ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md), [Redigera ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) och [Ta bort ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md).</li><li>Om rapporten innehåller data för konton med olika valutor inkluderas inte summor för penningmängdsbaserade kolumner (till exempel Kostnad och CPC).</li><li>Du kan [tillfälligt redigera kolumnuppsättningen från kolumnrubrikmenyn](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) och [redigera och sortera kolumnuppsättningen från [!UICONTROL Columns] -ikonen](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Kolumnikon](/help/search-social-commerce/assets/custom-columns.png "Kolumnikon")).</li></ul> |
|   | Sortera efter | Den kolumn som data ska sorteras efter. Standardvärdet är olika för varje rapporttyp. |
|   | Sorteringsordning | Om data ska sorteras i **stigande** eller **fallande** ordning. |
| Filter | [Filterdefinitioner] | (Valfritt) Filter som ska användas på data. När du använder filter returneras bara rader när värdet för en kolumn uppfyller angivna villkor.<p>För varje filter som ska användas:<ol><li>Välj ett kolumnnamn på menyn [!UICONTROL Add Filter]. Listan innehåller alla tillgängliga kolumner och sorteras efter kolumntyp, med egenskapskolumner först.</li><li>Definiera filtret i kolumnen</li></ol>(Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde. Värden är inte skiftlägeskänsliga.<p>Om du till exempel har markerat kolumnen&quot;Klickningar&quot; och bara vill returnera rader med fler än 100 klick, väljer du _\>_ och anger `100` i indatafältet.<p>Beroende på datatypen kan tillgängliga operatorer innehålla <i>större än</i>, <i>mindre än</i>, <i>lika</i>, <i>innehåller</i>, <i>inte innehåller</i>, <i>börjar med</i>, <i>slutar med</i>,<i>inget värde</i> eller <i> 6&rbrace;har värde</i> <i>före</i>, <i>efter</i> eller <i>inget datum</i>.<p>(Filter utan inmatningsfält) Klicka på ![pilen nedåt](/help/search-social-commerce/assets/arrow-down-expand.png) bredvid menyn Välj listalternativ och markera sedan kryssrutorna intill varje värde som ska inkluderas.<p><b>Anteckningar:</b><ul><li>Du kan tillämpa men inte spara ändringar på filter i standardinställningarna för vyn.</li><li>Du kan också [tillfälligt ändra tillämpliga filter](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) i vyn.</li></ul> |
| Ytterligare inställningar | Datumintervall | (När Inkludera datumintervall är markerat)<p>Datumintervallet som data ska genereras för. Välj ett alternativ:<ul><li><i>[Förinställt intervall]</i>: En lista med vanliga tidsintervall, från <i>I dag</i> till <i>De senaste 180 dagarna</i>. Välj ett alternativ i listan. Standardvärdet är <i>Gårdagen</i>. Obs! <i>Senaste månaden</i>, <i>De senaste tre månaderna</i> och <i>De senaste sex månaderna</i> visar data för de föregående kalendermånaderna.</li><li><i>Anpassat datumintervall:</i> Ange startdatum och slutdatum. Ange datum i formatet MM/DD/ÅÅÅÅ eller M/D/ÅÅÅÅ, eller klicka på ![kalenderikonen](/help/search-social-commerce/assets/calendar.png) bredvid ett fält och välj ett datum.</li></ul> |
|   | Jämförelse | Jämför data för det angivna datumintervallet med data för ett andra datumintervall. När du väljer det här alternativet anger du det andra datumintervallet. Två extra kolumner läggs till för varje vanlig datakolumn. I stället för att ta med bara en kolumn för &quot;Impressions&quot;, innehåller rapporten kolumner för &quot;Impressions Range 1&quot;, &quot;Impressions Range 2&quot; och &quot;Impressions Difference&quot;.<p><b>Anteckningar:</b><ul><li>Skillnadskolumnen visas inte för härledda mått.</li><li>Rapporter som jämför stora datumintervall kan ta längre tid att generera.</li></ul> |
|   | Jämförelseformat | (När [!UICONTROL Comparison] är aktiverat) Hur du uttrycker skillnaden mellan data i de två markerade datumintervallen i kolumnen [_Differens i datafältet_]. Välj ett alternativ:<ul><li><i>Varians</i> (standard): Visar skillnaden som ett numeriskt värde.</li><li><i>% ändring</i>: Visar skillnaden i procent.</li></ul> |
|   | Attributregel | (Annonsörer med Adobe Advertising pixelbaserade konverteringsspårningstjänst) På fliken kan du se hur man attribuerar konverteringsdata - eventuellt i flera annonskanaler och portföljer - i en serie händelser som leder till konvertering. Som standard är regeln som anges i inställningarna för konverteringsattribuering på annonsörnivå vald.<ul><li> <i>Första händelsen</i>: Attribuerar konverteringen till det första betalda klicket i serien inom annonsörens klickningsfönster eller, om inga betalda klick inträffade, till det sista intrycket i annonsörens visningsfönster.</li><li><i>Viktad första händelse, mer</i>: Attribuerar konverteringen till alla händelser i serien som inträffade i annonsörens fönster för klickning och visningssökning, men ger den största vikten till den första händelsen och har en successivt mindre vikt till följande händelser. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Jämn fördelning</i>: Attribuerar konverteringen lika till alla händelser i serien som inträffade i annonserarens fönster för klickning och visningssökning. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Viktning av senaste händelse Mer</i>: Attribuerar konverteringen till alla händelser i serien som inträffade i annonserarens fönster för klickning och visningssökning, men ger den största vikten till den senaste händelsen och har en successivt mindre vikt än föregående händelser. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Senaste händelse</i> (standard): Attribuerar konverteringen till den senaste betalda klickningen i serien inom annonsörens fönster för klickning eller, om inga betalda klick inträffade, till det senaste intrycket i annonsörens fönster för visningssökning.</li><li><i>U-formad</i>: Attributerar konverteringen till alla händelser i serien som inträffade i annonserarens fönster för klicksökning och visningssökning, men ger den största vikten till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringsbanan. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li></ul><p><b>Anteckningar:</b><ul><li>Alla attribueringsregler förutom Last Event är bara tillgängliga för annonsörer med Adobe Advertising klickspårning och konverteringsspårning från antingen Adobe Advertising eller Adobe Analytics (med en Analytics-integrering).</li><li>Attributregler gäller för klick på betalda annonser i alla kanaler. De gäller inte för visningar av betalda sökannonser, som inte kan spåras på eventnivå.</li><li>När du rapporterar konverteringsdata med någon attribueringsregel förutom en av reglerna för&quot;senaste händelse&quot;, kan händelserna som leder konverteringen inträffa i flera portföljer. I så fall inkluderar vyn endast data för konverteringen när annonserna eller nyckelorden i portföljerna inkluderas i vyn.</li><li>För standardvyer rekommenderar vi att du behåller standardregeln för attribuering, som används för att beräkna det [objektiva värdet](/help/search-social-commerce/glossary.md#o-p) (kallades tidigare&quot;viktad intäkt&quot;) för varje anbudsenhet under anbudsoptimeringen.</li></ul> |
|   | Konverteringar baserade på | Rapportera konverteringsdata:<ul><li><i>Klicka på datum</i>: Om du vill visa transaktioner som har skapats av ett klick som inträffade under den angivna tidsperioden. När en portfölj har en avsevärd fördröjning mellan klick och transaktioner är det här alternativet användbart för att beräkna den historiska intäkten per klick för portföljen, vilket anger de intäktsbeteenden som ska förväntas över tid.</li><li><i>Transaktionsdatum</i> (standard): Om du vill visa transaktioner vars transaktionsdatum inträffade under den angivna tidsperioden. Detta visar hur mycket intäkt som intjänats under den angivna tidsperioden.</li></ul> |

### (Äldre användargränssnitt) Standardinställningar och anpassade visningsinställningar {#view-settings}

| **Tabb** | **Fält** | **Beskrivning** |
| --- | --- | --- |
| [Över alla flikar] | Namn | Ett unikt namn för vyn. Du kan inte redigera namnet på en standardvy.<p><b>Tips!</b> Använd ett namn som hjälper dig att identifiera fliken och den information som den gäller för (till exempel&quot;Pausade kampanjer&quot; eller&quot;Top 50 Ads&quot;). |
|   | Universell vy | (Skrivskyddat för befintliga vyer) Gör datainställningarna tillgängliga i alla entitetsvyer (för Campaigns, Ads och så vidare). Universella vyer kan innehålla kolumnerna för mått och etikett, men inte egenskapskolumner (som entitetsnamn och status) eftersom de skiljer sig åt beroende på entitetstyp, samt alla andra visningsattribut. Alla filtervillkor tillämpas på enhetsvyn när de är tillämpliga och ignoreras i annat fall. Alla måttfilter utvärderas lokalt (för till exempel klick \> 1000 visar kampanjvyerna kampanjer med över 1000 klick, och i annonsgruppsvyn visas annonsgrupper med över 1000 klick).<p>Egenskapskolumnerna för en universell vy hämtas från enhetens standardvy. Du kan ändra standardegenskapskolumnerna för en viss enhet i standardvyinställningarna.<p>När du har aktiverat eller inaktiverat det här alternativet kan du inte spara ändringen i den befintliga vyn utan skapa en ny vy med ändringen. |
|   | Dela | (Endast befintliga anpassade vyer, valfritt) Gör vyn tillgänglig för alla andra användare som kan visa annonsörens data. Andra användare kan inte redigera eller ta bort vyn, men de kan skapa en ny vy från inställningarna. I visningslistorna är varje vy som en annan person delar kursiv, t.ex. _Kampanjer som presterar bäst_. |
| Kolumner | Markerade kolumner och ordning | Kolumner med data som visas och deras ordning:<ul><li> (Om du vill lägga till en kolumn) Klicka på ett kolumnnamn i listan Tillgängliga kolumner och dra det sedan till listan Valda kolumner och ordning eller klicka på ![högerpilen](/help/search-social-commerce/assets/chevron-right.png) för att flytta den dit.</li><li>(Om du vill ändra den vågräta placeringen för en kolumn) Klicka på kolumnnamnet i listan Markerade kolumner och ordning och dra sedan kolumnnamnet till önskad position eller klicka på ![uppilen](/help/search-social-commerce/assets/chevron-up.png) eller ![nedpilen](/help/search-social-commerce/assets/chevron-down.png) för att flytta den dit. Namnet på den övre kolumnen visas i den vänstra kolumnen.</li><li>(Om du vill ta bort en kolumn) Klicka på ett kolumnnamn i listan Valda kolumner och ordning och dra det sedan till listan Tillgängliga kolumner eller klicka på ![vänsterpil](/help/search-social-commerce/assets/chevron-left.png) för att flytta den dit.</li></ul><b>Filtrera data</b><p>Om du bara vill visa en viss typ av data klickar du på någon av ikonerna bredvid listan:<ul><li>![egenskapsikon](/help/search-social-commerce/assets/properties-icon.png) för egenskapsnamn och ID:n för sökkomponenter, till exempel Status</li><li>![trafikikon](/help/search-social-commerce/assets/traffic-metrics-icon.png) för standardtrafikstatistik, t.ex. visningar och klickningar</li><li>![intäktsikon](/help/search-social-commerce/assets/revenue-metrics-icon.png) (för konverteringsstatistik som spårats för annonseraren, inklusive konverterings- och webbplatsengagemangsstatistik som synkroniserats med Analytics)</li><li>![anpassad ikon](/help/search-social-commerce/assets/custom-metrics-icon.png) (för anpassade härledda värden som skapats av annonseraren)</li><li>![klassificeringsikon](/help/search-social-commerce/assets/classifications-icon.png) (för etikettklassificeringar).</li></ul> <b>Ytterligare information:</b><ul><li>Mer information om hur du lägger till, skapar eller redigerar nya mått finns i [Skapa ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md), [Redigera ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) och [Ta bort ett anpassat mått](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md).</li><li>Om rapporten innehåller data för konton med olika valutor inkluderas inte summor för penningmängdsbaserade kolumner (till exempel Kostnad och CPC).</li><li>Du kan [tillfälligt redigera kolumnuppsättningen från kolumnrubrikmenyn](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) och [redigera och sortera kolumnuppsättningen från [!UICONTROL Columns] -ikonen](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Kolumnikon](/help/search-social-commerce/assets/custom-columns.png "Kolumnikon")).</li></ul> |
|   | Sortera efter | Den kolumn som data ska sorteras efter. Standardvärdet är olika för varje rapporttyp. |
|   | Sorteringsordning | Om data ska sorteras i **stigande** eller **fallande** ordning. Välj ett alternativ genom att flytta skjutreglaget. |
| Filter | [Filterdefinitioner] | (Valfritt) Filter som ska användas på data. När du använder filter returneras bara rader när värdet för en kolumn uppfyller angivna villkor.<p>För varje filter som ska användas:<ol><li>Välj ett kolumnnamn på menyn [!UICONTROL Add Filter]. Listan innehåller alla tillgängliga kolumner och sorteras efter kolumntyp, med egenskapskolumner först.</li><li>Definiera filtret i kolumnen</li></ol>(Filter med indatafält) Välj en operator på den andra menyn och ange sedan önskat värde. Värden är inte skiftlägeskänsliga.<p>Om du till exempel har markerat kolumnen&quot;Klickningar&quot; och bara vill returnera rader med fler än 100 klick, väljer du _\>_ och anger `100` i indatafältet.<p>Beroende på datatypen kan tillgängliga operatorer innehålla <i>större än</i>, <i>mindre än</i>, <i>lika</i>, <i>innehåller</i>, <i>inte innehåller</i>, <i>börjar med</i>, <i>slutar med</i>,<i>inget värde</i> eller <i> 6&rbrace;har värde</i> <i>före</i>, <i>efter</i> eller <i>inget datum</i>.<p>(Filter utan inmatningsfält) Klicka på ![pilen nedåt](/help/search-social-commerce/assets/arrow-down-expand.png) bredvid menyn Välj listalternativ och markera sedan kryssrutorna intill varje värde som ska inkluderas.<p><b>Anteckningar:</b><ul><li>Du kan tillämpa men inte spara ändringar på filter i standardinställningarna för vyn.</li><li>Du kan också [tillfälligt ändra tillämpliga filter](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) i vyn.</li></ul> |
|   | Inkludera rader med enbart prestandadata | (Endast annonsgrupper, nyckelord, produktgrupper, placeringar och automatiska målvyer) <p>Inkluderar endast rader med prestandadata under de angivna datumen. Som standard är det här alternativet markerat för att minska sidans inläsningstid. <p><b>Varning</b>: Om du avmarkerar alternativet och vyn innehåller många entiteter utan prestandadata tar det längre tid att visa data.<p> <b>Obs!</b> Du kan tillämpa men inte spara ändringar på filter i standardinställningarna för vyn. Standardvyer visar alltid bara enheter med prestandadata. |
| Datum | Datumintervall | (När Inkludera datumintervall är markerat)<p>Datumintervallet som data ska genereras för. Välj ett alternativ:<ul><li><i>[Förinställt intervall]</i>: En lista med vanliga tidsintervall, från <i>I dag</i> till <i>De senaste 180 dagarna</i>. Välj ett alternativ i listan. Standardvärdet är <i>Gårdagen</i>. Obs! <i>Senaste månaden</i>, <i>De senaste tre månaderna</i> och <i>De senaste sex månaderna</i> visar data för de föregående kalendermånaderna.</li><li><i>Anpassat datumintervall:</i> Ange startdatum och slutdatum. Ange datum i formatet MM/DD/ÅÅÅÅ eller M/D/ÅÅÅÅ, eller klicka på ![kalenderikonen](/help/search-social-commerce/assets/calendar.png) bredvid ett fält och välj ett datum.</li></ul> |
|   | Jämförelse | Jämför data för det angivna datumintervallet med data för ett andra datumintervall. När du väljer det här alternativet anger du det andra datumintervallet. Två extra kolumner läggs till för varje vanlig datakolumn. I stället för att ta med bara en kolumn för &quot;Impressions&quot;, innehåller rapporten kolumner för &quot;Impressions Range 1&quot;, &quot;Impressions Range 2&quot; och &quot;Impressions Difference&quot;.<p><b>Anteckningar:</b><ul><li>Skillnadskolumnen visas inte för härledda mått.</li><li>Rapporter som jämför stora datumintervall kan ta längre tid att generera.</li></ul> |
|   | Jämförelseformat | (När [!UICONTROL Comparison] är aktiverat) Hur du uttrycker skillnaden mellan data i de två markerade datumintervallen i kolumnen [_Differens i datafältet_]. Välj ett alternativ:<ul><li><i>Varians</i> (standard): Visar skillnaden som ett numeriskt värde.</li><li><i>% ändring</i>: Visar skillnaden i procent.</li></ul> |
| Ytterligare inställningar | Använd standard | Tillämpar de attribueringsinställningar som anges i konverteringsattribueringsinställningarna på annonsörnivå. |
|   | Attributregel | (Annonsörer med Adobe Advertising pixelbaserade konverteringsspårningstjänst) På fliken kan du se hur man attribuerar konverteringsdata - eventuellt i flera annonskanaler och portföljer - i en serie händelser som leder till konvertering. Som standard är regeln som anges i inställningarna för konverteringsattribuering på annonsörnivå vald.<ul><li> <i>Första händelsen</i>: Attribuerar konverteringen till det första betalda klicket i serien inom annonsörens klickningsfönster eller, om inga betalda klick inträffade, till det sista intrycket i annonsörens visningsfönster.</li><li><i>Viktad första händelse, mer</i>: Attribuerar konverteringen till alla händelser i serien som inträffade i annonsörens fönster för klickning och visningssökning, men ger den största vikten till den första händelsen och har en successivt mindre vikt till följande händelser. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Jämn fördelning</i>: Attribuerar konverteringen lika till alla händelser i serien som inträffade i annonserarens fönster för klickning och visningssökning. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Viktning av senaste händelse Mer</i>: Attribuerar konverteringen till alla händelser i serien som inträffade i annonserarens fönster för klickning och visningssökning, men ger den största vikten till den senaste händelsen och har en successivt mindre vikt än föregående händelser. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li><li><i>Senaste händelse</i> (standard): Attribuerar konverteringen till den senaste betalda klickningen i serien inom annonsörens fönster för klickning eller, om inga betalda klick inträffade, till det senaste intrycket i annonsörens fönster för visningssökning.</li><li><i>U-formad</i>: Attributerar konverteringen till alla händelser i serien som inträffade i annonserarens fönster för klicksökning och visningssökning, men ger den största vikten till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringsbanan. När konverteringen föregås av både betalda klick och visningar används den angivna intrycksåsidosättningsvikten ytterligare på avtrycken. När konverteringen föregås av endast avtryck vägs avtrycken enligt annonsörens genomsiktsvikt i stället för att tryckets vikt åsidosätts.</li></ul><p><b>Anteckningar:</b><ul><li>Alla attribueringsregler förutom Last Event är bara tillgängliga för annonsörer med Adobe Advertising klickspårning och konverteringsspårning från antingen Adobe Advertising eller Adobe Analytics (med en Analytics-integrering).</li><li>Attributregler gäller för klick på betalda annonser i alla kanaler. De gäller inte för visningar av betalda sökannonser, som inte kan spåras på eventnivå.</li><li>När du rapporterar konverteringsdata med någon attribueringsregel förutom en av reglerna för&quot;senaste händelse&quot;, kan händelserna som leder konverteringen inträffa i flera portföljer. I så fall inkluderar vyn endast data för konverteringen när annonserna eller nyckelorden i portföljerna inkluderas i vyn.</li><li>För standardvyer rekommenderar vi att du behåller standardregeln för attribuering, som används för att beräkna det [objektiva värdet](/help/search-social-commerce/glossary.md#o-p) (kallades tidigare&quot;viktad intäkt&quot;) för varje anbudsenhet under anbudsoptimeringen.</li></ul> |
|   | Konverteringar baserade på | Rapportera konverteringsdata:<ul><li><i>Klicka på datum</i>: Om du vill visa transaktioner som har skapats av ett klick som inträffade under den angivna tidsperioden. När en portfölj har en avsevärd fördröjning mellan klick och transaktioner är det här alternativet användbart för att beräkna den historiska intäkten per klick för portföljen, vilket anger de intäktsbeteenden som ska förväntas över tid.</li><li><i>Transaktionsdatum</i> (standard): Om du vill visa transaktioner vars transaktionsdatum inträffade under den angivna tidsperioden. Detta visar hur mycket intäkt som intjänats under den angivna tidsperioden.</li></ul> |
