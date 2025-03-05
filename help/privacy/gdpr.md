---
title: Adobe Advertising Support for the General Data Protection Regulation
description: Lär dig mer om vilka dataförfrågningstyper som stöds, obligatoriska inställnings- och fältvärden samt exempel på API-åtkomstbegäranden som använder äldre produkt-ID:n och returnerade datafält
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Adobe Advertising Support for the General Data Protection Regulation

*För [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; och Adobe Advertising DCO*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om den allmänna dataskyddsförordningen.

Den allmänna dataskyddsförordningen (GDPR), som är en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter och förenklar regelmiljön för den internationella verksamheten. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som personuppgiftsbiträde för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvarig avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

I det här dokumentet beskrivs hur [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); och [!DNL Advertising DCO] stöder de registrerade personernas GDPR-behörighet för dataåtkomst och borttagning med Adobe Experience Platform Privacy Service API och Privacy Service UI.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och ditt företag](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Dataförfrågningstyper som stöds för Adobe Advertising

Adobe Experience Platform ger företag möjlighet att utföra följande uppgifter:

* Åtkomst till data på cookie-nivå eller data på enhets-ID-nivå för en datamedlem (för annonser i mobilappar) inom [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] eller [!DNL DCO].
* Ta bort data på cookie-nivå som lagras i [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] eller [!DNL DCO] för registrerade i en webbläsare, eller ta bort data på ID-nivå som lagras i [!DNL DSP] för registrerade som använder appar på mobila enheter.
* Kontrollera status för en eller alla befintliga begäranden.

## Nödvändiga inställningar för att skicka begäranden för Adobe Advertising

För att begära åtkomst till och radering av data för Adobe Advertising måste du:

1. Distribuera ett JavaScript-bibliotek för att hämta och ta bort era cookies för registrerade användare. Samma bibliotek `AdobePrivacy.js` används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Adobe Advertising kräver det.

   Du bör distribuera biblioteket på den webbsida från vilken de registrerade kan skicka in begäran om åtkomst och borttagning, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta [!DNL Adobe] cookies (namnområdes-ID: `gsurferID`) så att du kan skicka dessa identiteter som en del av begäran om åtkomst och borttagning via Adobe Experience Platform Privacy Service API.

   När den registrerade begär att få ta bort personuppgifter tar biblioteket också bort den registrerades cookie från den registrerades webbläsare.

   >[!NOTE]
   >
   >Att ta bort personuppgifter skiljer sig från avanmäl dig, vilket stoppar målsättningen för en slutanvändare med målgruppssegment. När en registrerade begär att få ta bort personuppgifter från [!DNL Creative], [!DNL DSP] eller [!DNL DCO] skickar biblioteket också en begäran till Adobe Advertising om att avanmäla den registrerade från segmentmål. För annonsörer med [!DNL Search, Social, & Commerce] rekommenderar vi att du ger de registrerade en länk till [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html) som förklarar hur du avanmäler målgruppsanpassning för målgruppssegment.

1. Identifiera ditt företags-ID för Experience Cloud och se till att det är länkat till dina Adobe Advertising-konton.

   Ett företags-ID från Experience Cloud är en 24-tecken lång alfanumerisk sträng som läggs till med &quot;@AdobeOrg&quot;. De flesta Experience Cloud-kunder har tilldelats ett företags-ID. Om ditt marknadsföringsteam eller den interna [!DNL Adobe]-systemadministratören inte känner till ditt företags-ID, eller inte vet om det har etablerats, kontaktar du Adobe kundtjänst på gdprsupport@adobe.com. Du behöver organisations-ID:t för att kunna skicka begäranden till sekretess-API:t med namnområdet `imsOrgID`.

   >[!IMPORTANT]
   >
   >Kontakta företagets Adobe Advertising-representant för att bekräfta att alla din organisations Adobe Advertising-konton - inklusive [!DNL DSP]-konton eller annonsörer, [!DNL Search, Social, & Commerce]-konton och [!DNL Creative]- eller [!DNL DCO]-konton - är kopplade till ditt Experience Cloud organisations-ID.

1. Använd antingen [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (för automatiska begäranden) eller [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (för ad hoc-begäranden) för att skicka åtkomst- och borttagningsbegäranden till Adobe Advertising för de registrerade och för att kontrollera status för befintliga begäranden.

   För annonsörer som har en mobilapp för att interagera med registrerade personer och lansera kampanjer med DSP måste du ladda ned de sekretessfärdiga SDK:erna för Experience Cloud. Tack vare SDK för mobiler kan datatekniker ange statusflaggor för avanmälan, hämta den registrerade personens enhets-ID (namnområdes-ID: `deviceID`) och skicka begäranden till Privacy Service API. Mobilappen kräver SDK Version 4.15.0 eller senare.

   När du skickar en begäran om åtkomst för en registrerad returnerar Privacy Service API information för den registrerade baserat på den angivna cookien eller enhets-ID:t, som du sedan måste returnera till den registrerade.

   När du skickar en begäran om borttagning av en registrerad tas cookie-ID:t eller enhets-ID:t och alla kostnads-, klicknings- och intäktsdata som är kopplade till cookien bort från servern.

   >[!NOTE]
   >
   >Om ditt företag har flera Experience Cloud organisation-ID:n måste du skicka separata API-förfrågningar för varje. Du kan dock göra en API-begäran till flera Adobe Advertising-underlösningar ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] och [!DNL DCO]), med ett konto per underlösning.

Alla steg är nödvändiga för Adobe Advertising. Mer information om dessa och andra relaterade uppgifter som du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar objekten som behövs, finns i &quot;[Privacy Service - översikt](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)&quot;.

## Obligatoriska fältvärden i Adobe Advertising JSON-begäranden

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ditt företags-ID*>

`"users":`

* `"key":` &lt;*vanligtvis namnet på dataobjektet*>

* `"action":` antingen `**access**` eller `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (vilket anger cookie-utrymmet [!DNL adcloud])

   * `"value":` &lt;*den faktiska datamottagarens cookie-ID som hämtats från`AdobePrivacy.js`*>

* `"include": **adCloud**` (som är den [!DNL Adobe] produkten som gäller för begäran)

* `"regulation": **gdpr**` (som är den sekretessregel som gäller för begäran)

## Exempel på begäran som skickats av den registrerade med ett användar-ID för Adobe Advertising som hämtats från `AdobePrivacy.js`

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
```

## Datafält som returneras för åtkomstbegäranden

Nedan följer ett exempel på ett åtkomstsvar för Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
