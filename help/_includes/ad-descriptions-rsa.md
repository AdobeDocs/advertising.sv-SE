---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# Ad Descriptions field in RSA ad settings

**[!UICONTROL Ad Descriptions]:** Minst två och upp till fyra annonsbeskrivningar med valfria positionspunkter. Annonsnätverket visar annonser med upp till två beskrivningar. Ange minst två. Den maximala längden för varje beskrivning är 90 tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).

Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Om du vill fästa en beskrivning på en viss plats väljer du nålalternativet (till exempel [!UICONTROL Pinned at position 1]). Minst en beskrivning måste finnas tillgänglig för varje position. Om du fäster flera beskrivningar på samma plats, kommer den sista annonsen alltid att innehålla en av dessa beskrivningar på den angivna positionen. Beskrivningar som fästs vid position 2 kanske inte visas tillsammans med annonsen.

Om du vill lägga till ytterligare en beskrivning klickar du på **[!UICONTROL + Add]**.
