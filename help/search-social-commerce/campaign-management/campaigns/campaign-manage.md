---
title: Hantera kampanjer
description: Lär dig hur du skapar och hanterar annonskampanjer.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# Hantera kampanjer

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]och [!DNL Yandex] endast konton*

En kampanj är den primära komponenten i ett annonsnätverkskonto. För de flesta kampanjtyper består den av en uppsättning annonsgrupper eller annonsuppsättningar. Kampanjinställningarna omfattar kampanjbudgetparametrar, annonsmål och valfria spårningsparametrar för alla annonser i kampanjen. Spårningsparametrar på kampanjnivå åsidosätter kontonivåparametrarna, men de kan i sig åsidosättas på en lägre nivå.

En gång [göra ett annonsnätverkskonto tillgängligt](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) och Search, Social, &amp; Commerce har synkroniserat kontouppgifterna med annonsnätverket kan ni skapa nya kampanjer med [kampanjtyper som stöds](/help/search-social-commerce/introduction/supported-inventory.md). Ni kan också redigera och ändra kampanjernas status.

## Skapa en kampanj

>[!NOTE]
>
>* Innan du skapar en kampanj [implementera konverteringsspårningstaggar](/help/search-social-commerce/tracking/conversion-tracking-about.md) på annonsörens webbsidor.
>* Om du vill skapa ett stort antal kampanjer samtidigt använder du [kopiera och klistra in](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) eller [kampanjlampor](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).


1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket, kontot och kampanjtypen och klicka sedan på **[!UICONTROL Continue]**.

   Beskrivningarna av varje kampanjtyp finns i [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md), eller [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) kampanjinställningar.

1. Ange [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md), eller [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) kampanjinställningar.

   Beroende på annonsnätverket kan inställningarna grupperas i [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Shopping Settings], [!UICONTROL Campaign Targeting], [!UICONTROL Advanced Device Options], [!UICONTROL URL Options]och [!UICONTROL (Google) DSA Options]. Så här konfigurerar du inställningar för [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites], [!UICONTROL Campaign Tracking], eller [!UICONTROL Asset Groups] (om tillgängligt), klicka på **[!UICONTROL Add Negative Keywords]**, **[!UICONTROL Add Negative Websites]**, **[!UICONTROL Set Campaign Tracking]**, eller **[!UICONTROL Manage Asset Groups]**, respektive.

1. Klicka på **[!UICONTROL Post]**.

Beroende på vilket annonsnätverk som kampanjen skapades på kan du behöva skapa associerade annonsgrupper och annonser innan kampanjen skickas till annonsnätverket.

## Redigera kampanjinställningar

Du kan redigera inställningar för enskilda kampanjer. Du kan också redigera vissa fält för flera kampanjer samtidigt, inklusive viss kampanjinformation, budgetalternativ och URL-alternativ som är gemensamma för alla valda kampanjer.

>[!TIP]
>
>Du kan också redigera data i grupp med kopierings- och inklistringsfunktionen eller kampanjmallar.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. Gör något av följande:

   1. (Om du vill redigera inställningarna för en enskild kampanj) Håll markören över enhetsnamnet klickar du på ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL Edit]**.

   1. (Så här redigerar du inställningar för en eller flera kampanjer):

      * Markera kryssrutan bredvid varje kampanj.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md), eller [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) kampanjinställningar.

   För flera kampanjer kan inställningarna grupperas i [!UICONTROL Campaign Details], [!UICONTROL Budget Options]och [!UICONTROL URL Options], beroende på annonsnätverk. Du kan bara redigera fält som är gemensamma för alla valda kampanjer, och dina ändringar tillämpas på alla valda kampanjer. För vissa alfanumeriska fält kan du ändra befintliga värden till ett angivet värde, ersätta en befintlig sträng med en angiven sträng, lägga till ett angivet prefix i början av varje värde eller lägga till ett suffix i slutet av varje värde. För vissa monetära fält har du möjlighet att ändra befintliga värden till ett angivet värde eller att antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

   Inställningarna kan grupperas i [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Shopping Settings], [!UICONTROL Campaign Targeting], [!UICONTROL Advanced Device Options], [!UICONTROL URL Options]och [!UICONTROL (Google) DSA Options]. Så här konfigurerar du inställningar för [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites], [!UICONTROL Campaign Tracking], eller [!UICONTROL Asset Groups] (om tillgängligt), klicka på **[!UICONTROL Add Negative Keywords]**, **[!UICONTROL Add Negative Websites]**, **[!UICONTROL Set Campaign Tracking]**, eller **[!UICONTROL Manage Asset Groups]**, respektive.

1. Spara data:

   * (Enstaka kampanjer) Klicka **[!UICONTROL Post]**.

   * (Flera kampanjer) Klicka **[!UICONTROL Post Now]**.

Beroende på vilket annonsnätverk kampanjen skapades på kan det vara nödvändigt att inkludera annonsgrupper och annonser innan kampanjen skickas till annonsnätverket.

## Ändra status för kampanjer

Du kan pausa en aktiv sökkampanj i ett annonsnätverk som stöds för att inaktivera budgivning på den. Du kan återuppta offerten senare genom att ändra status till aktiv.

Du kan också ta bort alla aktiva eller pausade sökkampanjer. Borttagna kampanjer tas bort från annonsnätverket. De visas fortfarande när du inkluderar dem i datafiltret, men du kan inte ändra dem.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika kampanjer.

1. Markera kryssrutan bredvid varje kampanj vars status du vill ändra.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på statusknappen i verktygsfältet:

   * Aktivera raderna genom att klicka ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera").

   * Om du vill pausa raderna klickar du på ![Pausa](/help/search-social-commerce/assets/pause.png "Pausa").

   * Om du vill ta bort raderna klickar du på ![Mer](/help/search-social-commerce/assets/more.png "Mer") och markera **[!UICONTROL Delete]**. Klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Inställningar för Baidu-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampanjinställningar för Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Inställningar för Microsoft Advertising-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Inställningar för japanska annonskampanjer](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Inställningar för Yandex-kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)

