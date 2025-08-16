---
title: Exportera och implementera en tagg för annonsupplevelser
description: Lär dig hur du exporterar en annonsupplevelsetagg och överför den till en Advertising DSP-kampanj.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# Exportera och implementera en tagg för annonsupplevelser

När en annonstagg för en viss kreativ storlek eller videouppspelning är tillgänglig för en [live](experience-about.md#experience-statuses) -upplevelse, kan du generera och kopiera taggen i JavaScript-, iframe- och videoformat för implementering i Advertising DSP eller andra DSP:er. Taggarna för DSP innehåller alla makron som krävs för DSP.

Annonsörer med Advertising DSP kan ladda upp taggar direkt till en Advertising DSP-kampanj som annonser med annonstypen&quot;standardvisning&quot; eller&quot;universell video&quot;.

>[!NOTE]
>
>* När du skapar en upplevelse med mål för beslutsträd skapar [!DNL Creative] automatiskt en annonstagg för varje tillämplig kreativ storlek (icke-videoredigerare) eller videouppspelning (videokreatörer).
>* När du skapar en upplevelse utan mål för beslutsträd måste du [manuellt skapa en annonstagg](experience-tag-create-manually.md) för varje tillämplig kreativ storlek (andra än videokreatörer) eller videouppspelning (videokreatörer).
>* Upplevelsetaggar är dynamiska. Du behöver inte uppdatera taggarna om du redigerar en upplevelse.
>* Se till att de kampanjer ni använder för att implementera en annonsupplevelse omfattar målgruppsanpassning som är kompatibel med upplevelsen. Hierarkisk målinriktning kan variera beroende på DSP. I Advertising DSP tillämpas målgruppsanpassning på annonsnivå ovanpå (inte i stället för) målgruppsanpassning på placeringsnivå.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. Gör något av följande:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Tag Manager]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Tag Manager]**.

1. Håll markören över raden för den tillämpliga annonstaggen och klicka på ![Exportera annonstaggar](/help/creative/assets/export.png "Exportera annonstaggar") **[!UICONTROL Export ad tags]** eller **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Om det gäller standardvideoreklamupplevelser väntar du tills kolumnen [!UICONTROL Tag Status] visar [!UICONTROL Ready], vilket anger att alla videoklipp i upplevelsen har konverterats. Alla videokreatörer omkodas automatiskt av DSP, men du kan också [använda omkodning för en annan DSP](experience-tag-video-transcoding.md) för alla taggar för videoannonsupplevelser.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Valfritt) På fliken [!UICONTROL Macros] anger du upp till fem anpassade makron som ska ingå i taggen. För varje makro som ska inkluderas:

   1. Markera en kryssruta.<!-- Explain more -->

   1. Ange det anpassade makrot.<!-- Explain more -->

1. Klicka på **[!UICONTROL Next]** i det övre högra hörnet eller klicka på **[!UICONTROL Generate ad tags]** i den vänstra menyn.

1. Välj taggtyp:

   * (Inte videoupplevelser) ** *JavaScript* ** eller ** *Iframe* **.

   * (Videoupplevelser) ** *Video* **.

1. Välj var du vill skapa annonser för upplevelsen i listan [!UICONTROL Destinations].

   * *Allmänt:* För annonser som du skapar i andra DSP:er. **Obs!** Du kan behöva inkludera [ytterligare makron](/help/creative/creative-macros.md) manuellt om det behövs.

   * *Adobe AdCloud:* För annonser som du skapar i Advertising DSP.

   * *Google CM360:* För annonser som du skapar i [!DNL Google Campaign Manager 360]. **Obs!** Du kan behöva inkludera [ytterligare makron](/help/creative/creative-macros.md) manuellt om det behövs.

1. Klicka på **[!UICONTROL Generate tags]**.

1. Kopiera eller hämta taggarna:

   * Om du vill kopiera en tagg för en annonsstorlek (annonser som inte är videoannonser) eller varaktighet (videoannonser) expanderar du taggraden, håller markören över raden och klickar sedan på ![Kopiera](/help/creative/assets/copy.png "Kopiera") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Om du vill hämta alla genererade taggar som en fil till webbläsarens standardhämtningsplats klickar du på ![Hämta taggar](/help/creative/assets/download.png "Hämta taggar").

   Du kan öppna filen i en textredigerare och kopiera varje tagg. För JavaScript-taggar omges taggen av `<script></script>`- och `<noscript></noscript>`-taggar. För iframe-taggar omges taggen av `<iframe></iframe>` taggar.

1. Implementera taggarna för relevanta DSP:

   * För andra DSP:er än Advertising DSP ska du ange de taggar som ska användas för att skapa annonserna i DSP.

   * För Advertising DSP:

      1. Klicka på **[!UICONTROL Next]** i det övre högra hörnet eller klicka på **[!UICONTROL DSP link]** i den vänstra menyn.

      1. Välj den kampanj som du vill överföra annonstaggen till.

      1. Klicka på **[!UICONTROL Assign Tags]**.

         DSP öppnar vyn [!UICONTROL Ads] för den valda kampanjen.

      1. Granska annonstaggarna i vyn [!UICONTROL Create ads], markera varje tagg som du vill skapa en annons för och klicka sedan på **[!UICONTROL Create]**.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Skapa en annonstagg manuellt för en tillämplig kreativ storlek](experience-tag-create-manually.md)
>* [Tilldela kreatörer till en annonstagg för upplevelser utan målinriktning](experience-tag-assign-creatives.md)
>* [Byt namn på en annonstagg](experience-tag-rename.md)
>* [Anpassa omkodningsalternativ för en videoannons ](experience-tag-video-transcoding.md)
