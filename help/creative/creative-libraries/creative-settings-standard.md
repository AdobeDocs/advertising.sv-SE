---
title: Kreativa inställningar
description: Läs mer om xxxx.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1830'
ht-degree: 0%

---

# Kreativa inställningar

*Stängd beta*

Inställningarna varierar beroende på kreativ typ.

När du redigerar flera kreatörer samtidigt:

* Du kan redigera inställningarna för varje kreatör samtidigt eller individuellt. Som standard markeras alla alternativ som du väljer, och alla inställningar som du anger gäller för alla valda kreatörer. Om du vill redigera inställningar för specifika kreatörer avmarkerar du alla ej tillämpliga kreativa innan du redigerar fälten. Upprepa för ytterligare kreatörer om det behövs.

* Vissa inställningar används för alla valda kreatörer.

## Flexibla kreativa inställningar för HTML5 {#creative-settings-flexible-html5}

### Fliken Detaljer

**Kreativt namn:** Namnet på den kreativa. Mallnamnet eller namnet på den överförda filen används som standard, men du kan ändra namnet. För flera kreatörer kan du redigera de enskilda namnen. **Tips!** Inkludera annonsstorleken i det kreativa namnet och använd ett namn som är enkelt att hitta när du tar med den kreativa delen i en upplevelse.

**Språk:** Standardspråket för varje annons som du associerar med kreatörerna. När du överför eller redigerar flera användare används samma värde på alla valda kreatörer.

**Kreativ storlek:** (skrivskyddat för befintliga kreatörer) Den kreativa personens dimensioner. Om några bilder som ingår i den kreativa filen är större än den angivna storleken ändras storleken på dem.

**[!UICONTROL Click Tags]:** Variablerna som tillåter klickspårning omdirigeras från de inkluderade bannerannonserna. Variabelnamnen och motsvarande URL:er för landningssidan fylls i från den överförda kreativa enheten, men du kan ändra standardwebbadresserna. För flera kreatörer kan du redigera de enskilda klicktaggarna.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Etikett:** (Valfritt) Etiketter som ska användas för alla valda kreatörer. Du kan filtrera kreatörer efter etikett i olika vyer i [!DNL Creative].

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas för kreatörerna öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

### Fliken Attribut

**\[Alla standardattribut för innehåll som gäller för den kreativa\]:** Standardattributnamnen och -värdena fylls i från den flexibla kreativa enheten, men du kan ändra värdena om du vill.

>[!NOTE]
>
>Du kan också ersätta standardvärdet för alla kreativa attribut med ett anpassat värde när du inkluderar den kreativa delen i en upplevelse. När du redigerar attributen i en upplevelse skapas en variant av den överordnade kreativiteten.

