---
title: Skapa ett [!UICONTROL Simple Ad Serving]-erbjudande
description: Lär dig hur du skapar en spårningspixel för en [!UICONTROL Simple Ad Serving]-affär.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Skapa ett [!UICONTROL Simple Ad Serving]-erbjudande

1. På huvudmenyn klickar du på **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]** och väljer sedan **[!UICONTROL Simple Ad Serving]**.

1. Ange [avtalsinställningarna](simple-deal-settings.md):

   1. I avsnittet [!UICONTROL Select Ad Source] anger du information om utgivaren, annonsören och kampanjen samt annonstypen. Klicka sedan på **[!UICONTROL Next]**.

   1. I avsnittet [!UICONTROL Select Ad(s)] anger du en annons som ska användas som proxy i DSP:

      1. Gör något av följande:

         * För befintliga annonser väljer du de annonser som ska användas.

         * Skapa en proxyannons [från tredje part](/help/dsp/campaign-management/ads/ad-create-multiple.md) för nya annonser.

      >[!NOTE]
      > DSP levererar inte de annonser du anger. Utgivaren står för annonsen.

      1. Klicka på **[!UICONTROL Next]**.

   1. Redigera flödesinformationen i Feed Details och klicka sedan på **[!UICONTROL Next]**.

      DSP genererar automatiskt en placering med namnet&quot;SAS-placering - &lt;*erbjudandenamn*>&quot; för annonsen. I placeringen anges erbjudandet automatiskt i avsnittet [!UICONTROL Inventory Targets]. Alla andra målinriktningsalternativ är inte tillämpliga.

1. Skicka pixlar för händelsespårning till utgivaren för implementering på något av följande sätt:

   * (Valfritt) På skärmen [!UICONTROL Activate Tag with Publisher] skickar du avtalstaggen till utgivaren.

     När du är klar med de föregående stegen genererar DSP ett e-postmeddelande som du kan skicka till utgivaren. Meddelandet innehåller avtalsinformationen, en länk från vilken du kan hämta avtalstaggen och en auktoriseringskod för länken.

      1. Granska avtalsinformationen och gör sedan något av följande:

         * Om du vill klistra in informationen i ett e-postmeddelande i ett e-postprogram på enheten klickar du på **[!UICONTROL Email & Done]** och väljer e-postprogrammet. Fältet [!UICONTROL CC:] är förifyllt med en [!DNL Adobe]-supportadress. Du kan sedan skicka meddelandet till lämplig kontakt för utgivaren.

         * Klicka på **[!UICONTROL Copy Email]om du vill kopiera informationen till Urklipp.** Du kan sedan klistra in innehållet manuellt i ett e-postmeddelande och skicka det till lämplig kontakt för utgivaren. Du måste inkludera en kopia (CC:) till `publisher-support-global@adobe.com`. När du är klar med kopieringen av meddelandet klickar du på **[!UICONTROL Email & Done]**.

      1. (Om det behövs) Följ upp med utgivaren för att se om taggen innehåller rätt makron så att taggen fungerar med utgivarens annonsserver.

   * (Valfritt) Skicka pixlarna för händelsespårning manuellt till utgivaren:

      1. Klicka på [!UICONTROL Deals]Alternativ-menyn![&#x200B; &#x200B;](/help/dsp/assets/options-menu.png)> **i avtalsraden i vyn[!UICONTROL show pixel]**.

         Händelsepixlarna innehåller en [!UICONTROL Clickthrough]-pixel och en [!UICONTROL Impression]-pixel. Video- och ljudannonser innehåller även händelsepixlar per kvartil (från [!UICONTROL 25% Complete] till [!UICONTROL 100% Complete]).

      1. Kopiera pixlarna för händelsespårning och skicka dem till din utgivare.

>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] inställningar](simple-deal-settings.md)
>* [Visa en detaljerad rapport om ett avtal](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
