---
title: Advertising DSP Macros
description: Referera till de tillgängliga makrona för allmän spårning och för att spåra klick på visningsannonser från tredje part.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Advertising DSP Macros

Ett makro är ett kort kommando eller en kortskrift för en instruktion och följer vanligtvis formatet `${MACRO_NAME}`. Makron som ingår i den kreativa koden eller klickbara URL:er utökas till en längre kodsträng som annonsservern kan förstå. DSP annonsserver kör makron när annonsen skickas eller klickas.

Ad-servermakron är användbara när du vill skicka viktig information till DSP eller till annonsservrar från tredje part. Makron används oftast vid handel med kod eller metadata från tredje part (t.ex. pixlar från tredje part).

Du kan infoga ett makro manuellt var som helst, t.ex. i en VAST-tagg, i en URL eller i en händelsepixel från DSP eller tredje part. Alla DSP-klienter och -partners har dock olika annonstaggformat och makrona bör infogas på olika ställen i taggen. Varje gång du arbetar med en ny kund eller partner måste du be dem om dokumentation om var makrona i deras annonstaggar som DSP hanterar ska infogas.

## Spårningsmakron

Använd allmänna spårningsmakron för alla annons- och taggtyper för att skicka tillbaka specifika data efter behov.

| Makro | Ersättningsbeskrivning | Typ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | Konto-ID. | heltal |
| `${TM_AD_ID}` | Annonsnyckeln (adKey). | string |
| `${TM_AD_ID_NUM}` | Annons-ID. | heltal |
| `${TM_ADVERTISER_ID}` | Annonsörs-ID. | heltal |
| `${TM_CAMPAIGN_ID}` | Kampanjnyckeln. | string |
| `${TM_CAMPAIGN_ID_NUM}` | Kampanjens ID. | heltal |
| ` ${TM_CLICK_URL}` | Omdirigerings-URL, som gör det möjligt för annonsservrar att spåra och räkna annonsklickningar. Om användaren klickar på annonsen aktiveras makrot och klickningen registreras och räknas i rapporteringssyfte. | string |
| ` ${TM_CLICK_URL_URLENC}` | Den kodade omdirigerings-URL:en, som gör det möjligt för annonsservrar att spåra och räkna annonsklickningar. Om användaren klickar på annonsen aktiveras makrot och klickningen registreras och räknas i rapporteringssyfte. Använd inte det här makrot om du inte skapar annonser från tredje part och leverantören kräver URL-kodning. | string |
| `${TM_FEED_ID}` | Nyckeln för medieplaceringen (feedKey). | string |
| `${TM_FEED_ID_NUM}` | ID för mediaplaceringen. | heltal |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Platsnyckeln för placeringen. Krävs för [!DNL AppsFlyer] klickningsspårare för installationsannonser för mobilappar.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | Placeringsnyckeln (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | Placerings-ID. | heltal |
| `${TM_RANDOM}` | Cachebuster: ett slumpmässigt tal mellan 1 och 100000. | long |
| `${TM_SESSION_ID}` | Sessionens ID, som motsvarar en enda hämtning av annonstaggen. | string |
| `${TM_SITE_DOMAIN_URLENC}` | Den sidunderdomän som tolkas från URL:en i anbudsförfrågan, URL-kodad. Stöds inte för annonser i banner, click-to-play. | string |
| ` ${TM_SITE_NAME}` | Platsnamnet för placeringen. | string |
| `${TM_SITE_URL_URLENC}` | Den URL som skickades i anbudsförfrågan, URL-kodad. Stöds inte för annonser i banner, click-to-play. | string |
| `${TM_SITE_ID_NUM}` | Platsens ID för placeringen. | heltal |
| `${TM_TIMESTAMP}` | Unix-tidsstämpeln anger hur många sekunder som har gått sedan midnatt (00:00 UTC) den 1 januari 1970. | long |
| ` ${TM_VIDEO_DURATION}` | Annonsvideons längd i sekunder. | heltal |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Mobilspecifika makron

| Makro | Ersättningsbeskrivning | Typ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) Plattforms-ID, som motsvarar enhetens operativsystem:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` när plattformen inte är något av ovanstående</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Enhetens modellnamn, URL-kodat. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Den miljö där annonsen betjänades:<ul><li>`a` = mobilprogram</li><li>`b` = mobilwebbplats</li></ul> | sträng (`a` eller `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) Plattforms-ID, som motsvarar enhetens operativsystem:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` när plattformen inte är något av ovanstående</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Enhetstypen som annonsen visades på:<ul><li>`TAB` = tablet</li><li>`PHN` = mobil</li><li>`computer` = dator</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Om användaren har valt bort annonsspårning eller inte:<ul><li>`1` (DNT-flagga = 1) = användaren har valt bort annonsspårning</li><li>`0` (DNT-flagga = 0) = användaren har angett annonsspårning</li></ul> | heltal (`0` eller `1`) |
| `${TM_BUNDLE}` | Programbutikens paket-ID [!DNL iOS] eller [!DNL Android]. Exempel: com.zynga.wwf2.free eller id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` anger om anbudsgivaren fastställer att anbudsförfrågan kommer från EU-ursprung och kräver GDPR-verkställighet:<ul><li>`1` = GDPR ska framtvingas</li><li>`0` = GDPR ska inte framtvingas</li></ul>`gdpr_consent=${GDPR_CONSENT}` är det medgivandevärde som skickas från leveranspartnern i den inkommande anbudsförfrågan:<ul><li>I de flesta fall är detta en base64url-kodad medgivandesträng, eller daisybit (exempel: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = inget samtycke</li><li>`1` = samtycke</li></ul> | daisybit eller heltal |

{style="table-layout:auto"}

## Klicka på Makron för visningsannonser från tredje part

För att kunna spåra klick efter annonser med hjälp av tredjepartstaggar krävs ett visningsklicksmakro i DSP. Endast en version av makrot krävs. Det relevanta makrot beror på taggens typ.

| Makro | Ersättningsbeskrivning | Typ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | Den omdirigerings-URL som gör att annonsservrar kan spåra och räkna annonsklickningar på plattformen. | string |
| `${TM_CLICK_URL_URLENC}` | Den omdirigerings-URL som gör det möjligt för annonsservrar som kräver URL-kodning att spåra och räkna annonsklickningar på plattformen. | string |

{style="table-layout:auto"}

DSP infogar automatiskt klickmakron i en tredjepartstagg när du:

* Exportera annonstaggar från en annonsserverpartner <!-- [Needs PM confirmation.] -->
* Ladda upp [!DNL Flashtalking] eller [!DNL Google DoubleClick for Advertisers] annonstaggar satsvis direkt i DSP

Om ett klickmakro saknas när du skapar en visningsannons visas ett varningsmeddelande i DSP, som uppmanar dig att manuellt infoga rätt visningsklicksmakro i rätt område i taggen.

## [!DNL Analytics for Advertising] makron

Ytterligare makron som är tillgängliga specifikt för [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)-kunder finns i [Bifoga [!DNL Analytics for Advertising] makron till [!DNL Flashtalking] Lägg till taggar](/help/integrations/analytics/macros-flashtalking.md) och [Bifoga [!DNL Analytics for Advertising] makron till [!DNL Google Campaign Manager 360] Lägg till taggar](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

## Felsökning av makrofel

När du lägger till makron i koden måste du använda makrots exakta syntax. När du validerar makrona kontrollerar DSP att makrot exakt matchar något av de giltiga makrona.

Fel genereras om tecken saknas i början eller slutet av makronamnet. Ett felmeddelande visas till exempel om:

* Du glömmer ett eller flera av tecknen i början av makronamnet, till exempel `${`. Om du inte inkluderar den fullständiga syntaxen kan posten inte tolkas som ett giltigt makro.
* Makrot avslutas inte med en giltig teckenuppsättning, till exempel `}`.

>[!MORELIKETHIS]
>
>* [Inställningar för ljudannons](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Inställningar för ansluten TV-annons](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Inställningar för visningsannons](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Inställningar för mobilannonsering](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Inbyggda annonsinställningar](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Inställningar för annonsering före registrering](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Universella inställningar för videoannonsering](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
