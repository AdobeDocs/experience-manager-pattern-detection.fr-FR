---
title: PCX
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# PCX {#pcx}

Complexité de la page

## Arrière-plan {#background}

`PCX` identifie les pages qui contiennent un grand nombre de noeuds dans leur structure.

Les sous-types permettent d’identifier les différents types d’informations :

* `page.complexity.medium`: Une page contient un nombre de noeuds modérément élevé qui peut affecter les performances de rendu.
* `page.complexity.high`: Une page contient un nombre très élevé de noeuds qui affecteront probablement les performances de rendu.

## Incidences possibles et risques {#implications-and-risks}

* Un grand nombre de noeuds dans une page peut affecter ses performances de rendu.

## Solutions possibles {#solutions}

* Prenez des mesures pour réduire le nombre total de noeuds dans une page, notamment :
   * Vérifiez qu’il n’y a pas de conteneurs inutiles.
   * Vérifiez si la même mise en page peut être réalisée avec moins de conteneurs.
   * Simplifiez le contenu de la page.
   * Réduisez la profondeur de la structure des noeuds.
   * Pour simplifier, refacturez les fragments d’expérience inclus.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
