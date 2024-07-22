---
title: Validera landningssidor i kalkylbladsfiler
description: Lär dig hur du validerar mål-URL:er i en enda kontolktsfil.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validera landningssidor i kalkylbladsfiler

*Konton med endast mål-URL:er*

Du kan validera landningssidorna i alla mål-URL:er i en enda kontofil. Du kan ange alla fraser och URL:er som indikerar en ogiltig sida och eventuellt rapportera omdirigeringar av landningssidan som fel. Search, Social och Commerce söker efter de angivna villkoren och efter saknade landningssidor (vilket resulterar i HTTP 404- eller &quot;Hittades inte&quot;-fel).

När fel hittas skapar Search, Social och Commerce en felfil för kalkylblad som innehåller alla rader i det ursprungliga kalkylbladet och felmeddelanden för alla rader med ogiltig landningssida. Felen noteras i kolumnen [!UICONTROL EF Errors]. Filnamnskonventionen är `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Du kan hämta filen senare, korrigera felen och överföra den korrigerade filen och sedan skicka den korrigerade filen till annonsnätverkskontot.

>[!NOTE]
>
>* Den här funktionen validerar inte värden i kolumnen Bas-URL/Slutlig URL.
>* Du kan publicera kalkylbladsfiler medan de valideras, eller även om fel hittas.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]** på huvudmenyn.

1. Markera kryssrutan bredvid varje fil som ska valideras.

1. Klicka på **[!UICONTROL Validate URLs]** i verktygsfältet ovanför datatabellen.

1. Ange information i fälten i dialogrutan och klicka sedan på **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Text i brödtexten på en landningssida som anger att sidan är ogiltig. Om du vill ange flera värden anger du dem på separata rader.

   **[!UICONTROL Enter invalid landing pages(one per line):]** URL:er för sidor som är ogiltiga som landningssidor. Om du vill ange flera värden anger du dem på separata rader.

   **[!UICONTROL User Agent:]** Så här identifieras agenten för validering av landningssida på den webbserver där landningssidan finns. Standardvärdet är default, vilket innebär att agentens vyer kopplas till en anonym [!DNL Mozilla Firefox]-användare. Om webbservern blockerar begäranden från anonyma [!DNL Mozilla Firefox]-användare anger du namnet på en annan agent. Ange till exempel `Googlebot/2.1;+http://www.google.com/bot.html` för [!DNL Googlebot].

   **[!UICONTROL Report redirects as errors]:** När en landningssida dirigeras om till en annan sida (t.ex. om landningssidan saknas och webbplatsen visar en ersättningssida), visar kolumnen [!UICONTROL ER Errors] i felfilen för landningssidan den URL till vilken landningssidan omdirigeras.

När aktiviteten startas läggs en ny rad till i [!UICONTROL Bulksheets view]. När filen skapas skickas ett e-postmeddelande med en länk till filen. Beroende på mängden data som kompileras kan e-postmeddelandet ta flera minuter eller mer. Du kan hämta filen för att redigera den och sedan överföra den igen för publicering, eller så kan du publicera filen som den är. Om det inte går att generera filen visas en felfil på sidan [!UICONTROL Bulksheet Management] och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>* Stora filer tar längre tid att validera.
>* Bulkbladsfiler för flera kampanjer kan innehålla upp till 500 000 datarader. Om du genererar data för flera kampanjer och de kombinerade data består av över 500 000 rader, delas data upp i kampanjer i två eller flera filer med namnen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` och så vidare.

>[!MORELIKETHIS]
>
>* [Om att hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Ta bort överförda kalkylblad och felfiler](bulksheet-delete.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
>* [Stoppa ett pågående kalkylbladsjobb](bulksheet-stop-job.md)
>* [Överför ett kalkylblad eller en korrigerad felfil](bulksheet-upload.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)
