---
title: Vanliga frågor
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Frågor och svar xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214 Som standard rapporterar Adobe Analytics alla hämtade händelser i alla rapporter. &quot;[!UICONTROL Unspecified]&quot; representerar händelser för ifyllnad av formulär som inte var kopplade till Adobe Advertising. I Ad Platform-rapporten skulle till exempel organiska konverteringar eller konverteringar som styrs av en e-postkampanj falla under&quot;ospecificerade&quot;.

Du kan använda filtret för att ta bort ospecificerade händelser från rapporter genom att ta bort markeringen med alternativet &quot;Inkludera ospecificerad (ingen)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323 Lägg Analytics-händelsetaggar i samma fläckar som Ad Cloud-pixlarna för att säkerställa att XXX matchar.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

F: Under vår interna säkerhetsrevision flaggades vissa funktioner som säkerhetsproblem som vi aktiverade när vi integrerade Ad Cloud i vår befintliga Adobe Analytics-installation.

Integrationen i fråga är mellan AdCloud och Adobe Audience Manager. Den här funktionen ökar matchningsfrekvensen för besökar-ID mellan AdCloud och Adobe Audience Manager. Det gör det genom att skicka nätverksbegäranden till pagead.l.doubleclick.net, star-mini.c10r.facebook.com och pug88000nf.pubmatic.com för att avgöra om dessa tjänster har ett befintligt ID för besökaren som kan utnyttjas. Detta är de nätverksförfrågningar som har flaggats som en säkerhetsrisk och som förekommer för alla webbplatsbesökare.

Vår revisor ber oss att inaktivera den här funktionen. Vad händer om vi blockerar dessa nätverksförfrågningar?

S: Vi kollade med vår produkt och de nämnde att pixlarna i fråga är avsedda att öka matchningsfrekvenserna för cookies mellan Ad Cloud, specifika lager-/SSP-partners (med avseende på DSP) och AAM.  Om de tas bort kanske kunden ser en viss nivå av minskad matchningsfrekvens mellan AAC/AAM och de lagerpartners som respektive pixlar är avsedda för, men de förväntar sig inte att den ska vara väsentlig.

För Ad Cloud Search ser vi att annonsörens organisation-ID för Experience Cloud är inställt för Mathworks, men vårt produktteam ser inte hur Matthworks är konfigurerat för att aktivera målgrupper i Ad Cloud. Använder du Adobe Audience Manager för att skicka publiker till Ad Cloud Search? Om de inte tas bort påverkas inte det aktuella arbetsflödet. AAM kundtjänst kan hjälpa dig att ta bort dessa pixlar om du inte vill att de ska aktiveras.

