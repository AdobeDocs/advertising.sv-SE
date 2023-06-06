---
title: Generera en grundläggande rapport eller avancerad rapport
description: Lär dig hur du skapar en anpassad grundläggande eller avancerad rapport.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Generera en grundläggande rapport eller avancerad rapport

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create Report]** håller du markören över **[!UICONTROL Basic Reports]** eller **[!UICONTROL Advanced Reports]** och klickar sedan på [rapporttyp](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Valfritt) I dialogrutan [!UICONTROL Report Settings] fönster, ändra standard [rapportinställningar](basic-advanced-report-settings.md):

   1. (Valfritt) Ange ett eget namn för rapporten och mallen (om du sparar rapporten som en mall).

   1. (Valfritt) Om du vill spara rapportinställningarna som en mall markerar du kryssrutan bredvid **[!UICONTROL Save as template]**.

   1. (Valfritt) På **[!UICONTROL Basic Settings]** väljer du en befintlig rapportmall som ska användas eller ändrar standardinställningarna för rapporten.

   1. (Valfritt) Klicka på **[!UICONTROL Columns tab]** och ändra standardkolumnerna i rapporten.

      Som standard visas alla monetära data i rapporter i formatet för US-dollar (till exempel 1 000,00). Om du vill visa värdet i rätt valutaformat (men utan valutasymboler i CSV- och TSV-format) lägger du till &quot;[!UICONTROL Currency]till rapporten. Om rapporten innehåller data för konton med olika valutor, kan alla[!UICONTROL Total]&quot;monetära värden är summan av alla tal i kolumnen, oavsett valuta.

   1. (Valfritt) [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report]och [!UICONTROL Label Classification Report] (endast) Klicka på **[!UICONTROL Classifications]** och begränsa rapportresultaten till att endast inkludera specifika etikettklassificeringar.

   1. (Valfritt) Klicka på **[!UICONTROL Advanced Filters]** och ändra de avancerade standardalternativen.

   1. (Valfritt) Klicka på **[!UICONTROL Attribution]** och ändra standardattribueringsregeln.

   1. (Valfritt) Klicka på **[!UICONTROL Scheduling and Delivery]** och ändra standardalternativen för schemaläggning och leverans.

1. (Valfritt när det är tillgängligt) Om du vill förhandsgranska de första 50 raderna i rapporten klickar du på **[!UICONTROL Preview]**. När du är klar klickar du på **[!UICONTROL Back]** för att återgå till sidan med rapportinställningar.

   >[!NOTE]
   >
   >Knappen Förhandsgranska är tillgänglig för alla grundläggande och avancerade rapporter förutom för [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report]och [!UICONTROL Transaction Report].

1. Klicka på **[!UICONTROL Create]**.

Om du inte angav ett rapportschema körs rapporten omedelbart; i annat fall körs den enligt angivet schema. Rapportnamnet läggs till i [[!UICONTROL Latest Reports] visa](/help/search-social-commerce/reports/report-about.md). Om du sparade rapporten som en mall läggs den även till i [[!UICONTROL Templates] visa](/help/search-social-commerce/reports/report-about.md). När rapporten är klar är filen tillgänglig för att öppnas eller sparas. -mallar är tillgängliga omedelbart.

Om du har angett e-postadresser för meddelanden får varje mottagare ett meddelande när rapportjobbet har slutförts eller misslyckats, baserat på användarens [konfigurerade meddelandeinställningar](/help/search-social-commerce/notifications/notification-edit.md) för rapporter.

>[!MORELIKETHIS]
>
>* [Grundläggande och avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Grundläggande och avancerade rapportinställningar](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Rapportkolumner för grundläggande och avancerade rapporter](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Ta bort rapporter](/help/search-social-commerce/reports/management/report-delete.md)

