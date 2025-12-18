---
title: Visa aviseringar
description: Lär dig hur du visar aviseringar och rekommenderade lösningar för kampanjer och kampanjkomponenter.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 9ab8d3345659f48d1d131c3c6c1e1b87f0b0a0e6
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Visa aviseringar

DSP hjälper er att identifiera när era kampanjer eller kampanjkomponenter har problem. För varje problem skapar DSP en avisering med en tidsstämpel och den rekommenderade åtgärden för att lösa problemet. Orsaker till varningar är konfigurationsproblem (t.ex. när inga annonser är kopplade till en placering eller när ett avtal har ställts in på fel sätt), annonsrefusering och kampanjhälsoproblem (t.ex. dålig annonsleverans eller prestanda). Aviseringar finns på kampanj-, paket-, annons- och avtalsnivå.

Aviseringar finns på följande platser:

* En [!UICONTROL Pulse Panel]-ikon i vyerna [!UICONTROL Campaigns], [!UICONTROL Packages] och paketinformation, [!UICONTROL Placements] och [!UICONTROL Ads] anger om det finns några varningar tillgängliga för objekten i den vyn. Om ikonen har en blå punkt (![Pulse Panel-ikon när varningar är tillgängliga](/help/dsp/assets/alerts-panel.png "Pulse Panel-ikon när varningar är tillgängliga")) är varningar tillgängliga. Om ingen punkt är synlig (![Ikonen för panelen Pulse när det inte finns några tillgängliga varningar](/help/dsp/assets/alerts-panel-empty.png "Ikonen för panelen Pulse när det inte finns några tillgängliga varningar")) är inga varningar tillgängliga.

* Datatabellerna i samma vyer innehåller en [!UICONTROL Alerts]-kolumn som anger när objektet - eller dess komponenter - har problem. Varningsindikatorerna innehåller&quot;Kritisk&quot; (![Kritisk](/help/dsp/assets/indicator-critical.png "Kritisk")),&quot;Varning&quot; (![Varning](/help/dsp/assets/indicator-warning.png "Varning")) och&quot;Information&quot; (![Information](/help/dsp/assets/indicator-information.png "Information")).

Du kan öppna den relevanta kampanjhanteringsvyn för alla aviseringar så att du kan redigera inställningarna efter behov för att lösa problemet.

Du kan också välja att ignorera en enskild varning, vilket tar bort den från panelen [!UICONTROL Pulse].

Varningar och varningsindikatorer försvinner automatiskt när de underliggande problemen löses.

## Visa aviseringar i [!UICONTROL Pulse Panel]

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Gör något av följande:

   * (För alla aviseringar som gäller för vyn) Klicka på ![Pulse Panel-ikonen till höger om verktygsfältet i en kampanjhanteringsvy när det finns tillgängliga aviseringar](/help/dsp/assets/alerts-panel.png "Pulse Panel-ikonen när aviseringar är tillgängliga").

   * (För alla aviseringar för en viss kampanj) Klicka på varningsindikatorn för en kampanjrad och klicka sedan på **[!UICONTROL View in Pulse panel]**.

   * (För alla varningar för ett visst paket, en viss placering eller en viss annons) Gör följande:

      1. Klicka på kampanjnamnet.

      1. Klicka på **[!UICONTROL Packages]**, **[!UICONTROL Placements]** eller **[!UICONTROL Ads]** på undermenyn för att öppna den relevanta kampanjkomponentvyn.

      1. Klicka på varningsindikatorn för ett paket, en placering eller en annonsrad och klicka sedan på **[!UICONTROL View in Pulse Panel]**.

   Alla varningar som är kopplade till kampanjen och dess komponenter, inklusive riktade avtal, listas. Som standard listas viktiga aviseringar först.

1. (Annonsörer med Advertising Creative; valfritt) Klicka på fliken **[!UICONTROL Creative]** om du vill visa aviseringar om placeringar som innehåller Advertising Creative-upplevelser.

1. (Valfritt) Om du vill gruppera aviseringarna efter deras första identifieringsdatum, eller om du vill filtrera aviseringarna efter aviseringsstatus, komponentstatus, komponenttyp eller med ett specifikt kampanjnamn, klickar du på ![Filterknapp](/help/dsp/assets/filter.png) i panelens övre högra hörn, väljer filteralternativen och klickar sedan på **[!UICONTROL Apply]** .

1. Om du vill visa en lista över alla kampanjkomponenter som påverkas för en viss larmtyp klickar du på varningsnamnet, till exempel [!UICONTROL Package: No Active Placement (*N*)]. Om du vill visa information för varje berörd komponent, inklusive den rekommenderade åtgärden, klickar du på [!UICONTROL EXPAND ALL] eller på komponentnamnet. Om du vill öppna den relevanta kampanjhanteringsvyn för en påverkad komponent så att du kan göra de rekommenderade ändringarna håller du markören över komponentnamnet och klickar på ![Gå till vy](/help/dsp/assets/go-to-view.png "Gå till vy").

1. (Valfritt) Om du vill ignorera (dölja) en varning håller du markören över komponentnamnet och klickar på ![Ignorera](/help/dsp/assets/alert-ignore.png "Ignorera"). Klicka sedan på **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]** eller **[!UICONTROL Ignore indefinitely]**.

Du har några sekunder på dig att ångra åtgärden efter att du ignorerat en varning. När alternativmeddelandet stängs kan du inte avbryta åtgärden.

1. (Valfritt) Om du vill hämta ignorerade aviseringar filtrerar du aviseringarna så att en [!UICONTROL Alert Status] av [!UICONTROL All] eller [!UICONTROL Ignored] visas. Om du vill ignorera en varning håller du markören över komponentnamnet och klickar på ![Ångra](/help/dsp/assets/alert-un-ignore.png "Ångra").

## Stäng [!UICONTROL Pulse Panel]

* Klicka på ikonen ![Pulse Panel (Pulse Panel) när varningar är tillgängliga](/help/dsp/assets/alerts-panel.png "Pulse Panel (Pulse Panel-ikon när varningar är tillgängliga)") eller ![Ikonen för panelen Pulse när det inte finns några tillgängliga varningar](/help/dsp/assets/alerts-panel-empty.png "Ikonen för panelen Pulse när det inte finns några tillgängliga varningar") till höger om verktygsfältet.

>[!MORELIKETHIS]
>
>* [Typer av prestandarapporter i kampanjhanteringsvyer](campaign-reports-about.md)
