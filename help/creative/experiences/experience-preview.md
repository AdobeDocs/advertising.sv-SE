---
title: Förhandsgranska en upplevelse
description: Lär dig förhandsgranska kreatörerna i en annonsupplevelse.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: ae226015d1a8a3da4ea2a0db0db31858e750b9a7
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Förhandsgranska en upplevelse

*Stängd beta*

Du kan förhandsgranska de som skapar en viss annonsstorlek och se resultatet för dem, inklusive alla hyperlänkar. För upplevelser med målgruppsanpassning i beslutsträd kan du förhandsgranska en enskild kreatör, kreatörerna för en viss gren (måltyp) eller alla kreatörer i upplevelsen. För upplevelser som saknar beslutsträdsanpassning kan ni förhandsgranska en enda kreativ. <!-- verify -->

* När du förhandsgranskar alla kreatörer för upplevelsen eller en viss gren visas alla relevanta kreatörer.

* När du förhandsgranskar en enskild kreatör och flera kreatörer passar kriterierna, baseras den kreativa du ser varje gång du uppdaterar förhandsgranskningen på annonsrotationsinställningarna för upplevelsen:

   * För algoritmisk annonsrotation väljs det kreativa alternativet baserat på optimeringsmålet.

   * För viktad annonsrotation väljs den kreativa delen baserat på den angivna vikten (t.ex. en 80-procentig chans att Creative A visas och en 20-procentig chans att Creative B visas) varje gång.

   * För schemalagd annonsrotation visas den första kreativiteten i schemat. Du kan fortsätta att uppdatera förhandsgranskningen om du vill fortsätta genom sekvensen.<!-- Refresh isn't there as of 2/3 -->

## Förgranska kreatörer i en upplevelse med målgruppsanpassning i beslutsträd

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika upplevelser.

1. Gör något av följande:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Preview]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Preview]**.

1. Välj vilka kreatörer som ska förhandsgranskas:

   * Så här förhandsgranskar du en enskild kreatör:

      1. Klicka på **[!UICONTROL Creative]**.

      1. Välj annonsstorlek.

      1. Välj det kreativa målet i avsnittet [!UICONTROL Decision Tree Targeting].

   * Så här förhandsgranskar du kreatörerna för en viss gren:

      1. Klicka på **[!UICONTROL Particular branch]**.

      1. Välj annonsstorlek.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Välj det kreativa målet.

   * Klicka på **[!UICONTROL Entire Tree]** om du vill förhandsgranska alla kreativa i upplevelsen.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Valfritt) Om du vill inkludera namnet på den kreativa personen, typ och storlek, landningssidans URL eller klicka på URL:er och flexibla attribut under varje kreativ del väljer du **[!UICONTROL Display Creative Metadata]**.

1. Klicka på **[!UICONTROL Preview]**.

1. (Förhandsgranska endast av den kreativa avdelningen; valfritt) Klicka på **[!UICONTROL Refresh]** i verktygsfältet om du vill förhandsgranska alla andra kreatörer som kan visas enligt inställningarna för annonsrotation.<!-- I don't see this as of 2/3 -->

1. (Valfritt) Om du vill kopiera en demo-URL för upplevelsen som ska delas med andra personer utan inloggning till [!DNL Creative]:

   1. Klicka på ![Dela](/help/creative/assets/share.png "Dela") i det övre högra hörnet av förhandsgranskningen.

   1. I dialogrutan [!UICONTROL Share Demo URL] klickar du på **[!UICONTROL Copy]** för att kopiera URL:en till Urklipp så att du kan dela den med någon annan.

## Förgranska kreatörer i en upplevelse utan målgruppsanpassning i beslutsträd

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika upplevelser.

1. Gör något av följande:

   * I kortvyn klickar du på **[!UICONTROL ...]** bredvid upplevelsenamnet och sedan på **[!UICONTROL Preview]**.

   * Håll markören över raden i tabellvyn, klicka på **[!UICONTROL More]** och klicka sedan på **[!UICONTROL Preview]**.

1. (Valfritt) Begränsa listan med kreatörer genom att välja en viss kreativ storlek.

   Som standard listas alla kreatörer i alla storlekar.

1. Klicka på namnet på en annonstagg för att expandera raden och förhandsgranska de kreativa.

1. (Valfritt) Om du vill gå till landningssidan för en kreatör klickar du på den kreativa sidan.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Valfritt) Om du vill kopiera en demo-URL för upplevelsen som ska delas med andra personer utan inloggning till [!DNL Creative]:

   1. Klicka på ![Dela](/help/creative/assets/share.png "Dela") i det övre högra hörnet av förhandsgranskningen.

   1. I dialogrutan [!UICONTROL Share Demo URL] klickar du på **[!UICONTROL Copy]** för att kopiera URL:en till Urklipp så att du kan dela den med någon annan.

>[!MORELIKETHIS]
>
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Skapa en upplevelse utan mål för beslutsträd](/help/creative/experiences/experience-create-no-targeting.md)
