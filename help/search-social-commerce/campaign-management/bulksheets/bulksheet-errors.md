---
title: Bulkbladsfel
description: Referera till möjliga orsaker till varje fel i kalkylblad.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Bulkbladsfel

Med Sök, Socialt och Commerce genereras två typer av felfiler under kalkylbladsåtgärder:

* **SE-fel:** När en fil har publicerats men annonsnätverket inte accepterar alla data skapas en felfil med namnet `<uploaded file name>_se_errors.<extension used for the bulksheet>`. När vissa men inte alla rader accepterades, visar felfilen de rader som inte var bokförda och en förklaring av varje fel så att du kan korrigera det. Felen ingår i kolumnen [!UICONTROL SE Error Message].

>[!NOTE]
>
>Om du publicerar [!DNL Google Ads] annonser som bryter mot annonsnätverkets annonspolicyer, men som kan vara berättigade till undantag, kommer dessa annonser automatiskt att postas på nytt med begäran om undantag. Om begäran om undantag misslyckas inkluderas information om överträdelsen i felfilen.

* **EF-fel:** Om det inte går att överföra eller bearbeta en fil eller enskilda rader i filen i kalkylbladsåtgärden skapas en felfil med namnet `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Om det är problem med enskilda rader inkluderas dessa rader,
med en förklaring av varje fel så att du kan korrigera det. Felen ingår i kolumnen [!UICONTROL EF Error Message].

## [!UICONTROL SE Error] meddelanden

Fel i kolumnen [!UICONTROL SE Error] kommer direkt från annonsnätverket.

## [!UICONTROL EF Error] meddelanden

Följande fel kan finnas i kolumnen [!UICONTROL EF Error] i [!UICONTROL EF Errors]-filer.

### Hämta/skapa fel

| Kategori | Meddelande | Beskrivning |
|----|----|----|
| Allmänt | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Åtgärden misslyckades helt på grund av ett okategoriserat eller ohanterat fel. Om problemet kvarstår kontaktar du kontoteamet på Adobe för att undersöka orsaken. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social och Commerce kunde inte synkronisera med annonsnätverket innan kalkylbladet skapades, så inget kalkylblad skapades. Kontakta ditt kontoteam på Adobe om problemet kvarstår. |

### Överföringsfel

| Kategori | Meddelande | Beskrivning |
|----|----|----|
| Allmänt | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | Åtgärden misslyckades helt. Kontakta ditt kontoteam på Adobe om problemet kvarstår. |
| Alla enheter | [!UICONTROL Invalid Fields.] \[ogiltiga fält och fel\] | Angivna data saknas eller är ogiltiga. |
|  | [!UICONTROL Invalid Reference Given] | Entitetens ID i annonsnätverket, eller en överordnad enhets ID (till exempel konto-ID), motsvarar inte en entitet i Sök, Socialt och Commerce. Detta kan inträffa när du redigerar ID:t i kalkylbladet. |
|  | [!UICONTROL <Entity> is deleted or expired] | Entiteten har gått ut eller tagits bort, och du kan inte ändra dess egenskaper. Enheten kan tas bort när någon har redigerat statusen manuellt. |
|  | [!UICONTROL <Entity> status should be Active or Paused] | (Nya entiteter) En ny entitet kan bara vara &quot;Aktiv&quot; eller &quot;Pausad&quot;. |
|  | [!UICONTROL Duplicate Entries are present] | Flera rader ingår för samma enhet, med olika attribut i varje rad. Konsolidera ändringarna i en rad. |
|  | [!UICONTROL Invalid AMO ID given] | AMO-ID:t för raden finns inte. Detta kan inträffa om du har redigerat ID:t i kalkylbladet. |
|  | [!UICONTROL Invalid row given] | Raden innehåller inte tillräckligt med information för att fastställa entitetstypen. Redigera raden så att den innehåller alla obligatoriska fält för entitetstypen. |
| Konton | [!UICONTROL Provide Valid Account Details] | (Mallar för flera konton) Kontoidentifierare inkluderas inte i alla rader. Ange värden för någon av följande kombinationer av kolumner för varje rad: a) [!UICONTROL AMO ID] eller b) [!UICONTROL Account Name] och [!UICONTROL Platform]. |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social och Commerce har inte åtkomst till annonsnätverkskontot, så du kan inte skapa eller redigera kampanjdata. Kontrollera att autentiseringsuppgifterna för sökkontot är korrekta och att kontot är aktiverat. |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | (Shoppingkampanjer) Värdet i fältet [!UICONTROL Sales Country] är ogiltigt. Visa en lista över giltiga länder [för [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) och [för [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Alla kampanjkomponenter | [!UICONTROL Campaign creation failed] | Den överordnade kampanjen skapades inte, så entiteten skapades inte. Se till att alla överordnade entiteter innehåller alla obligatoriska fält. |
| Annonsgrupp | [!UICONTROL Campaign Row missing] | Den angivna överordnade kampanjen finns inte, så annonsgruppen skapades inte. Skapa den överordnade kampanjen på en ny rad. |
|  | [!UICONTROL New adgroup has both keywords and placement] | En annonsgrupp kan innehålla antingen nyckelord eller placeringar, men inte båda. Skapa separata annonsgrupper för nyckelord och placeringar. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) Annonsgruppen skapades inte eftersom den inte innehåller minst ett nyckelord. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) Annonsgruppen skapades inte eftersom den inte innehåller minst en annons. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) Annonsgruppen skapades inte eftersom den inte innehåller minst en annons. |
| Alla annonsgruppskomponenter | [!UICONTROL Adgroup creation failed] | Den överordnade annonsgruppen skapades inte, så entiteten kunde inte skapas. Detta kan bero på ett fel i annonsgruppsfälten eller på att den överordnade kampanjen misslyckades. Se till att alla överordnade entiteter innehåller alla obligatoriska fält. |
|  | [!UICONTROL Adgroup Row Missing] | Den angivna överordnade annonsgruppen finns inte, så entiteten kunde inte skapas. Skapa den överordnade annonsgruppen på en ny rad. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | Fältet [!UICONTROL Tracking Template] är bara till för konton som använder slutliga/avancerade URL:er. Ta bort värdet tills du har migrerat kontot för att använda slutliga/avancerade URL:er. |
| Annons | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | (Andra annonstyper än text, utökad text, produkt, appinstallation och dynamisk sökning) Du kan bara redigera status och URL för den här annonstypen. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Varje annonsgrupp kan innehålla upp till 50 annonser och det här kalkylbladet innehåller mer än 50. Minska antalet annonser. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | Annonsen finns i en överordnad enhet som har gått ut eller tagits bort, så du kan inte redigera den. |
| Nyckelord | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Den överordnade kampanjen eller annonsgruppen tas bort eller har gått ut, så du kan inte ändra entiteten. |
| Placement | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Den överordnade kampanjen eller annonsgruppen tas bort eller har gått ut, så du kan inte ändra entiteten. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) Du kan endast lägga bud på praktik i kampanjer i söknätverket eller i innehållsnätverket, men inte på kampanjer som riktar sig till både sök- och innehållsnätverk. |
| Shoppingproduktgrupp | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Varje produktgruppsnivå måste innehålla en [!UICONTROL Everything Else]-grupp. Du kan inte ta bort en [!UICONTROL Everything Else]-grupp manuellt. Den tas automatiskt bort när du tar bort alla andra produktgrupper på samma nivå. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Den överordnade kampanjen eller annonsgruppen tas bort eller har gått ut, så du kan inte ändra entiteten. |
| Webblänk | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] endast) Meddelandet är felaktigt. Varje kampanj kan innehålla upp till fyra (inte 10) sitelinks, och det här kalkylbladet innehåller mer än fyra. Ta bort några sitelinks. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | Den överordnade kampanjen har gått ut eller tagits bort, så du kan inte redigera den. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Det gick inte att skapa sitelink eftersom annonsen inte skapades. |
| Platsmål | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | Den överordnade kampanjen eller annonsgruppen tas bort eller har gått ut, så du kan inte redigera platsmålen. |
| Undantag | [!UICONTROL Other than status is modified] | Du kan bara redigera status för ett undantag ([!UICONTROL Active] eller [!UICONTROL Deleted]). |
| Google mål/målgrupper för ommarknadsföringslista | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] kampanjer) RLSA-målet motsvarar inte en befintlig RLSA (publik). Korrigera värdena i kolumnerna [!UICONTROL Audience] och [!UICONTROL RLSA Target]. |

### Bokföringsfel

Följande fel inträffar endast i [!UICONTROL EF Errors] filer. De flesta bokföringsfel kommer från annonsnätverket och ingår i en SE-felfil.

| Kategori | Meddelande | Beskrivning |
|----|----|----|
| Allmänt | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | Åtgärden misslyckades helt. Kontakta ditt kontoteam på Adobe om problemet kvarstår. |
| Alla enheter | [!UICONTROL Entity] har publicerats i annonsnätverket | Enheten har bokförts i annonsnätverket, men den synkroniserades inte till Search, Social och Commerce samtidigt, så entitetsdata är inte direkt tillgängliga i Search, Social och Commerce. Synkroniseringsprocessen aktiveras automatiskt nu.<br><br>När stora datamängder synkroniseras kanske data inte är tillgängliga i Sök, Social och Commerce på flera timmar eller mer. |
| | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | Det gick inte att skapa den överordnade entiteten, så den underordnade entiteten skapades inte. |

>[!MORELIKETHIS]
>
>* [Om att hantera kampanjdata med hjälp av kalkylblad](bulksheet-about.md)
>* [Hämta/skapa en kalkylbladsfil](bulksheet-download.md)
>* [Validera landningssidor i kalkylbladsfiler](bulksheet-validate-landing-pages.md)
>* [Överför en kalkylbladsfil eller korrigerad felfil](bulksheet-upload.md)
>* [Bokför kalkylblad eller korrigerade felfiler](bulksheet-post.md)
