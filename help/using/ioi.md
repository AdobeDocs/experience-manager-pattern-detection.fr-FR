---
title: IOI
description: Page d’aide sur le code de détection des motifs.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 78%

---

# IOI {#ioi}

Internal Oak Import (import Oak interne)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import (import Oak interne)"
>abstract="Le code IOI identifie l’utilisation par le client ou la cliente de packages Oak internes, en les important par OSGi. Ils sont exportés sans version particulière. Les lots Oak ou les services AEM de bas niveau utilisent uniquement ces packages."

`IOI` identifie l’utilisation par le client ou la cliente de packages Oak internes, en les important via OSGi. Ils sont exportés sans version particulière. Les lots Oak ou les services AEM de bas niveau les utilisent uniquement.
Certaines de ces zones sont utilisées par `com.adobe.granite.repository`, qui configure un référentiel pour AEM au démarrage. Un autre exemple est le lot Adobe `com.adobe.granite.maintenance.oak`, qui englobe et fournit des tâches de maintenance Oak.

## Enjeux et risques possibles {#implications-and-risks}

* Dans une version d’AEM ultérieure, les exportations internes peuvent être supprimées, ce qui entraîne des dépendances rompues et des lots inactifs en fonction directement d’Oak.
* L’API dans les exportations internes peut changer.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients doivent passer en revue leur code personnalisé pour identifier l’utilisation de ces API et les modifier de telle manière à les rendre compatibles avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez l’API Sling Resource (ou l’API JCR) au lieu d’un accès de bas niveau.
* Évitez de dépendre de packages internes qui ne font partie d’aucune API ou SPI publique.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
