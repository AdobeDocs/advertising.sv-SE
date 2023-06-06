---
title: Implementera [!DNL Naver] konton med enbart spårning
description: Lär dig hur du ställer in spårningskampanjer för [!DNL Naver] så att ni kan spåra, rapportera om och visualisera resultatet för de annonser ni köper direkt från annonsnätverket.
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementera [!DNL Naver] konton med enbart spårning

*[!DNL Naver]endast konton*

Du kan skapa spårningskampanjer för [!DNL Naver] så att ni kan spåra, rapportera om och visualisera resultatet för de annonser ni köper direkt från annonsnätverket. Sökning, sociala medier och handel synkroniserar inte data med annonsnätverket, överför spårning automatiskt eller lägger bud på kontot.

Spåra kampanjer replikerar era befintliga kampanjer, annonsgrupper och nyckelord. När ni har skapat kontostrukturen i Sök, Socialt, &amp; Commerce och lagt till spårning till de ursprungliga kampanjerna i annonsnätverket, kan ni överföra daglig nätverkstrafikstatistik för era nyckelord eller annonser. Search, Social, &amp; Commerce kan sedan attribuera konverteringarna till era annonser och nyckelord.

Ni kan spåra resultatvärden för alla era kampanjer och för alla enskilda kampanjer, annonsgrupper och nyckelord/annonser. Du kan även inkludera information om dem i de mest grundläggande, avancerade och medföljande rapporterna, tillsammans med data för dina andra annonsnätverk. Det finns inte stöd för att exportera mätvärden till Adobe Analytics, men det går att synkronisera via Sök, Sociala och Commerce [mätvärden som ni spårar i [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) till sökning, sociala medier och handel.

>[!NOTE]
>
>Du kan inte lägga till spårningskampanjer i en portfölj för optimering.

1. Skapa spårningskampanjer i Sök, Socialt och Commerce:

   1. Skapa [dummy network account details](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Om du har flera konton i ett enda annonsnätverk kan du slå samman dem till ett konto i [!UICONTROL Accounts] vy.

      [!DNL Naver] saknar API-stöd för att överföra spårningsparametrar till annonsnätverket. Du kan dock generera spårningsparametrar med hjälp av kalkylblad och manuellt lägga till dem i annonsnätverket (per steg 2). Om du vill generera spårningsparametrarna måste du använda[!UICONTROL EF Redirect]&quot; spårningsmetod. Du kan också lägga till eventuella tilläggsparametrar.

      Sökning, sociala medier och handel inkluderar automatiskt parametern `ev_cl={ef_uniqueid}` i alla spårnings-URL:er som genereras i kalkylblad för kontot. Detta unika ID används för att matcha kampanjdata med alla kostnader och klicka på data som du överför.

   1. Ställ in kampanjer att spåra:

      1. I annonsnätverket skapar du en kalkylbladsfil som innehåller alla entiteter, och de överordnade entiteter som krävs, som du vill att Sök efter, Socialt och Commerce ska spåra för kontot.

         Ni kan inkludera data om nyckelord, inklusive överordnade kampanjer och annonsgrupper.

      1. Redigera eventuellt kalkylbladsfilen så att den följer Sök, Social och Commerce [kalkylbladsformat krävs för [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. I sökmotorkampanjer, sociala medier och handel [ladda upp kalkylbladsfilen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Obs! Data publiceras inte i annonsnätverkskontot via sökning, sociala medier och handel.

1. Ställ in spårning för kampanjerna:

   1. I sökmotorkampanjer, sociala medier och handel [ladda ned en ny kalkylbladsfil](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) med alternativet att[!UICONTROL Generate Tracking URLs].&quot;
   Använda &quot;[!UICONTROL Generate Tracking URLs]&quot; fyller i [!UICONTROL Destination URL] fält för varje nyckelord med spårningskoden Sök, Social och Commerce, som är prefix till [!UICONTROL Base URL] värde.

   Följande är ett exempel på mål-URL med spårning:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopiera [!UICONTROL Destination URL] värden i den hämtade kalkylbladsfilen till relevanta nyckelordsinställningar i nätverket.

      Du kan eventuellt lägga till URL:er till relevanta enheter genom att överföra filen till nätverket i annonsnätverkets redigerare. I så fall kan du behöva ta bort vissa kolumner, enligt nätverkets datakrav. Annars måste du ange URL:erna manuellt i nätverket.


1. Hämta klicknings- och kostnadsdata varje dag från annonsnätverket för de nyckelord eller annonser på gruppnivå som ni spårar, och sedan [ladda upp klicknings- och kostnadsdata](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) till sökning, sociala medier och handel i [obligatoriskt format](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Inkludera den fullständiga kontohierarkin och alla mått som du vill inkludera. Sök, Socialt och e-handel matchar överförda data med data i befintliga kampanjer.

1. (Valfritt) Om du använder taggar för konverteringsspårning i Adobe på dina webbsidor för att spåra konverteringar som inte spåras i annonsnätverket skickar du feedsfiler med daglig aggregerad konverteringsinformation som läggs till i dina spårningskampanjer.

   Kontakta kontoteamet på Adobe om du vill ha mer information.

Alla överförda spårningsdata är tillgängliga från [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] inom [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups]och [!UICONTROL Keywords] vyer. Det finns även för rapporter i [!UICONTROL Insights & Reports] vy.

>[!MORELIKETHIS]
>
>* [Bilaga - Obligatoriska data för kalkylblad för [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Ladda upp trafik- och konverteringsstatistik för [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Krav för mätdata för [!DNL Naver] konton med enbart spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Klickningsspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

