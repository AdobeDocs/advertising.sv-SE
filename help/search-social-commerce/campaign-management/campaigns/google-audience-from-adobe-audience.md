---
title: Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper
description: Lär dig hur du skapar [!DNL Google Ads] matchar kunderna målgrupper från era befintliga Adobe Analytics- och Audience Manager-målgrupper.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Skapa [!DNL Google Ads] som matchar målgrupper från Adobe Analytics och Audience Manager

*[!DNL Google Ads]konton som endast är berättigade till kundmatchning*

*Annonsörer med enbart integrering mellan Adobe Advertising-Adobe Audience Manager och Adobe Advertising-Adobe Analytics*

Annonsörer som kan väljas in kan skapa [!DNL Google Ads] matchar målgrupper med användar-ID:n från a) [!DNL Analytics] segment som delas med Adobe Experience Cloud och b) Audience Manager-segment som har Sök, Social och Commerce som mål, inklusive [!DNL Analytics] segment som publiceras till Adobe Experience Cloud och segment som skapas med Adobe Experience Cloud Audience Library. Search, Social, &amp; Commerce pushar automatiskt [!DNL Google] spåra URL tillbaka till varje [!DNL Analytics] eller Audience Manager så att [!DNL Google] kan spåra målgruppen.

Varje [!DNL Adobe] kan bara användas för en [!DNL Google] målgrupp.

Varje ny [!DNL Google] målgruppen har samma namn som originalet [!DNL Adobe] målgrupp. [!DNL Google] avgör hur stor målgruppen måste vara för att kunna målgruppsanpassas.

>[!TIP]
>
>Använd målgrupper som skapats i Audience Manager för segmentering i realtid. Segment skapade i [!DNL Analytics] och synkas till Adobe Experience Cloud kan ha mindre populationer eftersom de bara synkroniseras dagligen. en surfer som kvalificerar sig för ett segment kan inte inkluderas i segmentet förrän nästa dag. Segment från [!DNL Analytics] har en datakälla av typen&quot;report suite - .&quot;

>[!NOTE]
>
>Inga kunddata lagras i sökningar, sociala medier och e-handel från din [!DNL Adobe] segment som används för att skapa eller redigera en [!DNL Google] målgrupp.

1. Slutför kraven efter behov:

   1. (För att skapa användare-ID:n för ommarknadsföring listmålgrupper) [!DNL Adobe] Administratörsanvändare eller kontohanterare måste välja inställningen på annonsörnivå för att aktivera kundmatchande målgrupper. Inställningarna skiljer sig mellan annonsörer med Audience Manager och annonsörer med [!DNL Analytics] endast.

   1. Implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) version 2.0 eller senare.

   1. Distribuera följande tagg så högt som möjligt på annonsörens webbsidor som målgruppen ska spåras från

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      där `Advertising_Cloud_UserID` är det unika användar-ID som tilldelats annonsören. Exempel:  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Om det inte redan är ifyllt) En behörig användare måste konfigurera annonsörens konto till [synkronisera med annonsörens organisationskonto i Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. I **[!UICONTROL Data Source]** meny, välja **[!UICONTROL Adobe Audience]**.

   1. Välj [!UICONTROL Adobe Audience] som [!DNL Google] målgrupp.

      >[!NOTE]
      >
      >[!DNL Adobe] målgrupper som redan används för andra [!DNL Google] inte är tillgänglig.

      Du kan också söka efter målgrupper som innehåller en viss textsträng med minst tre tecken. För alla matchande målgrupper klickar du **[!UICONTROL Include]** för att markera den.

      Om du väljer flera [!DNL Adobe] målgrupper, sedan en separat [!DNL Google] målgruppen skapas för varje.

   1. Välj **[!UICONTROL Audience Type]** skapa: **[!UICONTROL Customer List_User ID]**.

      Annonsörens [!DNL Google Ads] kontot måste [kan få anpassad matchning](https://support.google.com/adspolicy/answer/6299717) och har valt att [återmarknadsföring av användar-ID](https://support.google.com/google-ads/answer/9199250).

   1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och annonsera sekretesspolicyer för nätverk.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar kvar hos publiken.

      Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren. Remarketing-listor har en maximal varaktighet på 540 dagar. Kundlistorna har ingen längsta varaktighet; Ange 10000 om du vill ange att cookien aldrig upphör att gälla.

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
>* [Hantera kundmatchande målgrupper med hjälp av kunddatalistor](audience-from-customer-data-list.md)
>* [Hantera målgrupper för dynamisk återmarknadsföring](audience-dynamic-remarketing-manage.md)

