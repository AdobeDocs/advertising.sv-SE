---
title: Hantera kundmatchande målgrupper med hjälp av kunddatalistor
description: Lär dig skapa och redigera [!DNL Google Ads] och [!DNL Microsoft® Advertising] matchar kunderna målgrupper utifrån era kunddatalistor.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Hantera [!DNL Google Ads] och [!DNL Microsoft® Advertising] kundmatcha målgrupper med hjälp av kunddatalistor

Du kan [!DNL Google Ads] och [!DNL Microsoft® Advertising] matchar kunderna målgrupper utifrån era kunddatalistor. Du kan även uppdatera [!DNL Google Ads] eller [!DNL Microsoft® Advertising] målgrupp med kundmatchning förutom [!DNL Google Ads] målgrupper skapade från en [!DNL Adobe] målgrupp.

## Skapa en kundmatchande målgrupp från en kunddatalista

*[!DNL Google Ads]och [!DNL Microsoft® Advertising] konton som endast är berättigade till kundmatchning*

Du kan skapa [!DNL Google Ads] eller [!DNL Microsoft® Advertising] kunddatabaserad lista från en datafil som du genererar från CRM-systemet (customer relationship management).

För [!DNL Microsoft® Advertising] kan filen innehålla e-postadresser. För [!DNL Google Ads] kan filen innehålla e-postadresser, e-postadresser eller telefonnummer, användar-ID:n eller mobila enhets-ID:n från CRM.

>[!NOTE]
>
>Sök, Socialt och e-handel lagrar inte någon av de kunddata som du överför eller från [!DNL Adobe] segment som används för att skapa eller redigera en [!DNL Google Ads] eller [!DNL Microsoft® Advertising] målgrupp.

