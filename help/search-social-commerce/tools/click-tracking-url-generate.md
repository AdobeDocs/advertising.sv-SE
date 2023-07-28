---
title: Generera en URL för klickspårning
description: Lär dig hur du manuellt skapar en klicknings-URL för sökning, sociala medier och handel.
exl-id: d22a472a-a562-4812-a067-fbd407cd7d00
feature: Search Tools, Search Tracking
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Generera en klicknings-URL för sökning, sociala medier och handel med verktyget för spårning av URL:er

*Annonsörer med enbart konverteringsspårning i Adobe Advertising*

Information om när du manuellt måste generera och implementera en klickspårnings-URL finns i &quot;[När och hur klickspårnings-URL:er ska genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Den här funktionen implementerar inte spårningsmallen eller mål-URL:en i det relevanta annonskontot.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Välj annonsnätverkskontot i listan.

   ([!DNL Google Ads] nyckelord; text, mobilappsinstallation och dynamiska sökannonser; placeringar; sitelinks; och produktgrupper) Spårningstaggar för spårningsmallsfältet visas. De innehåller inga tilläggsparametrar på kontonivå. Gå till steg 4.

   För alla andra typer av taggar anger du indatainformation för att generera en tagg.

1. (Vid behov) Generera en tagg:

   1. Ange landningssidorna, med sitelinks- eller produktnamn om det efterfrågas, på något av följande sätt:

      * Ange en fil som innehåller informationen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på **[!UICONTROL Browse]** för att hitta filen på enheten eller i nätverket. Filen måste vara en tabbavgränsad textfil med ett objekt per rad i följande format:

         * (Kreatörer, standardannonser) `**landing_page**`

           där `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           där `sitelink` är platshållarens namn och `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Filen kan innehålla upp till 10 000 rader.

         * ([!DNL Google Merchant Center] produktgrupper och [Microsoft® Advertising] produktannonser) `product name <tab> ** <tab> landing_page`

           där `product name` är produktnamnet och `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Filen kan innehålla upp till 10 000 rader.

      * I inmatningsfältet anger du ett objekt per rad i följande format:

         * (Kreatörer, standardannonser) `landing_page`

           där `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

           där `sitelink` är platshållarens namn och `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] produktgrupper och [!DNL Microsoft® Advertising] produktannonser) `product name**landing_page`

           där `product name` är produktnamnet och `landing_page` är en giltig URL för landningssida eller en bas-URL.

           Exempel: Acme PR208**http://www.example.com/travel.html

   1. Klicka på **[!UICONTROL Generate Tracking URLs]**.

1. (Valfritt) Kopiera URL-adresserna (med början med&quot;http&quot; eller&quot;https&quot;) från skärmen eller utdatasidan och implementera dem i söknings- eller sociala konton.

För konton med mål-URL:er anger du värdena i [!UICONTROL Base URL] fält.

För konton med slutliga URL:er anger du värdet på skärmen i lämplig [!UICONTROL Tracking Template] fält. Du måste lägga till en parameter för den slutliga URL:en efter `&url=` parameter (som `{lpurl}`). För [!DNL Yahoo! Japan Ads] konton, använd parametern `{lpurl}`. För en lista med [!DNL Google Ads] och [!DNL Microsoft® Advertising] parametrar för att ange slutliga URL:er i spårningsmallar finns i [[!DNL Google Ads] dokumentation](https://support.google.com/google-ads/answer/6305348) (se&quot;Endast spårningsmall&quot; i avsnittet&quot;Tillgängligt [!DNL ValueTrack] Parametrar&quot;) och [[!DNL Microsoft® Advertising] dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Om verktygen för att skapa och avkoda spårningstaggar](tracking-tools-about.md)
>* [När och hur klickspårnings-URL:er ska genereras](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Avkoda en klicknings-URL för sökning, sociala medier och handel](click-tracking-url-decode.md)
