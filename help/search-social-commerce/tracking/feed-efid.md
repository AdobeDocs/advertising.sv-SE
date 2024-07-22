---
title: Konverteringsspårning med en EF ID-feed
description: Lär dig hur du använder en EF ID-feed för konverteringsspårningsdata.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Konverteringsspårning med en EF ID-feed

I den här metoden samlar Advertising Cloud in ett `ef_id`-värde varje gång en användare klickar och annonserar och kommer till landningssidan, och annonsören lagrar `ef_id`-värdet med konverteringsdata och skickar det i en datafeed.

## Implementeringsöversikt

*Endast kontohanterare, [!DNL Adobe] kontohanterare och administratörsanvändarroller*

1. Använd konto- eller kampanjspårningsalternativen [!UICONTROL EF Redirect], omdirigeringstypen [!UICONTROL Token] och [!UICONTROL Auto Upload] om du automatiskt vill generera en mål-URL eller en slutlig URL med en Adobe Advertising-token (ef_id) för varje nyckelord (för nyckelordsspårning) eller annons (för annonsspårning) i kontot eller kampanjen.

   >[!NOTE]
   >* Den här metoden kräver inte att annonsören använder taggar för konvertering till Adobe Advertising.
   >* Om du byter omdirigeringstyp för ett befintligt konto eller en befintlig kampanj från [!UICONTROL Standard] till [!UICONTROL Token], eller vice versa, måste du återskapa alla tillämpliga spårnings-URL:er.

   ef_id fylls i och läggs till i landningssidans URL när slutanvändaren klickar på annonsen och omdirigeras till en Adobe Advertising-server. ef_id skickas sedan till annonsören i mål-URL:en eller den slutliga URL:en för annonsen eller nyckelordet. Följande är ett exempel på en mål-URL som skickas till annonsören under omdirigeringen:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. Annonsören extraherar ef_id från omdirigeringen och lagrar det med relevanta konverteringsdata som ska inkluderas i feed-filen. Ändra inte ef_id eller skiftläge.

1. (Valfritt men rekommenderas) Annonsören kan skapa ett unikt transaktions-ID för varje transaktion som ska ingå i matningsfilen.

1. Annonsören överför en fil med [obligatoriska konverteringsdata](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) till den angivna serverplatsen.

1. Technical Services tolkar konverteringsdata i de överförda filerna och överför sedan data till Adobe Advertising. Adobe Advertising spårar sedan data mot enskilda nyckelord, annonser och placeringar och skapar intäktsprognoser för varje.

1. Tekniska tjänster validerar bearbetade data mot feed-data och söker efter [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Datakrav för dataflöden som använder EF-ID:n](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
