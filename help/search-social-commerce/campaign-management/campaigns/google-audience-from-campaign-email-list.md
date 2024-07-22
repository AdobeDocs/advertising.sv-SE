---
title: Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign
description: Lär dig hur du skapar en [!DNL Google Ads] kundmatchande målgrupp utifrån en befintlig e-postlista från Adobe Campaign.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign

*[!DNL Google Ads]konton som är berättigade till kundmatchning är bara*

Du kan skapa en [!DNL Google Ads]-kundmatchande målgrupp från en e-postlista i Adobe Campaign genom att konfigurera en kontolänk och ett arbetsflöde i [!DNL Campaign].

För att kunna göra det måste du ha tillgång till din [!DNL Campaign]-instans och en XML-fil som innehåller det arbetsflöde som krävs, och som kontogruppen på Adobe ger dig. Instruktionerna kan variera för olika versioner av [!DNL Campaign]. Om det behövs kan ditt Adobe Account Team hjälpa dig att konfigurera arbetsflödet i [!DNL Campaign].

1. Hämta autentiseringsuppgifter för ett SFTP-konto som tillhandahålls av Advertising Search, Social och Commerce.

1. I [!DNL Campaign] anger du leverans av e-postlistan till Advertising Search, Social och Commerce:

   1. Skapa ett [externt konto](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) för att länka ditt SFTP-konto som tillhandahålls av Search, Social och Commerce:

      1. Gå till **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]** på den vänstra menyn.

      1. Klicka på ![Skapa konto](/help/search-social-commerce/assets/campaign-create-account.png "Skapa konto").

      1. Ange en etikett för kontot och välj **[!UICONTROL SFTP]** som kontotyp.

      1. Ange URL:en och portnumret för SFTP-servern [!DNL Adobe] samt annonsörens mappnamn, användarnamn och lösenord.

      1. Klicka på **[!UICONTROL Save]**.

   1. I [!DNL Campaign Client] installerar du det datapaket som innehåller det arbetsflöde som krävs för att skicka e-postdata:

      1. Gå till **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]** från menyraden.

      1. Välj **[!UICONTROL Install a package from a file]** och klicka sedan på **[!UICONTROL Next]**.

      1. Leta reda på datapaketfilen (`AMO_Workflow.xml`) på enheten eller nätverket och klicka sedan på **[!UICONTROL Next]**.

      1. Klicka på **[!UICONTROL Start]** och vänta tills arbetsflödet har installerats.

   1. Redigera det installerade arbetsflödet om du vill redigera filtren för datafrågan och identifiera det nya målgruppsnamnet och det externa SFTP-kontot:

      1. Gå till **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** och öppna paketet.

      1. (Valfritt) Redigera något av filtren för data:

         * Dubbelklicka på frågeaktiviteten (till exempel ForkTransition 1) i arbetsflödet.

         * Redigera filteruttrycken.

         * Klicka på **[!UICONTROL Finish]**.

      1. Namnge segmentet:

         * Dubbelklicka på aktiviteten **[!UICONTROL Data extraction (File)]** i arbetsflödet.

         * På fliken **[!UICONTROL Data extraction (File)]** anger du segmentnamnet med tillägget `.added` i fältet **[!UICONTROL File name]** (till exempel PaidSubscribers.added).

           Segmentnamnet får inte redan finnas. Segmentnamnet är skiftlägeskänsligt och måste innehålla ASCII-tecken, men får inte innehålla understreck (`_`).

           Om du vill lägga till segmentet i ett specifikt [!DNL Google Ad]-konto lägger du till segmentnamnet med ett understreck och [!UICONTROL User SE Account ID] (ID för sökning, sociala medier och Commerce för [!DNL Google Ads]-kontot, inte nätverkets konto-ID):

           `_<User SE Account ID>`

           Exempel: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Det här är ett undantag till regeln som förbjuder understreck i filnamnet.

           Annars läggs segmentet till i alla [!DNL Google Ads]-konton som Search, Social och Commerce synkroniserar för annonsören.

         * Låt alternativet **[!UICONTROL Generate an outbound transition]** vara markerat.

         * Klicka på **[!UICONTROL Ok]**.

      1. Ange det externa konto som data ska skickas till:

         * Dubbelklicka på aktiviteten **[!UICONTROL File Transfer]** i arbetsflödet.

         * Gå till fliken **[!UICONTROL File Transfer]** och välj alternativet **[!UICONTROL Use an external account]** i avsnittet **[!UICONTROL Remote server]**.

         * I fältet **[!UICONTROL External account]** väljer du etiketten för det externa konto du skapade i steg 2.

         * I fältet **[!UICONTROL Server folder]** väljer du värdet för fältet [!UICONTROL Account] för det externa kontot.

         * (Valfritt) Ange ett annat schema för filöverföringen på fliken **[!UICONTROL Schedule]**.

           Som standard körs arbetsflödet vid 00:00 (midnatt), vilket säkerställer att alla poster behandlas. Om du vill minimera fördröjningen schemalägger du arbetsflödet att köras senast 18:00.

         * Klicka på **[!UICONTROL Ok]**.

Search, Social, &amp; Commerce söker igenom katalogen var 30:e minut (på NN:30 och NN:59 i annonsörens tidszon) och flyttar alla filer som hittas till en annan plats, och skapar sedan automatiskt en målgrupp utifrån dessa data och överför den till Google kl. 22:00 (kl. 23). Search, Social, &amp; Commerce fortsätter att söka efter uppdateringar (tillägg och subtraktioner) i e-postlistan var 30:e minut och uppdaterar målgruppen på [!DNL Google Ads] därefter kl. 22:00 dagligen.

>[!NOTE]
>
>* Om du överför mer än en version av en fil mellan bearbetningscyklerna används den senaste filen.
>
>* Search, Social och Commerce lagrar inte kunddata från dina e-postlistor som används för att skapa eller redigera en [!DNL Google Ads]-målgrupp.
>
>* [!DNL Google Ads] kan ta ett tag att bearbeta uppdateringar till en målgrupp.
>
>* Se [[!DNL Google Ads] dokumentation om hur kundmatchning fungerar och begränsningar](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Hantera kundmatchande målgrupper med kunddatalistor](audience-from-customer-data-list.md)
>* [Hantera dynamiska målgrupper för återmarknadsföring](audience-dynamic-remarketing-manage.md)
