---
title: Tilldela och ta bort tilldelning av kreativa paket till en slutlig nod i en upplevelse
description: Lär dig hur ni tilldelar kreatörer till varje mål i era annonsupplevelser.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Tilldela och ta bort tilldelning av kreativa paket till en slutlig nod i en upplevelse

*Upplevelser med endast mål för beslutsträd*

Du kan tilldela kreativa paket till en målnod längst ned i ett upplevelsebeslutsträd. För upplevelser som du inte har konfigurerat mål för ligger den understa nivån under&quot;Alla&quot;.

För standardannonsupplevelser kan ni bara tilldela standardpaket. För dynamiska annonsupplevelser kan ni bara tilldela dynamiska kreativa paket.

>[!NOTE]
>
>Om du inte tilldelar minst ett kreativt paket till varje slutnod kan du välja att använda standardalternativen för varje otilldelad nod när du [sparar upplevelsen](experience-create-targeting.md). Om du vill publicera en upplevelse måste du antingen tilldela paket eller använda standardkreatörerna för varje slutlig nod.

<!-- 1. [ways to get to the decision tree] -->

1. Gör något av följande:

   * (Slutliga noder utan kreatörer) Klicka på ![Lägg till](/help/creative/assets/add.png "Lägg till") under noden och välj sedan **[!UICONTROL Assign Bundles]**.

   * (Noder med befintliga kreatörer) Håll markören över den kreativa paketrutan under målnoden <!-- wording???? --> och klicka på **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Markera kryssrutan bredvid varje paket som ska tilldelas målnoden och avmarkera kryssrutan bredvid varje paket som ska tas bort.

   Endast paket av den relevanta pakettypen för upplevelsen (standard eller dynamisk) listas.

1. Klicka på **[!UICONTROL Attach to Bundles]**.

1. (Valfritt) [Anpassa URL:er för spårning för kreatörer i de tilldelade paketen](experience-tracking-urls-targeting.md).

1. (Valfritt) [Anpassa den kreativa optimeringen och schemaläggningen](experience-optimization-scheduling-targeting.md) för de tilldelade paketen.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Lägg till en målnod på den sista nivån](experience-target-node-add-final.md)
>* [Infoga en målnod mellan noder](experience-target-node-add-inner.md)
>* [Lägg till en målnod på samma nivå mellan noder](experience-target-node-add-sibling.md)
>* [Kopiera underordnade noder och kreatörer till en annan nod på samma nivå](experience-target-node-copy.md)
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
>* [Inställningar för anpassad upplevelse](experience-settings-targeting.md)
>* [Exportera och implementera en annonsupplevelsetagg för en liveupplevelse](experience-tag-export.md)
