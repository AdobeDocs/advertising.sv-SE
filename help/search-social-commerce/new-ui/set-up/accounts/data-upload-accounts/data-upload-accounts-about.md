---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Om överföring av kontodata för rapportering och simuleringar

<!-- Move all related files into one page? -->

Om du använder annonsnätverk online som inte har stöd för API i Search, Social och Commerce kan du överföra kampanjinnehåll och offlinekostnader, klicka och konverteringsdata för ett konto för rapportering och prestandamuleringar. Annonsörer med [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md) kan också visa data för sina konton i Adobe Analytics.

Den här funktionen är tillgänglig för annonsnätverk som följer den standardiserade kampanjstrukturen på tre nivåer (kampanj, annonsgrupp eller annonsuppsättning samt budenhet (annons eller nyckelord)). För Adobe DSP är funktionen tillgänglig för paket och de placeringar som tilldelats ett paket, men inte för kampanjer eller placeringar med placeringsnivåpaketering.

Det finns support direkt för följande nätverk:<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

Klickspårning för sökning, sociala medier och Commerce samt Adobe Advertising-konverteringsspårning stöds inte med den här funktionen.

## Funktioner som finns i Search, Social och Commerce

* Spårning och rapportering:

   * Skrivskyddade kampanjkomponenter ned till anbudsenhetsnivå inom kampanjhanteringsvyer.

   * Prestandadata ned till annonsgruppnivån <!-- verify the entity level --> i kampanjhanteringsvyer och anpassade rapporter. Annonsörer med [!DNL Adobe Analytics for Advertising]) kan dessutom hämta prestandadata ner till annonsgruppsnivån <!-- verify the entity level --> i Adobe Analytics rapportsviter som angetts för annonsören.&lt;!— Verifiera om datatyperna är begränsade - kostnad, klickning, displayintryck, intäkt? —>

* Prestandasimuleringar när du lägger till kampanjer i en portfölj.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social och Commerce optimerar ingenting, och lägger inte ens bud, för den här typen av kampanjer i en portfolio.

## Arbetsflöde för att konfigurera offlinekonton

<!-- subtitle wording? -->

1. [Konfigurera en dummy-kontopost](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Skapa en datafil för ett enskilt konto <!--  in what file format? -->, inklusive status på dagnivå för kampanjer, annonsgrupper och annonser.

Data måste uppfylla datakraven för annonsnätverket, så datafälten för varje enhet kan variera beroende på annonsnätverk.

1. &#x200B;<!-- For all ad networks (excluding DSP), -->Överför initiala data för ett enskilt konto på något av följande sätt:

* Överför en fil manuellt från enheten eller nätverket.

* Överför data till en mapp som har tilldelats av Search, Social och Commerce i en [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])-bucket.

  >[!PREREQUISITES]
  >
  >* Kontakta Adobe Account Team för att aktivera kontodataöverföringar för ert Search-, Social- och Commerce-annonskonto. Teamet kommer att underlätta skapandet av en organisationsspecifik mapp i en [!DNL S3]-bucket, och de kommer att meddela dig när den är klar.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Hämta molnlagringssökvägen [!DNL S3], ID för åtkomstnyckel och hemlig åtkomstnyckel för ditt konto. Samma åtkomstnyckel-ID och hemlig åtkomstnyckel används för alla organisationens <!-- naming convention?-->-konton för dataöverföring.

1. Fortsätt att överföra nya datafiler dagligen.

1. När du har överfört data i 30 dagar kan du lägga till kampanjer i <!--what type? how should we refer to them? -->-portföljer och generera simuleringar.

Du kan [visa en logg över varje dataöverföring](upload-log.md) för att se dess status. Om du initierar en överföring men överföringen inte lyckas helt får du dessutom ett felmeddelande via [Notiscenter](/help/search-social-commerce/notifications/notification-about.md), baserat på dina meddelandeinställningar.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [Om överföring av kontodata för rapportering och simuleringar](data-upload-accounts-about.md)
>* [Överför kontodata till en [!DNL Amazon] [!DNL S3] bucket](upload-data-from-s3-bucket.md)
>* [Överför kontodata manuellt](upload-data-manually.md)
>* [Visa en logg över överförda kontodatafiler](upload-log.md)
>* [Hantera och nätverkskonton för dataöverföringar](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
