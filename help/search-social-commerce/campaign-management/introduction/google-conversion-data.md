---
title: "[!DNL Google Ads] konverteringsdata"
description: Läs mer om de olika typerna av [!DNL Google Ads]-spårade konverteringsdata finns i Sök, Socialt och Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel

Sök, sociala medier och handel synkroniseras automatiskt [!DNL Google Ads]-spårade konverteringsdata för alla era kampanjer på [!DNL Google Ads] söknings- och shoppingnätverk i söknings-, sociala och handelsmässiga nätverk för rapportering och optimering. Sök, Socialt och e-handel synkroniserar data för konverteringar som[!DNL Include in 'Conversions']&quot; är aktiverat, de senaste 30 dagarna hämtas data och data ändras sedan dagligen.

## Tillgängliga konverteringsdata

Upp till tre transaktionsegenskaper för varje [[!DNL Google Ads]-spårad konvertering](https://support.google.com/google-ads/answer/4677036) (som du konfigurerar i [!DNL Google Ads]) är automatiskt tillgängliga i Sök, Socialt och Commerce med hjälp av de konverteringsnamn som konfigurerats i [!DNL Google Ads]. Transaktionsegenskaperna för varje konvertering inkluderar:

* `GGL*` — (När du spårar det) Summan av konverteringsvärden för nyckelordet, med början med &quot;GGL&quot;-prefixet (till exempel GL Purchase).

* `GGL_CT*` — Antal konverteringar (antal), med början med prefixet &quot;GGL_CT&quot; (till exempel GGL_CT_Purchase).

* `GGL_XD_CT*` — (När det är tillgängligt för konverteringstypen, när du spårar dem) Antal (antal) konverteringar mellan enheter, enligt Google, med början med prefixet &quot;GGL_XD_CT_&quot; (till exempel GGL_XD_CT_Purchase).

Data är tillgängliga från det datum då funktionen aktiveras för kontot och uppdateras dagligen senast 09:00-10:00 i annonsörens tidszon.

[!DNL Google Ads] registrerar varje konvertering med [budenhet](/help/search-social-commerce/glossary.md#a-b), enhet och klicka på datumet (inte konverteringsdatumet). Attribution is based on default attribution setting for each metric in [!DNL Google Ads]; Attribuering med annonsering i Adobe är inte factot eftersom data på klickhändelsenivå inte är tillgängliga. Varje dag hämtas konverteringsdata för de senaste 30 dagarna från Sök, Sociala och Commerce och sedan beräknas inkrementella konverteringar sedan föregående dag med hjälp av klickdatumet från [!DNL Google Ads] och ange föregående dag som transaktionsdatum. Därför kan historiska data ändras från dag till dag när nya konverteringar spåras för varje klick. Om du jämför data i sökning, sociala medier och handel med data i [!DNL Google Ads], använder du vy- eller rapportalternativet för att visa &quot;[!UICONTROL Conversions by: Click date]&quot; (inte efter transaktionsdatum).

Alla mätvärden är automatiskt tillgängliga i era kampanjhanteringsvyer och grundläggande rapporter, och är också tillgängliga för användning i portföljmål för optimering.

>[!NOTE]
>
>* Om du har flera konton med samma konverteringsnamn kan du se duplicerade konverteringsnamn i Adobe Advertising. Om detta inträffar, [ändra visningsnamnet](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) för en av de dubblerade mätvärdena i [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Rapporteringen är inte korrekt när två olika mätvärden har samma namn.
>* Data på anbudsenhetsnivå matchar data i [!DNL Google Ads] på samma nivå. Men [!DNL Google Ads]&#39; egna konverteringsdata för högre nivåer kan innehålla ytterligare konverteringar som inte är kopplade till de underordnade budenheterna. Data i Sök, Socialt, &amp; Commerce samlas alltid in från anbudsenhetsnivån, så en kampanjnivårapport kanske inte har samma summor som en kampanjnivårapport i Google Ads.
>* Datavariansen är vanligtvis mindre efter morgonsynkroniseringen än den är senare under dagen, när ytterligare konverteringar ännu inte har synkroniserats. Vi rekommenderar att vi validerar data om morgonen.
>* Konverteringsdata är inte tillgängliga för [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App]och [!DNL YouTube] annonser. Filtrera ut den typen av annonser när du jämför data i [!DNL Google Ads] med data i sökningar, sociala medier och handel.
>* Data för [!DNL Google Ads] konverteringar är inte tillgängliga på målgrupps- eller geografisk platsnivå och används därför inte för automatisk optimering av RLSA och platsbudsjusteringar.


## Hur man jämför konverteringsdata i [!DNL Google Ads] med data i sökningar, sociala medier och handel

Använd följande rapportinställningar för att validera jämförbara data.

### Rapportinställningar att använda i [!DNL Google Ads]

1. Välj **[!DNL Reports]>[!DNL Report]**.

1. Välj **[!DNL + Custom]>[!DNL Table]**.

1. Ange rader och kolumner i rapporten i den vänstra rutan:

   1. Sök efter **[!DNL Day]** och drar till [!DNL Row] -avsnitt.

   1. Sök efter **[!DNL All conv].** och drar till [!DNL Column] -avsnitt.

   1. Sök efter **[!DNL Conversion action]** och drar till [!DNL Column] -avsnitt.

1. I verktygsfältet för rapportinställningar väljer du **[!DNL Filter]>[!DNL Ad status]** och markera sedan alla rutor.

1. I verktygsfältet för rapportinställningar väljer du **[!DNL Download]>[!DNL Excel .csv]**.

### Rapportinställningar som ska användas i sökning, sociala medier och handel

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
>* [Om kampanjhantering i Sök, Social och Commerce](campaign-management-about.md)
>* [Översikt över att implementera annonsnätverkskonton och -kampanjer](campaign-implemention-overview.md)
>* [Övervaka och hantera resultatet för era annonsnätverkskampanjer](monitor-performance-campaigns.md)

