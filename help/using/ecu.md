---
title: ECU
description: Page d’aide sur le code de détection des motifs.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '232'
ht-degree: 100%

---

# ECU {#ecu}

OBSOLÈTE : utilisation de contenu externe (remplacé par CAV, violation de zone de contenu)

## Contexte {#background}

`ECU` identifie le modèle dans lequel différentes zones de contenu sont utilisées d’une façon qui enfreint les règles de classification du contenu.

Le traitement des requêtes Sling définit la façon dont le contenu d’une ressource, en particulier sa propriété `sling:resourceType`, est utilisé pour déterminer le script à utiliser pour le rendu du contenu. (Voir [Localisation du script](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) pour plus d’informations). Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais des recouvrements et des remplacements. Ces techniques sont décrites comme faisant partie de [Sling Resource Merger](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) et des [recouvrements](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Pour permettre à la clientèle de mieux comprendre les zones de `/libs` qui peuvent être utilisées et recouvertes en toute sécurité, le contenu de `/libs` a été classé avec les propriétés « Mixin » :

* Public
* Résumé
* Final
* Interne

Chaque classification implique des règles sur la manière dont le contenu peut être utilisé, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) pour une description détaillée.

## Enjeux et risques possibles {#implications-and-risks}

* Une mise à niveau d’AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

* Réduisez l’utilisation de la superposition de contenu aux cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification Finale et Interne).
* Envisagez d’adapter les changements issus de `/libs` après les mises à niveau d’AEM, les installations du pack de services ou du pack de correctifs cumulatif.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
