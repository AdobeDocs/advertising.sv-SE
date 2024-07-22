---
title: Hantera lagerdataflödesfiler
description: Lär dig hur du konfigurerar inställningar som styr hur feed-data bearbetas.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Hantera lagerdataflödesfiler

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

Om du skickar in dina egna feed-data måste du överföra filer som innehåller dina produktdata för att dynamiskt skapa kampanjstruktur, annonser och nyckelord baserat på dina produktdata. Du kan sedan koppla dem till annonsnätverksspecifika annonsmallar och bearbeta data via mallarna, och sedan publicera data i relevanta annonsnätverk. Du kan associera flera mallar med en feed-fil, men varje mall kan bara associeras med en feed-fil.

>[!NOTE]
>
>Överför inte filer om du använder data direkt från ett handlarcenterkonto.

Du kan överföra och bearbeta dataflödesfiler på något av följande sätt:

* **Använd FTP automatiskt:** Du kan överföra filer direkt till en FTP-katalog. Feed-tjänsten söker efter nya filer varannan timme. När du har överfört en fil för första gången kan du koppla den till en annonsspecifik mall. Senare kopplas alla filer som du överför med samma namn automatiskt till samma mall. Beroende på hur du [konfigurerar feed-datainställningarna](feed-settings-manage.md) kan Search, Social och Commerce automatiskt sprida feed-data via alla tillämpliga mallar och eventuellt publicera kampanjdata och annonsdata till relevanta annonsnätverk.

  Om du vill konfigurera en FTP-katalog för insättning och automatisk bearbetning av datafiler kontaktar du kontogruppen på Adobe.

