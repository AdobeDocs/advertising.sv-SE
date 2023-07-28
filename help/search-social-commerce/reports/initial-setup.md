---
title: De inledande inställningsaktiviteterna för rapporter
description: Lär dig hur du gör mätvärden tillgängliga i rapporter och hur du automatiserar rapporter.
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# De inledande inställningsaktiviteterna för rapporter

Nya användare bör utföra följande initiala konfigurationsuppgifter:

* Gör transaktionsegenskaperna som Adobe Advertising spårar för en annonsörer [tillgängliga för rapporter och andra vyer](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)och valfritt [ändra namn på egenskapsnamnen](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) som visas i kolumnrubriker för läsbarhet.

  Transaktionsegenskaper är inte tillgängliga för rapporter om du inte uttryckligen gör dem tillgängliga.

  Om du senare börjar spåra en ny transaktionsegenskap måste du upprepa den här uppgiften.

* (Valfritt) Automatisera rapportgenerering:

   * Om du regelbundet vill generera rapportdata för en viss tidsperiod, till exempel en [!UICONTROL Campaign Report] för den senaste veckan eller de senaste 30 dagarna kan du konfigurera [rapportmallar](/help/search-social-commerce/reports/automation/templates/template-about.md) och schemalägga att de ska köras dagligen eller en viss dag i veckan eller månaden. Varje gång rapporten är schemalagd att köras genereras en ny rapport. Du kan meddela e-postadresserna till specifika användare av Sök, Socialt och Handel när rapporten är klar, baserat på [meddelandeinställningar konfigurerade i [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Om du vill visa aktuella, dagliga rapportdata i ett anpassat kalkylblad, med eller utan pivottabeller och eventuella ytterligare kolumner som du behöver utföra ytterligare beräkningar, kan du skapa en daglig [kalkylbladsmatning](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Kalkylbladsflödena uppdateras dagligen med de senaste prestandadata och fortsätter att behålla data för de föregående datumen. Om du vill konfigurera kalkylbladsfeeds måste du först skapa en anpassad kalkylbladsmall i [!DNL Microsoft Excel]. Du kan meddela e-postadresserna till specifika användare av Sök, Sociala och Commerce när en feed-fil är tillgänglig, baserat på [meddelandeinställningar konfigurerade i [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Om du vill få grundläggande och avancerade rapporter på en FTP-plats kan du konfigurera [FTP-åtkomst till grundläggande och avancerade rapporter](/help/search-social-commerce/reports/automation/ftp-reports.md) genom att begära ett FTP-konto och skapa rapportmallar med hjälp av en specifik namnkonvention.

>[!MORELIKETHIS]
>
>* [Rapporter](report-about.md)
>* [Data som används för rapporter](data-used-for-reports.md)
