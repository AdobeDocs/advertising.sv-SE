---
title: FTP-åtkomst till rapporter
description: Lär dig hur du tar emot rapporter på en skrivskyddad FTP-plats.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# FTP-åtkomst till rapporter

Du kan också ta emot rapporter på en skrivskyddad FTP-plats, där du kan hämta filerna för ytterligare automatiserade processer (till exempel för att analysera data med ett annat program). Alla grundläggande rapporter utom [!UICONTROL Search Engine Account Report] och alla avancerade rapporter kan levereras till en FTP-plats som zippade TSV-filer (standard) eller CSV-filer med filnamnstillägget ZIP. Alla TSV- eller CSV-filhuvuden inkluderas och kan inte undertryckas.

FTP-åtkomst till rapporter kräver åtkomst till ett visst FTP-konto, och du måste skapa rapportmallar med en viss namnkonvention och ett schema.

## Konfigurera ett FTP-konto för åtkomst till rapporter

* Kontakta kontoteamet på Adobe för att skapa ett FTP-konto för rapportåtkomst.

  Teamet förser dig med ditt användarnamn och lösenord.

## Ställ in rapportmallar för FTP-leverans

Skapa en [rapportmall](templates/template-create.md) med följande namnkonventioner och scheman.

>[!NOTE]
>
>Alla avancerade rapporter och alla grundläggande rapporter utom [!UICONTROL Search Engine Account Report] kan levereras till en FTP-plats.

1. I rapportmallen tar du med följande information var som helst i mallnamnet:

   * `FTP` (med versaler).

   * (Valfritt) Tre systemdatum, med följande skiftlägeskänsliga syntax, inklusive hakparenteser:

      * `[TODAY]` — Inkludera datum, timme och minut då rapporten kördes. Eftersom det här omfattar exakt tid kan samma mall köras flera gånger dagligen utan att den föregående rapporten skrivs över.

      * `[SDATE]` — Inkludera rapportens startdatum i datumintervallet.

      * `[EDATE]` — Inkludera slutdatumet för rapportens datumintervall.

   * (Valfritt) `[CSV]` (med versaler och omslutna av hakparenteser) om du vill skapa filer i CSV-format i stället för som standard-TSV-format.

   Exempel: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` skulle skapa en fil som 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Schemalägg rapporten så att den körs vid en viss tidpunkt.

   Rapporterna skickas till FTP-kontot inom en timme efter att de har slutförts.

>[!NOTE]
>
>* Om du vill skicka slutförda rapporter via e-post anger du bara adresserna till alla e-postmottagare när du genererar rapporten eller mallen.
>* Rapporterna körs enligt angivna scheman och levereras till FTP-kontot inom en timme efter att de har slutförts.

## Få åtkomst till rapporter i en FTP-databas

Anslut till någon av följande FTP-värdar med inloggningen för ditt FTP-konto (`amo<userID>rpt`, t.ex. amo1234rpt) och antingen ett lösenord eller en privat anslutningsnyckel om en sådan har konfigurerats:

* Internationella kunder: `ftp3.adobe.net`
* Kunder i USA: `ftp5.adobe.net`

>[!NOTE]
>
>Rapportdatabasen är skrivskyddad och rensas var 15:e dag.


>[!MORELIKETHIS]
>
>* [Skapa en rapportmall](/help/search-social-commerce/reports/automation/templates/template-create.md)
