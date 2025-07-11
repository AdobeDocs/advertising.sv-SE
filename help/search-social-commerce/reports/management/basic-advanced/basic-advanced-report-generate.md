---
title: Generera en grundläggande rapport eller avancerad rapport
description: Lär dig hur du skapar en anpassad grundläggande eller avancerad rapport.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Generera en grundläggande rapport eller avancerad rapport

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Report]** i verktygsfältet ovanför datatabellen, håll markören över **[!UICONTROL Basic Reports]** eller **[!UICONTROL Advanced Reports]** och klicka sedan på [rapporttypen](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Valfritt) Ändra standardinställningarna för [rapport](basic-advanced-report-settings.md) i fönstret [!UICONTROL Report Settings]:

   1. (Valfritt) Ange ett eget namn för rapporten och mallen (om du sparar rapporten som en mall).

   1. (Valfritt) Om du vill spara rapportinställningarna som en mall markerar du kryssrutan bredvid **[!UICONTROL Save as template]**.

   1. (Valfritt) På fliken **[!UICONTROL Basic Settings]** väljer du en befintlig rapportmall som du vill använda eller ändrar standardinställningarna för rapporten.

   1. (Valfritt) Klicka på **[!UICONTROL Columns tab]** och ändra standardkolumnerna i rapporten.

      Som standard visas alla monetära data i rapporter i formatet för USD (till exempel 1 000,00). Om du vill visa värdet i rätt valutaformat (men utan valutasymboler i CSV- och TSV-format) lägger du till kolumnen [!UICONTROL Currency] i rapporten. Om rapporten innehåller data för konton med olika valutor är alla [!UICONTROL Total]-monetära värden summan av alla tal i kolumnen, oavsett valuta.

   1. (Valfritt: endast [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] och [!UICONTROL Label Classification Report]) Klicka på fliken **[!UICONTROL Classifications]** och begränsa rapportresultaten så att de endast innehåller specifika etikettklassificeringar.

   1. (Valfritt) Klicka på fliken **[!UICONTROL Advanced Filters]** och ändra de avancerade standardalternativen.

   1. (Valfritt) Klicka på fliken **[!UICONTROL Attribution]** och ändra standardattribueringsregeln.

   1. (Valfritt) Klicka på fliken **[!UICONTROL Scheduling and Delivery]** och ändra standardalternativen för schemaläggning och leverans.

1. (Valfritt när det är tillgängligt) Om du vill förhandsgranska de första 50 raderna i rapporten klickar du på **[!UICONTROL Preview]**. När du är klar klickar du på **[!UICONTROL Back]** för att återgå till sidan med rapportinställningar.

   >[!NOTE]
   >
   >Knappen Förhandsgranska är tillgänglig för alla grundläggande och avancerade rapporter förutom för [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] och [!UICONTROL Transaction Report].

1. Klicka på **[!UICONTROL Create]**.

Om du inte angav ett rapportschema körs rapporten omedelbart, annars körs den enligt angivet schema. Rapportnamnet läggs till i vyn [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Om du sparade rapporten som en mall läggs den också till i [[!UICONTROL Templates]-vyn ](/help/search-social-commerce/reports/report-about.md). När rapporten är klar är filen tillgänglig för att öppnas eller sparas. Mallar är tillgängliga omedelbart.

Om du har angett e-postadresser för meddelanden får varje mottagare ett meddelande när rapportjobbet har slutförts eller misslyckats, baserat på användarens [konfigurerade meddelandeinställningar](/help/search-social-commerce/notifications/notification-edit.md) för rapporter.

>[!MORELIKETHIS]
>
>* [Om grundläggande och avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Grundläggande och avancerade rapportinställningar](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Rapportkolumner för grundläggande och avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Ta bort rapporter](/help/search-social-commerce/reports/management/report-delete.md)
