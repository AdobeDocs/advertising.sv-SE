---
title: Hantera handlarkonton
description: Lär dig hur du konfigurerar och hanterar kontoinformation för ett handlarcenterkonto.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: 35a27d075d5de7c3526cd6522376671954b608db
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Hantera handlarkonton

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Sökning, sociala medier och handel kan hämta och visa produktdata varje dag för annonsörens konton på Google Merchant Center eller Microsoft Merchant Center. Dessutom kan sökningar, sociala medier och handel automatisera annonsinställningarna baserat på innehållet i handelskontot.Om du vill arbeta direkt med produktdata i sökningar, sociala medier och handel måste du skapa en motsvarande kontopost som innehåller inloggningsuppgifterna och med åtkomst *aktiverad*.

>[!NOTE]
>
>Du kan inte ta bort en handlarkontopost. Du kan inaktivera åtkomst till ett konto genom att ändra kontotypen till *inaktiverad*.

## Skapa information om handelskonto {#create-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om du vill visa produktdata och generera spårningsmallar för ett handlarkonto, och skapa annonser baserade på dessa data, måste du skapa en motsvarande kontopost som innehåller kontots inloggningsuppgifter och med åtkomst till kontot *aktiverad*.

>[!NOTE]
>
>Gå till nätverkets webbplats om du vill skapa ett verkligt konto på handlarnätverket.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** som öppnas i [!UICONTROL Accounts] -fliken.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create Account]**.

1. Ange [inställningar för handelskonto](#merchant-account-settings):

   1. I [!UICONTROL Product Source] väljer du handlarcentret.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Krävs för [!DNL Google Ads] konton, valfria för [!DNL Microsoft Advertising] konton) Tillåt sökning, sociala medier och handel att komma åt kontot via [[!DNL OAuth] auktoriseringsprotokoll](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] endast konton) Välj **[!UICONTROL oAuth]**.

      1. Klicka på **[!UICONTROL Enable Connection]**.

      1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens konto. Det bästa sättet är att använda inloggningsuppgifterna för innehålls-API-åtkomst till handelscentret.

      1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om åtkomst/behörighet.

      1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i **[!UICONTROL oAuth Token]** fält.

      1. Ange de andra kontoinställningarna.

1. Klicka på **[!UICONTROL Save]**.

   Attributdata för alla produkter i kontot är tillgängliga i Sök, Socialt och Commerce efter nästa dagliga synkroniseringsprocess (cirka 06:00 i användarens lokala tidszon). Sedan kan ni använda produktdata för att automatisera annonsskapandet med hjälp av lagerflöden.

## Redigera information om handelskonto {#edit-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om kontoinloggningsuppgifterna ändras eller du inte längre vill hämta och använda data för ett handlarkonto redigerar du kontoinformationen.

>[!NOTE]
>
>Gå till nätverkets webbplats om du vill redigera ett faktiskt konto på handlarnätverket.

1. Klicka på **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]** som öppnas i [!UICONTROL Accounts] -fliken.

1. Klicka på bredvid kontonamnet ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar").

1. Redigera [inställningar för handelskonto](#merchant-account-settings).

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social, &amp; Commerce måste synkronisera nya kontodata med data i handelsnätverket. Detta sker automatiskt en gång om dagen kl. 06:00 i användarens lokala tidszon.

## Inaktivera åtkomst till ett handlarkonto {#disable-merchant-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

När du inaktiverar ett handlarkonto loggar inte Search, Social och Commerce in på kontot och hämtar därför inte uppdaterade produktdata. Data som samlats in medan kontot aktiverades lagras fortfarande, och befintliga annonser som skapats med produktdata uppdateras, pausas eller tas bort inte enligt inställningarna för matningsmall och matningsdata.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** som öppnas i [!UICONTROL Accounts] -fliken.

1. Klicka på bredvid kontonamnet ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar").

1. Ändra [!UICONTROL EF Account Type] till **[!UICONTROL Disabled]**.

1. Klicka på **[!UICONTROL Save]**.

## Inställningar för handelskonto {#merchant-account-settings}

>[!NOTE]
>
>Endast kontohanterare för byråer, [!DNL Adobe] kontohanteraren och administratörsanvändarroller kan konfigurera inställningar för handelskonton.

**[!UICONTROL Product Source]:** Handlarens nätverk. Du kan inte ändra värdet för ett befintligt konto.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] (endast konton) Kontots token för att auktorisera inloggningar med [[!DNL OAuth] auktoriseringsprotokoll](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] endast) Om inloggningar ska auktoriseras till kontot med:

* *[!UICONTROL Client login]:* Om du vill använda klientens inloggning.

* *[!UICONTROL oAuth]* (standard): Så här använder du [[!DNL OAuth] auktoriseringsprotokoll](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] bara) Åtkomstnyckeln som utvecklarkontot ska använda.

**[!UICONTROL Account Name]:** Namnet som visas för kontot i Sök, Socialt och Handel.

**[!UICONTROL Login]:** Inloggningsnamn eller ID för kontot.

**[!UICONTROL Password]:** Kontots lösenord.

**[!UICONTROL Confirm Password]:** Kontots lösenord.

**[!UICONTROL EF Account Type]:** Om Search, Social och Commerce kommer åt kontot:

* *[!UICONTROL Enabled]* (standard): Sök, Socialt och Commerce kan logga in på kontot för att hämta produktdata.

* *[!UICONTROL Disabled]:* Search, Social, &amp; Commerce loggar inte in på kontot och hämtar därför inte uppdaterade produktdata. Data som samlats in medan kontot aktiverades lagras fortfarande, och befintliga annonser som skapats med produktdata uppdateras, pausas eller tas bort inte enligt inställningarna för matningsmall och matningsdata.

**[!UICONTROL Account ID]:** Handlarens konto-ID. Om du bara har ett konto med den angivna inloggningsinformationen är det här värdet valfritt.

**[!UICONTROL Time Zone]:** Annonsörens tidszon. Använd samma tidszon som konfigurerats för annonsörens kontoinformation för sökning, sociala medier och handel (som anges när kontot skapas). Du kan inte ändra värdet för ett befintligt konto.

>[!MORELIKETHIS]
>
>* [Om och nätverkskonton](ad-network-account-about.md)
>* [Hantera och nätverkskonton](ad-network-account-manage.md)
