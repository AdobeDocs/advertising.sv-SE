---
title: Hantera annonser
description: Lär dig hur du skapar och hanterar annonser.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Hantera annonser

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]och [!DNL Yandex] endast konton*

Du kan skapa, redigera och ändra status för annonser i [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] vy.

## Skapa en annons

>[!NOTE]
>
>Ni behöver inte skapa produktannonser för shoppingkampanjer; annonsnätverket skapar dem automatiskt. För [!DNL Microsoft Advertising] shoppingkampanjer, men ni kan också definiera kampanjrader som ska ingå i annonser.

>[!TIP]
>
>Om du vill skapa flera annonser samtidigt använder du [kopiera och klistra in](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) eller [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket, kontot, kampanjen, annonsgruppen och annonstypen och klicka sedan på **[!UICONTROL Continue]**.

   Mer information om olika annonstyper finns i &quot;[Om annonser](ad-about.md).&quot;

1. Ange [[!DNL Baidu] text ad](ad-settings-baidu-text.md), [[!DNL Google Ads] annons endast för samtal](ad-settings-google-call.md), [[!DNL Google Ads] expanderad dynamisk sökannons](ad-settings-google-dsa.md) (kallas nu bara&quot;dynamisk sökannons&quot; i Google Ads), [[!DNL Google Ads] responsiv sökannons](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] expanderad dynamisk sökannons](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimediaannonser](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] produktannons](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] responsiv (målgrupp) annons](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsiv sökannons](ad-settings-microsoft-rsa.md), eller [[!DNL Yandex] text ad](ad-settings-yandex-text.md) inställningar.

   >[!NOTE]
   >
   >(Kampanjer med konverteringsspårning för annonsering i Adobe) Om konto- eller kampanjinställningarna endast anger spårning på nyckelordsnivå genereras ingen spårning för annonser i Sök, Socialt och Commerce.

1. Klicka på **[!UICONTROL Post]**.

1. (Shoppingannonser i kampanjer med konverteringsspårning för Adobe-annonsering. (valfritt) Om du vill spåra klickningar på annonsen [generera en spårnings-URL med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md)och lägg till den manuellt i inställningarna för konto, kampanj eller produktgrupp.

## Redigera annonsinställningar

>[!NOTE]
>
>* Följande annonstyper är *mutabel*, vilket innebär att du kan ändra annonskopian eller bilden och behålla samma annons-ID: alla [!DNL Google Ads] annonstyper förutom dynamiska sökannonser, och [!DNL Microsoft Advertising] expanderade textannonser.
>* Alla andra annonser som stöds är *ej ändringsbar*, vilket innebär att om du ändrar annonskopian eller bilden tas den befintliga annonsen bort och en ny skapas. Prestanda för den nya annonsen kan vara instabila i några veckor medan Search, Social och Commerce samlar in tillräckligt med data för att optimera anbuden.
>* Du kan inte redigera innehållet i en produktannons, förutom kampanjraden för [!DNL Microsoft Advertising] produktannonser. Du kan dock pausa eller ta bort en annons.


>[!TIP]
>
>Om du vill redigera stora mängder data samtidigt använder du [kopiera och klistra in](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) eller [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. Gör något av följande:

   * (Om du vill redigera inställningarna för en enskild annons) Håll markören över annonsförhandsvisningen och klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

   * (Så här redigerar du inställningar för en eller flera annonser):

      1. Markera kryssrutan bredvid varje rad.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [[!DNL Baidu] text ad](ad-settings-baidu-text.md), [[!DNL Google Ads] annons endast för samtal](ad-settings-google-call.md), [[!DNL Google Ads] expanderad dynamisk sökannons](ad-settings-google-dsa.md) (kallas nu bara&quot;dynamisk sökannons&quot; i Google Ads), [[!DNL Google Ads] responsiv sökannons](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] expanderad dynamisk sökannons](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimediaannonser](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] produktannons](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] responsiv (målgrupp) annons](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsiv sökannons](ad-settings-microsoft-rsa.md), eller [[!DNL Yandex] text ad](ad-settings-yandex-text.md) inställningar.

   För flera annonser kan du bara redigera fält som är gemensamma för alla markerade annonser, och dina ändringar tillämpas på alla markerade annonser. För vissa alfanumeriska fält kan du ändra befintliga värden till ett angivet värde, ersätta en befintlig sträng med en angiven sträng, lägga till ett angivet prefix i början av varje värde eller lägga till ett suffix i slutet av varje värde. För vissa monetära fält kan du ändra befintliga värden till ett angivet värde eller antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

1. Spara data:

   * (Enstaka annonser) Klicka på **[!UICONTROL Post]**.

   * (Flera annonser) Klicka på **[!UICONTROL Post Now]**.

## Ändra status för annonser

Du kan pausa en aktiv annons för att inaktivera budgivning. Du kan återuppta offerten senare genom att ändra status till aktiv.

Du kan också ta bort alla aktiva eller pausade sökannonser. Borttagna annonser tas bort från annonsnätverket. De är fortfarande synliga, men du kan inte ändra dem.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika annonser.

1. Markera kryssrutan bredvid varje annons vars status du vill ändra.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på statusknappen i verktygsfältet:

   * Aktivera raderna genom att klicka ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera").

   * Om du vill pausa raderna klickar du på ![Pausa](/help/search-social-commerce/assets/pause.png "Pausa").

   * Om du vill ta bort raderna klickar du på ![Mer](/help/search-social-commerce/assets/more.png "Mer") och markera **[!UICONTROL Delete]**. Klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Om annonser](ad-about.md)
>* [[!DNL Baidu] text och inställningar](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] annonsinställningar som bara kan anropas](ad-settings-google-call.md)
>* [[!DNL Google Ads] expanderade dynamiska sökannonsinställningar](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] inställningar för responsiv sökning och](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] expanderade dynamiska sökannonsinställningar](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] multimediaannonsinställningar](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] produkt- och annonsinställningar](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] inställningar för responsiv (målgrupp) annonsering](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] inställningar för responsiv sökning och](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] text och inställningar](ad-settings-yandex-text.md)

