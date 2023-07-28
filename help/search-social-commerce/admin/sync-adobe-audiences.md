---
title: Synkronisera [!DNL Adobe] målgrupper
description: Lär dig hur du synkroniserar metadata, hierarkidata och unika målgruppsdata för [!DNL Adobe] målgrupper.
exl-id: 7d4a3c66-5013-412f-8937-d64c336751e3
feature: Search Admin
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Synkronisera [!DNL Adobe] målgrupper

*[!DNL Direct Access]endast klientchefer och administratörer*

*Annonsörer med endast integrering mellan Adobe Advertising, Adobe Audience Manager och Adobe Advertising och Adobe Analytics*

Ni kan låta Search, Social och Commerce hämta in metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers [!DNL Adobe] målgrupper i [!UICONTROL Campaigns] > [!UICONTROL Audiences] vyer. Denna information innehåller uppgifter om

* Adobe Audience Manager segment

* Adobe Analytics-segment som publiceras till Adobe Experience Cloud

* Segment som har skapats med Adobe Experience Cloud [!DNL Audience Library]

För att vara berättigad måste annonsören eller reklambyrån genomföra [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) och ange sitt organisations-ID (kallades tidigare [!DNL IMS Org ID]).

Den första synkroniseringen tar ca 24 timmar. Efter det synkroniseras data i realtid med en fördröjning på en till två sekunder.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Ange det unika organisations-ID:t för annonserarens Adobe Experience Cloud-konto och klicka sedan på **[!UICONTROL Submit]**.

   Om du inte känner till annonsörens organisations-ID kan du slå upp det i **[!UICONTROL IMS Org ID]** i annonserarens inställningar på [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [Om målgrupper](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integrering med Adobe Experience Cloud lösningar och tjänster](/help/search-social-commerce/introduction/integrations.md)
