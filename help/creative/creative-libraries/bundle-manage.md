---
title: Hantera kreativa paket
description: Läs mer om xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---

# Hantera kreativa paket

*Stängd beta*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Paket är grupper av kreatörer som du kan lägga till i en upplevelse som en enhet. När du har skapat en paketbehållare kan du koppla kreatörer till paketet. Standardpaket kan bara innehålla standardannonser, och dynamiska paket kan bara innehålla dynamiska annonser. Du kan åsidosätta landningssidor, visningsspårningstaggar och klickspårningstaggar för alla kreatörer i ett paket som är tilldelat en upplevelse inifrån upplevelsebeslutsträdet, utan att det påverkar grundskaparna.

[!DNL Creative] roterar genom de kreativa i paketet enligt inställningarna för varje upplevelse som paketet är tilldelat till. Du kan också tillåta att [!DNL Creative] optimerar annonselementen för alla upplevelser baserat på prestanda med algoritmisk annonrotation, som drivs av Adobe Sensei.

För att optimera annonselement för olika paket i en annonsupplevelse kan varje paket bara innehålla en av varje kombination av \[kreativ storlek + språk\]. Om ett paket t.ex. innehåller en 250 × 250-creative med standardspråket &quot;French&quot;, kan du inte lägga till ytterligare en 250 × 250-creative med standardspråket &quot;French&quot;. Om du har flera kreatörer av samma storlek på samma språk kan du lägga till dem separat i upplevelsen.

Kreatörer som är knutna till programpaket är fortfarande tillgängliga som enskilda kreatörer. Du kan lägga till en enda kreatör i flera paket. Om du redigerar några inställningar för en kreatör som är kopplad till ett paket, sprids ändringarna till paketet. Alla anpassade landningssidor, taggar för visningsspårning och klickspårningstaggar som är konfigurerade för den kreativa delen av en upplevelse används alltid för upplevelsen.

<!-- multiselect only to duplicate and delete -->

## Skapa ett paket för ett kreativt bibliotek

Du kan bifoga ett kreativt program till flera paket.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]** i det övre högra hörnet.

1. Ange en unik **[!UICONTROL Bundle Name]** och **[!UICONTROL Bundle Type]:** *Standard* (för standardkreatörer) eller *Dynamisk* (för dynamiska kreatörer).

1. Klicka på **[!UICONTROL Create]**.

## Visa en lista över kreatörerna i ett paket

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Klicka på paketkortet eller raden för att visa alla kreatörer i paketet.

## Duplicera paket

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Markera de paket som ska dupliceras:

   * Så här duplicerar du ett enskilt paket:

      * I kortvyn klickar du på **[!UICONTROL ...]** bredvid paketnamnet och sedan på **[!UICONTROL Duplicate]**.

      * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Duplicate]**.

   * Om du vill duplicera ett eller flera paket markerar du kryssrutan för varje paket som du vill duplicera. Klicka på **[!UICONTROL Duplicate]i verktygsfältet för gruppåtgärder.**

     Om du vill markera alla rader markerar du den globala kryssrutan i det övre vänstra hörnet.

   De nya paketen har namnet `<original name> (copy) # 1` (eller nästa nummer i sekvensen). Om du t.ex. gör två kopior av&quot;Test bundle&quot;, får dubbletterna namnen&quot;Test bundle (copy) # 1&quot; och&quot;Test bundle (copy) # 2&quot;.

## Redigera ett paketnamn

Ändringar i ett paketnamn sprids över alla associerade upplevelser.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Välj paketet:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid biblioteksnamnet och sedan på **[!UICONTROL Edit]**.

   * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Edit]**.

1. Redigera **[!UICONTROL Bundle Name]**.

   [!UICONTROL Bundle Name] måste vara unik.

1. Klicka på **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Koppla samman kreatörer i ett paket

