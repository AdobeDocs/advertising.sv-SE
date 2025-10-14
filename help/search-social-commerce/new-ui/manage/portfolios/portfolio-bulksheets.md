---
title: Redigera portföljinställningar gruppvis med hjälp av kalkylbladsfiler
description: Lär dig hur du redigerar inställningarna för flera portföljer med hjälp av en kalkylbladsfil.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Redigera portföljinställningar gruppvis med hjälp av kalkylbladsfiler

*Beta-funktion*

Ett portföljblad är en fil som innehåller portföljinställningar i ett visst format och kan användas för att snabbt granska och ändra inställningarna. Du kan generera (hämta) kalkylblad med inställningar för en eller flera portföljer. Filen hämtas som en [!DNL Excel]-arbetsbok med två kalkylblad (XLSX-format). Arbetsboken innehåller följande:

* Ett skrivskyddat [!UICONTROL Instructions]-kalkylblad med information om hur du redigerar fälten.

* En [!UICONTROL Portfolio Settings Edit]-flik med en rad per inkluderad portfölj. Du kan redigera fälten efter behov, spara filen lokalt och sedan [överföra den redigerade filen](#portfolio-bulksheet-upload) till Sök, Socialt och Commerce. De redigerbara fälten markeras i färg.

## Hämta en kalkylbladsfil med portföljinställningar

1. Markera kryssrutan bredvid varje portfölj som ska ingå i kalkylbladet.

1. Klicka på **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]** i verktygsfältet ovanför datatabellen.

1. Ange namnet på den kalkylbladsfil som ska skapas och klicka sedan på **[!UICONTROL Export Now]**.

   Filen sparas i webbläsarens standardmapp för nedladdningar.

## Överför en kalkylbladsfil med uppdaterade portföljinställningar {#portfolio-bulksheet-upload}

Filen måste vara i XLSX-format.

1. Klicka på **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]** i verktygsfältet ovanför datatabellen. &lt;!— Should be &quot;Import Portfolio Settings&quot; — &quot;Details&quot; (Detaljer) kan vara för vag och föreslå något annat. —>

1. I dialogrutan [!UICONTROL Import Portfolio Details File]:<!-- reword if we change the name of the operation -->

   1. Dra och släpp en fil i rutan eller klicka på **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->för att välja en fil från enheten eller nätverket.

   1. Klicka på **[!UICONTROL Import]**.

Du kan kontrollera överföringsstatus från knappen [!UICONTROL Global Sync Status] (![Global synkroniseringsstatus](/help/search-social-commerce/assets/global-sync-status.png "Global synkroniseringsstatus")) bredvid datumintervallväljaren.<!-- icon similar to Refresh -->. Om någon av ändringarna inte lyckas kan du hämta en felfil som visar vad som misslyckades.

Meddelanden läggs också till i Notiscenter, och du kan öppna meddelandefönstret från ikonen ![Notifications](/help/search-social-commerce/assets/notifications-new.png "Notifications") bredvid knappen [!UICONTROL Global Sync Status] (![Global synkroniseringsstatus](/help/search-social-commerce/assets/global-sync-status.png "Global synkroniseringsstatus")).

## Datakrav för överförda kalkylbladsfiler

Se fliken [!UICONTROL Instructions] i den hämtade kalkylbladsfilen.

Förklaringar av kolumnerna för portföljinställningar på fliken [!UICONTROL Portfolio Settings Edit] finns i Optimeringsguiden, som du når från Sök, Socialt och Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(Nytt användargränssnitt) Redigera en portfölj &#x200B;](portfolio-edit.md)
>* [Skapa en portfölj](portfolio-create.md)
>* [(nytt användargränssnitt) Om portföljer &#x200B;](portfolio-about.md)
