---
title: ECU
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '264'
ht-degree: 100%

---


# ECU {#ecu}

OBSOLÈTE : utilisation de contenu externe (remplacé par CAV, violation de zone de contenu)

## Arrière-plan {#background}

`ECU` identifie le modèle selon lequel différentes zones de contenu sont utilisées d’une façon qui enfreint les règles de la classification de contenu.

Le traitement des requêtes Sling définit la façon dont le contenu d’une ressource, en particulier sa propriété `sling:resourceType`, est utilisé pour déterminer le script à utiliser pour le rendu du contenu. (Voir [Localisation du script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=fr#locating-the-script) pour plus d’informations.) Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais des superpositions et des remplacements. Ils sont décrits comme faisant partie de [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=fr) et des [Superpositions](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=fr).

Pour permettre aux utilisateurs de mieux comprendre les zones de `/libs` qui peuvent être utilisées et superposées en toute sécurité, le contenu de `/libs` a été classé avec les propriétés « Mixin » : Public, Abstract (Résumé), Final et Internal (Interne). Chaque classification implique des règles sur la manière dont le contenu peut être utilisé, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=fr) pour une description détaillée.

## Enjeux et risques possibles {#implications-and-risks}

* Une mise à niveau d’AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

* Réduisez l’utilisation de la superposition de contenu aux cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification Finale et Interne).
* Envisagez d’adapter les modifications provenant de `/libs` après les mises à niveau d’AEM, ou les installations des Service Packs ou packs de correctifs cumulés.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
