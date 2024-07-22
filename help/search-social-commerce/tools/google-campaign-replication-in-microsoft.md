---
title: Replikera [!DNL Google Ads] kampanjer i [!DNL Microsoft Advertising]
description: Lär dig hur du exporterar dina synkroniserade kampanjer i ett [!DNL Google Ads] konto direkt till ett synkroniserat [!DNL Microsoft Advertising] konto.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replikera [!DNL Google Ads] kampanjer i [!DNL Microsoft Advertising]

Du kan exportera dina synkroniserade kampanjer i ett [!DNL Google Ads]-konto direkt till ett synkroniserat [!DNL Microsoft Advertising]-konto som eCPC-kampanjer (Enhanced CPC). Befintliga anbud och kampanjbudgetar skalas. Befintlig sökning, social spårning och Commerce-spårning importeras inte.

Du kan replikera följande typer av kampanjer och deras kampanjstruktur:

* [!DNL Google Ads] sök- och displaykampanjer i [!DNL Microsoft Advertising] sök- och displaykampanjer.

* [!DNL Google Display Network] kampanjer, inklusive annonsbilder, till [!DNL Microsoft Advertising] målgruppskampanjer i Microsoft Audience Network.

  Om du vill replikera shoppingbaserade displaykampanjer måste du först replikera dina [!DNL Google Merchant Center]-produkterbjudanden till [!DNL Microsoft Merchant Center]. När du replikerar kampanjer väljer du butiken [!DNL Microsoft Merchant Center] i Importalternativ för att länka butiken till dina feed-baserade målgruppskampanjer.

* [!DNL Google Ads] maximala prestandakampanjer, inklusive lokala lagerannonser, till [!DNL Microsoft Advertising] maximala prestandakampanjer.

Du kan välja att uppdatera kampanjerna en gång, varje dag, varje vecka eller varje månad, eller enligt det rekommenderade schemat för [!DNL Microsoft Advertising]. Du kan konfigurera meddelanden varje gång ett importjobb körs eller när fel eller ändringar inträffar. När du har importerat dina kampanjer till [!DNL Microsoft Advertising] kan du kontrollera status för importjobbet, granska eventuella felloggar, manuellt köra ett importjobb samt redigera, pausa, aktivera eller ta bort importschemat.

