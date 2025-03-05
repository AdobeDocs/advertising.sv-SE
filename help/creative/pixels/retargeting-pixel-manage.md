---
title: Hantera återmarknadsföring av pixlar
description: Lär dig hur du skapar och implementerar återannonseringspixlar som ska användas som mål för annonsupplevelser.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Hantera återmarknadsföring av pixlar

*Stängd beta*

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Du kan skapa en omdirigerad pixel för att identifiera besökare på en annonsörs landningssidor eller konverteringssidor med användar-cookies eller universella ID:n och för att fånga upp specifika attribut som sidorna spårar för dessa besökare. Pixeln spårar den senaste händelsen som besökaren utför på sidan. När du har skapat pixeln kan du generera en pixeltagg som infogas på de relevanta webbsidorna för att börja spåra besökare.<!-- Note to self: surfer id=cookie or universal ID -->

Du kan sedan använda pixeln som mål för alla kreatörer i en annonsupplevelse för att endast visa annonser för användare med angivna attribut som tidigare besökt de webbsidor som är kopplade till pixeln. Du kan till exempel rikta in dig på besökare som tittar på röda skor i storlek 10 om webbsidorna spårar dessa attributvärden.<!-- better example? Make sure they match attribute examples below -->

Återmarknadsföringsprofiler lagras i 180 dagar.

Exempel på pixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] stöder för närvarande bara universella ID:n för Advertising DSP. En framtida release kommer att ha stöd för universella ID:n för DSP:er från tredje part.<!-- Clarify this and reword as needed -->
>* Du kan också använda dina egna målgrupper från Adobe Audience Manager och Adobe Analytics som [kreativa mål för dina upplevelser](/help/creative/experiences/experience-settings-targeting.md).
>* När du använder en upplevelse som en annons på en Advertising DSP-plats kan du rikta placeringen mot alla målgrupper som är tillgängliga för dig i DSP. Du kan också [skapa anpassade målgruppssegmenttaggar](/help/dsp/audiences/custom-segment-create.md) för att spåra alla besökare till specifika landningssidor och sedan använda dessa segment som kreativa mål för en placering.
>* Besökare på webbplatser som har valt att sluta spåra annonser för målinriktning får inte annonser med personaliserat kreativt innehåll baserat på målgruppssegment eller profiler för ny målinriktning.

## Skapa en återmarknadsföringspixel

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** på huvudmenyn.

1. Ovanför datatabellen klickar du på **[!UICONTROL Creative]** och väljer sedan > **[!UICONTROL Retargeting Pixel]**.

1. Ange pixelinställningarna [för återmarknadsföring](#retargeting-pixel-settings).

1. Klicka på **[!UICONTROL Save]**.

1. [Generera pixeltaggen ](#retargeting-pixel-generate) som ska skickas till annonsören eller webbplatskontakten.

   Den återmarknadsförande pixeltaggen måste vara den sista åtgärden på sidan.<!-- verify here and below -->

   Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

## Redigera en återmarknadsföringspixel

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** på huvudmenyn.

1. Håll markören över pixelnamnet och klicka på **[!UICONTROL Edit]**.

1. Redigera [inställningarna för omdirigering av pixlar](#retargeting-pixel-settings).

1. Klicka på **[!UICONTROL Save]**.

1. [Generera pixeltaggen ](#retargeting-pixel-generate) som ska tillhandahållas annonsören eller webbplatskontakten så att de kan ersätta den ursprungliga taggen.

   Den återskapande pixeltaggen måste vara den sista åtgärden på landningssidan.

   Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

## Generera en tagg för en omdirigerad pixel {#retargeting-pixel-generate}

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** på huvudmenyn.

1. Håll markören över pixelnamnet och klicka på **[!UICONTROL Generate Tag]**.

1. Klicka på **[!UICONTROL Copy to Clipboard]** om du vill kopiera taggen till Urklipp på datorn, där du kan klistra in texten i en fil som du vill spara.

1. I pixeltaggen anger du ett värde för varje attribut i både `<img src>`- och `<script src>`-avsnitten genom att ersätta varje `Insert <attribute>` med ett värde. Ange ett ID5-partner-ID om taggen hämtar ett universellt ID.

   Om du lägger till ytterligare attribut manuellt måste du inkludera URL-kodning.

   Om du till exempel inkluderade attributen &quot;category&quot;, &quot;color&quot;, &quot;size&quot; och &quot;capture ID5 Universal ID:n, innehåller pixeltaggen följande parametrar: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` och `&id5pid=--Insert ID5_PARTNER_ID--`. Om du till exempel vill ange användare som väljer röda sandaler i storlek 10 som mål, ändrar du parametrarna i både image-taggen och script-taggen till `&ut1=sandals&ut2=red&ut3=10` och anger även ID5-partner-ID:t i script-taggen, till exempel `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Ge annonsören eller webbplatskontakten den ifyllda pixeltaggen tillsammans med en lista över de relevanta landningssidor där den ska infogas.

   Den återskapande pixeltaggen måste vara den sista åtgärden på landningssidan.

   Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

## Ta bort en omdirigerad pixel

1. Klicka på **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** på huvudmenyn.

1. Håll markören över pixelnamnet och klicka på **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsemeddelandet.

## Återmarknadsföring av pixelinställningar {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** Namnet på pixeln. **Obs!** Pixeltaggen innehåller pixel-ID:t (`pxId=<ID>`), inte pixelnamnet.

**[!UICONTROL Advertiser]:** (skrivskyddat för befintliga pixlar) Annonsören som pixeln spåras för.

**[!UICONTROL Attribute 1]:** Ett attribut som ska inkluderas i pixeltaggen, till exempel&quot;SKU&quot;,&quot;category&quot;,&quot;size&quot; eller andra attribut för sidan eller produkten som visas på sidan. Ange ett värde för attributet i pixeltaggen innan du infogar den på de relevanta webbsidorna.

När ni riktar in annonsupplevelser mot användare som exponeras för pixeln anger målinställningarna de attributvärden som måste finnas för att visa de kreativa.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Valfritt) Ytterligare attribut som ska inkluderas i pixeltaggen. Ange ett värde för varje ytterligare attribut i pixeltaggen innan du infogar den på de relevanta webbsidorna.

När ni riktar in annonsupplevelser mot användare som exponeras för pixeln anger målinställningarna de attributvärden som måste finnas för att visa de kreativa.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (Beta-funktion; endast nya pixlar; valfritt) Typer av universella ID:n för den pixeltagg som ska spåras:

* *[!UICONTROL ID5]:* Pixeltaggen spårar [!DNL ID5] ID:n. Inga avgifter tas ut för visningar som skickas till universella ID:n.

* *[!UICONTROL Ramp ID]:* Pixeltaggen spårar [!DNL Ramp IDs]. Inga avgifter tas ut för visningar som skickas till universella ID:n.

Om du eller en annan användare på DSP-kontot ska kunna använda den här funktionen måste du acceptera villkoren i serviceavtalet för att kunna använda universella ID en gång innan du kan använda universella ID:n för en ny ID-typ. För kunder med hanterade tjänstekontrakt får ditt Adobe-kontoteam ditt samtycke och godkänner villkoren för din organisations räkning. Klicka på **[!UICONTROL Terms of Service]** om du vill läsa villkoren. Om du vill acceptera villkoren rullar du längst ned på villkoren och klickar på **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Inställningar för riktad annonsupplevelse](/help/creative/experiences/experience-settings-targeting.md)
>* [Om annonsupplevelser](/help/creative/experiences/experience-about.md)
