---
title: Skapa en konverteringstagg för  [!DNL Google Ads]
description: Lär dig hur du skapar en  [!DNL Google Ads] konverteringstagg.
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Skapa en konverteringstagg för [!DNL Google Ads]

Du kan skapa konverteringstaggar för nya konverteringar som ska spåras för enskilda [!DNL Google Ads]-konton, som inte spåras på en chefskontonivå.

Om du vill generera konverteringstaggar för befintliga konverteringar använder du annonsnätverkets redigerare.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** på huvudmenyn, som öppnas på fliken **[!UICONTROL Summary]**.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Ange [konverteringstagginställningarna](#conversion-tag-settings-google).

   1. Markera kontot och välj sedan konverteringstyp.

   1. Klicka på **[!UICONTROL Next]**.

   1. Ange konverteringsalternativen.

   1. Klicka på **[!UICONTROL Generate]**.

1. Kopiera konverteringstaggen och implementera den på de webbplatser du vill spåra konverteringsmåtten från.

   Se &quot;Installera taggen [!DNL Google]&quot; i hjälpen för [!DNL Google Ads] till &quot;[&quot;. Konfigurera din Google-tagg ](https://support.google.com/google-ads/answer/12215519).&quot;

1. Klicka på **[!UICONTROL Done].**

När du har lagt till taggarna på webbplatsen och börjar bränna dem konverteras [!DNL Google Ads] poster på webbplatsen. Search, Social och Commerce synkroniserar konverteringarna dagligen. Mer information om synkroniserade data finns i [[!DNL Google Ads] konverteringsdata i Sök, Socialt och Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Inställningar för konverteringstagg {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Det tillämpliga Google Ads-kontot.

**[!UICONTROL Type of Conversion]:** Den typ av konvertering som ska spåras: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* eller *[!UICONTROL Clicks to your number on your mobile website]*. **Obs!** *[!UICONTROL Import conversion]* används i ett annat syfte. Se &quot;[Skapa en konverteringsåtgärd för en [!DNL Google Ads] förbättrad konvertering för leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md).&quot;

**[!UICONTROL Conversion Name]:** Ett unikt namn för konverteringsmåttet.

**\[Konverteringskategori\]:** Konverteringskategorin. Vilka kategorier som är tillgängliga varierar beroende på konverteringstyp. För *[!UICONTROL Calls to a phone number on your website]* och *[!UICONTROL Clicks to your number on your mobile website]* är [!UICONTROL Phone Call Lead] markerat som standard.

**\[Åtgärdstyp\]:** Om målet är en *[!UICONTROL Primary action used for bidding optimization]* eller en *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Så här mäter du [värdet för varje konvertering](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* som kräver att du väljer en valuta och anger värdet för varje konvertering.

* *[!UICONTROL Use a different value for each conversion],* som kräver att du väljer en valuta och anger ett standardvärde för varje konvertering. Du kan ändra standardvärdet i taggen med ett transaktionsspecifikt värde när du implementerar taggen på en viss webbsida.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Hur många konverteringar som ska räknas per klickning eller interaktion ](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* eller *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Det maximala antalet dagar efter en annonsinteraktion som konverteringar registreras för. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL View Through Conversion Window]:** Det maximala antalet dagar efter att en användare visar dina annonser för vilka genomsiktskonverteringar registreras. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL Attribution Model]:** [Hur mycket kredit varje annonsinteraktion får](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* eller *[!UICONTROL Last click]*. **Obs!** Konverteringsåtgärder som tidigare använt *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* eller *[!UICONTROL Position based]* modeller som inte stöds används nu i modellen *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [Överför offlinekonverteringsdata för utökade konverteringar](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads] konverteringsdata i sökningar, sociala medier och Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
