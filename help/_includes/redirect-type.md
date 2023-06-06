---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Omdirigeringstypfält i konto- och kampanjinställningar

**[!UICONTROL Redirect Type]:** (för [!UICONTROL EF Redirect] endast) Metoden för omdirigering av slutanvändare till den slutliga URL:en eller mål-URL:en. Det valda alternativet gäller för alla annonser, nyckelord och placeringar i kontot eller kampanjen. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar och standardinställningen på kampanjnivå ärvs från kontoinställningarna.

* *[!UICONTROL Standard]:* Om du bara vill dirigera om slutanvändaren till den angivna URL:en.

* *[!UICONTROL Token]:* Om du vill dirigera om slutanvändaren till URL:en och även registrera ID:t för sökning, sociala medier och handel för klickningen (`ef_id`) som en frågesträngsparameter, som används som token. Välj det här alternativet om du ska rapportera offlinetransaktioner, om du vill att sökning, sociala medier och handel ska utbyta data med Adobe Analytics, eller om du vill spåra alla konverteringar som sker inom [!DNL Apple Safari] webbläsare.

**Anteckningar:**

* Om du byter från [!UICONTROL Standard] till [!UICONTROL Token], eller vice versa, måste du återskapa spårnings-URL:er för kontot.
* Du kan åsidosätta inställningen på kontonivå på kampanjnivå.
