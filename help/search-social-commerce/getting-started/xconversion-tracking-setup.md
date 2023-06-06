---
title: Konfigurera konverteringsspårning för webbsidor
description: Lär dig hur du kan göra det möjligt för Adobe Advertising att spåra konverteringar till följd av annonsvisningar och klick.
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Konfigurera konverteringsspårning för webbsidor

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

Innan du kan generera rapporter om konverteringsdata behöver Adobe Advertising visa, klicka, beräkna och konvertera (transaktion) data för alla nyckelord och annonser. Adobe Advertising använder också dessa data för att skapa de dataprognosmodeller som behövs för att optimera kampanjbudgeten och budskapen om era nyckelord och annonser.

Om du vill att Adobe Advertising ska kunna spåra konverteringar som är ett resultat av annonsvisningar och klick måste du göra följande:

* Inkludera en unik klickspårningskod (och kanske ytterligare kod för att dirigera om slutanvändaren till en spårningsserver) i spårningsmallen eller mål-URL:en för varje nyckelord, annons, placering, sitelink och produktgrupp i varje annonskampanj som hanteras av Search, Social och Commerce. På så sätt kan Adobe Advertising spåra varje annonsintryck (endast för annonser och annonser i sociala medier) och varje klick på en annons.

* Spåra konverteringsdata på något av följande sätt:

   * **Adobe Advertising-tracking convertions:** Annonsören infogar en Adobe-tagg för konvertering på varje konverteringssida.

   * **Adobe Analytics-konverteringar:** Annonsören använder Adobe Analytics tracking för alla konverteringar.

   * **[!DNL Google Analytics]konverteringar:** Annonsören använder [!DNL Google Analytics] för att spåra alla konverteringar.

   * **Konverteringar som spåras i annonser:** Annonsören tillhandahåller en daglig feed-fil med valfri kombination av online- och offlinekonverteringsdata.

Mer information om implementering av spårning finns i hjälpkapitlet om spårning.

>[!MORELIKETHIS]
>
>* [Generera en konverteringstagg för annonsering i Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Generera en klicknings-URL för sökning, sociala medier och handel med verktyget för spårning av URL:er](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [Avkoda en klicknings-URL för sökning, sociala medier och handel](/help/search-social-commerce/tools/click-tracking-url-decode.md)

