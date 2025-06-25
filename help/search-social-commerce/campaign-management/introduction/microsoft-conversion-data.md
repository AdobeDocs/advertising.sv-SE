---
title: '[!DNL Microsoft Advertising] konverteringsdata'
description: Läs mer om de  [!DNL Microsoft Advertising] spårade konverteringsdata som finns i Sök, Socialt och Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] konverteringsdata i sökningar, sociala medier och Commerce

Sök, socialt och Commerce synkroniserar automatiskt alla konverteringar som spåras av dina [[!DNL Microsoft Advertising] UET-taggar](https://help.ads.microsoft.com/#apex/ads/en/53056) för att hitta webbplatskonverteringar, inklusive genomskinliga konverteringar, för rapportering och optimering.

Alla mätvärden är automatiskt tillgängliga i kampanjhanteringsvyer och grundläggande rapporter, och är också tillgängliga för användning i portföljmål för optimering av [!DNL Microsoft Advertising]-kampanjer.

## Tillgängliga konverteringsdata

Sök, Socialt och Commerce synkroniserar data för konverteringar där alternativet [!DNL Include in 'Conversions'] har aktiverats, hämtar data för de senaste 35 dagarna och drar sedan ändringar av data dagligen med 09:00-10:00 i annonsörens tidszon. Historiska data kan ändras från dag till dag när nya konverteringar spåras för varje klick.

Två mätvärden för varje [[!DNL Microsoft Advertising]-spårad konvertering ](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (som du har konfigurerat i [!DNL Microsoft Advertising]) är automatiskt tillgängliga i Sök, Socialt och Commerce, med hjälp av konverteringsnamnen som har konfigurerats i [!DNL Microsoft Advertising]. Mätvärdena för varje konvertering är:

* `<conversion-name>` - Konverteringsvärdet för nyckelordet (till exempel Köp).

  >[!TIP]
  >
  >Använd den här typen av konverteringsmått i målet för portföljer som innehåller [!DNL Microsoft Advertising] kampanjer med anbudsstrategierna Max konverteringsvärde och Target ROAS.

* `CT_<conversion-name>` - Antal konverteringar (antal), med början med prefixet &quot;CT_&quot; (till exempel CT_Purchase).

  >[!TIP]
  >
  >Använd den här typen av konverteringsmått i målet för portföljer som innehåller [!DNL Microsoft Advertising] kampanjer med budstrategierna Max Conversions och Target CPA.

Data är tillgängliga baserat på klickningstiden och baserat på konverterings-/transaktionstiden från det datum då funktionen är aktiverad för kontot.

[!DNL Microsoft Advertising] registrerar varje konvertering med [budenhet](/help/search-social-commerce/glossary.md#a-b), enhet och klickningsdatum (inte konverteringsdatum). Attribution baseras på standardattribueringsinställningen för varje mätvärde i [!DNL Microsoft Advertising]. Adobe Advertising-attribuering beaktas inte eftersom klickhändelsenivådata inte är tillgängliga.

>[!NOTE]
>
>* Om du har flera konton med samma konverteringsnamn kan du se duplicerade konverteringsnamn i Adobe Advertising. Om detta inträffar [ändrar du visningsnamnet ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) för en av de dubblerade måtten i [!UICONTROL Admin] > [!UICONTROL Conversions]. Rapporteringen är inte korrekt när två olika mätvärden har samma namn.
>* Data på anbudsenhetsnivå matchar data i annonsnätverket på samma nivå. Annonsnätverkets egna konverteringsdata för högre nivåer kan dock innehålla ytterligare konverteringar som inte är kopplade till de underordnade budenheterna. Data i Sök, Socialt och Commerce samlas alltid in från anbudsenhetsnivån, så en kampanjnivårapport kanske inte har samma summor som en kampanjnivårapport i annonsnätverket.
>* Datavariansen är vanligtvis mindre efter morgonsynkroniseringen än den är senare under dagen, när ytterligare konverteringar ännu inte har synkroniserats. Vi rekommenderar att vi validerar data om morgonen.
>* Data är inte tillgängliga på målgrupps- eller geografisk platsnivå och används därför inte för automatisk optimering av RLSA och platsbudsjusteringar.

## Hur du jämför konverteringsdata i [!DNL Microsoft Advertising] med data i Sök, Socialt och Commerce

Använd följande rapportinställningar för att validera jämförbara data.

### Rapportinställningar som ska användas i [!DNL Microsoft Advertising]

Generera rapporten för de valda konverteringsåtgärderna per dag och inkludera data för alla annonsstatusar.

### Rapportinställningar som ska användas i sökningar, sociala medier och Commerce

I Sök, Socialt och Commerce kan du använda vy- eller rapportalternativet för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Report]** i verktygsfältet ovanför datatabellen, håll markören över **[!UICONTROL Basic Reports]** och klicka sedan på **[!UICONTROL Search Engine Account Report]**.

1. I fönstret [!UICONTROL Report Settings] anger du följande rapportinställningar:

   1. I avsnittet **[!UICONTROL Conversions Based]** på väljer du **[!UICONTROL Click date]**.

   1. Ange samma datumintervall som du använde för rapporten [!DNL Microsoft Advertising].

   1. Välj **[!UICONTROL Search Only]** i avsnittet **[!UICONTROL Search/Content]**.

   1. Expandera avsnittet [!UICONTROL Microsoft Advertising] i avsnittet **[!UICONTROL Search Engine Hierarchy]** och markera kontot.

   1. Öppna fliken [!UICONTROL Columns] och lägg till de [!DNL Microsoft Advertising]-mått som du vill jämföra.

1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Översikt över implementering av annonsnätverkskonton och kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera prestandan för annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
