---
title: DOPI
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Index des propriétés triées obsolète

## Arrière-plan {#background}

`DOPI` identifie l&#39;utilisation de définitions d&#39;index de propriété ordonnées (`primaryType=oak:QueryIndexDefinition` ET  `type="ordered"`), qui ont été abandonnées depuis le 6.1 et ont été supprimées dans le 6.2.

## Incidences possibles et risques {#implications-and-risks}

* Certaines requêtes peuvent ne pas répondre.
* La fonctionnalité du client peut fonctionner incorrectement.
* Les avertissements de trafic ou même les erreurs et les sanctions de performances importantes comme les index obsolètes n&#39;ont aucun effet.

## Solutions possibles {#solutions}

* Modifiez la définition d’index pour qu’elle devienne, ou remplacez l’index par, une définition d’index prise en charge. (Voir [Requêtes en chêne et indexation](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) et comprenez comment [les violations DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) peuvent être corrigées et rendues compatibles avec AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
