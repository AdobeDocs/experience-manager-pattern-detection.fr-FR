---
title: CCOM
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

Composant personnalisé

## Arrière-plan {#background}

`CCOM` identifie les composants personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis aux fins de l&#39;évaluation des meilleures pratiques.

Un sous-type est utilisé avec ce code pour identifier la catégorie du composant :

* `custom.core`: Un supertype de la chaîne de supertypes du composant contient &quot;core/wcm/components/&quot;, ce qui indique qu&#39;il hérite d&#39;un composant principal.
* `custom.foundation`: Un supertype de la chaîne de supertypes du composant contient &quot;core/wcm/components/&quot;, ce qui indique qu&#39;il hérite d&#39;un composant principal.
* `custom.overlay.foundation`: Le chemin du composant contient &quot;wcm/foundation/components/&quot; ou &quot;foundation/components/&quot;, ce qui indique qu’il recouvre un composant de fondation.
* `custom`: Le composant personnalisé n’hérite ni ne superpose aucun composant de base ou de base.

## Incidences possibles et risques {#implications-and-risks}

* La meilleure pratique consiste à réduire au minimum le nombre de composants personnalisés, à exploiter les composants de base et à utiliser les composants de base avec le système de style pour réduire la dette technique.

## Solutions possibles {#solutions}

* Pour plus d&#39;informations sur les composants de base, consultez [Présentation des composants de base](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=fr).
* Pour plus d&#39;informations sur le système de style, consultez [Utilisation du système de style](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
