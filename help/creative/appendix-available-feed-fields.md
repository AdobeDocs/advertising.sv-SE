---
title: Tillgängliga fält för dynamiska och feed-filer
description: Lär dig mer om de fält du kan inkludera i de flödesfiler du använder för att skapa dynamiska annonser.
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
source-git-commit: 5bf0474f49160775d31dff0d434ba1e069f27959
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Bilaga: Tillgängliga fält för dynamiska och feed-filer

Följande matningsfält är tillgängliga på Advertising Creative serverdel. Du kan överföra en [feed](/help/creative/feeds/asset-manage.md) som använder dina organisationsspecifika fältnamn. Innan du kan skapa en [katalog](/help/creative/feeds/catalog-manage.md) från din feed-fil måste du mappa varje fält i feed-filen till något av följande fält i [feed-mallen](/help/creative/feeds/feed-template-manage.md) som du använder för att skapa katalogen.

Det enda fältet som måste ha en motsvarighet i din feed-fil är `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Fältnamn | Datatyp | Obligatoriskt? |
|------------|-----------|-----------|
| AD_SIZE | varchar(32) | NEJ |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NEJ |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NEJ |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NEJ |
| AREA_CODE | text | NEJ |
| AUDIENCE_SEGMENT | text | NEJ |
| LJUD_1 | varchar(1024) | NEJ |
| LJUD_2 | varchar(1024) | NEJ |
| LJUD_3 | varchar(1024) | NEJ |
| LJUD_4 | varchar(1024) | NEJ |
| LJUD_5 | varchar(1024) | NEJ |
| ORT | text | NEJ |
| LAND | text | NEJ |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NEJ |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NEJ |
| DATAPASS_FILTER_1 | text | NEJ |
| DATAPASS_FILTER_2 | text | NEJ |
| DATAPASS_FILTER_3 | text | NEJ |
| DATAPASS_FILTER_4 | text | NEJ |
| DATAPASS_FILTER_5 | text | NEJ |
| RABATT_PRIS | decimal(10,2) | NEJ |
| DMA | text | NEJ |
| BILD | varchar(1024) | NEJ |
| IMAGE_1 | varchar(1024) | NEJ |
| IMAGE_2 | varchar(1024) | NEJ |
| IMAGE_3 | varchar(1024) | NEJ |
| IMAGE_4 | varchar(1024) | NEJ |
| IMAGE_5 | varchar(1024) | NEJ |
| IMAGE_6 | varchar(1024) | NEJ |
| IMAGE_7 | varchar(1024) | NEJ |
| IMAGE_8 | varchar(1024) | NEJ |
| IMAGE_9 | varchar(1024) | NEJ |
| IMAGE_10 | varchar(1024) | NEJ |
| IMAGE_HEIGHT | int | NEJ |
| IMAGE_WIDTH | int | NEJ |
| IS_DEFAULT | enum | NEJ |
| SPRÅK | text | NEJ |
| PART_NUM | varchar(64) | JA |
| PRIS | decimal(10,2) | NEJ |
| PRODUCT_NAME | text | NEJ |
| PRODUCT_URL | text | NEJ |
| PROFILE_FILTER_1 | text | NEJ |
| PROFILE_FILTER_2 | text | NEJ |
| PROFILE_FILTER_3 | text | NEJ |
| PROFILE_FILTER_4 | text | NEJ |
| PROFILE_FILTER_5 | text | NEJ |
| RANK | int | NEJ |
| LÄGE | text | NEJ |
| TEXT_1 | text | NEJ |
| TEXT_2 | text | NEJ |
| TEXT_3 | text | NEJ |
| TEXT_4 | text | NEJ |
| TEXT_5 | text | NEJ |
| TEXT_6 | text | NEJ |
| TEXT_7 | text | NEJ |
| TEXT_8 | text | NEJ |
| TEXT_9 | text | NEJ |
| TEXT_10 | text | NEJ |
| TEXT_11 | text | NEJ |
| TEXT_12 | text | NEJ |
| TEXT_13 | text | NEJ |
| TEXT_14 | text | NEJ |
| TEXT_15 | text | NEJ |
| VIDEO_1 | varchar(1024) | NEJ |
| VIDEO_2 | varchar(1024) | NEJ |
| VIDEO_3 | varchar(1024) | NEJ |
| VIDEO_4 | varchar(1024) | NEJ |
| VIDEO_5 | varchar(1024) | NEJ |
| ZIP | text | NEJ |

>[!MORELIKETHIS]
>
>* [Arbetsflöden för dynamiska annonser](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Hantera resursfiler](/help/creative/feeds/asset-manage.md)
>* [Hantera flödesmallar](/help/creative/feeds/feed-template-manage.md)
>* [Hantera kataloger](/help/creative/feeds/catalog-manage.md)
