---
title: Hantera annonsmallar för lagerflöden
description: Lär dig hur du hanterar annonsmallar genom vilka dina lagerdata kan bearbetas för att hantera kontostrukturen och leverera dynamiska annonser.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Hantera annonsmallar för lagerflöden

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (endast borttagningsåtgärder), och [!DNL Yandex] endast konton*

Före eller efter att du har överfört data kan du skapa sökmotorspecifika annonsmallar genom vilka dina data kan bearbetas. Du kan skapa mallar för textannonser och utökade/utökade textannonser, [!DNL Google Ads] och [!DNL Microsoft® Advertising] responsiva sökannonser och för [!DNL Google Ads] och [!DNL Microsoft® Advertising] shoppingannonser.

Du kan associera varje mall med en feed-fil, [!DNL Google Merchant Center] konto, eller [!DNL Microsoft® Merchant Center] och du kan koppla flera mallar till samma feed-fil eller konto. En annonsmall kan innehålla variabler, som ersätts med faktiska datakolumner från en överförd fil eller ett konto. I de flesta fall kan variablerna även innehålla [en modifieringsgrupp](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) som du skapat i Search, Social och Commerce för att skapa flera annonser, nyckelord, kampanjer eller annonsgrupper för varje tillämplig rad i datafilen. Med mallalternativen kan du antingen skapa en ny kontostruktur (kampanjer, annonsgrupper, nyckelord) för annonserna eller mappa annonserna till den befintliga kontostrukturen.

Förutom att skapa nya mallar från grunden kan du även skapa nya mallar genom att klona befintliga och redigera befintliga mallar.

När du har skapat en mall och associerat den med en dataflödesfil eller ett handlarcenterkonto kan du sprida informationen i filen via mallen för att skapa kampanjdata och kontostruktur, och eventuellt skapa en kalkylbladsfil för granskning eller för omedelbar publicering i annonsnätverket.

Alla mallar kan aktiveras, pausas eller tas bort. Feed-data kan bara spridas automatiskt via aktiva mallar. Du kan emellertid sprida data manuellt via en pausad mall.

## Skapa, klona eller redigera en flödesmall

Skapa separata mallar för text och utökade/utökade textannonser, responsiva sökannonser, [!DNL Google Ads] shoppingannonser, och [!DNL Microsoft® Advertising] shoppingannonser.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

1. Gör något av följande:

   * Om du vill skapa en mall från grunden klickar du på **[!UICONTROL Create/Clone]** i verktygsfältet ovanför datatabellen och välj sedan lämpligt annonsnätverk.

   * Så här klonar du en befintlig mall:

      1. Markera kryssrutan bredvid mallen som du vill kopiera.

      1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Create/Clone]** och välj sedan det annonsnätverk som ska användas.

   * (Om du vill redigera en befintlig mall) Klicka på bredvid mallnamnet ![Visa/redigera inställningar](/help/search-social-commerce/assets/settings.png "Visa/redigera inställningar").

