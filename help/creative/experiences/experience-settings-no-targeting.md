---
title: Inställningar för icke-målinriktade upplevelser
description: Se beskrivningar av alla inställningar för annonsupplevelser utan målgruppsanpassning för beslutsträd.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: e070e676b9ae321ddc73acfff0dfc05ea91f9715
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# Inställningar för icke-målinriktade upplevelser

*Stängd beta*

## [!UICONTROL Experience basics] avsnitt

**[!UICONTROL Advertiser]:** (Skrivskyddad för befintliga upplevelser) Annonsören som ska lägga bud på de kreatörer som ingår i upplevelsen. När du väl har sparat upplevelsen kan du inte ändra annonsören.

**[!UICONTROL Experience Name]:** Ett unikt namn för upplevelsen. **Tips!** Använd ett namn som du enkelt hittar när du använder upplevelsen som en annons i Advertising DSP eller andra DSP.

**[!UICONTROL Creative Library]:** (skrivskyddat för befintliga upplevelser) Ett enskilt kreativt bibliotek att använda för upplevelsen. När du har sparat upplevelsen kan du inte ändra biblioteket.

## [!UICONTROL Default creatives] avsnitt

**\[Standardalternativ har angetts\]:** Standardbildskapare som ska användas när en webbläsare inte kan visa användare som är tilldelade upplevelsen, till exempel när webbläsaren inte är JavaScript-aktiverad eller annonsservern inte kan anpassa annonsen på grund av förseningar. Inkludera en kreativ bild per annonsstorlek som upplevelsen gäller för. Dina val avgör vilka kreativa storlekar som kan användas för upplevelsen. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

För upplevelser utan mål för beslutsträd kan du åsidosätta standardkreatörerna med kreatörer i samma storlek inom [!UICONTROL Tag Manager].

* Om du vill lägga till en standardkreativ med olika dimensioner klickar du på **[!UICONTROL + Add Sizes]**, markerar kryssrutan bredvid varje kreativ som du vill lägga till i den högra rutan och klickar sedan på **[!UICONTROL Add Creatives]**.

* Om du vill ta bort en standardbild håller du markören över den kreativa miniatyrbilden och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort").

* Om du vill ta bort alla standardalternativ klickar du på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Delete all]**.

* Om du vill visa eller dölja rutan Creative till höger klickar du på ![Visa/Dölj](/help/creative/assets/hide-show-creatives.png "Visa/Dölj") i det övre högra hörnet av den högra rutan.

## [!UICONTROL Targeting] avsnitt

**[!UICONTROL Targeting]:** (Skrivskyddad för befintliga upplevelser) Gäller inte om du inte aktiverar mål med ett beslutsträd. Behåll det här alternativet inaktiverat. **Obs!** När du har sparat en upplevelse utan mål kan du inte lägga till målinriktning senare.

**[!UICONTROL Dynamic ads]:** (Skrivskyddad för befintliga upplevelser) Anger att upplevelsen innehåller dynamiska annonser. **Obs!** En upplevelse kan innehålla antingen alla standardannonser eller alla dynamiska annonser.

**[!UICONTROL Language Targeting]:** (Endast upplevelser med standardannonser, valfritt, skrivskyddat för befintliga upplevelser) Kontrollerar användarens språkinställningar i webbläsaren och visar ett kreativt språk på det angivna språket när det finns en kreativ på det språket. När det inte finns någon tillgänglig kreatör i det webbläsarangivna språket används inställningen [!UICONTROL Preferred language] i stället. När du har sparat upplevelsen kan du inte ändra den här inställningen.

**[!UICONTROL Preferred language]:** (Endast upplevelser med standardannonser, skrivskyddad för befintliga upplevelser) Språket för alla annonser som skapas från upplevelsen, utom när [!UICONTROL Language Targeting] är aktiverat. När du har sparat upplevelsen kan du inte ändra den här inställningen.

## [!UICONTROL Advanced] avsnitt

**Dataisolering:** (endast upplevelser med dynamiska annonser; valfritt) Om du vill rikta in användare baserat på specifika nyckelvärdepar som DSP, utgivaren eller partnern skickar i realtid vid intrycket. Du kan ange upp till fem databassnycklar (parametrar).<!-- May move this to just within the decision tree. -->

När du skapar en tagg för annonsupplevelser för en viss kreativ storlek läggs varje nyckel som anges i det här fältet till som ett makro i taggen. Ange värdet för varje nyckelvärdepar i taggen innan du implementerar taggen som en annons i din DSP.

