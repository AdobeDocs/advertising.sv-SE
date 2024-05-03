---
title: Redigera annonsplaner för praktik
description: Lär dig hur du ändrar annonsplanerna för annonser som är kopplade till placeringar.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Redigera annonsplaner för praktik

## Redigera annonsscheman för en eller flera placeringar

Du kan ändra schemalagda flygdatum och annonsrotation för annonser som är kopplade till flera placeringar med en [!DNL Microsoft Excel] kalkylblad. Varje annons kan vara aktiv under flera flygningar.

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Markera kryssrutan bredvid varje placering vars annonsdata du vill hämta.

1. Klicka på i verktygsfältet för gruppåtgärder **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. När filen är tillgänglig klickar du på **[!UICONTROL Download]** i meddelandet längst upp på webbläsarsidan om du vill hämta en kalkylbladsfil (i XLSX-format) enligt webbläsarens normala procedur.

   ![Ladda ned meddelande om klar hämtning](/help/dsp/assets/download-ready.png "Ladda ned meddelande om klar hämtning")

1. Öppna den hämtade filen, redigera flyginformationsfälten för varje annonsrad och spara den uppdaterade filen:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (till exempel [!UICONTROL Flight 1 Start Date] och [!UICONTROL Flight 1 End Date]): flygningens första och sista datum. Använd formatet ÅÅÅ-MM-DD för varje datum. Alla annonser med tomma fält för flygdatum behandlas som annonser som inte deltar.

   * **[!UICONTROL Flight N Weight]** (till exempel [!UICONTROL Flight 1 Weight]): Så här roterar du annonserna för ett flyg. Ange ett värde:

      * Om du vill rotera annonserna för en flygning jämnt anger du `[!UICONTROL Even]`.

      * Om du vill rotera annonserna för en flygning ojämnt anger du den relativa vikt som varje annons ska roteras med, i procent (till exempel `40` för 40 %). Flygningens totala vikt skall vara lika med 100.

1. Ladda upp mallen för redigerat annonsschema:

   1. Markera kryssrutan bredvid varje lämplig placering.

   1. Klicka på i verktygsfältet för gruppåtgärder **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** och ange vilken fil som ska överföras.

## Redigera annonsschemat för en enstaka placering

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Du kan ändra schemalagda flygdatum och annonsrotation för annonserna som är kopplade till en placering. Varje annons kan vara aktiv under flera flygningar.

1. Klicka på **[!UICONTROL Campaigns]**.

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Placements]**.

1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Gör något av följande:

   * Om du vill lägga till en flygning klickar du **[!UICONTROL Add Flight]** och ange sedan startdatum och slutdatum.

   * Om du vill lägga till en befintlig flygning i en annons klickar du på **[!UICONTROL +]** i annonsraden för flygkolumnen.

   * Om du vill ta bort en befintlig flygning från en annons klickar du på **[!UICONTROL x]** i annonsraden för flygkolumnen.

      * (När flera annonser har samma plan) Om du vill rotera annonserna ojämnt klickar du på **[!UICONTROL Even Rotation]** i flyginformationen och ange sedan den relativa vikt som varje annons ska roteras med, i procent.

        Den totala vikten måste vara lika med 100.

1. Klicka på uppe till höger **[!UICONTROL Continue]**.

1. Granska flyginformationen och klicka sedan på **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Redigera placeringar](placement-edit.md)
>* [Visa ändringsloggen för en placering](placement-change-log.md)
>* [Placeringsinställningar](placement-settings.md)
