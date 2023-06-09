---
title: Hur attribueringsregler beräknas
description: Lär dig hur Adobe Advertising beräknar varje typ av attribueringsregel.
source-git-commit: d4237253af7110a3ed02595c466c01359f5601d4
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Hur attribueringsregler beräknas för Adobe Advertising

*Annonsörer med endast konverteringsspårning för Adobe-annonsering*

<!-- Verify statements about cross-device events -->

Attributregeln på annonsörnivå används för att attribuera konverteringsdata - eventuellt i flera annonskanaler - i en serie händelser som leder till en konvertering.

I rapporter, standardvyer och anpassade vyer för annonssökning, sociala medier och handel (sökning, sociala medier och handel) samt (vissa användarroller) simuleringar på portföljnivå för sökning, sociala medier och handel, används den valda regeln endast för vydata, rapportdata eller simuleringsdata. De olika attribueringsreglerna tillämpas enligt följande.

>[!NOTE]
>
>* Attributregler gäller för klick på betalda annonser i alla kanaler och för visningar på displayannonser och sociala annonser. De gäller inte för visningar av betalda sökannonser, som inte kan spåras på eventnivå.
>* Adobe Advertising lagrar alltid följande händelser för varje webbsurfer före en konvertering: a) det första köpet, b) upp till 10 klickningar för varje kanal (sökning, social eller displayannonsering), inklusive det första klicket, och c) upp till 10 visningar. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* I Advertising DSP and Advertising Creative beaktas endast händelsemeddelandet från den valda attribueringsregeln för definitioner för olika enheter.<!-- cross-device attribution via LiveRamp only -->
* I rapporter och hanteringsvyer beror antalet decimaler som visas för ett värde på valutan, men Adobe Advertising lagrar mer exakta värden.

## Senaste händelse (standard)

Attributerar konverteringen till den senaste betalda klickningen i serien i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) eller, om inga betalda klick inträffar, till det sista intrycket i annonsörens [visningsfönster](/help/search-social-commerce/glossary.md#i-j).

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

![Procentsatser för senaste händelseattribuering](/help/search-social-commerce/assets/attribution-percent-last-event.png "Procentsatser för senaste händelseattribuering")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Click1, Click2, Click3, Conversion of 120 USD

Konverteringen tillskrivs Click 3 till ett belopp av 120 USD.

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Conversion of 120 USD

Konverteringen tillskrivs Click 1 till ett belopp av 120 USD.

### Exempel med alla visningar

**Obs!** Endast visningar för webbannonsering och social annonsering kan användas.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Konverteringen tillskrivs Impression 3. Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetod som valts i avsnittet &quot;Konverteringsattribut&quot; i rapportinställningarna:

* Om rapportparametern anger en vägd genomsynlig vikt, används den vikten på genomsynen. Om annonsören till exempel har en genomsynlig vikt på 40 % så tillskrivs Impression 3 120 USD x 40 % = 48 USD, vilket innebär att 48 USD tillskrivs Impression 3.

* Om rapportparametern anger att råvärden ska användas för att visa igenom, används ingen genomsiktsvikt för genomgången och de 120 USD som är de fullständiga tilldelas till Impression 3.

+++

<!-- end examples as collapsible content -->

## Första händelsen

Attributerar konverteringen till det första betalda klicket i serien inom annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) eller, om inga betalda klick inträffar, till det första intrycket i annonsörens [visningsfönster](/help/search-social-commerce/glossary.md#i-j). Den här regeln är endast tillgänglig för händelser på enskilda enheter.

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

![Procentsatser för första händelseattribuering](/help/search-social-commerce/assets/attribution-percent-first-event.png "Procentsatser för första händelseattribuering")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Klicka på 1, klicka på 2, klicka på 3, Konvertera 120 USD

Konverteringen tillskrivs Click 1 till ett belopp av 120 USD.

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Conversion of 120 USD

Konverteringen tillskrivs Click 1 till ett belopp av 120 USD.

### Exempel med alla visningar

**Obs!** Endast visningar för webbannonsering och social annonsering kan användas.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Konverteringen tillskrivs Impression 1. Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetod som valts i avsnittet &quot;(Display Campaigns) Conversion Attribution&quot; i rapportinställningarna:

* Om rapportparametern anger en vägd genomsynlig vikt, används den vikten på genomsynen. Om annonsören till exempel har en genomsiktsvikt på 40 %, tillskrivs alltså 120 x 40 % = 48 USD, vilket innebär att 48 USD tillskrivs Impression 1.

* Om rapportparametern anger att råvärden ska användas för att visa igenom, används ingen genomsiktsvikt för genomgången och de 120 USD som helhet tilldelas till Impression 1.

+++

<!-- end examples as collapsible content -->

## Vikt, första händelse Mer

Attributerar konverteringen till alla händelser i serien som inträffade i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j), men ger mest vikt åt den första händelsen och mindre vikt åt följande händelser. Den här regeln är endast tillgänglig för händelser på enskilda enheter.

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

