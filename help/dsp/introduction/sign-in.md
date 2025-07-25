---
title: Logga in på DSP
description: Lär dig hur du loggar in på DSP.
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
source-git-commit: 62430015c5252cdd1418000d05e49a1c7869e09e
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Logga in på Adobe Advertising DSP

Adobe Advertising DSP går över till Adobe Identity Management Service (IMS) för inloggningsautentisering. IMS ger åtkomst till enkel inloggning (SSO) med federerade ID:n för alla [!DNL Adobe]-produkter som stöder IMS, inklusive Real-Time Customer Data Platform, Customer Journey Analytics, Target och Analytics. Med ändringen:

* Du kan använda en [!DNL Adobe ID] för att logga in på [!DNL Adobe]-produkter från antingen inloggningssidan för Experience Cloud eller den äldre inloggningssidan för DSP. [!DNL Adobe ID] tillhandahåller hantering av användarprofiler. I en framtida version kan du ändra DSP-kontot, IMS-organisationskontot och [!DNL Adobe]-produkten på den översta menyn.

* Enterprise-autentisering stöds.

* Du kan vara inloggad i 24 timmar i stället för att logga in varje timme.

Dina nuvarande DSP-inloggningsuppgifter förblir aktiva under en kort tid så att du kan förbereda dig för ändringen.

## Använd en äldre DSP-inloggning för autentisering

* Gå till [advertising.adobe.com](https://advertising.adobe.com) och logga in med dina tidigare DSP-inloggningsuppgifter.

## Använd en [!DNL Adobe ID] för autentisering

1. Öppna någon av följande inloggningsskärmar:

   * Gå till [advertising.adobe.com](https://advertising.adobe.com). Klicka på [!UICONTROL Sign in with the Adobe Experience Cloud account] under **[!UICONTROL Continue]**.

   * Gå till [experience.adobe.com](https://experience.adobe.com).

1. Ange dina autentiseringsuppgifter:

   * Om du redan använder ett [!DNL Adobe]-konto loggar du in med dina befintliga autentiseringsuppgifter.

   * Om du inte har något [!DNL Adobe]-konto söker du efter ett e-postmeddelande som bjuder in dig att skapa ett [!DNL Adobe]-konto. Du får en inbjudan för varje DSP-konto. Följ länken i e-postmeddelandet för att konfigurera dina autentiseringsuppgifter. Om du har flera DSP-konton följer du instruktionerna för att länka dem.

1. Välj organisation:

   * Välj antingen **[!UICONTROL Personal Account] eller &#x200B;** [!UICONTROL Company or School Account]** om du uppmanas att göra det.

   * Om du har tillgång till flera IMS-organisationer väljer du rätt.

Mer information om Experience Cloud-gränssnittet, inklusive hur du hanterar din användarprofil, finns i &quot;[Experience Cloud-gränssnitt och -administration](https://experienceleague.adobe.com/sv/docs/core-services/interface/experience-cloud)&quot;.

### Felsökning

Allmänna inloggningsproblem finns även i [Lös inloggningsproblem för Adobe-konton](https://helpx.adobe.com/se/manage-account/kb/account-password-sign-help.linkfree.html).

#### Finns det några krav för att aktivera en ny IMS-inloggning för [!DNL Adobe]?

Om du vill lägga till ett nytt inloggningskonto delar du e-postadressen med ditt Adobe-kontoteam. Teamet lägger till din adress i användarlistan för den IMS-organisation som DSP har etablerats för.

Under tiden kan användaren fortsätta att använda sina tidigare DSP-inloggningsuppgifter.

#### När jag har loggat in med ett Adobe IMS-konto omdirigeras jag tillbaka till inloggningssidan adobe.advertising.com.

Kontrollera med IMS-organisationens administratör att e-postmeddelandet som du använder har lagts till i IMS-organisationen. Om administratören bekräftar att du har lagts till i IMS-organisationen ber du ditt Adobe-kontoteam att etablera ditt konto för att använda DSP.

Under tiden kan du fortsätta att använda dina tidigare DSP-inloggningsuppgifter.

#### Jag loggade in med en felaktig e-postadress som loggade in mig på [!DNL Adobe] men som inte ger DSP åtkomst.

1. Gå till [experience.adobe.com](https://experience.adobe.com) och logga ut.

1. Gå till [advertising.adobe.com](https://advertising.adobe.com) och logga in med rätt e-post-ID.

#### Mitt [!DNL Adobe] IMS-konto och DSP-konto är registrerade med olika e-postmeddelanden. Hur loggar jag in med mitt [!DNL Adobe] IMS-konto?

Be ditt Adobe-kontoteam att etablera ditt befintliga [!DNL Adobe] IMS-konto för att använda DSP.
