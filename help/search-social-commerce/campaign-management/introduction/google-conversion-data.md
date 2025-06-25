---
title: '[!DNL Google Ads] konverteringsdata'
description: Lär dig mer om de  [!DNL Google Ads] spårade konverteringsdata som finns i Sök, Socialt och Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# [!DNL Google Ads] konverteringsdata i sökningar, sociala medier och Commerce

Search, Social och Commerce synkroniserar automatiskt [!DNL Google Ads]-spårade konverteringsdata för alla dina kampanjer i söknings- och shoppingnätverket i [!DNL Google Ads] till Search, Social och Commerce för rapportering och optimering.

Alla mätvärden är automatiskt tillgängliga i era kampanjhanteringsvyer och grundläggande rapporter, och är också tillgängliga för användning i portföljmål för optimering.

## Tillgängliga konverteringsdata

Sök, Socialt och Commerce synkroniserar data för konverteringar där alternativet [!DNL Include in 'Conversions'] har aktiverats, hämtar data för de senaste 35 dagarna och drar sedan ändringar av data dagligen med 09:00-10:00 i annonsörens tidszon. Historiska data kan ändras från dag till dag när nya konverteringar spåras för varje klick.

Upp till tre mätvärden för varje [[!DNL Google Ads]-spårad konvertering ](https://support.google.com/google-ads/answer/4677036) (som du har konfigurerat i [!DNL Google Ads]) är automatiskt tillgängliga i Sök, Socialt och Commerce, med hjälp av konverteringsnamnen som har konfigurerats i [!DNL Google Ads]. Mätvärdena för varje konvertering är:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (När du spårar det) Konverteringsvärdet för nyckelordet, med början med GL-prefixet (till exempel GL Purchase).

* `GGL_CT*` - Antal konverteringar (antal), med början med prefixet &quot;GGL_CT&quot; (till exempel GGL_CT_Purchase).

* `GGL_XD_CT*` — (När det är tillgängligt för konverteringstypen, när du spårar dem) Antalet (antalet) konverteringar mellan enheter, enligt Google, med början med prefixet &quot;GGL_XD_CT_&quot; (till exempel GGL_XD_CT_Purchase).

[!DNL Google Ads] registrerar varje konvertering med [budenhet](/help/search-social-commerce/glossary.md#a-b), enhet och klickningsdatum (inte konverteringsdatum). Attribution baseras på standardattribueringsinställningen för varje mätvärde i [!DNL Google Ads]. Adobe Advertising-attribuering beaktas inte eftersom klickhändelsenivådata inte är tillgängliga.

>[!NOTE]
>
>* Om du har flera konton med samma konverteringsnamn kan du se duplicerade konverteringsnamn i Adobe Advertising. Om detta inträffar [ändrar du visningsnamnet ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) för en av de dubblerade måtten i [!UICONTROL Admin] > [!UICONTROL Conversions]. Rapporteringen är inte korrekt när två olika mätvärden har samma namn.
>* Data på anbudsenhetsnivå matchar data i [!DNL Google Ads] på samma nivå. [!DNL Google Ads] egna konverteringsdata för högre nivåer kan dock innehålla ytterligare konverteringar som inte har tilldelats de underordnade budenheterna. Data i Sök, Social och Commerce samlas alltid in från anbudsenhetsnivån, så till exempel har en kampanjnivårapport kanske inte samma summor som en kampanjnivårapport i Google Ads.
>* Datavariansen är vanligtvis mindre efter morgonsynkroniseringen än den är senare under dagen, när ytterligare konverteringar ännu inte har synkroniserats. Vi rekommenderar att vi validerar data om morgonen.
>* Konverteringsdata är inte tillgängliga för [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] och [!DNL YouTube] annonser. Filtrera ut de här annonstyperna när du jämför data i [!DNL Google Ads] med data i Sök, Socialt och Commerce.
>* Data för [!DNL Google Ads]-konverteringar är inte tillgängliga på målgrupps- eller geografisk platsnivå och används därför inte för automatisk optimering av RLSA och platsbudsjusteringar.

## Hur du jämför konverteringsdata i [!DNL Google Ads] med data i Sök, Socialt och Commerce

Om du jämför data i Sök, Socialt och Commerce med data i [!DNL Google Ads] kan du använda vy- eller rapportalternativet för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

Använd följande rapportinställningar för att validera jämförbara data.

### Rapportinställningar som ska användas i [!DNL Google Ads]

Generera rapporten för de valda konverteringsåtgärderna per dag och inkludera data för alla annonsstatusar.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Rapportinställningar som ska användas i sökningar, sociala medier och Commerce

I Sök, Socialt och Commerce kan du använda vy- eller rapportalternativet för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Report]** i verktygsfältet ovanför datatabellen, håll markören över **[!UICONTROL Basic Reports]** och klicka sedan på **[!UICONTROL Search Engine Account Report]**.

1. I fönstret [!UICONTROL Report Settings] anger du följande rapportinställningar:

   1. I avsnittet **[!UICONTROL Conversions Based]** på väljer du **[!UICONTROL Click date]**.

   1. Ange samma datumintervall som du använde för rapporten [!DNL Google Ads].

   1. Välj **[!UICONTROL Search Only]** i avsnittet **[!UICONTROL Search/Content]**.

   1. Expandera avsnittet [!UICONTROL Google Adwords] i avsnittet **[!UICONTROL Search Engine Hierarchy]** och markera kontot.

   1. Öppna fliken [!UICONTROL Columns] och lägg till de [!DNL Google Ads]-mått (som börjar med GGL) som du vill jämföra.

1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Översikt över implementering av annonsnätverkskonton och kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera prestandan för annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Visa konverteringsstatistik som spårats för en annonsörer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Skapa en konverteringstagg för [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
