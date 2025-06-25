---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Text och mall - Inställningar för negativa nyckelord på kampanjnivå

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alla annonsnätverk utom Yandex; valfritt) Tar bort befintliga negativa nyckelord på kampanjnivå som tidigare skapats med mallen som inte anges i listorna nedan. **Obs!** Negativa nyckelord som har skapats på andra sätt (t.ex. i oformaterade kalkylblad, [!UICONTROL Campaigns]-vyer eller i annonsnätverkets annonsredigerare) tas aldrig bort med mallen.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alla annonsnätverk förutom Yandex; valfritt) Gör att du kan ange negativa nyckelord för kampanjer vars namn innehåller en angiven sträng. När du väljer det här alternativet kan du lägga till upp till tre kampanjnamnssträngar och motsvarande nyckelord.

För varje sträng klickar du på **[!UICONTROL Add (Up to 3)]** och anger följande information:

* **[!UICONTROL If campaign name contains]:** En textsträng att söka efter var som helst i kampanjnamnet. Frågan är skiftlägeskänslig (till exempel matchar [!DNL Car] kampanjnamnet [!DNL Car Parts] men inte [!DNL INTERIOR CAR ACCESSORIES]).

* **[!UICONTROL Apply these negatives]:** Alla statiska negativa nyckelord på kampanjnivå som ska läggas till för kampanjer vars namn innehåller den angivna strängen. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Använd följande syntax utan ett minustecken:

   * Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft Advertising])
   * Negativ frasmatchning: `"keyword"`
   * Negativ exakt matchning: `[keyword]`

Den vanliga syntaxen för fras och exakta matchningstyper används i det kalkylblad som genereras när du sprider flödesdata via mallen. **Obs!** Du kan inte se de negativa nyckelorden på fliken [!UICONTROL Keywords] eller i vyn [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alla annonsnätverk förutom [!DNL Yandex]; valfritt) Alla statiska nyckelord på kampanjnivå som ska läggas till för kampanjer vars namn inte matchar en angiven sträng. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Använd följande syntax utan ett minustecken:

* Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft Advertising])
* Negativ frasmatchning: `"keyword"`
* Negativ exakt matchning: `[keyword]`

Den vanliga syntaxen för fras och exakta matchningstyper används i det kalkylblad som genereras när du sprider flödesdata via mallen. **Obs!** Du kan inte se de negativa nyckelorden på fliken [!UICONTROL Keywords] eller i vyn [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
