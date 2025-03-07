---
title: Inställningar för riktade upplevelser
description: Se beskrivningar av alla inställningar för riktade annonsupplevelser.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 0%

---

# Inställningar för riktade annonsupplevelser

*Stängd beta*

## [!UICONTROL Experience basics] avsnitt

**[!UICONTROL Advertiser]:** (Skrivskyddat för befintliga upplevelser) Annonsören som lägger bud på de kreativa kombinationer och målkombinationer som ingår i upplevelsen. När du väl har sparat upplevelsen kan du inte ändra annonsören.

**[!UICONTROL Experience Name]:** Ett unikt namn för upplevelsen. **Tips!** Använd ett namn som du enkelt hittar när du använder upplevelsen som en annons i Advertising DSP eller andra DSP.

**[!UICONTROL Creative Library]:** (skrivskyddat för befintliga upplevelser) Ett enskilt kreativt bibliotek att använda för upplevelsen. När du har sparat upplevelsen kan du inte ändra biblioteket.

## [!UICONTROL Default creatives] avsnitt

**\[Standardalternativ har angetts\]:** Standardbildskapare som ska användas när en webbläsare inte kan visa användare som är tilldelade upplevelsen, till exempel när webbläsaren inte är JavaScript-aktiverad eller annonsservern inte kan anpassa annonsen på grund av förseningar. Inkludera en kreativ bild per annonsstorlek som upplevelsen gäller för. Dina val avgör vilka kreativa storlekar som kan användas för upplevelsen.<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

För upplevelser med mål för beslutsträd kan du åsidosätta standardkreatörerna med kreativa paket som innehåller kreativa alternativ av samma storlek inifrån beslutsträdet.<!-- verify -->

* Om du vill lägga till en standardkreativ med olika dimensioner klickar du på **[!UICONTROL + Add Sizes]**, markerar kryssrutan bredvid varje kreativ som du vill lägga till i den högra rutan och klickar sedan på **[!UICONTROL Add Creatives]**.

* Om du vill ta bort en standardbild håller du markören över den kreativa miniatyrbilden och klickar på ![Ta bort](/help/creative/assets/delete.png "Ta bort").

* Om du vill ta bort alla standardalternativ klickar du på ![Ta bort](/help/creative/assets/delete.png "Ta bort") **[!UICONTROL Delete all]**.

* Om du vill visa eller dölja rutan Creative till höger klickar du på ![Visa/Dölj](/help/creative/assets/hide-show-creatives.png "Visa/Dölj") i det övre högra hörnet av den högra rutan.

## [!UICONTROL Targeting] avsnitt

**[!UICONTROL Targeting]:** (skrivskyddat för befintliga upplevelser) Aktiverar kreativ målgruppsanpassning med hjälp av ett beslutsträd och automatiskt skapande av taggar. När du har sparat upplevelsen kan du inte ändra den här inställningen.

**[!UICONTROL Dynamic ads]:** (Skrivskyddad för befintliga upplevelser) Anger att upplevelsen innehåller dynamiska annonser. **Obs!** En upplevelse kan innehålla antingen alla standardannonser eller alla dynamiska annonser. När du har sparat upplevelsen kan du inte ändra den här inställningen.

**[!UICONTROL Language Targeting]:** (Endast upplevelser med standardannonser, valfritt, skrivskyddat för befintliga upplevelser) Kontrollerar användarens språkinställningar i webbläsaren och visar ett kreativt språk på det angivna språket när det finns en kreativ på det språket. När det inte finns någon tillgänglig kreatör i det webbläsarangivna språket används inställningen [!UICONTROL Preferred language] i stället.

När du har sparat upplevelsen kan du inte ändra den här inställningen.

**[!UICONTROL Preferred language]:** (Endast upplevelser med standardannonser, skrivskyddad för befintliga upplevelser) Språket för alla annonser som skapas från upplevelsen, utom när [!UICONTROL Language Targeting] är aktiverat. När du har sparat upplevelsen kan du inte ändra den här inställningen.

## [!UICONTROL Advanced] avsnitt

**Dataisolering:** (skrivskyddat för befintliga upplevelser; valfritt) Om du vill rikta användare baserat på specifika nyckelvärdepar som DSP, utgivaren eller partnern skickar i realtid vid exponering. Du kan ange upp till fem databassnycklar (parametrar). När du ställer in mål inom beslutsträdet kan du ta med en nivå av målnoder för datapassage och ange vilka värden som ska användas för varje nod. Om du inte anger någon nyckel i det här fältet när du skapar upplevelsen kan du ändå ange en i beslutsträdet.<!-- May move this to just within the decision tree.  -->

Varje nyckel läggs till som ett makro i annonsupplevelsen
som du kan generera för att implementera som en annons i din DSP.

