---
title: Ladda upp offlinekontodata för rapportering och simuleringar
description: Lär dig hur du överför offlinekontodata manuellt eller till en  [!DNL Amazon] [!DNL S3]-bucket för rapportering och simuleringsstöd. Loggfiler håller reda på överföringsjobbens förlopp.
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 1%

---

# Ladda upp offlinekontodata för rapportering och simuleringar

*Annonsörer som är aktiverade för överföring av kontodata*

Ladda upp kampanjinnehåll och offlinekostnader, klicknings- och konverteringsdata för ett konto utan API-stöd för rapportering och prestandamuleringar.

Du kan spåra överföringsjobbens förlopp med funktionen [!UICONTROL Upload Logs]:

* Visa en lista över alla överförda filer för kontot. Information om varje filöverföringsjobb innehåller filnamn, överföringskanal (*[!UICONTROL Cloud Storage]* eller *[!UICONTROL Drag & Drop]*), synkroniseringsdatum och -status samt orsaker till ofullständiga överföringar.

* Hämta en fil med kontoentiteter och relaterade mått som har överförts för alla jobb. Filerna är i CSV-format (kommaavgränsade värden).

## Överför kontodata manuellt

Du kan fylla i ett konto med kampanjinnehåll och kostnader, klicka och konverteringsdata genom att överföra data manuellt i en fil.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Gör något av följande:

   * (Från vyn [!UICONTROL Accounts]):

      1. Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Upload]** i verktygsfältet för gruppåtgärder.

      1. Dra en fil till rutan eller klicka på **[!UICONTROL Browse Files]** och välj en fil från enheten eller nätverket.

      1. Klicka på **[!UICONTROL Upload Files]**.

   * (Från kontoinställningarna):

      1. Välj konto på något av följande sätt:

         * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

         * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

      1. Klicka på fliken **[!UICONTROL Upload File]**.

      1. Dra en fil till rutan eller klicka på **[!UICONTROL Browse Files]** och välj en fil från enheten eller nätverket.

      1. Klicka på **[!UICONTROL Save]**.

# Överför kontodata till en [!DNL Amazon] [!DNL S3]-bucket {#data-upload-s3}

Du kan fylla i ett konto med kampanjinnehåll och kostnads-, klicknings- och konverteringsdata genom att överföra data till en mapp som tilldelats av Search, Social och Commerce i en [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])-bucket.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Kontakta Adobe Account Team för att aktivera kontodataöverföringar för ert Search-, Social- och Commerce-annonskonto. Teamet kommer att underlätta skapandet av en organisationsspecifik mapp i en [!DNL S3]-bucket, och de kommer att meddela dig när den är klar.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Hämta molnlagringssökvägen [!DNL S3], ID för åtkomstnyckel och hemlig åtkomstnyckel för ditt konto. Samma åtkomstnyckel-ID och hemlig åtkomstnyckel används för alla organisationens <!-- naming convention?-->-konton för dataöverföring.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Gör något av följande:

   * (Från vyn [!UICONTROL Accounts]):

      1. Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Upload]** i verktygsfältet för gruppåtgärder.

      1. Klicka på [!UICONTROL Cloud Storage Link] i rutan **[!UICONTROL Go to the Link]**.

      1. Klicka på **[!UICONTROL Show Access Key and Secret]**.

      1. Klicka på [!UICONTROL Storage Link] bredvid fältet **[!UICONTROL Copy]** för att kopiera länken till Urklipp och lagra länken på en säker plats.

      1. På samma sätt kan du kopiera och lagra värdena [!UICONTROL Access Key] och [!UICONTROL Secret Key] på ett säkert sätt.

      1. Klicka på **[!UICONTROL Done]**.

   * (Från kontoinställningarna):

      1. Välj konto på något av följande sätt:

         * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

         * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

      1. Klicka på fliken **[!UICONTROL Upload File]**.

      1. Klicka på [!UICONTROL Cloud Storage Link] i rutan **[!UICONTROL Go to the Link]**.

      1. Klicka på **[!UICONTROL Show Access Key and Secret]**.

      1. Klicka på [!UICONTROL Storage Link] bredvid fältet **[!UICONTROL Copy]** för att kopiera länken till Urklipp och lagra länken på en säker plats.

      1. På samma sätt kan du kopiera och lagra värdena [!UICONTROL Access Key] och [!UICONTROL Secret Key] på ett säkert sätt.

      1. Klicka på **[!UICONTROL Done]**.

      1. Klicka på **[!UICONTROL Save]**.

1. (En gång per organisation) Konfigurera din lokala AWS-miljö:

   1. Hämta och installera [!DNL AWS Command Line Interface] (AWS CLI) från följande plats: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Konfigurera dina AWS-autentiseringsuppgifter:

      1. Skapa en textfil och ge den namnet `~/.aws/credentials` (utan filtillägg).

      1. Öppna filen i valfri textredigerare och ange organisationens nyckel-ID och hemlig åtkomstnyckel enligt följande:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Hämta din kontodatarapport från annonsnätverket och spara den.

1. Kör följande kommando i AWS CLI för att överföra dina kontodata till din [!DNL S3]-molnplats.

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Exempel: `aws s3 cp filename.txt s3://cloud-location/`

## Visa en logg över överförda kontodatafiler

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Upload Logs]**.

1. (Valfritt) Om du vill hämta data för en överförd fil klickar du på ![Hämta](/help/search-social-commerce/assets/download.png "Hämta") i kolumnen [!UICONTROL Download] och hämtar filen enligt webbläsarens normala procedur.

## Nödvändiga data

Uppgifterna måste uppfylla datakraven för annonsnätverket. Datafälten för varje enhet kan variera beroende på annonsnätverk.
