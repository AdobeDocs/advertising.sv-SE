---
title: Översikt över hur man implementerar Search, Social och Commerce
description: Läs mer om det allmänna arbetsflödet för att starta och underhålla en portfölj.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# Översikt över hur man implementerar Search, Social och Commerce

[!DNL Adobe] eller någon av dess filialer arbetar med varje annonsör för att lansera sina onlineannonsportföljer och för att spåra eventuella ytterligare annonskampanjer. Efter den första lanseringen ser ytterligare pågående uppgifter till att annonsören fortsätter att uppnå sina mål.

Här följer det allmänna arbetsflödet för implementering och användning av Search, Social och Commerce.

## Inledande start

[!DNL Adobe] och/eller din byrå arbetar med dig för att göra följande:

1. Utvärdera era övergripande affärsmål och utforma strategier för att uppnå dem:

   1. Identifiera er affärsmodell och era marknadsföringsmål.

   1. Identifiera kraven för konverteringsspårning

   1. Analysera era befintliga onlineannonsstrukturer.

   1. Identifiera mätvärden för portföljoptimering och rapportering.

1. (Administratör- eller kontohanterare) Konfigurera administratörskonton:

   1. Ställ in annonsörens konto. Om en byrå hanterar annonsörens uppgifter måste annonsörens konto kopplas till agenturkontot.

   1. (Om det behövs) Skapa användarkonton för annonsören för att visa och hantera kampanjdata och för att generera rapporter.

   Mer information om hur du konfigurerar konton finns i hjälpkapitlet om&quot;Admin&quot;.

1. Synkronisera med, eller skapa, kampanjer för alla era annonsnätverkskonton:

   * Synkronisera med kontot genom att a) skapa en motsvarande kontopost i Sök, Social och Commerce som innehåller kontoinloggningsuppgifterna och spårningsalternativen och b) ange kontostatusen till aktiverad.

   * Om kontona inte redan innehåller kampanjdata lägger du till kampanjer, annonsgrupper, nyckelord, annonser och placeringar inifrån Search, Social och Commerce eller inifrån annonsnätverket.

     Mer information om hur du ställer in sökkampanjer finns i hjälpkapitlet om kampanjhantering.

1. Ställ in spårning för alla annonser som du vill att Adobe Advertising ska spåra konverteringar för:

   1. (Om det behövs) Konfigurera klickspårning för annonser och eventuellt för nyckelord, [!DNL Google Ads]-placeringar och [!DNL Google Ads]-tillägg genom att generera och överföra klickspårnings-URL:er.

      Klickspårnings-URL:er för annonsörer med Adobe Advertising pixelbaserade konverteringsspårningstjänst innehåller en omdirigering till [!DNL Adobe] servrar.

   1. Ställ in konverteringsspårning. Beroende på implementeringen kan detta innebära att du lägger till taggar för konverteringsspårning på lämpliga webbsidor och/eller ställer in en daglig feed-släppning för konverteringsdata som du har samlat in med din egen metod.

      Mer information om hur du ställer in spårning finns i hjälpkapitlet om spårning.

1. Konfigurera integreringar med ytterligare produkter:

   1. (Advertisers with Adobe Analytics and/or Adobe Audience Manager) Konfigurera integreringar mellan olika konton så att Adobe Advertising kan utbyta data med dem.

      Se guiden om [Integreringar med Experience Cloud](/help/integrations/home.md).

   1. (Annonsörer med [!DNL Google Analytics]) Synkronisera konverteringsvärden för en [!DNL Google Analytics]-konto, -egenskap och -vykombination för optimering och rapportering.

      Se hjälpunderkapitlet &quot;Admin&quot; > &quot;[Konfigurera datakällor](/help/search-social-commerce/admin/data-sources/data-source-about.md)&quot;.

1. Skapa och lansera portfolior:

   1. Skapa portfolior som är konfigurerade för att uppfylla era mål och verksamhetsmål, med lämpliga kampanjer. Implementeringsteamet samlar sedan in och validerar klicknings- och intäktsdata i minst 14 dagar och validerar portföljinställningarna.

      >[!NOTE]
      >
      >Search, Social, &amp; Commerce spårar och rapporterar fortfarande data för kampanjer som inte är tilldelade till portföljer, men det erbjuder ingen optimering för dem.

   1. När det finns tillräckligt med data för att skapa en baslinje kan teamet lansera portföljen, så att Search, Social och Commerce kan optimera anbud och/eller budgetar för portföljen, baserat på optimeringstyp.

   Mer information om hur du konfigurerar och startar portföljer finns i hjälpen för Optimering, som finns på menyn [!UICONTROL Help] (![Hjälp-menyn](/help/search-social-commerce/assets/help-main-menu.png "Hjälp-menyn")) i det övre högra hörnet på en sida i Sök, Socialt och Commerce.

1. Övervaka portföljernas prestanda:

   1. Generera annonsinsikter, som är visuella, användbara data om era optimerade och aktiva portfolior.

   1. Ställ in, och eventuellt automatisera, anpassade rapporter för prestandaövervakning.

   Mer information om hur du kör annonsinsikter och skapar rapporter finns i hjälpkapitlet om Insights &amp; Reports.

1. (Valfritt) Konfigurera dina [prestandadatavyer](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) så att du kan visa de data du vill se.

## Pågående uppgifter

Efter den första starten krävs följande pågående åtgärder. Beroende på dina villkor utför antingen [!DNL Adobe], en filialbyrå eller annonsören följande uppgifter:

* Fortsätt övervaka och analysera resultatet för varje portfölj genom att visa varningar, prestandadata för varje portfölj och dess komponentkampanjer, anpassningsbara rapporter och (vissa roller) simuleringar.

* Justera de olika strategier och inställningar du använder för att hantera portföljuppsättningen, efter behov, baserat på portföljens faktiska och förväntade prestanda och tillväxtmöjligheter:

   * Justera portföljens budget, mål och andra inställningar.

   * Justera konto-/kampanjstrukturerna för att passa förändringar i marknadsföringsstrategin.

   * Lägg till/pausa/ta bort kampanjkomponenter. Detta kan omfatta utökade nyckelordsuppsättningar baserade på söktermsanalys samt testning av kopierings- och landningssidor.

   * Uppdatera strategier för geografisk och webbplatsanpassning baserat på avancerade resultatrapporter.

   * (Valfritt) Lägg till anbudsbegränsningar för enskilda söknyckelord eller för alla nyckelord i en annonsgrupp, kampanj eller portfölj.

   * Lägg till nya portfolior.

Instruktioner om hur du övervakar portföljer och justerar portföljstrategier finns i hjälpunderkapitlet&quot;Optimering&quot; >&quot;Hantera portföljer&quot; >&quot;Övervaka och hantera prestanda&quot;, som finns på [!UICONTROL Help]-menyn (![Hjälp-menyn](/help/search-social-commerce/assets/help-main-menu.png "Hjälp-menyn")) i det övre högra hörnet på en sida i Sök, Socialt och Commerce.