* **Manuell bearbetning:** Du kan [överföra feed-filer](#feed-file-upload) manuellt från ACM-vyn ([!UICONTROL Advanced]). När du har associerat en matningsfil med en eller flera annonsspecifika [mallar](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) kan du generera kampanj- och annonsdata genom att [sprida matningsdata via mallar](feed-data-propagate.md) enligt [inställningarna för matningsdata](feed-settings-manage.md). Du kan också förhandsgranska genererade data i kampanjhierarkivyer, generera en kalkylbladsfil för granskning eller generera en kalkylbladsfil för omedelbar publicering i annonsnätverket. Om du inte skickar data direkt kan du [förhandsgranska dem](propagated-data-view.md) och [publicera dem](propagated-data-post.md) senare. Du kan senare [ersätta den befintliga feed-filen med en ny fil](#feed-file-replace) utan att förlora befintliga mallassociationer.

## Krav för flödesfiler

Inga specifika datafält krävs i en enskild fil, men följande krävs för varje fil:

* Den första raden i filen måste innehålla kolumnnamn (kallas även *rubriker*), som motsvarar de dynamiska parametrarna i de associerade mallarna. De återstående raderna måste innehålla data som motsvarar kolumnnamnen. Varje datarad (rad) får bara omfatta en kontokomponent, till exempel en kampanj eller en annons. Värdena på alla rader måste separeras med tabbtecken eller kommatecken. Se exempelfilen [CSV](#example-csv-feed-file) och [TSV-exempelfilen](#example-tsv-feed-file) nedan.

* Filen kan ha vilken storlek som helst men måste ha något av följande filtillägg: `.tsv` (för tabbavgränsade värden), `.txt` (för [!DNL Unicode]-kompatibel ASCII-text), `.csv` (för kommaseparerade värden) eller `.zip` (för en fil i komprimerat ZIP-format som packar upp till en TSV-fil).

* Filnamnet är skiftlägeskänsligt och får inte innehålla följande tecken: `# % & * | \ : " < > . ? /`

* Om du sparar filer i en FTP-katalog måste du använda samma filnamn för varje version av filen.

* ([!DNL Google Ads] endast mallar) Om din mall använder annonsparametern Param2 eller Param2 i textannonser, måste motsvarande datafält i matningsfilen innehålla numeriska data, utan några monetära symboler.

* Om du vill uppdatera befintliga kontokomponenter inkluderar du namnet på den befintliga kampanjen (och dess komponenter, om det är relevant). Om den befintliga strukturen inte anges skapas nya komponenter.

### Exempel på en kommaavgränsad feed-fil {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Exempel på en tabbseparerad feed-fil {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## God praxis

* Använd filer i TSV- eller TXT-format för data som innehåller internationella tecken.

* För att få en upprepningsbar process med begränsad manuell granskning eller redigering ställer du in feedfiler och deras kontostrukturdata enligt följande:

   * Inkludera kolumner och rader som innehåller tillräckligt med data för att skapa kontostrukturen eller mappa till den befintliga kontostrukturen. I idealfallet bör du använda en befintlig kontostruktur som är nära kopplad till produkttaxonomin och till vilken feed-data är lätt att mappa.

   * Ta med beskrivningar som är tillräckligt korta för att användas i annonskopian.

   * Använd konsekventa datamönster och namnkonventioner för alla produktrader.

   * Ta bort alla föregående och efterföljande blanksteg.

   * Ta bort alla förvrängda tecken.

## Visa eller hämta en feed-fil

Du kan öppna eller hämta alla feedsfiler som har överförts manuellt eller med FTP.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Leta reda på feed-filen:

1. Leta reda på en mall som använder feed-filen i listan Mallar.

1. Klicka på **[!UICONTROL Feeds]** i verktygsfältet ovanför datatabellen för att öppna en lista över alla feed-filer.

1. Klicka på feed-filens namn.

1. Öppna eller spara filen enligt webbläsarens normala procedur.

Mer information finns i webbläsarens onlinehjälp.

## Överför en feed-fil manuellt {#feed-file-upload}

>[!NOTE]
> Om du kopplar en mall till en manuellt överförd fil, men sedan överför en annan fil med samma namn, filtillägg och grammatiska skiftläge via FTP, används FTP-filen när du sprider data via mallen. Till exempel ersätter myfile.csv myfile.csv, men det gör inte Myfile.CSV.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Klicka på **[!UICONTROL Feeds]** i verktygsfältet ovanför datatabellen.

1. Klicka på **[!UICONTROL Upload]** ovanför datatabellen.

1. Ange den fil som ska överföras antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på **[!UICONTROL Browse]** för att leta reda på filen på enheten eller i nätverket.

1. Klicka på **[!UICONTROL Upload].

Alla fält i filen valideras. Du kan inte publicera objekt med ogiltiga fältlängder senare förrän du korrigerar värdena. Alla kolumnnamn i filen blir tillgängliga i mallar som dynamiska parametrar.

## Ersätta en feed-fil {#feed-file-replace}

När du ersätter en feed-fil - även om den nya filen har ett annat filnamn eller tillägg - finns det kvar alla befintliga mallassociationer. Den nya filen används när du sprider data via alla mallar som ursprungligen var associerade med den tidigare filen.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Gör något av följande:

   * Klicka på ![Fler alternativ](/help/search-social-commerce/assets/options.png "Fler alternativ") i kolumnen [!UICONTROL Feed] för en tillämplig mall och välj **[!UICONTROL Re-upload]**.

   * Klicka på **[!UICONTROL Feeds]** i verktygsfältet ovanför datatabellen. Markera kryssrutan bredvid det befintliga filnamnet i listan över feedsfiler. Klicka på **[!UICONTROL Upload]** ovanför datatabellen.

   >[!NOTE]
   >
   >Källan till matningsfilen (&quot;[!UICONTROL FTP]&quot; eller &quot;&amp;mdash&quot; för manuellt överförda filer) ingår i kolumnen [!UICONTROL Source].

1. Ange den fil som ska överföras antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på **[!UICONTROL Browse]** för att leta reda på filen på enheten eller i nätverket.

Även om den nya filen har ett annat filnamn eller filtillägg skrivs den befintliga filen över med den nya filen.

1. Klicka på **[!UICONTROL Re-Upload]**.

Alla fält i filen valideras. Du kan inte publicera objekt med ogiltiga fältlängder senare förrän du korrigerar värdena. Alla kolumnnamn i filen blir tillgängliga i mallar som dynamiska parametrar.

## Ta bort feed-filer

Du kan ta bort alla feed-filer som har överförts manuellt eller via FTP. När du tar bort en feed-fil är den inte längre kopplad till några mallar.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Klicka på **[!UICONTROL Feeds]** i verktygsfältet ovanför datatabellen.

1. Markera kryssrutan bredvid varje fil som du vill ta bort.

1. Klicka på **[!UICONTROL Delete]** ovanför datatabellen.

1. Klicka på **[!UICONTROL Yes]** i bekräftelsemeddelandet.

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Sprid feed-data via mallar](feed-data-propagate.md)
>* [Visa data som har genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
