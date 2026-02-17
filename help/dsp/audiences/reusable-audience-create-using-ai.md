---
title: Skapa en återanvändbar publik med generativ AI
description: Lär dig hur du skapar återanvändbara målgrupper i Adobe Advertising DSP med hjälp av en AI-assisterad målgruppsagent. Beskriv målgruppen i naturliga språk; agenten föreslår segment från tredje part och bygger målgruppsuttryck som kan användas som mål eller undantag.
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: 63402a5148f5e4dc310b9d2229a9dddd5fe2f113
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Skapa en återanvändbar publik med generativ AI

*Beta-funktion*

*Frågar endast på engelska*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Använd en AI-assisterad målgruppsagent för att generera nya återanvändbara målgrupper med hjälp av alla tredjepartssegment som är tillgängliga för dig, enligt dina angivna krav. Ni kan använda era målgrupper som mål eller uteslutningar för flera praktik.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Funktionen är i betaläge och kan komma att ändras. Se till att det genererade målgruppsuttrycket representerar den målgrupp du vill ha innan du skapar målgruppen och använder det för dina placeringar.

## Skapa en återanvändbar publik med generativ AI

1. Klicka på **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create]** ovanför datatabellen.

1. Ange en unik **[!UICONTROL Audience Name]**.

1. (Valfritt) Avmarkera alternativet till **[!UICONTROL Share with all advertisers in my account]**.

   När ni delar en publik blir målgruppen tillgänglig som mål eller exkludering för alla annonsörer på kontot. De enskilda segmenten i målgruppen är dock bara tillgängliga för användare som segmenten delas med.

1. Klicka på **[!UICONTROL Save]**.

