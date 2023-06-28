---
title: Återautentisera en [!DNL Google Analytics] datakälla
description: Lär dig hur du autentiserar en [!DNL Google Analytics] datakälla om du ändrar det associerade lösenordet eller om certifikatet upphör att gälla.
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Återautentisera en [!DNL Google Analytics] datakälla

*Byråadministratörer, kontoansvariga för myndigheter, kontoansvariga för Adobe och administratörer*

Om du ändrar lösenordet för e-postkontot som används för en datakälla, eller om [!DNL OAuth] certifikatet för kontot upphör att gälla, alla öppna anslutningar till e-postkontot stängs och du måste autentisera igen för att kunna återuppta synkroniseringen av data.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Markera kryssrutan bredvid datakällan som du vill återautentisera.

1. Klicka på i verktygsfältet ovanför datatabellen ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [inställningar för datakälla](data-source-settings.md):

   1. I [!UICONTROL Connect to Google Analytics] gör du följande.

      1. (Om det behövs) Ange en ny e-postadress som du vill använda för att komma åt data för den här datakällan. E-postadressen måste registreras hos en [!DNL Google] kontot och har behörigheten&quot;Läs och analysera&quot; för [!DNL Google Analytics] konto. Se [instruktioner för att tilldela användarbehörigheter i [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Se till att bara [!DNL Google Analytics] Egenskaper och vyer är tillgängliga i Sök, Socialt och Commerce. Logga in med en e-postadress som bara har tillgång till dessa egenskaper och vyer.

   1. Markera kryssrutan om du vill auktorisera sökningar, sociala medier och handel för att komma åt kontots statistik.

   1. Klicka på **[!UICONTROL Re-Authenticate]**.

1. Klicka på **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Synkronisering [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] visa som en datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgänglig [!DNL Google Analytics] mått](data-source-ga-metrics.md)
