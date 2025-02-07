---
title: Beslutsträdets layout
description: Läs om beslutsträdets layout för upplevelser med målinriktning.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Beslutsträdeslayouten för [!DNL Creative] upplevelser

*Stängd beta*

När du aktiverar alternativet [!UICONTROL Targeting] för en upplevelse konfigurerar du upplevelsen med ett beslutsträd.

Inledningsvis börjar varje beslutsträd med rotnivån &quot;Alla&quot;. Du kan lägga till en eller flera målnoder och sedan tilldela kreativa paket till de sista noderna i varje gren av beslutsträdet.

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
—>

<!-- insert screen capture -->

## Villkor

**Träd:** Den övergripande beslutsstrukturen som ett träd med grenar.

**Målnod:** Ett mål inom en gren.

**Lövnod:** En uppsättning med kreativa alternativ som tilldelats en slutlig målnod.

## Målgrupper i ett beslutsträd

Varje beslutsträd kan ha upp till fem nivåer med mål. Varje målnivå kan innehålla flera grenar, där var och en har en eller flera noder med samma måltyp (målgruppssegment, geografisk platstyp, värden för angivna databassnycklar, attribut för en angiven återmarknadsföringspixel eller enhetskategori). Du kan tilldela kreativa paket i varje annonsstorlek som du har angett en standardbild som är kreativ till målnoderna på den lägsta nivån.

<!--insert screen capture -->

När du lägger till en målnod på den sista nivån anger du den nya nodens mål. En extra nod på samma nivå, &quot;Allt annat&quot;, skapas automatiskt för alla som inte matchar det angivna målet. Du kan sedan lägga till ytterligare noder på samma nivå med olika mål av samma typ.

När du infogar en målnod mellan befintliga nivåer tilldelas den första noden för den nya nivån till &quot;Alla&quot; från början. Om du vill identifiera ett specifikt mål skapar du en målnod på samma nivå, som du anger det faktiska målet för. Detta skapar målnoden och ersätter noden&quot;Alla&quot; med noden&quot;Allt annat&quot; (som innehåller alla kreativa paket som tidigare tilldelats till Alla). Du kan sedan lägga till ytterligare noder på samma nivå med olika mål av samma typ.

För alla överordnade noder kan du välja att kopiera alla underordnade målnoder och kreativa paket och klistra in dem i en annan nod på samma nivå, antingen lägga till dem i det befintliga ramverket eller ersätta det befintliga ramverket.

## Kreatörer i ett beslutsträd

Tilldela kreativa paket till varje målnod i upplevelsen.

Inom varje nod med kreativa paket kan du välja att rotera de medföljande kreativa delarna antingen enligt angivna vikter eller algoritmiskt för att optimera klickfrekvensen eller ett anpassat mål. Du kan också rotera kreatörerna i en viss tidssekvens med samma alternativ.

Du kan också anpassa landningssidans URL:er, visningsspårnings-URL:er och klickspårnings-URL:er efter behov för enskilda kreatörer. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Om upplevelser i Advertising Creative 2.0](experience-about.md)