Mer information om tillgängliga attribut i fördefinierade mallar finns i [Tillgängliga flexibla kreativa mallar](#flexible-creative-templates-available).

### Fliken Mallar

*Endast befintliga kreatörer*

Den flexibla HTML5-mallfilen för kreatörer.

Du kan också ersätta den befintliga mallen med en ny mall som har en annan layout men samma uppsättning attributnamn som den ursprungliga mallen. Den nya mallen måste vara i ZIP-format med högst 2 MB. När den kreativa delen finns i ett paket kommer alla upplevelser som använder paketet att använda layouten från den nya mallen.

När du uppdaterar mallen för en överordnad kreatör med underordnade varianter uppdateras variationerna med ändringar i mallayouten, men attributvärdena för variationen ändras inte.

Ersätta den befintliga annonsmallen:

1. Klicka på **Uppdatera mall**.

1. Klicka på **Fortsätt**.

1. Ange en ZIP-fil på något av följande sätt:

   * Dra och släpp en fil på enheten eller nätverket i rutan.

   * Klicka på **[!UICONTROL select a file]** för att leta upp filen på enheten eller i nätverket.

   Se de [flexibla annonsspecifikationerna](#flexible-ad-spec).

1. Redigera de nya [flexibla HTML-annonsinställningarna](#flexible-ad-settings) efter behov.

1. Klicka på **[!UICONTROL Edit]**

## HTML5 kreativa inställningar {#creative-settings-html5}

## Fliken Detaljer

För nya kreatörer finns följande inställningar inte på en namngiven flik.

**Kreativt namn:** Namnet på den kreativa. För en ny kreatör används filnamnet som standard, men du kan ändra namnet. För flera kreatörer kan du redigera de enskilda namnen. **Tips!** Inkludera annonsstorleken i det kreativa namnet och använd ett namn som är enkelt att hitta när du tar med den kreativa delen i en upplevelse.

**Språk:** Standardspråket för varje annons som du associerar med kreatörerna. När du överför eller redigerar flera användare används samma värde på alla valda kreatörer.

**Kreativ storlek:** (skrivskyddat för befintliga kreatörer) Den kreativa personens dimensioner. Om några bilder som ingår i den kreativa filen är större än den angivna storleken ändras storleken på dem.

**[!UICONTROL Click Tags]:** (Endast statiska HTML5-kreatörer) Variablerna som tillåter klickspårning omdirigeras från de inkluderade bannerannonserna. Variabelnamnen och motsvarande URL:er för landningssidan fylls i från den överförda kreativa enheten, men du kan ändra standardwebbadresserna. För flera kreatörer kan du redigera de enskilda klicktaggarna.

>[!NOTE]
>
>När du inkluderar den kreativa delen i en upplevelse kan du ersätta standardvärdet för någon av click-taggarna med en anpassad URL för landningssidan för att generera en härledning av den kreativa grundbilden.

**URL för landningssida:** (enkel HTML 5-användare med endast en landningssida) URL:en för standardlandningssidan för varje annons som du associerar med kreatörerna. Det måste vara en giltig URL som börjar med http:// eller https://. Den kan innehålla spårningsparametrar från tredje part eller [[!DNL Creative] makron](/help/creative/creative-macros.md) för egen användning.

När du inkluderar en kreatör i ett paket och tilldelar paketet till en upplevelse kan du ändra landningssidans URL-adress och lägga till URL-adresser för bild- och klickspårning samt JavaScript för varje kreatör i paketet. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etikett:** (Valfritt) Etiketter som ska användas för alla valda kreatörer. Du kan filtrera kreatörer efter etikett i olika vyer i [!DNL Creative].

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas för kreatörerna öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

### Fliken Mallar

*Endast befintliga statiska HTML5-kreatörer*

HTML5-mallfilen för kreatören.

Du kan också ersätta den befintliga mallen med en ny mall som har en annan layout men samma uppsättning attributnamn som den ursprungliga mallen. Den nya mallen måste vara i ZIP-format med högst 2 MB. När den kreativa delen finns i ett paket kommer alla upplevelser som använder paketet att använda layouten från den nya mallen.

När du uppdaterar mallen för en överordnad kreatör med underordnade varianter uppdateras variationerna med ändringar i mallayouten, men attributvärdena för variationen ändras inte.

Ersätta den befintliga annonsmallen:

1. Klicka på **Uppdatera mall**.

1. Klicka på **Fortsätt**.

1. Ange en ZIP-fil på något av följande sätt:

   * Dra och släpp en fil på enheten eller nätverket i rutan.

   * Klicka på **[!UICONTROL select a file]** för att leta upp filen på enheten eller i nätverket.

   Se specifikationerna för [HTML-annonsen](html5-creative-specification.md).

1. Redigera de nya [HTML5-annonsinställningarna](#creative-settings-html5) efter behov.

1. Klicka på **[!UICONTROL Edit]**

## Inställningar för bildkreativitet {#creative-settings-image}

**Kreativt namn:** Namnet på den kreativa. För en ny kreatör används filnamnet som standard, men du kan ändra namnet. För flera bilder kan du redigera de enskilda kreativa namnen. **Tips!** Använd ett namn som är enkelt att hitta när du inkluderar den kreativa delen i en upplevelse.

**Språk:** Standardspråket för varje annons som du associerar med kreatörerna. Samma värde gäller för alla markerade bilder. &lt;!— KONTROLLERA OM NÅGOT KAN HÄNDA PÅ BUNDLE-NIVÅ, och om upplevelseinställningarna endast finns på upplevelsenivå: När du tar med kreatörerna i en upplevelse kan du välja att anpassa språkinställningarna för upplevelsen.

**Kreativ storlek:** (skrivskyddat) Dimensionerna för de överförda bilderna.

**URL för landningssida:** URL-adressen till standardlandningssidan för varje annons som du associerar med kreatörerna. Landningssidans URL måste vara en giltig URL som börjar med http:// eller https://. Den kan innehålla spårningsparametrar från tredje part eller [[!DNL Creative] makron](/help/creative/creative-macros.md) för egen användning. Samma värde gäller för alla markerade bilder.

När du inkluderar en kreatör i ett paket och tilldelar paketet till en upplevelse kan du ändra landningssidans URL-adress och lägga till URL-adresser för bild- och klickspårning samt JavaScript för varje kreatör i paketet. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etikett:** (Valfritt) Etiketter som ska användas för alla valda kreatörer. Du kan filtrera kreatörer efter etikett i olika vyer i [!DNL Creative].

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas för kreatörerna öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

## Inställningar för tredjepartsprogram {#creative-settings-third-party}

**JavaScriptCode:** En JavaScript-tagg (och eventuellt en alternativ tagg för webbläsare som inte stöder JavaScript) som pekar på den kreativa personen på annonsservern från tredje part. Skriptet varierar beroende på annonsserver. När du redigerar flera kreatörer tillämpas samma värde på alla valda kreatörer.

Alla tillgängliga makron och de data som ersätter dem visas under indatafältet. Om du vill infoga ett av makrona i taggen håller du markören över makrobeskrivningen och klickar på ![Kopiera till Urklipp](/help/creative/assets/copy-to-clipboard.png "Kopiera till Urklipp"). Klistra sedan in bilden där du vill ha den i taggen.

När du inkluderar den här kreativiteten i en upplevelse som du implementerar som en annons från en DSP, använder DSP informationen i den här taggen för att visa annonsen och spåra visningar och klickningar på den, och sedan överför taggen till annonsutbytet. När annonsen visas och klickas kommer annonsservern, DSP och [!DNL Creative] att spåra händelserna.

**[!UICONTROL Advertiser]:** (skrivskyddat) Annonsören som biblioteket är tillgängligt för.

**Kreativt namn:** Namnet på den kreativa. **Tips!** Använd ett namn som är enkelt att hitta när du inkluderar den kreativa delen i en upplevelse.

**Kreativ storlek:** (skrivskyddat för befintliga annonser) Den kreativa personens dimensioner. För nya kreatörer väljer du bland en lista med standardannonsstorlekar.
u
**Språk:** Standardspråket för varje annons som du associerar med kreatörerna.

**URL för landningssida:** Den URL för landningssida som används för att validera varje annons som du associerar med kreatörerna. Den faktiska landningssidan för varje annons bestäms av annonsservern från tredje part.

**Etikett:** (Valfritt) Etiketter som ska användas för alla valda kreatörer. Du kan filtrera kreatörer efter etikett i olika vyer i [!DNL Creative].

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas för kreatörerna öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

>[!MORELIKETHIS]
>
>* [Lägg till standardkreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-standard.md)
>* [Redigera standardkreatörer](/help/creative/creative-libraries/creative-edit-standard.md)
