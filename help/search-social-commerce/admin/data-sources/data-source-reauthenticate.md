---
title: Återautentisera en  [!DNL Google Analytics] datakälla
description: Lär dig hur du autentiserar en  [!DNL Google Analytics] datakälla igen om du ändrar det associerade lösenordet eller om certifikatet upphör att gälla.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Återautentisera en [!DNL Google Analytics]-datakälla

*Endast kontoansvariga, kontoansvariga för Adobe, kontoansvariga och administratörer*

Om du ändrar lösenordet för e-postkontot som används för en datakälla, eller om [!DNL OAuth]-certifikatet för kontot upphör att gälla, stängs alla öppna anslutningar till e-postkontot och du måste autentisera igen för att kunna återuppta synkroniseringen av data.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]** på huvudmenyn.

1. Markera kryssrutan bredvid datakällan som du vill återautentisera.

1. Klicka på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera") i verktygsfältet ovanför datatabellen.

1. Redigera inställningarna för [datakälla](data-source-settings.md):

   1. Gör följande i avsnittet [!UICONTROL Connect to Google Analytics].

      1. (Om det behövs) Ange en ny e-postadress som du vill använda för att komma åt data för den här datakällan. E-postadressen måste vara registrerad för ett [!DNL Google]-konto och ha behörigheten Läs och analysera för [!DNL Google Analytics]-kontot. Se [instruktionerna om hur du tilldelar användarbehörigheter i  [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Om du vill vara säker på att endast specifika [!DNL Google Analytics] egenskaper och vyer är tillgängliga i Sök, Socialt och Commerce loggar du in med en e-postadress som bara har åtkomst till dessa egenskaper och vyer.

   1. Markera kryssrutan om du vill tillåta sökningar, sociala medier och Commerce att få åtkomst till kontots statistik.

   1. Klicka på **[!UICONTROL Re-Authenticate]**.

1. Klicka på **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Synkronisering av  [!DNL Google Analytics] konverteringsmått](data-source-about.md)
>* [Krav för att konfigurera en [!DNL Google Analytics] datakälla](data-source-prerequisites.md)
>* [Konfigurera en [!DNL Google Analytics] vy som datakälla](data-source-configure.md)
>* [Redigera en [!DNL Google Analytics] datakälla](data-source-edit.md)
>* [Pausa synkroniseringen av en datakälla](data-source-pause.md)
>* [[!DNL Google Analytics] inställningar för datakälla](data-source-settings.md)
>* [Bilaga - tillgängliga [!DNL Google Analytics] mått](data-source-ga-metrics.md)
