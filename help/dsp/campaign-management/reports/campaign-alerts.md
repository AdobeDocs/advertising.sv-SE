---
title: Visa aviseringar
description: Lär dig hur du visar aviseringar och rekommenderade lösningar för kampanjer och kampanjkomponenter.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Visa aviseringar

*Betafunktion*

DSP hjälper er att identifiera när någon av era kampanjer eller kampanjkomponenter har problem. För varje problem skapar DSP en varning med en tidsstämpel och den rekommenderade åtgärden för att lösa problemet. Orsaker till varningar är konfigurationsproblem (t.ex. när inga annonser är kopplade till en placering eller när ett avtal har ställts in på fel sätt), annonsrefusering och kampanjhälsoproblem (t.ex. dålig annonsleverans eller prestanda). Aviseringar finns på kampanj-, paket-, annons- och avtalsnivå.

Aviseringar finns på följande platser:

* A [!UICONTROL Pulse Panel] ikonen i [!UICONTROL Campaigns], [!UICONTROL Packages] och paketinformation, [!UICONTROL Placements]och [!UICONTROL Ads] vyer visar om det finns några varningar tillgängliga för objekten i den vyn. När ikonen har en blå punkt (![Ikonen för panelen Pulser när det finns varningsmeddelanden](/help/dsp/assets/alerts-panel.png "Ikonen för panelen Pulser när det finns varningsmeddelanden")) finns det varningsmeddelanden. När ingen punkt är synlig (![Ikonen för panelen Pulse när det inte finns några tillgängliga varningar](/help/dsp/assets/alerts-panel-empty.png "Ikonen för panelen Pulse när det inte finns några tillgängliga varningar")) finns inga varningsmeddelanden.

* Datatabellerna i samma vy innehåller en[!UICONTROL Alerts]&quot; som anger när objektet - eller dess komponenter - har ett problem. Aviseringsindikatorerna innehåller&quot;Kritisk&quot; (![Kritisk](/help/dsp/assets/indicator-critical.png "Kritisk")), &quot;Warning&quot; (![Varning](/help/dsp/assets/indicator-warning.png "Varning")) och &quot;Information&quot; (![Information](/help/dsp/assets/indicator-information.png "Information")).

Du kan öppna den relevanta kampanjhanteringsvyn för alla aviseringar så att du kan redigera inställningarna efter behov för att lösa problemet.

Du kan också välja att ignorera en enskild varning, vilket tar bort den från dialogrutan [!UICONTROL Pulse] -panelen.

Varningar och varningsindikatorer försvinner automatiskt när de underliggande problemen löses.

## Visa aviseringar i dialogrutan [!UICONTROL Pulse Panel]

1. Klicka på **[!UICONTROL Campaigns]**.

1. Gör något av följande:

   * (För alla aviseringar som gäller för vyn) Klicka på ![Ikonen för panelen Pulser när det finns varningsmeddelanden](/help/dsp/assets/alerts-panel.png "Ikonen för panelen Pulser när det finns varningsmeddelanden").

   * (För alla aviseringar för en viss kampanj) Klicka på varningsindikatorn för en kampanjrad och klicka sedan på **[!UICONTROL View in Pulse panel]**.

   * (För alla varningar för ett visst paket, en viss placering eller en viss annons) Gör följande:

      1. Klicka på kampanjnamnet.

      1. Klicka på **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, eller **[!UICONTROL Ads]** för att öppna den relevanta kampanjkomponentvyn.

      1. Klicka på varningsindikatorn för ett paket, en placering eller en annonsrad och klicka sedan på **[!UICONTROL View in Pulse Panel]**.

   Alla varningar som är kopplade till kampanjen och dess komponenter, inklusive riktade avtal, listas. Som standard listas viktiga aviseringar först.

1. (Valfritt) Om du vill gruppera aviseringarna efter deras första identifieringsdatum eller om du vill filtrera aviseringarna efter aviseringsstatus, komponentstatus, komponenttyp eller med ett visst kampanjnamn klickar du på ![Filterknapp](/help/dsp/assets/filter.png) i panelens övre högra hörn markerar du filteralternativen och klickar sedan på **[!UICONTROL Apply]**.

1. Om du vill visa en lista över alla kampanjkomponenter som påverkas för en viss typ av avisering klickar du på aviseringsnamnet, till exempel &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Om du vill visa information för varje påverkad komponent, inklusive rekommenderad åtgärd, klickar du på [!UICONTROL EXPAND ALL] eller klicka på komponentnamnet. Om du vill öppna den relevanta kampanjhanteringsvyn för en påverkad komponent så att du kan göra de rekommenderade ändringarna håller du markören över komponentnamnet och klickar på ![Gå till vyn](/help/dsp/assets/go-to-view.png "Gå till vyn").

1. (Valfritt) Om du vill ignorera (dölja) en varning håller du markören över komponentnamnet och klickar på ![Ignorera](/help/dsp/assets/alert-ignore.png "Ignorera")och klicka sedan på **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

Du har några sekunder på dig att ångra åtgärden efter att du ignorerat en varning. När alternativmeddelandet stängs kan du inte avbryta åtgärden.

1. (Valfritt) Om du vill hämta ignorerade aviseringar filtrerar du aviseringarna så att en [!UICONTROL Alert Status] av &quot;[!UICONTROL All]&quot; eller &quot;[!UICONTROL Ignored].&quot; Om du vill avaktivera en varning håller du markören över komponentnamnet och klickar på ![Ignorera](/help/dsp/assets/alert-un-ignore.png "Ignorera").

## Stäng [!UICONTROL Pulse Panel]

* Klicka på till höger om verktygsfältet ![Ikonen för panelen Pulser när det finns varningsmeddelanden](/help/dsp/assets/alerts-panel.png "Ikonen för panelen Pulser när det finns varningsmeddelanden") eller ![Ikonen för panelen Pulse när det inte finns några tillgängliga varningar](/help/dsp/assets/alerts-panel-empty.png "Ikonen för panelen Pulse när det inte finns några tillgängliga varningar").

>[!MORELIKETHIS]
>
>* [Typer av prestandarapporter i Campaign Management-vyer](campaign-reports-about.md)
