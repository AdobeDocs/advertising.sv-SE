---
title: Översikt över att implementera Search, Social och Commerce
description: Lär dig
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Översikt över att implementera Search, Social och Commerce

[!DNL Adobe] eller någon av dess filialer samarbetar med varje annonsör för att lansera sina onlineannonsportföljer och för att spåra eventuella ytterligare annonskampanjer. Efter den första lanseringen ser ytterligare pågående uppgifter till att annonsören fortsätter att uppnå sina mål.

Här följer det allmänna arbetsflödet för att implementera och använda sökningar, sociala medier och handel.

## Inledande start

[!DNL Adobe] och/eller så arbetar ni med följande:

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

   * Synkronisera med kontot genom att a) skapa en motsvarande kontopost i Sök, Socialt och Commerce som innehåller kontoinloggningsuppgifterna och spårningsalternativen och b) ange kontostatusen till aktiverad.

   * Om kontona inte redan innehåller kampanjdata lägger du till kampanjer, annonsgrupper, nyckelord, annonser och placeringar inifrån Search, Social och Commerce eller inifrån annonsnätverket.

      Mer information om hur du ställer in sökkampanjer finns i hjälpkapitlet om&quot;Campaign Management&quot;.

1. Ställ in spårning för alla annonser som du vill att Adobe Advertising ska spåra konverteringar för:

   1. (Om det behövs) Ställ in klickspårning för annonser och eventuellt för nyckelord, [!DNL Google Ads] placeringar, och [!DNL Google Ads] tillägg genom att generera och överföra klickspårnings-URL:er.

      Klickspårnings-URL:er för annonsörer med Adobe Advertising pixelbased conversion tracking service include a redirect to [!DNL Adobe] servrar.

   1. Ställ in konverteringsspårning. Beroende på implementeringen kan detta innebära att du lägger till taggar för konverteringsspårning på lämpliga webbsidor och/eller ställer in en daglig feed-släppning för konverteringsdata som du har samlat in med din egen metod.

      Mer information om hur du ställer in spårning finns i hjälpkapitlet om spårning.

1. Konfigurera integreringar med ytterligare produkter:

   1. (Annonsörer med Adobe Analytics och/eller Adobe Audience Manager) Konfigurera integreringar mellan olika konton så att Adobe Advertising kan utbyta data med dem.

      Se guiden på &quot;[Integrering med Experience Cloud](/help/integrations/home.md).&quot;

   1. (Annonsörer med [!DNL Google Analytics]) Synkronisera konverteringsvärden för en [!DNL Google Analytics] kombination av konto, egenskap och vy för optimering och rapportering.

      Se hjälpunderkapitlet &quot;Admin&quot; > &quot;[Konfigurera datakällor](/help/search-social-commerce/admin/data-sources/data-source-about.md).&quot;

1. Skapa och lansera portfolior:

   1. Skapa portfolior som är konfigurerade för att uppfylla era mål och verksamhetsmål, med lämpliga kampanjer. Implementeringsteamet samlar sedan in och validerar klicknings- och intäktsdata i minst 14 dagar och validerar portföljinställningarna.

      >[!NOTE]
      >
      >Sökning, sociala medier och handel håller fortfarande reda på och rapporterar data för kampanjer som inte är tilldelade till portföljer, men det optimerar inte anbuden för dem.

   1. När det finns tillräckligt med data för att skapa en baslinje kan teamet starta portföljen, vilket gör det möjligt för Search, Social och Commerce att optimera anbud och/eller budgetar för portföljen, baserat på optimeringstyp.
   Mer information om hur du skapar och startar portföljer finns i hjälpen om optimering, som du hittar på [!UICONTROL Help] meny (![Hjälp-menyn](/help/search-social-commerce/assets/help-main-menu.png "Hjälp-menyn")) i det övre högra hörnet på en sida i Sök, Social och Commerce.

1. Övervaka portföljernas prestanda:

   1. Generera annonsinsikter, som är visuella, användbara data om era optimerade och aktiva portfolior.

   1. Ställ in, och eventuellt automatisera, anpassade rapporter för prestandaövervakning.

   Mer information om hur du kör annonsinsikter och skapar rapporter finns i hjälpkapitlet om Insights &amp; Reports.

1. (Valfritt) Konfigurera [datavyer](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) för att visa de data som du vill se.

## Pågående uppgifter

Efter den första starten krävs följande pågående åtgärder. Beroende på dina villkor, antingen [!DNL Adobe], en filial eller annonsören utför följande uppgifter:

* Fortsätt övervaka och analysera resultatet för varje portfölj genom att visa varningar, prestandadata för varje portfölj och dess komponentkampanjer, anpassningsbara rapporter och (vissa roller) simuleringar.

* Justera de olika strategier och inställningar du använder för att hantera portföljuppsättningen, efter behov, baserat på portföljens faktiska och förväntade prestanda och tillväxtmöjligheter:

   * Justera portföljens budget, mål och andra inställningar.

   * Justera konto-/kampanjstrukturerna för att passa förändringar i marknadsföringsstrategin.

   * Lägg till/pausa/ta bort kampanjkomponenter. Detta kan omfatta utökade nyckelordsuppsättningar baserade på söktermsanalys samt testning av kopierings- och landningssidor.

   * Uppdatera strategier för geografisk och webbplatsanpassning baserat på avancerade resultatrapporter.

   * (Valfritt) Lägg till anbudsbegränsningar för enskilda söknyckelord eller för alla nyckelord i en annonsgrupp, kampanj eller portfölj.

   * Lägg till nya portfolior.

Instruktioner om hur du övervakar portföljer och justerar portföljstrategierna finns i hjälpunderkapitlet&quot;Optimering&quot; >&quot;Hantera Portfolio&quot; >&quot;Övervaka och hantera prestanda&quot;, som finns i [!UICONTROL Help] meny (![Hjälp-menyn](/help/search-social-commerce/assets/help-main-menu.png "Hjälp-menyn")) i det övre högra hörnet på en sida i Sök, Social och Commerce.
