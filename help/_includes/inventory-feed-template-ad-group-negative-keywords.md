---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Text och mall - Lägg till negativa nyckelordsinställningar på gruppnivå

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alla annonsnätverk utom Yandex; valfritt) Tar bort befintliga negativa nyckelord på annonsgruppnivå som tidigare skapats med mallen och som inte anges i listorna nedan. **Obs!** Negativa nyckelord som har skapats på andra sätt (t.ex. i oformaterade kalkylblad, [!UICONTROL Campaigns]-vyer eller i annonsnätverkets annonsredigerare) tas aldrig bort med mallen.

**[!UICONTROL Apply these negatives]:** (Alla annonsnätverk förutom [!DNL Yandex]; valfritt) Alla statiska och gruppnivånegativa nyckelord som ska läggas till. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Använd följande syntax utan ett minustecken:

* Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft Advertising])
* Negativ frasmatchning: `"keyword"`
* Negativ exakt matchning: `[keyword]`

Den vanliga syntaxen för fras och exakta matchningstyper används i det kalkylblad som genereras när du sprider flödesdata via mallen. **Obs!** Du kan inte se de negativa nyckelorden på fliken [!UICONTROL Keywords] eller i vyn [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
