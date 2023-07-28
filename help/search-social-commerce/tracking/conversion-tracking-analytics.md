---
title: Konverteringsspårning för Adobe Analytics
description: Läs om hur du använder Adobe Analytics konverteringsspårning för kampanjer i Adobe Advertising.
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Konverteringsspårning för Adobe Analytics

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

För annonsörer med integrering mellan Adobe Advertising och Adobe Analytics kan Advertising Cloud koppla samman annonsklickningar och visningar med de mått för webbplatsengagemang och konvertering som spåras av [!DNL Analytics] när du använder en omdirigering med token (`ef_id` parameter) i webbadresserna för klickspårning för [mängdenheter](/help/search-social-commerce/glossary.md#a-b). The [!DNL Analytics] data skickas automatiskt till Advertising Cloud via en daglig matningsfil.

Se &quot;[Översikt [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; om du vill ha mer information om integrationen.

>[!PREREQUISITES]
>
> Tidszoner i annonskontot för sökning, sociala medier och handel, [!DNL Analytics] rapportsviter och annonsnätverkskontona måste matcha. Om de inte matchar finns det dataavvikelser mellan systemen.

## Implementeringsöversikt

1. I [!DNL Analytics]ändrar implementeringsteamet för sökning, sociala medier och handel följande konfigurationsinställningar för varje rapportserie:

   * Giltighetstiden för `ef_id` eVar har ändrats så att den matchar annonsörens fönster för klickning för Adobe Advertising.

   * Användar-ID:t för Adobe Advertising.

   * Standardhändelser och anpassade händelser som ska användas för optimering.

1. I Search, Social, &amp; Commerce kan ditt implementeringsteam:

   1. Synkroniserar den befintliga kontohierarkin i annonsnätverk till Sök, Socialt och Commerce.

   1. Lägger till omdirigeringar med &quot;`ef_id`&quot;-token som skickas till spårnings-URL:er och som skickas till annonsnätverket.

   I det här steget förutsätts en omdirigering till spårningsservern för Adobe Advertising (förutom [!DNL Google Ads] och [!DNL Microsoft Advertising] annonser i webbläsare som stöder parallell spårning) och lägger till en dynamiskt ifylld &quot;ef_id&quot;-parameter i URL:en när annonsklicket görs. När parallell spårning används skickas slutanvändarna direkt från annonsen till den slutliga URL:en och URL:en för spårningsmallen (med klickmätning) läses in i bakgrunden.

När integreringen är klar får Search, Social och Commerce automatiskt alla sidhändelsedata som spåras i [!DNL Analytics] för de rapportsviter som har konfigurerats.

>[!MORELIKETHIS]
>
>* [Alternativ för konverteringsspårning](conversion-tracking-about.md)
