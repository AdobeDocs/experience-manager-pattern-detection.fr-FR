---
title: PCX
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '149'
ht-degree: 100%

---


# PCX {#pcx}

Page Complexity (complexité de la page)

## Arrière-plan {#background}

`PCX` identifie les pages qui contiennent un grand nombre de nœuds dans leur structure.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `page.complexity.medium` : une page contient un nombre de nœuds modérément élevé qui peut affecter les performances de rendu.
* `page.complexity.high` : une page contient un nombre très élevé de nœuds qui affecteront probablement les performances de rendu.

## Enjeux et risques possibles {#implications-and-risks}

* Un grand nombre de nœuds dans une page peut affecter ses performances de rendu.

## Solutions possibles {#solutions}

* Prenez des mesures pour réduire le nombre total de nœuds dans une page, notamment :
   * Vérifiez qu’il n’y a pas de conteneurs inutiles.
   * Testez si la même disposition peut être réalisée avec moins de conteneurs.
   * Simplifiez le contenu de la page.
   * Réduisez la profondeur de la structure des nœuds.
   * Pour simplifier, restructurez les fragments d’expérience inclus.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