När konverteringsprocessen omfattar både betalda klick och visningar behandlas dessa olika av olika Adobe-reklamprodukter:

* I Sök, Socialt, &amp; Commerce [visningsåsidosättningsvikt](/help/search-social-commerce/glossary.md#i-j) - som anges i annonsörens intryck åsidosätter viktinställningen och i rapport-, vy- eller anpassade simuleringsparametrar - tillämpas först på avtrycken.

* I DSP ignoreras intrycken och endast klick viktas. DSP tar inte hänsyn till intryck som åsidosätter vikter vid attribuering.

![Vikten av den första händelsen fler attribueringsprocentsatser](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Vikten av den första händelsen fler attribueringsprocentsatser")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Klicka på 1, klicka på 2, klicka på 3, Konvertera 120 USD

Attribution: Klicka på 1 = 60 USD, klicka på 2 = 40 USD, klicka på 3 = 20 USD (totalt 120 USD)

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Endast sökning, sociala medier och handel) Använder standardvärdet 10 % för&quot;Åsidosätt Impression Weight&quot;

Eftersom händelseserien innehöll både visningar och klickningar, gäller intrycket av åsidosatt vikt även för visningar.

Attribution: Impression 1 = 8 USD, Click 1 = 72 USD, Impression 2 = 4 USD, Click 2 = 36 USD (totalt 120 USD)

#### Använda (endast DSP) ingen inledande åsidosättningsvikt eller (endast sökning, sociala medier och handel) en inledande åsidosättningsvikt på 0 %

Eftersom eventserien innehöll både visningar och klickningar ignoreras dessa.

Attribution: Impression 1 = 0 USD, Click 1 = 80 USD, Impression 2 = 0 USD, Click 2 = 40 USD (totalt 120 USD)

### Exempel med alla visningar

**Obs!** Endast visningar för displayannonser kan användas.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetoden - i stället för den inledande vikten - för att fastställa värdet för varje intryck:

* Om rapportparametern anger en vägd genomsiktsvikt, används den vikten på visningsvärdena. Om t.ex. vybredden är 40 %, blir Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (totalt 48 USD)

* Om rapportparametern anger att råvärden ska användas för genomskinlighet, används ingen genomsynlig vikt på intrycket och den fullständiga 120 USD delas mellan de tre avtrycken: Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (totalt 120 USD)

+++

<!-- end examples as collapsible content -->

## Jämn fördelning

>[!NOTE]
>
>Den här regeln är endast tillgänglig för händelser på enskilda enheter.

Attributerar konverteringen på samma sätt för varje händelse i serien som inträffade i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j).

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

När konverteringsprocessen omfattar både betalda klick och visningar behandlas dessa olika av olika Adobe-reklamprodukter:

