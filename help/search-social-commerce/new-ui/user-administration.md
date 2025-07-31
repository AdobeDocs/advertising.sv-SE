---
title: (Nytt användargränssnitt) Användaradministration
description: Lär dig hur du hanterar användaråtkomst.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Nytt användargränssnitt) Användaradministration för sökning, sociala medier och handel

Vissa användare kan hantera åtkomst till det nya användargränssnittet Sök, Sociala och Commerce med hjälp av [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html), som är den centrala platsen för hantering av alla Adobe-berättiganden och användarhantering. Användare kategoriseras som antingen slutanvändare eller administratörer. Adobe-kontogruppen meddelar dig om du är administratör. Om du är administratör kan du läsa följande avsnitt för att identifiera dina behörigheter och arbetsflöden för att hantera användare.

## Typ av administratörer

Admin Console har flera typer av administratörer. Följande administratörstyper och behörigheter krävs för Search, Social och Commerce. Du kan lägga till ytterligare typer om du vill delegera användarhanteringsåtgärder.

**Systemadministratör:** Superanvändare som hanterar alla produkter för organisationen, inklusive alla klientinstanser för organisationen. (Kundinstanser är samma som äldre annonserkonton, med en eller flera instanser per organisations-ID). En systemadministratör kan utföra alla administrativa uppgifter i Admin Console för organisationen och delegera administrativa funktioner till andra användare för någon av organisationens produkter.

**Produktadministratör:** Hanterar åtkomst till en viss [!DNL Adobe]-produkt (som Search, Social och Commerce) och användarrättigheter för den produkten. Produktadministratörer kan skapa produktprofiler för produkten, skapa (men inte ta bort) användare och användargrupper för produkten, lägga till eller ta bort användare och användargrupper från produktprofiler samt lägga till eller ta bort andra produktadministratörer från produkten.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Standardproduktprofiler

Produktprofiler, som liknar roller, ger användare specifika tjänster för en viss produkt.

Det nya användargränssnittet för sökning, sociala medier och handel har följande standardproduktprofiler, som innehåller olika deluppsättningar av funktioner och tjänster. Du kan inte redigera produktbehörigheterna för standardproduktprofilerna eller ta bort standardproduktprofilerna. Produktadministratörer, produktprofiladministratörer och systemadministratörer kan dock vid behov skapa och hantera ytterligare produktprofiler med olika underuppsättningar av tillgängliga behörigheter.

* **[!UICONTROL Basic Optimization]:** Den här profilen innehåller följande funktioner:

   * [!UICONTROL Objectives]: Fullständig åtkomst

   * [!UICONTROL Simulations]: Fullständig åtkomst

   * [!UICONTROL Portfolio Groups]: Fullständig åtkomst

   * [!UICONTROL Portfolios]: Skapa/redigera åtkomst till portföljinställningar för [!UICONTROL Objectives], [!UICONTROL Campaigns] och spendera [!UICONTROL Management]; skrivskyddad åtkomst till de återstående portföljinställningarna.

   * [!UICONTROL Campaigns]: Skrivskyddad åtkomst till kampanjinställningar (inga funktioner för att skapa, redigera eller ta bort är tillgängliga); fullständig åtkomst till begränsningar och portföljtilldelningar

   * [!UICONTROL Ad Groups]: Skrivskyddad åtkomst till inställningar för annonsgrupper (inga funktioner för att skapa, redigera eller ta bort är tillgängliga); fullständig åtkomst till begränsningar och portföljtilldelningar

  Den här åtkomstnivån rekommenderas för användare som fortfarande håller på att lära sig att använda Search, Social och Commerce.

* **[!UICONTROL Expert Optimization]:** Den här profilen innehåller följande funktioner:

   * [!UICONTROL Objectives]: Fullständig åtkomst

   * [!UICONTROL Simulations]: Fullständig åtkomst

   * [!UICONTROL Portfolio Groups]: Fullständig åtkomst

   * [!UICONTROL Portfolios]: Fullständig åtkomst

   * [!UICONTROL Campaigns]: Skrivskyddad åtkomst till kampanjlistan (det finns ännu inga funktioner för att skapa, redigera eller ta bort kampanjer); fullständig åtkomst till begränsningar och portföljtilldelningar

   * [!UICONTROL Ad Groups]: Skrivskyddad åtkomst till annonsgruppslistan (det finns ännu inga funktioner för att skapa, redigera eller ta bort kampanjer); fullständig åtkomst till begränsnings- och portföljtilldelningar

  Den här åtkomstnivån rekommenderas för expertanvändare av Search, Social och Commerce.