All kampanjinformation har inte replikerats och du kan behöva lägga till viss information i dina [!DNL Microsoft Advertising]-kampanjer. Mer information om vilka data som importeras finns i [!DNL Microsoft Advertising]-hjälpen för [Vad importeras från [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851). Eftersom Sökning, Social och Commerce-spårning inte importeras bör du även lägga till spårning i inställningarna för [konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) eller [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) .

## Replikera [!DNL Google Ads] kampanjer

>[!NOTE]
>
>Om du vill replikera shoppingbaserade displaykampanjer måste du först [replikera dina [!DNL Google Merchant Center] produkterbjudanden i [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). När du replikerar kampanjer väljer du butiken [!DNL Microsoft Merchant Center] i importalternativen för att länka butiken till dina feed-baserade målgruppskampanjer.

Se [vad som importeras från [!DNL Google Ads] kampanjer](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** på huvudmenyn Sök, socialt och Commerce.

1. Klicka på **[!UICONTROL +Import]**.

1. Ange [importinställningarna](#campaign-import-settings):

   1. I avsnittet **[!UICONTROL Select accounts]**:

      1. Välj käll- och destinationskonton.

      1. Klicka på **[!UICONTROL Get Credential Id from MSA]**.

      1. Logga in på målkontot [!DNL Microsoft Advertising], kopiera det inloggnings-ID som visas och klistra in värdet i fältet **[!UICONTROL Credential ID]**.

   1. I avsnittet **[!UICONTROL Select campaigns & ad groups]** anger du de kampanjer och annonser som ska importeras.

   1. I avsnittet **[!UICONTROL Customize your import]** anger du de objekttyper som ska importeras.

   1. I avsnittet **[!UICONTROL Set schedule]** anger du när importjobbet ska köras.

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Lägg till sök-, sociala och Commerce-spårning i inställningarna för [kontot](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [kampanjen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [annonsgruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) eller [annonsgruppen](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Redigera schemainställningar för ett kampanjimportjobb

Se [vad som importeras från [!DNL Google Ads] kampanjer](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** på huvudmenyn.

1. Markera kryssrutan bredvid importjobbet och klicka sedan på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. I avsnittet **[!UICONTROL Set schedule]** anger du [schemainställningarna](#campaign-import-settings).

1. Klicka på **[!UICONTROL Post]**.

## Visa kampanjimportjobb

Du kan visa alla importjobb, inklusive källkontot [!DNL Google Ads], målkontot [!DNL Microsoft Advertising], importtiden eller importschemat samt användaren som skapade jobbet. När du kör ett importjobb flera gånger, inklusive vid regelbundet schemalagda importer, listas varje förekomst som ett separat jobb.

* Gör något av följande:

   * Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** på huvudmenyn.

     Vyn öppnas som standard på fliken [!UICONTROL List of Import Jobs].

   * Klicka på fliken **[!UICONTROL List of Import Jobs]** på fliken [[!UICONTROL Import Logs] ](#campaign-import-log).

## Kör ett kampanjimportjobb

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** på huvudmenyn.

1. Markera kryssrutan bredvid importjobbet.

1. Klicka på ![Kör nu](/help/search-social-commerce/assets/run.png "Kör nu").

## Visa loggar för kampanjimportjobb {#campaign-import-log}

Du kan visa alla slutförda eller misslyckade importjobb, inklusive starttid, källkontot [!DNL Google Ads], målkontot [!DNL Microsoft Advertising], användaren som skapade jobbet, antalet slutförda och misslyckade åtgärder samt e-postadresser som tagit emot meddelanden för varje jobb. Du kan visa mer information om ändringarna av målkontot [!DNL Microsoft Advertising] som inträffade för varje jobb, inklusive antalet objekt som lagts till, synkroniserats, tagits bort och som genererade fel för varje entitetsnivå (till exempel kampanj eller nyckelord) i kontot.

1. Klicka på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** på huvudmenyn.

1. Klicka på fliken **[!UICONTROL Import Logs]**.

1. (Valfritt) Om du vill visa information om ett importjobb klickar du på värdet i kolumnen [!UICONTROL Summary].

## Inställningar för kampanjimportjobb {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Det synkroniserade [!DNL Google Ads]-kontot som kampanjdata exporteras från.

**[!UICONTROL Credential ID]:** Ett ID som [!DNL Microsoft Advertising] använder för att representera dina [!DNL Google Ads]-autentiseringsuppgifter.

Automatisk generering av [!DNL Microsoft Advertising]-autentiseringsuppgifter för import är inte tillgänglig på grund av [!DNL Microsoft Advertising]-begränsningar. Kontakta kontoteamet på Adobe så genererar de autentiseringsuppgifterna och ger dig ID:t.

**[!UICONTROL Target Microsoft Ads account]:** Det synkroniserade [!DNL Microsoft Advertising]-kontot som kampanjdata importeras till.

### [!UICONTROL Select campaigns & ad groups]

**\[Data att importera\]:** Ange de data som ska importeras:

* *[!UICONTROL Import all new and existing campaigns]:* Att importera data för alla kampanjer som redan finns och kampanjer som inte finns i [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Välj specifika kampanjer och annonsgrupper.

   * Om du vill expandera en kampanj till dess underordnade annonsgrupper klickar du på **[!UICONTROL >]** efter kampanjnamnet.

   * Om du vill välja en kampanj eller annonsgrupp markerar du objektet så att en bock visas.

   * Så här tar du bort en kampanj eller annonsgrupp:

      * Avmarkera kampanjen eller annonsgruppen i kolumnen [!UICONTROL Campaigns] eller [!UICONTROL Adgroups] så att bockmarkeringen försvinner.

      * Klicka på ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort") i kolumnen [!UICONTROL Selected].

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Gör att du kan ange vad som ska importeras, bud och budgetar samt andra alternativ.

**[!UICONTROL What to import]:** Definierar de objekt som ska importeras. Alternativ för att importera artikelkategorier markeras som standard, med alla objekttyper markerade. Om du bara vill ta med vissa objekttyper klickar du på **[!UICONTROL Show advanced options]** och ändrar objekttyperna till Inkludera.

**[!UICONTROL Bids and budgets]:** Definierar vilka köp- och budgetinställningar som ska importeras, uppdateras och anpassas.

**[!UICONTROL Other options]:** Definierar hur importerade URL-adresser för landningssidor, spårningsmallar och andra alternativ för kampanj, annonsering och målinriktning ska hanteras.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Importjobbets namn.

**[!UICONTROL When]:** När de angivna kampanjerna ska importeras: *Auto* (för att [!DNL Microsoft Advertising] ska kunna ange ett schema som optimerar dina kampanjer), *[!UICONTROL Now]* (för att köra jobbet när du bokför jobbinställningarna), *[!UICONTROL Once]* vid en angiven tidpunkt, *[!UICONTROL Daily]* vid en angiven tidpunkt, *[!UICONTROL Weekly]* vid en angiven tidpunkt eller *[!UICONTROL Monthly]* vid en angiven tidpunkt.

**[!UICONTROL Receive email notifications]:** Om och när e-postmeddelanden om importjobb ska skickas till e-postadresserna i fältet Skicka rapporter till.

**[!UICONTROL Send reports to]:** E-postadresser som tar emot meddelanden om importjobb. Avgränsa flera adresser med kommatecken (`,`).
