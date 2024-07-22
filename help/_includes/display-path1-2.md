---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Visa fälten Sökväg 1 och Visa sökväg 2 i vissa annonsinställningar

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (valfritt) Text som läggs till i den visnings-URL som automatiskt extraheras från den slutliga URL:en. Varje sökväg föregås av ett snedstreck (`/`) i URL:en. En sökväg får inte innehålla snedstreck (`/`) eller radmatningstecken (`\n`). Den maximala längden för varje bana är 15 tecken eller 7 dubbelbyte-tecken.

Om du vill infoga en annonsanpassare använder du följande format, där `Default text` är ett valfritt värde att infoga när din feed-fil inte innehåller ett giltigt värde:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Om [!UICONTROL Display Path 1] till exempel är&quot;erbjudanden&quot; och [!UICONTROL Display Path 2] är&quot;lokal&quot; blir URL:en för visning `<display URL>/deals/local`, till exempel www.example.com/deals/local.
