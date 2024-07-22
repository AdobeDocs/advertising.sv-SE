---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Text och mall - Lägg till gruppmappningsmetod

**[!UICONTROL Map Method]:** (När [!UICONTROL Map Only] är aktiverat för annonsgrupper; alla annonsnätverk utom [!DNL Yandex]) Den metod som används för att mappa nya nyckelord och annonser till befintliga annonsgrupper:

* *[!UICONTROL Contains Anywhere]:* Lägger till data i en befintlig annonsgrupp vars namn innehåller den angivna strängen, om den finns.

* *[!UICONTROL Contains Exactly]:* Lägger till data i en befintlig annonsgrupp vars namn innehåller den angivna strängen, om den finns.

* *[!UICONTROL Exactly Matches]* (standardvärdet): Lägger till data i en befintlig annonsgrupp med samma namn, om det finns.

När ingen matchning hittas ignoreras alla data för annonsgruppen. Om annonsgruppsdata i feeden inte innehåller kampanjdata mappas annonsgruppen till en annonsgrupp med samma namn i alla kampanjer, om det finns någon. Om det finns flera matchningar av annonsgrupper mappas nyckelorden och annonserna till alla.
