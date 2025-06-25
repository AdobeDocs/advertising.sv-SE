---
title: Konfigurera cookie-baserad klickspårning
description: Lär dig hur du konfigurerar och validerar klickspårningstaggar.
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Konfigurera cookie-baserad klickspårning

För att det ska gå att spåra klickningar i Search, Social och Commerce måste följande element konfigureras och valideras.

1. (Adobe Account Team) Konfigurera annonsören som en pixelkund.

1. [Ange rätt spårningsalternativ för varje annonsörs annonsnätverkskonton och kampanjer](#set-up-click-tracking-options).

1. Om det behövs kan [generera spårnings-URL:er och överföra dem](#generate-upload-tracking-urls) för vissa kampanjelement.

1. [Verifiera formatet för några av klickspårnings-URL:erna och testa dem för att verifiera att rätt landningssida öppnas](#validate-tracking-urls).

## Ställ in spårningsalternativ för annonsnätverkskonton och kampanjer {#set-up-click-tracking-options}

*Endast kontohanterare, [!DNL Adobe] kontohanterare och administratörsanvändarroller*

1. Gör följande för varje annonsnätverkskonto:

   1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Accounts]** på undermenyerna.

   1. Håll markören över kontonamnet, klicka på ![menyikonen](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikonen") och välj sedan **[!UICONTROL Edit]**.

   1. Klicka på **[!UICONTROL Set Account Tracking]**.

   1. Välj **[!UICONTROL EF Redirect]** för inställningen [!UICONTROL Tracking Type].

   1. (Om du vill tillåta att sökningar, sociala medier och Commerce kan utbyta data med Adobe Analytics eller spåra konverteringar som inträffar i [!DNL Apple Safari]) väljer du [!UICONTROL Redirect Type] alternativ **[!UICONTROL Token]**.

   1. (Valfritt) Aktivera alternativet **[!UICONTROL Auto Upload]** om du automatiskt vill överföra nya spårnings-URL:er till annonsnätverket nästa gång som sökningen, sociala medier och Commerce synkroniseras med det. Det här värdet ärvs som standard för alla kampanjer i kontot, men kan åsidosättas på kampanjnivå.

1. Gör följande för varje kampanj:

   1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]>[!UICONTROL Campaigns]** på undermenyerna.

   1. Håll markören över kampanjnamnet, klicka på ![menyikonen](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menyikonen") och välj sedan **[!UICONTROL Edit]**.

   1. Klicka på **[!UICONTROL Set Campaign Tracking]**. Välj sedan alternativet **[!UICONTROL Override Account Tracking]**.

   1. Välj **[!UICONTROL EF Redirect]** för inställningen [!UICONTROL Tracking Type].

   1. (Om du vill tillåta att sökningar, sociala medier och Commerce kan utbyta data med Adobe Analytics eller spåra konverteringar som inträffar i [!DNL Apple Safari]) väljer du [!UICONTROL Redirect Type] alternativ **[!UICONTROL Token]**.

   1. (Valfritt) Aktivera alternativet **[!UICONTROL Auto Upload]** om du automatiskt vill överföra nya spårnings-URL:er till annonsnätverket nästa gång som sökningen, sociala medier och Commerce synkroniseras med det. Det här värdet ärvs som standard för alla kampanjer i kontot, men kan åsidosättas på kampanjnivå.

## Generera och ladda upp URL:er för spårning {#generate-upload-tracking-urls}

Se &quot;[När och hur klickspårnings-URL:er](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) ska genereras.&quot;

### Testa formatet för klickspårnings-URL:er {#validate-tracking-urls}

Verifiera att rätt landningssida öppnas för klickspårnings-URL:en.

1. Mimitera ett reklamklick genom att skicka trafik till annonsörens staging-miljö:

   1. Klistra in en klickningsspårnings-URL i en textredigerare, ändra landningssidans URL till att peka mot samma sida i annonsörens testmiljö och klistra sedan in den nya URL:en i webbläsarens adressfält och tryck på **[!DNL Enter]**.

   1. Leta efter cookie-filen i webbläsarens lagrade cookies.

   1. Slutför en transaktion på mellanlagringswebbplatsen och verifiera att framgångssidan utlöser rätt pixel. De faktiska parametrarna som spåras av pixeln varierar mellan annonsörs- och spårnings-URL. I följande exempel vill annonsören spåra antalet nya ansökningar och de nya intäkterna:

      För en ny slutanvändare (med en ny cookie) ska följande pixel aktiveras:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Om kakan inte är fräsch ska följande pixel aktiveras:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Upprepa för flera klicknings-URL:er i domänen.

1. Upprepa steg 1 för varje domän och använd olika landningssidor på motsvarande sätt.

1. Om det behövs kan du kontrollera att det går att se pixlarna för transaktions-ID:n (`ev_transid`) som genererats under testningen i Search, Social och Commerce.

>[!MORELIKETHIS]
>
>* [När och hur klickspårnings-URL:er genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
