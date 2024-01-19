---
title: Hantera och nätverkskonton
description: Lär dig hur du konfigurerar och hanterar kontoinformation för ett annonsnätverkskonto.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '2082'
ht-degree: 0%

---

# Hantera och nätverkskonton

Nedan följer instruktioner om hur du skapar och redigerar och uppdaterar information om nätverkskonton [!DNL oAuth] token för ett konto och inaktivera konton.

Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i &quot;[Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Skapa information om annonsnätverkskonton {#create-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om du vill aktivera synkronisering eller spårning av ett konto måste du skapa en motsvarande kontopost som innehåller kontoinloggningsuppgifterna och spårningsalternativen och med statusen *aktiv*.

>[!NOTE]
>
>* Support finns inte för nya [!DNL Baidu] konton.
>* Om du vill skapa ett verkligt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Klicka på i verktygsfältet ovanför datatabellen ![Skapa](/help/search-social-commerce/assets/add.png "Skapa").

1. Ange [kontoinställningar](#account-settings):

   1. Klicka på annonsnätverkets namn och klicka sedan på **[!UICONTROL Next]**.

   1. I **[!UICONTROL Account Details]** anger du kontoinformationen.

      För annonsnätverk som använder inloggningsauktoriseringstypen &quot;[!UICONTROL oAuth],&quot; tillåter att Search, Social och Commerce får åtkomst till kontot via [OAuth-auktoriseringsprotokoll](https://oauth.net/2/):

      1. Ange **[!UICONTROL Login]** för kontot, ange lösenordet och klicka sedan på **[!UICONTROL Authenticate]**.

         Det bästa sättet är att använda inloggningen för API-åtkomst till kontot. Ange lösenordet när du vill kryptera och spara det, så att kontogruppen på Adobe kan uppdatera token efter behov.

      1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens annonskonto. Det bästa sättet är att använda inloggningsuppgifterna för API-åtkomst till kontot.

      1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om behörighet/åtkomst.

      1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i **[!UICONTROL oAuth Token]** fält.

      1. Ange återstående kontoinformation.

   1. Klicka **[!UICONTROL Set Account Tracking]** och ange spårningsinställningarna.

1. Klicka på **[!UICONTROL Post]**.

   De senaste kostnads- och klickdatan för alla kampanjer på kontot är tillgängliga inom Sök, Sociala och Commerce på cirka 24 timmar. Som standard är data tillgängliga under de senaste 5-10 dagarna, beroende på annonsnätverket. Vid behov kan startteamet dock hämta data för upp till de senaste 60 dagarna.

## Redigera information om nätverkskonton {#edit-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om kontoinloggningsuppgifterna ändras vill du ändra standardspårningsparametrarna för ett konto, eller så vill du aktivera eller inaktivera aktiviteten för ett konto och sedan redigera kontoinformationen.

>[!NOTE]
>
>Om du vill redigera ett faktiskt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Håll markören över kontonamnet och klicka ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer")och sedan markera **[!UICONTROL Edit]**.

1. Redigera [kontoinställningar](#account-settings):

   1. (Valfritt) Redigera kontoinformationen.

   1. (Valfritt) Klicka på **[!UICONTROL Set Account Tracking]** och redigera spårningsinställningarna.

1. Klicka på **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social, &amp; Commerce måste synkronisera nya kontodata med data i annonsnätverket. Detta sker automatiskt en gång om dagen, eller oftare när Sök, Social och Commerce upptäcker ändringar i annonsnätverket.

## Uppdatera åtkomsttoken för autentisering för sökkonton {#refresh-oauth-tokens}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om Sök, Socialt och Commerce kommer åt kontot med [OAuth-auktoriseringsprotokoll](https://oauth.net/2/) och kontoinloggningsuppgifterna ändras, eller om ytterligare åtkomst krävs för att ge stöd åt nya funktioner i Sök, Socialt och Commerce, måste du skaffa en ny åtkomsttoken för kontot.

Kontoteamet på Adobe informerar dig om nya funktioner kräver en ny token.

1. (Om du är inloggad på ett annat konto för samma annonsnätverk i samma webbläsarprogram) Logga ut från något annat konto än annonsörens.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Håll markören över kontonamnet och klicka ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer")och sedan markera **[!UICONTROL Edit]**.

1. Skaffa en ny åtkomsttoken:

   1. Klicka på **[!UICONTROL Get oAuth Token]**.

   1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens annonskonto. Det bästa sättet är att använda inloggningsuppgifterna för API-åtkomst till kontot.

   1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om behörighet/åtkomst.

   1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i **[!UICONTROL oAuth Token]** fält.

1. Klicka på **[!UICONTROL Post]**.

## Aktivera eller inaktivera annonskonton {#enable-disable-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

När du aktiverar ett annonsnätverkskonto synkroniserar Search, Social och Commerce kampanjdata med kontot (när det stöds) och pushar automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer. När du inaktiverar ett annonsnätverkskonto stoppar Search, Social och Commerce all aktivitet på kontot. Data som samlats in medan kontot var aktivt lagras fortfarande, men kampanjhanteringsvyer och rapporter inkluderar inte data för den tidsperiod under vilken kontot inaktiveras. Du kan aktivera kontot igen senare om du vill återuppta aktiviteten med kontot.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Gör något av följande:

   * (Om du vill ändra status för ett konto) Håll markören över kontonamnet och klicka på ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer")och sedan markera **[!UICONTROL Edit]**. Ändra **[!UICONTROL Status]** till *Aktiverad* eller *Handikappade* och klicka sedan på **[!UICONTROL Post]**.

   * (Så här ändrar du status för ett eller flera konton):

      1. Markera kryssrutan bredvid varje konto.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicka på i verktygsfältet ovanför datatabellen ![Ikonen Aktivera](/help/search-social-commerce/assets/activate.png "Ikonen Aktivera") för att aktivera kontot eller ![Inaktivera ikon](/help/search-social-commerce/assets/disable.png "Inaktivera ikon") för att inaktivera kontot.

## Inställningar för annonsnätverkskonto {#account-settings}

>[!NOTE]
>
>Endast kontohanterare för byråer, [!DNL Adobe] kontohanterare och administratörsanvändare kan konfigurera kontoinställningar.

### Kontoinformation

**[!UICONTROL SE Account ID]:** (Alla konton utom [!DNL Naver] och [!DNL Yandex] konton; kan endast redigeras för nya konton) Konto-ID som tilldelats av annonsnätverket.

>[!NOTE]
>
>Konton för annonsnätverkshanterare stöds inte här. Identifiera ett chefskonto för [!DNL Microsoft Advertising] eller [!DNL Yandex]använder du fältet Huvudkonto-ID eller MCC-konto. Till [konfigurera autentiseringsuppgifter för en [!DNL Google Ads] huvudkonto](/help/search-social-commerce/admin/manager-accounts.md), gå till [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Namnet som ska visas för kontot i Sök, Socialt och Commerce.

>[!NOTE]
>
>Om du har en integrering med Search, Social och Commerce-Adobe Analytics och ändrar namnet på sökkontot kontaktar du ditt kontoteam på Adobe så att de kan uppdatera mappningen.

**[!UICONTROL Login Details]: \[Inloggningstyp\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] endast) Om inloggningar ska auktoriseras till kontot med:

* *[!UICONTROL oAuth]* (standard): Så här använder du [[!DNL OAuth] auktoriseringsprotokoll](https://oauth.net/2/).

* *[!UICONTROL Password]:* För att använda klientens lösenord.

För [!DNL Microsoft Advertising] konton, endast [!DNL oAuth]-auktoriserade inloggningar kan användas.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alla annonsnätverk utom [!DNL Naver]) Inloggningsnamnet eller ID:t för att aktivera API-åtkomst till kontot.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-aktiverad och alla andra nätverk förutom [!DNL Meta] och [!DNL Yandex]) Kontots token för att auktorisera inloggningar med [[!DNL OAuth] auktoriseringsprotokoll](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alla annonsnätverk utom [!DNL Naver]) Kontots lösenord. För lösenordsaktiverade konton på [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]och [!DNL Yandex]är det här fältet obligatoriskt. För [!DNL oAuth]-aktiverade konton, det här fältet är valfritt. Använd det när du vill kryptera och spara lösenordet så att kontohanteraren kan uppdatera tokens efter behov.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Yandex] endast konton) Åtkomstnyckeln för det utvecklarkonto som ska användas.

**[!UICONTROL Currency]:** Förkortningen för valutan som används för kontot. Det här fältet kan redigeras för nya [!DNL Naver] konton. För alla andra söknätverk fylls värdet automatiskt i med den valuta som konfigurerats för kontot i annonsnätverket när du sparar posten.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] och [!DNL Microsoft Advertising] endast konton (valfritt) Alla parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information, inklusive alla parametrar som företaget måste spåra.

Exempel: `param1=value1&param2=value2`

Konton som använder klickspårning i Adobe Advertising måste innehålla annonsnätverkets klickningsidentifierare (`msclkid` for [!DNL Microsoft Advertising]; `gclid` för Google) i suffixet. Konton med Adobe Analytics-integrering måste använda parametern AMO ID (med början `s_kwcid`). Om kontot har en AMO ID-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. I annat fall måste du lägga till den manuellt här. Se [obligatoriska suffixformat för [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Det här fältet uppdateras inte av [!UICONTROL Auto Upload] spårningsinställning.
>* Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

**Tidszon:** (Alla annonsnätverk utom [!DNL Baidu] och [!DNL Yahoo! Display Network]) Annonsörens tidszon. Det här fältet är redigerbart och valfritt för nya [!DNL Naver] konton. För alla andra söknätverk fylls värdet automatiskt i med den tidszon som konfigurerats för annonserarens konto Sök, Sociala och Commerce när du har sparat posten.

**Status:** Kontostatus i Sök, Socialt och Commerce:

* *Aktiverad:* Sökning, sociala medier och handel synkroniserar kampanjdata med kontot (när det stöds) och pushar för automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer.
* *Inaktiverad:* Sök, Socialt och Commerce stoppar all aktivitet på kontot. Data som samlats in medan kontot var aktivt lagras fortfarande, men kampanjhanteringsvyer och rapporter inkluderar inte data för den tidsperiod under vilken kontot pausas. Du kan återaktivera kontot senare om du vill återuppta aktiviteten med kontot.

**Spårningsmall** - ([!DNL Google Ads], [!DNL Microsoft Advertising]och [!DNL Yahoo! Japan Ads] endast konton (valfritt) Standardspårningsmallen för kontot, som anger alla omdirigeringar och spårningsparametrar utanför landningsdomänen och även bäddar in URL:en för sista sidan/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` för att inkludera en omdirigering.

* Så här bäddar du in den slutliga URL:en:

   * ([!DNL Google Ads] och [!DNL Microsoft Advertising] (endast) En lista med parametrar som anger de slutliga URL:erna i spårningsmallar finns i[!DNL Microsoft Advertising] endast) [[!DNL Microsoft Advertising] dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) eller ([!DNL Google Ads] endast) parametrarna &quot;Endast spårningsmall&quot; i avsnittet &quot;Tillgängligt&quot; [!DNL ValueTrack] Parametrar&quot; i [[!DNL Google Ads] dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] endast) Använd parametern `!{lpurl}` Ange landningssidans URL.

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel `{lpurl}?matchtype={matchtype}&device={device}`.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

* När kampanjinställningarna innehåller &quot;[!UICONTROL EF Redirect]och &quot;[!UICONTROL Auto Upload],&quot; Sökning, sociala medier och handel prefixar automatiskt sin egen omdirigerings- och spårningskod när du sparar posten.

>[!NOTE]
>
>* För [!DNL Google Ads]bör du undvika att använda makron, som inte ersätts med klick från källor som möjliggör parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Om du uppdaterar en spårningsmall på annons-, sitelink- eller nyckelordsnivå skickas relevanta annonser om för granskning. Du kan uppdatera dina spårningsmallar på konto-, kampanj- eller annonsgruppsnivå utan att skicka in dina annonser på nytt för godkännande.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] endast konton) ID:t för ett agenturkonto/förvaltningskonto som är associerat med kontot.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] endast konton (valfritt) En byrå/ett förvaltningskonto som är associerat med kontot. Om du vill ta bort en befintlig association väljer du &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] endast konton) Den utvecklartoken som ska användas för kontot. Samma token används för alla [!DNL Yandex] konton.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] konton med inställningen Delat konto inaktiverad endast; valfritt) Det numeriska ID:t för kampanjen som ska användas för att betala för alla annonskampanjer i kontot.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] konton med inställningen Delat konto inaktiverad endast; valfritt) Den utvecklartoken som ska användas för finansrelaterade API-anrop, t.ex. för omfördelning av pengar från plånboken mellan annonserarens kampanjer efter behov för portföljoptimering.

### Kontouppföljning

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (för [!UICONTROL EF Redirect] endast) Ej implementerat

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid-format** - (Befintlig [!DNL Google Ads] konton för annonsörer med integrering mellan Adobe Advertising och Adobe Analytics och för vilka AMO-ID (s_kwcid) inte redan har migrerats)

Det här kontot använder det äldre formatet för spårningskoden för AMO ID, som gör att Adobe Advertising kan dela data om kontot med Adobe Analytics. The [senaste formatet](/help/integrations/analytics/ids.md#amo-id-formats) innehåller parametrar för kampanj-ID och annonsgrupp-ID, som behövs för att kunna rapportera korrekt på kampanjnivå och annonsgruppsnivå för [!DNL Google Ads] max-prestandakampanjer och utkast och experimentera med kampanjer i Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Om det här kontot behöver rapportera på kampanj- och annonsgruppsnivå klickar du på [!UICONTROL Edit] (blyertspenna) och sedan **[!UICONTROL Migrate to new s_kwcid format]** för att byta till det nya formatet. För konton som inte innehåller de här kampanjtyperna är migrering till det nya formatet valfritt, men rekommenderas.

Fullständiga anvisningar finns i &quot;[Uppdatera spårningskoden för AMO ID för en [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Namn på rapportsvit** - (For EF Redirect with token only; publishers with an Adobe Advertising-Adobe Analytics integration; optional) One or more Analytics report suites to which Search, Social, &amp; Commerce sending data it samlar in från annonsnätverket, inklusive entitetsklassificeringar och klickdata för kontot. Den här funktionen är bara tillgänglig för annonsnätverk som stöds.

För att data ska kunna visas i rapportsviterna måste antingen (a) funktionen för AMO ID på serversidan konfigureras för kontot eller (b) inställningen på annonsörnivå måste vara &quot;[!UICONTROL Enable tracking for SAINT feeds]måste vara aktiverat. Dessutom måste annonsörens Analytics-konto vara konfigurerat för att ta emot data från Search, Social och Commerce. Kontakta kontohanteraren för Adobe om du vill ha mer information.

>[!MORELIKETHIS]
>
>* [Om och nätverkskonton](ad-network-account-about.md)
>* [Hantera säljcenterkonton](merchant-account-manage.md)
>* [Uppdatera s_kwcid-spårningskoden för en [!DNL Google Ads] konto](update-amo-id-google.md)
