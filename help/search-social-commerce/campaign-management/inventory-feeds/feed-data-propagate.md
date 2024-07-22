---
title: Sprida lagerflödesdata via mallar
description: Lär dig mer om att sprida data från era inventeringsflöden via annonsmallar för att hantera kontostrukturen och leverera dynamiska annonser.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Sprida lagerflödesdata via mallar

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder) och [!DNL Yandex] enbart konton*

När du har skapat en annonsspecifik feed-mall och associerat en feed-fil eller ett [!DNL Google]- eller [!DNL Microsoft] handlancenter med den, kan du dynamiskt skapa annonser genom att sprida feed-data via mallen enligt [feed-datainställningarna](feed-settings-manage.md). Under spridningen ersätts kolumnnamnen i mallen med datavärden i feeden, och de genererade kampanjerna och deras komponenter har standardinställningarna om inte mallen anger något annat. Beroende på mallalternativen skapar Search, Social och Commerce antingen en ny kontostruktur (kampanjer, annonsgrupper, nyckelord) för annonserna eller mappar annonserna till den befintliga kontostrukturen.

När nya feed-data innehåller nya datavärden för ett objekt, eller mallen har ändrats, tas befintliga annonser bort och nya skapas. Om den enda ändringen är beteckningen [!DNL Google Ads] Param 1 och Param 2 uppdateras endast dessa värden. Dubblerade annonser (samma annonskopia och landningssida) skapas aldrig.

När du sprider data kan du eventuellt förhandsgranska genererade data i en kampanjhierarkivy, generera en kalkylbladsfil för granskning eller generera en kalkylbladsfil för omedelbar publicering i annonsnätverket. När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till på fliken Spridningar, som anger antalet för varje entitetstyp som skapades, pausades eller skulle tas bort baserat på spridningen. Om du inte skickar data direkt kan du förhandsgranska dem och publicera dem senare.

## Sprid feedsfiler från fliken [!UICONTROL Templates]

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Markera kryssrutan bredvid mallarna som ska spridas.

1. Klicka på **[!UICONTROL Propagate]** i verktygsfältet och välj sedan något av följande alternativ:

   * **[!UICONTROL Propagate Only]:** Om du vill visa spridda data på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads]. Du kan fortfarande publicera data för alla komponenter och dess underkomponenter senare från fliken [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Om du vill skapa en kalkylbladsfil (med namnet `<feed file name>_<template name>`) som är tillgänglig i [!UICONTROL Bulksheets]-vyn för granskning (men inte på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads]). Du kan senare publicera kalkylbladsfilen från vyn [!UICONTROL Bulksheets].

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

   * **[!UICONTROL Propagate and Post to SE]:** Om du vill skapa en kalkylbladsfil (med namnet `<feed file name>_<template name>`) som står i kö för publicering i annonsnätverket. Kolumnbladsfilen är tillgänglig i vyn [!UICONTROL Bulksheets], men den är inte tillgänglig på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format.

   &quot;Sista Prop. Status&quot; visas i kolumnen jobbstatus för de tillämpliga mallarna.

   När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till på fliken [!UICONTROL Propagations], som anger antalet för varje entitetstyp som skapades, pausades eller skulle tas bort baserat på spridningen. Beräkningen inkluderar inte ändringar som gjorts i annonsnätverkets egen annonsredigerare.

## Sprid feedsfiler från listan [!UICONTROL Feeds]

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på **[!UICONTROL Feeds]** i verktygsfältet ovanför datatabellen.

1. Markera kryssrutan intill matningsfilen.

1. Ovanför datatabellen klickar du på **[!UICONTROL Propagate/Post Feed Data]** och väljer sedan något av följande alternativ:

   * **[!UICONTROL Propagate Only]:** Om du vill visa spridda data på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads]. Du kan fortfarande publicera data för alla komponenter och dess underkomponenter senare från fliken [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Om du vill skapa en kalkylbladsfil (med namnet `<feed file name>_<template name>`) som är tillgänglig i [!UICONTROL Bulksheets]-vyn för granskning (men inte på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads]). Du kan senare publicera kalkylbladsfilen från vyn [!UICONTROL Bulksheets].

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

   * **[!UICONTROL Propagate and Post to SE]:** Om du vill skapa en kalkylbladsfil (med namnet `<feed file name>_<template name>`) som står i kö för publicering i annonsnätverket. Kolumnbladsfilen är tillgänglig i vyn [!UICONTROL Bulksheets], men den är inte tillgänglig på flikarna [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] och [!UICONTROL Ads].

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format.

1. I popup-fönstret markerar du kryssrutan bredvid varje mall som du vill använda för att sprida data från feed-filen och klickar sedan på **[!UICONTROL Propagate Feed]**.

   Alla mallar som är associerade med filen visas.

Fliken [!UICONTROL Templates] öppnas och kolumnen [!UICONTROL Last Prop. Status] visar jobbstatusen för de tillämpliga mallarna.

När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till på fliken [!UICONTROL Propagations], som anger antalet för varje entitetstyp som skapades, pausades eller skulle tas bort baserat på spridningen. Beräkningen inkluderar inte ändringar som gjorts i annonsnätverkets egen annonsredigerare.

## Visa en spridningssammanfattning

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Propagations]**.

1. Klicka på ikonen ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar") bredvid mallnamnet.

## Stoppa ett spridningsjobb

Du kan stoppa ett spridningsjobb för lagerfeeddata medan jobbet fortfarande är i kö.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** på huvudmenyn, som öppnas på fliken [!UICONTROL Templates].

1. Klicka på **[!UICONTROL Cancel]** i kolumnen [!UICONTROL Last Prop. Status] bredvid mallnamnet.

>[!MORELIKETHIS]
>
>* [Om lagerfeeds](inventory-feeds-about.md)
>* [Hantera annonsmallar för lagerflöden](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Visa data som har genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Publicera kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
