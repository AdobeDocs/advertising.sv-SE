---
title: '''[!DNL Microsoft® Advertising] konverteringsdata'
description: Läs mer om olika typer av [!DNL Microsoft® Advertising]-spårade konverteringsdata finns i Sök, Socialt och Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: f119876669e226d75376535b801c57da9590ac72
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] konverteringsdata i sökning, sociala medier och handel

Alla konverteringar som spåras av din [[!DNL Microsoft® Advertising] UET-taggar (Universal Event tracking)](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) för webbkonverteringar, inklusive genomskinliga konverteringar, för rapportering och optimering.

Alla mätvärden är automatiskt tillgängliga i era kampanjhanteringsvyer och grundläggande rapporter, och är också tillgängliga för användning i portföljmål för optimering av [!DNL Microsoft® Advertising] kampanjer.

## Tillgängliga konverteringsdata

Sök, Socialt och e-handel synkroniserar data för konverteringar som[!DNL Include in 'Conversions']&quot; är aktiverat, de senaste 35 dagarna hämtas data och data ändras dagligen med 09:00-10:00 i annonsörens tidszon. Historiska data kan ändras från dag till dag när nya konverteringar spåras för varje klick.

Två mätvärden för varje [[!DNL Microsoft® Advertising]-spårad konvertering](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (som du konfigurerar i [!DNL Microsoft® Advertising]) är automatiskt tillgängliga i Sök, Socialt och Commerce med hjälp av de konverteringsnamn som konfigurerats i [!DNL Microsoft® Advertising]. Mätvärdena för varje konvertering är:

* `<conversion-name>` — Konverteringsvärdet för nyckelordet (till exempel Köp).

  >[!TIP]
  >
  >Använd den här typen av konverteringsmått i målet för portföljer som innehåller [!DNL Microsoft® Advertising] kampanjer med budstrategierna Max Conversion Value och Target ROAS.

* `CT_<conversion-name>` — Antal konverteringar (antal), med början med prefixet &quot;CT_&quot; (till exempel CT_Purchase).

  >[!TIP]
  >
  >Använd den här typen av konverteringsmått i målet för portföljer som innehåller [!DNL Microsoft® Advertising] kampanjer med budstrategierna Max Conversions och Target CPA.

Data är tillgängliga baserat på klickningstiden och baserat på konverterings-/transaktionstiden från det datum då funktionen är aktiverad för kontot.

[!DNL Microsoft® Advertising] registrerar varje konvertering med [budenhet](/help/search-social-commerce/glossary.md#a-b), enhet och klicka på datumet (inte konverteringsdatumet). Attribution is based on default attribution setting for each metric in [!DNL Microsoft® Advertising]; Adobe Advertising-attribuering är inte indelad eftersom klickdata inte är tillgängliga.

>[!NOTE]
>
>* Om du har flera konton med samma konverteringsnamn kan du se duplicerade konverteringsnamn i Adobe Advertising. Om detta inträffar, [ändra visningsnamnet](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) för en av de dubblerade mätvärdena i [!UICONTROL Admin] > [!UICONTROL Conversions]. Rapporteringen är inte korrekt när två olika mätvärden har samma namn.
>* Data på anbudsenhetsnivå matchar data i annonsnätverket på samma nivå. Annonsnätverkets egna konverteringsdata för högre nivåer kan dock innehålla ytterligare konverteringar som inte är kopplade till de underordnade budenheterna. Data i Sök, Socialt, &amp; Commerce samlas alltid in från nivån för budenheter, så en kampanjnivårapport kanske inte har samma summor som en kampanjnivårapport i annonsnätverket.
>* Datavariansen är vanligtvis mindre efter morgonsynkroniseringen än den är senare under dagen, när ytterligare konverteringar ännu inte har synkroniserats. Vi rekommenderar att vi validerar data om morgonen.
>* Data är inte tillgängliga på målgrupps- eller geografisk platsnivå och används därför inte för automatisk optimering av RLSA och platsbudsjusteringar.

## Hur man jämför konverteringsdata i [!DNL Microsoft® Advertising] med data i sökningar, sociala medier och handel

Använd följande rapportinställningar för att validera jämförbara data.

### Rapportinställningar att använda i [!DNL Microsoft® Advertising]

Generera rapporten för de valda konverteringsåtgärderna per dag och inkludera data för alla annonsstatusar.

### Rapportinställningar som ska användas i sökning, sociala medier och handel

I Sök, Socialt, &amp; Commerce använder du alternativet view eller report för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create Report]** håller du markören över **[!UICONTROL Basic Reports]** och klicka sedan på **[!UICONTROL Search Engine Account Report]**.

1. I [!UICONTROL Report Settings] anger du följande rapportinställningar:

   1. I **[!UICONTROL Conversions Based]** väljer du **[!UICONTROL Click date]**.

   1. Ange samma datumintervall som du använde för [!DNL Microsoft® Advertising] rapport.

   1. I **[!UICONTROL Search/Content]** avsnitt, markera **[!UICONTROL Search Only]**.

   1. I **[!UICONTROL Search Engine Hierarchy]** -avsnittet expanderar du [!UICONTROL Microsoft® Advertising] och välj kontot.

   1. Öppna [!UICONTROL Columns] och lägga till [!DNL Microsoft® Advertising] mätvärden som du vill jämföra.

1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Översikt över att implementera annonsnätverkskonton och -kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera resultatet för era annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
