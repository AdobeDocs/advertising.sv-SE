---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---
# Ad Descriptions field in RSA ad settings

**[!UICONTROL Ad Descriptions]:** Minst två och upp till fyra annonsbeskrivningar med valfria positionspunkter. Annonsnätverket visar annonser med upp till två beskrivningar. ange minst två. Den maximala längden för varje beskrivning är 90 tecken, inklusive all dynamisk text (till exempel värdena för nyckelord och annonsanpassare).

Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde som ska infogas när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Om du vill fästa en beskrivning vid en viss position väljer du nålalternativet (till exempel &quot;[!UICONTROL Pinned at position 1]&quot;). Minst en beskrivning måste finnas tillgänglig för varje position. Om du fäster flera beskrivningar på samma plats, kommer den sista annonsen alltid att innehålla en av dessa beskrivningar på den angivna positionen. Beskrivningar som fästs vid position 2 kanske inte visas med annonsen.

Om du vill lägga till ytterligare en beskrivning klickar du på **[!UICONTROL + Add]**.
