---
title: Hantera [!DNL Google Ads] platstillägg
description: Lär dig skapa och hantera [!DNL Google Ads] platstillägg.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] platstillägg

I ett platstillägg visas din företagsadress, ditt klickbara telefonnummer och en kartmarkör med din textannons. Annonser som visas på mobila enheter innehåller en länk med anvisningar till ditt företag. [!DNL Google Ads] platstillägg använder information från [länkad [!DNL Google My Business] konto](https://support.google.com/google-ads/answer/2404182).

Du kan skapa platstillägg på både kampanj- och annonsgruppsnivå. När en kampanj eller annonsgrupp har flera platstillägg, visas annonsnätverket det som är närmast användaren. Du kan även inaktivera alla platstillägg för specifika [!DNL Google Ads] kampanjer och annonsgrupper från platsens tilläggsinställningar.

## Prestandadata för platstillägg

Annonsnätverket mappar klickningarna på ett platstillägg till det nyckelord som är associerat med annonsen som tillägget ingår i.  Det finns inga kostnadsdata eller klickdata på tilläggsnivån tillgängliga i Sök, Socialt och Commerce. I [!DNL Google Ads]kan du se kostnad och klicka på data på [!DNL Campaigns] tab > [!DNL Ad Extensions] -fliken. Eftersom det inte finns någon URL att spåra för platstillägg kan inte konverteringsdata rapporteras för dem i Sök, Socialt och Commerce.

*[!DNL Google Ads]endast konton*

## Skapa platstillägg för kampanjer och annonsgrupper

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Associations]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa")och sedan markera **[!UICONTROL Location]**.

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange [inställningar för platstillägg](#location-extension-settings):

   * I [!UICONTROL Location Settings] anger du platserna.

   * I [!UICONTROL Assignment] väljer du de kampanjer och annonser som platsinställningarna gäller för.

1. Klicka på **[!UICONTROL Post]**.

## Inaktivera platstillägg för kampanjer och annonsgrupper

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Associations]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa")och sedan markera **[!UICONTROL Location]**.

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange [inställningar för platstillägg](#location-extension-settings):

   * I [!UICONTROL Location Settings] avsnitt, markera **[!UICONTROL Disable Locations]**.

   * I [!UICONTROL Assignment] väljer du de kampanjer och annonser som platsinställningarna gäller för.

1. Klicka på **[!UICONTROL Post]**.

## Inställningar för platstillägg för Google Ads {#location-extension-settings}

### [!UICONTROL Location Settings]

Vilka affärsplatser för en [länkat Google My Business-konto](https://support.google.com/google-ads/answer/2404182?vid=1-635794239083658097-1242615452#link) kan användas i platstillägg för de angivna kampanjerna och annonsgrupperna:

* *[!UICONTROL All Locations]:* Om du vill använda platserna för alla företag i det länkade kontot.

* *[!UICONTROL Locations matching filter]:* Ange ett företagsnamn och eventuellt upp till tre företagskategorier, som företagen i det länkade kontot kan filtreras med.

* *[!UICONTROL Locations I pick]:* Välj från en lista över alla företag i det länkade kontot. Om du vill välja ett företag klickar du på namnet och flyttar det sedan till den högra kolumnen genom att klicka.

* *[!UICONTROL Disable Locations]:* Inaktiverar alla platstillägg för de angivna kampanjerna eller annonsgrupperna.

### [!UICONTROL Assignment]

**[!UICONTROL Campaigns/Ad Groups]:** De kampanjer och annonseringsgrupper som platsinställningarna gäller för.

* Om du vill visa de underordnade entiteterna för en kampanj klickar du på kampanjnamnet.

* Om du vill filtrera en kampanjlista eller annonsgrupplista med en textsträng som ingår i namnet klickar du på ![Filter](/help/search-social-commerce/assets/filter.png "Filter"), antingen anger eller klistrar in textsträngen i inmatningsfältet och trycker sedan på **Retur** nyckel.

* Om du vill välja en enhet klickar du på cirkeln bredvid den (![Välj](/help/search-social-commerce/assets/include.png "Välj")).
