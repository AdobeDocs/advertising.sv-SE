---
title: Beslutsträdets layout
description: Läs om beslutsträdets layout för upplevelser med målinriktning.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 4057f413b58343580a965f9a419af1e002892ff6
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Beslutsträdeslayouten för [!DNL Creative] upplevelser

När du aktiverar alternativet [!UICONTROL Targeting] för en upplevelse konfigurerar du upplevelsen med ett beslutsträd.

Inledningsvis börjar varje beslutsträd med rotnivån &quot;Alla&quot;. Du kan lägga till en eller flera målnoder och sedan tilldela kreativa paket till de sista noderna i varje gren av beslutsträdet. Beslutsträdet visas som standard lodrätt, men du kan välja att visa trädet vågrätt i stället.

![Exempel på ett lodrätt beslutsträd utan mål](/help/creative/assets/experience-decision-tree-no-targets.png "Exempel på ett lodrätt beslutsträd utan mål")

![Exempel på ett vågrätt beslutsträd utan mål](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Exempel på ett vågrätt beslutsträd utan mål")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>—>

## Villkor

**Träd:** Den övergripande beslutsstrukturen som ett träd med grenar.

**Målnod:** Ett mål inom en gren.

**Lövnod:** En uppsättning med kreativa alternativ som tilldelats en slutlig målnod.

## Målgrupper i ett beslutsträd

Varje beslutsträd kan ha upp till fem nivåer med mål. Målen på erfarenhetsnivå tillämpas tillsammans med DSP alternativ för målinriktning. Det hierarkiska beteendet för målinriktning kan variera mellan DSP. Se till att era annonsupplevelser omfattar målgruppsanpassning som är kompatibel med de kampanjer ni ska implementera den i.

Varje målnivå kan innehålla flera grenar, där var och en har en eller flera noder med samma måltyp (målgruppssegment, geografisk platstyp, värden för angivna databassnycklar, attribut för en angiven återmarknadsföringspixel eller enhetskategori). Du kan tilldela kreativa paket i varje annonsstorlek som du har angett en standardbild som kreativ eller videoredigerad till målnoderna på den lägsta nivån.

![Exempel på ett beslutsträd med mål](/help/creative/assets/experience-decision-tree.png "Exempel på ett beslutsträd med mål")

När du lägger till en målnod på den sista nivån anger du den nya nodens mål. En extra nod på samma nivå, &quot;Allt annat&quot;, skapas automatiskt för alla som inte matchar det angivna målet. Du kan sedan lägga till ytterligare noder på samma nivå med olika mål av samma typ.

När du infogar en målnod mellan befintliga nivåer tilldelas den första noden för den nya nivån till &quot;Alla&quot; från början. Om du vill identifiera ett specifikt mål skapar du en målnod på samma nivå, som du anger det faktiska målet för. Den här åtgärden skapar målnoden och ersätter noden&quot;Alla&quot; med noden&quot;Allt annat&quot; (som innehåller alla kreativa paket som tidigare tilldelats till Alla). Du kan sedan lägga till ytterligare noder på samma nivå med olika mål av samma typ.

För alla överordnade noder kan du även kopiera alla underordnade målnoder och kreativa paket och klistra in dem i en annan nod på samma nivå. Du kan antingen lägga till de inklistrade noderna i det befintliga ramverket eller ersätta det befintliga ramverket med dem.

## Kreatörer i ett beslutsträd

Tilldela kreativa paket till varje målnod i upplevelsen.

I varje nod med kreativa paket kan du rotera de medföljande kreativa (a) algoritmiskt för att optimera klickfrekvensen eller ett anpassat mål, (b) enligt angivna vikter, eller (c) i en viss sekvens. Du kan också rotera kreatörerna i en viss tidssekvens om du vill.

Du kan också anpassa landningssidans URL:er, visningsspårnings-URL:er och klickspårnings-URL:er efter behov för enskilda kreatörer. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Om upplevelser i Advertising Creative 2.0](experience-about.md)
>* [Skapa en upplevelse med målinriktning](/help/creative/experiences/experience-create-targeting.md)
>* [Inställningar för anpassad upplevelse](/help/creative/experiences/experience-settings-targeting.md)
