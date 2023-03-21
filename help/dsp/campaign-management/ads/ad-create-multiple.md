---
title: Skapa flera tredjepartsannonser
description: Lär dig skapa flera tredjepartsannonser samtidigt.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 5139e6022cd5f5f11046d8f38bd0f1db91464928
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Skapa flera tredjepartsannonser

Du kan skapa upp till 500 tredjepartsannonser i taget genom att överföra taggar som pekar på kreativa resurser på annonsservrar från tredje part. Du kan ta med spårning av pixlar för annonserna.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Du kan överföra antingen [!DNL DoubleClick] och [!DNL Flashtalking] eller en fil som fylls i manuellt med hjälp av den angivna mallen.

>[!TIP]
>
> Det bästa sättet är att använda tredjepartsannonser som hanteras säkert med HTTPS. URL:er som hanteras med HTTPS börjar med &quot;https&quot;.

1. På huvudmenyn klickar du på **[!UICONTROL Campaigns]**.

1. Klicka på namnet på kampanjen där annonsen ska inkluderas.

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**. Klicka på i avsnittet Ad Types på menyn **[!UICONTROL Bulk upload ads]**.

1. Välj annonsservern som annonsen finns på: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*, eller *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] och [!DNL Flashtalking] ads) Välj vilken taggtyp som ska användas för varje videoresurs och varje visningsresurs. Vilka alternativ som är tillgängliga varierar beroende på annonsserver.

1. (Annonser på alla annonsservrar utom [!DNL DoubleClick] och [!DNL Flashtalking]) Klicka **[!UICONTROL Download this template]** för att hämta en mall i [!DNL Microsoft Excel] kalkylbladsformat (XLSX), som du kan fylla med annonsdata och spara lokalt. De kolumner som krävs är [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]och [!UICONTROL Ad Types].

1. Klicka **[!UICONTROL Upload]** och välj en fil i formaten .xlsx eller .xls på enheten eller i nätverket.

   För [!DNL DoubleClick] och [!DNL Flashtalking] annonser, överför oredigerade taggblad från annonsservern. För andra annonsservrar använder du mallen som du hämtade i steg 3.

1. När överföringen är klar klickar du på **[!UICONTROL Start Building Ads]**.

1. Granska information och status för varje annons:

   1. (Universal Video ads using [!DNL Google] eller [!DNL Flashtalking] taggar) Klicka på **[!UICONTROL Ad Type]** fält och markera **[!UICONTROL Universal Video]**.

   1. (Universal video ads) För varje ny annons klickar du på ![redigera](/help/dsp/assets/edit.png)väljer du [tillämpligt videoformat](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)och klicka sedan på **Spara**.

   1. Granska status för varje annons, som baseras på valideringskontroller för den överförda taggen.

   1. (Valfritt) Gör något av följande för varje annons:

      * Om du vill förhandsgranska en annons klickar du på ![play](/help/dsp/assets/play.png) i annonsraden.

      * Om du vill redigera annonsinformationen klickar du på ![redigera](/help/dsp/assets/edit.png), redigera informationen och klicka sedan på **Spara**.

      * Om du vill ta bort en annons klickar du på **[!UICONTROL X]** i annonsraden.

1. Klicka **[!UICONTROL Create *N *Annonser]**.

1. Gör något av följande:

   * Klicka på **[!UICONTROL Done]**.

   * (Om en annons avslås. (valfritt) Om du vill redigera annonsposten och skicka om annonsen för granskning:

      1. Klicka på annonsens namn.

      1. Redigera annonsinställningarna.

      1. Klicka på **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Universella videoannonser kan bara bifogas till universella videomaterial.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [Skapa en annons](ad-create.md)
>* [Video: Så här överför du tredjeparts-annonstaggar gruppvis](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)

