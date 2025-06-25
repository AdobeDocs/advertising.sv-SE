---
title: Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper
description: Lär dig skapa [!DNL Google Ads] kundmatchande målgrupper från era befintliga Adobe Analytics- och Audience Manager-målgrupper.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Skapa [!DNL Google Ads] kundmatchande målgrupper från Adobe Analytics och Audience Manager

*[!DNL Google Ads]konton som är berättigade till kundmatchning är bara*

*Endast annonsörer med integrering mellan Adobe Advertising, Adobe Audience Manager eller Adobe Advertising och Adobe Analytics*

Valfria annonsörer kan skapa [!DNL Google Ads] kundmatchande målgrupper med användar-ID:n från a) [!DNL Analytics] segment som delas med Adobe Experience Cloud och b) Audience Manager-segment som har Search, Social och Commerce som mål, inklusive [!DNL Analytics] segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud Audience Library. Search, Social och Commerce skickar automatiskt en [!DNL Google]-spårnings-URL tillbaka till varje [!DNL Analytics] - eller Audience Manager-segment så att [!DNL Google] kan spåra målgruppen.

Varje [!DNL Adobe]-målgrupp kan bara användas för en [!DNL Google]-målgrupp.

Varje ny [!DNL Google]-målgrupp har samma namn som den ursprungliga [!DNL Adobe]-målgruppen. [!DNL Google] avgör hur stor målgruppen måste vara för att kunna målgruppsanpassas.

>[!TIP]
>
>Använd målgrupper som skapats av Audience Manager för segmentering i realtid. Segment som har skapats i [!DNL Analytics] och synkroniserats med Adobe Experience Cloud kan ha mindre populationer eftersom de bara synkroniseras dagligen. En surfer som kvalificerar sig för ett segment kanske inte inkluderas i segmentet förrän nästa dag. Segment från [!DNL Analytics] har en datakälla av &quot;report suite - .&quot;

>[!NOTE]
>
>Sökning, Socialt och Commerce lagrar inte några kunddata från dina [!DNL Adobe]-segment som används för att skapa eller redigera en [!DNL Google]-målgrupp.

1. Slutför kraven efter behov:

   1. (Om du vill skapa målgrupper med återmarknadsföringslistor för användar-ID) En [!DNL Adobe]-administratör eller kontohanterare måste välja inställningen på annonsörnivå för att aktivera kundmatchning.

   1. Implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) version 2.0 eller senare.

   1. Distribuera följande tagg så högt som möjligt på annonsörens webbsidor som målgruppen ska spåras från

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      där `Advertising_Cloud_UserID` är det unika numeriska användar-ID som tilldelats annonsören.

      Exempel: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Om det inte redan är klart) En behörig användare måste konfigurera annonsörens konto så att det [synkroniseras med annonsörens organisationskonto i Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Markera annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. Välj **[!UICONTROL Adobe Audience]** på menyn **[!UICONTROL Data Source]**.

   1. Välj den [!UICONTROL Adobe Audience] som målgruppen [!DNL Google] ska baseras på.

      >[!NOTE]
      >
      >[!DNL Adobe] målgrupper som redan används för en annan [!DNL Google]-målgrupp är inte tillgängliga.

      Du kan också söka efter målgrupper som innehåller en viss textsträng med minst tre tecken. För alla matchande målgrupper klickar du på **[!UICONTROL Include]** för att markera den.

      Om du väljer flera [!DNL Adobe]-målgrupper skapas en separat [!DNL Google]-målgrupp för varje.

   1. Välj **[!UICONTROL Audience Type]** som ska skapas: **[!UICONTROL Customer List_User ID]**.

      Annonsörens [!DNL Google Ads]-konto måste vara [kvalificerat för anpassad matchning](https://support.google.com/adspolicy/answer/6299717) och vara inanmält för [återmarknadsföring av användar-ID](https://support.google.com/google-ads/answer/9199250).

   1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och sekretesspolicyer för annonsnätverk.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar i målgruppen.

      Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren. Remarketing-listor har en maximal varaktighet på 540 dagar. Kundlistor har inte en maximal varaktighet. Ange 10000 om du vill ange att cookien aldrig upphör att gälla.

   1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] kan ta upp till 24 timmar att bearbeta filen.
>
>* Se [[!DNL Google Ads] dokumentation om hur kundmatchning fungerar och begränsningar](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera kundmatchande målgrupper med kunddatalistor](audience-from-customer-data-list.md)
>* [Hantera dynamiska målgrupper för återmarknadsföring](audience-dynamic-remarketing-manage.md)
