---
title: Lägg till standardkreatörer i ett kreativt bibliotek
description: Lär dig hur du lägger till standardkreatörer (icke-dynamiska) i ett kreativt bibliotek.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 5bbc8b17b0f88c928b6ab2b8805ecec10bb398fb
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 0%

---

# Lägg till standardkreatörer i ett kreativt bibliotek

Lägg till standardkreatörer i dina [kreativa bibliotek](creative-library-manage.md) som kan användas med [standardannonsupplevelser](/help/creative/experiences/experience-about.md).

>[!NOTE]
>
> Ni kan inkludera enskilda kreatörer direkt i annonsupplevelser som inte har definierade användarmål. Du kan också gruppera dina kreatörer i [paket](bundle-manage.md) som du kan inkludera i riktade annonsupplevelser.

## Lägg till flexibla HTML-annonser i ett kreativt bibliotek {#flexible-creative-add}

Du kan göra något av följande:

* Ladda upp egna flexibla kreatörer i ZIP-filer.

* Använd någon av de fördefinierade flexibla kreativa mallarna som du har överfört till ditt konto som startpunkt för din egen flexibla kreativitet.

### Ladda upp egna flexibla kreatörer {#flexible-creative-upload}

Du kan överföra flera flexibla kreativa enheter. Flexibla kreatörer måste ha ZIP-format och kan vara upp till 2 MB. Information om filkrav finns i [HTML5 Creative-specifikationen](html5-creative-specification.md).

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Klicka på **[!UICONTROL Upload New]**.

1. Ange ZIP-filer på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL Select a file]** för att leta upp filerna på enheten eller i nätverket.

   Se de [flexibla annonsspecifikationerna](#flexible-ad-spec).

1. Lägg till eller ta bort flexibla kreativa filer:

   * Om du vill lägga till en fil klickar du på ![Lägg till](/help/creative/assets/create.png "Lägg till") i det övre vänstra hörnet och letar upp filen på enheten eller i nätverket.

   * Om du vill ta bort en fil avmarkerar du kryssrutan bredvid den.

1. Ange [flexibla annonsinställningar för HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   Som standard markeras alla användare som du just överfört. Alla inställningar som bara har ett värde gäller för alla valda kreatörer. För vissa inställningar kan du ange enskilda värden. Om du vill ange inställningar för specifika kreatörer avmarkerar du kryssrutan bredvid varje ej tillämpligt kreativt alternativ.

1. Klicka på **[!UICONTROL Create]**

### Lägg till flexibla kreatörer med en mall {#flexible-creative-use-template}

Du kan använda någon av de flexibla kreativa mallarna som du har överfört till ditt konto för att skapa annonser i en fördefinierad storlek. När du har valt en mall som ska användas redigerar du klickningstaggar och -attribut.&lt;!— Ersätt den sista meningen med den här om vi lägger till funktionen för mallhämtning igen: Du kan antingen a\) välja en mall som ska användas och sedan redigera klicktaggar och attribut; eller b\) [hämta en mall som en ZIP-fil](#download-flexible-creative-template), redigera innehållet offline för att skapa din egen kreativitet och sedan [överföra den redigerade filen som en ny kreativ fil](flexible-creative-upload).>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Klicka på **[!UICONTROL Browse System Flexible Templates]**.

1. (Valfritt) Om du vill förhandsgranska mallen klickar du på **[!UICONTROL ...]** bredvid mallnamnet och sedan på **[!UICONTROL Preview]**.

   Du kan även hämta mallen

1. Klicka på **[!UICONTROL ...]** och sedan **[!UICONTROL Use Selected]** bredvid mallnamnet.

1. Redigera de [flexibla kreativa HTML5-inställningarna](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) för att ange språk och inkludera egna klicktaggar, bilder och andra attribut.

   Den maximala filstorleken för den kreativa delen är 2 MB när den har zippats.<!-- Still true? -->

1. Klicka på **[!UICONTROL Create]**.

<!-- Not options as of 5/22/25:

1. In the left panel, select the creative size to see all available templates for that size.

1. Select the template:

   * In card view, click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Use Selected]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Use Selected]**.
-->

## Lägg till en HTML5-kreatör i ett kreativt bibliotek

