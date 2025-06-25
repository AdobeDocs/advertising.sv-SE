---
title: Generera en URL för klickspårning
description: Lär dig hur du manuellt skapar en klicknings-URL för sökning, sociala medier och Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Generera en sök-, social- och Commerce klickspårnings-URL med verktyget för spårning av URL:er

*Annonsörer med endast Adobe Advertising-konverteringsspårning*

Mer information om när du måste generera och implementera en klickspårnings-URL manuellt finns i &quot;[När och hur klickspårnings-URL:er](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) ska genereras.&quot;

>[!NOTE]
>
>Den här funktionen implementerar inte spårningsmallen eller mål-URL:en i det relevanta annonskontot.

1. Klicka på **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]** på huvudmenyn.

1. Välj annonsnätverkskontot i listan.

   ([!DNL Google Ads] nyckelord; text, mobilappsinstallation och dynamiska sökannonser; placeringar; sitelinks; och produktgrupper) Spårningstaggar för spårningsmallsfältet visas. De innehåller inga tilläggsparametrar på kontonivå. Gå till steg 4.

   För alla andra typer av taggar anger du indatainformation för att generera en tagg.

1. (Vid behov) Generera en tagg:

   1. Ange landningssidorna, med sitelinks- eller produktnamn om det efterfrågas, på något av följande sätt:

      * Ange en fil som innehåller informationen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på **[!UICONTROL Browse]** för att leta reda på filen på enheten eller i nätverket. Filen måste vara en tabbavgränsad textfil med ett objekt per rad i följande format:

         * (Kreatörer, standardannonser) `**landing_page**`

           där `landing_page` är en giltig URL eller bas-URL för landningssidan.

           Exempel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           där `sitelink` är platslänkens namn och `landing_page` är en giltig URL för landningssidan eller en bas-URL.

           Exempel: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Filen kan innehålla upp till 10 000 rader.

         * ([!DNL Google Merchant Center] produktgrupper och [!DNL Microsoft Advertising] produktannonser) `product name <tab> ** <tab> landing_page`

           där `product name` är produktnamnet och `landing_page` är en giltig URL eller bas-URL för landningssidan.

           Exempel: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Filen kan innehålla upp till 10 000 rader.

      * I inmatningsfältet anger du ett objekt per rad i följande format:

         * (Kreatörer, standardannonser) `landing_page`

           där `landing_page` är en giltig URL eller bas-URL för landningssidan.

           Exempel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink**landing_page`

           där `sitelink` är platslänkens namn och `landing_page` är en giltig URL för landningssidan eller en bas-URL.

           Exempel: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] produktgrupper och [!DNL Microsoft Advertising] produktannonser) `product name**landing_page`

           där `product name` är produktnamnet och `landing_page` är en giltig URL eller bas-URL för landningssidan.

           Exempel: Acme PR208**http://www.example.com/travel.html

   1. Klicka på **[!UICONTROL Generate Tracking URLs]**.

1. (Valfritt) Kopiera URL-adresserna (med början med&quot;http&quot; eller&quot;https&quot;) från skärmen eller utdatasidan och implementera dem i söknings- eller sociala konton.

För konton med mål-URL:er anger du värdena i rätt [!UICONTROL Base URL]-fält.

För konton med slutliga URL:er anger du värdet på skärmen i lämpligt [!UICONTROL Tracking Template]-fält. Du måste lägga till en parameter för den sista URL:en efter parametern `&url=` (till exempel `{lpurl}`). Använd parametern `{lpurl}` för [!DNL Yahoo! Japan Ads]-konton. En lista över [!DNL Google Ads]- och [!DNL Microsoft Advertising]-parametrar som anger de slutliga URL:erna i spårningsmallar finns i [[!DNL Google Ads]  dokumentationen ](https://support.google.com/google-ads/answer/6305348) (se parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängliga [!DNL ValueTrack] parametrar&quot;) och i [[!DNL Microsoft Advertising] dokumentationen](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Om verktygen för att skapa och avkoda spårningstaggar](tracking-tools-about.md)
>* [När och hur klickspårnings-URL:er genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Avkoda en klicknings-URL för sökning, sociala medier och Commerce](click-tracking-url-decode.md)