* I Sök, Socialt, &amp; Commerce [visningsåsidosättningsvikt](/help/search-social-commerce/glossary.md#i-j) - som anges i annonsörens intryck åsidosätter viktinställningen och i rapport-, vy- eller anpassade simuleringsparametrar - tillämpas först på avtrycken.

* I DSP ignoreras intrycken och endast klick viktas. DSP tar inte hänsyn till intryck som åsidosätter vikter vid attribuering.

![Jämn attribueringsprocent](/help/search-social-commerce/assets/attribution-percent-even.png "Jämn attribueringsprocent")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Klicka på 1, klicka på 2, klicka på 3, konvertera 120 USD

Inga avbildningar ledde till konverteringen, så intrycket att åsidosättningsvikten inte kan användas och konverteringen delas lika mellan de tre klickningarna:

Attribution: Klicka på 1 = 40 USD, klicka på 2 = 40 USD, klicka på 3 = 40 USD (totalt 120 USD)

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Endast sökning, sociala medier och handel) Använder standardvärdet 10 % för&quot;Åsidosätt Impression Weight&quot;

Eftersom händelseserien innehöll både visningar och klickningar, gäller intrycket av åsidosatt vikt även för visningar.

Attribution: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (totalt 120 USD)

#### Använda (endast Adobe-DSP) ingen inledande åsidosättningsvikt eller (endast sökning, sociala medier och handel) en inledande åsidosättningsvikt på 0 %

Eftersom eventserien innehöll både visningar och klickningar ignoreras dessa.

Attribution: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (totalt 120 USD)

## Exempel med alla visningar

**Obs!** Endast visningar för displayannonser kan användas.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetoden - i stället för den inledande vikten - för att fastställa värdet för varje intryck:

* Om rapportparametern anger en vägd genomsiktsvikt, används den vikten på visningsvärdena. Om t.ex. vybredden är 40 %, blir Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (totalt 48 USD)

* Om rapportparametern anger att råvärden ska användas för genomskinlighet, används ingen genomsynlig vikt på intrycket och den fullständiga 120 USD delas mellan de tre avtrycken: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (totalt 120 USD)

+++

<!-- end examples as collapsible content -->

## Vikt för senaste händelse Mer

Attributerar konverteringen till alla händelser i serien som inträffade i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j), men ger störst vikt till den senaste händelsen och har en successivt mindre vikt än föregående händelser.

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

När konverteringsprocessen omfattar både betalda klick och visningar hanteras intryck på olika sätt i olika Adobe Advertising-produkter:

