---
title: Hantera handlarkonton
description: Lär dig hur du konfigurerar och hanterar kontoinformation för ett handlarcenterkonto.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Hantera handlarkonton

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Search, Social, &amp; Commerce kan ladda ned och visa produktdata varje dag för alla annonsörer som har konton på Google Merchant Center eller Microsoft Merchant Center. Dessutom kan sökningar, sociala medier och Commerce automatisera annonsinställningarna baserat på innehållet i handelskontot.Om du vill arbeta direkt med produktdata i sökningar, sociala medier och Commerce måste du skapa en motsvarande kontopost som innehåller inloggningsuppgifterna för kontoåtkomst och med åtkomsten *aktiverad*.

>[!NOTE]
>
>Du kan inte ta bort en handlarkontopost. Du kan inaktivera åtkomst till ett konto genom att ändra kontotypen till *inaktiverad*.

## Skapa information om handelskonto {#create-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om du vill visa produktdata och generera spårningsmallar för ett handlarkonto, och skapa annonser baserade på dessa data, måste du skapa en motsvarande kontopost som innehåller inloggningsuppgifterna för kontot och med åtkomst till kontot *enabled*.

>[!NOTE]
>
>Gå till nätverkets webbplats om du vill skapa ett verkligt konto på handlarnätverket.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** på huvudmenyn, som öppnas på fliken [!UICONTROL Accounts].

1. Klicka på **[!UICONTROL Create Account]** i verktygsfältet ovanför datatabellen.

1. Ange inställningarna för [handlarkontot](#merchant-account-settings):

   1. Välj handlarcenter på menyn [!UICONTROL Product Source].

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Krävs för [!DNL Google Ads]-konton; valfritt för [!DNL Microsoft Advertising]-konton) Tillåt att Search, Social och Commerce får åtkomst till kontot med hjälp av [[!DNL OAuth] auktoriseringsprotokollet](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] endast konton) Välj **[!UICONTROL oAuth]**.

      1. Klicka på **[!UICONTROL Enable Connection]**.

      1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens konto. Det bästa sättet är att använda inloggningsuppgifterna för innehålls-API-åtkomst till handelscentret.

      1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om åtkomst/behörighet.

      1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i fältet **[!UICONTROL oAuth Token]**.

      1. Ange de andra kontoinställningarna.

1. Klicka på **[!UICONTROL Save]**.

   Attributdata för alla produkter i kontot är tillgängliga i Sök, Socialt och Commerce efter nästa dagliga synkroniseringsprocess (cirka 06:00 i användarens lokala tidszon). Sedan kan ni använda produktdata för att automatisera annonsskapandet med hjälp av lagerflöden.

## Redigera information om handelskonto {#edit-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om kontoinloggningsuppgifterna ändras eller du inte längre vill hämta och använda data för ett handlarkonto redigerar du kontoinformationen.

>[!NOTE]
>
>Gå till nätverkets webbplats om du vill redigera ett faktiskt konto på handlarnätverket.

1. Klicka på **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]** på huvudmenyn, som öppnas på fliken [!UICONTROL Accounts].

1. Klicka på ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar") bredvid kontonamnet.

1. Redigera inställningarna för [handlarkontot](#merchant-account-settings).

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social och Commerce måste synkronisera de nya kontodata med de som finns i handelsnätverket. Detta sker automatiskt en gång om dagen kl. 06:00 i användarens lokala tidszon.

## Inaktivera åtkomst till ett handlarkonto {#disable-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

När du inaktiverar ett handlarkonto loggar inte Search, Social och Commerce in på kontot och hämtar därför inte uppdaterade produktdata. Data som samlats in medan kontot aktiverades lagras fortfarande, och befintliga annonser som skapats med produktdata uppdateras, pausas eller tas bort inte enligt inställningarna för matningsmall och matningsdata.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** på huvudmenyn, som öppnas på fliken [!UICONTROL Accounts].

1. Klicka på ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar") bredvid kontonamnet.

1. Ändra [!UICONTROL EF Account Type] till **[!UICONTROL Disabled]**.

1. Klicka på **[!UICONTROL Save]**.

## Inställningar för handelskonto {#merchant-account-settings}

>[!NOTE]
>
>Det är bara kontohanteraren, kontohanteraren för [!DNL Adobe] och administratörsanvändarroller som kan konfigurera inställningar för handelskonton.

**[!UICONTROL Product Source]:** Handelsnätverket. Du kan inte ändra värdet för ett befintligt konto.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] endast konton) Kontots token för att auktorisera inloggningar med [[!DNL OAuth] auktoriseringsprotokollet](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] endast) Anger om inloggningar till kontot ska auktoriseras med:

* *[!UICONTROL Client login]:* Om du vill använda klientens inloggning.

* *[!UICONTROL oAuth]* (standardvärdet): Använder [[!DNL OAuth] auktoriseringsprotokollet](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] endast) Åtkomstnyckeln för utvecklarkontot som ska användas.

**[!UICONTROL Account Name]:** Det namn som visas för kontot i Sök, Socialt och Commerce.

**[!UICONTROL Login]:** Inloggningsnamnet eller ID:t för kontot.

**[!UICONTROL Password]:** Lösenordet för kontot.

**[!UICONTROL Confirm Password]:** Lösenordet för kontot.

**[!UICONTROL EF Account Type]:** Om Search, Social och Commerce har åtkomst till kontot:

* *[!UICONTROL Enabled]* (standardvärdet): Sök, Socialt och Commerce kan logga in på kontot för att hämta produktdata.

* *[!UICONTROL Disabled]:* Search, Social och Commerce loggar inte in på kontot och hämtar därför inte uppdaterade produktdata. Data som samlats in medan kontot aktiverades lagras fortfarande, och befintliga annonser som skapats med produktdata uppdateras, pausas eller tas bort inte enligt inställningarna för matningsmall och matningsdata.

**[!UICONTROL Account ID]:** Handlarens konto-ID. Om du bara har ett konto med den angivna inloggningsinformationen är det här värdet valfritt.

**[!UICONTROL Time Zone]:** Annonsörens tidszon. Använd samma tidszon som konfigurerats för annonsörens kontoinformation för sökning, sociala medier och Commerce (som ställs in när kontot skapas). Du kan inte ändra värdet för ett befintligt konto.

>[!MORELIKETHIS]
>
>* [Om annonskonton](ad-network-account-about.md)
>* [Hantera annonskonton](ad-network-account-manage.md)
