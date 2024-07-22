---
title: Filkrav för konvertering av feed-filer
description: Referera till kraven för konvertering av feed-filer.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Filkrav för konvertering av feed-filer

Följande krav gäller för filformat, obligatoriska och valfria datafält, filnamn och filöverföringsprotokoll för feed-filer.

## Filformat

Datafilen måste vara i platt text (TXT), kommaavgränsade värden (CSV) eller tabbseparerade värden (TSV). Filen kan bestå av en rubrikrad och datarader med värden som avgränsas med tabbar, kommatecken eller något annat tecken (men inte blanksteg):

* **Rubrikrad:** (Valfritt) Den första raden i filen är en rubrik som anger de obligatoriska fältnamnen (eller kolumnnamnen) i en viss ordning, avgränsade med tabbar eller kommatecken. De kolumnnamn som krävs inkluderar konverteringsmåtten som Adobe Advertising spårar som konverteringar.

* **Datarader:** Varje efterföljande rad innehåller datafält i samma ordning som rubriken och avgränsas med tabbar eller kommatecken. Om den första posten inte är en rubrik, måste varje datarad innehålla alla möjliga fält i en angiven ordning. Värdena för alla ID:n och konverteringsmåtten måste vara alfanumeriska.

  När flera klick på en eller flera annonser leder till en transaktion, måste du bestämma vilket klick-ID och vilket spårnings-ID som transaktionen ska kopplas till. Eftersom ett unikt ID rapporteras för varje transaktion kan du uppdatera enskilda transaktioner.

## Namnkonvention

Filnamnet måste innehålla datumet och vara konsekvent. Om du till exempel använder formatet ÅÅÅÅMMDD.txt måste en fil som skickades den 15 maj 2011 ha namnet 20110515.txt.

## Filöverföringsprotokoll

Skicka filen via SFTP-överföringsprotokollet med port 22. Du måste ange din offentliga nyckel.  Kontoteamet eller implementeringsteamet på Adobe tillhandahåller serverplatsen tillsammans med de autentiseringsuppgifter som krävs för att ditt system ska kunna överföra filerna.

>[!TIP]
>
>Konverteringsdataflöden behandlas flera gånger om dagen. Överför den dagliga matningen så snart som möjligt efter kl. 12.00 lokal tid så att Adobe Advertising kan bearbeta dina data och göra dem tillgängliga i det rapporterande användargränssnittet tidigt på morgonen.

>[!MORELIKETHIS]
>
>* [Datakrav för dataflöden som använder EF-ID:n](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Datakrav för dataflöden med ett transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
