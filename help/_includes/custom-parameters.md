---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Fältet Egna parametrar i inställningarna för GL- och MS-kampanjer, inställningar för MS och grupper samt inställningar för MS-multimedia och responsiv annonsering

**[!UICONTROL Custom Parameters]:** (Valfritt) gäller endast målgruppskampanjer för [!DNL Microsoft Advertising]) Namn- och värdepar för upp till tre anpassade parametrar. Namnet får innehålla högst 16 alfanumeriska tecken. den maximala längden för värden är 200 tecken, inklusive inbäddade parametrar.

Du kan inkludera dina egna parameternamn i spårningsmallarna för enheten och dess underordnade enheter. När en användare klickar på en relevant annons ersätter annonsnätverket parameternamnet med det definierade parametervärdet. Om du till exempel skapar en kundparameter `{_color}=red` och spårningsmallen innehåller `http://tracker.example.com/?color={_color}&u={lpurl}`infogas&quot;red&quot; i färgparametern när en användare klickar på en annons.

Egna parametrar i annonsgruppen eller ([!DNL Microsoft Advertising] endast) och nivå åsidosätter anpassade parametrar på kampanjnivå med samma namn.
