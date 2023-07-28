---
title: Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign
description: Lär dig skapa en [!DNL Google Ads] matchar kunderna utifrån en befintlig e-postlista från Adobe Campaign.
exl-id: 967580fc-52c3-42f5-8d60-18cb83bc714a
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign

*[!DNL Google Ads]konton som endast är berättigade till kundmatchning*

Du kan skapa [!DNL Google Ads] genom att skapa en kontolänk och ett arbetsflöde i Adobe Campaign [!DNL Campaign].

Om du vill göra det måste du ha tillgång till [!DNL Campaign] -instans och en XML-fil som innehåller det arbetsflöde som krävs, vilket kontogruppen på Adobe ger dig. Instruktionerna kan variera för olika versioner av [!DNL Campaign]. Om det behövs kan ditt Adobe-kontoteam hjälpa dig att konfigurera arbetsflödet i [!DNL Campaign].

1. Hämta autentiseringsuppgifter för ett SFTP-konto som tillhandahålls av Advertising Search, Social och Commerce.

1. I [!DNL Campaign], konfigurera leverans av e-postlistan till Advertising Search, Social, &amp; Commerce:

   1. Skapa en [externt konto](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) för att länka ditt SFTP-konto som tillhandahålls av Search, Social och Commerce:

      1. Gå till från den vänstra menyn **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Klicka ![Skapa konto](/help/search-social-commerce/assets/campaign-create-account.png "Skapa konto").

      1. Ange en etikett för kontot och välj **[!UICONTROL SFTP]** som kontotyp.

      1. Ange URL och portnummer för [!DNL Adobe] SFTP-server och annonsörens mappnamn, användarnamn och lösenord.

      1. Klicka på **[!UICONTROL Save]**.

   1. I [!DNL Campaign Client]installerar du det datapaket som innehåller det arbetsflöde som krävs för att skicka e-postdata:

      1. Gå till **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Välj **[!UICONTROL Install a package from a file]** och klicka sedan på **[!UICONTROL Next]**.

      1. Leta reda på datapaketfilen (`AMO_Workflow.xml`) på enheten eller nätverket och klicka sedan på **[!UICONTROL Next]**.

      1. Klicka **[!UICONTROL Start]** och vänta på att arbetsflödet ska installeras.

   1. Redigera det installerade arbetsflödet om du vill redigera filtren för datafrågan och identifiera det nya målgruppsnamnet och det externa SFTP-kontot:

      1. Gå till **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** och öppna paketet.

      1. (Valfritt) Redigera något av filtren för data:

         * Dubbelklicka på frågeaktiviteten (till exempel ForkTransition 1) i arbetsflödet.

         * Redigera filteruttrycken.

         * Klicka på **[!UICONTROL Finish]**.

      1. Namnge segmentet:

         * Dubbelklicka på aktiviteten i arbetsflödet **[!UICONTROL Data extraction (File)]**.

         * På sidan **[!UICONTROL Data extraction (File)]** -fliken, i **[!UICONTROL File name]** anger du segmentnamnet med tillägget`.added`&quot; (till exempel PaidSubscribers.added).

           Segmentnamnet får inte redan finnas. Segmentnamnet är skiftlägeskänsligt och måste innehålla ASCII-tecken, men får inte innehålla understreck (`_`).

           Om du vill lägga till segmentet i ett specifikt [!DNL Google Ad] lägg sedan till segmentnamnet med ett understreck och [!UICONTROL User SE Account ID] (ID för sökning, sociala medier och handel för [!DNL Google Ads] konto, inte nätverkets konto-ID):

           `_<User SE Account ID>`

           Exempel: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Det här är ett undantag till regeln som förbjuder understreck i filnamnet.

           Annars läggs segmentet till i alla [!DNL Google Ads] konton som Search, Social och Commerce synkroniserar för annonsören.

         * Lämna alternativet att **[!UICONTROL Generate an outbound transition]** markerat.

         * Klicka på **[!UICONTROL Ok]**.

      1. Ange det externa konto som data ska skickas till:

         * Dubbelklicka på aktiviteten i arbetsflödet **[!UICONTROL File Transfer]**.

         * På sidan **[!UICONTROL File Transfer]** -fliken, i **[!UICONTROL Remote server]** väljer du alternativet att **[!UICONTROL Use an external account]**.

         * I **[!UICONTROL External account]** markerar du etiketten för det externa konto du skapade i steg 2.

         * I **[!UICONTROL Server folder]** väljer du värdet för [!UICONTROL Account] fält för det externa kontot.

         * (Valfritt) På **[!UICONTROL Schedule]** anger du ett annat schema för filöverföringen.

           Som standard körs arbetsflödet vid 00:00 (midnatt), vilket säkerställer att alla poster behandlas. Om du vill minimera fördröjningen schemalägger du arbetsflödet att köras senast 18:00.

         * Klicka på **[!UICONTROL Ok]**.

Search, Social, &amp; Commerce kontrollerar katalogen var 30:e minut (på NN:30 och NN:59 i annonsörens tidszon) och flyttar alla filer som hittas till en annan plats, och skapar sedan automatiskt en målgrupp från data och överför den till Google kl. 22:00 (kl. 10). Sökning, sociala medier och handel fortsätter att söka efter uppdateringar (tillägg och subtraktioner) i e-postlistan var 30:e minut och uppdaterar publiken på [!DNL Google Ads] därefter kl. 22.00 dagligen.

>[!NOTE]
>
>* Om du överför mer än en version av en fil mellan bearbetningscyklerna används den senaste filen.
>
>* Sökning, sociala medier och handel lagrar inte någon kundinformation från dina e-postlistor som används för att skapa eller redigera en [!DNL Google Ads] målgrupp.
>
>* [!DNL Google Ads] kan ta ett tag att bearbeta uppdateringar till en viss målgrupp.
>
>* Se [[!DNL Google Ads] dokumentation om hur kundmatchning fungerar och begränsningar](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Hantera kundmatchande målgrupper med hjälp av kunddatalistor](audience-from-customer-data-list.md)
>* [Hantera målgrupper för dynamisk återmarknadsföring](audience-dynamic-remarketing-manage.md)
