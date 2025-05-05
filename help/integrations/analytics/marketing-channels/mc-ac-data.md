---
title: Använda  [!DNL Marketing Channels]  med data från Adobe Advertising
description: Lär dig hur du använder Adobe Advertising-data i  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Använder [!DNL Analytics Marketing Channels] med Adobe Advertising-data

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

Genom att använda både Adobe Advertising- och [!DNL Analytics Marketing Channels]-rapporter kan du få värdefulla insikter om hur dina digitala medier påverkar webbplatsaktiviteten.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Följande bild visar hur Adobe Advertising och [!DNL Marketing Channels] spårar de enskilda besök som utgör en besökares resa. Adobe Advertising-rapporter i [!DNL Analytics] är begränsade till enbart betalannonsering, sökannonsering, social annonsering och e-handelskanal som handlas via Adobe Advertising, med AMO-ID:t. [!DNL Marketing Channels] spårar dock alla kanaler som har konfigurerats i bearbetningsreglerna för [!DNL Marketing Channels].

![Spåra de enskilda besöken på en besökares resa med Adobe Advertising och [!DNL Marketing Channels]](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Vid det första besöket gick användaren in på webbplatsen via en e-postkampanj, genomförde tio sidvisningar och sedan gick han/hon. Vid det andra besöket gick användaren in på webbplatsen via en displayannons, genomförde tio sidvisningar och sedan gick han/hon. Vid det tredje besöket gick användaren in på webbplatsen via naturlig sökning, utförde fem sidvisningar, genomförde en konvertering på 250 dollar och åt vänster. Observera skillnaden i spårning mellan [!DNL Marketing Channels] och Adobe Advertising. Den enda kanal som Adobe Advertising spårar under den här resan är [!UICONTROL Display]. Adobe Advertising spårar [!UICONTROL Display]-kanalbesöket och attribuerar efterföljande interaktionsdata (till exempel sidvisningar) och konverterar tillbaka till den annonsens påverkan. [!DNL Marketing Channels] ger å andra sidan en fullständig bild av alla kanaler.

Eftersom AMO-ID:t finns kvar under besökarens resa kan du använda AMO-ID-data för att se hur Adobe Advertising påverkar andra marknadsföringskanaler. AMO-ID:t [kvarstår i 60 dagar som standard](/help/integrations/analytics/overview.md), men du kan konfigurera beständigheten efter behov.

## Kombinera data från Adobe Advertising och marknadsföringskanaler för att analysera medieprestanda

Inom [!DNL Analytics] kan du kombinera betald annonsinformation som är kvar i Adobe Advertising och [!DNL Marketing Channels] omfattande besöksdata för att bättre analysera dina medieprestanda så att du bättre kan påverka kundresan.

I följande analys används data från Adobe Advertising för att visa olika versioner av hur en annonsering påverkar webbplatskonverteringen. Alla tre kolumnerna använder samma konverteringsmått, men varje kolumn ger en egen berättelse:

* I kolumn 1 behandlas AMO ID-data som är permanenta under besökarens resa. Kolumn 1 anger att 641-program som startas vid ett tillfälle var länkade med en Adobe Advertising-annons, antingen via en genomskinlig eller klickbar händelse. I den här vyn beaktas ingen annan [!DNL Marketing Channels]-attribuering.

* I datauppsättningen [!DNL Marketing Channels] tilldelas dock 641-programmen Starts till andra marknadsföringskanaler. De sista två kolumnerna tar 641-programmen igång och begränsar data till kanalerna [!UICONTROL Display Click-Through] och [!UICONTROL Display View-Through], vilket visar konverteringarna som inträffar i en senaste pekattribueringsmodell.

![exempel på hur en displayannons påverkar webbplatskonverteringen](/help/integrations/assets/a4adc-mc-display-impact.png)

Du kan gå ett steg längre med den här analysen. Du kan dela upp Adobe Advertising-raden ytterligare via en marknadsföringskanal för att se var konverteringarna i Adobe Advertising är kopplade till 641-programmen börjar. Du vet redan att fem av dessa konverteringar är kopplade till en sista pekskärm genom klickning och 19 är kopplade till en sista pekskärm genom. Det betyder fortfarande att 617 Applications Starts kan tillskrivas andra marknadsföringskanaler. Du kan dra och släppa dimensionen Sista beröringskanalen ovanpå Advertising DSP-radobjektet för att visa kanalattribueringen för resten av programmen Starts och visa visningskanalens påverkan över flera kanaler.

![Så här lägger du till dimensionen Senaste beröringskanal](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Nu kan du se hur de återstående programmen börjar. E-post beviljas för 357 program med senaste beröring som har ett AMO-ID kvar. Med hjälp av den här typen av analyser kan ni se vilken effekt Adobe Advertising har på alla kanaler. Med bara en datauppsättning och attribueringsmodell är den här typen av insikter inte tillgängliga.

![exempel på visningskanalernas påverkan över flera kanaler](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Du kan förbättra analysen ytterligare genom att använda ett Staplingsdiagram som är inställt på&quot;100 % staplade&quot; för att visa trenddata över tiden. Den här visualiseringen gör det enklare att övervaka vilka sista beröringskanaler som påverkas mest av era displaymarknadsföringskampanjer.

![exempel på hur visningskanalerna påverkas av olika kanaler](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundprinciper för [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Adobe Advertising-ID:n för att skapa [!DNL Marketing Channels] bearbetningsregler](mc-ids.md)
>* [Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Använder  [!DNL Marketing Channels] för Adobe Advertising-rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=sv-SE)
>* [Översikt över [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
