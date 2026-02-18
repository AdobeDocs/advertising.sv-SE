---
title: Lägg till dynamiska kreatörer i ett kreativt bibliotek
description: Lär dig lägga till dynamiska kreatörer i ett kreativt bibliotek.
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
source-git-commit: 8a304eb74549ca1a81257e9f672d311d39987b79
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Lägg till dynamiska kreatörer i ett kreativt bibliotek

Lägg till dynamiska kreatörer i dina [kreativa bibliotek](creative-library-manage.md) som du kan använda med dynamiska [annonsupplevelser](/help/creative/experiences/experience-about.md). Du kan skapa antingen en enda statisk HTML5-annons eller dynamiska HTML5-annonser från en enda annonsmall. För dynamiska HTML5-annonser använder du resurser i angivna kataloger som har skapats från feed-filer.

>[!PREREQUISITES]
>
>Innan du kan lägga till dynamiska kreatörer i ett kreativt bibliotek måste du slutföra andra steg - som att skapa annonsmallen, överföra resurser och (dynamiska annonser från HTML5) skapa en flödesmall och en katalog. Se [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md).

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## Lägg till dynamiska kreatörer med en dynamisk HTML5-annonsmall

1. Gör något av följande:

   * Från ett kreativt bibliotek:

      1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

      1. Klicka på biblioteksnamnet.

      1. På fliken **[!UICONTROL Creatives]** klickar du på **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

   * Från en annonsmall:

      1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

      1. Håll markören över annonsmallsraden och klicka på **[!UICONTROL Create Dynamic Ad]**.

1. Ange [dynamiska annonsinställningar](/help/creative/creative-libraries/creative-settings-dynamic.md):

   1. Ange grundläggande annonsinformation, inklusive den kreativa typen.

   1. Välj annonsmallen som ska användas för kreatörerna.

      Använd en HTML5-annonsmall för webbannonser och en videoreklammall för videoannonser.

   1. Välj den katalog från vilken annonserna ska skapas.

   1. Välj villkoren för vilka katalograder som ska användas för att skapa annonser.

   1. Mappa varje attribut (dynamiskt annonsfält) i den angivna annonsmallen till en kolumn i den angivna feed-filen (katalogetikett) eller ange statiska värden.

   1. Klicka på **[!UICONTROL Continue]** om du vill förhandsgranska de kreatörer som ska genereras. Du kan göra något av följande i förhandsgranskningen:

      * Använd filtren ovanför förhandsvisningsområdet om du vill filtrera kreatörerna efter katalog, filtervärde <!-- explain more--> och annonsstorlek.

      * Om du vill söka efter en produkt med hjälp av dess unika ID i sökfältet nedanför förhandsvisningsområdet.

      * Om du vill ändra vilka kolumner som visas klickar du på ![Kolumnfilter](/help/creative/assets/custom-columns.png "Kolumnfilter") under förhandsvisningsområdet.

      * Markera kryssrutan för raden om du vill förhandsgranska en viss kreativ.

      * Ändra innehållet:

         * Om du vill redigera värdet för en cell i tabellen klickar du inuti cellen och redigerar värdet. Klicka utanför cellen eller tryck på **[!DNL Enter]** om du vill spara ändringarna.

         * Om du vill markera en enskild produkt som standard <!--Explain what this means. --> håller du pekaren över raden och klickar på **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

         * (När annonsen innehåller mer än ett erbjudande) Om du vill markera flera produkter som standard markerar du raderna (upp till antalet erbjudanden) och klickar på **[!UICONTROL Set as Default]** i verktygsfältet för gruppåtgärder.

      * Om du vill ta bort en produkt från katalogen håller du pekaren över raden och klickar på **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

      * (När annonsen innehåller mer än ett erbjudande) Om du vill ta bort flera produkter från katalogen markerar du raderna (upp till antalet erbjudanden) och klickar på **[!UICONTROL Delete Row]** i verktygsfältet för gruppåtgärder.

1. Spara kreatörerna:

   * Så här sparar du annonserna och lägger till dem i ett [kreativt paket](/help/creative/creative-libraries/bundle-manage.md) i biblioteket:

      1. Klicka på **[!UICONTROL Save and Attach to Bundle]**.

      1. Klicka på **[!UICONTROL Save]** om du vill spara annonserna.

      1. Markera paketen och klicka sedan på **[!UICONTROL Attach Creative to Bundles]**.

   * Om du vill spara annonserna och avsluta konfigurationen klickar du på **[!UICONTROL Save]** och sedan på **[!UICONTROL Save]** igen.

>[!MORELIKETHIS]
>
>* [Dynamiska kreativa inställningar](creative-settings-dynamic.md)
>* [Redigera en dynamisk kreativ i ett kreativt bibliotek](creative-edit-dynamic.md)
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
