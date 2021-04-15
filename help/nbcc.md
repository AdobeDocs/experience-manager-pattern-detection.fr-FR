---
title: NBCC
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '123'
ht-degree: 100%

---


# NBCC {#nbcc}

Non-Backwards Compatible Changes (modifications non rétrocompatibles)

## Arrière-plan {#background}

`NBCC` identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des modifications non rétrocompatibles peuvent être rompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

* Superposez ou référencez uniquement les composants Sling rétrocompatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau d’AEM.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