Du kan lägga till flera HTML5-kreatörer av samma typ (enkla eller statiska) i taget.

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>Du kan också [lägga till flexibla HTML5-kreatörer](#flexible-creative-add), som är HTML5-kreatörer med alla sina attribut som HTML-standardtaggar som du kan redigera direkt i [!DNL Creative].

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Ange filerna på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL Select a file]** för att leta upp filen på enheten eller i nätverket.

   Se [HTML5-annonsspecifikationen](/help/creative/creative-libraries/html5-creative-specification.md).

1. Ange [annonsinställningarna för HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Som standard markeras alla användare som du just överfört. Alla inställningar som bara har ett värde gäller för alla valda kreatörer. För vissa inställningar kan du ange enskilda värden. Om du vill ange inställningar för specifika kreatörer avmarkerar du kryssrutan bredvid varje ej tillämpligt kreativt alternativ.

1. Klicka på **[!UICONTROL Create]**

## Lägga till en bild som är kreativ i ett kreativt bibliotek

De som skapar bilderna kan vara i GIF-, JPEG-, JPG- eller PNG-format. Den maximala filstorleken är två (2) MB. Se de [kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md).

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Image]**.

1. Ange bilderna:

   * Gör något av följande för lokala bildresurser:

      * Dra och släpp filer på enheten eller nätverket i lådan.

      * Klicka på **[!UICONTROL Select a file]** om du vill söka efter filer på enheten eller i nätverket.

   * Gör följande för godkända bilder i ett [Adobe Experience Manager-bibliotek som är anslutet till ditt DSP-konto](/help/creative/creative-libraries/aem-assets-configure.md):

      1. Klicka på **[!UICONTROL AEM Asset Library]**.

      1. Logga in på ditt Experience Manager-konto.

      1. Leta reda på och markera filerna i [!UICONTROL Assets]- eller [!UICONTROL Collections]-vyerna och klicka sedan på **[!UICONTROL Select]** i det övre högra hörnet.

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

1. Lägg till eller ta bort bilder:

   * Om du vill lägga till en bild klickar du på ![Lägg till](/help/creative/assets/create.png "Lägg till") i det övre vänstra hörnet och letar upp filen på enheten eller i nätverket.

   * Om du vill ta bort en bild avmarkerar du kryssrutan bredvid den.

1. Ange de [kreativa bildinställningarna](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   Som standard markeras alla användare som du just överfört och alla inställningar du anger gäller alla valda användare. Alla inställningar med endast ett värde gäller för alla valda kreatörer. Om du vill ange inställningar för specifika kreatörer avmarkerar du de ej tillämpliga kreativa.

1. Klicka på **[!UICONTROL Create]**

## Lägg till en tredjepartsskapare i ett kreativt bibliotek {#creative-add-third-party}

[!DNL Creative] har stöd för JavaScript-spårningstaggar för kreatörer som finns på de flesta annonsservrar från tredje part.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**.

1. Ange JavaScript-taggen och andra inställningar för den kreativa i de [kreativa inställningarna från tredje part](#creative-settings-third-party).

   Du kan kopiera och klistra in alla [tillgängliga makron](/help/creative/creative-macros.md) i JavaScript-taggen.

1. Klicka på **[!UICONTROL Create]**

## Lägga till en videoredigerare i ett kreativt bibliotek

Se de [videokreativa specifikationerna](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs) och de [kreativa storlekar](/help/creative/creative-libraries/creative-sizes.md) som stöds.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**.

1. Ange videofilerna på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL Select a file]** om du vill söka efter filer på enheten eller i nätverket.

1. Ange de [kreativa inställningarna för video](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video).

   Som standard markeras den kreativitet som du just överförde och alla inställningar som du anger gäller för den valda kreativiteten.<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. Klicka på **[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [Redigera standardkreatörer](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Standardinställningar för kreativitet](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Tillgängliga makron för att spåra URL:er](/help/creative/creative-macros.md)
>* [Kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md)
>* [Förhandsgranska en kreativ](/help/creative/creative-libraries/creative-preview.md)
>* [Bifoga och koppla loss kreatörer från paket](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [Om dina kreativa bibliotek](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Hantera kreativa bibliotek](/help/creative/creative-libraries/creative-library-manage.md)
