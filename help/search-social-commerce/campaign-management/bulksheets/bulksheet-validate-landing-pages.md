---
title: Validera landningssidor i kalkylbladsfiler
description: Lär dig hur du validerar mål-URL:er i en enda kontonyckelarksfil.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Validera landningssidor i kalkylbladsfiler

*Konton med endast mål-URL:er*

Du kan validera landningssidorna i alla mål-URL:er i en enda kontofil. Du kan ange alla fraser och URL:er som indikerar en ogiltig sida och eventuellt rapportera omdirigeringar av landningssidan som fel. Sök, social- och handelskontroller för de angivna villkoren och för saknade landningssidor (vilket resulterar i HTTP 404- eller &quot;Hittades inte&quot;-fel).

När fel hittas skapas en felfil för kalkylbladet som innehåller alla rader i det ursprungliga kalkylbladet och felmeddelanden för alla rader med ogiltig landningssida. Felen beskrivs i [!UICONTROL EF Errors] kolumn. Filnamnskonventionen är `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Du kan hämta filen senare, korrigera felen och överföra den korrigerade filen och sedan skicka den korrigerade filen till annonsnätverkskontot.

>[!NOTE]
>
>* Den här funktionen validerar inte värden i kolumnen Bas-URL/Slutlig URL.
>* Du kan publicera kalkylbladsfiler medan de valideras, eller även om fel hittas.


1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Markera kryssrutan bredvid varje fil som ska valideras.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Validate URLs]**.

1. Ange information i fälten i dialogrutan och klicka sedan på **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Text i brödtexten på en landningssida som anger att sidan är ogiltig. Om du vill ange flera värden anger du dem på separata rader.

   **[!UICONTROL Enter invalid landing pages(one per line):]** URL:er för sidor som är ogiltiga som landningssidor. Om du vill ange flera värden anger du dem på separata rader.

   **[!UICONTROL User Agent:]** Hur valideringsagenten för landningssidan identifieras för den webbserver där landningssidan finns. Standardvärdet är default, vilket innebär att agentens vyer kopplas till en anonym [!DNL Mozilla Firefox] användare. Om webbservern blockerar begäranden från anonyma [!DNL Mozilla Firefox] anger du namnet på en annan agent. Till exempel [!DNL Googlebot], ange `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** När en landningssida dirigeras om till en annan sida (t.ex. om landningssidan saknas och platsen visar en ersättningssida), [!UICONTROL ER Errors] kolumnen i felfilen för landningssidan anger den URL till vilken landningssidan omdirigeras.

När aktiviteten startas läggs en ny rad till i [!UICONTROL Bulksheets view]. När filen skapas skickas ett e-postmeddelande med en länk till filen. Beroende på mängden data som kompileras kan e-postmeddelandet ta flera minuter eller mer. Du kan hämta filen för att redigera den och sedan överföra den igen för publicering, eller så kan du publicera filen som den är. Om det inte går att generera filen visas dock en felfil på [!UICONTROL Bulksheet Management] och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>* Stora filer tar längre tid att validera.
>* Bulkbladsfiler för flera kampanjer kan innehålla upp till 500 000 datarader. Om ni genererar data för flera kampanjer och de kombinerade data består av över 500 000 rader, delas data upp efter kampanj i två eller flera filer med namnet `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`och så vidare.


>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Ta bort skickade kalkylblad och felfiler](bulksheet-delete.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
>* [Stoppa ett pågående bulkbladsjobb](bulksheet-stop-job.md)
>* [Överför ett kalkylblad eller en korrigerad felfil](bulksheet-upload.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)

