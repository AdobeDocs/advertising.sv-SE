---
title: Skapa flera tredjepartsannonser
description: Lär dig skapa flera tredjepartsannonser samtidigt.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Skapa flera tredjepartsannonser

Du kan skapa upp till 500 tredjepartsannonser i taget genom att överföra taggar som pekar på kreativa resurser på annonsservrar från tredje part. Du kan ta med spårningspixlar för annonserna.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Du kan överföra taggarna [!DNL DoubleClick] och [!DNL Flashtalking] eller en manuellt ifylld fil med hjälp av den angivna mallen.

>[!TIP]
>
> Det bästa sättet är att använda annonser från tredje part som hanteras säkert med HTTPS. URL:er som hanteras med HTTPS börjar med &quot;https&quot;.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.

1. Klicka på namnet på kampanjen där annonsen ska inkluderas.

1. Klicka på **[!UICONTROL Create]** ovanför datatabellen. Klicka på **[!UICONTROL Bulk upload ads]** i avsnittet Ad Types på menyn.

1. Välj annonsservern som annonsen finns på: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* eller *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] och [!DNL Flashtalking] annonser) Välj den taggtyp som ska användas för varje videoresurs och varje visningsresurs. Vilka alternativ som är tillgängliga varierar beroende på annonsserver.

1. (Annonserar på alla annonsservrar utom [!DNL DoubleClick] och [!DNL Flashtalking]) Klicka på **[!UICONTROL Download this template]** om du vill hämta en mall i formatet [!DNL Microsoft Excel] kalkylblad (XLSX), som du kan fylla i med annonsdata och spara lokalt. De obligatoriska kolumnerna är [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] och [!UICONTROL Ad Types].

1. Klicka på **[!UICONTROL Upload]** och välj en fil i formaten .xlsx eller .xls från enheten eller nätverket.

   För [!DNL DoubleClick]- och [!DNL Flashtalking]-annonser överför du oredigerade taggblad från annonsservern. För andra annonsservrar använder du mallen som du hämtade i steg 3.

1. När överföringen är klar klickar du på **[!UICONTROL Start Building Ads]**.

1. Granska information och status för varje annons:

   1. (Universal video ads using [!DNL Google] or [!DNL Flashtalking] tags) Klicka på fältet **[!UICONTROL Ad Type]** och välj **[!UICONTROL Universal Video]**.

   1. (Universella videoannonser) För varje ny annons klickar du på ![redigera](/help/dsp/assets/edit.png), väljer det [tillämpliga videoformatet](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) och sedan på **Spara**.

   1. Granska status för varje annons, som baseras på valideringskontroller för den överförda taggen.

   1. (Valfritt) Gör något av följande för varje annons:

      * Om du vill förhandsgranska en annons klickar du på ![play](/help/dsp/assets/play.png) i annonsraden.

      * Om du vill redigera annonsinformationen klickar du på ![redigera](/help/dsp/assets/edit.png), redigerar informationen och klickar sedan på **Spara**.

      * Om du vill ta bort en annons klickar du på **[!UICONTROL X]** i annonsraden.

1. Klicka på **[!UICONTROL Create *N *Lägg till]**.

1. Gör något av följande:

   * Klicka på **[!UICONTROL Done]**.

   * (Om en annons refuseras, valfritt) Om du vill redigera annonsposten och skicka annonsen igen för granskning:

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
>* [Video: Så här överför du tredjepartstaggar i grupp](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Frågor och svar om universell video](/help/dsp/campaign-management/faq-universal-video.md)
