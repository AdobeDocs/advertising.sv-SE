---
title: Dynamiska kreativa inställningar
description: Referera inställningarna för dynamiska kreatörer.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Dynamiska kreativa inställningar

<!-- add a description -->

## Dynamiska annonsinställningar<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Grundläggande information

**[!UICONTROL Creative Type]:** Om den kreativa delen är en *[!UICONTROL Display]* annons (HTML5) eller en *[!UICONTROL Video]* annons.

**[!UICONTROL Dynamic Display Ad Name]** eller **[!UICONTROL Dynamic Video Ad Name]:** Ett unikt namn för den kreativa.

**[!UICONTROL Advertiser]:** Annonsören som annonserna ska skapas för. Om du skapar annonserna inifrån [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] är annonsören redan markerad och skrivskyddad.

**[!UICONTROL Library]:** Det kreativa bibliotek där annonserna ska skapas. Om du skapar annonserna inifrån [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] är biblioteksnamnet redan markerat och skrivskyddat.

## Annonsmall

**[!UICONTROL Ad Template]:** Annonsmallen som annonserna ska skapas från. Välj en befintlig annonsmall eller överför en ny annonsmall och välj malltypen (*Statisk* eller *Dynamisk*). Mallen måste vara i ZIP-format och innehålla:<!-- Need to add more specs for templates -->

* Visningsalternativ: HTML5-filer med önskat annonsformat och (endast dynamiska HTML5-annonser) en fil med annonsattributen (.tdf)

* Videoredigerare: En .scene-fil med önskat annonsformat. ZIP-filen kan vara högst 512 MB.

Klicka på **[!UICONTROL Select Ad Template]** om du vill fortsätta.

**[!UICONTROL Size]:** (Endast dynamiska displayannonser, skrivskyddade) [annonsdimensionerna](/help/creative/creative-libraries/creative-sizes.md) för den valda annonsmallen, som används för att skapa annonserna.

**[!UICONTROL Card Count (Max 50)]:** (Endast displayannonser) Antalet produkter som ska visas i en karusell.

**[!UICONTROL Duration]:** (Endast videoannonser, skrivskyddad) Den videouppspelning som härleds från den valda annonsmallen. Varaktigheten för varje video måste vara mellan 1 och 90 sekunder.

## Kataloger

**\[Kataloger\]**: En eller flera kataloger att generera annonser från. Välj en befintlig katalog eller skapa en ny katalog genom att hämta en befintlig feed-mall och skapa och överföra den nya katalogen. Klicka på **[!UICONTROL Select Catalog]**.

Överförda kataloger måste vara i ZIP-format och innehålla följande:

* (Dynamiska displayannonser och videoannonser) En eller flera flödesfiler i CSV-, TSV- eller Microsoft Excel-kalkylbladsformat (XLSX). Den maximala filstorleken är 512 MB.<!-- Need to add more specs for the feed files -->

* (Visningsannonser) Bildresurser i GIF-, JPEG-, JPG- eller PNG-format

* (Videoannonser) Videomaterial i MP4-, MOV- eller WEBM-format. Bland annonsmallarna finns startkort, slutkort, övertäckning, bottenövertäckning och L-formade. Varaktigheten för varje video måste vara mellan 1 och 90 sekunder.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->De typer av kolumner i feed-filen som det måste finnas värden för för att skapa annonser: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Obs!** De här inställningarna fungerar oberoende av de avancerade inställningarna för annonsupplevelser.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappa varje attribut (dynamiskt annonsfält) i den angivna annonsmallen till en kolumn i den angivna katalogen (katalogetikett) eller ange ett statiskt värde.

>[!MORELIKETHIS]
>
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](creative-add-dynamic.md)
>* [Redigera dynamiska kreatörer i ett kreativt bibliotek](creative-edit-dynamic.md)
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
