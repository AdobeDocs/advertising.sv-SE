---
title: Om dina kreativa bibliotek
description: Lär dig hur du hanterar de kreatörer du kommer att använda i era annonsupplevelser.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# Om dina kreativa bibliotek

*Avslutade betafunktioner*

Med era kreativa bibliotek kan ni hantera alla kreativa funktioner ni kan använda i era annonsupplevelser. Du kan skapa flera bibliotek, där var och en har en uppsättning kreativa funktioner och *kreativa paket*, som är grupper med kreativa alternativ som du kan lägga till i en upplevelse som en enhet.

Biblioteken kan innehålla:

* **Enskilda kreatörer:** Du kan inkludera enskilda kreatörer direkt i annonsupplevelser som inte har definierade användarmål. Du kan också använda dina kreatörer för att skapa paket, som du kan inkludera i riktade [annonsupplevelser](/help/creative/experiences/experience-about.md).

   * **Standardkreatörer:** Du kan överföra och hantera kreatörer i [olika format](#creative-creative-formats). För varje kreatör anger du standardspråket för varje annons som du associerar den kreativa, standardstartsidan som öppnas när en användare klickar på en annons som innehåller den kreativa samt valfria etiketter som ska användas som filter i olika vyer i [!DNL Creative].

   * **Dynamiska kreatörer:** (endast befintliga Adobe Advertising-DCO-kunder) Administratörsanvändare kan skapa dynamiskt genererade kreatörer genom att mappa dynamiska variabler i en annonsmall till värden i en feed-fil. Alla användare kan förhandsgranska, duplicera och ta bort befintliga dynamiska annonser.

* **Creative bundles:** Gruppera kreatörer i paket som kan användas för flera upplevelser med definierade användarmål. Du kan skapa *standardpaket* som består av standardannonser och *dynamiska paket* som består av dynamiskt genererade annonser.

## Creative-format som stöds {#creative-creative-formats}

### Format för standardkreatörer

Du kan lägga till och hantera följande kreativa typer i de [kreativa storlekar](creative-sizes.md) som stöds.

>[!IMPORTANT]
>
>Även om du tänker använda HTML5, Flexible HTML5 eller andra kreatörer för annonsupplevelserna måste du också lägga till bildkreatörer för varje kreativ storlek du kommer att använda.
>
>För varje upplevelse krävs en standardbild som är kreativ för varje kreativ storlek som tilldelats upplevelsen. Standardbildskaparna används när en webbläsare inte är JavaScript-aktiverad eller när annonsservern inte kan anpassa annonsen på grund av förseningar.

#### Flexibel HTML5

Flexibla HTML5-kreatörer är HTML5-kreatörer med alla sina bilder och andra attribut som standardtaggar för HTML, som du kan redigera direkt i [!DNL Creative], antingen i ett kreativt bibliotek eller i en enskild upplevelse (vilket skapar en variation av originalet). De som skapar flexibla HTML5 använder IAB-standarden (Interactive Advertising Bureau) Technology Laboratory för en [annonsportfölj](https://flexibleads.iabtechlab.com/), för vilken annonsformaten är flexibla (och inte fasta) och baseras på annonsens proportioner och storleksintervall, och för vilka annonserna behåller sin upplösning på olika enheter och utgivarplatser.

Du kan <!-- either --> överföra flexibla HTML5-användare som ZIP-filer <!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->. Se [specifikationerna för flexibla HTML5-kreatörer](html5-creative-specification.md).

<!-- Will flattening the view be possible in the MVP?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

Du kan också ändra standardvärdena för attributen som anges i en flexibel HTML5-kreatör. Senare kan du ange anpassade värden för attributen i en viss upplevelse, vilket skapar en variation av den överordnade kreativiteten.

#### HTML5-kreatörer

Du kan överföra enkla eller statiska HTML5-kreatörer med alla attribut och bilder angivna som ZIP-filer. Du kan inte redigera några attribut eller lägga till bilder. Överför i stället en ny ZIP-fil för att lägga till en ny kreatör. Se [specifikationerna för enkla och statiska HTML5-kreatörer](html5-creative-specification.md).

#### Bildkreatörer

Du kan inkludera bildkreatörer i GIF, JPEG, JPG eller PNG-format. Du kan överföra <!--LATER:   images from your Adobe Experience Manager accounts or --> bilder från din enhet eller ditt nätverk.

För varje annonsvisning krävs en standardbild som är kreativ för varje kreativ storlek som tilldelats upplevelsen.

#### Tredjepartskreatörer

Ange JavaScript spårningstaggar för kreatörer som har en annonsserver från tredje part. Skriptet varierar beroende på annonsserver. Följande är ett exempel:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Format för dynamiska annonser

Administratörsanvändare kan skapa dynamiskt genererade kreatörer i statiskt HTML5- och dynamiskt HTML 5-format genom att mappa dynamiska variabler i en annonsmall till värden i en feed-fil. Detta kan omfatta kreatörer från dina gamla Adobe Advertising Dynamic Creative Optimization-upplevelser (DCO).

## [!UICONTROL Creative Libraries]-vyerna

Mer information om hur du anpassar vyn finns i [Anpassa datavyer](/help/creative/introduction/customize-data-views.md).

### Huvudvyn [!UICONTROL Creative Libraries]

Huvudvyerna i [!UICONTROL Creative Libraries] visar alla dina kreativa bibliotek. Data för varje bibliotek omfattar antalet upplevelser som biblioteket tilldelas till, antalet paket, antalet kreatörer, antalet kreativa storlekar, antalet standardspråkmål, skapandedatum och det senaste ändringsdatumet för något element i biblioteket. Tabelläget innehåller även en kolumn för annonsören.

#### Tillgängliga åtgärder

* Skapa nya bibliotek

* För varje kreativt bibliotek:

   * Redigera biblioteksnamnet

   * Öppna biblioteket för att visa de kreatörer och paket som har tilldelats biblioteket

   * Ta bort biblioteket

### Vyerna [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

På fliken [!UICONTROL Standard Ads] visas alla standardalternativ som du har skapat. Data för varje kreatör inkluderar den kreativa storleken, den kreativa typen och datumet då de skapades. Tabelläget innehåller även kolumner för standardspråket och standardstartsidan.

##### Tillgängliga åtgärder

* [Lägga till standardkreatörer i ett bibliotek](creative-add-standard.md)

* [Redigera en vanlig kreativ](creative-edit-standard.md)

* [Förgranska en vanlig kreativ](creative-preview.md)

* [Lägg till standardkreatörer i standardpaket och ta bort standardkreatörer från standardpaket](creative-attach-detach-bundles.md)

* [Duplicera standardkreatörer](creative-duplicate.md)

* [Hämta standardkreatörer](creative-download.md)

* [Ta bort standardkreatörer](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

Fliken [!UICONTROL Dynamic Ads] visar alla dynamiska kreatörer som har skapats dynamiskt för dina kreativa kataloger, förutom alla dynamiska kreatörer som du [tagit bort manuellt](creative-delete.md) från fliken [!UICONTROL Dynamic Ads]. Om du [manuellt duplicerade](creative-duplicate.md) alla dynamiska kreatörer sedan en katalog senast bearbetades, kommer listan med användare för den katalogen även att innehålla dubblettkreatörer.

Data för varje kreatör omfattar den kreativa typen, den kreativa storleken, antalet kataloger som den kreativa delen tillhör samt skapandedatumet. Tabelläget innehåller även kolumner för mallen som den kreativa personen genererades genom och antalet erbjudanden.

>[!NOTE]
>
>Varje gång en katalog bearbetas uppdateras data för de befintliga dynamiska kreatörerna för den katalogen.

##### Tillgängliga åtgärder

Möjligheten att skapa och redigera dynamiska kreatörer är för närvarande bara tillgängligt för Adobe Account Team. Alla användare kan dock:

* [Förgranska dynamiska kreatörer](creative-preview.md)

* [Lägg till dynamiska kreatörer i dynamiska paket och ta bort dynamiska kreatörer från ett dynamiskt paket](creative-attach-detach-bundles.md)

* [Duplicera dynamiska kreatörer](creative-duplicate.md)

* [Ta bort dynamiska kreatörer](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Vyn [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

I vyn [!UICONTROL Bundles] visas alla standardpaketbehållare och dynamiska paketbehållare. Du kan se kreativa namn, kreativa storlekar och språk för de kreatörer som ingår i varje paket.

#### Tillgängliga åtgärder

* Lägga till standardpaket och dynamiska paket i ett bibliotek

* Visa en lista över de kreativa i ett paket

* Redigera ett paketnamn

* Lägg till standardkreatörer i standardpaket och ta bort standardkreatörer från standardpaket

* Duplicera paket

* Ta bort paket

>[!MORELIKETHIS]
>
>* [Hantera kreativa bibliotek](/help/creative/creative-libraries/creative-library-manage.md)
>* [Lägg till standardkreatörer i ett kreativt bibliotek](creative-add-standard.md)
>* [Hantera kreativa paket](bundle-manage.md)
>* [Anpassa datavyer](/help/creative/introduction/customize-data-views.md)
