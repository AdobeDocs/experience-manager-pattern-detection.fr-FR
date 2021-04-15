---
title: OCU
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---


# OCU {#ocu}

Outdated Code Usage (utilisation de code obsolète)

## Arrière-plan {#background}

`OCU` identifie la situation dans laquelle certains nœuds JCR, tels que Sling ou les composants AEM ou les exportations OSGi de l’API, sont modifiés ou supprimés d’une manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout.

Comme les anciennes versions ne sont pas installées par défaut, l’application cliente risque de ne pas fonctionner correctement.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des composants ou des API obsolètes peuvent être rompues et ne pas être résolues correctement après une mise à niveau.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement ou ne pas être actives après une mise à niveau.

## Solutions possibles {#solutions}

* À court terme : l’installation du package de compatibilité peut vous aider.
* À long terme : adaptez le code client pour utiliser la dernière version des composants ou API AEM.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