**Radie:** (Endast upplevelser med dynamiska annonser; valfritt) En radie från ett amerikanskt postnummer som anges i feed-filen att rikta. Välj en radie från 0 engelska mil till 200 engelska mil. Den feed-fil som används för att skapa dynamiska annonser för upplevelsen måste innehålla en [!UICONTROL ZIP]-kolumn <!-- or a user-named column mapped to a ZIP column --> med ett värde för varje produktrad i filen. För en radie på 10 engelska mil kan till exempel en annons för en produkt som är tillgänglig i 95110 visas för användare inom 10 engelska mil av 95110 (bestäms av användarens IP-adress).

**RT-pixel:** (Upplevelser med enbart dynamiska annonser; valfritt) En [!UICONTROL Creative] återmarknadsföringspixel som kan ha som mål. När du ställer in mål inom beslutsträdet kan du inkludera en nivå med målnoder för RT-pixlar. För varje nod ska du ange vilken pixel som ska användas som mål och vilka värden för pixelns attribut som krävs för att visa kreatörerna i de tilldelade kreativa paketen. Om du inte anger en pixel i det här fältet kan du ändå ange en i beslutsträdet.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> (Valfritt) Alla [!DNL Creative]-specifika etiketter som ska användas för upplevelsen. Du kan filtrera upplevelser efter etikett i vyn Erfarenheter <!-- sic -->.

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

**[!UICONTROL Impression Tracking URL]:** (Valfritt) En URL för visningsspårning från tredje part som ska läggas till på landningssidans URL för alla annonser som skapats från upplevelsen. Du kan inkludera upp till fem URL-adresser. Om du vill lägga till ytterligare en URL-adress klickar du på ![ikonen](/help/creative/assets/create.png) **[!UICONTROL Add More] och anger URL-adressen.

När du anger en URL listas alla [tillgängliga makron](/help/creative/creative-macros.md) och de data som de ersätts med längre ned på sidan. Om du vill infoga något av makrona i URL-adressen håller du markören över makrobeskrivningen och klickar på ![Kopiera till Urklipp](/help/creative/assets/copy-to-clipboard.png "Kopiera till Urklipp"). Klistra sedan in makrot där du vill ha det i URL-fältet.

>[!NOTE]
>
>* [!DNL Creative] prefixerar automatiskt sina egna taggar för uppvisningsspårning till landningssidans URL.
>* Du kan åsidosätta den här URL:en för alla kreatörer i upplevelsen.
>* Du kan även ange JavaScript-visningsspårningskod från tredje part i fältet [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (Valfritt) (Valfritt) En URL för klickspårning från tredje part som ska läggas till på landningssidans URL. Du kan inkludera upp till fem URL-adresser. Om du vill lägga till ytterligare en URL-adress klickar du på ![ikonen](/help/creative/assets/create.png) **[!UICONTROL Add More]** och anger URL-adressen.

När du anger en URL listas alla [tillgängliga makron](/help/creative/creative-macros.md) och de data som de ersätts med längre ned på sidan. Om du vill infoga något av makrona i URL-adressen håller du markören över makrobeskrivningen och klickar på ![Kopiera till Urklipp](/help/creative/assets/copy-to-clipboard.png "Kopiera till Urklipp"). Klistra sedan in makrot där du vill ha det i URL-fältet.

>[!NOTE]
>
>* [!DNL Creative] prefixerar automatiskt sina egna taggar för uppvisningsspårning till landningssidans URL.
>* Du kan åsidosätta den här URL:en för alla kreativa <!-- creative bundle for targeted experiences --> i upplevelsen.

**[!UICONTROL Client JS]:** (Valfritt) Något av följande:

* (När annonsören använder en OBA-kompatibel leverantör för annonserna) JavaScript-kod som pekar på annonsövertäckningen som gör att användarna kan välja bort onlinebeteendeanpassning (OBA).

* Eventuell tredjepartskod för JavaScript-visningsspårning som läggs till på landningssidan. **Obs!** Du kan även ange en URL för visningsspårning från tredje part i fältet [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Skapa en upplevelse utan mål för beslutsträd](experience-create-no-targeting.md)
>* [Redigera en upplevelse utan mål för beslutsträd](experience-edit-no-targeting.md)
>* [Tillgängliga makron för att spåra URL:er](/help/creative/creative-macros.md)
>* [Skapa en annonstagg manuellt för en tillämplig kreativ storlek](experience-tag-create-manually.md)
>* [Tilldela kreatörer till en annonstagg för upplevelser utan målinriktning](experience-tag-assign-creatives.md)
>* [Anpassa spårnings-URL:er för en upplevelse utan att ange mål](experience-tracking-urls-no-targeting.md)
>* [Anpassa den kreativa optimeringen och schemaläggningen för en upplevelse utan målinriktning](experience-optimization-scheduling-no-targeting.md)
