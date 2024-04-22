---
title: ECU
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 49%

---

# ECU {#ecu}

OBSOLÈTE : utilisation de contenu externe (remplacé par CAV, violation de zone de contenu)

## Contexte {#background}

L’UC identifie le modèle dans lequel différentes zones de contenu sont utilisées d’une manière qui viole les règles de la classification de contenu.

Le traitement des requêtes Sling définit la manière dont le contenu d’une ressource, sa `sling:resourceType` en particulier, est utilisée pour déterminer le script utilisé pour effectuer le rendu du contenu. (Voir [Localisation du script](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) pour plus d’informations.) Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais des superpositions et des remplacements. Ils sont décrits comme faisant partie de [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) et des [Superpositions](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Pour que les clients puissent comprendre plus facilement et plus en toute sécurité les zones d’ `/libs` peuvent utiliser et superposer le contenu en toute sécurité dans `/libs` a été classé avec des propriétés &quot;mixin&quot; : Public, Abstract, Final et Interne. Chaque classification implique des règles sur la manière dont le contenu peut être utilisé, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) pour une description détaillée.

## Enjeux et risques possibles {#implications-and-risks}

* Une mise à niveau d’AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

* Réduisez l’utilisation de la superposition de contenu aux cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification Finale et Interne).
* Envisagez d’adapter les changements issus de `/libs` après AEM mises à niveau, installations Service Pack ou Cumulative Fix Pack.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
