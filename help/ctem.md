---
title: CTEM
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# CTEM {#ctem}

Modèle personnalisé

## Arrière-plan {#background}

`CTEM` identifie les modèles personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis aux fins de l&#39;évaluation des meilleures pratiques.

Les modèles sont identifiés par une Principale valeur de type &quot;cq:Template&quot;. Un sous-type est utilisé avec ce code pour identifier la catégorie du modèle :

* `custom.editable.template`: Le chemin d’accès du modèle n’est pas début avec &quot;/apps&quot;.
* `custom.static.template`: Chemin d’accès des débuts de modèle avec &quot;/apps&quot;.

## Incidences possibles et risques {#implications-and-risks}

* Il est recommandé de déplacer tous les modèles statiques vers des modèles modifiables.

## Solutions possibles {#solutions}

* Tirez parti des [outils de modernisation de l&#39;AEM](https://opensource.adobe.com/aem-modernize-tools/) pour migrer des modèles statiques vers des modèles modifiables.
* Pour plus d&#39;informations sur les modèles modifiables, consultez [Modèles](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
