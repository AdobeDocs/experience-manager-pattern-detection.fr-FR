---
title: DOPI
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '143'
ht-degree: 100%

---


# DOPI {#dopi}

Deprecated Ordered Property Index (index des propriétés organisées obsolète)

## Arrière-plan {#background}

`DOPI` identifie l’utilisation de définitions d’index de propriété organisées (`primaryType=oak:QueryIndexDefinition` ET `type="ordered"`), obsolètes depuis la version 6.1 et supprimées dans la version 6.2.

## Enjeux et risques possibles {#implications-and-risks}

* Certaines requêtes peuvent ne pas répondre.
* La fonctionnalité du client peut ne pas fonctionner correctement.
* Les avertissements transversaux ou même les erreurs et les sanctions de performances importantes comme les index obsolètes n’ont aucun effet.

## Solutions possibles {#solutions}

* Modifiez la définition d’index ou remplacez l’index par une définition d’index prise en charge. (Voir [Requêtes et indexation Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=fr)).
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) et découvrez comment [les violations DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