1. Ange inställningarna för [text och mall](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] mall för annonser](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md), eller [[!DNL Microsoft® Advertising] mall för annonser](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Överst i mallinställningsfönstret anger du mallnamnet och det konto som ska användas.

      När du klonar en befintlig mall byter du namn på den nya mallen så att annonserna som skapas från den nya mallen inte associeras med annonser som skapas från källmallen.

   1. (Valfritt) I den vänstra kolumnen anger du den produktflödesfil eller det handlarcenterkonto vars data ska spridas via mallen:

      * (För produktflödesfiler) Om du vill välja en fil som har överförts tidigare klickar du på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-dropdown.png "Nedåtpil") och välj en fil i listan över tillgängliga feed-filer. Om du vill överföra en ny fil anger du filen antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på **[!UICONTROL Browse]** för att hitta filen på din enhet eller ditt nätverk och klicka sedan på **[!UICONTROL Upload]**.

      * (För ett synkat handlarcenterkonto) Välj kontonamnet.

      Kolumnerna för den valda filen eller kontot visas.

   1. På **[!UICONTROL Account Structure]** anger du kontostrukturinställningarna.

   1. (Endast textannonser) Klicka på **[!UICONTROL Keywords]** och ange nyckelordsinställningarna.

   1. (Endast text och responsiva sökannonser) Klicka på **[!UICONTROL Ads]** och gör något av följande:

      >[!NOTE]
      >
      >* Du kan inkludera upp till fyra mallar för annonsvariationer per standardmall för text och annonser, fem mallar för annonsvariationer per mall för utökad/utökad text och tre mallar för annonsvariationer per mall för responsiv sökning och annonsering.
      >* Varje annonsgrupp kan innehålla upp till tre aktiverade responsiva sökannonser.
      >* Du kan inte redigera befintlig standardtext och varianter, och befintliga mallar genererar inte längre standardtextannonser.
      >* Om du ändrar en annonsvariantmall kan befintliga annonser tas bort och nya kan skapas när du sprider data via mallen, [beroende på annonstyp och annonsnätverk](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Så här lägger du till en annonsvariation:

         1. Klicka **[!UICONTROL Add Ad Variation]** för att skapa en textannons **[!UICONTROL Add ETA Variation]** för att skapa en utökad/utökad textannons, eller **[!UICONTROL Add RSA Variation]** för att skapa en responsiv textannons.

            När du har angett annonstypen kan du bara skapa den annonstypen med mallen.

         1. Ange annonsinställningarna.

            För responsiva sökannonser kan du inkludera 3-15 rubriker och 2-4 beskrivningar.

         1. (Valfritt) Om du vill förifylla alla alternativa fält och kopieringsfält med text från de ursprungliga kopiefälten markerar du kryssrutan intill **[!UICONTROL Prefill]**.

         1. (Valfritt) Om du vill lägga till ytterligare en uppsättning annonskopior i en annons, som kan användas om någon av raderna i den ursprungliga annonskopian överskrider maxlängden när alla dynamiska parametrar ersätts med data under spridningen, klickar du på **[!UICONTROL Add Alternate]** och lägg sedan till de alternativa värdena.

            >[!NOTE]
            >
            >* Om [!UICONTROL Prefill] är markerat, fylls de alternativa fälten i förväg med originalfälten och du kan redigera dem efter behov.
            >* Endast de reklamkopieringsfält som överskrider maxlängden ersätts med det alternativa värdet. Om t.ex. bara en originalrubrik eller -titel är för lång, används den alternativa rubriken eller titeln och de ursprungliga beskrivningarna för den genererade annonsvarianten. Se därför till att den alternativa annonskopian passar när den kombineras med den ursprungliga annonskopian.
            >* Om den ursprungliga annonskopian uppfyller sökmotorns krav på längd, ignoreras den alternativa annonskopian.
            >* Du kan ange upp till fyra alternativ för varje reklamkopieringsfält.

         * Så här redigerar du en annonsvariation:

            1. Redigera annonsinställningarna.

               För responsiva sökannonser kan du inkludera 3-15 rubriker och 2-4 beskrivningar.

            1. (Valfritt) Om du vill förifylla alla alternativa fält och kopieringsfält med text från de ursprungliga kopiefälten markerar du kryssrutan intill **[!UICONTROL Prefill]**.

            1. (Valfritt) Om du vill lägga till ytterligare en uppsättning annonskopior i en annons, som kan användas om någon av raderna i den ursprungliga annonskopian överskrider maxlängden när alla dynamiska parametrar ersätts med data under spridningen, klickar du på **[!UICONTROL Add Alternate]** och lägg sedan till de alternativa värdena.

               >[!NOTE]
               >
               >* Om [!UICONTROL Prefill] är markerat, fylls de alternativa fälten i förväg med originalfälten och du kan redigera dem efter behov.
               >* Endast de reklamkopieringsfält som överskrider maxlängden ersätts med det alternativa värdet. Om t.ex. bara en originalrubrik eller -titel är för lång, används den alternativa rubriken eller titeln och de ursprungliga beskrivningarna för den genererade annonsvarianten. Se därför till att den alternativa annonskopian passar när den kombineras med den ursprungliga annonskopian.
               >* Om den ursprungliga annonskopian uppfyller sökmotorns krav på längd, ignoreras den alternativa annonskopian.
               >* Du kan ange upp till fyra alternativ för varje reklamkopieringsfält.

         * Om du vill ta bort en annonsvariation klickar du på **[!UICONTROL Remove ETA Variation]** (för expanderade/utökade textannonser) eller **[!UICONTROL Remove RSA Variation]** (för responsiva sökannonser) bredvid annonsvariationen, beroende på vad som är tillämpligt.

   1. (Endast köpmallar) Klicka på **[!UICONTROL Product Groups]** och sedan ange information om de produktgrupper du vill använda som mål.

   1. (Valfritt) Klicka på **[!UICONTROL Feed Filters]** och sedan ange vilka rader i matningsfilen som ska spridas.

   1. (Valfritt) Klicka på **[!UICONTROL Label Classifications tab]** och ange de etikettklassificeringsvärden som ska tilldelas till de olika kampanjkomponenterna som skapas:

      1. Klicka i kryssrutan bredvid **[!DNL \[Component\] Label Classifications]**.

      1. För varje etikettklassificering som ska tilldelas komponenten gör du följande:

         1. Klicka på **[!UICONTROL Add Label Classification]**.

         1. Välj etikettklassificeringen och välj sedan ett befintligt värde eller ange ett nytt värde.

1. Spara mallen:

   * Klicka på om du bara vill spara mallen **[!UICONTROL Save]** och klicka sedan på **[!UICONTROL Save]** igen.

   * Om du vill spara mallen och sprida den angivna datafilen genom den klickar du på **[!UICONTROL Save]** och klicka sedan på **[!UICONTROL Save & Propagate]**.

## Ändra status för flödesmallar

Du kan aktivera alla pausade dataflödesmallar eller pausa alla aktiva datafeedmallar.

>[!NOTE]
>
>Du kan sprida data manuellt via en pausad mall, men data sprids inte automatiskt genom den.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

1. Markera kryssrutan bredvid varje mall vars status du vill ändra.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Change Status]** och klicka sedan på **[!UICONTROL Activate]** eller **[!UICONTROL Pause]**.

## Ta bort feed-mallar

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** som öppnas i [!UICONTROL Templates] -fliken.

1. Markera kryssrutan bredvid varje mall som du vill ta bort.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Automatisera och hantera lagerflöden](../inventory-feeds-about.md)
>* [Inställningar för textannons och responsiv sökning och mallar](template-text-rsa.md)
>* [[!DNL Google Ads] inställningar för butiks- och mallinställningar](template-google-shopping.md)
>* [[!DNL Microsoft® Advertising] inställningar för butiks- och mallinställningar](template-microsoft-shopping.md)
>* [Sprida feed-data via mallar](../feed-data-propagate.md)
