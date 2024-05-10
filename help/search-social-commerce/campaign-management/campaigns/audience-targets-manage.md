---
title: Hantera målgruppsmål för kampanjer och annonsgrupper
description: Lär dig konfigurera och hantera målgruppsmål för [!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer och annonsgrupper.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Hantera målgruppsanpassningar för [!DNL Google Ads] och [!DNL Microsoft Advertising] kampanjer och annonsgrupper

*[!DNL Google Ads]och [!DNL Microsoft Advertising] endast*

[!DNL Google Ads] kampanjer och annonsgrupper, och [!DNL Microsoft Advertising] annonsgrupper, kan inrikta sig på specifika målgrupper från samma annonsnätverk. Annonsnätverket avgör hur stor en målgrupp måste vara för att kunna målgruppsanpassas.

>[!NOTE]
>
>Undantag åsidosätter alltid inkluderingar/mål.

Ni kan konfigurera målgruppsmål, redigera budmodifierare för målgruppsmål och ändra status för målgruppsmål.

## Konfigurera målgruppsmål

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Konfigurera målgruppsmålen för specifika kampanjer och annonsgrupper:

   1. Välj vilka målgrupper som ska användas för det angivna annonsnätverket.

      Du kan också söka efter målgrupper som innehåller en viss textsträng med minst tre tecken. För alla matchande målgrupper klickar du **[!UICONTROL Include]** för att markera den.

      [!DNL Google Ads] målgrupper som matchar kunderna är bara tillgängliga för sök- och shoppingkampanjer.

   1. Ange mål:

      1. (Valfritt) Klicka på kampanjnamnet om du vill expandera en kampanj till dess underordnade annonsgrupper.

      1. (Valfritt) Om du vill filtrera en kampanjlista eller annonsgrupplista med en textsträng som ingår i namnet klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter") , antingen anger eller klistrar in textsträngen i indatafältet och trycker sedan på **[!UICONTROL Enter]** -tangenten.

      1. Ange varje kampanj och annonsgruppmål för det angivna annonsnätverket genom att klicka på den intilliggande tomma cirkeln så att en blå bock (![Välj](/help/search-social-commerce/assets/include.png "Välj")) visas.

      Du kan inte konfigurera ett mål för både en överordnad kampanj och en underordnad annonsgrupp (som automatiskt använder målet).

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Ange en anbudsjustering för målet på något av följande sätt från [!UICONTROL Targets] vy:

   * Klicka på **[!UICONTROL Bid Adjustment]** och ange ett värde.

   * Markera kryssrutan bredvid målraden. Klicka på i verktygsfältet ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera"), ange budmodifieraren och klicka sedan på **[!UICONTROL Post]**.

   Värdena kan vara:

   * *0 %:* Att inte justera anbuden för annonser för den här målgruppen.

   * /[*Andra värden från -90 % till 900 %*/]: Att öka eller minska antalet annonser för den här målgruppen. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för ett specifikt målgruppsmål är 50 %, ökar anbudet för den målgruppen till 1,50 USD.

## Redigera anbudsmodifieraren för målgruppsmål

Ni kan ändra anbudsmodifieraren och statusen för målgruppsmål för alla målgruppstyper utom för målgrupper på marknaden.

>[!NOTE]
>
>Search, Social och Commerce optimerar automatiskt budmodifieraren när den överordnade kampanjen använder CPC:s budstrategi och finns i en portfölj som konfigurerats för automatisk optimering av anbudsjusteringsvärden för målgrupper.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Gör något av följande:

   * Om du vill redigera en budmodifierare för ett mål klickar du på **[!UICONTROL Bid Adjustment]** och redigera budjusteringen.

   * Så här redigerar du en budmodifierare för ett eller flera mål:

      1. Markera kryssrutan bredvid varje mål som ska redigeras.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

      1. Redigera **[!UICONTROL Bid Modifier]** och/eller **[!UICONTROL Status]** fält.

         För [!UICONTROL Bid Modifier] har du möjlighet att ändra befintliga värden till ett angivet värde eller att antingen öka eller minska beloppet med en angiven procentandel eller ett penningbelopp, med en gräns.

         För ett angivet värde kan värdet innehålla:

         * *0 %:* Att inte justera anbuden för annonser för den här målgruppen.

         * /[*Andra värden från -90 % till 900 %*/]: Att öka eller minska antalet annonser för den här målgruppen. Om t.ex. anbudet på nyckelordsnivå är 1 USD och budjusteringen för ett specifikt målgruppsmål är 50 %, ökar anbudet för den målgruppen till 1,50 USD.

         För flera mål tillämpas ändringarna på alla valda mål.

      1. (Valfritt) Klicka på **[!UICONTROL Additional Details]** och kan även ange ett projektnamn och en beskrivning.

      1. Klicka på **[!UICONTROL Post]**.

## Ändra status för målgruppsmål

Du kan pausa ett aktivt målgruppsmål om du vill inaktivera budgivning på det. Du kan återuppta offerten senare genom att ändra status till aktiv.

Du kan också ta bort ett aktivt eller pausat sökmålgruppsmål.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Valfritt) Filtrera listan så att den innehåller specifika målgruppsmål.

1. Markera kryssrutan bredvid varje målgruppsmål vars status du vill ändra.

   Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicka på statusknappen i verktygsfältet:

   * Aktivera raderna genom att klicka ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera").

   * Om du vill pausa raderna klickar du på ![Pausa](/help/search-social-commerce/assets/pause.png "Pausa").

   * Klicka på om du vill ta bort raderna ![Fler åtgärder](/help/search-social-commerce/assets/more.png "Fler åtgärder") och markera **[!UICONTROL Delete]**. Klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Hantera publikundantag för kampanjer och annonsgrupper](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
