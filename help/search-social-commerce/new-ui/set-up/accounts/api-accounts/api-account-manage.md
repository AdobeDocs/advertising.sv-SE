---
title: (Nytt användargränssnitt) Hantera och nätverkskonton
description: Lär dig hur du konfigurerar och hanterar kontoinformation i det nya gränssnittet för ett annonsnätverk som synkroniseras via annonsnätverkets API.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nytt användargränssnitt) Hantera annonsnätverkskonton via API-anslutning

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta-funktion*

<!-- Move out info about Naver into a separate page -->

Nedan följer instruktioner för hur du hanterar annonsnätverkskonton som synkroniseras med API:t i annonsnätverket.

<!-- Move out info about Naver into a separate page -->

Mer information om vilka funktioner som är tillgängliga för varje annonsnätverk finns i [Lager som stöds](/help/search-social-commerce/introduction/supported-inventory.md).

## Skapa information om annonsnätverkskonton {#create-account}

Om du vill aktivera synkronisering av ett konto måste du skapa en motsvarande kontopost som innehåller kontoinloggningsuppgifterna och spårningsalternativen och med statusen *aktiverad*.

>[!NOTE]
>
>Om du vill skapa ett verkligt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Klicka på **[!UICONTROL Create Account]**.

1. Klicka på annonsnätverkets namn och sedan på **[!UICONTROL Next]**.

1. (Alla annonsnätverk utom [!DNL Yandex]) Logga in i annonsnätverket med annonsörens autentiseringsuppgifter. Välj alternativet Kontospårning för det här kontot. Klicka sedan på **[!UICONTROL Next]** i det övre högra hörnet.

