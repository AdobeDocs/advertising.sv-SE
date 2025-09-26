---
title: Hantera flödeskataloger
description: Lär dig hantera flödeskataloger.
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Hantera flödeskataloger

Bearbetade flödeskataloger är uppsättningar med potentiella annonsvariationer som skapas från en angiven feedfil och en angiven feedmall. Dynamiska HTML5-annonser, men inte statiska HTML5-annonser, kräver en katalog för att skapa dynamiska annonser.

Bearbeta katalogen innan du kan skapa annonsvariationer och [lägga till dynamiska annonser i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md). Du kan uppdatera feed-filen senare och bearbeta om katalogen för att skapa en ny uppsättning annonsvariationer.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

## Skapa en katalog {#feed-catalog-create}

>[!NOTE]
>
>Du kan också överföra en katalog direkt när du [lägger till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md). Alla kataloger som du skapar där blir tillgängliga i vyn [!UICONTROL Catalogs] för framtida bruk.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Catalog]**.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Template]** i det övre högra hörnet.

1. Ange [kataloginställningarna](#catalog-settings) efter behov.

1. Klicka på **[!UICONTROL Next]**.

1. Granska möjliga annonsvariationer som kan skapas för katalogen.

1. Klicka på **[!UICONTROL Save]**.

## Redigera en katalog

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Catalog]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Edit]**.

1. Redigera [kataloginställningarna](#catalog-settings) efter behov.

1. Granska möjliga annonsvariationer som kan skapas för katalogen.

1. Klicka på **[!UICONTROL Save]**.

## Bearbeta en katalog {#feed-catalog-process}

När du bearbetar en katalog blir annonsvariationerna tillgängliga för att skapa dynamiska HTML5-annonser.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Catalog]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Run Now]**.

## Pausa en aktiv katalog

Pausa en katalog för att göra den inaktiv.<!-- Can you Activate it again? -->

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Aktivera en pausad katalog

<!-- Verify if this is available. -->

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Activate]**.

## Arkivera en katalog

Arkivera en katalog för att ta bort den.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Templates]**.

1. Håll markören över mallraden och klicka på **[!UICONTROL Archive]**.

1. Klicka på **[!UICONTROL Archive]** i bekräftelsemeddelandet.

## Kataloginställningar {#catalog-settings}

**[!UICONTROL Advertiser]:** Annonsören som kan använda katalogen.

**[!UICONTROL Asset]:** Den feed-fil som ska användas som indata för katalogen.

**[!UICONTROL Catalog Name]:** Ett unikt katalognamn för den angivna annonsören. Som standard används feed-filens namn, inklusive filtillägget, vilket är det bästa sättet att identifiera.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** Den feed-mall som ska användas för att mappa fält i den angivna resurs-/feed-filen till fält på Advertising Creative serverdel.

>[!MORELIKETHIS]
>
>* [Spåra status för katalogbearbetningsjobb](/help/creative/feeds/job-status-track.md)
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera resursfiler](/help/creative/feeds/asset-manage.md)
>* [Hantera flödesmallar](/help/creative/feeds/feed-template-manage.md)
>* [Hantera dynamiska annonsmallar](/help/creative/ad-templates/ad-template-manage.md)
>* [Lägg till dynamiska kreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-dynamic.md)
