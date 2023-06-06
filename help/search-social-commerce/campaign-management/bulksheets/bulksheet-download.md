---
title: Hämta/skapa en kalkylbladsfil
description: Lär dig hur du skapar kalkylbladsfiler genom att hämta kontodata för dina annonsnätverk.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---

# Hämta/skapa en kalkylbladsfil

Du kan skapa kalkylblad med anpassade inställningar för ett eller flera konton på ett eller flera [stödda annonsnätverk](bulksheet-about.md#bulksheet-functionality-by-network). Bulksheets innehåller data från sökning, sociala medier och handel.

För synkroniserade kampanjer kan du synkronisera med annonsnätverket innan du hämtar data för att säkerställa att de senaste dataändringarna på annonsnätverkets sida inkluderas. För alla annonsnätverk kan du välja att generera nya klickspårnings-URL:er som ska inkluderas i filen.

>[!NOTE]
>
>Du kan också [skapa en kalkylbladsfil baserat på synliga kolumner i en kampanjhanteringsvy](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. På huvudmenyn klickar du på **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Klicka på i verktygsfältet **[!UICONTROL Download Bulksheet]**.

1. Ange [inställningar för kalkylblad](#bulksheet-download-settings):

1. På sidan **[!UICONTROL Selections] anger eller väljer du information i fälten.

1. (Valfritt) Klicka på **[!UICONTROL Rows and Columns]** anger du de kontokomponenter och de komponentlägen för vilka rader ska inkluderas i kalkylbladet och anger sedan de kolumner som ska inkluderas för varje vald komponent.

   En lista över tillgängliga kalkylbladsrader finns i &quot;[Bulkbladsrader efter annonsnätverk](#bulksheet-rows-by-ad-network).&quot;

1. (Valfritt) Klicka på **[!UICONTROL Filters]** och ange sedan kriterier för specifika kampanjer, annonser, annonser/kreatörer, nyckelord, utplaceringar och andra enheter som ska ingå i kalkylbladet:

   1. Välj en parameter (enhetsnamn eller ID; eller något element i en annons, nyckelord eller placering) väljer du en operator och anger sedan det tillämpliga värdet. Om du till exempel bara vill returnera annonser med&quot;skor&quot; i rubriken för en [!DNL Google Ads] konto, välj *Headline*, markera *[!UICONTROL contains]* och sedan ange `shoes` i indatafältet.

   1. (Om du vill använda ytterligare filter) För varje ytterligare filter klickar du på **[!UICONTROL +Add Filter]**, markera **[!UICONTROL AND]** eller **[!UICONTROL OR]**, markerar ett annonselement eller nyckelord och en operator och anger sedan det tillämpliga värdet.

1. Klicka på **[!UICONTROL Download].

När aktiviteten startas visas ett meddelande i fönstret, men det är fortfarande öppet så att du kan fortsätta skapa ytterligare kalkylblad om du vill. Alla angivna filter och undantag som gäller för alla nya konton som du väljer behålls. När aktiviteten startas visas filen i vyn Länkark. När filen skapas får du ett e-postmeddelande med en länk till filen; Beroende på mängden data som sammanställs kan det ta flera minuter eller mer att skicka meddelandet. Om det inte går att skapa filen visas en felfil i vyn Bulksheets och du får ett e-postmeddelande med en länk till felfilen.

## Hämtningsinställningar för bulkark {#bulksheet-download-settings}

| Tabb | Parameter | Beskrivning |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | Konton, kampanjer eller annonsgrupper dit data ska överföras:<ul><li>Markera kryssrutan bredvid kontonamnet och klicka sedan på >> för att flytta det till [!UICONTROL Selected Filters] kolumn.</li><li>Om du vill välja enskilda kampanjer eller annonsgrupper klickar du bredvid kontot för att expandera det (om det behövs), klickar på bredvid kampanjen för att expandera den, markerar kryssrutan bredvid kampanjnamnet eller annonsgruppnamnet och klickar sedan på >> för att flytta den till [!UICONTROL Selected Filters] kolumn. Om du till exempel bara vill hämta data för Campaign 1 i Konto 1 expanderar du Konto 1, markerar kryssrutan bredvid Campaign 1 och flyttar den sedan till [!UICONTROL Selected Filters] kolumn.</li></ul><b>Anteckningar:</b><ul><li>Ett enda kalkylblad kan användas för flera konton i flera annonsnätverk. Annonsspecifika nätverkskolumner är märkta i kalkylblad med annonsnätverksnamnet (t.ex.&quot;Mobile Carriers (Google Ads)&quot;).</li><li>Om du vill se vilken typ av komponent ett objekt är håller du markören över den.</li><li>För kampanjer är den första bokstaven i annonsnätverksnamnet inom parentes efter kontonamnet (till exempel&quot;Acme Realty (G)&quot; för [!DNL Google Ads] konto).</li><li>Som standard visas bara aktiva och aktiverade konton och deras aktiva komponenter. Om du vill visa pausade och borttagna komponenter klickar du på ![Nedåtpil](/help/search-social-commerce/assets/arrow-down-expand.png "Nedåtpil") nästa [!UICONTROL Show] och välj **[!UICONTROL All]. |
|  | [!UICONTROL Generate Tracking URLs] | (Valfritt) Inkluderar spårningsmallar och landningssidessuffix (för tillämpliga annonsnätverk) i konton med spårningsmallar, eller mål-URL:er med inbäddade spårningskoder i konton med mål-URL:er, för nyckelord, annonser, placeringar, sitelinks och [!DNL Google Ads] produktgrupper i kalkylbladet. Som standard är det här alternativet markerat.<br><br>När det här alternativet är markerat genereras URL-adresserna enligt parametrarna i [!UICONTROL Campaign Tracking] i kontoinställningarna eller kampanjinställningarna. Om det redan finns spårnings-URL:er genereras de inte om om de inte behövs (till exempel om nyckelordsmatchningstypen, annonstexten eller kontots spårningsparametrar har ändrats).<br><br><b>Anteckningar:</b><ul><li>Om annonsören använder konverteringsspårning för annonsering i Adobe och det aktuella kontot inte är konfigurerat för att automatiskt generera och överföra URL:er för spårning, måste du generera nya URL:er för spårning när bas-URL:erna har ändrats.</li><li>Om du inte markerar det här alternativet kan du fortfarande generera spårnings-URL:er senare när du överför eller skickar filen.</li></ul> |
|  | [!UICONTROL Perform Pre-sync] | (Valfritt) Instruerar Search, Social och Commerce att synkronisera filerna med de angivna kampanjerna för att säkerställa att alla data är desamma. Som standard är det här alternativet inte markerat.<br><b>Obs!</b> Search, Social, &amp; Commerce synkroniserar automatiskt med annonsnätverket en gång om dagen, när det upptäcker en ny kampanj i annonsnätverket och varje gång du ändrar kampanjdata inifrån Search, Social och Commerce. Välj det här alternativet om du tror att de senaste ändringarna av kampanj- eller kontodata gjordes direkt i annonsnätverket eller med annonsnätverkets redigerare. Det tar längre tid att skapa flera kalkylblad när du väljer det här alternativet. |
|  | [!UICONTROL Bulksheet Name] | Namnet på det nya kalkylbladet och filtypen. Som standard skapas filen i tabbseparerat värdeformat och får ett av följande namn:<ul><li>(för alla konton i annonsnätverket) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(för enstaka konton) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(för flera konton) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>Du kan byta namn på filen. Namnet får inte innehålla följande tecken: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>Du kan också ändra filtypen. Alternativen är *[!UICONTROL .tsv]* (för tabbseparerade värden), *[!UICONTROL .txt]* (för Unicode-kompatibel ASCII-text), *[!UICONTROL .csv]* (för kommaavgränsade värden), eller *[!UICONTROL .zip]* (för komprimerat ZIP-format, som packar upp till en TSV-fil).<br><br><b>Tips:</b> Använd formatet TSV eller TXT för kalkylblad som innehåller internationella tecken. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | Enheterna, och deras motsvarande status, som ska inkluderas i kalkylbladet, med en datarad per post. Om du t.ex. inkluderar aktiva kampanjer innehåller kalkylbladet en rad per aktiv kampanj. Endast valda enheter med vald status inkluderas. Standardvärden är förmarkerade baserat på det angivna annonsnätverket. Som standard inkluderas endast aktiva instanser av de markerade entiteterna. En lista över tillgängliga kalkylbladsrader finns i &quot;[Bulkbladsrader efter annonsnätverk](#bulksheet-rows-by-ad-network).&quot;<br><br>Om du vill lägga till eller ta bort enheter markerar eller avmarkerar du kryssrutorna intill enheterna. Om du vill lägga till eller ta bort status för en enhet klickar du på bredvid statusmenyn och markerar eller avmarkerar kryssrutorna intill enheterna. |
|  | [!UICONTROL Cascading Status Hierarchy] | Filtrerar omfånget för underordnade entiteter till de som har de angivna överordnade entitetsstatusarna med en AND-åtgärd. Om du t.ex. väljer&quot;Aktiv kampanj&quot;,&quot;Aktiv grupp&quot; och&quot;Aktiv nyckelord&quot;, innehåller kalkylbladet bara aktiva nyckelord i aktiva annonsgrupper i aktiva kampanjer.<br><br>Om du inte markerar det här alternativet beaktas inte den överordnade statusen och filtret använder en OR-åtgärd. Om du t.ex. väljer&quot;Aktiv kampanj&quot;,&quot;Aktiv Adgroup&quot; och&quot;Aktiv nyckelord&quot; innehåller bulkbladet alla aktiva kampanjer; Alla aktiva annonseringsgrupper, oavsett status för den överordnade kampanjen. och alla aktiva nyckelord, oavsett status för den överordnade kampanjen och annonsgruppen. |
|  | [!UICONTROL Bulksheet Columns] | Kolumner som ska inkluderas i den hämtade kalkylbladsfilen:&lt;ul><li><li>*[!UICONTROL AMO ID]*: (Krävs om &quot;[!UICONTROL SE ID]&quot; är inte markerat) Innehåller en [!DNL Adobe]-genererad unik identifierare för varje entitet/rad. Search, Social, &amp; Commerce använder värdet för att fastställa rätt identitet för redigering, men publicerar det inte i annonsnätverket. Senare kan du redigera data för enheten med [!UICONTROL AMO ID] som identifierare, i stället för enhets-ID och överordnade enhets-ID.</li><li>*[!UICONTROL SE ID]*: (Krävs om &quot;[!UICONTROL AMO ID]&quot; är inte valt) Inkluderar annonsnätverkets unika identifierare för varje inkluderad kolumn och dess överordnade enheter. Senare, om du redigerar data för en enhet med [!UICONTROL SE ID] som identifierare måste du även inkludera rader för de överordnade entiteterna (inklusive deras [!UICONTROL SE ID] värden).</li><li>*[!UICONTROL Platform]*: Innehåller en [!UICONTROL Platform column] i början av varje rad för att ange annonsplattformen (till exempel&quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (Krävs om &quot;[!UICONTROL AMO ID]&quot; är inte markerat) Inkluderar annonsens nätverkskontonamn för varje entitet/rad.</li><li>\[Kolumner att inkludera\]: Om du vill ta med alla, inga eller bara markerade kolumner som är relevanta för varje markerad enhet i [!UICONTROL Bulksheet Rows] -avsnitt. Om du vill se de enskilda kolumnerna som är relevanta för en enhet klickar du på ![Högerpil](/help/search-social-commerce/assets/compressed-item.png "Högerpil") bredvid enhetsnamnet. Som standard inkluderas alla relevanta kolumner för varje vald entitetsrad. Avmarkera kryssrutan bredvid en enhet eller bredvid en enskild kolumn om du vill utesluta den från kalkylbladet.</li></ul><br><br><b>Tips:</b> Se till att du inkluderar lämpliga kolumner för att identifiera objektet i varje rad i kalkylbladsfilen. Exempel: du tar med nyckelordsrader per [!UICONTROL Bulksheet Rows] -väljaren men du utelämnar alla nyckelordsrelaterade kolumner. Det resulterande kalkylbladet innehåller en rad för varje nyckelordsinstans. Eftersom inga nyckelordsrelaterade kolumner ingår - inte ens AMO ID eller SE ID - kan du inte identifiera vilken nyckelordsinstans som gäller för en viss rad, och du kan inte använda detta blad för att uppdatera data om du inte manuellt lägger till rätt ID-kolumn och värden. |
| [!UICONTROL Filters] |  | Kriterier för specifika kampanjer, annonsgrupper, annonser/kreatörer, nyckelord och/eller placeringar som ska ingå i kalkylbladet:<ol><li>Välj en parameter (enhetsnamn eller ID; eller ett element i ett kreativt nyckelord eller en placering) väljer du en operator och anger sedan det tillämpliga värdet.<br><br>Om du till exempel bara vill returnera annonser med&quot;skor&quot; i rubriken för en [!DNL Google Ads] konto, välj *[!UICONTROL Headline]*, markera *[!UICONTROL contains]* och sedan ange `shoes` i indatafältet.</li><li>(Om du vill använda ytterligare filter) För varje ytterligare filter klickar du på **[!UICONTROL +Add Filter]**, markera **[!UICONTROL AND]** eller **[!UICONTROL OR]**, markerar ett annonselement eller nyckelord och en operator och anger sedan det tillämpliga värdet.</li></ul> |

## Bulkbladsrader efter annonsnätverk {#bulksheet-rows-by-ad-network}

| Bulkbladsrad | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Anteckningar |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *eller* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | — | — | Ja | Ja | Ja | Ja | ([!DNL Google  Ads]) Använd för alla annonstyper utom för responsiva sökannonser, som finns i [!UICONTROL Responsive Search Ad] rad. |
| [!UICONTROL Responsive Search Ad] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Ja | Använd endast för icke-negativa nyckelord. Om du vill visa negativa nyckelord som skapats på kampanj- eller annonsgruppsnivå använder du [!UICONTROL Campaign Negative Keyword] eller [!UICONTROL Adgroup Negative Keyword] rad om den är tillgänglig. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Ja | — | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | Ja | — | — | — | — | — | — | Används för dynamiska sökmål för en annonsgrupp. |
| [!UICONTROL Shopping Product Group] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | Använd endast för negativa nyckelord som skapats på kampanj- eller annonsgruppsnivå. Om du vill visa icke-negativa nyckelord använder du [!UICONTROL Keyword] rad om den är tillgänglig. |
| [!UICONTROL Campaign Negative Website] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Site Link] | — | Ja | — | — | — | — | — | Ja | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Ja | — |
| [!UICONTROL Adgroup Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [Hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
>* [Validera landningssidor i kalkylbladsfiler](bulksheet-validate-landing-pages.md)
>* [Exportera en genererad eller överförd kalkylbladsfil](bulksheet-export.md)

