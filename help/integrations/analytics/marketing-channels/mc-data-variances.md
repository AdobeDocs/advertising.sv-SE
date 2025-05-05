---
title: Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]
description: Lär dig varför kanaldata som spåras av AMO-ID kan variera från kanaldata som spåras av  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Varför kanaldata kan variera mellan Adobe Advertising och [!DNL Marketing Channels]

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

En vanlig fråga från användare som lär sig om integreringen av datauppsättningarna Adobe Advertising och [!DNL Marketing Channels] är&quot;Vad orsakar datavariationen mellan AMO-ID:t och [!DNL Marketing Channels]?&quot; Eller ibland: &quot;Varför bryts data? Jag behöver all statistik för att matcha alla rapporter.&quot; Men diskrepanser visar inte att data är &quot;brutna&quot;, och diskrepanser förväntas och är till och med önskade. Låt oss se varför integreringen har utformats på det här sättet.

De två datauppsättningarna har olika primära användningsområden:

* [!DNL Marketing Channels]: Det primära användningsfallet för [!DNL Marketing Channels] är att jämföra data över flera kanaler med en gemensam attribueringsmodell. Analytikerna kan använda dimensionen [!UICONTROL Marketing Channel] för att få bättre insikter om hur kanalerna interagerar med varandra. Denna insikt kan hjälpa er att fatta beslut på makronivå om hur ni ska investera i varje kanal och kan leda till insikter om hur besökare från varje kanal interagerar med webbplatsen.

  Dimensionen [!DNL Analytics] [!UICONTROL Marketing Channel] är därför konfigurerad att hämta och spåra alla kanaler. [!DNL Marketing Channels] kan även konfigureras för att fånga upp Advertising DSP-visningar och klickningar, och det gör det i relation till andra marknadsföringskanaler.

* Adobe Advertising AMO ID: Det primära användningsområdet för Adobe Advertising AMO ID-data är att mata in de avancerade [!DNL Adobe Sensei]-baserade budgivningsalgoritmerna. Algoritmerna fattar automatiskt tusentals anbudsbeslut på mikronivå varje dag för att maximera annonsutgifterna och uppnå målen för [!DNL DSP]-kampanjen eller [!DNL Search, Social, & Commerce]-portföljen. Ju mer konverteringsdata algoritmerna kan koppla ihop kampanjer, desto bättre kan algoritmerna fatta dessa beslut.

  För att samla in dessa data skickar integreringen [!DNL Analytics for Advertising] AMO-ID:n i Raw-format som kan översättas som klicknings- och genomskinlighetsspårningskoder i Adobe Analytics-dimensionens AMO-ID - som lagras antingen som en anpassad variabel (eVar) eller en reserverad variabel (rVar). Klickningar för andra kanaler är inte inställda i AMO ID-dimensionen, så AMO ID-dimensionen kan inte spåra inmatning från dessa andra kanaler. Resultatet är att AMO-ID:t kvarstår genom [!DNL Marketing Channels] startpunkter.

Mer information om möjliga dataavvikelser mellan data som spåras i Adobe Advertising och data som spåras i [!DNL Analytics] finns i [Förväntade datavarianser mellan  [!DNL Analytics]  och Adobe Advertising](../data-variances.md).

>[!MORELIKETHIS]
>
>* [Förväntade datavarianser mellan [!DNL Analytics] och Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Grundprinciper för [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Adobe Advertising-ID:n för att skapa [!DNL Marketing Channels] bearbetningsregler](mc-ids.md)
>* [Använda [!DNL Analytics Marketing Channels] med Adobe Advertising-data](mc-ac-data.md)
>* [Video: Använder  [!DNL Marketing Channels] för Adobe Advertising-rapportering](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=sv-SE)
