---
title: Hantera målgruppsmål för kampanjer och annonsgrupper
description: Lär dig hur du konfigurerar och hanterar målgruppsmål för  [!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer och annonsgrupper.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Hantera målgruppsmål för era [!DNL Google Ads]- och [!DNL Microsoft Advertising]-kampanjer och annonsgrupper

*[!DNL Google Ads]och [!DNL Microsoft Advertising] only*

[!DNL Google Ads] kampanjer och annonsgrupper, och [!DNL Microsoft Advertising] annonsgrupper, kan rikta sig till specifika målgrupper från samma annonsnätverk. Annonsnätverket avgör hur stor en målgrupp måste vara för att kunna målgruppsanpassas.

>[!NOTE]
>
>Undantag åsidosätter alltid inkluderingar/mål.

Ni kan konfigurera målgruppsmål, redigera budmodifierare för målgruppsmål och ändra status för målgruppsmål.

## Konfigurera målgruppsmål

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Markera annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Konfigurera målgruppsmålen för specifika kampanjer och annonsgrupper:

   1. Välj vilka målgrupper som ska användas för det angivna annonsnätverket.

      Du kan också söka efter målgrupper som innehåller en viss textsträng med minst tre tecken. För alla matchande målgrupper klickar du på **[!UICONTROL Include]** för att markera den.

      [!DNL Google Ads] kundmatchande målgrupper är bara tillgängliga för sök- och shoppingkampanjer.

   1. Ange mål:

      1. (Valfritt) Klicka på kampanjnamnet om du vill expandera en kampanj till dess underordnade annonsgrupper.

      1. (Valfritt) Om du vill filtrera en kampanjlista eller en annonsgrupplista med en textsträng som ingår i namnet klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") , anger eller klistrar in textsträngen i indatafältet och trycker sedan på **[!UICONTROL Enter]** .

      1. Ange varje kampanj- och annonsgruppsmål för det angivna annonsnätverket genom att klicka på den intilliggande tomma cirkeln så att en blå bock (![Select](/help/search-social-commerce/assets/include.png "Select")) visas.

      Du kan inte konfigurera ett mål för både en överordnad kampanj och en underordnad annonsgrupp (som automatiskt använder målet).

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Ange en anbudsjustering för målet på något av följande sätt i vyn [!UICONTROL Targets]:

   * Klicka i kolumnen **[!UICONTROL Bid Adjustment]** och ange ett värde.

   * Markera kryssrutan bredvid målraden. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet, ange budmodifieraren och klicka sedan på **[!UICONTROL Post]**.

   Värdena kan vara:

   * *0%:* Om du inte vill justera annonser för den här målgruppen.

   * /[*Andra värden från -90 % till 900 %*/]: Om du vill öka eller minska antalet annonser för den här målgruppen. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för ett specifikt målgruppsmål är 50 %, ökar anbudet för den målgruppen till 1,50 USD.

## Redigera anbudsmodifieraren för målgruppsmål

Ni kan ändra anbudsmodifieraren och statusen för målgruppsmål för alla målgruppstyper utom för målgrupper på marknaden.

>[!NOTE]
>
>Search, Social och Commerce optimerar automatiskt budmodifieraren när den överordnade kampanjen använder CPC:s budstrategi och finns i en portfölj som konfigurerats för automatisk optimering av anbudsjusteringsvärden för målgrupper.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** på undermenyerna.

1. Gör något av följande:

   * Om du vill redigera en budmodifierare för ett mål klickar du i kolumnen **[!UICONTROL Bid Adjustment]** och redigerar budjusteringen.

   * Så här redigerar du en budmodifierare för ett eller flera mål:

      1. Markera kryssrutan bredvid varje mål som ska redigeras.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet ovanför datatabellen.

      1. Redigera fälten **[!UICONTROL Bid Modifier]** och/eller **[!UICONTROL Status]**.

         För fältet [!UICONTROL Bid Modifier] kan du ändra befintliga värden till ett angivet värde eller antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

         För ett angivet värde kan värdet innehålla:

         * *0%:* Om du inte vill justera annonser för den här målgruppen.

         * /[*Andra värden från -90 % till 900 %*/]: Om du vill öka eller minska antalet annonser för den här målgruppen. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för ett specifikt målgruppsmål är 50 %, ökar anbudet för den målgruppen till 1,50 USD.

         För flera mål tillämpas ändringarna på alla valda mål.

      1. (Valfritt) Klicka på **[!UICONTROL Additional Details]** och ange eventuellt ett projektnamn och en beskrivning.

      1. Klicka på **[!UICONTROL Post]**.

## Ändra status för målgruppsmål

Du kan pausa ett aktivt målgruppsmål om du vill inaktivera budgivning på det. Du kan återuppta offerten senare genom att ändra status till aktiv.

Du kan också ta bort ett aktivt eller pausat sökmålgruppsmål.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** på undermenyerna.

1. (Valfritt) Filtrera listan så att den innehåller specifika målgruppsmål.

1. Markera kryssrutan bredvid varje målgruppsmål vars status du vill ändra.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicka på statusknappen i verktygsfältet:

   * Aktivera raderna genom att klicka på ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera").

   * Om du vill pausa raderna klickar du på ![Paus](/help/search-social-commerce/assets/pause.png "Paus").

   * Om du vill ta bort raderna klickar du på ![Fler åtgärder](/help/search-social-commerce/assets/more.png "Fler åtgärder") och väljer **[!UICONTROL Delete]**. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Hantera publikundantag för kampanjer och annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
