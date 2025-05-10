---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale Support
description: Läs mer om stöd för att hämta in förfrågningar om att avanmäla sig från försäljning till konsumenter.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-Out of Sale Support

*För Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om Kaliforniens konsumentsekretesslag.

California Consumer Privacy Act (CCPA) är Kaliforniens nya integritetslag, som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina uppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Advertising support så att ditt företag kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av Adobe Advertising produkter och tjänster, inklusive hantering av kundförfrågningar om åtkomst och radering av personuppgifter och hantering av konsumentförfrågningar om att avanmäla försäljning av personuppgifter.

I det här dokumentet beskrivs hur Adobe Advertising Demand Side Platform (DSP), som tjänsteleverantör, stöder konsumentens rätt att välja bort&quot;försäljning&quot; av&quot;personuppgifter&quot;, eftersom varje term definieras av CCPA. Det innehåller information om hur man skickar avanmälningsförfrågningar till Adobe Advertising och hur man hämtar rapporter om organisationens avanmälningsförfrågningar.

Mer information om hur [!DNL Advertising Search, Social, & Commerce], Advertising Creative och [!DNL Advertising DCO] ger stöd åt konsumenternas behörigheter för åtkomst och borttagning av personuppgifter finns i [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ccpa/ccpa-access-delete.md).

Mer information om Adobe sekretesstjänster för CCPA finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Kommunicera förfrågningar om avanmälan till Adobe Advertising

Du kan förmedla önskemål om avanmälan från försäljning till konsumenter genom att antingen:

* ett avanmälningssegment för CCPA som skapats i Advertising DSP
* ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API

### Metod 1: Kommunicera CCPA-begäranden om att avanmäla sig från försäljning med ett [!UICONTROL CCPA Opt-Out-of-Sale]-segment i Advertising DSP

>[!NOTE]
>
>Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

1. Logga in på annonsörens konto i Advertising DSP på [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Skapa ett CCPA-segment för avanmälan från försäljning och implementera segmentpixeln för att hämta avanmälningsbegäranden](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Metod 2: Kommunicera CCPA-förfrågningar om att avanmäla sig från försäljning med hjälp av Adobe Experience Platform Privacy Service API

*Annonsörer tilldelade endast ett Adobe Experience Cloud-organisations-ID*

1. Distribuera ett JavaScript-bibliotek för att hämta kundens cookies. Samma bibliotek `AdobePrivacy.js` används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Adobe Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Adobe Advertising kräver det.

   Du bör distribuera biblioteket på webbsidan där dina kunder kan skicka in begäranden om att avanmäla dig, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta Adobe-cookies (namnområdes-ID: `gsurferID`) så att du kan skicka dessa identiteter som en del av begäran om att avanmäla dig via Adobe Experience Platform Privacy Service API.

1. Identifiera ditt företags-ID för Experience Cloud och se till att det är länkat till dina Adobe Advertising-konton.

   Ett företags-ID från Experience Cloud är en 24-tecken lång alfanumerisk sträng som läggs till med &quot;@AdobeOrg&quot;. De flesta Experience Cloud-kunder har tilldelats ett företags-ID. Om marknadsföringsteamet eller den interna systemadministratören i Adobe inte känner till ditt företags-ID eller inte vet om det har etablerats kontaktar du ditt Adobe-kontoteam. Du behöver organisations-ID:t för att kunna skicka begäranden till sekretess-API:t med namnområdet `imsOrgID`.

   >[!IMPORTANT]
   >
   >Kontakta företagets Adobe Advertising-representant för att bekräfta att alla din organisations Adobe Advertising-konton - inklusive [!DNL DSP]-konton eller annonsörer, [!DNL Search, Social, & Commerce]-konton och [!DNL Creative]- eller [!DNL DCO]-konton - är kopplade till ditt Experience Cloud organisations-ID.

1. Använd Adobe Experience Platform Privacy Service-API:t för att [skicka begäran om avanmälan](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html?lang=sv-SE) till Adobe Advertising för konsumenternas räkning och för att kontrollera status för befintliga begäranden.

   Se bilagan nedan för ett exempel på en begäran om avanmälan från försäljning.

   >[!NOTE]
   >
   >Om ditt företag har flera Experience Cloud organisation-ID:n måste du skicka separata API-förfrågningar för varje. Du kan dock göra en API-begäran till flera Adobe Advertising-underlösningar ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] och [!DNL DCO]), med ett konto per underlösning.

Alla dessa steg är nödvändiga för att få support från Adobe Advertising. Mer information om dessa och andra relaterade uppgifter som du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar objekten som behövs, finns på [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=sv-SE](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=sv-SE).

## Hämtar rapporter om konsumenter som har lämnat in begäran om avanmälan vid försäljning

Adobe Advertising genererar månatliga rapporter om ID:n som kunder har skickat in för att avanmäla sig från försäljning för kontot. Varje rapport är tillgänglig som en tabbseparerad textfil komprimerad till GZIP-format. Data konsoliderar begäranden som samlats in med CCPA-segmentet för avanmälan som skapats i Advertising DSP och alla inlämningar som gjorts via Privacy Service API. Användar-ID:n som används i CCPA-segment för avanmälan identifieras av segment och annonsörer. Rapporterna skapas den första i varje månad för föregående månad. Till exempel är användarlistan för juni tillgänglig den 1 juli.

Du kan hämta länkar till de månadsrapporter som har skapats under de senaste tre månaderna, antingen från Advertising DSP eller via Advertising DSP [!DNL Trafficking API]. Varje länk gäller i sju dagar, men uppdateras varje gång en kund försöker hämta en länk.

### Metod 1: Hämta rapporter om konsumentens avanmälan från försäljning inom Advertising DSP

1. Logga in på annonsörens konto i Advertising DSP på [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Hämta rapporterna](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Metod 2: Hämta rapporter om konsumentavanmälan från försäljning med Advertising DSP [!DNL Trafficking API]

Den här funktionen är tillgänglig för organisationer som använder [!DNL Trafficking API]. Mer information finns i dokumentationen för [!DNL Trafficking API].<!-- Add link to API doc once it's published. -->

Om din organisation inte använder [!DNL Trafficking API] men är intresserad av mer information kan du kontakta ditt Adobe-kontoteam.

## Bilaga: Exempel på [!UICONTROL CCPA Opt-Out-of-Sale]-begäran för Privacy Service API-användare

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

var, enligt [API-specifikationerna för Privacy Service](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` anger cookie-utrymmet `AdCloud` och det motsvarande värdet är kundens cookie-ID som hämtats från `AdobePrivacy.js`
* `"include": ["adCloud"]` anger att begäran gäller för produkten Adobe Advertising
