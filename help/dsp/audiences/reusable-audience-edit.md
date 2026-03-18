---
title: Redigera en återanvändbar målgrupp
description: Lär dig hur du redigerar en återanvändbar målgrupp.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 62d27f4af9705194f4254ffcb3145719dfd5af2f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Redigera en återanvändbar målgrupp

När du redigerar en målgrupp som används i någon placering eller annan återanvändbar målgrupp tillämpas ändringarna omedelbart på dessa placeringar och målgrupper.<!-- verify -->

>[!NOTE]
>
>(Annonsörer för vilka DSP konverterar hashade e-post-ID:n till LiveRamp-rampID-segment) Första parts-RampID-segment som inte är kopplade till en aktiv, schemalagd eller pausad placering pausas. Segmentet markeras i segmentlistan som&quot;Automatiskt pausat&quot;.

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]** på huvudmenyn.

1. Håll markören över målgruppsraden och klicka på **[!UICONTROL Edit]**.

1. Redigera målgruppsinställningarna på något av följande sätt:

   >[!NOTE]
   >
   >Om du redigerar målgruppssegmentslogiken uppdateras detaljerade [målgruppsdata](audience-about.md) i den högra panelen.

   * (Valfritt) Om du vill redigera **[!UICONTROL Audience Name]** klickar du på ![Redigera](/help/dsp/assets/edit.png) bredvid målgruppsnamnet, anger ett unikt målgruppsnamn och klickar sedan på **[!UICONTROL Apply]**.

   * (Valfritt) Om du vill redigera segmentlogiken manuellt använder du segment som finns på flikarna [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] och [!UICONTROL Saved Audiences] ](audience-settings.md) gör du följande.

      * Lägga till ett segment i en befintlig segmentgrupp:

      1. Klicka på segmentgruppen på den högra panelen.

      1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* eller *[!UICONTROL Exclude All]* efter behov.

         *[!UICONTROL Exclude All]* är inte tillgänglig för den första segmentgruppen. För en målgrupp som endast innehåller undantag skapar du den här målgruppen som *[!UICONTROL Include Any]* och sedan, inom en placering, väljer du den målgruppen på menyn Uteslutna målgrupper.

      1. Leta reda på det nya segmentet i den vänstra panelen och markera kryssrutan bredvid segmentnamnet.

         Segmentgruppen uppdateras automatiskt med det nya segmentet.

   * Så här lägger du till en ny segmentgrupp:

      1. Klicka på **[!UICONTROL + New Group]** i den högra panelen.

      1. (Valfritt) Ändra logiken mellan den föregående gruppen och den nya gruppen till *[!UICONTROL And]* eller *[!UICONTROL Or]* efter behov.

      1. Leta reda på segmenten för den nya gruppen i den vänstra panelen och markera kryssrutorna bredvid segmentnamnen.

      1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* eller *[!UICONTROL Exclude All]* efter behov.

   * Så här använder du segmentlogik från en befintlig målgrupp:

      1. Kopiera segmentlogiken från den befintliga målgruppen på något av följande sätt:

         * I vyn Alla målgrupper håller du markören över målgruppsraden och klickar sedan på **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Klicka på **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]** längst upp på segmentlogikpanelen i inställningarna för den befintliga målgruppen.

         * I en textredigerare skapar du segmentlogiken manuellt med alfanumeriska segment-ID:n och [boolesk syntax](audience-segment-logic-syntax.md) och kopierar den till Urklipp.

      1. Klicka på **[!UICONTROL paste in an audience rule to begin building]**, klistra in den befintliga segmentlogiken i indatafältet och klicka sedan på **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Om målgruppen redan innehåller någon segmentlogik skrivs den befintliga logiken över när du klistrar in den i den nya segmentlogiken.

1. Klicka på **[!UICONTROL Save]**.

1. Klicka på **[!UICONTROL Continue]** i bekräftelsemeddelandet.

>[!MORELIKETHIS]
>
>* [Om målgruppshantering](audience-about.md)
>* [Skapa en återanvändbar målgrupp](reusable-audience-create.md)
>* [Duplicera en återanvändbar publik](reusable-audience-duplicate.md)
>* [Visa information om en återanvändbar målgrupp](reusable-audience-view-details.md)
>* [Dela en återanvändbar målgrupp](reusable-audience-share.md)
>* [Exportera en återanvändbar målgrupp](reusable-audience-export.md)
>* [Kopiera segmentnyckeln för en återanvändbar publik till Urklipp](reusable-audience-clipboard.md)
>* [Ta bort en återanvändbar publik](reusable-audience-delete.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Syntax för målgruppssegmentslogik](audience-segment-logic-syntax.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