1. Ange [kontoinställningarna](#account-settings-api):

   1. På fliken **[!UICONTROL Select Accounts]** anger du de allmänna kontoinställningarna. Ange kontoautentiseringsuppgifterna för [!DNL Yandex]-konton.

   1. Klicka på fliken **[!UICONTROL Setup Tracking]** och ange spårningsinställningarna.

   1. (Annonsörer med en [[!DNL Adobe Analytics for Advertising] integrering](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och välj alla [!DNL Analytics] rapporteringsprogram som ska användas för att spåra och rapportera kampanjaktiviteter.

1. Klicka på **[!UICONTROL Save]**.

   Nyligen gjorda kostnads- och klickdata för alla kampanjer på kontot uppdateras varje timme i Sök, Socialt och Commerce. Som standard är data tillgängliga under de senaste 5-10 dagarna, beroende på annonsnätverket. Vid behov kan startteamet dock hämta data för upp till de senaste 60 dagarna.

## Redigera information om nätverkskonton {#edit-account}

Om du vill autentisera kontoinställningarna på nytt för att uppdatera anslutningen eller uppdatera behörigheter aktiverar eller inaktiverar du aktivitet för ett konto, ändrar standardspårningsparametrarna för ett konto eller ändrar rapportsviterna för [!DNL Analytics] för att använda för spårning och rapportering. Redigera sedan kontoinformationen.

>[!NOTE]
>
>Om du vill redigera ett faktiskt konto i annonsnätverket går du till annonsnätverkets webbplats.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Välj konto på något av följande sätt:

   * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

   * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

1. Redigera [kontoinställningarna](#account-settings-api):

   1. (Valfritt) Redigera kontoinformationen på fliken **[!UICONTROL Account Details]**.

   1. (Valfritt) Klicka på fliken **[!UICONTROL Setup Tracking]** och redigera spårningsinställningarna.

   1. (Valfritt, annonsörer med en [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Klicka på fliken **[!UICONTROL Set up Adobe Analytics]** och redigera [!DNL Analytics]-rapporteringssviterna som ska användas för att spåra och rapportera kampanjaktiviteter.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicka på **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social och Commerce måste synkronisera de nya kontodata med de som finns i annonsnätverket. Detta sker automatiskt en gång om dagen, eller oftare när Search, Social och Commerce upptäcker ändringar i annonsnätverket.

## Återautentisera ett annonsnätverkskonto {#reauthenticate}

Autentisera kontot igen om du vill uppdatera annonsnätverksanslutningen eller uppdatera behörigheterna för kontot.

1. (Om du är inloggad på ett annat konto för samma annonsnätverk i samma webbläsarprogram) Logga ut från något annat konto än annonsörens.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Välj konto på något av följande sätt:

   * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

   * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

1. Klicka på **[!UICONTROL Account Details]** på fliken **[!UICONTROL Re authenticate]** och logga in i annonsnätverket med annonsörens inloggningsuppgifter.

1. Klicka på **[!UICONTROL Save]**.

## Aktivera eller inaktivera annonskonton {#enable-disable-account}

När ni aktiverar ett annonsnätverkskonto synkroniserar Search, Social och Commerce kampanjdata med kontot (när det stöds) och pushar för automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer. När du inaktiverar ett annonsnätverkskonto avbryts alla aktiviteter på kontot av Sök, Sociala och Commerce. Data som samlats in medan kontot var aktivt lagras fortfarande, men kampanjhanteringsvyer och rapporter inkluderar inte data för den tidsperiod under vilken kontot inaktiveras. Du kan aktivera kontot igen senare om du vill återuppta aktiviteten med kontot.

1. Klicka på **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** på huvudmenyn.

1. Gör något av följande:

   * (Från vyn [!UICONTROL Accounts]):

      * (Om du vill aktivera kontot) Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Activate]** i verktygsfältet för gruppåtgärder.

      * (Om du vill inaktivera kontot) Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Pause]** i verktygsfältet för gruppåtgärder.

   * (Från kontoinställningarna):

      1. Välj konto på något av följande sätt:

         * Håll markören över kontonamnet, klicka på **..** och klicka sedan på **[!UICONTROL Edit]**.

         * Markera kryssrutan bredvid kontonamnet och klicka sedan på **[!UICONTROL Edit]** i verktygsfältet för gruppåtgärder.

      1. Stäng av **[!UICONTROL Account Details]** på fliken **[!UICONTROL Account enabled]**.

      1. Klicka på **[!UICONTROL Save]**.

## Inställningar för annonsnätverkskonto {#account-settings-api}

Kontoinställningarna varierar beroende på annonsnätverk. Du kanske inte ser alla inställningar nedan.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Fliken [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Namnet som ska visas för kontot i Sök, Socialt och Commerce.

>[!NOTE]
>
>Om du har en integrering med Search, Social och Commerce-Adobe Analytics och ändrar namnet på sökkontot ber du ditt Adobe-kontoteam att uppdatera mappningen.

**[!DNL [Lägg till nätverk] konton]:** (synligt när du skapar ett konto) Annonsnätverkskontot som ska synkroniseras.

**[Inloggningsinformation]:** (endast Yandex-konton) Kontoautentiseringsuppgifterna som ska användas:

* **[!UICONTROL Login]:** Inloggningsnamnet eller ID:t för att aktivera API-åtkomst till kontot.

* **[!UICONTROL Password]:** Lösenordet för kontot.

* **[!UICONTROL Access Key]:** Åtkomstnyckeln för det utvecklarkonto som ska användas.

* **[!UICONTROL Application ID]:** Den utvecklartoken som ska användas för kontot. Samma token används för alla [!DNL Yandex]-konton.

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] konton med inställningen Delat konto är endast inaktiverad; valfritt) Det numeriska ID:t för kampanjen som används för att betala för alla annonskampanjer i kontot.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] konton med inställningen Delat konto är endast inaktiverad; valfritt) Den utvecklartoken som ska användas för finansrelaterade API-anrop, till exempel för omallokering av pengar från plånboken mellan annonserarens kampanjer, om det behövs för portföljoptimering.

**[!UICONTROL Network Account ID]:** (Alla annonsnätverk förutom [!DNL Yandex] Det konto-ID som tilldelats av annonsnätverket.

>[!NOTE]
>
>Konton för annonsnätverkshanterare stöds inte här. Om du vill identifiera ett hanterarkonto för [!DNL Microsoft Advertising] använder du fältet Huvudkonto-ID eller MCC-konto. Om du vill [konfigurera autentiseringsuppgifter för ett [!DNL Google Ads] hanterarkonto](/help/search-social-commerce/admin/manager-accounts.md) går du till [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (skrivskyddad) Förkortningen för valutan som används för kontot. Värdet fylls i automatiskt med den valuta som konfigurerats för kontot i annonsnätverket när du sparar posten.

**[!UICONTROL Time Zone]:** Annonsörens tidszon. Värdet fylls i automatiskt med den tidszon som konfigurerats för annonserarens konto Search, Social och Commerce när du sparar posten.

**[!UICONTROL Login]:** (skrivskyddat) Användarkontot som används för att logga in på kontot.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Sökning, socialt och Commerce synkroniserar kampanjdata med kontot (när det stöds) och pushar automatiserade bud och/eller kampanjbudgetar för kampanjer i portföljer.

## Fliken [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Om spårning ska aktiveras eller inte använder du Adobe Advertising tjänst för spårning av konvertering. Den här metoden genererar unika ID:n för klickspårning och dirigerar om användare till Adobe Advertising-servern för spårningsändamål innan de skickas till klientens landningssida. Den här metoden har standardalternativ för spårning som du kan anpassa, och du kan också ange parametrar som ska läggas till i varje URL.

Aktivera **[Aktivera spårning]** om du vill aktivera den här funktionen.

>[!NOTE]
>
>* Om du ändrar den här inställningen måste du återskapa spårnings-URL:er för kontot.
>* Spårningsalternativ på kampanjnivå åsidosätter kontonivåinställningar.

**[!UICONTROL Tracking Type]:** (När Sökning, Social och Commerce-spårning är aktiverat) Metoden för att dirigera om slutanvändare till den slutliga URL:en eller mål-URL:en. Det valda alternativet gäller för alla budenheter i kontot eller kampanjen. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar och standardinställningen på kampanjnivå ärvs från kontoinställningarna.

* *[!UICONTROL Standard]:* Om du bara vill dirigera om slutanvändaren till den angivna URL:en.

* *[!UICONTROL Token]:* Om du vill dirigera om slutanvändaren till URL:en och även registrera ID:t Search, Social och Commerce för klickningen (`ef_id`) som en frågesträngsparameter, som används som token. Välj det här alternativet om du ska rapportera offlinetransaktioner, om du vill att Search, Social och Commerce ska utbyta data med Adobe Analytics, eller om du vill spåra alla konverteringar som sker i [!DNL Apple Safari] webbläsare.

>[!NOTE]
>
>* Om du växlar från [!UICONTROL Standard] till [!UICONTROL Token], eller vice versa, måste du återskapa spårnings-URL:er för kontot.
>* Du kan åsidosätta inställningen på kontonivå på kampanjnivå.

**[!UICONTROL Auto Update]:** (När Sökning, Social och Commerce-spårning är aktiverat) Standardiserar URL:er för spårning för kompatibilitet mellan webbläsare och servrar. Search, Social, &amp; Commerce skickar automatiskt följande till annonsnätverket under nästa synkronisering: a) parametrar för sökning, social och Commerce-spårning för spårningsmallar och samma parametrar som läggs till i de slutliga URL:erna eller b) nya mål-URL:er som är inbäddade med spårningskod för sökningar, sociala nätverk och Commerce. För annonsörer med en [Adobe Advertising-Adobe Analytics-integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) och en AMO ID (s_kwcid)-konfiguration på serversidan, innehåller överföringen även [AMO ID-parametrar](/help/integrations/analytics/ids.md#amo-id) för dina [!DNL Google Ads]- och [!DNL Microsoft Advertising]-konton. Standardinställningen på kontonivå ärvs från annonsörens spårningsinställningar. Du kan åsidosätta inställningen på kontonivå på kampanjnivå.

Spårnings-URL:er uppdateras dagligen endast för entiteter som är osynkroniserade (det vill säga nya entiteter som lagts till och befintliga entiteter vars egenskaper har ändrats). Om du ändrar den här inställningen från inaktiverad till aktiverad för en befintlig annonserare/konto/kampanj uppdateras därför inte spårnings-URL:er för befintliga enheter som redan är synkroniserade. Om du vill lägga till spårning i URL:er för befintliga, synkroniserade enheter kontaktar du Adobe Account Team och begär en manuell synkroniseringsprocess en gång. Den automatiska överföringsprocessen hanterar framtida ändringar.

**[!UICONTROL URL Encoding]:** (När Sökning, Social och Commerce-spårning är aktiverat, endast konton med mål-URL:er) Kodar bas-URL:en i slutanvändarens adressfält (till exempel `%3D` i stället för `=`):

**[!UICONTROL Tracking Level]:** (När Sökning, Social och Commerce-spårning är aktiverat, tillgängligt på konto- och kampanjnivå, inte tillgängligt för annonsnätverk som har aktiverats för parallell spårning) Den nivå på vilken klickningar och intäkter ska spåras genom att lägga till en omdirigeringsparametrar (när det är relevant) och lägga till parametrar till de relevanta URL-adresserna:

* *[!UICONTROL Keyword]:* Om du bara vill spåra data på nyckelordsnivå. Inte tillgängligt för [!DNL Yandex].

* *[!UICONTROL Ad]:* Om du bara vill spåra data på annonsnivå. Inte tillgängligt för [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* Om du vill spåra data på både nyckelords- och annonsnivåer. Inte tillgängligt för [!DNL Naver] och [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] och [!DNL Microsoft Advertising] enbart konton; valfritt) Alla parametrar som ska läggas till i slutet av de slutliga URL:erna för att spåra information, inklusive alla parametrar som företaget måste spåra.

Exempel: `param1=value1&param2=value2`

Konton som använder Adobe Advertising klickspårning måste inkludera annonsnätverkets klickidentifierare (`msclkid` för [!DNL Microsoft Advertising]; `gclid` för Google) i suffixet. Konton med en Adobe Analytics-integrering måste använda parametern AMO ID (med början från `s_kwcid`). Om kontot har en AMO ID-implementering på serversidan läggs parametern till automatiskt när en användare klickar på en annons. I annat fall måste du lägga till den manuellt här. Se de [suffixformat som krävs för  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) och [obligatoriska suffixformat för  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Det här fältet uppdateras inte av spårningsinställningen [!UICONTROL Auto Update].
>* Slutliga URL-suffix på lägre nivåer åsidosätter suffixet på kontonivå. För enklare underhåll bör du bara använda suffixet på kontonivå om inte olika spårning för enskilda kontokomponenter krävs. Om du vill konfigurera ett suffix på annonsgruppsnivå eller lägre använder du annonsnätverkets redigerare.

**URL för kontospårning**: ([!DNL Google Ads], [!DNL Microsoft Advertising] och [!DNL Yahoo! Japan Ads] konton endast; valfritt) Standardspårningsmallen för kontot, som anger alla omdirigeringar och spårningsparametrar utanför domänen och bäddar även in URL:en för den slutliga sidan/landningssidan i en parameter. Exempel: `{lpurl}?source={network}&id=5` eller `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` som ska inkludera en omdirigering.

* Så här bäddar du in den slutliga URL:en:

   * ([!DNL Google Ads] och endast [!DNL Microsoft Advertising]) En lista med parametrar som anger de slutliga URL:erna i spårningsmallar finns i [!DNL Microsoft Advertising]-dokumentationen [[!DNL Microsoft Advertising] eller (](https://help.ads.microsoft.com/#apex/3/en/56799) endast) i parametrarna för spårningsmallen i avsnittet Tillgängliga [!DNL Google Ads]-parametrar i [!DNL ValueTrack]dokumentationen[[!DNL Google Ads] .](https://support.google.com/google-ads/answer/6305348)

   * ([!DNL Yahoo! Japan Ads] endast) Använd parametern `!{lpurl}` för att ange landningssidans URL.

* Du kan också inkludera URL-parametrar och anpassade parametrar som definierats för kampanjen, avgränsade med et-tecken (&amp;), till exempel `{lpurl}?matchtype={matchtype}&device={device}`.

* Du kan också lägga till omdirigeringar och spårning från tredje part.

* När kampanjinställningarna innehåller [!UICONTROL EF Redirect] och [!UICONTROL Auto Upload] prefixas automatiskt en egen omdirigerings- och spårningskod när du sparar posten i Search, Social och Commerce.

>[!NOTE]
>
>* Undvik att använda makron för [!DNL Google Ads], som inte ersätts med klick från källor som aktiverar parallell spårning. Om annonsören måste använda makron bör Adobe kontoteam arbeta med kundsupport eller implementeringsteamet för att lägga till dem.
>* Spårningsmallen på den mest detaljerade nivån åsidosätter värdena på alla högre nivåer. Om till exempel både kontoinställningarna och nyckelordsinställningarna innehåller ett värde används nyckelordsvärdet.
>* Om du uppdaterar en spårningsmall på annons-, sitelink- eller nyckelordsnivå skickas relevanta annonser om för granskning. Du kan uppdatera dina spårningsmallar på konto-, kampanj- eller annonsgruppsnivå utan att skicka in dina annonser på nytt för godkännande.

## Fliken [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, &amp; Commerce skickar data som samlas in från annonsnätverket, inklusive entitetsklassificeringar och klickdata för kontot. Den här funktionen är bara tillgänglig för annonsnätverk som stöds.

För att data ska visas i rapportsviterna måste antingen (a) funktionen för AMO ID på serversidan konfigureras för kontot eller (b) inställningen [!UICONTROL Enable Advertising reporting in Analytics] på annonsörnivå måste aktiveras. Dessutom måste annonserarens [!DNL Analytics]-konto vara konfigurerat för att ta emot data från Search, Social och Commerce. Kontakta Adobe Account Team om du vill ha mer information.

>[!MORELIKETHIS]
>
>* [Om annonskonton](../ad-network-account-about.md)
>* [Hantera handlarcenterkonton](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Uppdatera s_kwcid-spårningskoden för ett [!DNL Google Ads] konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
