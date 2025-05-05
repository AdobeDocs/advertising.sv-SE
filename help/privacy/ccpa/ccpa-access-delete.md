---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer Data Access and Delete Support
description: Lär dig mer om vilka dataförfrågningstyper som stöds, obligatoriska inställnings- och fältvärden samt exempel på API-åtkomstbegäranden som använder äldre produkt-ID:n och returnerade datafält.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: a3e39ca4fa89f84ddc2669662c34bccb4425a2bb
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support

*För [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; och Adobe Advertising DCO*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om Kaliforniens konsumentsekretesslag.

California Consumer Privacy Act (CCPA) är Kaliforniens nya integritetslag, som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina personuppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Advertising support så att ditt företag kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av Adobe Advertising produkter och tjänster, inklusive hantering av förfrågningar om åtkomst och radering av personuppgifter och hantering av förfrågningar om att avanmäla försäljning av personuppgifter.

I det här dokumentet beskrivs hur [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); och [!DNL Advertising DCO] - som tjänsteleverantörer - stöder konsumenternas rättigheter att få tillgång till och ta bort personuppgifter med Adobe [!DNL Experience Platform Privacy Service API] och [!DNL Privacy Service UI].

Information om hur Advertising DSP stöder konsumentens rätt att avanmäla sig från försäljning av personuppgifter finns i [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Mer information om Adobe sekretesstjänster för CCPA finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Dataförfrågningstyper som stöds för Adobe Advertising

Adobe Experience Platform ger företag möjlighet att utföra följande uppgifter:

* Få åtkomst till data på cookie-nivå eller data på enhets-ID-nivå (för annonser i mobilappar) inom [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] eller [!DNL DCO].
* Ta bort data på cookie-nivå som lagras i [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] eller [!DNL DCO] för konsumenter med en webbläsare, eller ta bort data på ID-nivå som lagras i [!DNL DSP] för konsumenter med appar på mobila enheter.
* Kontrollera status för en eller alla befintliga begäranden.

## Nödvändiga inställningar för att skicka begäranden för Adobe Advertising

Om du vill begära åtkomst till och radera konsumentpersonuppgifter från Adobe Advertising måste du:

1. Distribuera ett JavaScript-bibliotek för att hämta och ta bort kundens cookies. Samma bibliotek `AdobePrivacy.js` används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Adobe Advertising kräver det.

   Du bör distribuera biblioteket på den webbsida från vilken dina kunder kan skicka in begäran om åtkomst och borttagning, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta Adobe-cookies (namnområdes-ID: `gsurferID`) så att du kan skicka dessa identiteter som en del av begäran om åtkomst och borttagning via [!DNL Adobe Experience Platform Privacy Service API].

   När kunden begär att få ta bort personuppgifter tar biblioteket också bort kundens cookie från kundens webbläsare.

   >[!NOTE]
   >
   >Att ta bort personuppgifter skiljer sig från att avanmäla sig, vilket förhindrar målgruppsanpassningen för en slutanvändare med målgruppssegment. När en konsument begär att få ta bort personuppgifter från [!DNL Creative], [!DNL DSP] eller [!DNL DCO] skickar biblioteket också en begäran till Adobe Advertising om att avanmäla kunden från segmentmålanpassning. För annonsörer med [!DNL Search, Social, & Commerce] rekommenderar vi att du ger dina kunder en länk till [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse) som förklarar hur du avanmäler dig från målgruppssegmentering.

1. Identifiera ditt företags-ID för Experience Cloud och se till att det är länkat till dina Adobe Advertising-konton.

   Ett företags-ID från Experience Cloud är en 24-tecken lång alfanumerisk sträng som läggs till med &quot;@AdobeOrg&quot;. De flesta Experience Cloud-kunder har tilldelats ett företags-ID. Om ditt marknadsföringsteam eller den interna [!DNL Adobe]-systemadministratören inte känner till ditt organisations-ID, eller inte vet om det har etablerats, kontaktar du ditt Adobe-kontoteam. Du behöver organisations-ID:t för att kunna skicka begäranden till sekretess-API:t med namnområdet `imsOrgID`.

   >[!IMPORTANT]
   >
   >Kontakta företagets Adobe Advertising-representant för att bekräfta att alla din organisations Adobe Advertising-konton - inklusive [!DNL DSP]-konton eller annonsörer, [!DNL Search, Social, & Commerce]-konton och [!DNL Creative]- eller [!DNL DCO]-konton - är kopplade till ditt Experience Cloud organisations-ID.

1. Använd antingen [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=sv-SE) (för automatiserade begäranden) eller [Privacy Service-gränssnittet](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=sv-SE) (för ad hoc-begäranden) för att skicka begäranden om åtkomst och radering av personuppgifter till Adobe Advertising för konsumenternas räkning och för att kontrollera status för befintliga förfrågningar.

   För annonsörer som har en mobilapp att interagera med kunder och starta kampanjer med [!DNL DSP] måste du hämta sekretessfärdiga SDK:er för Experience Cloud. Med Mobile SDK:er kan företag ange statusflaggor för avanmälan, hämta konsumentens enhets-ID (namnområdes-ID: `deviceID`) och skicka begäranden till Privacy Service API. Mobilappen kräver SDK Version 4.15.0 eller senare.

   När du skickar en begäran om konsumentåtkomst, returnerar Privacy Service-API kundens information baserat på den angivna cookien eller det angivna enhets-ID:t, som du sedan måste returnera till konsumenten.

   När du skickar en begäran om att ta bort en kund tas cookie-ID:t eller enhets-ID:t och alla kostnads-, klicknings- och intäktsdata som är kopplade till cookien bort från servern.

   >[!NOTE]
   >
   >Om ditt företag har flera Experience Cloud organisation-ID:n måste du skicka separata API-förfrågningar för varje. Du kan dock göra en API-begäran till flera Adobe Advertising-underlösningar ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] och [!DNL DCO]), med ett konto per underlösning.

Alla steg är nödvändiga för att få support från Adobe Advertising. Mer information om dessa och andra relaterade uppgifter som du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar objekten som behövs, finns på [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=sv-SE](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=sv-SE).

## Obligatoriska fältvärden i Adobe Advertising JSON-begäranden

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ditt företags-ID*>

användare:

* `"key":` &lt;*vanligtvis kundens namn*>

* `"action":` antingen `**access**` eller `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (vilket anger [[!DNL AdCloud] cookie space](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/api/appendix))

   * `"value":` &lt;*den faktiska kundens cookie-ID som hämtats från`AdobePrivacy.js`*>

* `"include": **adCloud**` (som är den [[!DNL Adobe] produkt](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/api/appendix) som gäller för begäran)

* `"regulation": **ccpa**` (som är den sekretessregel som gäller för begäran)

## Exempel på begäran som har skickats av en konsument med ett användar-ID från Adobe Advertising som har hämtats från AdobePrivacy.js

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
    "regulation":"ccpa"
}
```

## Datafält som returneras för åtkomstbegäranden

Nedan följer ett exempel på ett personligt informationsåtkomstsvar för Adobe Advertising.

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
