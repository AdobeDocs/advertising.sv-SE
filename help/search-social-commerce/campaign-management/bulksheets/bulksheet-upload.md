---
title: Överför ett kalkylblad eller en korrigerad felfil
description: Lär dig hur du manuellt överför en kalkylbladsfil eller korrigerad felfil för validering av landningssida.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Överför ett kalkylblad eller en korrigerad felfil

Du kan överföra kalkylbladsfiler, korrigerade valideringsfelfiler för landningssidor och andra korrigerade felfiler från enheten eller nätverket för att [stödda annonsnätverk](bulksheet-about.md#bulksheet-functionality-by-network). Alla anpassade kolumner i filen tas bort när du överför filen.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Klicka på i verktygsfältet ovanför datatabellen **[!UICONTROL Upload Bulksheet]**.

1. Ange eller välj information i [[!UICONTROL Upload Bulksheet] inställningar](#bulksheet-upload-settings).

1. Klicka på **[!UICONTROL Apply]**.

När uppgiften börjar visas filen i [!UICONTROL Bulksheets] vy. När filen är klar skickas ett e-postmeddelande med en länk till filen. Beroende på mängden data som kompileras kan e-postmeddelandet ta flera minuter eller mer. Om det inte går att generera filen visas dock en felfil på [!UICONTROL Bulksheets] och ett e-postmeddelande skickas med en länk till felfilen.

>[!NOTE]
>
>Om du skickar kalkylbladsdata till annonsnätverket kan du följa förloppet för filen i [!UICONTROL Progress] kolumn i [!UICONTROL Bulksheets] vy. Det tar längre tid att publicera stora mängder data.

## Överför inställningar för kalkylblad och korrigerade felfiler {#bulksheet-upload-settings}

| Parameter | Beskrivning |
|----|----|
| [!UICONTROL File to Upload] | Den fil som ska överföras. Ange filen antingen genom att ange den fullständiga sökvägen och filnamnet eller genom att klicka på <b>[!UICONTROL Browse]</b> för att hitta filen på enheten eller i nätverket.<br><br>Bulkbladsfiler kan vara upp till 2,5 GB (cirka 2,5 miljoner rader) och måste ha något av följande filtillägg: <i>[!UICONTROL .tsv]</i> (för tabbseparerade värden), <i>[!UICONTROL .txt]</i> (för Unicode-kompatibel ASCII-text), <i>[!UICONTROL .csv]</i> (för kommaavgränsade värden), eller <i>[!UICONTROL .zip]</i> (för komprimerat ZIP-format, som packar upp till en TSV-fil). Filnamnet får inte innehålla följande tecken: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Tips:</b> Använd filer i TSV- eller TXT-format för data som innehåller internationella tecken. |
| [!UICONTROL Single Account] | Anger om filen gäller ett konto: <i>[!UICONTROL Yes]</i> (för ett konto) eller <i>[!UICONTROL No]</i>(för flera konton). |
| [!UICONTROL Account (Search Engine)] | (När filen gäller ett enda konto) Det konto som data ska överföras till. |
| [!UICONTROL Search Engine] | (När filen gäller flera konton) Annonsnätverket som data ska överföras till. |
| [!UICONTROL Scheduling] | När eller om filen ska skickas till det angivna annonsnätverket:<ul><li><i>[!UICONTROL Post to ad network now]</i> (standard): Börjar publicera data direkt.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Börjar publicera data på angivet datum och angiven tid. I morgon kl. 02.00 (2.00). Om du vill ändra datumet anger du ett datum i formatet DD/MM/ÅÅÅÅ eller D/M/ÅÅÅÅ eller klickar på ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") för att öppna kalendern och [välj ett datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Om du vill ändra tiden anger du tiden i formatet HH/MM eller H/M eller väljer en tid (i 15-minutersintervall) i listan.</li><li><i>[!UICONTROL Preview only]:</i> Om du vill överföra filen till Sök, Socialt och Commerce utan att publicera informationen i annonsnätverket kan du fortfarande publicera filen senare. När kalkylbladsfilen är större än 10 MB men mindre än 2 GB är filen i ZIP-format. Du behöver inte packa upp filen för att kunna publicera den.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Om spårningsmallar och landningssidessuffix (för tillämpliga annonsnätverk) ska inkluderas i konton med spårningsmallar, eller mål-URL:er med inbäddade spårningskoder i konton med mål-URL:er, för alla nyckelord, annonser, placeringar, sitelinks och [!DNL Google Ads] produktgrupper i bokföringen: <i>[!UICONTROL Yes]</i> (standard) eller <i>[!UICONTROL No]</i>. Det spelar ingen roll om anbudsenheterna ingår i en portfölj.<br><br>Om du väljer <i>[!UICONTROL Yes]</i>, genereras URL-adresserna enligt parametrarna i [!UICONTROL Tracking Methods] i de relevanta kontoinställningarna eller kampanjinställningarna. Om det finns spårnings-URL:er genereras de inte om om de inte behövs (till exempel om nyckelordsmatchningstypen, annonstexten eller spårningsparametrarna för de relevanta kontona har ändrats).<br><br>Om du väljer <i>[!UICONTROL No]</i>kan du fortfarande generera spårnings-URL:er senare genom att manuellt skicka den överförda filen.<br><br><b>Obs!</b> Om annonsören använder spårning av Adobe Advertising och bas-URL:en har ändrats, måste du generera nya spårnings-URL:er såvida inte kontot har konfigurerats för att automatiskt generera och överföra spårnings-URL:er. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Tillåter budgetändringar av kampanjer i optimerade portföljer baserat på bokförda data. Som standard är det här alternativet inte markerat. Om du väljer det här alternativet gäller alla angivna ändringar av kampanjbudgeten tills optimeringsfunktionen bestämmer att budgeten ska omfördelas (vanligtvis vid nästa budcykel).<br><br><b>Obs!</b> Alla budgetändringar som är ett resultat av bokförda data för kampanjer i icke-optimerade portföljer inträffar när filen publiceras. Förändringarna visas i kampanjhanteringsvyerna nästa dag. |
| [!UICONTROL Enable bidding on ads within portfolios] | När de inkluderade kampanjkomponenterna finns i en optimerad portfölj åsidosätter den här funktionen optimeringsstrategin och tillåter anbudsändringar baserat på data i kalkylbladet fram till ett angivet slutdatum. Om du väljer det här alternativet anger du ett slutdatum mellan 1 och 7 dagar i dialogrutan **[!UICONTROL Hold bulksheet bids until]** fält. |

>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Hämta/skapa en kalkylbladsfil](bulksheet-download.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
>* [Validera landningssidor i kalkylbladsfiler](bulksheet-validate-landing-pages.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)
