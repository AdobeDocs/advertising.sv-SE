---
title: Konverteringsspårning för Adobe Analytics
description: Läs om hur du använder Adobe Analytics konverteringsspårning för kampanjer i Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: a6dc9edb12484499069a68222a3007ae08d9dfea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Konverteringsspårning för Adobe Analytics

*Annonsörer med endast integrering mellan Adobe Advertising och Adobe Analytics*

För annonsörer med integrering mellan Adobe Advertising och Adobe Analytics kan Advertising Cloud koppla samman dina annonsklickningar och visningar med de mått för webbplatsengagemang och konvertering som spåras av [!DNL Analytics] när du använder en omdirigering med en token (`ef_id` parameter) i dina klickspårnings-URL:er för dina [budenheter](/help/search-social-commerce/glossary.md#a-b). [!DNL Analytics]-data skickas automatiskt till Advertising Cloud via en daglig feed-fil.

Mer information om integrationen finns i [Översikt över [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/sv/docs/advertising/integrations/analytics/overview){target="_blank"}.

>[!PREREQUISITES]
>
> Tidszoner i annonskontot Search, Social och Commerce, rapportsviterna [!DNL Analytics] och annonsnätverkskontona måste matcha. Om de inte matchar varandra sker dataavvikelser mellan systemen.

## Implementeringsöversikt

1. I [!DNL Analytics] ändrar ditt implementeringsteam för sökning, sociala medier och Commerce följande konfigurationsinställningar för varje rapportserie:

   * Utgångsdatumet för `ef_id` [!DNL eVar] har ändrats så att den matchar annonsörens fönster för klickning för Adobe Advertising.

   * Användar-ID:t för Adobe Advertising.

   * Standardhändelser och anpassade händelser som ska användas för optimering.

1. I Search, Social, &amp; Commerce, ditt implementeringsteam:

   1. Synkroniserar den befintliga kontohierarkin i annonsnätverk till Search, Social och Commerce.

   1. Lägger till omdirigeringar med token `ef_id` som skickas till spårnings-URL:erna och lägger in dem i annonsnätverket.

   I det här steget förutsätts en omdirigering till spårningsservern för Adobe Advertising (förutom för [!DNL Google Ads] och [!DNL Microsoft Advertising] annonser i webbläsare som stöder parallell spårning) och en dynamiskt ifylld &quot;ef_id&quot;-parameter läggs till i URL:en när annonsklicket görs. När parallell spårning används skickas slutanvändarna direkt från annonsen till den slutliga URL:en och URL:en för spårningsmallen (med klickmätning) läses in i bakgrunden.

När integreringen är klar får Search, Social och Commerce automatiskt alla händelsedata på sidan som spåras i [!DNL Analytics] för de rapportsviter som konfigurerats.

>[!MORELIKETHIS]
>
>* [Alternativ för konverteringsspårning](conversion-tracking-about.md)
