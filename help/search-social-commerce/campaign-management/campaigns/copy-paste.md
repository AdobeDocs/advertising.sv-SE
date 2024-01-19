---
title: Skapa och redigera kampanjdata i grupp med kopiera och klistra in
description: Lär dig hur du hanterar kampanjdata gruppvis med kopierings- och inklistringsfunktionen.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Skapa och redigera kampanjdata i grupp med kopiera och klistra in

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]och befintlig [!DNL Baidu] endast konton*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] vyer*

Du kan kopiera upp till 10 000 rader från [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] vyer och klistra in dem i [!DNL Microsoft Excel] eller en annan redigerare för att redigera icke-ID-fält. Du kan sedan kopiera [!DNL Excel] och klistra in dem som tabbseparerade data i vyn för att göra ändringarna. Funktionen använder datorns urklipp.

Du kan använda den här funktionen för att redigera befintliga kampanjobjekt (med ID-fält) och för att skapa nya kampanjobjekt utan ID-fält.

## Kopiera datarader

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Markera kryssrutan bredvid varje rad som du vill kopiera.

   Du kan kopiera upp till 10 000 rader.

1. Klicka på i verktygsfältet ovanför datatabellen ![Mer](/help/search-social-commerce/assets/more.png "Mer")och klicka sedan på **[!UICONTROL Copy]**.

   Du kan även använda operativsystemets &quot;kopiera&quot;-tangentbordskommando, som **[!DNL Ctrl+C]** for [!DNL Microsoft Windows] eller **[!DNL Command-C]** for [!DNL Apple Mac].

1. I [!UICONTROL Copy to Clipboard] dialogruta, klicka **[!UICONTROL Continue]**. När data är klara att kopieras klickar du **[!UICONTROL Copy]**.

1. Klistra in raderna i [!DNL Excel] eller en annan redigerare.

## Redigera och skapa datarader

1. Redigera data enligt följande krav:

   * De inklistrade data måste innehålla en rubrikrad och nödvändiga kampanjobjektvärden. Se de kolumner i kalkylbladet som krävs för [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Visa nätverk](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)och [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). Kolumnordningen spelar ingen roll.

      * För befintliga objekt som du vill redigera måste du inkludera alla relevanta ID-kolumner, entitetsnamn och det attribut som ska redigeras. Redigera inte det numeriska ID:t för objektet.

      * Inkludera alla relevanta enhetsnamn och attribut för nya kampanjobjekt, men inkludera inte objekt-ID:n (som genereras automatiskt). Om du till exempel skapar en ny annons lämnar du [!UICONTROL Ad ID] fältet är tomt. Annonsnätverket skapar automatiskt ett ID när du skickar objektet.

   * Värdet i en icke obligatorisk kolumn kan vara null (tom), men varje rad måste ha samma antal tabbseparerade värden.

1. Spara data som tabbseparerade värden.

## Klistra in datarader i kampanjhanteringsvyer

>[!NOTE]
>
>Om de inklistrade raderna innehåller data som är identiska med data som finns i de befintliga entiteterna, eller som duplicerar en befintlig entitet, ignoreras dubblettdata.

1. I [!DNL Excel] eller annan redigerare, kopiera de relevanta tabbseparerade raderna.

1. På huvudmenyn Sök, Socialt, &amp; Commerce klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Öppna den vy där data ska klistras in (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Klicka på i verktygsfältet ovanför datatabellen ![Mer](/help/search-social-commerce/assets/more.png "Mer")och klicka sedan på **[!UICONTROL Paste]**.

   Du kan även använda operativsystemets&quot;Klistra in&quot;-tangentbordskommando, som **[!DNL Ctrl+V]** for [!DNL Microsoft Windows] eller **[!DNL Command-V]** for [!DNL Apple Mac].

1. Klistra in data i indatarutan och klicka sedan på **[!UICONTROL Process]**.

1. (Valfritt) Ange ytterligare information:

   * (Om **[!UICONTROL Additional Details]** är komprimerad) Klicka ![Öppna](/help/search-social-commerce/assets/chevron-up.png "Öppna") för att utöka detaljerna.

   * Ange ett valfritt **[!UICONTROL Job Name]** och/eller valfritt **[!UICONTROL Job Description]**.

1. Klicka på **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Redigera inställningar direkt i en rad](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Hantera kampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Hantera annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Hantera nyckelord](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Hantera annonser](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
