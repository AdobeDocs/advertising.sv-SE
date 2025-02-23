---
title: Tillgängliga makron för att spåra URL:er
description: Referera till de makron som du kan lägga till i URL:er för spårning av landningssidor och andra kreatörer.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: 40a8afc7ec8d880137493118efb122778704eb8c
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Tillgängliga makron för att spåra URL:er

*Stängd beta*

<!-- More feature metadata??? -->

Du kan inkludera följande makron i dina tredjepartsskapare, i spårnings-URL:er från tredje part för dina upplevelser och i landningssidans URL:er för eget bruk.

Vissa av de tillgängliga makrona, eller deras motsvarigheter, inkluderas automatiskt i upplevelsetaggar.

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| Makro | Beskrivning | Vill du att upplevelsetaggar för Advertising DSP ska infogas automatiskt? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Spårar och rapporterar kampanj-ID:t från DSP | Ja |
| `${TM_SITE_ID_NUM}` | Spårar och rapporterar webbplats-ID:t från DSP | Ja |
| `${TM_PLACEMENT_ID_NUM}` | Spårar och rapporterar placering-ID:t från DSP | Ja |
| `${TM_AD_ID_NUM}` | Spårar och rapporterar annons-ID från DSP | Ja |
| `${TM_CREATIVE_ID_NUM}` | Spårar och rapporterar det kreativa ID:t från DSP | Ej tillämpligt |
| `${TM_SESSION_ID}` | Spårar och rapporterar intrycks-ID från DSP. Om ett värde inte returneras genereras ett. | Ja |
| `${TM_ACC_EXPERIENCE_ID}` | Spåra och rapportera Advertising Creative upplevelse-ID | — |
| `${TM_ACC_CREATIVE_ID}` | Spårar och rapporterar Advertising Creative Creative ID | — |
| `${TM_RANDOM}` | Ett slumpmässigt tal mellan 1 och 100000 | — |
| `${TM_TIMESTAMP}` | Unix-tidsstämpeln (i sekunder) | — |
| `${TM_CLICK_URL_URLENC}` | (För annonser från tredje part från leverantörer som kräver URL-kodning) Den kodade klickomdirigerings-URL:en, som gör att annonsservrar kan spåra och räkna annonsklickningar. När annonsen visas och användaren klickar på den aktiveras makrot och klickningen registreras och räknas i rapporteringssyfte. | Ja |

>[!MORELIKETHIS]
>
>* [Lägg till standardkreatörer i ett kreativt bibliotek](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Standardinställningar för kreativitet](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* 
