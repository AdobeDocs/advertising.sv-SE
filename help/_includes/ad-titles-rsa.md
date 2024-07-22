---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Ad Titles field in RSA ad settings

**[!UICONTROL Ad Titles]:** Minst tre och upp till femton annonstitlar (rubriker), med valfria positionspunkter. Annonsnätverket visar annonser med upp till tre rubriker. Ange minst tre. Den maximala längden för varje rubrik är 30 tecken, inklusive alla dynamiska tecken
text (t.ex. värden för nyckelord och annonsanpassare).

Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Om du vill fästa en titel på en viss plats väljer du nålalternativet (till exempel [!UICONTROL Pinned at position 1]). Det måste finnas minst en rubrik för varje position. Om du fäster flera titlar på samma plats, kommer den sista annonsen alltid att innehålla en av dessa titlar på den angivna positionen. Titlar som är fästa på position 3 kanske inte visas med annonsen.

Om du vill lägga till ytterligare en titel klickar du på **[!UICONTROL + Add]**.
