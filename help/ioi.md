---
title: IOI
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# IOI {#ioi}

Importation interne de chêne

## Arrière-plan {#background}

`IOI` identifie l&#39;utilisation par le client des packages Oak internes, en les important via OSGi. Ils sont généralement exportés sans aucune version particulière et ne sont destinés à la consommation que par d&#39;autres lots de chêne ou des services d&#39;AEM de bas niveau.

Certains d&#39;entre eux sont utilisés par `com.adobe.granite.repository`, qui installe un référentiel pour AEM au démarrage. Un autre exemple est le lot d&#39;Adobes `com.adobe.granite.maintenance.oak`, qui encapsule et fournit des tâches de maintenance Oak.

## Incidences possibles et risques {#implications-and-risks}

* Dans une future version AEM, les exportations internes pourraient être supprimées, ce qui provoquerait des dépendances brisées et des assemblages inactifs dépendant directement du chêne.
* L’API dans les exportations internes peut changer.

## Solutions possibles {#solutions}

* Utilisez l’API Ressource Sling (ou l’API JCR) au lieu d’un accès de bas niveau.
* Evitez de dépendre de packages internes qui ne font partie d’aucune API ou SPI publique.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.