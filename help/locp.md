---
title: LOCP
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# LOCP {#locp}

/libs Remplacement de packages personnalisés

## Arrière-plan {#background}

`LOCP` identifie la détection d’un package personnalisé qui livre du contenu à  `/libs`un format antimodèle (sauf dans le cas des ACL).

## Incidences possibles et risques {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour toute mise à niveau de CFP, SP ou AEM majeure.
* Dans certains cas, le nouveau contenu peut ne pas être correctement installé.

## Solutions possibles {#solutions}

* Les packs clients doivent déployer le contenu sur `/apps` au lieu de `/libs`.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
