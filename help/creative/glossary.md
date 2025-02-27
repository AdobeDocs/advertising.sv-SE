---
title: Ordlista
description: Se definitioner av nyckeltermer.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Ordlista {#glossary}

*Stängd beta*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**klickfrekvens:** Ett annonsklick som resulterar i en konvertering.

**datapassmål:** Med datapassmål kan annonselement väljas baserat på data som tillhandahålls i realtid av DSP, utgivaren eller partnern. Detta kan inkludera data från tredje part.

<!-- verify this -->I en annonsupplevelse kan varje datapassmål innehålla upp till fem nyckelvärdepar. Du anger nycklarna och minst ett värde i den första målnoden på den nivån, och samma nycklar är tillgängliga för målnoder på samma nivå. Alla nyckelvärdepar läggs till som ett makro till annonstaggen för den här upplevelsen. När annonsen visas är DSP, utgivaren eller partnern ansvarig för att ersätta värdena med data som är specifika för det intrycket. Informationen skickas tillbaka till [!DNL Creative] så att den kan visa en lämplig annonsupplevelse baserat på de regler som definierats i upplevelsen.

Om du till exempel vill rikta en eller flera möjliga användare till tittare som är kvinnliga och som är i segment 1234, konfigurerar du datapassmålen `gender=female` och `segment=1234` för målnoden. Den DSP som visar hur taggen ser ut fyller i den med information om kön och segment, och besökare som uppfyller de angivna kraven visas som en av de associerade kreatörerna.

**Engagemang:** Ett annonsengagemang (som att bläddra igenom en karusell annons eller utöka en annons) som resulterar i en konvertering. Denna typ av händelse är skild från att klicka på annonsen för att nå en landningssida eller en händelse på landningssidan.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**visa-igenom:** Ett annonsintryck, eller en sträng med visningar, som resulterar i en konvertering utan att användaren klickar på en annons.
