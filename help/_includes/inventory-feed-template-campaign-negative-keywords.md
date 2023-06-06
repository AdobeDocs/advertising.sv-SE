---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Text och mall - Inställningar för negativa nyckelord på kampanjnivå

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alla annonsnätverk utom Yandex. (valfritt) Tar bort befintliga negativa nyckelord på kampanjnivå som tidigare skapats med mallen som inte anges i listorna nedan. **Obs!** Negativa nyckelord som har skapats på andra sätt (t.ex. i oformaterade kalkylblad, [!UICONTROL Campaigns] vyer, eller annonsnätverkets annonsredigerare) tas aldrig bort med mallen.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alla annonsnätverk utom Yandex. (valfritt) Gör att du kan ange negativa nyckelord för kampanjer vars namn innehåller en angiven sträng. När du väljer det här alternativet kan du lägga till upp till tre kampanjnamnssträngar och motsvarande nyckelord.

För varje sträng klickar du på **[!UICONTROL Add (Up to 3)]** och ange följande information:

* **[!UICONTROL If campaign name contains]:**  En textsträng att söka efter var som helst i kampanjnamnet. Frågan är skiftlägeskänslig (till exempel &quot;[!DNL Car]&quot; matchar kampanjnamnet &quot;[!DNL Car Parts]&quot; men inte &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Alla statiska negativa nyckelord på kampanjnivå som ska läggas till för kampanjer vars namn innehåller den angivna strängen. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Använd följande syntax utan ett minustecken:

   * Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft Advertising])
   * Negativ frasmatchning: `"keyword"`
   * Negativ exakt matchning: `[keyword]`

Den vanliga syntaxen för fras och exakta matchningstyper används i det kalkylblad som genereras när du sprider flödesdata via mallen. **Obs!** Du kan inte se de negativa nyckelorden i [!UICONTROL Keywords] eller på [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vy.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alla annonsnätverk utom [!DNL Yandex]; valfritt) Alla statiska negativa nyckelord på kampanjnivå som ska läggas till för kampanjer vars namn inte matchar en angiven sträng. Om du vill ange flera nyckelord eller flera matchningstyper för samma nyckelord anger du dem på separata rader. Använd följande syntax utan ett minustecken:

* Negativ bred matchning: `keyword` (stöds inte av [!DNL Microsoft Advertising])
* Negativ frasmatchning: `"keyword"`
* Negativ exakt matchning: `[keyword]`

Den vanliga syntaxen för fras och exakta matchningstyper används i det kalkylblad som genereras när du sprider flödesdata via mallen. **Obs!** Du kan inte se de negativa nyckelorden i [!UICONTROL Keywords] eller på [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vy.