* I Sök, Socialt, &amp; Commerce [visningsåsidosättningsvikt](/help/search-social-commerce/glossary.md#i-j) - som anges i annonsörens intryck åsidosätter viktinställningen och i rapport-, vy- eller anpassade simuleringsparametrar - tillämpas först på avtrycken.

* I DSP ignoreras intrycken och endast klick viktas. DSP tar inte hänsyn till intryck som åsidosätter vikter vid attribuering.

![Vikten för den senaste händelsen, fler attribueringsprocent](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Vikten för den senaste händelsen, fler attribueringsprocent")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Klicka på 1, klicka på 2, klicka på 3, Konvertera 120 USD

Attribution: Klicka på 3 = 60 USD, klicka på 2 = 40 USD, klicka på 1 = 20 USD (totalt 120 USD)

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Endast sökning, sociala medier och handel) Använder standardvärdet 10 % för&quot;Åsidosätt Impression Weight&quot;

Eftersom händelseserien innehöll både visningar och klickningar, gäller intrycket av åsidosatt vikt även för visningar.

Attribution: Impression 1 = 4 USD, Click 1 = 36 USD, Impression 2 = 8 USD, Click 2 = 72 USD (totalt 120 USD)

#### Använda (endast DSP) ingen inledande åsidosättningsvikt eller (endast sökning, sociala medier och handel) en inledande åsidosättningsvikt på 0 %

Eftersom eventserien innehöll både visningar och klickningar ignoreras dessa.

Attribution: Impression 1 = 0 USD, Click 1 = 40 USD, Impression 2 = 0 USD, Click 2 = 80 USD (totalt 120 USD)

### Exempel med alla visningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetoden - i stället för den inledande vikten - för att fastställa värdet för varje intryck:

* Om rapportparametern anger en vägd genomsiktsvikt, används den vikten på visningsvärdena. Om t.ex. vybredden är 40 % multiplicerar du varje värde i &quot;Exempel med alla klick&quot; med 40 %: Impression 3 = 24 USD, Impression 2 = 16 USD, Impression 1 = 8 USD (totalt 48 USD)

* Om rapportparametern anger att råvärden ska användas för att visa igenom, delas hela 120-dollardollarn in mellan avtrycken: Impression 3 = 60 USD, Impression 2 = 40 USD, Impression 1 = 20 USD (totalt 120 USD)

+++

<!-- end examples as collapsible content -->

## U-formad

Attributerar konverteringen till alla händelser i serien som inträffade i annonserarens [klicka på uppslagsfönstret](/help/search-social-commerce/glossary.md#c-d) och [visningsfönster](/help/search-social-commerce/glossary.md#i-j), men ger störst vikt till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringsbanan.

När konverteringen föregås av endast visningar betraktas konverteringen som *genomgång*, som vägs antingen enligt annonsörens [inställning för genomskinlig vikt](/help/search-social-commerce/glossary.md#uv) eller - enligt vad som anges - enligt den vybaserade värderingsmetod som anges i rapporten, vyn eller anpassade simuleringsparametrar.

När konverteringsprocessen omfattar både betalda klick och visningar hanteras intryck på olika sätt i olika Adobe Advertising-produkter:

* I Sök, Socialt, &amp; Commerce [visningsåsidosättningsvikt](/help/search-social-commerce/glossary.md#i-j) - som anges i annonsörens intryck åsidosätter viktinställningen och i rapport-, vy- eller anpassade simuleringsparametrar - tillämpas först på avtrycken.

* I DSP ignoreras intrycken och endast klick viktas. DSP tar inte hänsyn till intryck som åsidosätter vikter vid attribuering.

![U-formade attribueringsprocentsatser](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U-formade attribueringsprocentsatser")

<!-- start examples as collapsible content -->

+++Exempel på händelseberäkningar

### Exempel med alla klick

Händelsens sökväg: Klicka på 1, klicka på 2, klicka 3, klicka 4, konvertera 120 USD

Attribution: Klicka på 1 = 36 USD, klicka på 2 = 24 USD, klicka på 3 = 24 USD, klicka på 4 = 36 USD (totalt 120 USD)

### Exempel med både visningar och klickningar

**Obs!** Impressions kan bara användas från annonser på webben och i sociala medier.

Händelsens sökväg: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Endast sökning, sociala medier och handel) Använder standardvärdet 10 % för&quot;Åsidosätt Impression Weight&quot;

Eftersom händelseserien innehöll både visningar och klickningar, gäller intrycket av åsidosatt vikt även för visningar.

Attribution: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (totalt 120 USD)

#### Använder (endast DSP) inget intryck åsidosätter vikt eller (endast sökning, sociala medier och handel) en inledande åsidosättningsvikt på 0 %

Eftersom eventserien innehöll både visningar och klickningar ignoreras dessa.

Attribution: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (totalt 120 USD)

### Exempel med alla visningar

**Obs!** Endast visningar för displayannonser kan användas.

Händelsens sökväg: Impression 1, Impression 2, Impression 3, Impression 4, Conversion of 120 USD

Eftersom konverteringen är en genomskinlig metod används den genomskinliga värderingsmetoden - i stället för den inledande vikten - för att fastställa värdet för varje intryck:

* Om rapportparametern anger en vägd genomsiktsvikt, används den vikten på visningsvärdena. Om t.ex. vybredden är 40 % klickar du på 1 = 14,40 USD, klickar på 2 = 9,60 USD, klickar på 3 = 9,60 USD, klickar på 4 = 14,40 USD (totalt 48 USD)

* Om rapportparametern anger att råvärden ska användas för att visa igenom, delas hela 120-dollardollarn in mellan avtrycken: Klicka på 1 = 36 USD, klicka på 2 = 24 USD, klicka på 3 = 24 USD, klicka på 4 = 36 USD (totalt 120 USD)

+++

<!-- end examples as collapsible content -->
