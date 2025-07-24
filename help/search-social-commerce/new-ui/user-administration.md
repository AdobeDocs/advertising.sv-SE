---
title: Användaradministration
description: Lär dig hur du .
feature: Search Introduction
source-git-commit: ab6acc0ac777edb625b91a29464ca00a4407dcf1
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# (Nytt användargränssnitt) Användaradministration för sökning, sociala medier och handel

Vissa användare kan hantera åtkomsten till det nya användargränssnittet Sök, Sociala och Commerce med Adobe Admin Console, som är den centrala platsen för hantering av alla Adobe-berättiganden och användarhantering. Användare kategoriseras som antingen slutanvändare eller administratörer. Adobe-kontogruppen meddelar dig om du är administratör. Om du är administratör kan du läsa följande avsnitt för att identifiera dina behörigheter och arbetsflöden för att hantera användare.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Relevanta typer av administratörer

Admin Console har flera typer av administratörer, men endast följande administratörstyper och behörigheter är relevanta för Search, Social och Commerce.

**Systemadministratör:** Superanvändare för organisationen. En systemadministratör kan utföra alla administrativa uppgifter i Admin Console för organisationen och delegera administrativa funktioner till andra användare (produktadministratörer).&lt;!—, administratörer av produktprofiler och administratörer av användargrupper.  — Jag tror att det BARA är PRODUKTADMINISTRATÖRER FÖR OSS?  Verifiera. —>

**Produktadministratör:** Hanterar åtkomst till en viss [!DNL Adobe]-produkt (som Search, Social och Commerce) och användarnas rättigheter till den produkten. Produktadministratörer kan skapa produktprofiler för produkten, skapa (men inte ta bort) användare och användargrupper, lägga till eller ta bort användare och användargrupper från produktprofiler samt lägga till eller ta bort andra produktadministratörer från produkten.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Standardproduktprofiler

Produktprofiler, som liknar roller, ger användare specifika tjänster för en viss produkt.

Det nya användargränssnittet för sökning, sociala medier och handel har följande standardproduktprofiler, som innehåller olika deluppsättningar av funktioner och tjänster. Du kan inte redigera eller ta bort standardproduktprofilerna. Systemadministratörer kan dock vid behov skapa och hantera ytterligare produktprofiler med olika underuppsättningar behörigheter.

* **Grundläggande optimering:** Den här profilen har följande funktioner:

   * Mål: Fullständig åtkomst

   * Simuleringar: fullständig åtkomst

   * Portfolio Groups: fullständig åtkomst

   * Portföljer: Skapa/redigera åtkomst till portföljinställningar för mål, kampanjer och utgiftshantering, skrivskyddad åtkomst till de återstående portföljinställningarna.

   * Kampanjer: Skrivskyddad åtkomst till kampanjinställningar (inga funktioner för att skapa, redigera eller ta bort är tillgängliga); fullständig åtkomst till begränsnings- och portföljtilldelningar<!-- Is that the correct wording? -->

   * Annonsgrupper: Skrivskyddad åtkomst till inställningar för annonsgrupper (inga funktioner för att skapa, redigera eller ta bort är tillgängliga); fullständig åtkomst till begränsning- och portföljtilldelningar<!-- Is that the correct wording? -->

  Den här åtkomstnivån rekommenderas för användare som fortfarande håller på att lära sig att använda Search, Social och Commerce.

* **Expertoptimering:** Den här profilen har följande funktioner:

   * Mål: Fullständig åtkomst

   * Simuleringar: fullständig åtkomst

   * Portfolio Groups: fullständig åtkomst

   * Portföljer: Fullständig åtkomst

   * Kampanjer: Skrivskyddad åtkomst till kampanjlistan (det finns ännu inga funktioner för att skapa, redigera eller ta bort kampanjer); fullständig åtkomst till begränsningar och portföljtilldelningar<!-- Is that the correct wording? -->

   * Annonsgrupper: Skrivskyddad åtkomst till annonsgruppslistan (det finns ännu inga funktioner för att skapa, redigera eller ta bort kampanjer); fullständig åtkomst till begränsningar och portföljtilldelningar<!-- Is that the correct wording? -->

  Den här åtkomstnivån rekommenderas för expertanvändare av Search, Social och Commerce.

