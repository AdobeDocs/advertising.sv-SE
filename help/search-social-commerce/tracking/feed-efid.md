---
title: Konverteringsspårning med en EF ID-feed
description: Lär dig hur du använder en EF ID-feed för konverteringsspårningsdata.
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Konverteringsspårning med en EF ID-feed

I den här metoden samlar Advertising Cloud in `ef_id` varje gång en användare klickar på och annonserar och kommer till landningssidan lagrar annonsören `ef_id` med konverteringsdata och skickar dem i en datafeed.

## Implementeringsöversikt

*Kontorsansvarig [!DNL Adobe] endast kontohanterare och administratörsanvändarroller*

1. Använd alternativen för konto- eller kampanjspårning &quot;[!UICONTROL EF Redirect],&quot; omdirigeringstypen för &quot;[!UICONTROL Token],&quot; och &quot;[!UICONTROL Auto Upload]&quot; för att automatiskt generera en mål-URL eller en slutlig URL med en Adobe Advertising-token (ef_id) för varje nyckelord (för nyckelordsspårning) eller annons (för annonsnivåspårning) i kontot eller kampanjen.

   >[!NOTE]
   >* Den här metoden kräver inte att annonsören använder konverteringsspårningstaggar för Adobe.
   >* Om du byter omdirigeringstyp för ett befintligt konto eller en befintlig kampanj från [!UICONTROL Standard] till [!UICONTROL Token], eller vice versa, måste du återskapa alla tillämpliga spårnings-URL:er.

   ef_id fylls i och läggs till på landningssidans URL när slutanvändaren klickar på annonsen och omdirigeras till en Adobe-annonsserver. ef_id skickas sedan till annonsören i mål-URL:en eller den slutliga URL:en för annonsen eller nyckelordet. Följande är ett exempel på en mål-URL som skickas till annonsören under omdirigeringen:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. Annonsören extraherar ef_id från omdirigeringen och lagrar det med relevanta konverteringsdata som ska inkluderas i feed-filen. Ändra inte ef_id eller skiftläge.

1. (Valfritt men rekommenderas) Annonsören kan skapa ett unikt transaktions-ID för varje transaktion som ska ingå i matningsfilen.

1. Annonsören överför en fil med [obligatoriska konverteringsdata](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) till den angivna serverplatsen.

1. Technical Services tolkar konverteringsdata i de överförda filerna och överför sedan data till Adobe Advertising. Adobe Advertising spårar sedan data mot enskilda nyckelord, annonser och placeringar och skapar intäktsprognoser för varje.

1. Tekniska tjänster validerar bearbetade data mot feed-data och kontrollerar om det finns några [överblivna transaktioner](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Filkrav för konvertering av feed-filer](feed-file-requirements.md)
>* [Datakrav för dataflöden som använder EF-ID:n](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


