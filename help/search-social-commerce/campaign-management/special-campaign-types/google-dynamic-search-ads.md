---
title: Implementera [!DNL Google Ads] dynamiska sökannonser
description: Läs mer om arbetsflödet för konfiguration [!DNL Google Ads] dynamiska sökannonser.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementera [!DNL Google Ads] dynamiska sökannonser

*[!DNL Google Ads]sökbara kampanjer med enbart nyckelords- eller nyckelordsspårning och endast på kreativ nivå*

Dynamiska sökannonser använder innehåll från er webbplats, i stället för nyckelord, för att bestämma när era annonser ska visas. Du kan definiera de sidor på dina webbplatser vars innehåll används för att rikta in dina dynamiska sökannonser genom att antingen ställa in separata dynamiska sökmål för annonsgruppen eller välja en inställning på kampanjnivå för att rikta annonserna med webbplatsens innehåll.

Du kan konfigurera dynamiska sökannonser antingen individuellt eller med hjälp av kalkylblad. Följande instruktioner innehåller länkar till hur du skapar enskilda enheter.

## Steg som ska konfigureras [!DNL Google Ads] dynamiska sökannonser

1. [Skapa en kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för dynamiska sökannonser:

   1. Ställ initialt in kampanjbudgeten på 10 % av era dagliga utgifter för sökkampanjer.

      Du kan öka budgeten senare när annonserna har visat sig vara värdefulla.

   1. (Om du vill [!DNL Google Ads] för att visa dina dynamiska sökannonser baserat på innehållet på din webbplats) Ange rotdomänen och språket för domänen i [!UICONTROL DSA Options] i kampanjinställningarna.

      >[!NOTE]
      >
      >Din domän måste indexeras av [!DNL Google Ads] organiskt sökindex som ska anges som mål. Om domänen innehåller sidor på flera språk och du vill ha alla som mål, skapar du en separat kampanj för varje språk.

      Om du inte använder din webbplatsdomän som mål för dina annonser skapar du dynamiska sökmål (se steg 4) för varje annonsgrupp. Du kan skapa målen [individuellt](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) eller använda [bulkark](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Se till att kampanjen riktas mot sökkanalen och endast mot [!DNL Google Ads] söknätverk (inte visningsnätverk). De här inställningarna är tillgängliga i [!UICONTROL Networks and Devices] -fliken.

   1. (Valfritt) Uteslut nyckelord på [!UICONTROL Negatives] -fliken.

   1. (Valfritt) Konfigurera en spårningsmall på kampanjnivå som åsidosätter spårningsmallen på kontonivå men kan åsidosättas på lägre nivåer.

      (Annonsörer med Adobe Analytics utan spårning på serversidan) Om du vill ta med spårning för omvänd feed från Search, Social och Commerce till Analytics, lägger du till spårningskoden s_kwcid i tilläggsparametrarna på kontonivå, som lägger till koden i den slutliga URL:en. Se &quot;[s_kwcid tracking-parametern](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Skapa en annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) i kampanjen, inklusive följande steg:

   1. Ange [!UICONTROL Ad Group Type] till **[!UICONTROL Search Dynamic].**

   1. Ange standardbud för alla annonser.

      Du kan åsidosätta standarderbjudandet för enskilda dynamiska sökmål om du konfigurerar dem.

   1. (Valfritt) Konfigurera en spårningsmall på annonsgruppsnivå, som åsidosätter spårningsmallar på högre nivåer men som kan åsidosättas på annonsnivå.

      Om du har lagt till Adobe Analytics tracking på kampanjnivå och vill inkludera det för annonsgruppen lägger du till det här. Se steg 1e.

1. [Skapa varje dynamisk sökannons](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) inom annonsgruppen.

   [!DNL Google Ads] genererar dynamiskt rubriken, URL:en för visning och landningssidans URL för varje annons. Du kan lägga till omdirigeringar och spårning till spårningsmallen på annonsnivå, som åsidosätter spårningsmallar på högre nivåer.
Om du vill åsidosätta Adobe Analytics-spårning på högre nivåer med spårning på annonsnivå lägger du till den här. Se steg 1e och 2c.

1. (Obligatoriskt om du inte inkluderar rotdomänen och språket för domänen i DSA-alternativavsnittet i kampanjinställningarna. Annars kan du skapa) [dynamiska sökmål](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) för annonsgruppen. Du kan också åsidosätta annonsgruppsnivåerbjudandet med anbud på målnivå.

   Målen definierar om annonsnätverket använder alla eller en del av sidorna på webbplatsen för att rikta in sig på era dynamiska sökannonser. För att få bästa möjliga resultat bör du konfigurera kampanjen med en annonsgrupp per dynamiskt sökmål och inkludera en annonsgrupp som uppfyller alla villkor.

1. Vid behov [redigera kampanjinställningarna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) för att justera kampanjbudgeten och förfina trafiken genom att utesluta ytterligare nyckelord från kampanjen.
