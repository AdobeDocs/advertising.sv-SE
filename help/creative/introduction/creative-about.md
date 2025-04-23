---
title: Om Adobe Advertising Creative
description: Läs mer om  [!DNL Creative].
feature: Creative Introduction
source-git-commit: 1ab83cfe82bde4a7b1a32cf3773cdce4738af497
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Om Adobe Advertising Creative 2.0

*Stängd beta*

<!-- verify all and rewrite to include new stuff -->

Som en del av Adobe Advertising är Advertising Creative en självbetjäningsplattform för automatisering av personaliserade annonsupplevelser i realtid och optimering av annonser på elementnivå för det kreativa.

## Egna kreativa bibliotek med återanvändbara kreatörer

Med Creative Libraries kan ni hantera de kreativa verktyg ni kommer att använda i era annonsupplevelser. Du kan skapa flera bibliotek där var och en innehåller enskilda kreatörer och kreativa grupper (kallas *paket*). Ni kommer att lägga till kreativa paket till era annonsupplevelser.

## Regelbaserade upplevelser

Med [!DNL Creative] kan du skapa artiklar med hjälp av en regelbaserad beslutsträdsmodell, som visar en koreografisk sträng med annonser som har anpassats i realtid baserat på vad du vet om din publik, och som följer dina kunder även när de går över till olika webbplatser<!-- verify if that's true without Adobe CDP -->. Berättelserna kan till exempel ändras utifrån kundbeteende, geografi, demografiska förhållanden, återmarknadsföring, position i kundresan och mycket annat.

<!-- Add when available:

## [!DNL Adobe] content and data integrations

[!DNL Creative] has direct integrations with Adobe Experience Manager, allowing you to easily upload the [!DNL Adobe] assets that your design team creates and use them for real-time storyboarding and editing of ad experiences.

You also can use your first-party audience segments from Adobe Audience Manager and Adobe Analytics &mdash; as well as audience segments you create in Advertising Cloud DSP
or retargeting pixels you create using [!DNL Creative] &mdash; as targets for specific creatives in an ad experience.
-->

### Implementering av upplevelser som annonser

När du har skapat en upplevelse kan du skapa en JavaScript- eller iframe-tagg för upplevelsen och implementera taggen som en tredjepartsannons i Advertising DSP eller någon annan DSP.<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level Retargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### Optimering av annonselement

Du kan också tillåta att [!DNL Creative] optimerar annonselementen för alla upplevelser baserat på prestanda - oavsett om du definierar specifika målgruppsmål eller inte - med optimerad, viktad annonrotation, som drivs av Adobe Sensei.

## Återmarknadsföring av pixlar

Du kan skapa återmarknadsföringspixlar som ska användas som mål för kreatörer i en annonsupplevelse. Målen visar endast annonser för användare med angivna attribut som tidigare besökt specifika webbsidor.

## Imponera, klicka och konvertera

[!DNL Creative] spårar automatiskt alla visningar och klickningar efter annonser som har skickats från en upplevelse. Du kan också lägga till URL:er för visningsspårning och klickspårning från tredje part till kreatörer i Creative Libraries samt anpassade URL:er för spårning i en upplevelse.

[!DNL Creative] spårar även konverteringar från hanterade annonser som har skapats från dina annonsupplevelser.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Resultatrapportering

Du kan visa detaljerade resultatrapporter på erfarenhetsnivå i Creative > Experiences.

Du kan också skapa anpassade Creative-rapporter på Rapporter > Anpassade rapporter för att övervaka prestandan på upplevelsenivå i alla dina upplevelser. Om du använder dina [!DNL Creative]-upplevelser som annonser inom DSP-kampanjer finns det resultatdata för dessa annonser i ytterligare anpassade rapporter, precis som data för dina andra DSP-annonser. <!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

Du kan också leverera dina anpassade rapporter till angivna [rapportmål](/help/dsp/reports/report-destinations/report-destination-about.md).

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Om dina kreativa bibliotek](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Om upplevelser i Advertising Creative](/help/creative/experiences/experience-about.md)
