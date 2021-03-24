---
title: NBCC
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# NBCC {#nbcc}

Modifications non rétrocompatibles

## Arrière-plan {#background}

`NBCC` identifie la situation dans laquelle certains noeuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau.

## Incidences possibles et risques {#implications-and-risks}

* La fonctionnalité qui dépend de n&#39;importe quel composant qui utilise des modifications non rétrocompatibles peut être endommagée et peut ne pas être résolue correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

* Incrustation ou référence uniquement les composants Sling rétrocompatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau AEM.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
