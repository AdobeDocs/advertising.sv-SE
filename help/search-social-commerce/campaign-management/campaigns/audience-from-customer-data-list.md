---
title: Hantera kundmatchande målgrupper med hjälp av kunddatalistor
description: Lär dig hur du skapar och redigerar [!DNL Google Ads] och [!DNL Microsoft Advertising] kundmatchningar utifrån era kunddatalistor.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 46d736c3e14bf407c513c5cb6a153a578aa65121
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] och [!DNL Microsoft Advertising] kundmatchande målgrupper med hjälp av kunddatalistor

Du kan skapa [!DNL Google Ads] och [!DNL Microsoft Advertising] kundmatchande målgrupper från dina kunddatalistor. Du kan även uppdatera alla [!DNL Google Ads]- eller [!DNL Microsoft Advertising] kundmatchande målgrupper, förutom [!DNL Google Ads] målgrupper som skapats från en [!DNL Adobe]-målgrupp.

## Skapa en kundmatchande målgrupp från en kunddatalista

*[!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton som endast är berättigade för kundmatchning*

Du kan skapa en [!DNL Google Ads]- eller [!DNL Microsoft Advertising] kunddatabaserad lista från en datafil som du genererar från CRM-systemet (customer relationship management).

För [!DNL Microsoft Advertising]-konton kan filen innehålla e-postadresser. För [!DNL Google Ads]-konton kan filen innehålla e-postadresser, e-postadresser eller telefonnummer, användar-ID:n eller mobila enhets-ID:n från CRM.

>[!NOTE]
>
>Search, Social och Commerce lagrar inte någon av de kunddata som du överför eller från de [!DNL Adobe] segment som används för att skapa eller redigera en [!DNL Google Ads] eller [!DNL Microsoft Advertising] målgrupp.

1. Generera en fil med kunddata i det format som krävs.

   För- och efternamn, e-postadresser och telefonnummer måste hashas med SHA-256-algoritmen. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> För [!DNL Google Ads] målgrupper, se [!DNL Google Ads]-dokumentationen om [Formateringsriktlinjer för överföring av hash-kodade data](https://support.google.com/google-ads/answer/7476159) för en lista över tillåtna kontaktinformationsfält och krav. För [!DNL Microsoft Advertising] målgrupper, se [!DNL Microsoft Advertising]-dokumentationen om hur du [förbereder kundmatchningslistor](https://help.ads.microsoft.com/#apex/ads/en/56921). Du kan även hämta en [!DNL Microsoft Excel]-mall för kontaktinformation.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Markera annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. Välj **[!UICONTROL Customer List]** på menyn [!UICONTROL Data Source].

   1. Ange **[!UICONTROL Audience Name]**.

   1. Överför filen:

      1. Välj [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* eller *[!UICONTROL Mobile Device IDs]*.

         Alternativet för användar-ID är bara tillgängligt för [!DNL Google Ads] annonsörer i USA som har valts in för [användar-ID-segment](https://support.google.com/google-ads/answer/9199250)

      1. (Endast i listan med mobila enhets-ID) Markera **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* eller *[!UICONTROL iOS]*) och ange **[!UICONTROL App ID]**.

         Program-ID är en unik identifierare som mobiloperativsystemet använder för att tillåta att ditt program ansluter till Google Play eller Apple App Store:

         * ([!DNL Android™] program) Paketnamnet [!DNL Android™] i [!DNL Google Play], identifieras av `id=<package_name>`.

           I `https://play.google.com/store/apps/details?id=com.example.game` är till exempel paketnamnet com.example.game.

         * ([!DNL iOS] appar) Program-ID:t i [!DNL iTunes App Store], som identifieras av `<idNNNNNNNNN>` i slutet av URL:en. Den är också tillgänglig i [!DNL iOS Developer Console].

           I `https://itunes.apple.com/us/app/id284882215` är till exempel ID id284882215.

         Utvecklingsteamet har åtkomst till [!UICONTROL App ID] för den aktuella plattformen.

      1. Klicka på **[!UICONTROL Choose File]** i fältet [!UICONTROL Select File] och markera filen i nätverket eller enheten.

      1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och sekretesspolicyer för annonsnätverk.

      1. (Annonsörer som skapar [!DNL Google Ads] målgrupper som gör affärer i Europeiska ekonomiska samarbetsområdet (EES) eller Storbritannien (UK); valfritt) Om du har inhämtat samtycke från användare i EES och Storbritannien att överföra sina data i annonssyfte markerar du kryssrutan bredvid **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignorerar alla data för EEA- och UK-användare med ospecificerad medgivandestatus. Detta kan leda till diskrepans och prestandaproblem.

      1. Klicka på **[!UICONTROL Upload File]**.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar i målgruppen.

   Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren. Kundlistor förfaller inte om du inte anger ett värde.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>* Annonsnätverket kan ta upp till 24 timmar att bearbeta filen.
>* Se [[!DNL Google Ads] dokumentation om hur kundmatchning fungerar och begränsningar](https://support.google.com/displayvideo/answer/9539301).

## Redigera en kundmatchande målgrupp med hjälp av en kunddatalista

Du kan uppdatera alla [!DNL Google Ads]- eller [!DNL Microsoft Advertising] kundmatchande målgrupper, förutom [!DNL Google Ads] målgrupper som skapats från en [!DNL Adobe]-målgrupp. Du kan överföra data som ska läggas till, tas bort eller ersätta alla befintliga data för målgruppen.

Data måste vara av samma typ som den ursprungliga kundlistan (e-postadresser, e-postadresser, telefonnummer, användar-ID:n eller mobilenhets-ID:n för en viss app i ett visst mobiloperativsystem).

1. Generera en fil med kunddata i det format som krävs för den befintliga datatypen.

För- och efternamn, e-postadresser och telefonnummer måste hashas med SHA-256-algoritmen. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> För [!DNL Google Ads] målgrupper, se [!DNL Google Ads]-dokumentationen om [Formateringsriktlinjer för överföring av hash-kodade data](https://support.google.com/google-ads/answer/7476159) för en lista över tillåtna kontaktinformationsfält och krav. För [!DNL Microsoft Advertising] målgrupper, se [!DNL Microsoft Advertising]-dokumentationen om hur du [förbereder kundmatchningslistor](https://help.ads.microsoft.com/#apex/ads/en/56921. Du kan även hämta en [!DNL Microsoft Excel]-mall för kontaktinformation.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** på undermenyerna.

1. Markera kryssrutan bredvid målgruppen som ska redigeras.

1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png) i verktygsfältet ovanför datatabellen.

1. Välj åtgärden: *[!UICONTROL Add]* (om du vill lägga till överförda data till befintliga data, om det inte redan finns), *[!UICONTROL Delete]* (om du vill ta bort överförda data från befintliga data, om det redan finns) eller *[!UICONTROL Replace]* (om du vill ta bort alla befintliga data och ersätta dem med överförda data).

1. Överför filen:

   1. Klicka på **[!UICONTROL Choose File]** i fältet [!UICONTROL Select File] och markera filen i nätverket eller enheten.

   1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och sekretesspolicyer för annonsnätverk.

   1. Klicka på **[!UICONTROL Upload File]**.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>Annonsnätverket kan ta en stund att bearbeta uppdateringar till en viss målgrupp.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatchande målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera dynamiska målgrupper för återmarknadsföring](audience-dynamic-remarketing-manage.md)
