---
title: LOCP
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '93'
ht-degree: 100%

---


# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Arrière-plan {#background}

`LOCP` identifie la détection d’un package personnalisé qui livre du contenu à `/libs`, qui est antimodèle (sauf dans le cas des ACL).

## Enjeux et risques possibles {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour tout Service Pack, pack de correctifs cumulés ou mise à niveau majeure d’AEM.
* Dans certains cas, le nouveau contenu peut ne pas s’installer correctement.

## Solutions possibles {#solutions}

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