1. Bygg målgruppen:

   För användare med betabehörighet är AI-alternativet standard. Om du vill [sätta ihop målgruppen själv](/help/dsp/audiences/reusable-audience-create.md) klickar du på knappen Växla till manuellt läge längst ned.

   1. Ange en eller flera uppmaningar för att beskriva de målgruppsegenskaper som du vill inkludera och exkludera. Klicka på ![Skicka-fråga](/help/dsp/assets/submit-prompt.png "Skicka-fråga") om du vill skicka varje fråga.

      Mer information finns i [Skrivfrågor](#writing-prompts) och [Bästa metoder för att skapa en publiksammanfattning](#audience-brief-best-practices).

      Efterhand som målgruppsagenten hittar relevanta segment skapas ett målgruppsuttryck baserat på era kriterier. Ni ombeds också godkänna innan ni söker efter matchande segment för att sätta ihop målgruppen.

      Du kan även ignorera begäran och fortsätta att ange ytterligare målgruppskriterier i stället.

   1. När målgruppsagenten presenterar ett målgruppsuttryck som beskriver er målgrupp på ett adekvat sätt, kan du tala om för målgruppsagenten att fortsätta sätta ihop målgruppen.

      Du kan ange &quot;gå&quot;, &quot;OK&quot;, &quot;ja&quot; eller något annat liknande ord.

   1. (Om det behövs) Ange ytterligare villkor. När målgruppsagenten presenterar ett målgruppsuttryck som uppfyller alla dina kriterier, ska du be målgruppsanmälaren att fortsätta sätta ihop målgruppen.

      Om du vill samla målgruppen anger du&quot;gå&quot;,&quot;OK&quot;,&quot;OK&quot;,&quot;Ja&quot; eller något annat liknande ord.

1. När du är nöjd med den sammansatta målgruppen klickar du på **[!UICONTROL Create]** för att skapa den angivna målgruppen.

   >[!NOTE]
   >
   >Du kan inte redigera målgruppen senare med målgruppsagenten. [Redigera i stället målgruppsuttrycket manuellt](/help/dsp/audiences/reusable-audience-edit.md).

## Grunderna för skrivfrågor {#writing-prompts}

### Vad ska en fråga innehålla?

* Använd tydligt och beskrivande språk för att beskriva målgruppen.

   * Du kan ange antingen fullständiga meningar eller bara en sträng med egenskaper. Interpunktion krävs inte utom när det är nödvändigt för tydlighet.

   * Vanligtvis är uppmaningar inte skiftlägeskänsliga.

   * Publiken känner igen de vanligaste synonymerna.

* Var tydlig och ange information om alla målgruppsegenskaper som du vill ta med och alla egenskaper som du vill utesluta. Ju mer information du anger, desto större chans får du att få de resultat som passar dina behov.

* Identifiera platser, enhetstyper och dataleverantörer som ska inkluderas eller exkluderas.

* Ange i stället information för att förfina kriterierna och det genererade målgruppsuttrycket innan du sparar målgruppen.

* Läs om hur du får en fråga genom att experimentera.

  Om frågan inte är tydlig begär målgruppsanmälaren bara en ny fråga så att du kan försöka igen.

  Publiken sparar inte automatiskt ett genererat målgruppsuttryck som en målgrupp. Du kan bara spara en målgrupp genom att klicka på knappen [!UICONTROL Create], som ligger utanför promptområdet, så att du kan ångra ändringar som du inte vill behålla.

Mer information om hur du optimerar uppmaningar för målgrupper finns i [Bästa metoder för att skapa en publiksammanfattning](#audience-brief-best-practices).

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### Vad kan du inte inkludera i en fråga?

* Referenser till befintliga målgruppsuttryck.

* Text på andra språk än engelska.

### Exempel på svar från målgruppsanställda och hur man svarar

När målgruppsagenten behöver ett svar från dig kan du svara med nyckelord i begäran eller med vanliga synonymer.

#### Målgruppsagenten ställer en fråga

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Dina bekräftande svar: &quot;gå vidare&quot;, &quot;okej&quot;, &quot;ok&quot;, &quot;ja&quot; eller liknande ord

Du kan också ignorera begäran och fortsätta att ange ytterligare målgruppskriterier i stället.

#### Audience Agent ber dig välja bland flera alternativ

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Ditt svar: `1`, `proceed`, `2`, `maximum reach` och så vidare.

Du kan också ignorera begäran och fortsätta att ange ytterligare målgruppskriterier i stället.

## Best Practices for Creating an Audience Brief {#audience-brief-best-practices}

En publikrapport är en strategisk beskrivning som definierar målgruppen för en kampanj. En välutformad översikt hjälper DSP målgruppsanställd att identifiera de mest relevanta segmenten för att sätta ihop er målgrupp.

### Grundläggande komponenter i en effektiv målgruppssammanfattning

Ta med så många typer av målgruppsattribut som möjligt från följande lista i rapporten. Specificera vilka attribut du vill utesluta.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demografi**

  Inkluderar attribut som åldersintervall, kön, civilstånd, hushållens sammansättning (familjestorlek, barnens närvaro, hushåll med flera generationer).

* **Socioekonomiska indikatorer**

  Fastställer den finansiella kapaciteten genom hushållsinkomstband (HHI), utbildningsnivå, befattningar/befattningar, anställningsstatus och ägandestatus.

* **Geografiska parametrar**

  Definierar platsomfattningen inklusive land/länder, region (EMEA, APAC, NA), befolkningstäthet (stad/förstad/landsbygden).

* **Intresse och tillhörigheter**

  Identifierar passioner och preferenser som hobbies (sport, konst, utomhusaktiviteter), mediekonsumtionsmönster, varumärkeskänsla och livsstilsaktiviteter (resor, matning, underhållning).

* **Psychografi**

  Fångar tankesätt och värderingar, inklusive ambitioner (statussökning, självförbättring), kärnvärden (hållbarhet, innovation, tradition), personlighetsdrag (risktagare, tidiga användare) och inköpsmotiv.

* **Beteendesignaler**

  observerbara åtgärder, bland annat köpbeteende (kundfrekvens, kanalpreferenser, varumärkeslojalitet), onlinebeteende (webbplatsbesök, innehållsengagemang, sociala medier) och offlinebeteende (butiksbesök, eventnärvaro, medlemskap).

* **Återgivning på marknaden**

  Identifierar inköpsberedskap via produkt-/tjänstekategorier som undersöks, inköpstidslinje (omedelbar, nästan-långsiktig, långsiktig) och relevanta livshändelser som utlöser inköpsbeslut.

* **Livslängd**

  Aktuell fasförståelse som omfattar karriärstadium (studerande, nybörjarnivå, medelkarriär, verkställande, pensionerad), familjefas (nygifta, nya föräldrar, tomma nester) och större livstidsövergångar.

### Exempel på en välstrukturerad publiksammanfattning för en potentiell kampanj

Nedan följer ett exempel på en omfattande publiköversikt för en kampanj som ökar medvetenheten och testversionen av en premiumprenumerationstjänst för måltider:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplicera en återanvändbar publik](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Redigera en återanvändbar målgrupp](/help/dsp/audiences/reusable-audience-edit.md)
>* [Visa information om en återanvändbar målgrupp](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Dela en återanvändbar målgrupp](/help/dsp/audiences/reusable-audience-share.md)
>* [Exportera en återanvändbar målgrupp](/help/dsp/audiences/reusable-audience-export.md)
>* [Kopiera segmentnyckeln för en återanvändbar publik till Urklipp](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Ta bort en återanvändbar publik](/help/dsp/audiences/reusable-audience-delete.md)
