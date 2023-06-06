---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Fältet Spårningstyp i konto- och kampanjinställningar

**[!UICONTROL Tracking Type]:** Metoden som URL:er genereras med:

* *[!UICONTROL EF Redirect]* (standard): För kunder som vill använda Adobe Advertising Conversion Service. Den här metoden genererar unika ID:n för klickspårning och dirigerar om användare till Adobe-annonsservern för spårningsändamål innan de skickas till klientens landningssida.

   Den här metoden har standardalternativ för spårning som du kan anpassa, och du kan också ange parametrar som ska läggas till i varje URL.

* *[!UICONTROL No EF Redirect]:* För kunder som bara vill använda sina egna klickspårningskoder. Sök, Socialt och e-handel innehåller inte ID:n för klickspårning eller omdirigeringskoder. För konton med mål-URL:er är varje mål-URL samma som bas-URL:en.

   **Anteckningar:**

   * Endast kontohanterare, kontohanterare för Adobe och administratörsanvändare kan ändra det här värdet.
   * Om du ändrar spårningsmetoden måste du generera om spårnings-URL:er för kontot.
   * Spårningsalternativ på kampanjnivå åsidosätter kontonivåinställningar.
