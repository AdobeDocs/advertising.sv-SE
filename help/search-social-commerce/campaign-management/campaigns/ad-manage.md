---
title: Hantera annonser
description: Lär dig hur du skapar och hanterar annonser.
exl-id: 5ec410cd-9dff-41e6-9ecc-d6ceee84755e
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Hantera annonser

Endast *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] och befintliga [!DNL Baidu]-konton*

Du kan skapa, redigera och ändra status för annonser i vyn [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads].

## Skapa en annons

>[!NOTE]
>
>Ni behöver inte skapa produktannonser för shoppingkampanjer, annonsnätverket skapar dem automatiskt. För [!DNL Microsoft Advertising] shoppingkampanjer kan du dock välja att definiera kampanjrader som ska inkluderas i annonser.

>[!TIP]
>
>Om du vill skapa flera annonser samtidigt använder du [kopiera och klistra in-funktionen](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) eller [kampanjkalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Välj annonsnätverket, kontot, kampanjen, annonsgruppen och annonstypen och klicka sedan på **[!UICONTROL Continue]**.

   Mer information om olika annonstyper finns i [Om annonser](ad-about.md).

1. Ange [[!DNL Baidu] textannons](ad-settings-baidu-text.md), [[!DNL Google Ads] annons endast för samtal](ad-settings-google-call.md), [[!DNL Google Ads] utökad dynamisk sökannons](ad-settings-google-dsa.md) (kallas nu bara&quot;dynamisk sökannons&quot; i Google Ads), [[!DNL Google Ads] responsiv sökannons](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] utökad dynamisk sökannons](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimediaannons](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] produktannons](ad-settings-microsoft-product.md),   [[!DNL Microsoft Advertising] &rbrace;responsiva (målgrupp) annonser](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsiva sökannonser](ad-settings-microsoft-rsa.md) eller inställningar för [[!DNL Yandex] text och ](ad-settings-yandex-text.md) .

   >[!NOTE]
   >
   >(Kampanjer med Adobe Advertising konverteringsspårning) Om konto- eller kampanjinställningarna anger spårning endast på nyckelordsnivå genereras ingen spårning för annonser i sökningen, sociala medier och Commerce.

1. Klicka på **[!UICONTROL Post]**.

1. (Shoppingannonser i kampanjer med Adobe Advertising konverteringsspårning, valfritt) Om du vill spåra klick på annonsen [genererar du en spårnings-URL med hjälp av verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md) och lägger till den manuellt i inställningarna för konto, kampanj eller produktgrupp.

## Redigera annonsinställningar

>[!NOTE]
>
>* Följande annonstyper är *mutable*, vilket betyder att du kan ändra annonskopian eller bilden och behålla samma annons-ID: alla [!DNL Google Ads] annonstyper förutom dynamiska sökannonser och [!DNL Microsoft Advertising] expanderade textannonser.
>* Alla andra annonser som stöds är *inte ändringsbara*, vilket innebär att om du ändrar annonskopian eller bilden tas den befintliga annonsen bort och en ny skapas. Prestanda för den nya annonsen kan vara instabila i några veckor medan Search, Social och Commerce samlar in tillräckligt med data för optimering.
>* Du kan inte redigera innehållet i en produktannons, förutom kampanjraden för [!DNL Microsoft Advertising] produktannonser. Du kan dock pausa eller ta bort en annons.

>[!TIP]
>
>Om du vill redigera stora mängder data samtidigt använder du [kopiera och klistra in-funktionen](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) eller [kampanjkalkylblad](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]** på undermenyerna.

1. Gör något av följande:

   * (Om du vill redigera inställningar för en enskild annons håller du markören över annonsförhandsvisningen och klickar på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

   * (Så här redigerar du inställningar för en eller flera annonser):

      1. Markera kryssrutan bredvid varje rad.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet ovanför datatabellen.

1. Redigera [[!DNL Baidu] textannons](ad-settings-baidu-text.md), [[!DNL Google Ads] annons för endast samtal](ad-settings-google-call.md), [[!DNL Google Ads] utökad dynamisk sökannons](ad-settings-google-dsa.md) (kallas nu bara&quot;dynamisk sökannons&quot; i Google Ads), [[!DNL Google Ads] responsiv sökannons](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] utökad dynamisk sökannons](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimediaannons](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] produktannons](ad-settings-microsoft-product.md),   [[!DNL Microsoft Advertising] &rbrace;responsiva (målgrupp) annonser](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsiva sökannonser](ad-settings-microsoft-rsa.md) eller inställningar för [[!DNL Yandex] text och ](ad-settings-yandex-text.md) .

   För flera annonser kan du bara redigera fält som är gemensamma för alla markerade annonser, och dina ändringar tillämpas på alla markerade annonser. För vissa alfanumeriska fält kan du ändra befintliga värden till ett angivet värde, ersätta en befintlig sträng med en angiven sträng, lägga till ett angivet prefix i början av varje värde eller lägga till ett suffix i slutet av varje värde. För vissa monetära fält kan du ändra befintliga värden till ett angivet värde eller antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

1. Spara data:

   * (Enstaka annonser) Klicka på **[!UICONTROL Post]**.

   * (Flera annonser) Klicka på **[!UICONTROL Post Now]**.

## Ändra status för annonser

Du kan pausa en aktiv annons för att inaktivera budgivning. Du kan återuppta offerten senare genom att ändra status till aktiv.

Du kan också ta bort alla aktiva eller pausade sökannonser. Borttagna annonser tas bort från annonsnätverket. De är fortfarande synliga, men du kan inte ändra dem.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Ads]** på undermenyerna.

1. (Valfritt) Filtrera listan så att den innehåller specifika annonser.

1. Markera kryssrutan bredvid varje annons vars status du vill ändra.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på statusknappen i verktygsfältet:

   * Aktivera raderna genom att klicka på ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera").

   * Om du vill pausa raderna klickar du på ![Paus](/help/search-social-commerce/assets/pause.png "Paus").

   * Om du vill ta bort raderna klickar du på ![Mer](/help/search-social-commerce/assets/more.png "Mer") och väljer **[!UICONTROL Delete]**. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

>[!MORELIKETHIS]
>
>* [Om annonser](ad-about.md)
>* [[!DNL Baidu] text och inställningar](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] annonsinställningar för endast samtal](ad-settings-google-call.md)
>* [[!DNL Google Ads] utökade inställningar för dynamisk sökning och annonser](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Inställningar för responsiv sökannonsering](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] utökade inställningar för dynamisk sökning och annonser](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] inställningar för multimediaannons](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] inställningar för produktannons](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] Reklaminställningar för responsiv (publik)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] Inställningar för responsiv sökannonsering](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] text och inställningar](ad-settings-yandex-text.md)
