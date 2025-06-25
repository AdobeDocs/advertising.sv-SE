---
title: Implementera [!DNL Naver] konton med endast spårning
description: Lär dig hur du ställer in spårningskampanjer för dina [!DNL Naver] konton så att du kan spåra, rapportera om och visualisera prestanda för annonser som du köper direkt från annonsnätverket.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implementera [!DNL Naver]-konton med enbart spårning

Endast *[!DNL Naver]konton*

Du kan skapa spårningskampanjer för dina [!DNL Naver]-konton så att du kan spåra, rapportera om och visualisera prestanda för annonser som du köper direkt från annonsnätverket. Search, Social, &amp; Commerce synkroniserar inte data med annonsnätverket, överför automatiskt spårning eller lägger bud på kontot.

Spåra kampanjer replikerar era befintliga kampanjer, annonsgrupper och nyckelord. När ni har skapat kontostrukturen i Search, Social och Commerce och lagt till spårning till de ursprungliga kampanjerna i annonsnätverket kan ni överföra daglig nätverkstrafikstatistik för era nyckelord eller annonser. Search, Social och Commerce kan sedan attribuera konverteringarna till era annonser och nyckelord.

Ni kan spåra resultatvärden för alla era kampanjer och för alla enskilda kampanjer, annonsgrupper och nyckelord/annonser. Du kan även inkludera information om dem i de mest grundläggande, avancerade och medföljande rapporterna, tillsammans med data för dina andra annonsnätverk. Det finns inte stöd för att exportera mätvärden till Adobe Analytics, men i Search, Social och Commerce kan du synkronisera [mätvärden som du spårar i [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) till Search, Social och Commerce.

>[!NOTE]
>
>Du kan inte lägga till spårningskampanjer i en portfölj för optimering.

1. Skapa spårningskampanjer i Search, Social och Commerce:

   1. Skapa [information om dummy-nätverkskonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Om du har flera konton i ett enda annonsnätverk kan du konsolidera dem till ett konto i vyn [!UICONTROL Accounts].

      [!DNL Naver] har inte API-stöd för att överföra spårningsparametrar till annonsnätverket. Du kan dock generera spårningsparametrar med hjälp av kalkylblad och manuellt lägga till dem i annonsnätverket (per steg 2). Om du vill generera spårningsparametrarna måste du använda spårningsmetoden [!UICONTROL EF Redirect]. Du kan också lägga till eventuella tilläggsparametrar.

      Search, Social och Commerce inkluderar automatiskt parametern `ev_cl={ef_uniqueid}` i alla spårnings-URL:er som genereras i kalkylblad för kontot. Detta unika ID används för att matcha kampanjdata med alla kostnader och klicka på data som du överför.

   1. Ställ in kampanjer för att spåra:

      1. I annonsnätverket skapar du en kalkylbladsfil som innehåller alla entiteter, och de överordnade entiteter som krävs, som du vill att Search, Social och Commerce ska spåra för kontot.

         Ni kan inkludera data om nyckelord, inklusive överordnade kampanjer och annonsgrupper.

      1. Redigera om nödvändigt kalkylbladsfilen så att den följer skalbladsformatet Sök, Socialt och Commerce [som krävs för  [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. I Sök, Socialt och Commerce [överför du kalkylbladsfilen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Obs! Data skickas inte till annonsnätverkskontot via Search, Social och Commerce.

1. Ställ in spårning för kampanjerna:

   1. I Sök, Socialt och Commerce [hämtar du en ny kalkylbladsfil](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) med alternativet [!UICONTROL Generate Tracking URLs].

   Om du använder alternativet [!UICONTROL Generate Tracking URLs] fylls fältet [!UICONTROL Destination URL] för varje nyckelord i med spårningskoden Sök, Socialt och Commerce som har prefixet [!UICONTROL Base URL].

   Följande är ett exempel på mål-URL med spårning:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopiera [!UICONTROL Destination URL]-värdena i den hämtade kalkylbladsfilen till relevanta nyckelordsinställningar i nätverket.

      Du kan eventuellt lägga till URL:er till relevanta enheter genom att överföra filen till nätverket i annonsnätverkets redigerare. I så fall kan du behöva ta bort vissa kolumner, enligt nätverkets datakrav. Annars måste du ange URL:erna manuellt i nätverket.

1. Hämta klicknings- och kostnadsdata varje dag från annonsnätverket för de nyckelord eller annonser på gruppnivå som du spårar, och [överför sedan klicknings- och kostnadsdata](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) till Sök, socialt och Commerce i det [obligatoriska formatet](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Inkludera den fullständiga kontohierarkin och alla mått som du vill inkludera. Search, Social och Commerce matchar överförda data med data i befintliga kampanjer.

1. (Valfritt) Om du använder taggar för Adobe Advertising-tjänsten för konverteringsspårning på dina webbsidor för att spåra konverteringar som inte spåras i annonsnätverket skickar du feedsfiler med daglig aggregerad konverteringsinformation som läggs till i dina spårningskampanjer.

   Kontakta Adobe Account Team om du vill ha mer information.

Alla överförda spårningsdata är tillgängliga från [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] i vyerna [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] och [!UICONTROL Keywords]. Den är även tillgänglig för rapporter i vyn [!UICONTROL Insights & Reports].

>[!MORELIKETHIS]
>
>* [Bilaga - obligatoriska kalkylbladsdata för [!DNL Naver] konton](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Överför trafik- och konverteringsstatistik för [!DNL Naver] konton med endast spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Krav för måttdata för [!DNL Naver] konton med endast spårning](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Klickspårningsformat för [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
