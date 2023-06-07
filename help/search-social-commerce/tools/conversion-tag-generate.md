---
title: Generera en konverteringstagg för annonsering i Adobe
description: Lär dig hur du skapar en konverteringstagg för Adobe-annonsering för att spåra konverteringshändelser.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Generera en konverteringstagg för annonsering i Adobe

*Annonsörer med endast konverteringsspårning för Adobe-annonsering*

Skapa en separat konverteringstagg för varje uppsättning mätvärden som du vill spåra och förse annonsören eller reklambyrån med en lista över webbsidor där varje konverteringstagg ska infogas.

>[!NOTE]
>
>Den här funktionen lägger inte till bildtaggar eller [!DNL JavaScript] taggar till annonsörens webbsidor. Taggarna måste läggas till enligt annonsörens normala procedur för uppdatering av webbsidor.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Ange [konverteringsinställningar](#conversion-tag-settings).

1. Generera taggen:

   * Om webbplatsen använder HTTP klickar du på **[!UICONTROL Generate Conversion Tag]**.

   * Om webbplatsen körs på en säker server (HTTPS) klickar du på **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopiera taggen från dialogrutan och klistra in den på lämpliga webbsidor efter behov.

>[!NOTE]
>
>Varje mätvärde i den nya konverteringstaggen visas automatiskt i [!UICONTROL Admin] > [!UICONTROL Transaction Properties]även om det inte är implementerat eller webbsidorna har det inte fått några klick. Detta beteende skiljer sig från beteendet för mätvärden i taggar som skapats manuellt eller någon annanstans och som inte finns med i listan [!UICONTROL Admin] > [!UICONTROL Transaction Properties] tills någon av webbsidorna har fått ett klick. I samtliga fall undantas dock varje mätvärde från början från portföljmål, rapporter och vyer tills du uttryckligen gör dem tillgängliga. Innan du lägger till mätvärden i portföljmål bör du dock överväga att först göra mätvärdena tillgängliga och lägga till dem i rapporter för att kontrollera när de får klickningar.

## Konverteringsinställningar för konverteringstagg i Adobe {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Den typ av tagg som ska skapas:

* *[!UICONTROL Image]:* Om du vill skapa en bildtagg för att visa en 1-pixel x 1-pixel genomskinlig bild (pixel), som är osynlig för slutanvändarna, på webbsidan. Det bästa sättet är att bara använda bildtaggar när webbplatsen har en profil som förhindrar att JavaScript-taggar används.

* *[!UICONTROL JavaScript]:* Skapa en JavaScript-tagg.

Mer information om skillnaderna mellan taggtyperna finns i &quot;[Vanliga frågor om taggar för annonskonvertering och spårning av sidvy i Adobe](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** En eller flera transaktionsegenskaper (mått) som ska spåras när en användare visar en sida som innehåller konverteringstaggen. Om du vill lägga till ett mått i listan anger du måttnamnet i rutan[!UICONTROL Add new property]&quot; och klicka **[!UICONTROL Add]**.

När flera mätvärden spåras förenas de med ett et-tecken (`&`) i taggen, till exempel `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Mätvärden som läggs till i den här listan sparas inte någonstans eller är integrerade med klientens [!UICONTROL Transaction Properties] listan på [!UICONTROL Admin] -fliken. Mått läggs dock till i klientens [!UICONTROL Transaction Properties] automatiskt när Adobe Advertising faktiskt samlar in data för ett mätvärde, vilket inträffar när konverteringstaggen implementeras på en sida och slutanvändaren slutför en transaktion som öppnar den sidan.

**[!UICONTROL Include unique transaction IDs]:** (Valfritt) Innehåller en transaktions-ID-egenskap (`ev_transid=<transid>`) i -taggen. Alternativet är markerat som standard.

När du väljer det här alternativet måste annonsören generera ett unikt värde för `<transid>` (till exempel ett faktiskt beställnings-ID) när transaktionen är slutförd och skickar tillbaka den till Adobe Advertising, till exempel `ev_transid=0123`. Adobe Advertising använder transaktions-ID:t för att eliminera dubbletttransaktioner med samma transaktions-ID och egenskapsvärde. Transaktions-ID:t får inte innehålla et-tecken (`&`), som är reserverade som parameteravgränsare. Transaktions-ID ingår i [den [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), som du kan använda för att validera data i Sök, Socialt och Commerce med annonsörens data.

Om data inte innehåller ett unikt ID per transaktion genererar Adobe Advertising fortfarande ett baserat på transaktionstid.

>[!NOTE]
>
>Om du skickar [transaktions-ID-flöden](/help/search-social-commerce/tracking/feed-transaction-id.md) med konverteringsdata för offlinekonverteringar måste du skicka transaktions-ID:t (`ev_transid`) för onlinedelen av transaktionen i flödesuppgifterna för offlinedelar av transaktionen.

**[!UICONTROL Page is inside FB app]:** Föråldrad

**[!UICONTROL Segment users]:** Föråldrad

**[!UICONTROL JS Version]:** ([!DNL JavaScript] endast taggar) Vilken version av [!DNL JavaScript] tagg som ska skapas: *[!UICONTROL v2]* (standard) eller *[!UICONTROL v3]*.

Se &quot;[Vanliga frågor om taggar för annonskonvertering och spårning av sidvy i Adobe](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; för mer information om skillnaderna.

>[!MORELIKETHIS]
>
>* [Om konverteringsspårningstaggar för Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Om verktygen för att skapa och avkoda spårningstaggar](tracking-tools-about.md)
>* [Vanliga frågor om konvertering och spårningstaggar för sidvy](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format för spårningstaggar för JavaScript-konvertering, version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format för spårningstaggar för bildkonvertering](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [JavaScript-konverteringskoden Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Hantera en annonsörs transaktionsegenskaper](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
