---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---
# Text och mall - Etikettklassificeringar

**\[komponent\] [!UICONTROL Label Classifications] > \[Etikettklassificering och värde\]:** (Valfritt) Värden för upp till fem befintliga etikettklassificeringar som ska tilldelas till olika kampanjkomponenter som skapas eller redigeras med hjälp av mallen. Etikettvärden ärvs av underordnade entiteter (inklusive underordnade entiteter som skapas senare), så du behöver inte ange värden för underordnade entiteter om du inte vill åsidosätta de ärvda värdena. Etikettklassificeringar för produktgrupper används på enhetsnivån (mest detaljnivå).

För varje kampanjkomponent som du vill tilldela etikettklassificeringar till:

1. Klicka i kryssrutan bredvid **\[komponent\][!UICONTROL Label Classifications]**.

1. Konfigurera etikettklassificeringsvärden för mallen:

   * För varje etikettklassificering och värde som ska tilldelas komponenten gör du följande:

      1. Klicka på **[!UICONTROL Add Label Classification]**.

      1. Välj den befintliga etikettklassificeringen och välj sedan ett befintligt värde eller ange ett nytt värde.

         Värdet får innehålla högst 100 tecken och kan innehålla ASCII-tecken och tecken som inte är ASCII-tecken.

         Om du vill infoga ett kolumnnamn som en dynamisk parameter för ett etikettklassificeringsvärde klickar du i indatafältet (det andra fältet) och sedan på ett kolumnnamn i kolumnlistan.

         Du kan bara inkludera ett värde per klassificering och kampanjkomponent. En kampanj kan till exempel ha Color=Red men inte Color=Red och Color=Blue.
   * Om du vill ändra ett befintligt etikettklassificeringsvärde markerar eller anger du ett nytt värde.

   * Om du vill ta bort ett befintligt etikettklassificeringsvärde klickar du på **[!UICONTROL X]** bredvid värdet.
