---
title: OCU
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Utilisation du code obsolète

## Arrière-plan {#background}

`OCU` identifie la situation dans laquelle certains noeuds JCR, tels que Sling ou les composants AEM ou les exportations OSGi d’API, sont modifiés ou supprimés d’une manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout.

Comme les anciennes versions ne sont pas installées par défaut, l’application cliente risque de ne pas fonctionner correctement.

## Incidences possibles et risques {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des composants ou des API obsolètes peuvent être rompues et ne pas être résolues correctement après une mise à niveau.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement ou ne pas être principales après une mise à niveau.

## Solutions possibles {#solutions}

* À court terme : L&#39;installation du package de compatibilité peut vous aider.
* À long terme : Adaptez le code client pour utiliser la dernière version des composants ou API AEM.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
