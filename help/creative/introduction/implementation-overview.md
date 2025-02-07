---
title: Översikt över att implementera Adobe Advertising Creative
description: Läs om det grundläggande arbetsflödet för implementering av  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Översikt över att implementera Adobe Advertising Creative

*Stängd beta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative]-åtgärdsteamet samarbetar med varje annonsörer för att konfigurera sina kreativa och kreativa upplevelser, antingen implementera annonsupplevelserna som annonser i din DSP eller förse ditt team med tredjepartstaggar för att implementera sig själva och validera initiala kostnader, klick och konverteringsdata.

Kontinuerligt måste kontoteamet, reklamteamet eller annonsören (beroende på villkoren i service level agreement) övervaka varje upplevelse och redigera den efter behov för att uppfylla annonsörens mål.

## Inledande inställningsaktiviteter för [!DNL Creative] kampanjer <!-- Experiences? "Campaigns" may be confusing now. -->

Implementeringsteamet och/eller er byrå kommer att arbeta tillsammans med er för att göra följande:

1. Definiera era personaliseringsmål (t.ex. om ni ska personalisera annonser för prospektering eller återmarknadsföring), alla första-, andra- och tredjepartsdata som är tillgängliga, inklusive kreativa resurser, målgruppssegment och CRM-data <!-- used how/where? --> samt er strategi för att uppnå era mål.

1. (Nya annonserkonton) Konfigurera administratörskonton:

   1. Konfigurera annonserarens konto för [!DNL Creative]<!-- and/or DSP? --> och skapa även ett konto i Advertising Search.

      Kontoinställningarna för [!DNL Creative] finns i Advertising DSP, även om annonsören inte är en DSP kund.

      Även om annonsören inte är en [!DNL Search]-kund används [!DNL Search]-kontot för att skapa spårningstaggar för konvertering och ställa in konverteringskolumner i [!DNL Creative].

   1. (Om det behövs) Skapa användarkonton för annonsören för att visa och hantera sina kreativa och annonsupplevelser och för att generera rapporter.

1. (Valfritt) Om du vill skapa egna målgruppssegment som ska inkluderas som mål för dina kreatörer skapar du taggarna på något av följande sätt:

   * [Skapa omdirigerade pixlar](/help/creative/pixels/retargeting-pixel-manage.md) för att omdirigera annonser till besökare med specifika attribut till specifika landningssidor eller konverteringssidor, och generera sedan taggar som ska infogas på de relevanta webbsidorna.

   * (Annonsörer med DSP) I DSP [skapar du anpassade målgruppssegment](/help/dsp/audiences/custom-segment-create.md) för att spåra alla besökare till specifika landningssidor eller konverteringssidor och sedan generera taggar som ska infogas på de relevanta webbsidorna.

   Båda taggtyperna är bildtaggar, som visar en genomskinlig bild på 1 pixel x 1 pixel (pixel), som är osynlig för slutanvändarna, på den webbsida där de läggs till. Senare kan du konfigurera kreatörer i en annonsupplevelse att rikta sig till specifika återannonseringspixlar eller segment, så att de relevanta annonselementen endast visas för användare som tidigare besökt webbplatssidor som är kopplade till pixeln eller segmentet.

   Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

   **Obs!** Du kan också använda dina egna målgrupper från Adobe Audience Manager och Adobe Analytics som kreativa mål. När en besökare kvalificerar sig för en målgrupp som delas från [!DNL Analytics], kan informationen agera på [!DNL Creative] om cirka 24-48 timmar. <!--Still true? And what about AAM and DSP? -->

1. Ställ in annonsupplevelser baserat på era marknadsföringsmål:

   * **Automatiseringsarbetsflöde:** Operationsteamet [!DNL Creative] kan skapa dynamiska annonser för din organisation med annonsmallar och dataflöden.

     Mer information får du om du pratar med ditt Adobe-kontoteam.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Manuellt arbetsflöde:** Konfigurera annonsupplevelser manuellt:

      1. Skapa kreativa verktyg som ni kan använda i era upplevelser:

         * För kreatörer som [!DNL Creative] ska vara värd för överför du dem.<!-- Add x-ref and reword if necessary to cover all cases -->

         * För kreatörer som har en tredjeparts annonsserver som stöds pekar [på de kreativa filerna](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Valfritt) [Gruppera kreatörer i paket](/help/creative/creative-libraries/bundle-manage.md) som du kan koppla till upplevelser i ett enda steg.

      1. Sekvensskapare och valfria annonseringsmål som [annonsupplevelser](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Annonsmålen kan omfatta återannonseringspixlar som du skapar i [!DNL Creative], målgruppssegmenten i Adobe Experience Cloud (inklusive i DSP, Audience Manager eller [!DNL Analytics]), geografiska mål eller specifika datautlösare på webbsidan (till exempel SKU=01234567890123 eller Cart=empty).&lt;!- Jag ser inga målgruppssegment tillgängliga, och jag ser radiemål (som inte fungerar) men inte andra geografiska mål - verifiera alla dessa. —>

1. Ställ in konverteringsspårning för era annonsupplevelser:


Ställ in konverteringsspårning. Beroende på implementeringen kan det innebära att du lägger till
konverteringsspårningstaggar till annonsörens webbsidor och/eller konfigurera en daglig
skicka in data för konvertering som annonsören har samlat in separat.


Du kan generera spårningstaggar för Advertising Cloud-konvertering i Advertising Cloud
Sök i eller i Dynamic Tag Manager för Adobe (tidigare Dynamic Tag Manager).
Obs! Du måste använda JavaScript konverteringstaggar, inte bildtaggar.


Annonsörens IT-avdelning eller annan grupp kan behöva göra en tidplan eller informeras
om taggdistributionen.


(Valfritt) Gör varje konvertering i Advertising Cloud Search (egenskapen transaction)
som finns som en enskild kolumnuppsättning i datavyer och rapporter.


En konvertering (transaktionsegenskap) visas i Advertising Cloud Search efter
minst en konverteringshändelse har spårats.


Om du inte gör specifika mätvärden tillgängliga konsolideras alla konverteringar
i en kolumnuppsättning &quot;Conversions&quot;.


Validera de data som spåras.


(Valfritt) Konfigurera leverans av schemalagda rapporter till angivna e-postadresser.


Instruktioner finns i hjälpkapitlet om &quot;Rapporter&quot;.


Ställ in annonskampanjer på Advertising Cloud DSP eller andra DSP och tillhandahåll JavaScript
eller iframe-taggar för annonsupplevelsen till annonsören, som kan implementera dem som
annonser från tredje part i DSP.


Övervaka resultatet av era färdiga annonsupplevelser, antingen genom att visa fördefinierade
prestandainformation för enskilda upplevelser eller för att skapa anpassade resultatrapporter.


(Vid behov) Uppdatera annonsupplevelserna baserat på prestanda och uppdaterade meddelanden.






>[!MORELIKETHIS]
>
>* [Om Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Hur användargränssnittet är organiserat](/help/creative/introduction/ui.md)
