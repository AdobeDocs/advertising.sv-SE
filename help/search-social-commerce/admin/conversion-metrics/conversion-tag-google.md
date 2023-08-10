---
title: Skapa en konverteringstagg för [!DNL Google Ads]
description: Lär dig skapa en [!DNL Google Ads] konverteringstagg.
feature: Conversions
source-git-commit: 8f08151013ec63df14843733a0c83badcceba4c3
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Skapa en konverteringstagg för [!DNL Google Ads]

Du kan skapa konverteringstaggar för nya konverteringar som ska spåras för enskilda [!DNL Google Ads] konton, inte spårade på chefskontonivå.

Om du vill generera konverteringstaggar för befintliga konverteringar använder du annonsnätverkets redigerare.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Ange [konverteringsinställningar](#conversion-tag-settings-google).

   1. Markera kontot och välj sedan konverteringstyp.

   1. Klicka på **[!UICONTROL Next]**.

   1. Ange konverteringsalternativen.

   1. Klicka på **[!UICONTROL Generate]**.

1. Kopiera konverteringstaggen och implementera den på de webbplatser du vill spåra konverteringsmåtten från.

   Se &quot;Installera [!DNL Google] taggen&quot; i [!DNL Google Ads] hjälp att[2. Konfigurera din Google-tagg](https://support.google.com/google-ads/answer/12215519).&quot;

1. Klicka på **[!UICONTROL Done].**

När du har lagt till taggarna på webbplatsen och de börjar skjuta, [!DNL Google Ads] registrerar konverteringar på webbplatsen. Sökning, sociala medier och handel synkroniserar konverteringarna dagligen. Mer information om synkroniserade data finns i &quot;[[!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Inställningar för konverteringstagg {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Google Ads-kontot.

**[!UICONTROL Type of Conversion]:** Den typ av konvertering som ska spåras: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, eller *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Ett unikt namn för konverteringsmåttet.

**\[Målkategori\]:** Konverteringskategorin. Vilka kategorier som är tillgängliga varierar beroende på konverteringstyp. För *[!UICONTROL Calls to a phone number on your website]* och *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; är markerat som standard.

**\[Åtgärdstyp\]:** Om målet är ett *[!UICONTROL Primary action used for bidding optimization]* eller en *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Mät [värde för varje konvertering](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* som kräver att du väljer en valuta och anger värdet för varje konvertering.

* *[!UICONTROL Use a different value for each conversion],* som kräver att du väljer en valuta och anger ett standardvärde för varje konvertering. Du kan ändra standardvärdet i taggen med ett transaktionsspecifikt värde när du implementerar taggen på en viss webbsida.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Hur många konverteringar som ska räknas per klick eller interaktion](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* eller *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Det högsta antal dagar efter en annonsinteraktion som konverteringar registreras för. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL View Through Conversion Window]:** Det högsta antalet dagar efter att en användare har tittat på dina annonser för vilka genomsiktskonverteringar har registrerats. För sök-, display- och shoppingkampanjer kan fönstret vara mellan 1 och 90 dagar. Välj ett tal eller välj **[!UICONTROL Custom]** och ange ett tal.

**[!UICONTROL Attribution Model]:** [Hur mycket kredit varje annonsinteraktion får](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, eller *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] konverteringsdata i sökning, sociala medier och handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