**Radie:** (Endast upplevelser med dynamiska annonser; valfritt) En radie från ett amerikanskt postnummer som anges i feed-filen att rikta. Välj en radie från 0 engelska mil till 200 engelska mil. Den feed-fil som används för att skapa dynamiska annonser för upplevelsen måste innehålla en [!UICONTROL ZIP]-kolumn <!-- or a user-named column mapped to a ZIP column --> med ett värde för varje produktrad i filen. För en radie på 10 engelska mil kan till exempel en annons för en produkt som är tillgänglig i 95110 visas för användare inom 10 engelska mil av 95110 (bestäms av användarens IP-adress).

**RT-pixel:** (skrivskyddat för befintliga upplevelser; valfritt) En [!UICONTROL Creative] återmarknadsföringspixel som kan ha som mål. När du ställer in mål inom beslutsträdet kan du inkludera en nivå med målnoder för RT-pixlar. För varje nod ska du ange vilken pixel som ska användas som mål och vilka värden för pixelns attribut som krävs för att visa kreatörerna i de tilldelade kreativa paketen. Om du inte anger en pixel i det här fältet när du skapar upplevelsen kan du ändå ange en i beslutsträdet.<!-- May move this to just within the decision tree. -->

**Etikett:**<!-- should be "Labels" --> (Valfritt) Alla [!DNL Creative]-specifika etiketter som ska användas för upplevelsen. Du kan filtrera upplevelser efter etikett i vyn Erfarenheter <!-- sic -->.

* Om du vill välja befintliga etiketter klickar du på ![Ned](/help/creative/assets/chevron-down.png "Ned") och markerar kryssrutan bredvid varje etikett som ska användas.

* Om du vill söka efter befintliga etiketter börjar du med att ange en textsträng i etikettnamnet.

* Om du vill skapa en ny etikett som ska användas öppnar du listan, klickar på **+ Lägg till etikett**, anger ett nytt etikettnamn i fältet [!UICONTROL Label] och klickar sedan på **Skapa**.

* Om du vill ta bort en etikett avmarkerar du kryssrutan bredvid etikettnamnet.

**URL för Impression Tracking:** (valfritt) En URL för intrycksspårning från tredje part som ska läggas till på landningssidans URL för alla annonser som skapas från upplevelsen. Du kan inkludera upp till fem URL-adresser. Om du vill lägga till ytterligare en URL-adress klickar du på ![ikonen](/help/creative/assets/create.png) **[!UICONTROL Add More] och anger URL-adressen.

När du anger en URL listas alla [tillgängliga makron](/help/creative/creative-macros.md) och de data som de ersätts med längre ned på sidan. Om du vill infoga något av makrona i URL-adressen håller du markören över makrobeskrivningen och klickar på ![Kopiera till Urklipp](/help/creative/assets/copy-to-clipboard.png "Kopiera till Urklipp"). Klistra sedan in makrot där du vill ha det i URL-fältet.

>[!NOTE]
>
>* [!DNL Creative] prefixerar automatiskt sina egna taggar för uppvisningsspårning till landningssidans URL.
>* Du kan [åsidosätta den här URL:en för alla kreatörer i upplevelsen](experience-tracking-urls-targeting.md).
>* Du kan även ange JavaScript-visningsspårningskod från tredje part i fältet [!UICONTROL Client JS]

**Klicka på Spårnings-URL:** (valfritt) (Valfritt) En klicknings-URL från tredje part som ska läggas till på landningssidans URL. Du kan inkludera upp till fem URL-adresser. Om du vill lägga till ytterligare en URL-adress klickar du på ![ikonen](/help/creative/assets/create.png) **[!UICONTROL Add More] och anger URL-adressen.

När du anger en URL listas alla [tillgängliga makron](/help/creative/creative-macros.md) och de data som de ersätts med längre ned på sidan. Om du vill infoga något av makrona i URL-adressen håller du markören över makrobeskrivningen och klickar på ![Kopiera till Urklipp](/help/creative/assets/copy-to-clipboard.png "Kopiera till Urklipp"). Klistra sedan in makrot där du vill ha det i URL-fältet.

>[!NOTE]
>
>* [!DNL Creative] prefixerar automatiskt sina egna taggar för uppvisningsspårning till landningssidans URL.
>* Du kan [åsidosätta den här URL:en för alla kreatörer i upplevelsen](experience-tracking-urls-targeting.md).

**Klient-JS:** (valfritt) Något av följande:

* (När annonsören använder en OBA-kompatibel leverantör för annonserna) JavaScript-kod som pekar på annonsövertäckningen som gör att användarna kan välja bort onlinebeteendeanpassning (OBA).

* Eventuell tredjepartskod för JavaScript-visningsspårning som läggs till på landningssidan. **Obs!** Du kan även ange en URL för visningsspårning från tredje part i fältet [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Skapa en upplevelse med mål för beslutsträd](experience-create-targeting.md)
>* [Redigera en upplevelse med mål för beslutsträd](experience-edit-targeting.md)
>* [Tillgängliga makron för att spåra URL:er](/help/creative/creative-macros.md)
