---
title: Hantera flödesmallar
description: Lär dig hur du hanterar flödesmallar.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Hantera flödesmallar

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Flödesmallar mappar fält i dina matningsfiler/kataloger med fält på Advertising Creative-serverdel. Dynamiska HTML5-annonser, men inte statiska HTML5-annonser, kräver en matningsmall för att skapa dynamiska annonser.

Du kan använda en feed-mall med flera annonsmallar.

## Skapa en flödesmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Template]** i det övre högra hörnet.

1. Ange inställningarna för [feed-mallen](#feed-template-settings).

1. Klicka på **[!UICONTROL Save]**.

## Redigera en feed-mall

**Obs!** Du kan bara redigera feedelsmallar som du har skapat.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Duplicate]**.

1. Redigera inställningarna för [feed-mallen](#feed-template-settings) efter behov.

1. Klicka på **[!UICONTROL Save]**.

## Visa en flödesmall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL View]**.

## Duplicera en feed-mall

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Duplicate]**.

1. Ange en unik [!UICONTROL Duplicate Template] på skärmen **[!UICONTROL Template Name]**. Om du duplicerar en mall som har skapats av någon annan väljer du **[!UICONTROL Advertiser]**. Om du vill kan du redigera andra inställningar för [feed-mallen](#feed-template-settings) efter behov.

1. Klicka på **[!UICONTROL Save]**.

## Hämta en feed-mall

Hämtade feedmallar är i zippat Microsoft Excel-kalkylbladsformat (XLSX).

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Download]**.

   Filen laddas ned enligt webbläsarens normala procedur.

## Inställningar för flödesmall {#feed-template-settings}

### Inställningar för [!UICONTROL General]

**[!UICONTROL Template Name]:** Ett unikt mallnamn för den angivna annonsören.

**[!UICONTROL Advertiser]:** Annonsören som kan använda mallen.

**[!UICONTROL Description]:** (Valfritt) Information som är till hjälp för alla som använder feed-mallen.

### Inställningar för [!UICONTROL Field Mapping]

Mappa varje fält i feed-filen till ett fält på Advertising Creative-serverdelen. En lista över backend-fält och deras obligatoriska attribut finns i [Tillgängliga fält för dynamiska och feed-filer](/help/creative/appendix-available-feed-fields.md).<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

Minst ett matningsfilfält måste markeras som [!UICONTROL Is Unique]. Klicka på **[!UICONTROL +]** om du vill lägga till en fältmappning. Klicka på **[!UICONTROL +]** om du vill ta bort den senaste fältmappningen.

**[!UICONTROL Field Name]:** Fältet i feed-filen.

**[!UICONTROL Description]:** (Valfritt) Information som är till hjälp för alla som använder feed-mallen.

**[!UICONTROL Is Unique]:** Anger att fältet är ett unikt ID (nyckel). Minst ett fält per feed-mall måste vara unikt. Om du vill välja det här alternativet klickar du på knappen för att flytta det åt höger.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** Fältet [ på Advertising Creative backend](/help/creative/appendix-available-feed-fields.md) som mappar till den angivna [!UICONTROL Field Name] i feed-filen.

>[!MORELIKETHIS]
>
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera resursfiler](/help/creative/feeds/asset-manage.md)
>* [Hantera kataloger](/help/creative/feeds/catalog-manage.md)
>* [Spåra status för katalogbearbetningsjobb](/help/creative/feeds/job-status-track.md)
>* [Hantera dynamiska annonsmallar](/help/creative/ad-templates/ad-template-manage.md)
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md)