Du kan koppla [befintliga standardkreatörer](/help/creative/creative-libraries/creative-libraries-about.md) till ett standardpaket och koppla befintliga dynamiska kreatörer<!-- [existing dynamic creatives](creative-dynamic-manage.md) --> till ett dynamiskt paket. Genom att bifoga ett kreativt innehåll i ett paket blir det kreativa tillgängliga i alla upplevelser som paketet är avsett för. Varje paket kan bara innehålla en av varje kombination av \[creative size + language\].

<!--
>[!NOTE]
>
>You can also [attach creatives to bundles from the Standard Ads and Dynamic Ads views](creative-attach-detach-bundles.md).
-->

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Välj paketet:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid paketnamnet och sedan på **[!UICONTROL Attach Creatives]**.

   * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Attach Creatives]**.

   Alla kreatörer som är berättigade till programpaketet visas i rätt ram. Creative-program som redan är kopplade till paketet listas men kan inte markeras.

1. Markera kryssrutan bredvid varje kreatör som ska kopplas till paketet i den högra bildrutan och klicka sedan på **[!UICONTROL Attach Creative to Bundle]**.

## Frigör kreatörer från ett paket {#bundle-detach-creatives}

Att frigöra en kreatör från ett paket tar bort kopplingen mellan de båda, så att den kreativa delen inte längre används för upplevelser som riktar sig mot paketet.

Att frigöra en kreatör från paketet innebär inte att den kreativa personen tas bort från fliken Creative i ditt kreativa bibliotek.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Klicka på paketkortet eller raden för att visa alla kreatörer i paketet.

1. Välj vilka kreatörer som ska kopplas loss från paketet:

   * Så här frigör du en enskild kreatör:

      * I kortvyn klickar du på **[!UICONTROL ...]** bredvid det kreativa namnet och sedan på **[!UICONTROL Detach]**.

      * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Detach]**.

   * Om du vill frigöra en eller flera kreatörer markerar du kryssrutan för varje kreatör som du vill frigöra. Klicka på **[!UICONTROL Detach]** i verktygsfältet för gruppåtgärder.

     Om du vill markera alla rader markerar du den globala kryssrutan i det övre vänstra hörnet.

## Förhandsgranska en kreatör i ett paket

Du kan förhandsgranska en kreativ bild som tittarna ser den, med hyperlänkar.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Klicka på paketkortet eller raden för att visa alla kreatörer i paketet.

1. Välj kreatör:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid det kreativa namnet och sedan på **[!UICONTROL Preview]**.

   * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Preview]**.

1. (Valfritt) Om du vill ändra storlek på bilden på skärmen väljer du ett alternativ i listan **[!UICONTROL Zoom]**, från 10 % till 100 % av bildstorleken.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Valfritt) Klicka på ![Hämta](/help/creative/assets/download.png "Hämta") om du vill hämta den kreativa versionen.

   Filen laddas ned enligt webbläsarens normala procedur.


<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Ta bort paket

Du kan ta bort paket som inte har tilldelats en [live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses)-upplevelse. Om ett paket har tilldelats en direktsänd upplevelse [tar du bort paketet från beslutsträdet](/help/creative/experiences/experience-target-node-delete.md) för upplevelsen innan du fortsätter.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. Klicka på fliken **[!UICONTROL Bundles]**.

1. Markera de paket som ska tas bort:

   * Så här tar du bort ett enskilt paket:

      * I kortvyn klickar du på **[!UICONTROL ...]** bredvid paketnamnet och sedan på **[!UICONTROL Delete]**.

      * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Delete]**.

   * Om du vill ta bort ett eller flera paket markerar du kryssrutan för varje paket som du vill ta bort. Klicka på **[!UICONTROL Delete]i verktygsfältet för gruppåtgärder.**

     Om du vill markera alla rader markerar du den globala kryssrutan i det övre vänstra hörnet.

1. Klicka på **[!UICONTROL Delete]i bekräftelsemeddelandet.**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Tilldela och ta bort tilldelning av kreativa paket till en slutlig nod i en upplevelse](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Lägg till standardkreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-standard.md)
>* [Hantera kreativa bibliotek](/help/creative/creative-libraries/creative-library-manage.md)
>* [Om dina kreativa bibliotek](/help/creative/creative-libraries/creative-libraries-about.md)
