---
title: Översikt över Adobe Advertising Creative
description: Läs om det grundläggande arbetsflödet för implementering av  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Översikt över Adobe Advertising Creative

*Stängd beta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative]-åtgärdsteamet samarbetar med varje annonsörer för att konfigurera sina kreativa och kreativa upplevelser, antingen implementera annonsupplevelserna som annonser i din DSP eller förse ditt team med tredjepartstaggar för att implementera sig själva och validera initiala kostnader, klick och konverteringsdata.

På löpande basis måste Adobe Account Team, reklambyrån eller annonsören (beroende på villkoren i service level agreement) övervaka varje upplevelse och redigera den om det behövs för att uppfylla annonsörens mål.

## Inledande inställningsuppgifter för [!DNL Creative]-upplevelser

Implementeringsteamet och/eller er byrå kommer att arbeta tillsammans med er för att göra följande:

1. Definiera era personaliseringsmål (t.ex. om ni ska personalisera annonser för prospektering eller återmarknadsföring), alla första-, andra- och tredjepartsdata som är tillgängliga, inklusive kreativa resurser och målgruppssegment, och er strategi för att uppnå era mål.<!-- and CRM data? used how/where? -->

1. (Nya annonserkonton) Konfigurera administratörskonton:

   1. Konfigurera annonsörens konto för [!DNL Creative] och skapa även ett konto i Advertising Search, Social och Commerce.

      Kontokonfigurationen [!DNL Creative] finns i Advertising DSP, även om annonsören inte använder resten av DSP.

      Även om annonsören inte är en [!DNL Search, Social, & Commerce]-kund används [!DNL Search, Social, & Commerce]-kontot för att skapa spårningstaggar för konvertering och ställa in konverteringskolumner i [!DNL Creative].

   1. (Om det behövs) Skapa användarkonton för annonsören för att visa och hantera sina kreativa och annonsupplevelser och för att generera rapporter.

1. (Valfritt) Om du vill skapa egna målgruppssegment som ska inkluderas som mål för dina kreatörer skapar du taggarna på något av följande sätt:

   * [Skapa omdirigerade pixlar](/help/creative/pixels/retargeting-pixel-manage.md) för att omdirigera annonser till besökare med specifika attribut till specifika landningssidor eller konverteringssidor, och generera sedan taggar som ska infogas på de relevanta webbsidorna.

   * (Annonsörer med DSP) I DSP [skapar du anpassade målgruppssegment](/help/dsp/audiences/custom-segment-create.md) för att spåra alla besökare till specifika landningssidor eller konverteringssidor och sedan generera taggar som ska infogas på de relevanta webbsidorna.

   Båda taggtyperna är bildtaggar, som visar en genomskinlig bild på 1 pixel x 1 pixel (pixel), som är osynlig för slutanvändarna, på den webbsida där de läggs till. Senare kan du konfigurera kreatörer i en annonsupplevelse att rikta sig till specifika återannonseringspixlar eller segment, så att de relevanta annonselementen endast visas för användare som tidigare besökt webbplatssidor som är kopplade till pixeln eller segmentet.

   Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

   **Obs!** Du kan också använda dina egna målgrupper från Adobe Audience Manager och Adobe Analytics som kreativa mål. När en besökare kvalificerar sig för en målgrupp som delas från [!DNL Analytics], kan informationen agera på [!DNL Creative] om cirka 24-48 timmar. <!--Are times still true? -->

1. Ställ in kampanjhierarkin inom de DSP:er där ni implementerar era annonsupplevelser. Använd målgruppsanpassning som är kompatibel med målgruppsanpassningen i annonsupplevelserna som ni implementerar i kampanjerna.

   Hierarkisk målinriktning kan variera beroende på DSP. Advertising DSP lägger in målgruppsanpassning på annonsnivå ovanpå (inte i stället för) målinriktning på placeringsnivå. Om en placering till exempel riktar sig till användare i Australien och en annons riktar sig till användare i Japan, kommer annonsen att rikta sig till grenen&quot;Alla andra&quot; för upplevelsen. Se till att du tänker igenom hela kampanjstrukturen.

