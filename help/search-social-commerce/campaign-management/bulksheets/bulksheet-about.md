---
title: Hantera kampanjdata med hjälp av kalkylblad
description: Lär dig mer om vilka funktioner som är tillgängliga i annonsnätverk, arbetsflödet för kalkylblad och felhanteringen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Hantera kampanjdata med hjälp av kalkylblad

Ett kalkylblad är en fil som innehåller kampanjdata i ett visst format och kan användas för att snabbt skapa eller ändra kampanjdata och annonsgruppsstrukturdata och textannonser. Du kan generera (ladda ned) kalkylblad med data för ett eller flera konton, för specifika kampanjer och annonsgrupper eller till och med för specifika textannonser, placeringar och produktgrupper. Du kan använda kalkylblad för att hantera stora datauppsättningar eller för att göra små ändringar. Varje annonsnätverk kräver olika informationskolumner.

Du kan generera kalkylblad med så mycket data du vill - eller skapa dem manuellt och överföra dem (se kapitlet&quot;Obligatoriska/inkluderade data i kalkylblad&quot;).

När du har skapat ett kalkylblad kan du identifiera alla brutna landningssidor som behöver korrigeras eller ytterligare data som ska läggas till eller redigeras. Du kan sedan redigera filen och överföra den till Sök, Socialt, &amp; Commerce. Om du vill kan du schemalägga att den ska bokföras i det relevanta annonsnätverket omedelbart eller senare. Du kan också publicera ett tillgängligt kalkylblad antingen direkt eller senare.

Du kan överföra kalkylbladsfiler till ett angivet FTP-konto för hämtning och automatisk bokföring. Katalogen genomsöks varje timme och nya filer läggs in i söknätverket i den ordning som de tas emot.

Alla kalkylblad, valideringsfelfiler för landningssidor och andra felfiler tas automatiskt bort 30 dagar efter att de har skapats, såvida du inte tar bort dem tidigare.

## Ad Network-funktionalitet

* **Ladda ned, ladda upp och posta:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising]och [!DNL Yandex] konton

* **Endast nedladdning och uppladdning:** [!DNL Naver] konton

   Du kan överföra [!DNL Naver] data som ska användas i sökningar, sociala medier och handel, men som inte kan publicera dem i annonsnätverket. Du kan även hämta befintliga (osynkroniserade) data.

* **Hämta endast data:**  [!DNL Pinterest], [!DNL Yahoo Native]och [!DNL Yahoo! Display Network] konton

   Du kan hämta befintliga (osynkroniserade) data.

## Översikt över användning av kalkylblad

Standardstegen för användning av kalkylblad för synkroniserade konton är följande:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Hämta data för ett eller flera konton, kampanjer eller annonsgrupper till en kalkylbladsfil](bulksheet-download.md). Du kan också manuellt fylla i ett annonsspecifikt kalkylblad och överföra filen.

1. [Validera landningssidorna](bulksheet-validate-landing-pages.md) i de grundläggande (slutliga) URL:erna eller mål-URL:erna i filen.

1. När du behöver lägga till data eller göra korrigeringar:

   1. [Exportera filen](bulksheet-export.md) till datorn och redigera den i [!DNL Microsoft® Excel].

   1. [Överför den redigerade filen manuellt](bulksheet-upload.md) till sökning, sociala medier och handel, eller [överföra filen till ett angivet FTP-konto](bulksheet-ftp-account.md) för automatisk bokföring.

1. (För filer som överförts manuellt) [Bokför filen](bulksheet-post.md) till annonsnätverket antingen när du överför det eller senare.

1. (Om det behövs) Hämta eventuella nya felfiler, korrigera raderna och posta om filen.

## Hantera fel vid överföring och bokföring av kampanjdata

Sökning, sociala medier och handel överför och skickar så många rader med data som det kan från ett kampanjgruppsblad, inklusive URL:er för spårning som genereras vid behov.

När fel uppstår under en bladåtgärd genereras en av följande två typer av felfiler:

* **[!UICONTROL EF Errors]:**  När en fil eller enskilda rader i filen inte kan överföras eller bearbetas, visas en felfil som kallas `<uploaded file name>_ef_errors.<extension used for the bulksheet>` skapas. Om problemet gäller enskilda rader inkluderas dessa rader, med en förklaring av varje fel så att de kan korrigeras.

* **[!UICONTROL SE Errors]:**  När en fil har publicerats men annonsnätverket inte accepterar vissa eller alla data, visas en felfil med namnet `<uploaded file name>_se_errors.<extension used for the bulksheet>` skapas. När vissa men inte alla rader accepterades, visar felfilen de rader som inte hade bokförts och en förklaring av varje fel så att de kan korrigeras. Felmeddelandena visas i de tre sista kolumnerna på varje rad.

>[!NOTE]
>
>Om du publicerar [!DNL Google Ads] annonser som bryter mot annonsnätverkets annonspolicyer men som kan vara berättigade till undantag, så postas dessa annonser automatiskt om med begäran om undantag. Om begäran om undantag misslyckas inkluderas information om överträdelsen i felfilen.

Du kan hämta vilken typ av felfil du vill, korrigera direkt i raderna och sedan överföra och publicera filen igen.

Felfiler tas automatiskt bort efter 30 dagar om du inte tar bort dem tidigare.

## Information om varje fil

Alla hämtade datafiler, överförda filer och felfiler är tillgängliga från [!UICONTROL Search] > [!UICONTROL Bulksheets].

Informationen för varje fil innehåller aktivitetsstatus och procent av uppgiften som är slutförd, det datum då den skapades (när det är tillämpligt) det datum då den var eller kommer att bokföras i det angivna annonsnätverket, det schemalagda raderingsdatumet och inloggningsnamnet för användaren som initierade uppgiften.

>[!MORELIKETHIS]
>
>* [Hämta/skapa en kalkylbladsfil](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Överför ett kalkylblad eller en korrigerad felfil](bulksheet-upload.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)

