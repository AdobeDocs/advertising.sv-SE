---
title: Hantera resursfiler
description: Lär dig hur du överför och hanterar resursfiler för en annonsörer.
feature: Creative Dynamic Creatives
source-git-commit: 6f2f6580e8d4fc11f52a97b086ce453e423ab4e6
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# Hantera resursfiler

Annonser i dynamiska HTML5 kräver både en feed-fil i kalkylbladet (XLSX) i Microsoft Excel och de bildresurser som kalkylbladet refererar till (förutom Adobe Experience Manager-resursreferenser). Statiska HTML5-annonser kräver endast en enda bildresurs per annons.

>[!NOTE]
>
> Du kan bara använda varje feed-fil för en katalog.

## Filkrav

* Dynamiska HTML5-annonser:

   * En flödesfil i Microsoft Excel-kalkylbladsformat (XLSX), med en rubrikrad och en datarad för varje annonsvariant. Inkludera ett bildnamn eller en referens till en Adobe Experience Manager i varje rad.<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

     Referera bilden med formatet `images/image_name` (till exempel `images/300x250_acme_logo.png`.)<!-- Verify.  Also need to include the spec for how to reference images in AEM --> för bilder som du ska överföra

   * De associerade bildresurserna i GIF-, JPEG-, JPG- eller PNG-format.<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. --> Se de [kreativa storlekar som stöds](/help/creative/creative-libraries/creative-sizes.md).

  Du kan överföra en enskild XLSX-fil, en enda bildfil eller en enskild ZIP-fil som innehåller en kombination av XLSX- och bildfiler.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statiska HTML5-annonser:

   * En bildresurs per annons i GIF-, JPG-, JPEG- eller PNG-format.

     Du kan överföra en eller flera bilder i en ZIP-fil.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

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
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera flödesmallar](/help/creative/feeds/feed-template-manage.md)
>* [Hantera kataloger](/help/creative/feeds/catalog-manage.md)
>* [Hantera dynamiska annonsmallar](/help/creative/ad-templates/ad-template-manage.md)
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md)