1. Ställ in annonsupplevelser baserat på era marknadsföringsmål:

   * **Automatiseringsarbetsflöde:** Operationsteamet [!DNL Creative] kan skapa dynamiska annonser för din organisation med annonsmallar och dataflöden.

     Mer information får du om du pratar med ditt Adobe-kontoteam.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Manuellt arbetsflöde:** Konfigurera annonsupplevelser manuellt:

      1. [Konfigurera standardkreatörer som ska användas i dina upplevelser](/help/creative/creative-libraries/creative-add-standard.md):

         * Överför dem till kreatörer som [!DNL Creative] ska vara värd för. Detta kan inkludera bildresurser i ett Adobe Experience Manager-konto.

         * För kreatörer som har en tredjeparts annonsserver som stöds pekar du på de kreativa filerna.

      1. (Valfritt) [Gruppera kreatörer i paket](/help/creative/creative-libraries/bundle-manage.md) som du kan koppla till riktade upplevelser i ett enda steg.

      1. Konfigurera [annonsupplevelser](/help/creative/experiences/experience-about.md):

         * För [riktade annonsupplevelser](/help/creative/experiences/experience-create-targeting.md), sekvensskapare och valfria annonseringsmål.

           Annonsmålen kan omfatta återannonseringspixlar som du skapar i [!DNL Creative], målgruppssegment i Adobe Experience Cloud (inklusive i DSP, Audience Manager eller [!DNL Analytics]), geografiska mål eller specifika datainlösare på webbsidan (till exempel SKU=01234567890123 eller Cart=empty).

         * Skapa allmänna upplevelseinställningar för [icke-målinriktade annonsupplevelser](/help/creative/experiences/experience-create-no-targeting.md).

           Annonsmålen kan omfatta återannonseringspixlar som du skapar i [!DNL Creative], målgruppssegment i Adobe Experience Cloud (inklusive i DSP, Audience Manager eller [!DNL Analytics]), geografiska mål eller specifika datainlösare på webbsidan (till exempel SKU=01234567890123 eller Cart=empty).













1. Ställ in konverteringsspårning för era annonsupplevelser:


Ställ in konverteringsspårning. Beroende på implementeringen kan det innebära att du lägger till
konverteringsspårningstaggar till annonsörens webbsidor och/eller konfigurera en daglig
skicka in data för konvertering som annonsören har samlat in separat.


Du kan generera spårningstaggar för Adobe Advertising-konvertering i Advertising Search, Social och Commerce eller i Adobe Dynamic Tag Manager (kallades tidigare Dynamic Tag Manager).
Obs! Du måste använda JavaScript konverteringstaggar, inte bildtaggar.


Annonsörens IT-avdelning eller annan grupp kan behöva göra en tidplan eller informeras
om taggdistributionen.


(Valfritt) Gör varje konvertering (egenskapen transaction) i Sök, Socialt och Commerce
som finns som en enskild kolumnuppsättning i datavyer och rapporter.


En konvertering (transaktionsegenskap) visas i Sök, Socialt och Commerce efter
minst en konverteringshändelse har spårats.


Om du inte gör specifika mätvärden tillgängliga konsolideras alla konverteringar
i en kolumnuppsättning &quot;Conversions&quot;.


Validera de data som spåras.


(Valfritt) Konfigurera leverans av schemalagda rapporter till angivna e-postadresser.


Instruktioner finns i hjälpkapitlet om &quot;Rapporter&quot;.


Lägg upp annonskampanjer på Advertising DSP eller någon annan DSP och leverera JavaScript
eller iframe-taggar för annonsupplevelsen till annonsören, som kan implementera dem som
annonser från tredje part i DSP.


Övervaka resultatet av era färdiga annonsupplevelser, antingen genom att visa fördefinierade
prestandainformation för enskilda upplevelser eller för att skapa anpassade resultatrapporter.


(Vid behov) Uppdatera annonsupplevelserna baserat på prestanda och uppdaterade meddelanden.






>[!MORELIKETHIS]
>
>* [Om Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Hur användargränssnittet är organiserat](/help/creative/introduction/ui.md)
