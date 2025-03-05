---
title: Lägg till standardkreatörer i ett kreativt bibliotek
description: Lär dig hur du lägger till standardkreatörer (icke-dynamiska) i ett kreativt bibliotek.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Lägg till standardkreatörer i ett kreativt bibliotek

*Stängd beta*

Lägg till kreatörer i dina [kreativa bibliotek](creative-library-manage.md) som du kan använda med [annonsupplevelser](/help/creative/experiences/experience-about.md).

>[!NOTE]
>
> Ni kan inkludera enskilda kreatörer direkt i annonsupplevelser som inte har definierade användarmål. Du kan också gruppera dina kreatörer i [paket](bundle-manage.md) som du kan inkludera i riktade annonsupplevelser.

## Lägg till flexibla HTML-annonser i ett kreativt bibliotek {#flexible-creative-add}

<!-- Later:
You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

-->

Du kan överföra flera flexibla kreativa enheter. Flexibla kreatörer måste ha ZIP-format och kan vara upp till 2 MB. Information om filkrav finns i [HTML5 Creative-specifikationen](html5-creative-specification.md).

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. Klicka på underfliken **[!UICONTROL Standard Ads]** på fliken **[!UICONTROL Creatives]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Klicka på **[!UICONTROL Upload New]**.

1. Ange ZIP-filer på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL select a file]** för att leta upp filerna på enheten eller i nätverket.

   Se de [flexibla annonsspecifikationerna](#flexible-ad-spec).

1. Lägg till eller ta bort flexibla kreativa filer:

   * Om du vill lägga till en fil klickar du på ![Lägg till](/help/creative/assets/create.png "Lägg till") i det övre vänstra hörnet och letar upp filen på enheten eller i nätverket.

   * Om du vill ta bort en fil avmarkerar du kryssrutan bredvid den.

1. Ange [flexibla annonsinställningar för HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   Som standard markeras alla användare som du just överfört. Alla inställningar som bara har ett värde gäller för alla valda kreatörer. För vissa inställningar kan du ange enskilda värden. Om du vill ange inställningar för specifika kreatörer avmarkerar du kryssrutan bredvid varje ej tillämpligt kreativt alternativ.

1. Klicka på **[!UICONTROL Create]**

<!-- In a later phase:

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads. Once you select a template to use, you'll edit the click tags and attributes.<!-- Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).>

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click the **[!UICONTROL Standard Ads]** subtab.

1. Click **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.



[The following are old instructions; see how this works in the new UI]


1. In the left panel, select the creative size to see all available templates for that size.

1. Under the template name, click **[!UICONTROL Use This Creative]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.[Will saving the creative zip it??]

1. (Optional) Once you've made your changes, click []()[add image] to preview the new creative. 

1. Click **[!UICONTROL Save]**.

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

1. Klicka på underfliken **[!UICONTROL Standard Ads]** på fliken **[!UICONTROL Creatives]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Ange filerna på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL select a file]** för att leta upp filen på enheten eller i nätverket.

   Se [HTML5-annonsspecifikationen](/help/creative/creative-libraries/html5-creative-specification.md).

1. Ange [annonsinställningarna för HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Som standard markeras alla användare som du just överfört. Alla inställningar som bara har ett värde gäller för alla valda kreatörer. För vissa inställningar kan du ange enskilda värden. Om du vill ange inställningar för specifika kreatörer avmarkerar du kryssrutan bredvid varje ej tillämpligt kreativt alternativ.

1. Klicka på **[!UICONTROL Create]**

## Lägga till en bild som är kreativ i ett kreativt bibliotek

De som skapar bilderna kan vara i GIF-, JPEG-, JPG- eller PNG-format. Den maximala filstorleken är två (2) MB. Se de [kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md).

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. Klicka på underfliken **[!UICONTROL Standard Ads]** på fliken **[!UICONTROL Creatives]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**.

1. Ange filerna på något av följande sätt:

   * Dra och släpp filer på enheten eller nätverket i lådan.

   * Klicka på **[!UICONTROL select a file]** för att leta upp filen på enheten eller i nätverket.

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

1. Klicka på underfliken **[!UICONTROL Standard Ads]** på fliken **[!UICONTROL Creatives]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**.

1. Ange JavaScript-taggen och andra inställningar för den kreativa i de [kreativa inställningarna från tredje part](#creative-settings-third-party).

   Du kan kopiera och klistra in alla [tillgängliga makron](/help/creative/creative-macros.md) i JavaScript-taggen.

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
