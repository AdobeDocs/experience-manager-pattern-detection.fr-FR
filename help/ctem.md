---
title: CTEM
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: ht
source-wordcount: '140'
ht-degree: 100%

---


# CTEM {#ctem}

Modèle personnalisé

## Arrière-plan {#background}

`CTEM` identifie les modèles personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques.

Les modèles sont identifiés par une valeur principale de type « cq:Template ». Un sous-type est utilisé avec ce code pour identifier la catégorie du modèle :

* `custom.editable.template` : le chemin d’accès du modèle ne commence pas par « /apps ».
* `custom.static.template` : le chemin d’accès du modèle commence par « /apps ».

## Enjeux et risques possibles {#implications-and-risks}

* La bonne pratique consiste à changer tous les modèles statiques en modèles modifiables.

## Solutions possibles {#solutions}

* Tirez profit des [Outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/) pour migrer des modèles statiques vers des modèles modifiables.
* Pour plus d’informations sur les modèles modifiables, consultez [Modèles](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=fr).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
