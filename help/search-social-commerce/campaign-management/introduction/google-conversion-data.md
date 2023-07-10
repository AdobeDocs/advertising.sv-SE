---
title: '''[!DNL Google Ads] konverteringsdata'
description: Läs mer om de olika typerna av [!DNL Google Ads]-spårade konverteringsdata finns i Sök, Socialt och Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
source-git-commit: 29cda72cac949663cd2df822cf7223335a14504d
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# [!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel

Sök, sociala medier och handel synkroniseras automatiskt [!DNL Google Ads]-spårade konverteringsdata för alla era kampanjer på [!DNL Google Ads] söknings- och shoppingnätverk i söknings-, sociala och handelsmässiga nätverk för rapportering och optimering.

Alla mätvärden är automatiskt tillgängliga i era kampanjhanteringsvyer och grundläggande rapporter, och är också tillgängliga för användning i portföljmål för optimering.

## Tillgängliga konverteringsdata

Sök, Socialt och e-handel synkroniserar data för konverteringar som[!DNL Include in 'Conversions']&quot; är aktiverat, de senaste 35 dagarna hämtas data och data ändras dagligen med 09:00-10:00 i annonsörens tidszon. Historiska data kan ändras från dag till dag när nya konverteringar spåras för varje klick.

Upp till tre transaktionsegenskaper för varje [[!DNL Google Ads]-spårad konvertering](https://support.google.com/google-ads/answer/4677036) (som du konfigurerar i [!DNL Google Ads]) är automatiskt tillgängliga i Sök, Socialt och Commerce med hjälp av de konverteringsnamn som konfigurerats i [!DNL Google Ads]. Transaktionsegenskaperna för varje konvertering inkluderar:

* `GGL*` — (När du spårar det) Konverteringsvärdet för nyckelordet, med början med &quot;GGL&quot;-prefixet (till exempel GL Purchase).

* `GGL_CT*` — Antal konverteringar (antal), med början med prefixet &quot;GGL_CT&quot; (till exempel GGL_CT_Purchase).

* `GGL_XD_CT*` — (När det är tillgängligt för konverteringstypen, när du spårar dem) Antal (antal) konverteringar mellan enheter, enligt Google, med början med prefixet &quot;GGL_XD_CT_&quot; (till exempel GGL_XD_CT_Purchase).

[!DNL Google Ads] registrerar varje konvertering med [budenhet](/help/search-social-commerce/glossary.md#a-b), enhet och klicka på datumet (inte konverteringsdatumet). Attribution is based on default attribution setting for each metric in [!DNL Google Ads]; Adobe Advertising-attribuering beaktas inte eftersom klickdata inte är tillgängliga.

>[!NOTE]
>
>* Om du har flera konton med samma konverteringsnamn kan du se duplicerade konverteringsnamn i Adobe Advertising. Om detta inträffar, [ändra visningsnamnet](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) för en av de dubblerade mätvärdena i [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Rapporteringen är inte korrekt när två olika mätvärden har samma namn.
>* Data på anbudsenhetsnivå matchar data i [!DNL Google Ads] på samma nivå. Men [!DNL Google Ads]&#39; egna konverteringsdata för högre nivåer kan innehålla ytterligare konverteringar som inte är kopplade till de underordnade budenheterna. Data i Sök, Socialt, &amp; Commerce samlas alltid in från anbudsenhetsnivån, så en kampanjnivårapport kanske inte har samma summor som en kampanjnivårapport i Google Ads.
>* Datavariansen är vanligtvis mindre efter morgonsynkroniseringen än den är senare under dagen, när ytterligare konverteringar ännu inte har synkroniserats. Vi rekommenderar att vi validerar data om morgonen.
>* Konverteringsdata är inte tillgängliga för [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App]och [!DNL YouTube] annonser. Filtrera ut den typen av annonser när du jämför data i [!DNL Google Ads] med data i sökningar, sociala medier och handel.
>* Data för [!DNL Google Ads] konverteringar är inte tillgängliga på målgrupps- eller geografisk platsnivå och används därför inte för automatisk optimering av RLSA och platsbudsjusteringar.

## Hur man jämför konverteringsdata i [!DNL Google Ads] med data i sökningar, sociala medier och handel

Om du jämför data i sökning, sociala medier och handel med data i [!DNL Google Ads]använder du alternativet view eller report för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

Använd följande rapportinställningar för att validera jämförbara data.

### Rapportinställningar att använda i [!DNL Google Ads]

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

### Rapportinställningar som ska användas i sökning, sociala medier och handel

I Sök, Socialt, &amp; Commerce använder du alternativet view eller report för att visa konverteringar baserat på klickdatumet (inte transaktionsdatumet).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create Report]** håller du markören över **[!UICONTROL Basic Reports]** och klicka sedan på **[!UICONTROL Search Engine Account Report]**.

1. I [!UICONTROL Report Settings] anger du följande rapportinställningar:

   1. I **[!UICONTROL Conversions Based]** väljer du **[!UICONTROL Click date]**.

   1. Ange samma datumintervall som du använde för [!DNL Google Ads] rapport.

   1. I **[!UICONTROL Search/Content]** avsnitt, markera **[!UICONTROL Search Only]**.

   1. I **[!UICONTROL Search Engine Hierarchy]** -avsnittet, expandera [!UICONTROL Google Adwords] och välj kontot.

   1. Öppna [!UICONTROL Columns] och lägga till [!DNL Google Ads] mätvärden (med början från &quot;GGL&quot;) som du vill jämföra.

1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Översikt över att implementera annonsnätverkskonton och -kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera resultatet för era annonsnätverkskampanjer](monitor-performance-campaigns.md)
>* [Visa transaktionsegenskaper som spårats för en annonsörer](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
