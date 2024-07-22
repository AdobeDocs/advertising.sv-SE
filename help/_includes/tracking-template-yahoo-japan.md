---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Spårningsmallfält för Yahoo! Japan Ads entities

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Valfritt) Spårningsmallen eller spårnings-URL:en, som anger alla icke-landningsdomäner omdirigerar och spårningsparametrar och bäddar även in URL:en för slut-/landningssidan i en parameter. Använd parametern `!{lpurl}` för att ange landningssidans URL. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` som ska inkludera en omdirigering.

Du kan också lägga till omdirigeringar och spårning från tredje part.

För spårning av Adobe Advertising-konvertering, som används när kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload], prefix automatiskt för Sökning, Socialt och Commerce för sin egen omdirigerings- och spårningskod när du sparar posten.

>[!NOTE]
>
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Du kan uppdatera dina spårningsmallar på vilken nivå som helst utan att skicka in dina annonser på nytt för godkännande.
