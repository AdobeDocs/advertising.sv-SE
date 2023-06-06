---
title: Replikera [!DNL Google Ads] kampanjer i [!DNL Microsoft® Advertising]
description: Lär dig hur du exporterar synkroniserade kampanjer i en [!DNL Google Ads] konto direkt i en synkroniserad [!DNL Microsoft® Advertising] konto.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Replikera [!DNL Google Ads] kampanjer i [!DNL Microsoft® Advertising]

Du kan exportera dina synkroniserade kampanjer i en [!DNL Google Ads] konto direkt i en synkroniserad [!DNL Microsoft® Advertising] som utökade CPC-kampanjer (eCPC). Befintliga anbud och kampanjbudgetar skalas. Befintlig sökning, social spårning och handelsspårning importeras inte.

Du kan replikera följande typer av kampanjer och deras kampanjstruktur:

* [!DNL Google Ads] sök- och webbkampanjer i [!DNL Microsoft® Advertising] sök- och displaykampanjer.

* [!DNL Google Display Network] kampanjer, inklusive annonser, i [!DNL Microsoft® Advertising] målgruppskampanjer i Microsoft® Audience Network.

   Om du vill upprepa shoppingbaserade displaykampanjer måste du först upprepa [!DNL Google Merchant Center] erbjuder [!DNL Microsoft® Merchant Center]. När du replikerar kampanjerna väljer du [!DNL Microsoft® Merchant Center] lagra i Importalternativen för att länka butiken till era feedbaserade målgruppskampanjer.

* [!DNL Google Ads] max-kampanjer, inklusive lokala annonser, i [!DNL Microsoft® Advertising] smarta shoppingkampanjer.

Du kan välja att uppdatera kampanjerna en gång; varje vecka eller varje månad, eller enligt [!DNL Microsoft® Advertising]Rekommenderat schema. Du kan konfigurera meddelanden varje gång ett importjobb körs eller när fel eller ändringar inträffar. När ni har importerat era kampanjer till [!DNL Microsoft® Advertising]kan du kontrollera status för importjobbet, granska felloggar, manuellt köra ett importjobb samt redigera, pausa, aktivera eller ta bort importschemat.

