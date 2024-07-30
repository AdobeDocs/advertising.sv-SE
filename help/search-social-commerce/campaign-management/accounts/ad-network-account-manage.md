---
title: Hantera och nätverkskonton
description: Lär dig hur du konfigurerar och hanterar kontoinformation för ett annonsnätverkskonto.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 68efad8ad3bc2985ac75a0f9437a2eafb194e4b6
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Hantera och nätverkskonton

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Nedan följer instruktioner om hur du skapar och redigerar information om nätverkskonton, uppdaterar token [!DNL oAuth] för ett konto och inaktiverar konton.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).

## Skapa information om annonsnätverkskonton {#create-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om du vill aktivera synkronisering eller spårning av ett konto måste du skapa en motsvarande kontopost som innehåller kontoinloggningsuppgifterna och spårningsalternativen och med statusen *aktiv*.

>[!NOTE]
>
>* Det finns ingen support för nya [!DNL Baidu]-konton.
>* Om du vill skapa ett verkligt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** på undermenyn.

1. Klicka på ![Skapa](/help/search-social-commerce/assets/add.png "Skapa") i verktygsfältet ovanför datatabellen.

1. Ange [kontoinställningarna](#account-settings):

   1. Klicka på annonsnätverkets namn och sedan på **[!UICONTROL Next]**.

   1. Ange kontoinformationen i avsnittet **[!UICONTROL Account Details]**.

      För annonsnätverk som använder inloggningsauktoriseringstypen [!UICONTROL oAuth] tillåter du Search, Social och Commerce att få åtkomst till kontot via [OAuth-auktoriseringsprotokollet](https://oauth.net/2/):

      1. Ange värdet **[!UICONTROL Login]** för kontot, ange lösenordet om du vill och klicka sedan på **[!UICONTROL Authenticate]**.

         Det bästa sättet är att använda inloggningen för API-åtkomst till kontot. Ange lösenordet när du vill kryptera och spara det, så att kontogruppen på Adobe kan uppdatera token efter behov.

      1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens annonskonto. Det bästa sättet är att använda inloggningsuppgifterna för API-åtkomst till kontot.

      1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om behörighet/åtkomst.

      1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i fältet **[!UICONTROL oAuth Token]**.

      1. Ange återstående kontoinformation.

   1. Klicka på **[!UICONTROL Set Account Tracking]** och ange spårningsinställningarna.

1. Klicka på **[!UICONTROL Post]**.

   De senaste kostnads- och klickuppgifterna för alla kampanjer på kontot finns tillgängliga i Search, Social och Commerce på cirka 24 timmar. Som standard är data tillgängliga under de senaste 5-10 dagarna, beroende på annonsnätverket. Vid behov kan startteamet dock hämta data för upp till de senaste 60 dagarna.

## Redigera information om nätverkskonton {#edit-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om kontoinloggningsuppgifterna ändras vill du ändra standardspårningsparametrarna för ett konto, eller så vill du aktivera eller inaktivera aktiviteten för ett konto och sedan redigera kontoinformationen.

>[!NOTE]
>
>Om du vill redigera ett faktiskt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** på undermenyn.

1. Håll markören över kontonamnet, klicka på ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer") och välj sedan **[!UICONTROL Edit]**.

1. Redigera [kontoinställningarna](#account-settings):

   1. (Valfritt) Redigera kontoinformationen.

   1. (Valfritt) Klicka på **[!UICONTROL Set Account Tracking]** och redigera spårningsinställningarna.

1. Klicka på **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social och Commerce måste synkronisera de nya kontodata med de som finns i annonsnätverket. Detta sker automatiskt en gång om dagen, eller oftare när Search, Social och Commerce upptäcker ändringar i annonsnätverket.

## Uppdatera åtkomsttoken för autentisering för sökkonton {#refresh-oauth-tokens}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

Om Search, Social och Commerce använder kontot med hjälp av [OAuth-auktoriseringsprotokollet](https://oauth.net/2/) och kontoinloggningsuppgifterna ändras, eller om ytterligare åtkomst krävs för att ge stöd för nya funktioner i Search, Social och Commerce, måste du skaffa en ny åtkomsttoken för kontot.

Kontoteamet på Adobe informerar dig om nya funktioner kräver en ny token.

1. (Om du är inloggad på ett annat konto för samma annonsnätverk i samma webbläsarprogram) Logga ut från något annat konto än annonsörens.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** på undermenyn.

1. Håll markören över kontonamnet, klicka på ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer") och välj sedan **[!UICONTROL Edit]**.

1. Skaffa en ny åtkomsttoken:

   1. Klicka på **[!UICONTROL Get oAuth Token]**.

   1. (Om du inte är inloggad på annonsörens konto) Logga in på annonsörens annonskonto. Det bästa sättet är att använda inloggningsuppgifterna för API-åtkomst till kontot.

   1. Klicka på knappen för att bekräfta behörighet på skärmen för begäran om behörighet/åtkomst.

   1. Kopiera autentiseringssträngen i popup-fönstret som öppnas och klistra in strängen i fältet **[!UICONTROL oAuth Token]**.

1. Klicka på **[!UICONTROL Post]**.

## Aktivera eller inaktivera annonskonton {#enable-disable-account}

*Endast kontohanterare, kontohanterare för Adobe och administratörsanvändarroller*

När du aktiverar ett annonsnätverkskonto synkroniserar Search, Social och Commerce kampanjdata med kontot (när det stöds) och pushar för automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer. När du inaktiverar ett annonsnätverkskonto stoppar Search, Social och Commerce all aktivitet på kontot. Data som samlats in medan kontot var aktivt lagras fortfarande, men kampanjhanteringsvyer och rapporter inkluderar inte data för den tidsperiod under vilken kontot inaktiveras. Du kan aktivera kontot igen senare om du vill återuppta aktiviteten med kontot.

1. Klicka på **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** på huvudmenyn. Klicka på **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** på undermenyn.

1. Gör något av följande:

   * (Om du vill ändra status för ett konto) Håll markören över kontonamnet, klicka på ![Mer](/help/search-social-commerce/assets/more-filters.png "Mer") och välj sedan **[!UICONTROL Edit]**. Ändra **[!UICONTROL Status]** till *Aktiverad* eller *Inaktiverad* och klicka sedan på **[!UICONTROL Post]**.

   * (Så här ändrar du status för ett eller flera konton):

      1. Markera kryssrutan bredvid varje konto.

         Tips om hur du markerar flera rader finns i &quot;[Markera flera rader](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicka på ikonen ![Aktivera](/help/search-social-commerce/assets/activate.png "Aktivera ") i verktygsfältet ovanför datatabellen om du vill aktivera kontot eller på ![Inaktivera ikon](/help/search-social-commerce/assets/disable.png "Inaktivera ikon") om du vill inaktivera kontot.

## Inställningar för annonsnätverkskonto {#account-settings}

>[!NOTE]
>
>Endast kontohanterare, kontohanterare för [!DNL Adobe] och administratörsanvändare kan konfigurera kontoinställningar.

### Kontoinformation

**[!UICONTROL SE Account ID]:** (Alla konton utom för [!DNL Naver]- och [!DNL Yandex]-konton, kan endast redigeras för nya konton) Det konto-ID som tilldelats av annonsnätverket.

>[!NOTE]
>
>Konton för annonsnätverkshanterare stöds inte här. Om du vill identifiera ett hanterarkonto för [!DNL Microsoft Advertising] eller [!DNL Yandex] använder du fältet Huvudkonto-ID eller MCC-konto. Om du vill [konfigurera autentiseringsuppgifter för ett [!DNL Google Ads] hanterarkonto](/help/search-social-commerce/admin/manager-accounts.md) går du till [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Namnet som ska visas för kontot i Sök, Socialt och Commerce.

>[!NOTE]
>
>Om du har en integrering med Search, Social och Commerce-Adobe Analytics och ändrar namnet på sökkontot kontaktar du ditt kontoteam på Adobe så att de kan uppdatera mappningen.

**[!UICONTROL Login Details]: \[Inloggningstyp\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] endast) Om inloggningar ska auktoriseras för kontot med:

* *[!UICONTROL oAuth]* (standardvärdet): Använder [[!DNL OAuth] auktoriseringsprotokollet](https://oauth.net/2/).

* *[!UICONTROL Password]:* Använda klientens lösenord.

För [!DNL Microsoft Advertising]-konton kan bara [!DNL oAuth]-auktoriserade inloggningar användas.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alla annonsnätverk utom [!DNL Naver]) Inloggningsnamnet eller ID:t som aktiverar API-åtkomst till kontot.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-aktiverad och alla andra nätverk förutom [!DNL Meta] och [!DNL Yandex]) Kontots token för att auktorisera inloggningar med [[!DNL OAuth] auktoriseringsprotokollet](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alla annonsnätverk förutom [!DNL Naver]) Lösenordet för kontot. För lösenordsaktiverade konton på [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] och [!DNL Yandex] är det här fältet obligatoriskt. För [!DNL oAuth]-aktiverade konton är det här fältet valfritt. Använd det när du vill kryptera och spara lösenordet så att kontohanteraren kan uppdatera tokens efter behov.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Yandex] endast konton) Åtkomstnyckeln för det utvecklarkonto som ska användas.

**[!UICONTROL Currency]:** Förkortningen för valutan som används för kontot. Det här fältet kan redigeras för nya [!DNL Naver]-konton. För alla andra söknätverk fylls värdet automatiskt i med den valuta som konfigurerats för kontot i annonsnätverket när du sparar posten.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] och [!DNL Microsoft Advertising] enbart konton; valfritt) Alla parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information, inklusive alla parametrar som företaget måste spåra.

