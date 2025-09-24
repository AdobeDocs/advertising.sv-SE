---
title: Dynamiska kreativa inställningar
description: Referera inställningarna för dynamiska kreatörer.
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Dynamiska kreativa inställningar

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Dynamiska annonsinställningar<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Grundläggande information

**[!UICONTROL Dynamic Ad Name]:** Ett unikt namn för den kreativa.

**[!UICONTROL Advertiser]:** Annonsören som annonserna ska skapas för.

**[!UICONTROL Library]:** Det kreativa bibliotek där annonserna ska skapas. Om du skapar annonserna inifrån [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] är biblioteksnamnet redan markerat och skrivskyddat.

**[!UICONTROL Ad Template Size]:** Annonsdimensionerna för annonsmallen som annonsen ska skapas från. Om du först väljer en specifik [!UICONTROL Ad Template] markeras värdet automatiskt.

## Annonsmall

**[!UICONTROL Ad Template]:** Annonsmallen som annonserna ska skapas från.&lt;!— även ett alternativ för att ladda upp en egen annonsmall — måste du lägga till specifikationerna för det —>

**[!UICONTROL Number of offers (Max 50)]:** Antalet erbjudanden som kan skapas för varje annons.&lt;!— Klargör detta - är detta frekvensbegränsningen (max antal gånger en annons kan användas)? —>

## Kataloger

**[!UICONTROL Template]:** Den feed-mall som ska användas för att skapa annonserna.&lt;!— även ett alternativ för att överföra en egen feed-mall — måste du lägga till specifikationerna för det —>

**\[Kataloger\]**: En eller flera av de angivna annonserarnas kataloger som annonser ska genereras från.&lt;!— även ett alternativ för att överföra din egen katalog (Kan du inte hitta den katalog du behöver? Ladda ned en mall, skapa en egen och ladda upp den från din enhet.) — need to add the specfor that —>

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: De typer av kolumner i feed-filen som det måste finnas värden för för att skapa annonser: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Obs!** De här inställningarna fungerar oberoende av de avancerade inställningarna för annonsupplevelser.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappa varje attribut (dynamiskt annonsfält) i den angivna annonsmallen till en kolumn i den angivna feed-filen (katalogetikett).

>[!MORELIKETHIS]
>
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](creative-add-dynamic.md)
>* [Redigera dynamiska kreatörer i ett kreativt bibliotek](creative-edit-dynamic.md)
>* [Arbetsflöde för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
