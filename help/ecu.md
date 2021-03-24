---
title: ECU
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# Écus {#ecu}

DÉCONSEILLÉ : Utilisation de contenu externe (remplacée par le format CAV, Violation de zone de contenu)

## Arrière-plan {#background}

`ECU` identifie le modèle selon lequel différentes zones de contenu sont utilisées de manière à violer les règles de la classification de contenu.

Le traitement des requêtes Sling définit comment le contenu d&#39;une ressource, en particulier sa propriété `sling:resourceType`, est utilisé pour déterminer le script à utiliser pour le rendu du contenu. (Voir [Localisation du script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) pour plus d’informations.) Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais de &quot;Overlays&quot; et de &quot;Overrides&quot;. Ils sont décrits comme faisant partie de la [fusion de ressources Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) et dans [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Afin de rendre plus sûr et plus facile pour les clients de comprendre quelles zones de `/libs` peuvent être utilisées en toute sécurité et de superposer le contenu dans `/libs` a été classé avec des propriétés de &quot;mixin&quot; : Public, Extrait, Final et Interne. Chaque classification implique des règles sur la manière dont le contenu peut être utilisateur, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) pour une description détaillée.

## Incidences possibles et risques {#implications-and-risks}

* Une mise à niveau AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

* Réduisez l’utilisation de l’incrustation de contenu en fonction des cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification finale et interne).
* Envisagez d&#39;adapter les modifications provenant de `/libs` après AEM mises à niveau, des installations ServicePack ou CumulativeFixPack.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
