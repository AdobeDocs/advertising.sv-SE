---
title: Synkronisera [!DNL Adobe] målgrupper
description: Lär dig hur du synkroniserar metadata, hierarkidata och unika målgruppsdata för dina [!DNL Adobe] målgrupper.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Synkronisera [!DNL Adobe] målgrupper

Endast *[!DNL Direct Access]klienthanterare och administratörer*

*Annonsörer med endast integrering mellan Adobe Advertising, Adobe Audience Manager och Adobe Advertising och Adobe Analytics*

Du kan tillåta att Search, Social och Commerce hämtar in metadata, hierarkidata och unika målgruppsdata för alla en annonsörs eller annonsörs [!DNL Adobe] målgrupper i [!UICONTROL Campaigns] > [!UICONTROL Audiences] -vyer. Denna information innehåller uppgifter om

* Adobe Audience Manager segment

* Adobe Analytics-segment som publiceras till Adobe Experience Cloud

* Segment som har skapats med Adobe Experience Cloud [!DNL Audience Library]

För att vara berättigad måste annonsören eller reklambyrån implementera [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) och ange sitt organisations-ID (kallades tidigare [!DNL IMS Org ID]).

Den första synkroniseringen tar ca 24 timmar. Efter det synkroniseras data i realtid med en fördröjning på en till två sekunder.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]** på huvudmenyn.

1. Ange det unika organisations-ID:t för annonserarens Adobe Experience Cloud-konto och klicka sedan på **[!UICONTROL Submit]**.

   Om du inte känner till annonsörens organisations-ID kan du slå upp det i fältet **[!UICONTROL IMS Org ID]** i annonsörens inställningar på [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [Om målgrupper](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integrering med Adobe Experience Cloud lösningar och tjänster](/help/search-social-commerce/introduction/integrations.md)
