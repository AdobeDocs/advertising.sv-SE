---
title: Redigera standardkreatörer i ett kreativt bibliotek
description: Lär dig hur du ändrar inställningarna för vanliga (icke-dynamiska) kreatörer i ett kreativt bibliotek.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Redigera standardkreatörer i ett kreativt bibliotek

*Stängd beta*

Du kan redigera vissa inställningar för varje typ av standardprogram. Du kan endast redigera flera användare av <!-- or creative variations --> av samma typ (enkel HTML5 med endast en landningssida, statisk HTML5 med flera landningssidor, flexibel HTML5, bild eller tredje part <!-- , or dynamic -->).

För flexibla användare av HTML5 och statiska HTML 5 kan du överföra en ny mallfil med en annan layout men med samma uppsättning attributnamn. För användare som har HTML 5 kan du redigera alla attribut eller lägga till bilder genom att ladda upp en ny mall med de nya attributen eller bilderna. I samtliga fall måste mallen vara en lokal fil i ZIP-format med högst 2 MB.

När du redigerar en <!-- or creative variation --> som ingår i ett paket tillämpas dina ändringar automatiskt på alla upplevelser som innehåller paketet, förutom att eventuella anpassade landningssidor och URL:er för spårning som anges på upplevelsenivån fortfarande gäller för det paket som är kopplat till den upplevelsen.

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** på huvudmenyn.

1. (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika bibliotek.

1. Klicka på biblioteksnamnet.

1. På fliken **[!UICONTROL Creatives]** > **[!UICONTROL Standard Ads]** väljer du kreatörer:

   * (Valfritt) [Anpassa vyn](/help/creative/introduction/customize-data-views.md) så att den innehåller specifika kreatörer.

   * Så här redigerar du en enskild kreatör:

      * I kortvyn klickar du på **[!UICONTROL ...]** bredvid det kreativa namnet och sedan på **[!UICONTROL Edit]**.

      * Håll markören över raden i tabellvyn och klicka på **[!UICONTROL Edit]**.

   * Om du vill redigera en eller flera kreatörer markerar du kryssrutan för varje kreatör som du vill redigera. Klicka på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

     Om du vill markera alla rader markerar du den globala kryssrutan i det övre vänstra hörnet.

1. Redigera de [bildkreativa inställningarna](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image), [HTML5-kreativa inställningarna](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5), [flexibla HTML5-kreativa inställningar](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) eller [inställningar från tredje part](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party). <!-- , or [dynamic creative settings](/help/creative/creative-libraries/creative-settings-dynamic.md) -->

   När du redigerar flera kreatörer samtidigt:

   * Du kan redigera inställningarna för varje kreatör samtidigt eller individuellt. Som standard markeras alla alternativ som du väljer, och alla inställningar som du anger gäller för alla valda kreatörer. Om du vill redigera inställningar för specifika kreatörer avmarkerar du alla ej tillämpliga kreativa innan du redigerar fälten. Upprepa för ytterligare kreatörer om det behövs.

   * Vissa inställningar används för alla valda kreatörer.

   >[!NOTE]
   >
   >* (Endast flexibla HTML5-kreatörer) Du kan bara redigera attribut för enskilda användare.<!-- Also, when you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed. -->

<!-- Not there as of 1/16/25. If we do add it, verify the applicable ad types:   
1. (Flexible HTML5 [or third-party should be possible, but not so] creatives; optional) Once you've made your changes, click ![]() to preview the new creative. 
-->

1. Klicka på **Spara**.

<!-- Not there as of 1/16/25. If we do add it, add back in:
1. (Flexible HTML5 or third-party creatives; optional) Regenerate the thumbnail within the table view or cards view if the change isn't visible immediately.
-->

>[!MORELIKETHIS]
>
>* [Lägg till standardkreatörer i ett kreativt bibliotek](creative-add-standard.md)
>* [Standardinställningar för kreativitet](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Förhandsgranska en kreativ](/help/creative/creative-libraries/creative-preview.md)
>* [Duplicera kreatörer](/help/creative/creative-libraries/creative-duplicate.md)
>* [Ta bort kreatörer](/help/creative/creative-libraries/creative-delete.md)