* **[!UICONTROL Read-Only]:** Den här profilen innehåller följande funktioner:

   * [!UICONTROL Objectives]: Skrivskyddad åtkomst

   * [!UICONTROL Simulations]: Skrivskyddad åtkomst

   * [!UICONTROL Portfolio Groups]: Skrivskyddad åtkomst

   * [!UICONTROL Portfolios]: Skrivskyddad åtkomst

   * [!UICONTROL Campaigns]: Skrivskyddad åtkomst

   * [!UICONTROL Ad Groups]: Skrivskyddad åtkomst

* **[!UICONTROL Admin]:** Den här profilen ger fullständig åtkomst till alla funktioner som är tillgängliga och tillåter användare att skapa nya klientinstanser (samma som äldre annonserarkonton, med en eller flera instanser per organisations-ID). Tilldela inte den här rättigheten till någon om du inte har en lämplig affärsjustering.

## Uppgifter för administratörer

### Logga in på Adobe Admin Console och öppna det för att söka, socialt och Commerce

>[!PREREQUISITES]
>
>Du måste ha någon typ av administratörsåtkomst till Search, Social och Commerce för att kunna logga in på Admin Console.

1. Gå till https://adminconsole.adobe.com/enterprise/.

1. (Om du inte är inloggad på Experience Cloud) Logga in på Experience Cloud:

   1. Ange ditt [!DNL Adobe]-ID och klicka på **[!UICONTROL Continue]**.

   1. Välj antingen **[!UICONTROL Personal Account] eller &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Välj lämplig Experience Cloud-organisation.

      Admin Console öppnas på fliken [!UICONTROL Overview].

   1. Klicka på [!UICONTROL Product & services] under [!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name].

      Produktsidan öppnas på fliken [!UICONTROL Product profiles] för Search, Social och Commerce. Ytterligare flikar är [!UICONTROL Users] och [!UICONTROL Product Admins].

### Arbetsflöde för systemadministratörer

Följ det här arbetsflödet för varje klientinstans av Search, Social och Commerce.

1. [Logga in på Adobe Admin Console och öppna den för sökning, sociala medier och Commerce](#open-admin-console).

1. (Valfritt) [Lägg till en annan systemadministratör](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) som säkerhetskopia.

1. Delegera produkt- och användarhantering genom att [lägga till produktadministratörer](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Arbetsflöde för produktadministratörer

Följ det här arbetsflödet för varje klientinstans av Search, Social och Commerce.

1. [Logga in på Adobe Admin Console och öppna den för sökning, sociala medier och Commerce](#open-admin-console).

1. Skapa slutanvändare [individuellt](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) eller [ gruppvis](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) efter behov.

1. (Valfritt) Skapa [användargrupper](https://helpx.adobe.com/enterprise/using/user-groups.html) för instansen och tilldela användare till varje användargrupp.

   Om instansen har många användare skapar du användargrupper som ser till att användarna tilldelas rätt profiler utifrån deras kunskapsnivå. (Se steg 4 för att tilldela användargrupper till produktprofiler.) Du kan skapa användargrupper baserat på verksamhetsområde, behov av användaråtkomst, datum för användaruthyrning eller andra kriterier.

   >[!IMPORTANT]
   >
   >Användargruppsnamn ska tydligt informera om vilka rättigheter gruppen med användare ska tilldelas. Om du till exempel vill skapa en användargrupp med behörigheten&quot;Skrivskyddad&quot; inkluderar du&quot;Skrivskyddad&quot; i användargruppens namn, till exempel&quot;Acme_Uk_ReadOnly&quot; eller&quot;Acme_ReadOnly&quot;.

1. (Valfritt) [Skapa anpassade produktprofiler](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) med definierade behörighetsgrupper.

   Anpassade profiler är utöver de fyra standardproduktprofiler som redan är tillgängliga.

   Varje produktprofil för en organisation måste ha ett unikt namn. Om din organisation använder flera instanser av Search, Social och Commerce (till exempel Acme_US och Acme_JP) kan du inte duplicera ett produktprofilnamn i flera instanser. **Bästa tillvägagångssätt:** Använd namnkonventionen `<Name>_<Instance>,`, till exempel &quot;Simulations_Only_JP.&quot;

   **Varning!** Produktbehörigheter är mycket detaljerade. Var försiktig när du konfigurerar anpassade produktprofiler, annars kanske du utelämnar funktioner som du vill inkludera.

1. [Tilldela varje användare eller användargrupp till den relevanta produktprofilen](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manuellt eller gruppvis.

## Komplett handbok för användaradministration och ytterligare länkar

* Mer information om användaradministration med Adobe Admin Console finns i [Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html), inklusive [Admin Console overview](https://helpx.adobe.com/se/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
