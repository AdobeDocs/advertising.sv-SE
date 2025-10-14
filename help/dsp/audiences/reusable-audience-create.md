---
title: Skapa en återanvändbar publik
description: Lär dig hur du skapar återanvändbara målgrupper som består av målgruppssegment och andra sparade målgrupper.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Skapa en återanvändbar publik

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Ni kan spara och hantera återanvändbara målgrupper, som är grupper av målgruppssegment och till och med andra sparade målgrupper, som ni kan använda som mål eller exkluderingar för flera platser.

>[!NOTE]
>
>(Annonsörer för vilka DSP konverterar hashade e-post-ID:n till LiveRamp-rampID-segment) Första parts-RampID-segment som inte är kopplade till en aktiv, schemalagd eller pausad placering pausas. Segmentet markeras i segmentlistan som&quot;Automatiskt pausat&quot;.

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create]** ovanför datatabellen.

1. Ange en unik **[!UICONTROL Audience Name]**.

1. (Valfritt) Avmarkera alternativet till **[!UICONTROL Share with all advertisers in my account]**.

   När ni delar en publik blir målgruppen tillgänglig som mål eller exkludering för alla annonsörer på kontot. De enskilda segmenten i målgruppen är dock bara tillgängliga för användare som segmenten delas med. Om du till exempel delar en publik som innehåller Adobe Analytics-segment med en annonsörer som inte är mappade till samma [!DNL Analytics]-konto förhandsvisas inte segmentet i den målgruppen för den annonsören. Endast de segment som är tillgängliga för den annonsören förhandsgranskas i målgruppen.

1. Klicka på **[!UICONTROL Save]**.

1. Bygg målgruppen:

   >[!NOTE]
   >
   >När du skapar målgruppen uppdateras detaljerade [data om målgruppens storlek](audience-about.md) i den högra panelen

   * Så här skapar du segmentlogiken manuellt med hjälp av segment som finns på flikarna [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] och [!UICONTROL Saved Audiences] &#x200B;](audience-settings.md):

      * Om du vill lägga till det första segmentet letar du reda på segmentet i den vänstra panelen och markerar kryssrutan bredvid segmentnamnet.

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

1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Om målgruppshantering](audience-about.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Syntax för målgruppssegmentslogik](audience-segment-logic-syntax.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Skapa och implementera ett [!UICONTROL CCPA Opt-Out-of-Sale] segment &#x200B;](ccpa-opt-out-segment-create.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
