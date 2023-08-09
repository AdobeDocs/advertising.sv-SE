---
title: Generera en Adobe Advertising-tagg för konverteringsspårning
description: Lär dig hur du skapar en konverteringstagg för Adobe Advertising för att spåra konverteringshändelser.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Generera en Adobe Advertising-tagg för konverteringsspårning

*Annonsörer med enbart konverteringsspårning i Adobe Advertising*

Skapa en separat konverteringstagg för varje uppsättning mätvärden som du vill spåra och förse annonsören eller reklambyrån med en lista över webbsidor där varje konverteringstagg ska infogas.

>[!NOTE]
>
>Den här funktionen lägger inte till bildtaggar eller [!DNL JavaScript] taggar till annonsörens webbsidor. Taggarna måste läggas till enligt annonsörens normala procedur för uppdatering av webbsidor.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Ange [konverteringsinställningar](#conversion-tag-settings).

1. Generera taggen:

   * Om webbplatsen använder HTTP klickar du på **[!UICONTROL Generate Conversion Tag]**.

   * Om webbplatsen körs på en säker server (HTTPS) klickar du på **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopiera taggen från dialogrutan och klistra in den på lämpliga webbsidor efter behov.

>[!NOTE]
>
>Varje mätvärde i den nya konverteringstaggen visas automatiskt i [!UICONTROL Admin] > [!UICONTROL Conversions]även om det inte är implementerat eller webbsidorna har det inte fått några klick. Detta beteende skiljer sig från beteendet för mätvärden i taggar som skapats manuellt eller någon annanstans och som inte finns med i listan [!UICONTROL Admin] > [!UICONTROL Conversions] tills någon av webbsidorna har fått ett klick. I samtliga fall undantas dock varje mätvärde från början från portföljmål, rapporter och vyer tills du uttryckligen gör dem tillgängliga. Innan du lägger till mätvärden i portföljmål bör du dock överväga att först göra mätvärdena tillgängliga och lägga till dem i rapporter för att kontrollera när de får klickningar.

## Inställningar för konverteringstaggar i Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Den typ av tagg som ska skapas:

* *[!UICONTROL Image]:* Om du vill skapa en bildtagg för att visa en 1-pixel x 1-pixel genomskinlig bild (pixel), som är osynlig för slutanvändarna, på webbsidan. Det bästa sättet är att bara använda bildtaggar när webbplatsen har en profil som förhindrar att JavaScript-taggar används.

* *[!UICONTROL JavaScript]:* Skapa en JavaScript-tagg.

Mer information om skillnaderna mellan taggtyperna finns i &quot;[Frågor och svar om spårningstaggar för Adobe Advertising och sidvisning](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** En eller flera konverteringsvärden som ska spåras när en slutanvändare visar en sida som innehåller konverteringstaggen. Om du vill lägga till ett mått i listan anger du måttnamnet i rutan[!UICONTROL Add new property]&quot; och klicka **[!UICONTROL Add]**.

När flera mätvärden spåras förenas de med ett et-tecken (`&`) i taggen, till exempel `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Mätvärden som läggs till i den här listan sparas inte någonstans eller är integrerade med klientens [!UICONTROL Conversions] listan på [!UICONTROL Admin] -fliken. Mått läggs dock till i klientens [!UICONTROL Conversions] automatiskt när Adobe Advertising verkligen samlar in data för ett mätvärde, vilket inträffar när konverteringstaggen implementeras på en sida och en slutanvändare slutför en transaktion som öppnar den sidan.

**[!UICONTROL Include unique transaction IDs]:** (Valfritt) Innehåller en transaktions-ID-egenskap (`ev_transid=<transid>`) i -taggen. Alternativet är markerat som standard.

När du väljer det här alternativet måste annonsören generera ett unikt värde för `<transid>` (till exempel ett faktiskt order-ID) när transaktionen är slutförd och skickar tillbaka den till Adobe Advertising, till exempel `ev_transid=0123`. Adobe Advertising använder transaktions-ID för att ta bort dubbletttransaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t får inte innehålla et-tecken (`&`), som är reserverade som parameteravgränsare. Transaktions-ID ingår i [den [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), som du kan använda för att validera data i Sök, Socialt och Commerce med annonsörens data.

Om data inte innehåller ett unikt ID per transaktion genererar Adobe Advertising fortfarande ett baserat på transaktionstid.

>[!NOTE]
>
>Om du skickar [transaktions-ID-flöden](/help/search-social-commerce/tracking/feed-transaction-id.md) med konverteringsdata för offlinekonverteringar måste du skicka transaktions-ID:t (`ev_transid`) för onlinedelen av transaktionen i flödesuppgifterna för offlinedelar av transaktionen.

**[!UICONTROL Page is inside FB app]:** Föråldrad

**[!UICONTROL Segment users]:** Föråldrad

**[!UICONTROL JS Version]:** ([!DNL JavaScript] endast taggar) Vilken version av [!DNL JavaScript] som ska skapas: *[!UICONTROL v2]* (standard) eller *[!UICONTROL v3]*.

Se &quot;[Frågor och svar om spårningstaggar för Adobe Advertising och sidvisning](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; för mer information om skillnaderna.

>[!MORELIKETHIS]
>
>* [Om taggar för Adobe Advertising-konverteringsspårning](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Om verktygen för att skapa och avkoda spårningstaggar](tracking-tools-about.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för JavaScript-konvertering version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Konverteringstaggen för JavaScript-konvertering i Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Om att hantera en annonsörs konverteringsstatistik](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
