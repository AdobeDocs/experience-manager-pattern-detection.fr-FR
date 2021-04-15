---
title: IOI
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '152'
ht-degree: 100%

---


# IOI {#ioi}

Internal Oak Import (importation Oak interne)

## Arrière-plan {#background}

`IOI` identifie l’utilisation par le client de packages Oak internes, en les important via OSGi. Ils sont généralement exportés sans aucune version particulière et sont uniquement destinés à une consommation par d’autres lots Oak ou des services AEM de bas niveau.

Certains d’entre eux sont utilisés par `com.adobe.granite.repository`, qui installe un référentiel pour AEM au démarrage. Un autre exemple est le lot Adobe `com.adobe.granite.maintenance.oak`, qui englobe et fournit des tâches de maintenance Oak.

## Enjeux et risques possibles {#implications-and-risks}

* Dans une future version d’AEM, les exportations internes pourraient être supprimées, ce qui provoquerait des problèmes de dépendances brisées et des lots inactifs dépendant directement d’Oak.
* L’API dans les exportations internes peut changer.

## Solutions possibles {#solutions}

* Utilisez l’API Sling Resource (ou l’API JCR) au lieu d’un accès de bas niveau.
* Évitez de dépendre de packages internes qui ne font partie d’aucune API ou SPI publique.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.