---
title: Ordlista
description: Se definitioner av nyckeltermer.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Ordlista {#glossary}

*Stängd beta*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**klickfrekvens:** Ett annonsklick som resulterar i en konvertering.

**datapassmål:** Med datapassmål kan annonselement väljas baserat på data som tillhandahålls i realtid av DSP, utgivare eller partner. Detta kan inkludera data från tredje part.

<!-- verify this -->I en annonsupplevelse kan varje datapassmål innehålla upp till fem nyckelvärdepar. Du anger nycklarna och minst ett värde i den första målnoden på den nivån, och samma nycklar är tillgängliga för målnoder på samma nivå. Alla nyckelvärdepar läggs till som ett makro till annonstaggen för den här upplevelsen. Vid tidpunkten för annonsintrycket ansvarar DSP, utgivare eller partner för att ersätta värdena med data som är specifika för det intrycket. Informationen skickas tillbaka till [!DNL Creative] så att den kan visa en lämplig annonsupplevelse baserat på de regler som definierats i upplevelsen.

Om du till exempel vill rikta en eller flera möjliga användare till tittare som är kvinnliga och som är i segment 1234, konfigurerar du datapassmålen `gender=female` och `segment=1234` för målnoden. Den DSP som ger intryck fyller taggen med information om kön och segment, och besökare som uppfyller de angivna kraven visas som en av de associerade kreatörerna.

**Engagemang:** Ett annonsengagemang (som att titta på en video eller utöka en annons) som resulterar i en konvertering.

<!-- or flexible html5 creative variation? -->
**variant av en flexibel kreativ HTML5-resurs:** En härledning av en flexibel kreativ HTML5-resurs i din [!UICONTROL Creative Libraries] som genereras när du tilldelar den kreativa upplevelsen en upplevelse och ändrar något av standardattributen i upplevelsen.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**visa-igenom:** Ett annonsintryck, eller en sträng med visningar, som resulterar i en konvertering utan att användaren klickar på en annons.
