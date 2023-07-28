---
title: Sprida lagerflödesdata via mallar
description: Lär dig mer om att sprida data från era inventeringsflöden via annonsmallar för att hantera kontostrukturen och leverera dynamiska annonser.
exl-id: 40de75e8-8440-48f4-9fa7-1aeb2ae392c5
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Sprida lagerflödesdata via mallar

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

När du har skapat en annonsspecifik feed-mall och associerat en feed-fil eller en [!DNL Google] eller [!DNL Microsoft®] säljcenterkonto med det kan du dynamiskt skapa annonser genom att sprida flödesuppgifterna via mallen enligt [inställningar för feed-data](feed-settings-manage.md). Under spridningen ersätts kolumnnamnen i mallen med datavärden i feeden, och de genererade kampanjerna och deras komponenter har standardinställningarna om inte mallen anger något annat. Beroende på mallalternativen skapar Search, Social och Commerce antingen en ny kontostruktur (kampanjer, annonsgrupper, nyckelord) för annonserna eller mappar annonserna till den befintliga kontostrukturen.

När nya feed-data innehåller nya datavärden för ett objekt, eller mallen har ändrats, tas befintliga annonser bort och nya skapas. Om den enda förändringen är [!DNL Google Ads] Param 1 och Param 2, så uppdateras bara dessa värden. Dubblerade annonser (samma annonskopia och landningssida) skapas aldrig.

När du sprider data kan du eventuellt förhandsgranska genererade data i en kampanjhierarkivy, generera en kalkylbladsfil för granskning eller generera en kalkylbladsfil för omedelbar publicering i annonsnätverket. När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till på fliken Spridningar, som anger antalet för varje entitetstyp som skapades, pausades eller skulle tas bort baserat på spridningen. Om du inte skickar data direkt kan du förhandsgranska dem och publicera dem senare.

## Sprid feed-filer från [!UICONTROL Templates] tab

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

1. Markera kryssrutan bredvid mallarna som ska spridas.

1. Klicka på i verktygsfältet **[!UICONTROL Propagate]** och välj sedan något av följande alternativ:

   * **[!UICONTROL Propagate Only]:** Visa spridda data på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar. Du kan fortfarande publicera data för en komponent och dess underkomponenter senare från [!UICONTROL Templates] -fliken.

   * **[!UICONTROL Propagate and Preview]:** Skapa en kalkylbladsfil (med namnet &quot;`<feed file name>_<template name>`&quot;), som finns i [!UICONTROL Bulksheets] visa för granskning (men inte på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] tabbar). Du kan senare publicera kalkylbladsfilen från [!UICONTROL Bulksheets] vy.

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

   * **[!UICONTROL Propagate and Post to SE]:** Skapa en kalkylbladsfil (med namnet &quot;`<feed file name>_<template name>`&quot;) som står i kö för publicering i annonsnätverket. Kolumnmallsfilen finns i [!UICONTROL Bulksheets] vyn, men den är inte tillgänglig på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar.

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format.

   &quot;Sista Prop. Status&quot; visas i kolumnen jobbstatus för de tillämpliga mallarna.

   När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till i [!UICONTROL Propagations] som anger antalet entitetstyper som skapades, pausades eller togs bort baserat på spridningen. Beräkningen inkluderar inte ändringar som gjorts i annonsnätverkets egen annonsredigerare.

## Sprid feed-filer från [!UICONTROL Feeds] list

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Feeds]**.

1. Markera kryssrutan intill matningsfilen.

1. Ovanför datatabellen klickar du **[!UICONTROL Propagate/Post Feed Data]** och välj sedan något av följande alternativ:

   * **[!UICONTROL Propagate Only]:** Visa spridda data på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar. Du kan fortfarande publicera data för en komponent och dess underkomponenter senare från [!UICONTROL Templates] -fliken.

   * **[!UICONTROL Propagate and Preview]:** Skapa en kalkylbladsfil (med namnet &quot;`<feed file name>_<template name>`&quot;), som finns i [!UICONTROL Bulksheets] visa för granskning (men inte på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] tabbar). Du kan senare publicera kalkylbladsfilen från [!UICONTROL Bulksheets] vy.

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format. Du behöver inte packa upp filen för att publicera den.

   * **[!UICONTROL Propagate and Post to SE]:** Skapa en kalkylbladsfil (med namnet &quot;`<feed file name>_<template name>`&quot;) som står i kö för publicering i annonsnätverket. Kolumnmallsfilen finns i [!UICONTROL Bulksheets] vyn, men den är inte tillgänglig på [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]och [!UICONTROL Ads] -tabbar.

     När den resulterande kalkylbladsfilen är större än 2 MB är filen i ZIP-format.

1. I popup-fönstret markerar du kryssrutan bredvid varje mall som du vill använda för att sprida data från feed-filen. Klicka sedan på **[!UICONTROL Propagate Feed]**.

   Alla mallar som är associerade med filen visas.

The [!UICONTROL Templates] öppnas och &quot;[!UICONTROL Last Prop. Status]&quot;kolumn visar jobbstatus för tillämpliga mallar.

När varje spridningsåtgärd har slutförts läggs en spridningssammanfattning till i [!UICONTROL Propagations] som anger antalet entitetstyper som skapades, pausades eller togs bort baserat på spridningen. Beräkningen inkluderar inte ändringar som gjorts i annonsnätverkets egen annonsredigerare.

## Visa en spridningssammanfattning

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicka på **[!UICONTROL Propagations]** -fliken.

1. Klicka på bredvid mallnamnet ![Ikon för Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Ikon för Visa/redigera inställningar") .

## Stoppa ett spridningsjobb

Du kan stoppa ett spridningsjobb för lagerfeeddata medan jobbet fortfarande är i kö.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

1. I dialogrutan[!UICONTROL Last Prop. Status]kolumnen bredvid mallnamnet klickar du på **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Om lagerflöden](inventory-feeds-about.md)
>* [Hantera annonsmallar för lagerflöden](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Visa data som genererats från feeds](propagated-data-view.md)
>* [Redigera data som genererats från feeds](propagated-data-edit.md)
>* [Posta kampanjdata som genererats från feeds till annonsnätverk](propagated-data-post.md)
>* [Stoppa ett bokföringsjobb för lagerfeed-data](stop-job.md)
>* [Status för data som genererats från feeds](propagated-data-status.md)