1. Generera en fil med kunddata i det format som krävs.

   För- och efternamn, e-postadresser och telefonnummer måste hashas med SHA-256-algoritmen. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> För [!DNL Google Ads] målgrupper, se [!DNL Google Ads] dokumentation om[Formateringsriktlinjer för överföring av streckade data](https://support.google.com/google-ads/answer/7476159)&quot; för en lista över tillåtna fält och krav för kontaktinformation. För [!DNL Microsoft® Advertising] målgrupper, se [!DNL Microsoft® Advertising] dokumentation om [förbereda kundmatchningslistor](https://help.ads.microsoft.com/#apex/ads/en/56921. Du kan ladda ned en [!DNL Microsoft® Excel] mall för kontaktinformation.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Välj annonsnätverket och kontonamnet och klicka sedan på **[!UICONTROL Continue]**.

1. Ange målgruppsinformation:

   1. I [!UICONTROL Data Source] meny, välja **[!UICONTROL Customer List]**.

   1. Ange **[!UICONTROL Audience Name]**.

   1. Överför filen:

      1. Välj [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, eller *[!UICONTROL Mobile Device IDs]*.

         Alternativet Användar-ID är bara tillgängligt för [!DNL Google Ads] annonsörer i USA [användar-ID-segment](https://support.google.com/google-ads/answer/9199250)

      1. (Endast för mobila enhets-ID-listor) Välj **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* eller *[!UICONTROL iOS]*) och anger **[!UICONTROL App ID]**.

         Program-ID är en unik identifierare som mobiloperativsystemet använder för att tillåta att ditt program ansluter till Google Play eller Apple App Store:

         * ([!DNL Android™] appar) [!DNL Android™] paketnamn i [!DNL Google Play], identifieras med &quot;`id=<package_name>`.&quot;

           I https://play.google.com/store/apps/details?id=com.example.game heter paketet till exempel com.example.game.

         * ([!DNL iOS] program) Program-ID:t i [!DNL iTunes App Store], identifieras med &quot;`<idNNNNNNNNN>`&quot; i slutet av URL:en. Det finns också i [!DNL iOS Developer Console].

           I https://itunes.apple.com/us/app/id284882215 är till exempel ID id284882215.

         Utvecklingsteamet har tillgång till [!UICONTROL App ID] för den relevanta plattformen.

      1. I [!UICONTROL Select File] fält, klicka **[!UICONTROL Choose File]** och välj filen i nätverket eller enheten.

      1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och annonsera sekretesspolicyer för nätverk.

      1. (Advertisers skapa [!DNL Google Ads] målgrupper som gör affärer i EES (European Economic Area) eller UK (UK); valfritt) Om du har inhämtat samtycke från användare i EES och Storbritannien att överföra sina data för annonsändamål, markerar du kryssrutan bredvid **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignorerar alla data för användare i EES och UK med ospecificerad medgivandestatus. Detta kan leda till diskrepans och prestandaproblem.

      1. Klicka på **[!UICONTROL Upload File]**.

   1. Ange antalet **[!UICONTROL Membership Days]**, vilket är antalet dagar som en användares cookie stannar kvar hos publiken.

   Använd den tid under vilken du förväntar dig att annonsen ska vara relevant för användaren. Kundlistor förfaller inte om du inte anger ett värde.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>* Annonsnätverket kan ta upp till 24 timmar att bearbeta filen.
>* Se [[!DNL Google Ads] dokumentation om hur kundmatchning fungerar och begränsningar](https://support.google.com/displayvideo/answer/9539301).

## Redigera en kundmatchande målgrupp med hjälp av en kunddatalista

Du kan uppdatera alla [!DNL Google Ads] eller [!DNL Microsoft® Advertising] målgrupp med kundmatchning förutom [!DNL Google Ads] målgrupper skapade från en [!DNL Adobe] målgrupp. Du kan överföra data som ska läggas till, tas bort eller ersätta alla befintliga data för målgruppen.

Data måste vara av samma typ som den ursprungliga kundlistan (e-postadresser, e-postadresser, telefonnummer, användar-ID:n eller mobilenhets-ID:n för en viss app i ett visst mobiloperativsystem).

1. Generera en fil med kunddata i det format som krävs för den befintliga datatypen.

För- och efternamn, e-postadresser och telefonnummer måste hashas med SHA-256-algoritmen. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> För [!DNL Google Ads] målgrupper, se [!DNL Google Ads] dokumentation om[Formateringsriktlinjer för överföring av streckade data](https://support.google.com/google-ads/answer/7476159)&quot; för en lista över tillåtna fält och krav för kontaktinformation. För [!DNL Microsoft® Advertising] målgrupper, se [!DNL Microsoft® Advertising] dokumentation om [förbereda kundmatchningslistor](https://help.ads.microsoft.com/#apex/ads/en/56921. Du kan ladda ned en [!DNL Microsoft® Excel] mall för kontaktinformation.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Markera kryssrutan bredvid målgruppen som ska redigeras.

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png).

1. Välj åtgärd: *[!UICONTROL Add]* (för att lägga till överförda data till befintliga data, såvida det inte redan finns) *[!UICONTROL Delete]* (för att ta bort överförda data från befintliga data, om sådana redan finns) eller *[!UICONTROL Replace]* (för att ta bort alla befintliga data och ersätta dem med överförda data).

1. Överför filen:

   1. I [!UICONTROL Select File] fält, klicka **[!UICONTROL Choose File]** och välj filen i nätverket eller enheten.

   1. Markera kryssrutan för att ange att du godkänner villkoren i [!DNL Adobe] och annonsera sekretesspolicyer för nätverk.

   1. Klicka på **[!UICONTROL Upload File]**.

1. Klicka på **[!UICONTROL Post]**.

>[!NOTE]
>
>Annonsnätverket kan ta en stund att bearbeta uppdateringar till en viss målgrupp.

>[!MORELIKETHIS]
>
>* [Om målgrupper](audience-about.md)
>* [Skapa [!DNL Google Ads] kundmatcha målgrupper från [!DNL Adobe] målgrupper](google-audience-from-adobe-audience.md)
>* [Skapa en [!DNL Google Ads] kundmatchande målgrupp från en e-postlista från Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Hantera målgrupper för dynamisk återmarknadsföring](audience-dynamic-remarketing-manage.md)
