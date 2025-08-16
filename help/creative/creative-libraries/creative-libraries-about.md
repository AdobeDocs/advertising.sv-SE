---
title: Om dina kreativa bibliotek
description: Lär dig hur du hanterar kreatörerna för era annonsupplevelser.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 3c4fcd4cf63003cf10775ebec23ae3f68d3bbd07
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---

# Om dina kreativa bibliotek

Med era kreativa bibliotek kan ni hantera de kreativa verktyg ni kommer att använda i era annonsupplevelser. Du kan skapa flera bibliotek, där var och en har en uppsättning kreativa funktioner och *kreativa paket*, som är grupper med kreativa alternativ som du kan lägga till i en upplevelse som en enhet.

Biblioteken kan innehålla:

* **Enskilda kreatörer:** Du kan inkludera enskilda kreatörer direkt i annonsupplevelser som inte har definierade användarmål. Du kan också använda dina kreatörer för att skapa paket, som du kan inkludera i riktade [annonsupplevelser](/help/creative/experiences/experience-about.md).

   * **Standardkreatörer:** Du kan överföra och hantera kreatörer i [olika format](#creative-creative-formats). För varje kreatör anger du standardspråket för varje annons som du kopplar till den kreativa sidan och standardstartsidan som öppnas när en användare klickar på en annons som innehåller den kreativa sidan. Du kan också ange etiketter som ska användas som filter i olika vyer inom [!DNL Creative] och som kolumnvärden i [!UICONTROL Custom Creative Report] när du inkluderar med dimensionen [!UICONTROL Creative Label].

   * **Dynamiska kreatörer:** (endast befintliga Adobe Advertising DCO-kunder) Administratörsanvändare kan skapa dynamiskt genererade kreatörer genom att mappa dynamiska variabler i en annonsmall till värden i en feed-fil. Alla användare kan förhandsgranska, duplicera och ta bort befintliga dynamiska annonser.

* **Creative bundles:** Gruppera kreatörer i paket som kan användas för flera upplevelser med definierade användarmål. Du kan skapa *standardvisningspaket* som består av standarddisplayannonser, *standardvideopaket* som består av standardvideoannonser och *dynamiska visningspaket* som består av dynamiskt genererade displayannonser.

## Creative-format som stöds {#creative-creative-formats}

### Format för standardkreatörer

Du kan lägga till och hantera följande kreativa typer i de [kreativa storlekar](creative-sizes.md) som stöds.

>[!IMPORTANT]
>
>* Även om du tänker använda HTML5, Flexible HTML5 eller andra kreatörer för att skapa standardannonsupplevelser måste du också lägga till bildkreatörer för varje kreativ storlek du använder.
>* För varje standardvisning krävs en standardbild som är kreativ för varje kreativ storlek som tilldelats upplevelsen. Standardbildskaparna används när en webbläsare inte är JavaScript-aktiverad eller när annonsservern inte kan anpassa annonsen på grund av förseningar.
>* För varje standardvideoupplevelse krävs en standardvideokreativ för varje kreativ längd som tilldelats upplevelsen.<!-- when is it used? -->

#### Flexibel HTML5

Flexibla HTML5-kreatörer är HTML5-kreatörer med alla sina bilder och andra attribut som HTML-standardtaggar, som du kan redigera direkt i [!DNL Creative], antingen i ett kreativt bibliotek eller i en enskild upplevelse (vilket skapar en variation av originalet). I DSP är de flexibla HTML 5-programmen avsedda för en viss annonsstorlek (i pixlar). Du kan också ändra standardvärdena för attributen som anges i en flexibel HTML5-kreatör. Senare kan du ange anpassade värden för attributen i en viss upplevelse, vilket skapar en variation av den överordnade kreativiteten.

Du kan antingen överföra flexibla HTML5-användare som ZIP-filer eller använda någon av de mallar som är tillgängliga för ditt konto som utgångspunkt. Se [specifikationerna för flexibla HTML5-kreatörer](html5-creative-specification.md).

#### HTML5 kreatörer

Du kan överföra enkla eller statiska HTML5-kreatörer med alla attribut och bilder angivna som ZIP-filer. Du kan inte redigera några attribut eller lägga till bilder. Överför i stället en ny ZIP-fil för att lägga till en ny kreatör. Se [specifikationerna för enkla och statiska HTML5-kreatörer](html5-creative-specification.md).

#### Bildkreatörer

Du kan inkludera bildkreatörer i GIF-, JPEG-, JPG- eller PNG-format. Du kan överföra godkända bilder från dina Adobe Experience Manager-konton eller bilder från din enhet eller ditt nätverk.

För varje standard-visning och -upplevelse krävs en standardbild som är kreativ för varje kreativ storlek som upplevelsen tilldelas.

#### Tredjepartskreatörer

Ange JavaScript spårningstaggar för kreatörer som har en annonsserver från tredje part. Skriptet varierar beroende på annonsserver. Följande är ett exempel:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Videoredigerare {#creative-video-specs}

Du kan överföra förstahandsvideor för webben, mobiler eller ansluten TV från din enhet eller ditt nätverk. För varje standardvideoreklamupplevelse krävs en standardvideoredigerare för varje kreativ längd som tilldelats upplevelsen. Alla videokreatörer omkodas automatiskt av DSP som VAST 2.0-taggar så att du kan förhandsgranska dem. I [!UICONTROL Tag Manager] kan du välja att [använda DSP-specifik transkodning](/help/creative/experiences/experience-tag-video-transcoding.md) för alla videoannonsupplevelsetaggar.

Se följande krav för videoredigering. **Obs!** Om du ska överföra videoupplevelser till Advertising DSP läser du även DSP [Krav för HD-video i Assets](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets), som kan vara mer begränsat.

**Filtyp:** .mov, .mp4, .webm

**Filstorlek:** Maximalt 512 MB

**Videoproportioner:** 16:9, 4:3

**Videoupplösning:** 640x360 för 360p, 1 280 x 720 för 720p, 1 920 x 1 080 för 1080p

**Videolängd:** Maximalt 90 sekunder

**Bithastighet:** 600-1200 kbit/s för 360p, 1 500-2 500 kbit/s för 720p, 3 000-5 000 kbit/s för 1 080p

**Videobildrutefrekvens:** 23,98 FPS. Ytterligare bildrutefrekvenser kan accepteras baserat på regionala krav eller krav från förlag

**Videokodek:** H.264 (branschstandard), AV1, H.265

**Ljudformat:** ACC (branschstandard/MP4), Opus (WebM/AV1)

**Ljudbithastighet:** 16-512 kbit/s

**Samplingsfrekvens för ljud:** 44100-48000 Hz

**Ljudhastighet:** 44,1 kHz eller 48 kHz

**Annan ljudfil:** Den överförda filen får inte vara sammanflätad, blandad och innehålla ett ljudspår. Det kanske inte finns något ljud, men ett ljudspår måste inkluderas i videofilen.

### Format för dynamiska annonser

Administratörsanvändare kan dynamiskt generera kreatörer i statiskt HTML5- och dynamiskt HTML5-format genom att mappa dynamiska variabler i en annonsmall till värden i en feed-fil. Dynamiska kreatörer kan inkludera kreatörer från era gamla Adobe Advertising Dynamic Creative Optimization-upplevelser (DCO).

## [!UICONTROL Creative Libraries]-vyerna

Mer information om hur du anpassar vyn finns i [Anpassa datavyer](/help/creative/introduction/customize-data-views.md).

### Huvudvyn [!UICONTROL Creative Libraries]

I huvudvyn i [!UICONTROL Creative Libraries] visas alla dina kreativa bibliotek. Data för varje bibliotek omfattar antalet upplevelser som biblioteket tilldelas till, antalet paket, antalet kreatörer, antalet kreativa storlekar, antalet standardspråkmål, skapandedatum och det senaste ändringsdatumet för något element i biblioteket. Tabelläget innehåller även en kolumn för annonsören.

När du är i kortläge kan du bläddra bland bilderna i ett bibliotek med flera kreatörer med hjälp av knapparna &lt; och >.

#### Tillgängliga åtgärder

* [Skapa ett nytt bibliotek](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* För varje kreativt bibliotek:

   * [Redigera ett bibliotek](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Öppna ett bibliotek för att visa de kreatörer och paket som har tilldelats biblioteket](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Ta bort bibliotek](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Vyerna [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

På fliken [!UICONTROL Standard Ads] visas alla standardalternativ som du har skapat. Data för varje kreatör inkluderar den kreativa storleken, den kreativa typen och datumet då de skapades. Tabelläget innehåller även kolumner för standardspråket och standardstartsidan.

##### Tillgängliga åtgärder

* [Lägga till standardkreatörer i ett bibliotek](creative-add-standard.md)

* [Redigera en vanlig kreativ](creative-edit-standard.md)

* [Förgranska en vanlig kreativ](creative-preview.md)

* [Lägg till standardkreatörer i standardpaket för visning och ta bort standardkreatörer från ett standardpaket för visning](creative-attach-detach-bundles.md)

* [Lägg in videokreatörer i standardvideopaket och ta bort videokreatörer från standardvideopaket](creative-attach-detach-bundles.md)

* [Duplicera standardkreatörer](creative-duplicate.md)

* [Hämta standardkreatörer](creative-download.md)

* [Ta bort standardkreatörer](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

Fliken [!UICONTROL Dynamic Ads] visar alla dynamiska kreatörer som har skapats dynamiskt för dina kreativa kataloger, förutom alla dynamiska kreatörer som du [tagit bort manuellt](creative-delete.md) från fliken [!UICONTROL Dynamic Ads]. Om du [manuellt duplicerade](creative-duplicate.md) alla dynamiska kreatörer sedan en katalog senast bearbetades, innehåller listan med användare för den katalogen även dubblettkreatörerna.

Data för varje kreatör omfattar den kreativa typen, den kreativa storleken, antalet kataloger som den kreativa delen tillhör samt skapandedatumet. Tabelläget innehåller även kolumner för mallen som den kreativa personen genererades genom och antalet erbjudanden.

>[!NOTE]
>
>Varje gång en katalog bearbetas uppdateras data för de befintliga dynamiska kreatörerna för den katalogen.

##### Tillgängliga åtgärder

Möjligheten att skapa och redigera dynamiska kreatörer är för närvarande bara tillgängligt för Adobe Account Team. Alla användare kan dock:

* [Förgranska dynamiska kreatörer](creative-preview.md)

* [Lägg till dynamiska kreatörer i dynamiska displaypaket och ta bort dynamiska kreatörer från ett dynamiskt displaypaket](creative-attach-detach-bundles.md)

* [Duplicera dynamiska kreatörer](creative-duplicate.md)

* [Ta bort dynamiska kreatörer](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Vyn [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

I vyn [!UICONTROL Bundles] visas alla standardpaketbehållare och dynamiska paketbehållare. Du kan se kreativa namn, kreativa storlekar och språk för de kreatörer som ingår i varje paket. När du är i kortläge kan du bläddra bland bilderna i ett paket med flera kreatörer med hjälp av knapparna &lt; och >.

#### Tillgängliga åtgärder

* Lägga till standardskärmar, standardvideo och dynamiska bildskärmspaket i ett bibliotek

* Visa en lista över de kreativa i ett paket

* Redigera ett paketnamn

* Lägg in standardskärmar i standardpaket och ta bort standardskärmar från standardpaket

* Lägg in standardvideoklipp i standardvideopaket och ta bort standardvideoklipp från standardvideopaket

* Duplicera paket

* Ta bort paket

>[!MORELIKETHIS]
>
>* [Hantera kreativa bibliotek](/help/creative/creative-libraries/creative-library-manage.md)
>* [Lägg till standardkreatörer i ett kreativt bibliotek](creative-add-standard.md)
>* [Hantera kreativa paket](bundle-manage.md)
>* [Anpassa datavyer](/help/creative/introduction/customize-data-views.md)
