---
title: Hantera resursfiler
description: Lär dig hur du överför och hanterar resursfiler för en annonsörer.
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Hantera resursfiler

* Dynamiska HTML5-annonser kräver en feed-fil i Microsoft Excel-kalkylbladsformat (XLSX) och de faktiska bildresurserna som kalkylbladet refererar till.

* Statiska HTML5-annonser kräver endast en enda bildresurs per annons.

* Videoannonser kräver en flödesfil i Microsoft Excel-kalkylbladsformat (XLSX) och de faktiska videoresurserna som kalkylbladet refererar till.

>[!NOTE]
>
> Du kan bara använda varje feed-fil för en katalog.

## Filkrav

* Dynamiska HTML5-annonser:

   * En flödesfil i CSV-, TSV- eller Microsoft Excel-kalkylbladsformat (XLSX), med en rubrikrad och en datarad för varje annonsvariant. Inkludera ett bildnamn i varje rad med formatet `images/image_name` (till exempel `images/300x250_acme_logo.png`).

     Annonsörsspecifika fältnamn måste mappa till de [tillgängliga fälten för dynamiska annonsflödesfiler](/help/creative/appendix-available-feed-fields.md).

   * De associerade bildresurserna i GIF-, JPEG-, JPG- eller PNG-format.<!-- Is this true: The maximum file size is two (2) MB. --> Se de [kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md).

  Du kan överföra en enskild XLSX-fil, en enda bildfil eller en enskild ZIP-fil som innehåller en kombination av XLSX- och bildfiler.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statiska HTML5-annonser:

   * En bildresurs per annons i GIF-, JPG-, JPEG- eller PNG-format.

     Du kan överföra en eller flera bilder i en ZIP-fil.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Dynamiska videoannonser:

   * En flödesfil i CSV-, TSV- eller Microsoft Excel-kalkylbladsformat (XLSX), med en rubrikrad och en datarad för varje annonsvariant. Inkludera ett videonamn i varje rad med formatet `videos/image_name` (till exempel `videos/300x250_acme_logo.png`). ZIP-filen kan vara högst 512 MB med högst 500 rader.

     Annonsörsspecifika fältnamn måste mappa till de [tillgängliga fälten för dynamiska annonsflödesfiler](/help/creative/appendix-available-feed-fields.md).

     För alla konton med dynamiska videoklipp är det bästa sättet att [skapa en katalog](catalog-manage.md) med resursfilen tillsammans med en kopia av [huvudflödesmallen [!UICONTROL Adobe Creative Template]](feed-template-manage.md) där du mappar varje fält i resursfilen till ett fält på Advertising Creative-serverdelen.

   * De associerade videoresurserna i MP4-, MOV- eller WEBM-format. Bland annonsmallarna finns startkort, slutkort, övertäckning, bottenövertäckning och L-formade. Varaktigheten för varje video måste vara mellan 1 och 90 sekunder. Se de [kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md).

  Du kan överföra en enskild XLSX-fil, en enda bildfil eller en enskild ZIP-fil som innehåller valfri kombination av XLSX- och videofiler.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Överföra en resursfil

>[!NOTE]
>
>I stället för att överföra resursfiler kan du överföra en katalog direkt när du [lägger till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md). Alla kataloger som du skapar där blir tillgängliga i vyn [!UICONTROL Catalogs] för framtida bruk.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Assets]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Asset]** i det övre högra hörnet.

1. Konfigurera resursfilen:

   1. Välj annonsören som har åtkomst till resursfilen.

   1. Ange resursfilen på något av följande sätt:

      * Dra och släpp en fil på enheten eller nätverket i rutan.

      * Klicka på **[!UICONTROL Select a file]** för att leta upp filen på enheten eller i nätverket.

   1. Klicka på **[!UICONTROL Upload]**.

Alla ZIP-filer dekomprimeras automatiskt. När du överför en kalkylbladsfil visas filen på underfliken [!UICONTROL Feeds]. När du överför en bildfil visas bildfilen på underfliken [!UICONTROL Images].

## Hämta en resursfil

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Assets]**.

1. Håll markören över resursraden och klicka på **[!UICONTROL Download]**.

   Filen laddas ned enligt webbläsarens normala procedur.

## Ta bort en resursfil

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Assets]**.

1. Håll markören över resursraden och klicka på **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Tillgängliga fält för dynamiska och feed-filer](/help/creative/appendix-available-feed-fields.md)
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera flödesmallar](/help/creative/feeds/feed-template-manage.md)
>* [Hantera kataloger](/help/creative/feeds/catalog-manage.md)
>* [Hantera dynamiska annonsmallar](/help/creative/ad-templates/ad-template-manage.md)
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md)