Exempel: `param1=value1&param2=value2`

Konton som använder klickspårning i Adobe Advertising måste inkludera annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]; `gclid` för Google) i suffixet. Konton med en Adobe Analytics-integrering måste använda parametern AMO ID (med början från `s_kwcid`). Om kontot har en AMO ID-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. I annat fall måste du lägga till den manuellt här. Se de [suffixformat som krävs för  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Det här fältet uppdateras inte av spårningsinställningen [!UICONTROL Auto Upload].
>* Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

**Tidszon:** (Alla annonsnätverk förutom [!DNL Baidu] och [!DNL Yahoo! Display Network]) Annonsörens tidszon. Det här fältet är redigerbart och valfritt för nya [!DNL Naver]-konton. För alla andra söknätverk fylls värdet automatiskt i med den tidszon som konfigurerats för annonserarens konto Sök, Socialt och Commerce när du har sparat posten.

**Status:** Kontostatus i Sök, Social och Commerce:

* *Aktiverad:* Sökning, socialt arbete och Commerce synkroniserar kampanjdata med kontot (när det stöds) och pushar för automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer.
* *Inaktiverad:* Sök, social och Commerce stoppar all aktivitet på kontot. Data som samlats in medan kontot var aktivt lagras fortfarande, men kampanjhanteringsvyer och rapporter inkluderar inte data för den tidsperiod under vilken kontot pausas. Du kan återaktivera kontot senare om du vill återuppta aktiviteten med kontot.

**Spårningsmall** - ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] endast konton; valfritt) Standardspårningsmallen för kontot, som anger alla omdirigeringar och spårningsparametrar utanför domänen och bäddar även in URL:en för sista sidan/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` som ska inkludera en omdirigering.

* Så här bäddar du in den slutliga URL:en:

   * ([!DNL Google Ads] och endast [!DNL Microsoft Advertising]) En lista med parametrar som anger de slutliga URL:erna i spårningsmallar finns i [!DNL Microsoft Advertising]-dokumentationen [[!DNL Microsoft Advertising] eller ([!DNL Google Ads] endast) i parametrarna för spårningsmallen i avsnittet Tillgängliga [!DNL ValueTrack]-parametrar i [[!DNL Google Ads] dokumentationen](https://support.google.com/google-ads/answer/6305348).](https://help.ads.microsoft.com/#apex/3/en/56799)

   * ([!DNL Yahoo! Japan Ads] endast) Använd parametern `!{lpurl}` för att ange landningssidans URL.

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel `{lpurl}?matchtype={matchtype}&device={device}`.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

* När kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] prefixas automatiskt en egen omdirigerings- och spårningskod när du sparar posten i Search, Social och Commerce.

>[!NOTE]
>
>* Undvik att använda makron för [!DNL Google Ads], som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör kontogruppen på Adobe arbeta med kundsupport eller implementeringsteamet för att lägga till dem.
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Om du uppdaterar en spårningsmall på annons-, sitelink- eller nyckelordsnivå skickas relevanta annonser om för granskning. Du kan uppdatera dina spårningsmallar på konto-, kampanj- eller annonsgruppsnivå utan att skicka in dina annonser på nytt för godkännande.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] endast konton) ID:t för ett agentkonto/hanteringskonto som är associerat med kontot.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] enbart konton; valfritt) Ett agentkonto/hanteringskonto som är associerat med kontot. Om du vill ta bort en befintlig association väljer du [!UICONTROL No MCC Account].

**[!UICONTROL Application ID]:** ([!DNL Yandex] endast konton) Den utvecklartoken som ska användas för kontot. Samma token används för alla [!DNL Yandex]-konton.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] konton med inställningen Delat konto är endast inaktiverad; valfritt) Det numeriska ID:t för kampanjen som används för att betala för alla annonskampanjer i kontot.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] konton med inställningen Delat konto är endast inaktiverad; valfritt) Den utvecklartoken som ska användas för finansrelaterade API-anrop, till exempel för omallokering av pengar från plånboken mellan annonserarens kampanjer, om det behövs för portföljoptimering.

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

**[!UICONTROL Track Product Group]:** (endast för [!UICONTROL EF Redirect]) har inte implementerats

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid-format:** (Befintliga [!DNL Google Ads]-konton för annonsörer med integrering mellan Adobe Advertising och Adobe Analytics och för vilka AMO-ID:t (s_kwcid) inte redan har migrerats)

Det här kontot använder det äldre formatet för spårningskoden för AMO ID, som gör att Adobe Advertising kan dela data om kontot med Adobe Analytics. Det [senaste formatet](/help/integrations/analytics/ids.md#amo-id-formats) innehåller parametrar för kampanj-ID och annonsgrupp-ID, som krävs för att korrekt rapportera på kampanjnivå och annonsgruppsnivå för [!DNL Google Ads] prestandamängdskampanjer samt utkast och experimentkampanjer i Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Om det här kontot behöver rapportera på kampanj- och annonsgruppsnivå klickar du på pennikonen [!UICONTROL Edit] och sedan **[!UICONTROL Migrate to new s_kwcid format]** för att ändra till det nya formatet. För konton som inte innehåller de här kampanjtyperna är migrering till det nya formatet valfritt, men rekommenderas.

Fullständiga anvisningar finns i &quot;[Uppdatera spårningskoden för AMO-ID för ett [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)&quot;.

**Rapportsvitnamn:** (Endast för EF-omdirigering med token; annonsörer med integrering mellan Adobe Advertising och Adobe Analytics; valfritt) En eller flera analysrapportsviter dit Search, Social och Commerce skickar data som samlas in från annonsnätverket, inklusive entitetsklassificeringar och klickdata för kontot. Den här funktionen är bara tillgänglig för annonsnätverk som stöds.

För att data ska visas i rapportsviterna måste antingen (a) funktionen för AMO ID på serversidan konfigureras för kontot eller (b) inställningen [!UICONTROL Enable tracking for SAINT feeds] på annonsörnivå måste aktiveras. Dessutom måste annonsörens Analytics-konto vara konfigurerat för att ta emot data från Search, Social och Commerce. Kontakta kontoteamet på Adobe om du vill ha mer information.

>[!MORELIKETHIS]
>
>* [Om annonskonton](ad-network-account-about.md)
>* [Hantera handlarcenterkonton](merchant-account-manage.md)
>* [Uppdatera s_kwcid-spårningskoden för ett [!DNL Google Ads] konto](update-amo-id-google.md)
