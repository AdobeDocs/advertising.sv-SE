---
title: Dynamiska kreativa inställningar
description: Referera inställningarna för dynamiska kreatörer.
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
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

**[!UICONTROL Ad Template Size]:** [annonsdimensionerna](/help/creative/creative-libraries/creative-sizes.md) för annonsmallen som annonsen ska skapas från. Om du först väljer en specifik [!UICONTROL Ad Template] markeras värdet automatiskt.

## Annonsmall

**[!UICONTROL Ad Template]:** Annonsmallen som annonserna ska skapas från. Välj en befintlig annonsmall eller överför en ny annonsmall och välj malltypen (*Statisk* eller *Dynamisk*). En överförd mall måste vara i ZIP-format och innehålla HTML5-filer och malldefinitionsfil (template.TDF). <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** Antalet produkter som ska visas i en karusell.

## Kataloger

**[!UICONTROL Template]:** Den feed-mall som ska användas för att skapa annonserna.

**\[Kataloger\]**: En eller flera kataloger att generera annonser från. Välj en befintlig katalog eller skapa en ny katalog genom att hämta en befintlig feed-mall och skapa och överföra den nya katalogen.

Överförda kataloger måste vara i ZIP-format och innehålla följande:

* En eller flera feed-filer i CSV-, TSV- eller Microsoft Excel-kalkylbladsformat (XLSX).<!-- Need to add more specs for that -->

* Bildresurser i GIF-, JPEG-, JPG- eller PNG-format

* (Valfritt) Videomaterial i MP4- eller WEBM-format

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->De typer av kolumner i feed-filen som det måste finnas värden för för att skapa annonser: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Obs!** De här inställningarna fungerar oberoende av de avancerade inställningarna för annonsupplevelser.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappa varje attribut (dynamiskt annonsfält) i den angivna annonsmallen till en kolumn i den angivna katalogen (katalogetikett) eller ange ett statiskt värde.

>[!MORELIKETHIS]
>
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](creative-add-dynamic.md)
>* [Redigera dynamiska kreatörer i ett kreativt bibliotek](creative-edit-dynamic.md)
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
