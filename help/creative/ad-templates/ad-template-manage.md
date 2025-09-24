---
title: Hantera dynamiska annonsmallar
description: Läs mer om xxxx.
feature: Creative Templates
source-git-commit: 5828fada55ba9506589df6088ea58b896084700c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Hantera dynamiska annonsmallar

Skapa en separat annonsmall för varje kombination av annonstyp (statisk HTML5 eller dynamisk HTML5) och annonsstorlek genom att överföra en zippad HTML5-fil med det önskade annonsformatet. För dynamiska HTML5-annonser överför du också en fil som innehåller annonsattributen <!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Skapa en dynamisk annonsmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Ad Template]** uppe till höger

1. Ange inställningar för [annonsmallen](#ad-template-settings)

1. Klicka på **[!UICONTROL Create]**.

## Redigera en dynamisk annonsmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

1. Håll markören över annonsmallsraden och klicka på **[!UICONTROL Edit]**.

1. Redigera [annonsmallsinställningarna](#ad-template-settings).

1. Klicka på **[!UICONTROL Save]**.

## Ladda ned en dynamisk annonsmall

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

1. Håll markören över annonsmallsraden och klicka på **[!UICONTROL Download]**.

   Filen laddas ned enligt webbläsarens normala procedur.

## Ta bort en dynamisk annonsmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

1. Håll markören över annonsmallsraden och klicka på **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.<!-- Confirm -->

## Skapa dynamiska annonser från en annonsmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** på huvudmenyn.

1. Håll markören över annonsmallsraden och klicka på **[!UICONTROL Create Dynamic Ad]**.

   Fälten [!UICONTROL New Dynamic Ad], [!UICONTROL Ad Template Size] och [!UICONTROL Ad Template Type] markeras automatiskt och är skrivskyddade på skärmen [!UICONTROL Ad Template].

1. Ange dynamiska annonsinställningar för att [skapa dynamiska annonser](/help/creative/creative-libraries/creative-add-dynamic.md).

## Lägg till mallinställningar {#ad-template-settings}

### Information om annonsmall

**[!UICONTROL Advertiser]**: (Skrivskyddat för befintliga mallar) Annonsören som annonser ska genereras för.

**[!UICONTROL Ad Template Name]**: Ett unikt annonsmallsnamn för annonseraren.

**[!UICONTROL Ad Template Type]**: (Skrivskyddat för befintliga mallar) Annonsmallformatet: *Static HTML5* eller *Dynamic HTML5*.

**[!UICONTROL Ad Template Size]**: (Skrivskyddat för befintliga mallar) Dimensionerna för annonserna som skapas av mallen.

**[!UICONTROL Description]**: (Valfritt) Information som är till hjälp för alla som använder annonsmallen.

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

En zippad HTML5-fil med önskat annonsformat. Om du redan har överfört en fil visas filnamnet.

Se den [HTML5-kreativa specifikationen](/help/creative/creative-libraries/html5-creative-specification.md).

Så här överför du en fil:

1. Klicka på **[!UICONTROL Upload HTML5 zip]**.

1. Leta reda på filen på enheten eller i nätverket.

### (dynamiska HTML5-annonsmallar) Attributfil

<!-- EXPLAIN -->En fil som innehåller attribut för annonsmallen. Om du redan har överfört en fil visas filnamnet.

<!-- Add specs for this file type -->

Så här överför du en fil:

1. Klicka på **[!UICONTROL Upload Attributes File]**.

1. Leta reda på filen på enheten eller i nätverket.

>[!MORELIKETHIS]
>
>* [Arbetsflöde för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera resursfiler](/help/creative/feeds/asset-manage.md)
>* [Hantera flödesmallar](/help/creative/feeds/feed-template-manage.md)
>* [Hantera kataloger](/help/creative/feeds/catalog-manage.md)
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md)