All kampanjinformation replikeras inte och du kan behöva lägga till viss information i [!DNL Microsoft® Advertising] kampanjer. Mer information om vilka data som importeras finns i [!DNL Microsoft® Advertising] hjälp om &quot;[Vad importeras från [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Eftersom sökning, social spårning och handelsspårning inte importeras bör du även lägga till spårning i dialogrutan [konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), eller [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) inställningar.

## Replikera [!DNL Google Ads] kampanjer

>[!NOTE]
>
>Om du vill upprepa shoppingbaserade displaykampanjer börjar du med att [replikera [!DNL Google Merchant Center] erbjuder [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). När du replikerar kampanjerna väljer du [!DNL Microsoft® Merchant Center] lagra importalternativen för att länka butiken till era feedbaserade målgruppskampanjer.

Se [vad som importeras från [!DNL Google Ads] kampanjer](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Hämta ett ID för importautentiseringsuppgifter från [!DNL Microsoft® Advertising] för att representera [!DNL Google Ads] autentiseringsuppgifter.

   Automatisk generering av [!DNL Microsoft® Advertising] autentiseringsuppgifter för import är inte tillgängliga på grund av [!DNL Microsoft® Advertising] API-begränsningar. Kontakta Adobe tekniska support eller ditt kontoteam på Adobe, så genererar de autentiseringsuppgifterna och ger dig ID:t.

   Du måste ha ett ID för att konfigurera importjobbet.

1. På huvudmenyn Sök, Socialt, &amp; Commerce klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicka på **[!UICONTROL +Import]**.

1. Ange [importinställningar](#campaign-import-settings):

   1. I **[!UICONTROL Select accounts]** väljer du käll- och målkonton och det autentiserings-ID som [!DNL Microsoft® Advertising] kräver.

   1. I **[!UICONTROL Select campaigns & ad groups]** anger du de kampanjer och annonser som ska importeras.

   1. I **[!UICONTROL Customize your import]** anger du de objekttyper som ska importeras.

   1. I **[!UICONTROL Set schedule]** anger du när importjobbet ska köras.

1. Klicka på **[!UICONTROL Post]**.

1. (Valfritt) Lägg till sökning, social- och handelsspårning i [konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [kampanj](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [annonsgrupp](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), eller [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) inställningar.

## Redigera information för ett kampanjimportjobb

Se [vad som importeras från [!DNL Google Ads] kampanjer](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Markera kryssrutan bredvid importjobbet och klicka sedan på ![Redigera](/help/search-social-commerce/assets/edit.png "Redigera").

1. Redigera [importinställningar](#campaign-import-settings).

   1. I **[!UICONTROL Select accounts]** väljer du käll- och målkonton och det autentiserings-ID som [!DNL Microsoft® Advertising] kräver.

   1. I **[!UICONTROL Select campaigns & ad groups]** anger du de kampanjer och annonser som ska importeras.

   1. I **[!UICONTROL Customize your import]** anger du de objekttyper som ska importeras.

   1. I **[!UICONTROL Set schedule]** anger du när importjobbet ska köras.

1. Klicka på **[!UICONTROL Post]**.

## Visa kampanjimportjobb

Du kan visa alla importjobb, inklusive källan [!DNL Google Ads] konto, målet [!DNL Microsoft® Advertising] konto, importtid eller importschema samt användaren som skapade jobbet. När du kör ett importjobb flera gånger, inklusive vid regelbundet schemalagda importer, listas varje förekomst som ett separat jobb.

* Gör något av följande:

   * På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

      Som standard öppnas vyn i [!UICONTROL List of Import Jobs] -fliken.

   * Från [[!UICONTROL Import Logs] tab](#campaign-import-log)klickar du på **[!UICONTROL List of Import Jobs]** -fliken.

## Kör ett kampanjimportjobb

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Markera kryssrutan bredvid importjobbet.

1. Klicka ![Kör nu](/help/search-social-commerce/assets/run.png "Kör nu").

## Visa loggar för kampanjimportjobb {#campaign-import-log}

Du kan visa alla slutförda eller misslyckade importjobb, inklusive starttiden, källan [!DNL Google Ads] konto, målet [!DNL Microsoft® Advertising] konto, den användare som skapade jobbet, antalet slutförda och misslyckade åtgärder samt e-postadresser som tagit emot meddelanden för varje jobb. Du kan visa mer information om ändringarna av målet [!DNL Microsoft® Advertising] konto som inträffade för varje jobb, inklusive antalet objekt som lagts till, synkroniserats, tagits bort och som genererade fel för varje entitetsnivå (till exempel kampanj eller nyckelord) i kontot.

1. På huvudmenyn klickar du på **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicka på **[!UICONTROL Import Logs]** -fliken.

1. (Valfritt) Om du vill visa information om ett importjobb klickar du på värdet i [!UICONTROL Summary] kolumn.

## Inställningar för kampanjimportjobb {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Det synkroniserade [!DNL Google Ads] konto som kampanjdata exporteras från.

**[!UICONTROL Credential ID]:** Ett ID som [!DNL Microsoft® Advertising] använder [!DNL Google Ads] autentiseringsuppgifter.

Automatisk generering av [!DNL Microsoft® Advertising] autentiseringsuppgifter för import är inte tillgängliga på grund av [!DNL Microsoft® Advertising] begränsningar. Kontakta Adobe tekniska support eller ditt kontoteam på Adobe, så genererar de autentiseringsuppgifterna och ger dig ID:t.

**[!UICONTROL Target Microsoft® Ads account]:** Det synkroniserade [!DNL Microsoft® Advertising] vilket konto kampanjdata importeras till.

### [!UICONTROL Select campaigns & ad groups]

**\[Data att importera\]:** Ange de data som ska importeras:

* *[!UICONTROL Import all new and existing campaigns]:* Importera data för alla kampanjer som redan finns och kampanjer som inte finns i [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Välj specifika kampanjer och annonsgrupper.

   * Om du vill expandera en kampanj till dess underordnade annonsgrupper klickar du på **[!UICONTROL >]** efter kampanjnamnet.

   * Om du vill välja en kampanj eller annonsgrupp markerar du objektet så att en bock visas.

   * Så här tar du bort en kampanj eller annonsgrupp:

      * I [!UICONTROL Campaigns] eller [!UICONTROL Adgroups] avmarkera kampanjen eller annonsgruppen så att bockmarkeringen försvinner.

      * I [!UICONTROL Selected] kolumn, klicka ![Ta bort](/help/search-social-commerce/assets/delete.png "Ta bort").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Gör att du kan ange vad som ska importeras, bud och budgetar samt andra alternativ.

**[!UICONTROL What to import]:** Definierar de objekt som ska importeras. Alternativ för att importera artikelkategorier markeras som standard, med alla objekttyper markerade. Om du bara vill inkludera vissa objekttyper klickar du på **[!UICONTROL Show advanced options]** och ändra de objekttyper som ska inkluderas.

**[!UICONTROL Bids and budgets]:** Definierar vilka köp- och budgetinställningar som ska importeras, uppdateras och anpassas.

**[!UICONTROL Other options]:** Definierar hur importerade URL:er för landningssidor, spårningsmallar och andra alternativ för kampanjer, annonser och målinriktning ska hanteras.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Importjobbets namn.

**[!UICONTROL When]:** När de angivna kampanjerna ska importeras: *Auto* (för att [!DNL Microsoft® Advertising] ange ett schema för att optimera era kampanjer), *[!UICONTROL Now]* (för att köra jobbet när du bokför jobbinställningarna), *[!UICONTROL Once]* vid en viss tidpunkt, *[!UICONTROL Daily]* vid en viss tidpunkt, *[!UICONTROL Weekly]* vid en viss tidpunkt, eller *[!UICONTROL Monthly]* vid en angiven tidpunkt.

**[!UICONTROL Receive email notifications]:** Om och när e-postmeddelanden om importjobb ska skickas till e-postadresserna i fältet Skicka rapporter till.

**[!UICONTROL Send reports to]:** E-postadresser som tar emot meddelanden om importjobb. Avgränsa flera adresser med kommatecken (`,`).