* **Skrivskyddad:** Den här profilen innehåller följande funktioner:

   * Mål: Skrivskyddad åtkomst

   * Simuleringar: skrivskyddad åtkomst

   * Portfolio-grupper: skrivskyddad åtkomst

   * Portföljer: skrivskyddad åtkomst

   * Kampanjer: skrivskyddad åtkomst

   * Annonsgrupper: skrivskyddad åtkomst

* **Admin:** Den här profilen ger fullständig åtkomst till alla funktioner som är tillgängliga och tillåter användare att skapa nya klientinstanser. Tilldela inte den här rättigheten till någon om du inte har en lämplig affärsjustering.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Uppgifter för administratörer

### Logga in på Adobe Admin Console och öppna det för att söka, socialt och Commerce

>[!PREREQUISITES]
>
>Du måste ha administratörsåtkomst&lt;!- vilket slags? Produktadministratör, systemadministratör, men jag är säker på att jag även kan göra det med administratör för produktprofiler eller användargrupper (som kan vara en intern grupp — bock) —> för att söka, socialt och Commerce.

1. Gå till https://adminconsole.adobe.com/enterprise/.

1. (Om du inte är inloggad på Experience Cloud) Logga in på Experience Cloud:

   1. Ange ditt [!DNL Adobe]-ID och klicka på **[!UICONTROL Continue]**.

   1. Välj antingen **[!UICONTROL Personal Account] eller **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Välj lämplig Experience Cloud-organisation.

   1. Klicka på [!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name] under Produkt och tjänster.

   Produktsidan öppnas som standard på fliken [!UICONTROL Product profiles] för Search, Social och Commerce. Ytterligare flikar är [!UICONTROL Users] och [!UICONTROL Product Admins].

### Arbetsflöde för systemadministratörer

1. [Logga in på Adobe Admin Console och öppna den för sökning, sociala medier och Commerce](#open-admin-console).

1. Delegera produkt- och användarhantering genom att [lägga till produktadministratörer](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Arbetsflöde för produktadministratörer

1. [Logga in på Adobe Admin Console och öppna den för sökning, sociala medier och Commerce](#open-admin-console).

1. Skapa slutanvändare [individuellt](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) eller [ gruppvis](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) efter behov.

1. (Valfritt) Skapa [användargrupper](https://helpx.adobe.com/enterprise/using/user-groups.html) för varje produktinstans och tilldela användare till varje användargrupp.

   Om instansen har många användare skapar du användargrupper som ser till att användarna tilldelas rätt profiler utifrån deras kunskapsnivå. (Se steg 4 för att tilldela användargrupper till produktprofiler.) Du kan skapa användargrupper baserat på verksamhetsområde, behov av användaråtkomst, datum för användaruthyrning eller andra kriterier.

   >[!IMPORTANT]
   >
   >Användargruppsnamn ska tydligt informera om vilka rättigheter gruppen med användare ska tilldelas. Om du till exempel vill skapa en användargrupp med behörigheten&quot;Skrivskyddad&quot; inkluderar du&quot;Skrivskyddad&quot; i användargruppens namn, till exempel&quot;Acme_Uk_ReadOnly&quot; eller&quot;Acme_ReadOnly&quot;.

1. (Valfritt) [Skapa anpassade produktprofiler](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) med definierade behörighetsgrupper.

   Anpassade profiler är utöver de fyra standardproduktprofiler som redan är tillgängliga.

   Varje produktprofil för en organisation måste ha ett unikt namn. Om din organisation använder flera instanser av Search, Social och Commerce (till exempel Acme_US och Acme_JP) kan du inte duplicera ett produktprofilnamn i flera instanser. **Bästa praxis:** Använd namnkonventionen<Name>_<Instance>, till exempel&quot;Simulations_Only_JP.&quot;

1. [Tilldela varje användare eller användargrupp till den relevanta produktprofilen](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manuellt eller gruppvis.

## Komplett handbok för användaradministration och ytterligare länkar

* Mer information om användaradministration med Adobe Admin Console finns i [Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html), inklusive [Admin Console overview](https://helpx.adobe.com/se/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
