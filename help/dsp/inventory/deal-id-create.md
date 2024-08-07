---
title: Skapa information om avtal-ID manuellt
description: Lär dig hur du manuellt anger information för ett avtal-ID.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Skapa information om avtal-ID manuellt

1. På huvudmenyn klickar du på **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]** och väljer sedan **[!UICONTROL Deal ID]**.

1. Ange [avtalsinställningarna](deal-id-settings.md):

   1. I avsnittet [!UICONTROL Deal ID basics] anger du avtalsinformation och vilka annonsörer som har åtkomst till erbjudandet. För garanterade erbjudanden måste du även ange planerade flygdatum och det uppskattade antalet avtryck, endast i spårningssyfte.

      Du kan spåra placeringen av garanterade erbjudanden genom att ta med kolumnen&quot;PG Impression Pacing&quot; i vyn Inventory > Deals.

   1. (Endast administratörsanvändare; valfritt) I avsnittet [!UICONTROL Technical] redigerar du standardinställningarna efter behov.

   1. Klicka på **[!UICONTROL Save]**.

1. (Garanterade erbjudanden) Välj annonser som ska användas för erbjudandet (eller 1 x 1 pixel för annonser som hanteras av utgivaren) och skapa en standardplacering med garanterad programmatisk annonsering (PG).

   Standardplaceringar av PG-paket ser till att ditt avtal alltid returnerar ett bud för varje anbudsförfrågan. Om du inte skapar en standardplacering i PG-format lägger inte eventuella placeringar som är avsedda för erbjudandet anbud om de inte är rätt konfigurerade. Du bör alltid skapa en standardplacering för PG. I vyn [!UICONTROL Placements] har standardplaceringar av PG-filer kolumnvärdet [!UICONTROL Sub-type] [!UICONTROL PG Default].

   Du kan också använda erbjudandet som ett lagermål i ytterligare placeringar, men du måste konfigurera dem på rätt sätt för att placera offerter.

   1. I inställningarna för [!UICONTROL Ad & Campaign Selection] väljer du de annonser som ska användas för erbjudandet:

      1. Välj annonsören, kampanjen och annonstypen. Du kan också välja en annonsstatus att filtrera annonserna med.

      1. I listan med tillgängliga annonser markerar du kryssrutan bredvid varje annons som ska användas för erbjudandet.

         För varje annons som hanteras av utgivaren tillämpas en spårningspixel på 1x1 automatiskt när en annonsörer och kampanj har valts.

      1. Klicka på **[!UICONTROL Apply]**.

   1. På skärmen för placeringsinställningar:

      1. Ange placeringsnamnet.

      1. (Valfritt) Redigera [placeringsinställningarna](/help/dsp/campaign-management/placements/placement-settings.md), inklusive att skriva över standarderbjudandet, som automatiskt fylls med CPM-värdet från avtalet, ändra datumintervallet eller bifoga fler annonser.

      Avtalen anges automatiskt i avsnittet Inventeringsmål. Alla andra målinriktningsalternativ är inte tillämpliga.

      1. Klicka på **[!UICONTROL Create placement]**.

När du har skapat avtalet kan du använda det som ett lagermål för flera placeringar.

>[!NOTE]
>
> Du behöver inte skicka avtalstaggen till utgivaren för verifiering.

>[!TIP]
>
>* I [!UICONTROL Inventory] > [!UICONTROL Deals]-vyn visar kolumnen [!UICONTROL Pacing & Budget] hur erbjudandet matchar det angivna flygdatumet och det angivna visningsmålet.
>
>* Om leveransen är under- eller överbelagd kontaktar du utgivaren för att justera hur mycket av volymen den skickar genom erbjudandet.

>[!MORELIKETHIS]
>
>* [Inställningar för manuellt avtal-ID](deal-id-settings.md)
>* [Konfigurera ett garanterat programavtal](programmatic-guaranteed-set-up.md)
>* [Skicka in en annons för en programmatisk garanterad transaktion med [!DNL FreeWheel]](freewheel-submit.md)
>* [Om programmatiska garanterade erbjudanden](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
