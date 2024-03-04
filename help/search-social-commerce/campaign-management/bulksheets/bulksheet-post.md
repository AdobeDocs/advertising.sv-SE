---
title: Bokför kalkylblad eller korrigerade felfiler
description: Lär dig hur du skickar kalkylbladsfiler till dina annonsnätverk.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Bokför kalkylblad eller korrigerade felfiler

Du kan bokföra befintliga kalkylbladsfiler eller korrigerade felfiler på relevanta konton för [stödda annonsnätverk](bulksheet-about.md#bulksheet-functionality-by-network). Om filen är i ZIP-format behöver du inte packa upp den först.

Bulkbladsfiler och felfiler tas automatiskt bort 30 dagar efter att de har överförts eller genererats.

>[!NOTE]
>Du kan också publicera en kalkylbladsfil eller felfil när du överför filen.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Markera kryssrutan bredvid varje fil som ska skickas.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Post]**.

1. Ange eller välj information i dialogrutan [[!UICONTROL Post Bulksheet] inställningar](#bulksheet-post-settings)och klicka sedan på **[!UICONTROL Post]**.

   Samma inställningar gäller för alla filer som du skickar.

När aktiviteten startar ändras status och schemalagt postdatum för raden i [!UICONTROL Bulksheets] vy. När filen har skickats skickas ett e-postmeddelande med en länk till filen. Beroende på mängden data som kompileras kan e-postmeddelandet ta flera minuter eller mer. Om det inte går att publicera data visas en felfil på [!UICONTROL Bulksheets] och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>* Det tar längre tid att publicera stora mängder data. Du kan följa förloppet för filen i [!UICONTROL Progress] kolumn i [!UICONTROL Bulksheets] vy.
>* Alla bokförda data är underställda nätverkets redaktionella process.
* Du kan avbryta bokföringen innan kalkylbladsfilen har bokförts.

## Bokför inställningar för kalkylblad och korrigerade felfiler {#bulksheet-post-settings}

| Parameter | Beskrivning |
|----|----|
| [!UICONTROL Account (Search Engine)] | Annonsnätverkskontot som data har bokförts för. Om du skickar flera filer samtidigt eller en fil som gäller flera konton är värdet <i>Flera konton har valts</i>.<br><br>Den första bokstaven i annonsnätverksnamnet står inom parentes efter kontonamnet (till exempel&quot;Acme Realty (G)&quot; för en [!DNL Google Ads] konto). |
| [!UICONTROL Scheduling] | När filen ska skickas till det angivna annonsnätverket:<ul><li><i>[!UICONTROL Post to ad network now]</i> (standard): Börjar publicera data direkt.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Börjar publicera data på angivet datum och angiven tid. I morgon kl. 02.00 (2.00). Om du vill ändra datumet anger du ett datum i formatet DD/MM/ÅÅÅÅ eller D/M/ÅÅÅÅ eller klickar på ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") för att öppna kalendern och [välj ett datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Om du vill ändra tiden anger du tiden i formatet HH/MM eller H/M eller väljer en tid (i 15-minutersintervall) i listan.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Om spårningsmallar och landningssidessuffix (för tillämpliga annonsnätverk) ska inkluderas i konton med spårningsmallar, eller mål-URL:er med inbäddade spårningskoder i konton med mål-URL:er, för alla nyckelord, annonser, placeringar, sitelinks och [!DNL Google Ads] produktgrupper i bokföringen: <i>[!UICONTROL Yes]</i> (standard) eller <i>[!UICONTROL No]</i>. Det spelar ingen roll om anbudsenheterna ingår i en portfölj.<br><br>Om du väljer <i>[!UICONTROL Yes]</i>, genereras URL-adresserna enligt parametrarna i [!UICONTROL Tracking Methods] i de relevanta kontoinställningarna eller kampanjinställningarna. Om det finns spårnings-URL:er genereras de inte om om de inte behövs (till exempel om nyckelordsmatchningstypen, annonstexten eller spårningsparametrarna för de relevanta kontona har ändrats).<br><br>Om du väljer <i>[!UICONTROL No]</i>kan du fortfarande generera spårnings-URL:er senare genom att manuellt skicka den överförda filen.<br><br><b>Obs!</b> Om annonsören använder spårning av Adobe Advertising och bas-URL:en har ändrats, måste du generera nya spårnings-URL:er såvida inte kontot har konfigurerats för att automatiskt generera och överföra spårnings-URL:er. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Tillåter budgetändringar av kampanjer i optimerade portföljer baserat på bokförda data. Som standard är det här alternativet inte markerat. Om du väljer det här alternativet gäller alla angivna ändringar av kampanjbudgeten tills optimeringsfunktionen bestämmer att budgeten ska omfördelas (vanligtvis vid nästa budcykel).<br><br><b>Obs!</b> Alla budgetändringar som är ett resultat av bokförda data för kampanjer i icke-optimerade portföljer inträffar när filen publiceras. Förändringarna visas i kampanjhanteringsvyerna nästa dag. |
| [!UICONTROL Enable bidding on ads within portfolios] | När de inkluderade kampanjkomponenterna finns i en optimerad portfölj åsidosätter den här funktionen optimeringsstrategin och tillåter anbudsändringar baserat på data i kalkylbladet fram till ett angivet slutdatum. Om du väljer det här alternativet anger du ett slutdatum mellan 1 och 7 dagar i dialogrutan **[!UICONTROL Hold bulksheet bids until]** fält. |

>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Hämta/skapa en kalkylbladsfil](bulksheet-download.md)
>* [Överför kalkylblad eller korrigerade felfiler](bulksheet-upload.md)
>* [Validera landningssidor i kalkylbladsfiler](bulksheet-validate-landing-pages.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)
