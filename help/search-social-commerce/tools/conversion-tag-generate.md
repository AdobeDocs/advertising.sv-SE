---
title: Generera en Adobe Advertising-tagg för konverteringsspårning
description: Lär dig hur du skapar en konverteringstagg för Adobe Advertising för att spåra konverteringshändelser.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Generera en Adobe Advertising-tagg för konverteringsspårning

*Annonsörer med endast Adobe Advertising-konverteringsspårning*

Skapa en separat konverteringstagg för varje uppsättning mätvärden som du vill spåra och förse annonsören eller reklambyrån med en lista över webbsidor där varje konverteringstagg ska infogas.

>[!NOTE]
>
>Den här funktionen lägger inte till bildtaggar eller [!DNL JavaScript]-taggar på annonsörens webbsidor. Taggarna måste läggas till enligt annonsörens normala procedur för uppdatering av webbsidor.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]** på huvudmenyn.

1. Ange [konverteringstagginställningarna](#conversion-tag-settings).

1. Generera taggen:

   * Om webbplatsen använder HTTP klickar du på **[!UICONTROL Generate Conversion Tag]**.

   * Om webbplatsen körs på en säker server (HTTPS) klickar du på **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopiera taggen från dialogrutan och klistra in den på lämpliga webbsidor efter behov.

>[!NOTE]
>
>Varje mätvärde i den nya konverteringstaggen listas automatiskt i [!UICONTROL Admin] > [!UICONTROL Conversions], även om det inte implementeras eller webbsidorna som den är på inte har fått några klick. Det här beteendet skiljer sig från beteendet för mätvärden i taggar som skapats manuellt eller någon annanstans, som inte listas i [!UICONTROL Admin] > [!UICONTROL Conversions] förrän någon av de webbsidor som den är aktiverad har fått ett klick. I samtliga fall undantas dock varje mätvärde från början från portföljmål, rapporter och vyer tills du uttryckligen gör dem tillgängliga. Innan du lägger till mätvärden i portföljmål bör du dock överväga att först göra mätvärdena tillgängliga och lägga till dem i rapporter för att kontrollera när de får klickningar.

## Inställningar för Adobe Advertising-konverteringstaggar {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Den typ av tagg som ska skapas:

* *[!UICONTROL Image]:* Om du vill skapa en bildtagg som visar en genomskinlig bild på 1 pixel x 1 pixel (pixel), som är osynlig för slutanvändarna, på webbsidan. Det bästa sättet är att bara använda bildtaggar när webbplatsen har en policy för att använda JavaScript-taggar.

* *[!UICONTROL JavaScript]:* Så här skapar du en JavaScript-tagg.

Mer information om skillnaderna mellan taggtyperna finns i [Vanliga frågor om Adobe Advertising-konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

**[!UICONTROL Tag Properties]:** En eller flera konverteringsmått som ska spåras när en slutanvändare visar en sida som innehåller konverteringstaggen. Om du vill lägga till ett mått i listan anger du måttnamnet i fältet [!UICONTROL Add new property] och klickar på **[!UICONTROL Add]**.

När flera mätvärden spåras förenas de med ett et-tecken (`&`) i taggen, till exempel `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Mätvärden som läggs till i den här listan sparas inte någonstans eller är integrerade med klientens [!UICONTROL Conversions]-lista på fliken [!UICONTROL Admin]. Mått läggs dock till i klientens [!UICONTROL Conversions]-lista automatiskt när Adobe Advertising samlar in data för ett mått, vilket inträffar när konverteringstaggen implementeras på en sida och en slutanvändare slutför en transaktion som öppnar sidan.

**[!UICONTROL Include unique transaction IDs]:** (Valfritt) Innehåller en transaktions-ID-egenskap (`ev_transid=<transid>`) i taggen. Alternativet är markerat som standard.

När du väljer det här alternativet måste annonsören generera ett unikt värde för `<transid>` (till exempel ett faktiskt order-ID) när transaktionen är slutförd och skicka tillbaka den till Adobe Advertising, till exempel `ev_transid=0123`. Adobe Advertising använder transaktions-ID:t för att eliminera dubbletttransaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t får inte innehålla et-tecken (`&`) som är reserverade som parameteravgränsare. Transaktions-ID:t ingår i [den [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) som du kan använda för att validera data i Search, Social och Commerce med annonsörens data.

Om data inte innehåller ett unikt ID per transaktion genererar Adobe Advertising fortfarande ett baserat på transaktionstid.

>[!NOTE]
>
>Om du skickar [transaktions-ID-flöden](/help/search-social-commerce/tracking/feed-transaction-id.md) med konverteringsdata för offlinekonverteringar måste du skicka transaktions-ID (`ev_transid`) för onlinedelen av transaktionen i feed-data för offlinedelar av transaktionen.

**[!UICONTROL Page is inside FB app]:** Föråldrad

**[!UICONTROL Segment users]:** Föråldrad

**[!UICONTROL JS Version]:** ([!DNL JavaScript] endast taggar) Vilken version av [!DNL JavaScript]-taggen som ska skapas: *[!UICONTROL v2]* (standard) eller *[!UICONTROL v3]*.

Se &quot;[Vanliga frågor om Adobe Advertising-konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; för mer information om skillnaderna.

>[!MORELIKETHIS]
>
>* [Om Adobe Advertising-konverteringstaggar](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Om verktygen för att skapa och avkoda spårningstaggar](tracking-tools-about.md)
>* [Frågor och svar om spårningstaggar för konvertering och sidvisning](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för JavaScript-konverteringstaggar, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format för JavaScript-konverteringstaggar, version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Konverteringsmappningstaggen för Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Om att hantera en annonsörs konverteringsmått](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
