---
title: Skapa en konverteringsåtgärd för en  [!DNL Google Ads] förbättrad konvertering för leads
description: Lär dig hur du skapar en  [!DNL Google Ads] konverteringsåtgärd för en förbättrad konvertering av leads.
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Skapa en konverteringsåtgärd för en [!DNL Google Ads] förbättrad konvertering för leads

Endast *[!DNL Google Ads]konton*

Du kan skapa konverteringsåtgärder för [!DNL Google Ads] förbättrade konverteringar för leads som ska spåras för enskilda [!DNL Google Ads]-konton, inte konverteringar som spåras på en chefskontonivå.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** på huvudmenyn, som öppnar fliken **[!UICONTROL Summary]**.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Ange inställningar för [konverteringsåtgärd](#conversion-action-settings-google).

   1. Markera kontot och välj sedan konverteringstypen: *[!UICONTROL Import conversion]*.

   1. Klicka på **[!UICONTROL Next]**.

   1. Ange alternativ för konverteringsåtgärd.

   1. Klicka på **[!UICONTROL Generate]**.

1. Läs information om hur du skapar en spårningstagg för den förbättrade konverteringen för leads och klicka sedan på **[!UICONTROL Next]**.

   Skapa konverteringstaggen och implementera den efter behov på de webbplatser som du vill spåra konverteringsmåtten från. Instruktioner finns i följande:

   * Information om hur du använder taggen [!DNL Google] finns i [!DNL Google Ads]-instruktionerna för att konfigurera [!DNL Google]-tagginställningar i [Konfigurera förbättrade konverteringar för leads med taggen  [!DNL Google] ](https://support.google.com/google-ads/answer/11347292).

   * Information om hur du använder [!DNL Google Tag Manager] finns i [!DNL Google Ads]-instruktionerna för att konfigurera [!DNL Google]-tagginställningar och för att verifiera konfigurationen och publicera behållaren i [Konfigurera förbättrade konverteringar för leads med [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure).

1. Klicka på **[!UICONTROL Done].**

När du har skapat konverteringsåtgärden och implementerat en konverteringsspårningstagg kan du överföra offlinekonverteringsdata som din organisation hämtar och tilldela dem till konverteringsåtgärden. Se [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md).

## Inställningar för konverteringsåtgärd {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** Det tillämpliga Google Ads-kontot.

**[!UICONTROL Type of Conversion]:** Den typ av konvertering som ska spåras: Välj *[!UICONTROL Import conversion]*. Alla andra typer används för att skapa konverteringsspårningstaggar (inte konverteringsåtgärder) för andra typer av konverteringar.

**[!UICONTROL Conversion Name]:** Ett unikt namn för konverteringsåtgärden.

**\[Konverteringskategori\]:** Konverteringskategorin, till exempel *Kvalificerad lead* eller *Registrering*.

**\[Åtgärdstyp\]:** Om målet är en *[!UICONTROL Primary action used for bidding optimization]* eller en *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Så här mäter du [värdet för varje konvertering](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* som kräver att du väljer en valuta och anger värdet för varje konvertering.

* *[!UICONTROL Use a different value for each conversion],* som kräver att du väljer en valuta och anger ett standardvärde för varje konvertering. Du kan ändra standardvärdet i taggen med ett transaktionsspecifikt värde när du implementerar taggen på en viss webbsida.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Hur många konverteringar som ska räknas per klickning eller interaktion ](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* eller *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Det maximala antalet dagar efter en annonsinteraktion som konverteringar registreras för. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL View Through Conversion Window]:** Det maximala antalet dagar efter att en användare visar dina annonser för vilka genomsiktskonverteringar registreras. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL Attribution Model]:** [Hur mycket kredit varje annonsinteraktion får](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* eller *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementera [!DNL Google Ads] förbättrade konverteringar för leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
