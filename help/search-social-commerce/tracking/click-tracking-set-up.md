---
title: Konfigurera cookie-baserad klickspårning
description: Lär dig hur du konfigurerar och validerar klickspårningstaggar.
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Konfigurera cookie-baserad klickspårning

Följande element måste konfigureras och valideras för att du ska kunna spåra klickningar i Sök, Socialt och Commerce.

1. (Adobe Account Team) Konfigurera annonsören som en pixelkund.

1. [Ange rätt spårningsalternativ för varje annonsörs annonsnätverkskonton och kampanjer](#set-up-click-tracking-options).

1. Vid behov, [generera spårnings-URL:er och överföra dem](#generate-upload-tracking-urls) för vissa kampanjelement.

1. [Validera formatet för några av klickspårnings-URL:erna och testa dem för att validera att rätt landningssida öppnas](#validate-tracking-urls).

## Ställ in spårningsalternativ för annonsnätverkskonton och kampanjer {#set-up-click-tracking-options}

*Kontorsansvarig [!DNL Adobe] endast kontohanterare och administratörsanvändarroller*

1. Gör följande för varje annonsnätverkskonto:

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Håll markören över kontonamnet och klicka ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL Edit]**.

   1. Klicka på **[!UICONTROL Set Account Tracking]**.

   1. För [!UICONTROL Tracking Type] ställa in, välja **[!UICONTROL EF Redirect]**.

   1. (För att tillåta att sökningar, sociala medier och handel utbyter data med Adobe Analytics eller för att spåra konverteringar som sker i [!DNL Apple Safari]) Välj [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Valfritt) Aktivera **[!UICONTROL Auto Upload]** möjlighet att automatiskt överföra nya spårnings-URL:er till annonsnätverket nästa gång som sökningen, sociala medier och handel synkroniseras med det. Det här värdet ärvs som standard för alla kampanjer i kontot, men kan åsidosättas på kampanjnivå.

1. Gör följande för varje kampanj:

   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Håll markören över kampanjnamnet och klicka ![Menyikon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikon")och sedan markera **[!UICONTROL Edit]**.

   1. Klicka på **[!UICONTROL Set Campaign Tracking]**. Välj sedan alternativet att **[!UICONTROL Override Account Tracking]**.

   1. För [!UICONTROL Tracking Type] ställa in, välja **[!UICONTROL EF Redirect]**.

   1. (För att tillåta att sökningar, sociala medier och handel utbyter data med Adobe Analytics eller för att spåra konverteringar som sker i [!DNL Apple Safari]) Välj [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Valfritt) Aktivera **[!UICONTROL Auto Upload]** möjlighet att automatiskt överföra nya spårnings-URL:er till annonsnätverket nästa gång som sökningen, sociala medier och handel synkroniseras med det. Det här värdet ärvs som standard för alla kampanjer i kontot, men kan åsidosättas på kampanjnivå.

## Generera och ladda upp URL:er för spårning {#generate-upload-tracking-urls}

Se &quot;[När och hur klickspårnings-URL:er ska genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### Testa formatet för klickspårnings-URL:er {#validate-tracking-urls}

Verifiera att rätt landningssida öppnas för klickspårnings-URL:en.

1. Mimitera ett reklamklick genom att skicka trafik till annonsörens staging-miljö:

   1. Klistra in en klicknings-URL i en textredigerare, ändra landningssidans URL till att peka mot samma sida i annonsörens testmiljö och klistra sedan in den nya URL:en i webbläsarens adressfält och tryck på **[!DNL Enter]** -tangenten.

   1. Leta efter cookie-filen i webbläsarens lagrade cookies.

   1. Slutför en transaktion på mellanlagringswebbplatsen och verifiera att framgångssidan utlöser rätt pixel. De faktiska parametrarna som spåras av pixeln varierar mellan annonsörs- och spårnings-URL. I följande exempel vill annonsören spåra antalet nya ansökningar och de nya intäkterna:

      För en ny slutanvändare (med en ny cookie) ska följande pixel aktiveras:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Om kakan inte är fräsch ska följande pixel aktiveras:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Upprepa för flera klicknings-URL:er i domänen.

1. Upprepa steg 1 för varje domän och använd olika landningssidor på motsvarande sätt.

1. Om det behövs kan du kontrollera att det går att se pixlarna för transaktions-ID:n i Sök, Socialt och Commerce (`ev_transid`) som genereras under testningen.

>[!MORELIKETHIS]
>
>* [När och hur klickspårnings-URL:er ska genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
