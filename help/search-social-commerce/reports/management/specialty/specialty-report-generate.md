---
title: Generera en specialrapport
description: Lär dig hur du skapar en specialrapport.
exl-id: 5edf7b11-37ae-4488-962a-7b4f50e7c569
feature: Search Reports, Search Specialty Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Generera en specialrapport

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create Report]** håller du markören över **[!UICONTROL Specialty Reports]** och klickar sedan på [rapporttyp](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md).

1. (Valfritt) I dialogrutan [!UICONTROL Report Settings] fönster, ändra standard [rapportinställningar](specialty-report-settings.md):

   1. (Valfritt) Ange ett eget namn för rapporten och mallen (om du sparar rapporten som en mall).

   1. (Valfritt) Om du vill spara rapportinställningarna som en mall markerar du kryssrutan bredvid **[!UICONTROL Save as template]**.

   1. (Valfritt) På **[!UICONTROL Basic Settings]** väljer du en befintlig rapportmall som du vill använda eller ändrar standardinställningarna för rapporten.

   1. (Valfritt) Klicka på **[!UICONTROL Columns tab]** och ändra standardkolumnerna i rapporten.

      Som standard visas alla monetära data i rapporter i formatet för USD (till exempel 1 000,00). Om du vill visa värdet i rätt valutaformat (men utan valutasymboler i CSV- och TSV-format) lägger du till &quot;[!UICONTROL Currency]till rapporten. Om rapporten innehåller data för konton med olika valutor, kan alla &quot;[!UICONTROL Total]&quot;monetära värden är summan av alla tal i kolumnen, oavsett valuta.

   1. (Valfritt) Klicka på **[!UICONTROL Advanced Filters]** och ändra de avancerade standardalternativen.

   1. (Valfritt) Klicka på **[!UICONTROL Attribution]** och ändra standardattribueringsregeln.

   1. (Valfritt) Klicka på **[!UICONTROL Scheduling and Delivery]** och ändra standardalternativen för schemaläggning och leverans.

1. ([!UICONTROL AdWords Conversion Report] och [!UICONTROL AdWords Shopping Performance Report] (endast; valfritt) Om du vill förhandsgranska de första 50 raderna i rapporten klickar du på **[!UICONTROL Preview]**. När du är klar klickar du **[!UICONTROL Back]** för att återgå till sidan med rapportinställningar.

1. Klicka på **[!UICONTROL Create]**.

Om du inte angav ett rapportschema körs rapporten omedelbart, annars körs den enligt angivet schema. Rapportnamnet läggs till i [[!UICONTROL Latest Reports] visa](/help/search-social-commerce/reports/report-about.md). Om du sparade rapporten som en mall läggs den även till i [[!UICONTROL Templates] visa](/help/search-social-commerce/reports/report-about.md). När rapporten är klar är filen tillgänglig för att öppnas eller sparas. Mallar är tillgängliga omedelbart.

Om du har angett e-postadresser för meddelanden får varje mottagare ett meddelande när rapportjobbet har slutförts eller misslyckats, baserat på användarens [konfigurerade meddelandeinställningar](/help/search-social-commerce/notifications/notification-edit.md) för rapporter.

>[!MORELIKETHIS]
>
>* [Specialrapporter](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md)
>* [Inställningar för specialrapport](/help/search-social-commerce/reports/management/specialty/specialty-report-settings.md)
>* [Rapportkolumner för specialrapporter](/help/search-social-commerce/reports/management/specialty/specialty-report-columns.md)
>* [Ta bort rapporter](/help/search-social-commerce/reports/management/report-delete.md)
